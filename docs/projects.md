---
layout: single
title: "Projects"
author_profile: true
permalink: /projects/
---

<div id="projects"></div>

<style>
    .project-card {
        border: 1px solid #ddd;
        padding: 20px;
        margin-bottom: 20px;
        border-radius: 8px;
        transition: box-shadow 0.2s;
    }
    .project-card:hover {
        box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    .project-card h3 {
        margin-top: 0;
    }
    .project-link {
        display: inline-block;
        margin-top: 10px;
        padding: 8px 16px;
        background: #0079b8;
        color: white;
        border-radius: 4px;
        text-decoration: none;
    }
    .project-link:hover {
        background: #005f8e;
        color: white;
    }
    .project-language {
        display: inline-block;
        padding: 2px 8px;
        background: #f1f1f1;
        border-radius: 12px;
        font-size: 0.8em;
        margin-bottom: 8px;

    .project-image {
        width: 100%;
        height: 180px;
        object-fit: cover;
        border-radius: 4px;
        margin-bottom: 15px;
        background: #eee;
    }
    }
</style>

<script>
    fetch("https://api.github.com/users/yessamno/repos?sort=updated&per_page=20")
        .then(res => res.json())
        .then(repos => {
            const container = document.getElementById("projects");
            repos
                .filter(repo => !repo.fork)
                .forEach(repo => {
                    const socialPreviewCard = `https://opengraph.githubassets.com/1/${repo.full_name}`;
                    container.innerHTML += `
          <div class="project-card">
            <img src="${socialPreviewCard}" alt="${repo.name} preview" style="width:100%; border-radius:4px; margin-bottom:15px;">
            <h3>${repo.name}</h3>
            ${repo.language ? `<span class="project-language">${repo.language}</span>` : ""}
            <p>${repo.description || "No description provided."}</p>
            <a class="project-link" href="${repo.html_url}" target="_blank">View on GitHub</a>
          </div>`;
                });
        })
        .catch(() => {
            document.getElementById("projects").innerHTML = "<p>Could not load projects. Please try again later.</p>";
        });
</script>