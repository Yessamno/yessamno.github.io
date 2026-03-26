---
title: "About"
author_profile: true
---
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Me - Timeline</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        terracotta: '#D97D55',
                        cream: '#F4E9D7',
                        sage: '#B8C4A9',
                        teal: '#6FA4AF',
                    }
                }
            }
        }
    </script>
    <style>
        /* Timeline vertical line */
        .timeline-line {
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 4px;
            height: 100%;
            background: linear-gradient(to bottom, #6FA4AF, #B8C4A9, #D97D55);
            z-index: 0;
        }
        .timeline-dot {
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 20px;
            height: 20px;
            background-color: #D97D55;
            border: 4px solid #F4E9D7;
            border-radius: 50%;
            z-index: 10;
            box-shadow: 0 0 0 4px #6FA4AF;
        }
        /* Animation */
        .timeline-item {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease-out;
        }
        .timeline-item.visible {
            opacity: 1;
            transform: translateY(0);
        }
        /* Mobile responsiveness for timeline */
        @media (max-width: 768px) {
            .timeline-line {
                left: 30px;
            }
            .timeline-dot {
                left: 30px;
            }
        }
        /* Smooth scrolling */
        html {
            scroll-behavior: smooth;
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        /*::-webkit-scrollbar-track {*/
        /*    background: #F4E9D7;*/
        /*}*/
        ::-webkit-scrollbar-thumb {
            background: #D97D55;
            border-radius: 5px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #6FA4AF;
        }
    </style>
</head>
<body class="bg-cream text-gray-800 font-sans antialiased">
    <!-- Hero Section -->
    <section class="pt-32 pb-16 px-6 max-w-6xl mx-auto">
        <div class="bg-white rounded-3xl shadow-xl overflow-hidden border-2 border-sage/30">
            <div class="flex flex-col md:flex-row">
                <!-- Portrait Image Left -->
                <div class="md:w-2/5 relative overflow-hidden bg-sage/20">
                    <div class="aspect-[3/4] md:aspect-auto md:h-full relative">
                        <img src="assets/images/firstpic.jpg"
                             class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" alt="">
                        <div class="absolute inset-0 bg-gradient-to-t from-terracotta/20 to-transparent"></div>
                    </div>
                </div>
                <!-- Text Content Right -->
                <div class="md:w-3/5 p-8 md:p-12 flex flex-col justify-center bg-cream">
                    <div class="inline-flex items-center gap-2 text-terracotta font-semibold mb-4">
                        <i data-lucide="user" class="w-5 h-5"></i>
                        <span>About Me</span>
                    </div>
                    <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-6 leading-tight">
                        Hello, I'm <span class="text-terracotta">Saifeldeen</span>
                    </h1>
                    <p class="text-lg text-gray-700 mb-6 leading-relaxed">
                        I'm a creative developer and designer with a passion for building beautiful, functional experiences. 
                        This timeline represents my journey, skills, and the moments that shaped my career.
                    </p>
                    <div class="flex flex-wrap gap-3 mb-6">
                        <span class="px-4 py-2 bg-sage/30 text-teal rounded-full text-sm font-medium">Developer</span>
                        <span class="px-4 py-2 bg-terracotta/20 text-terracotta rounded-full text-sm font-medium">Designer</span>
                        <span class="px-4 py-2 bg-teal/20 text-teal rounded-full text-sm font-medium">Creator</span>
                    </div>
                    <div class="flex gap-4">
                        <a href="#timeline" class="inline-flex items-center gap-2 px-6 py-3 bg-terracotta text-white rounded-full hover:bg-terracotta/90 transition-all shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                            <span>Explore Timeline</span>
                            <i data-lucide="arrow-down" class="w-4 h-4"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Timeline Section -->
    <section id="timeline" class="py-16 px-6 max-w-6xl mx-auto relative">
        <div class="text-center mb-16">
            <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">My Journey</h2>
            <div class="w-24 h-1 bg-terracotta mx-auto rounded-full"></div>
        </div>
        <div class="relative">
            <!-- Vertical Line -->
            <div class="timeline-line"></div>
            <!-- Timeline Item 1: Landscape Image (Left text, Right image) -->
            <div class="timeline-item relative mb-16 md:mb-24">
                <div class="timeline-dot top-8"></div>
                <div class="grid md:grid-cols-2 gap-8 items-center">
                    <!-- Text Side -->
                    <div class="md:text-right md:pr-12 order-2 md:order-1">
                        <div class="bg-white p-6 rounded-2xl shadow-lg border-l-4 border-terracotta md:border-l-0 md:border-r-4">
                            <span class="text-terracotta font-bold text-sm uppercase tracking-wider">2024 - Present</span>
                            <h3 class="text-2xl font-bold text-gray-900 mt-2 mb-3">Senior Developer</h3>
                            <p class="text-gray-600 leading-relaxed">
                                Leading development teams and architecting scalable solutions. 
                                Currently focused on full-stack applications and modern web technologies.
                            </p>
                            <div class="mt-4 flex md:justify-end gap-2">
                                <span class="w-2 h-2 bg-teal rounded-full"></span>
                                <span class="w-2 h-2 bg-sage rounded-full"></span>
                                <span class="w-2 h-2 bg-terracotta rounded-full"></span>
                            </div>
                        </div>
                    </div>
                    <!-- Image Side - Landscape -->
                    <div class="md:pl-12 order-1 md:order-2">
                        <div class="relative group">
                            <div class="absolute -inset-2 bg-gradient-to-r from-teal to-sage rounded-2xl blur opacity-20 group-hover:opacity-40 transition-opacity"></div>
                            <img src="http://static.photos/technology/1024x576/456" 
                                 alt="Current Work" 
                                 class="relative w-full aspect-video object-cover rounded-2xl shadow-lg group-hover:scale-[1.02] transition-transform duration-500">
                            <div class="absolute bottom-4 left-4 bg-white/90 backdrop-blur px-4 py-2 rounded-full text-sm font-medium text-terracotta">
                                <i data-lucide="briefcase" class="w-4 h-4 inline mr-1"></i>
                                Current Role
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Timeline Item 2: Portrait Image (Left image, Right text) -->
            <div class="timeline-item relative mb-16 md:mb-24">
                <div class="timeline-dot top-8"></div>
                <div class="grid md:grid-cols-2 gap-8 items-center">
                    <!-- Image Side - Portrait -->
                    <div class="md:pr-12">
                        <div class="relative group max-w-sm mx-auto md:mx-0 md:ml-auto">
                            <div class="absolute -inset-2 bg-gradient-to-r from-terracotta to-sage rounded-2xl blur opacity-20 group-hover:opacity-40 transition-opacity"></div>
                            <img src="http://static.photos/workspace/640x800/789" 
                                 alt="Design Work" 
                                 class="relative w-full aspect-[3/4] object-cover rounded-2xl shadow-lg group-hover:scale-[1.02] transition-transform duration-500">
                            <div class="absolute top-4 right-4 bg-white/90 backdrop-blur px-4 py-2 rounded-full text-sm font-medium text-teal">
                                <i data-lucide="palette" class="w-4 h-4 inline mr-1"></i>
                                Design Phase
                            </div>
                        </div>
                    </div>
                    <!-- Text Side -->
                    <div class="md:pl-12">
                        <div class="bg-white p-6 rounded-2xl shadow-lg border-l-4 border-teal">
                            <span class="text-teal font-bold text-sm uppercase tracking-wider">2022 - 2024</span>
                            <h3 class="text-2xl font-bold text-gray-900 mt-2 mb-3">UI/UX Designer</h3>
                            <p class="text-gray-600 leading-relaxed">
                                Transitioned into design, creating user-centered interfaces and design systems.
                                Collaborated with cross-functional teams to deliver exceptional user experiences.
                            </p>
                            <div class="mt-4 flex gap-2">
                                <span class="w-2 h-2 bg-terracotta rounded-full"></span>
                                <span class="w-2 h-2 bg-sage rounded-full"></span>
                                <span class="w-2 h-2 bg-teal rounded-full"></span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Timeline Item 3: Landscape Image (Left text, Right image) -->
            <div class="timeline-item relative mb-16 md:mb-24">
                <div class="timeline-dot top-8"></div>
                <div class="grid md:grid-cols-2 gap-8 items-center">
                    <!-- Text Side -->
                    <div class="md:text-right md:pr-12 order-2 md:order-1">
                        <div class="bg-white p-6 rounded-2xl shadow-lg border-l-4 border-sage md:border-l-0 md:border-r-4">
                            <span class="text-sage font-bold text-sm uppercase tracking-wider">2020 - 2022</span>
                            <h3 class="text-2xl font-bold text-gray-900 mt-2 mb-3">Frontend Developer</h3>
                            <p class="text-gray-600 leading-relaxed">
                                Specialized in React and modern JavaScript frameworks. Built responsive,
                                accessible web applications for various clients and industries.
                            </p>
                            <div class="mt-4 flex md:justify-end gap-2">
                                <span class="w-2 h-2 bg-teal rounded-full"></span>
                                <span class="w-2 h-2 bg-terracotta rounded-full"></span>
                                <span class="w-2 h-2 bg-sage rounded-full"></span>
                            </div>
                        </div>
                    </div>
                    <!-- Image Side - Landscape -->
                    <div class="md:pl-12 order-1 md:order-2">
                        <div class="relative group">
                            <div class="absolute -inset-2 bg-gradient-to-r from-sage to-terracotta rounded-2xl blur opacity-20 group-hover:opacity-40 transition-opacity"></div>
                            <img src="http://static.photos/office/1024x576/321" 
                                 alt="Coding Setup" 
                                 class="relative w-full aspect-video object-cover rounded-2xl shadow-lg group-hover:scale-[1.02] transition-transform duration-500">
                            <div class="absolute bottom-4 left-4 bg-white/90 backdrop-blur px-4 py-2 rounded-full text-sm font-medium text-sage">
                                <i data-lucide="code" class="w-4 h-4 inline mr-1"></i>
                                Development
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            # <!-- Timeline Item 4: Portrait Image (Left image, Right text) -->
            <div class="timeline-item relative mb-16 md:mb-24">
                <div class="timeline-dot top-8"></div>
                <div class="grid md:grid-cols-2 gap-8 items-center">
                    <!-- Image Side - Portrait -->
                    <div class="md:pr-12">
                        <div class="relative group max-w-sm mx-auto md:mx-0 md:ml-auto">
                            <div class="absolute -inset-2 bg-gradient-to-r from-teal to-terracotta rounded-2xl blur opacity-20 group-hover:opacity-40 transition-opacity"></div>
                            <img src="http://static.photos/education/640x800/654" 
                                 alt="Education" 
                                 class="relative w-full aspect-[3/4] object-cover rounded-2xl shadow-lg group-hover:scale-[1.02] transition-transform duration-500">
                            <div class="absolute top-4 right-4 bg-white/90 backdrop-blur px-4 py-2 rounded-full text-sm font-medium text-terracotta">
                                <i data-lucide="graduation-cap" class="w-4 h-4 inline mr-1"></i>
                                Learning
                            </div>
                        </div>
                    </div>
                    <!-- Text Side -->
                    <div class="md:pl-12">
                        <div class="bg-white p-6 rounded-2xl shadow-lg border-l-4 border-terracotta">
                            <span class="text-terracotta font-bold text-sm uppercase tracking-wider">2018 - 2020</span>
                            <h3 class="text-2xl font-bold text-gray-900 mt-2 mb-3">Computer Science Degree</h3>
                            <p class="text-gray-600 leading-relaxed">
                                Earned my Bachelor's degree with honors. Focused on web technologies,
                                algorithms, and software engineering principles.
                            </p>
                            <div class="mt-4 flex gap-2">
                                <span class="w-2 h-2 bg-sage rounded-full"></span>
                                <span class="w-2 h-2 bg-teal rounded-full"></span>
                                <span class="w-2 h-2 bg-terracotta rounded-full"></span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
<!-- Timeline Item 5: Landscape Image &#40;Left text, Right image&#41; -->)
            <div class="timeline-item relative mb-16">
                <div class="timeline-dot top-8"></div>
                <div class="grid md:grid-cols-2 gap-8 items-center">
                    <!-- Text Side -->
                    <div class="md:text-right md:pr-12 order-2 md:order-1">
                        <div class="bg-white p-6 rounded-2xl shadow-lg border-l-4 border-teal md:border-l-0 md:border-r-4">
                            <span class="text-teal font-bold text-sm uppercase tracking-wider">2016 - 2018</span>
                            <h3 class="text-2xl font-bold text-gray-900 mt-2 mb-3">First Code</h3>
                            <p class="text-gray-600 leading-relaxed">
                                Wrote my first "Hello World" and fell in love with programming.
                                Started with HTML/CSS and quickly moved into JavaScript and beyond.
                            </p>
                            <div class="mt-4 flex md:justify-end gap-2">
                                <span class="w-2 h-2 bg-terracotta rounded-full"></span>
                                <span class="w-2 h-2 bg-sage rounded-full"></span>
                                <span class="w-2 h-2 bg-teal rounded-full"></span>
                            </div>
                        </div>
                    </div>
                    <!-- Image Side - Landscape -->
                    <div class="md:pl-12 order-1 md:order-2">
                        <div class="relative group">
                            <div class="absolute -inset-2 bg-gradient-to-r from-terracotta to-teal rounded-2xl blur opacity-20 group-hover:opacity-40 transition-opacity"></div>
                            <img src="http://static.photos/minimal/1024x576/987" 
                                 alt="First Steps" 
                                 class="relative w-full aspect-video object-cover rounded-2xl shadow-lg group-hover:scale-[1.02] transition-transform duration-500">
                            <div class="absolute bottom-4 left-4 bg-white/90 backdrop-blur px-4 py-2 rounded-full text-sm font-medium text-teal">
                                <i data-lucide="rocket" class="w-4 h-4 inline mr-1"></i>
                                Beginning
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Footer -->
    <footer class="bg-white border-t-2 border-sage/30 mt-16 py-12 px-6">
        <div class="max-w-6xl mx-auto text-center">
            <div class="flex justify-center gap-6 mb-6">
                <a href="#" class="w-10 h-10 rounded-full bg-cream flex items-center justify-center text-terracotta hover:bg-terracotta hover:text-white transition-all">
                    <i data-lucide="github" class="w-5 h-5"></i>
                </a>
                <a href="#" class="w-10 h-10 rounded-full bg-cream flex items-center justify-center text-teal hover:bg-teal hover:text-white transition-all">
                    <i data-lucide="linkedin" class="w-5 h-5"></i>
                </a>
                <a href="#" class="w-10 h-10 rounded-full bg-cream flex items-center justify-center text-sage hover:bg-sage hover:text-white transition-all">
                    <i data-lucide="twitter" class="w-5 h-5"></i>
                </a>
                <a href="#" class="w-10 h-10 rounded-full bg-cream flex items-center justify-center text-terracotta hover:bg-terracotta hover:text-white transition-all">
                    <i data-lucide="mail" class="w-5 h-5"></i>
                </a>
            </div>
            <p class="text-gray-600">&copy; 2024 Your Name. Built with passion and code.</p>
        </div>
    </footer>
    <script>
        // Initialize Lucide icons
        lucide.createIcons();
        // Intersection Observer for scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);
        // Observe all timeline items
        document.querySelectorAll('.timeline-item').forEach(item => {
            observer.observe(item);
        });
        // Add parallax effect to hero image
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const heroImage = document.querySelector('img[alt="Portrait"]');
            if (heroImage && scrolled < 600) {
                heroImage.style.transform = `translateY(${scrolled * 0.5}px) scale(${1 + scrolled * 0.0005})`;
            }
        });
    </script>
</body>



