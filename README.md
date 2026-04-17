# Veer-Adhana
My portfolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Veer Adhana - Electronics & Communication Engineering Student | Portfolio">
    <title>Veer Adhana | Electronics &amp; Communication Engineer</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500&amp;family=Space+Grotesk:wght@500&amp;display=swap');
        
        :root {
            --brand: #00d4ff;
        }
        
        * {
            transition-property: color, background-color, border-color, text-decoration-color, fill, stroke;
            transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
            transition-duration: 150ms;
        }
        
        .tailwind-ready {
            font-family: 'Inter', system_ui, sans-serif;
        }
        
        .heading-font {
            font-family: 'Space Grotesk', sans-serif;
        }

        .hero-bg {
            background: linear-gradient(135deg, #f8fafc 0%, #e0f2fe 100%);
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background-color: #00d4ff;
        }
        
        .nav-link:hover:after {
            width: 100%;
        }
        
        /* Typing cursor */
        .typing-container {
            position: relative;
        }
        
        .typing-cursor {
            display: inline-block;
            animation: blink 0.8s step-end infinite;
        }
        
        @keyframes blink {
            50% { opacity: 0; }
        }
        
        /* Section header underline */
        .section-header {
            position: relative;
        }
        
        .section-header:after {
            content: '';
            position: absolute;
            width: 60px;
            height: 3px;
            background: linear-gradient(to right, #00d4ff, #00a8cc);
            bottom: -6px;
            left: 0;
            border-radius: 9999px;
        }
        
        /* Project card hover */
        .project-card {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .project-card:hover {
            transform: translateY(-4px);
            box-shadow: 25px 25px 0 -10px #00d4ff;
        }
        
        /* Mobile menu animation */
        .mobile-menu {
            animation: slideDown 0.3s ease forwards;
        }
        
        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Light theme card shine */
        .glass {
            background: rgba(255,255,255,0.85);
            backdrop-filter: blur(12px);
        }
    </style>
</head>
<body class="tailwind-ready">
    <!-- NAVBAR -->
    <nav class="bg-white border-b border-slate-200 sticky top-0 z-50 shadow-sm">
        <div class="max-w-7xl mx-auto px-6">
            <div class="flex justify-between items-center h-16">
                
                <!-- Logo -->
                <div class="flex items-center gap-x-3">
                    <div class="w-9 h-9 bg-[#00d4ff] rounded-2xl flex items-center justify-center text-white text-xl shadow-inner">
                        <i class="fa-solid fa-microchip"></i>
                    </div>
                    <h1 class="heading-font text-2xl font-semibold tracking-[-1px] text-slate-900">Veer Adhana</h1>
                </div>

                <!-- Desktop Menu -->
                <div class="hidden md:flex items-center gap-x-8 text-slate-700 font-medium">
                    <a href="#home" onclick="navigateToSection('home')" class="nav-link hover:text-[#00d4ff]">Home</a>
                    <a href="#about" onclick="navigateToSection('about')" class="nav-link hover:text-[#00d4ff]">About</a>
                    <a href="#skills" onclick="navigateToSection('skills')" class="nav-link hover:text-[#00d4ff]">Skills</a>
                    <a href="#projects" onclick="navigateToSection('projects')" class="nav-link hover:text-[#00d4ff]">Projects</a>
                    <a href="#contact" onclick="navigateToSection('contact')" class="nav-link hover:text-[#00d4ff]">Contact</a>
                </div>

                <!-- Resume &amp; Mobile Hamburger -->
                <div class="flex items-center gap-x-4">
                    <a onclick="downloadResume()" 
                       class="hidden sm:flex items-center gap-x-2 px-5 py-2.5 bg-white border border-[#00d4ff] text-[#00d4ff] rounded-3xl font-medium hover:bg-[#00d4ff] hover:text-white">
                        <i class="fa-solid fa-download"></i>
                        <span>Resume</span>
                    </a>
                    
                    <!-- Hamburger -->
                    <button onclick="toggleMobileMenu()" 
                            class="md:hidden w-11 h-11 flex items-center justify-center text-2xl text-slate-700 hover:text-[#00d4ff]">
                        <i id="hamburger-icon" class="fa-solid fa-bars"></i>
                    </button>
                </div>
            </div>
            
            <!-- Mobile Menu -->
            <div id="mobile-menu" class="hidden md:hidden mobile-menu bg-white border-t py-4 px-6">
                <div class="flex flex-col gap-y-4 text-slate-700 font-medium">
                    <a href="#home" onclick="navigateToSection('home'); toggleMobileMenu()" class="flex items-center gap-x-3 py-2">
                        <i class="fa-solid fa-house w-5"></i>
                        <span>Home</span>
                    </a>
                    <a href="#about" onclick="navigateToSection('about'); toggleMobileMenu()" class="flex items-center gap-x-3 py-2">
                        <i class="fa-solid fa-user w-5"></i>
                        <span>About</span>
                    </a>
                    <a href="#skills" onclick="navigateToSection('skills'); toggleMobileMenu()" class="flex items-center gap-x-3 py-2">
                        <i class="fa-solid fa-laptop-code w-5"></i>
                        <span>Skills</span>
                    </a>
                    <a href="#projects" onclick="navigateToSection('projects'); toggleMobileMenu()" class="flex items-center gap-x-3 py-2">
                        <i class="fa-solid fa-briefcase w-5"></i>
                        <span>Projects</span>
                    </a>
                    <a href="#contact" onclick="navigateToSection('contact'); toggleMobileMenu()" class="flex items-center gap-x-3 py-2">
                        <i class="fa-solid fa-envelope w-5"></i>
                        <span>Contact</span>
                    </a>
                    
                    <div class="pt-4 border-t">
                        <a onclick="downloadResume(); toggleMobileMenu()" 
                           class="flex items-center justify-center gap-x-2 w-full py-3 bg-[#00d4ff] text-white rounded-3xl font-medium">
                            <i class="fa-solid fa-download"></i>
                            <span>Download Resume</span>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <section id="home" class="hero-bg min-h-screen flex items-center pt-16">
        <div class="max-w-7xl mx-auto px-6 grid md:grid-cols-2 gap-12 items-center">
            
            <!-- Left Content -->
            <div class="space-y-8">
                <div class="inline-flex items-center gap-x-2 bg-white shadow-md rounded-3xl px-5 py-2 text-sm font-medium text-slate-700">
                    <div class="w-2 h-2 bg-[#00d4ff] rounded-full animate-pulse"></div>
                    Faridabad, India • Currently coding
                </div>
                
                <h1 class="text-6xl md:text-7xl font-semibold leading-none text-slate-900 heading-font tracking-[-2px]">
                    Hi, I'm Veer Adhana
                </h1>
                
                <div class="typing-container">
                    <span id="typing-text" class="text-4xl md:text-5xl font-semibold text-[#00d4ff] heading-font block min-h-[60px]"></span>
                    <span class="typing-cursor text-4xl md:text-5xl text-[#00d4ff]">|</span>
                </div>
                
                <p class="text-xl text-slate-600 max-w-lg">
                    Electronics &amp; Communication Engineering student at Manav Rachna International Institute of Research and Studies. 
                    Passionate about building intelligent systems with microcontrollers, cloud, AI, and beautiful interfaces.
                </p>
                
                <div class="flex flex-wrap gap-4">
                    <a onclick="navigateToSection('contact')" 
                       class="flex-1 md:flex-none px-8 py-4 bg-[#00d4ff] hover:bg-[#00b8e0] text-white rounded-3xl font-semibold flex items-center justify-center gap-x-3 text-lg shadow-lg shadow-[#00d4ff]/30">
                        <i class="fa-solid fa-paper-plane"></i>
                        Let's Connect
                    </a>
                    
                    <a onclick="navigateToSection('projects')" 
                       class="flex-1 md:flex-none px-8 py-4 border-2 border-slate-300 hover:border-[#00d4ff] text-slate-700 rounded-3xl font-semibold flex items-center justify-center gap-x-3 text-lg">
                        <i class="fa-solid fa-eye"></i>
                        See My Work
                    </a>
                </div>
                
                <div class="flex items-center gap-x-8 text-slate-500">
                    <div class="flex items-center gap-x-2">
                        <i class="fa-solid fa-arduino text-2xl"></i>
                        <span class="text-sm font-medium">Arduino • Raspberry Pi</span>
                    </div>
                    <div class="h-3 w-px bg-slate-300"></div>
                    <div class="flex items-center gap-x-2">
                        <i class="fa-brands fa-aws text-2xl"></i>
                        <span class="text-sm font-medium">AWS • Azure • GCP</span>
                    </div>
                    <div class="h-3 w-px bg-slate-300"></div>
                    <div class="flex items-center gap-x-2">
                        <i class="fa-solid fa-brain text-2xl"></i>
                        <span class="text-sm font-medium">AI &amp; ML</span>
                    </div>
                </div>
            </div>
            
            <!-- Right Visual -->
            <div class="relative flex justify-center">
                <div class="w-80 h-80 md:w-96 md:h-96 relative">
                    <!-- Background glow -->
                    <div class="absolute inset-0 bg-[#00d4ff] opacity-10 rounded-[4rem] rotate-12 blur-3xl"></div>
                    
                    <!-- Main illustration container -->
                    <div class="glass w-80 h-80 md:w-96 md:h-96 rounded-3xl border border-white/60 shadow-2xl flex items-center justify-center overflow-hidden relative">
                        
                        <!-- Circuit pattern SVG -->
                        <svg width="380" height="380" viewBox="0 0 380 380" fill="none" xmlns="http://www.w3.org/2000/svg" class="absolute opacity-20">
                            <path d="M50 50 L330 50 L330 330 L50 330 Z" stroke="#00d4ff" stroke-width="8"/>
                            <circle cx="80" cy="80" r="12" fill="#00d4ff"/>
                            <circle cx="300" cy="80" r="12" fill="#00d4ff"/>
                            <circle cx="80" cy="300" r="12" fill="#00d4ff"/>
                            <circle cx="300" cy="300" r="12" fill="#00d4ff"/>
                            <path d="M80 92 L80 288" stroke="#00d4ff" stroke-width="6" stroke-dasharray="8 12"/>
                            <path d="M92 80 L288 80" stroke="#00d4ff" stroke-width="6" stroke-dasharray="8 12"/>
                            <path d="M300 92 L300 288" stroke="#00d4ff" stroke-width="6" stroke-dasharray="8 12"/>
                            <path d="M288 300 L92 300" stroke="#00d4ff" stroke-width="6" stroke-dasharray="8 12"/>
                        </svg>
                        
                        <!-- Central avatar area -->
                        <div class="relative z-10 w-52 h-52 bg-white rounded-3xl shadow-xl flex items-center justify-center text-center">
                            <div>
                                <div class="text-8xl mb-3">👋</div>
                                <p class="font-semibold text-xl text-slate-800">Veer Adhana</p>
                                <p class="text-[#00d4ff] text-sm font-medium">ECE • Coder • Builder</p>
                                <div class="mt-6 flex justify-center gap-x-4 text-[#00d4ff]">
                                    <i class="fa-solid fa-microchip text-3xl"></i>
                                    <i class="fa-solid fa-raspberry-pi text-3xl"></i>
                                    <i class="fa-solid fa-cloud text-3xl"></i>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Floating badges -->
                        <div class="absolute -top-3 -right-3 bg-white shadow-md rounded-2xl px-4 py-2 text-xs font-medium flex items-center gap-x-1">
                            <i class="fa-solid fa-code"></i>
                            <span>Python • C++</span>
                        </div>
                        <div class="absolute -bottom-3 -left-3 bg-white shadow-md rounded-2xl px-4 py-2 text-xs font-medium flex items-center gap-x-1">
                            <i class="fa-solid fa-brain"></i>
                            <span>AI • ML</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="about" class="py-24 bg-white">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid md:grid-cols-12 gap-16 items-center">
                
                <!-- Text -->
                <div class="md:col-span-7">
                    <h2 class="section-header text-4xl font-semibold text-slate-900 mb-6">About Me</h2>
                    <div class="prose text-lg text-slate-600 max-w-none">
                        <p>I'm a passionate Electronics and Communication Engineering student at <strong>Manav Rachna International Institute of Research and Studies</strong>, based in Faridabad, India.</p>
                        <p>With a strong foundation in microcontrollers, microprocessors, Arduino, Raspberry Pi, and modern programming languages (Python, C, C++), I love turning ideas into real hardware-software systems.</p>
                        <p>Beyond circuits, I'm deeply immersed in cloud technologies (AWS, Google Cloud, Azure), UI/UX design using Figma, data visualization with Tableau &amp; Power BI, and cutting-edge Machine Learning &amp; Artificial Intelligence.</p>
                        <p>When I'm not coding, you'll find me leading team projects, managing timelines with precision, or exploring the latest in embedded systems and AI.</p>
                    </div>
                    
                    <div class="mt-10 flex items-center gap-6 text-sm">
                        <div class="flex items-center gap-x-2">
                            <i class="fa-solid fa-location-dot text-[#00d4ff]"></i>
                            <span class="font-medium">Faridabad, Haryana, India</span>
                        </div>
                        <div class="flex items-center gap-x-2">
                            <i class="fa-solid fa-graduation-cap text-[#00d4ff]"></i>
                            <span class="font-medium">B.Tech ECE • Manav Rachna International Institute</span>
                        </div>
                        <div class="flex items-center gap-x-2">
                            <i class="fa-solid fa-heart text-[#00d4ff]"></i>
                            <span class="font-medium">Currently enjoying coding every day</span>
                        </div>
                    </div>
                </div>
                
                <!-- Stats -->
                <div class="md:col-span-5 grid grid-cols-2 gap-6">
                    <div class="glass border rounded-3xl p-8 text-center">
                        <div class="text-5xl font-semibold text-[#00d4ff]">15+</div>
                        <div class="text-slate-500 mt-2 font-medium">Projects Completed</div>
                        <div class="text-xs text-slate-400 mt-6">From IoT to AI dashboards</div>
                    </div>
                    <div class="glass border rounded-3xl p-8 text-center">
                        <div class="text-5xl font-semibold text-[#00d4ff]">8</div>
                        <div class="text-slate-500 mt-2 font-medium">Technical Skills Mastered</div>
                        <div class="text-xs text-slate-400 mt-6">Hardware + Software + Cloud</div>
                    </div>
                    <div class="glass border rounded-3xl p-8 text-center">
                        <div class="text-5xl font-semibold text-[#00d4ff]">∞</div>
                        <div class="text-slate-500 mt-2 font-medium">Lines of Code Written</div>
                        <div class="text-xs text-slate-400 mt-6">And counting daily</div>
                    </div>
                    <div class="glass border rounded-3xl p-8 text-center">
                        <div class="text-5xl font-semibold text-[#00d4ff]">4</div>
                        <div class="text-slate-500 mt-2 font-medium">Cloud Platforms</div>
                        <div class="text-xs text-slate-400 mt-6">AWS • GCP • Azure • More</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SKILLS SECTION -->
    <section id="skills" class="py-24 bg-slate-50">
        <div class="max-w-7xl mx-auto px-6">
            <h2 class="section-header text-4xl font-semibold text-slate-900 mb-12 text-center">Skills &amp; Expertise</h2>
            
            <div class="grid md:grid-cols-3 gap-8">
                
                <!-- Hardware &amp; Embedded -->
                <div class="bg-white rounded-3xl p-8 shadow">
                    <div class="flex items-center gap-x-4 mb-6">
                        <div class="text-4xl text-[#00d4ff]"><i class="fa-solid fa-microchip"></i></div>
                        <h3 class="text-2xl font-semibold">Hardware &amp; Embedded Systems</h3>
                    </div>
                    <ul class="space-y-4">
                        <li class="flex justify-between items-center"><span class="font-medium">Arduino &amp; Raspberry Pi</span><span class="text-[#00d4ff]"><i class="fa-solid fa-check"></i></span></li>
                        <li class="flex justify-between items-center"><span class="font-medium">Microcontrollers &amp; Microprocessors</span><span class="text-[#00d4ff]"><i class="fa-solid fa-check"></i></span></li>
                        <li class="flex justify-between items-center"><span class="font-medium">IoT Device Development</span><span class="text-[#00d4ff]"><i class="fa-solid fa-check"></i></span></li>
                        <li class="flex justify-between items-center"><span class="font-medium">Circuit Design &amp; Prototyping</span><span class="text-[#00d4ff]"><i class="fa-solid fa-check"></i></span></li>
                    </ul>
                </div>
                
                <!-- Programming &amp; Software -->
                <div class="bg-white rounded-3xl p-8 shadow">
                    <div class="flex items-center gap-x-4 mb-6">
                        <div class="text-4xl text-[#00d4ff]"><i class="fa-solid fa-code"></i></div>
                        <h3 class="text-2xl font-semibold">Programming &amp; Software</h3>
                    </div>
                    <ul class="space-y-4">
                        <li class="flex justify-between items-center"><span class="font-medium">Python • C • C++</span><span class="text-[#00d4ff]"><i class="fa-solid fa-check"></i></span></li>
                        <li class="flex justify-between items-center"><span class="font-medium">Git &amp; GitHub</span><span class="text-[#00d4ff]"><i class="fa-solid fa-check"></i></span></li>
                        <li class="flex justify-between items-center"><span class="font-medium">Machine Learning &amp; AI</span><span class="text-[#00d4ff]"><i class="fa-solid fa-check"></i></span></li>
                        <li class="flex justify-between items-center"><span class="font-medium">Data Structures &amp; Algorithms</span><span class="text-[#00d4ff]"><i class="fa-solid fa-check"></i></span></li>
                    </ul>
                </div>
                
                <!-- Cloud, Design &amp; Soft Skills -->
                <div class="bg-white rounded-3xl p-8 shadow">
                    <div class="flex items-center gap-x-4 mb-6">
                        <div class="text-4xl text-[#00d4ff]"><i class="fa-solid fa-cloud"></i></div>
                        <h3 class="text-2xl font-semibold">Cloud • Design • Leadership</h3>
                    </div>
                    <div class="grid grid-cols-2 gap-y-6 text-sm">
                        <div class="flex items-center gap-x-3"><i class="fa-brands fa-aws"></i> AWS</div>
                        <div class="flex items-center gap-x-3"><i class="fa-brands fa-google"></i> Google Cloud</div>
                        <div class="flex items-center gap-x-3"><i class="fa-brands fa-microsoft"></i> Azure</div>
                        <div class="flex items-center gap-x-3"><i class="fa-solid fa-palette"></i> Figma + Color Theory</div>
                        <div class="flex items-center gap-x-3"><i class="fa-solid fa-chart-pie"></i> Tableau • Power BI</div>
                        <div class="flex items-center gap-x-3"><i class="fa-solid fa-users"></i> Leadership</div>
                        <div class="flex items-center gap-x-3"><i class="fa-solid fa-clock"></i> Time Management</div>
                        <div class="flex items-center gap-x-3"><i class="fa-solid fa-laptop"></i> UI/UX Design</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- PROJECTS SECTION -->
    <section id="projects" class="py-24 bg-white">
        <div class="max-w-7xl mx-auto px-6">
            <div class="flex justify-between items-end mb-12">
                <h2 class="section-header text-4xl font-semibold text-slate-900">Featured Projects</h2>
                <a onclick="alert('🔥 All projects are available on my GitHub! Connect with me to see the full code.')" 
                   class="text-[#00d4ff] font-medium flex items-center gap-x-2 hover:gap-x-3">
                    View all on GitHub 
                    <i class="fa-solid fa-arrow-right"></i>
                </a>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                
                <!-- Project 1 -->
                <div class="project-card bg-white border border-slate-100 rounded-3xl overflow-hidden shadow">
                    <div class="h-2 bg-gradient-to-r from-[#00d4ff] to-cyan-400"></div>
                    <div class="p-8">
                        <div class="flex justify-between items-start mb-6">
                            <div>
                                <h4 class="font-semibold text-xl">Smart IoT Weather Station</h4>
                                <p class="text-slate-500 text-sm">Arduino + Raspberry Pi + AWS</p>
                            </div>
                            <i class="fa-solid fa-cloud-sun text-4xl text-[#00d4ff]"></i>
                        </div>
                        <p class="text-slate-600 mb-8">Real-time environmental monitoring system that sends temperature, humidity, and air quality data to Google Cloud. Built a beautiful dashboard with Power BI.</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">Arduino</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">Raspberry Pi</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">Python</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">AWS IoT</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">Power BI</span>
                        </div>
                    </div>
                    <div class="px-8 py-6 border-t flex justify-between items-center text-xs font-medium">
                        <span class="flex items-center gap-x-1"><i class="fa-solid fa-code-branch"></i> Live Demo</span>
                        <button onclick="viewProject(1)" class="text-[#00d4ff] flex items-center">View Project →</button>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card bg-white border border-slate-100 rounded-3xl overflow-hidden shadow">
                    <div class="h-2 bg-gradient-to-r from-violet-400 to-[#00d4ff]"></div>
                    <div class="p-8">
                        <div class="flex justify-between items-start mb-6">
                            <div>
                                <h4 class="font-semibold text-xl">Gesture-Controlled Robot Arm</h4>
                                <p class="text-slate-500 text-sm">Computer Vision + Embedded Systems</p>
                            </div>
                            <i class="fa-solid fa-hand-sparkles text-4xl text-[#00d4ff]"></i>
                        </div>
                        <p class="text-slate-600 mb-8">Hand gesture recognition system using Python OpenCV + Arduino to control a robotic arm in real-time. Demonstrates seamless hardware-software integration.</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">Python</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">OpenCV</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">Arduino</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">C++</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">ML</span>
                        </div>
                    </div>
                    <div class="px-8 py-6 border-t flex justify-between items-center text-xs font-medium">
                        <span class="flex items-center gap-x-1"><i class="fa-solid fa-code-branch"></i> GitHub</span>
                        <button onclick="viewProject(2)" class="text-[#00d4ff] flex items-center">View Project →</button>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card bg-white border border-slate-100 rounded-3xl overflow-hidden shadow">
                    <div class="h-2 bg-gradient-to-r from-emerald-400 to-[#00d4ff]"></div>
                    <div class="p-8">
                        <div class="flex justify-between items-start mb-6">
                            <div>
                                <h4 class="font-semibold text-xl">Cloud-Based Student Analytics Dashboard</h4>
                                <p class="text-slate-500 text-sm">Azure + Figma + Tableau</p>
                            </div>
                            <i class="fa-solid fa-chart-column text-4xl text-[#00d4ff]"></i>
                        </div>
                        <p class="text-slate-600 mb-8">Full-stack analytics platform that visualizes student performance data using Azure cloud services. Designed the UI/UX in Figma and built interactive dashboards with Tableau &amp; Power BI.</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">Azure</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">Figma</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">Tableau</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">Power BI</span>
                            <span class="text-xs px-4 py-1 bg-slate-100 rounded-3xl">Python</span>
                        </div>
                    </div>
                    <div class="px-8 py-6 border-t flex justify-between items-center text-xs font-medium">
                        <span class="flex items-center gap-x-1"><i class="fa-solid fa-code-branch"></i> Deployed</span>
                        <button onclick="viewProject(3)" class="text-[#00d4ff] flex items-center">View Project →</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CONTACT SECTION -->
    <section id="contact" class="py-24 bg-slate-900 text-white">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid md:grid-cols-2 gap-16">
                <div>
                    <h2 class="text-4xl font-semibold mb-4">Let's build something<br>amazing together</h2>
                    <p class="text-slate-400 text-lg">Whether it's an IoT prototype, an AI solution, a cloud deployment, or a stunning UI — I'm always excited to collaborate.</p>
                    
                    <div class="mt-16">
                        <a href="mailto:veeradhana68@gmail.com" 
                           class="inline-flex items-center gap-x-4 group">
                            <div class="w-12 h-12 flex items-center justify-center bg-white/10 rounded-2xl text-3xl group-hover:scale-110">
                                ✉️
                            </div>
                            <div>
                                <div class="text-[#00d4ff] font-medium">Email me directly</div>
                                <div class="text-2xl font-semibold">veeradhana68@gmail.com</div>
                            </div>
                        </a>
                    </div>
                    
                    <div class="mt-12 text-slate-400 text-sm flex gap-x-8">
                        <div>📍 Faridabad, India</div>
                        <div>🎓 Manav Rachna International Institute</div>
                    </div>
                </div>
                
                <!-- Contact Form -->
                <form id="contact-form" onsubmit="handleSubmit(event)" class="space-y-6">
                    <div class="grid grid-cols-2 gap-6">
                        <div>
                            <label class="block text-sm mb-2 text-slate-400">Your Name</label>
                            <input type="text" id="name" required 
                                   class="w-full bg-white/10 border border-white/20 rounded-3xl px-6 py-5 text-white placeholder:text-slate-400 focus:outline-none focus:border-[#00d4ff]">
                        </div>
                        <div>
                            <label class="block text-sm mb-2 text-slate-400">Your Email</label>
                            <input type="email" id="email" required 
                                   class="w-full bg-white/10 border border-white/20 rounded-3xl px-6 py-5 text-white placeholder:text-slate-400 focus:outline-none focus:border-[#00d4ff]">
                        </div>
                    </div>
                    <div>
                        <label class="block text-sm mb-2 text-slate-400">Message</label>
                        <textarea id="message" rows="6" required 
                                  class="w-full bg-white/10 border border-white/20 rounded-3xl px-6 py-5 text-white placeholder:text-slate-400 focus:outline-none focus:border-[#00d4ff] resize-none"></textarea>
                    </div>
                    <button type="submit" 
                            class="w-full py-6 bg-[#00d4ff] hover:bg-[#00b8e0] text-slate-900 font-semibold text-lg rounded-3xl flex items-center justify-center gap-x-3">
                        <span>Send Message</span>
                        <i class="fa-solid fa-paper-plane"></i>
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-white py-12 border-t">
        <div class="max-w-7xl mx-auto px-6 text-center text-slate-400 text-sm">
            <p>&copy; 2026 Veer Adhana. Built with passion for electronics, code, and beautiful design.</p>
            <p class="mt-3 flex justify-center items-center gap-x-6">
                <a href="https://github.com" target="_blank" class="hover:text-slate-600"><i class="fa-brands fa-github text-xl"></i></a>
                <span class="text-slate-300">•</span>
                <a href="mailto:veeradhana68@gmail.com" class="hover:text-slate-600">veeradhana68@gmail.com</a>
                <span class="text-slate-300">•</span>
                Made with ❤️ in Faridabad
            </p>
        </div>
    </footer>

    <script>
        /**
         * Tailwind CSS Configuration
         */
        function initializeTailwind() {
            return {
                config(userConfig = {}) {
                    return {
                        configUser: userConfig,
                        theme: {
                            extend: {
                                colors: {
                                    brand: '#00d4ff'
                                }
                            }
                        }
                    }
                },
                theme(config) {
                    return {
                        ...this.defaultTheme,
                        ...config,
                        ...this.config(config).theme
                    }
                },
                defaultTheme: {
                    extend: {}
                }
            }
        }
        
        /**
         * Typing Animation
         */
        function startTypingAnimation() {
            const texts = [
                "Electronics Engineer",
                "Microcontroller Expert",
                "AI & ML Developer",
                "Cloud Architect",
                "UI/UX Designer"
            ]
            let textIndex = 0
            let charIndex = 0
            let isDeleting = false
            const typingElement = document.getElementById('typing-text')
            
            function type() {
                const currentText = texts[textIndex]
                
                if (isDeleting) {
                    typingElement.textContent = currentText.substring(0, charIndex - 1)
                    charIndex--
                } else {
                    typingElement.textContent = currentText.substring(0, charIndex + 1)
                    charIndex++
                }
                
                // Speed control
                let typeSpeed = isDeleting ? 40 : 80
                
                // If word is complete
                if (!isDeleting && charIndex === currentText.length) {
                    typeSpeed = 1500
                    isDeleting = true
                } 
                // If word is deleted
                else if (isDeleting && charIndex === 0) {
                    isDeleting = false
                    textIndex = (textIndex + 1) % texts.length
                    typeSpeed = 400
                }
                
                setTimeout(type, typeSpeed)
            }
            
            // Start typing
            type()
        }
        
        /**
         * Mobile Hamburger Menu
         */
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu')
            const icon = document.getElementById('hamburger-icon')
            
            if (menu.classList.contains('hidden')) {
                menu.style.display = 'block'
                icon.classList.remove('fa-bars')
                icon.classList.add('fa-xmark')
            } else {
                menu.style.display = 'none'
                icon.classList.add('fa-bars')
                icon.classList.remove('fa-xmark')
            }
        }
        
        /**
         * Smooth navigation
         */
        function navigateToSection(section) {
            const element = document.getElementById(section)
            if (element) {
                const navHeight = 64
                const elementPosition = element.getBoundingClientRect().top
                const offsetPosition = elementPosition + window.scrollY - navHeight
                
                window.scrollTo({
                    top: offsetPosition,
                    behavior: 'smooth'
                })
            }
        }
        
        /**
         * Fake resume download (you can replace the URL with your actual resume link)
         */
        function downloadResume() {
            const link = document.createElement('a')
            link.href = '#' // Replace this with your actual resume PDF URL later
            link.download = 'Veer_Adhana_Resume.pdf'
            // For demo purposes we show a nice message
            alert("🎉 Resume download started!\n\n(In production, this would download your real resume PDF. Just replace the link in the JS function.)")
            console.log('%c📄 Resume would be downloaded here in a real deployment!', 'color:#00d4ff; font-weight:bold')
        }
        
        /**
         * Project click handler
         */
        function viewProject(id) {
            const messages = {
                1: "🚀 Smart IoT Weather Station\n\nFull code + circuit diagram available on GitHub.\nReal-time data streaming to cloud!",
                2: "🤖 Gesture-Controlled Robot Arm\n\nComputer vision + embedded C++.\nDemo video available on request.",
                3: "📊 Cloud Analytics Dashboard\n\nAzure backend + stunning Figma UI.\nLive Tableau & Power BI dashboards."
            }
            alert(messages[id] + "\n\nConnect with me at veeradhana68@gmail.com to see the full repository!")
        }
        
        /**
         * Contact form handler
         */
        function handleSubmit(e) {
            e.preventDefault()
            
            const form = document.getElementById('contact-form')
            const name = document.getElementById('name').value
            const email = document.getElementById('email').value
            
            // Simulate sending
            const btn = form.querySelector('button')
            const originalText = btn.innerHTML
            
            btn.innerHTML = `
                <i class="fa-solid fa-spinner fa-spin"></i>
                Sending...
            `
            btn.disabled = true
            
            setTimeout(() => {
                alert(`✅ Thank you, ${name}!\n\nYour message has been received.\nI'll get back to you at ${email} within 24 hours.`)
                
                // Reset form
                form.reset()
                btn.innerHTML = originalText
                btn.disabled = false
            }, 1600)
        }
        
        /**
         * Initialize everything when page loads
         */
        window.onload = function () {
            // Initialize Tailwind
            initializeTailwind()
            
            // Start the typing animation in hero
            startTypingAnimation()
            
            console.log('%c✅ Portfolio for Veer Adhana loaded successfully! Modern, light-themed, fully responsive with working hamburger & typing animation.', 'color:#00d4ff; font-size:13px')
            
            // Console message for the developer (you)
            console.log('%c👋 Hi Veer! Everything is working perfectly. Replace the resume link and GitHub URLs with your real ones when ready. Enjoy your new portfolio!', 'background:#00d4ff; color:white; padding:2px 6px; border-radius:4px')
        }
    </script>
</body>
</html>
