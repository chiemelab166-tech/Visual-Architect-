<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Visual Architect | Luxury Creative Agency</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        :root {
            --charcoal: #0B0B0D;
            --ivory: #F5F5F2;
            --gold: #C6A75E;
            --slate: #6E6E73;
        }

        body {
            background-color: var(--charcoal);
            color: var(--ivory);
            font-family: 'Inter', sans-serif;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        h1, h2, h3, .font-serif {
            font-family: 'Playfair Display', serif;
        }

        .blueprint-bg {
            background-image: 
                linear-gradient(rgba(110, 110, 115, 0.05) 1px, transparent 1px),
                linear-gradient(90deg, rgba(110, 110, 115, 0.05) 1px, transparent 1px);
            background-size: 50px 50px;
        }

        .line-accent {
            width: 60px;
            height: 1px;
            background-color: var(--gold);
        }

        /* Fixed Button Styles */
        .btn-premium {
            background-color: var(--gold);
            color: var(--charcoal);
            display: inline-block;
            transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
            border: 1px solid var(--gold);
            cursor: pointer;
            position: relative;
            z-index: 20;
        }

        .btn-premium:hover {
            background-color: transparent;
            color: var(--gold);
            transform: translateY(-2px);
        }

        .btn-outline {
            display: inline-block;
            border: 1px solid var(--slate);
            color: var(--ivory);
            transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
            cursor: pointer;
            position: relative;
            z-index: 20;
        }

        .btn-outline:hover {
            border-color: var(--gold);
            color: var(--gold);
            transform: translateY(-2px);
        }

        .service-card {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(110, 110, 115, 0.1);
            transition: all 0.5s ease;
        }

        .service-card:hover {
            border-color: var(--gold);
            background: rgba(255, 255, 255, 0.04);
        }

        /* Animation Classes */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        .portfolio-item img {
            transition: transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .portfolio-item:hover img {
            transform: scale(1.05);
        }

        .nav-link::after {
            content: '';
            display: block;
            width: 0;
            height: 1px;
            background: var(--gold);
            transition: width .3s;
        }

        .nav-link:hover::after {
            width: 100%;
        }

        ::-webkit-scrollbar { width: 6px; }
        ::-webkit-scrollbar-track { background: var(--charcoal); }
        ::-webkit-scrollbar-thumb { background: #222; }
        ::-webkit-scrollbar-thumb:hover { background: var(--gold); }
    </style>
</head>
<body class="blueprint-bg">

    <!-- NAVIGATION -->
    <nav class="fixed top-0 left-0 w-full z-50 px-6 py-8 md:px-12 flex justify-between items-center bg-[#0B0B0D]/90 backdrop-blur-md">
        <div class="flex items-center space-x-2">
            <span class="text-xl font-bold tracking-tighter uppercase border-l-2 border-[#C6A75E] pl-3">
                Visual Architect
            </span>
        </div>
        <div class="hidden md:flex space-x-12 text-xs uppercase tracking-[0.2em] font-medium text-[#6E6E73]">
            <a href="#about" class="nav-link hover:text-white transition">About</a>
            <a href="#services" class="nav-link hover:text-white transition">Services</a>
            <a href="#portfolio" class="nav-link hover:text-white transition">Selected Works</a>
            <a href="mailto:Chiemelab166@gmail.com" class="nav-link hover:text-white transition text-[#C6A75E]">Contact</a>
        </div>
        <div class="md:hidden">
            <i data-lucide="menu" class="w-6 h-6 text-[#C6A75E]"></i>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <section class="relative min-h-screen flex flex-col justify-center px-6 md:px-24 pt-20">
        <div class="max-w-5xl z-10">
            <div class="flex items-center space-x-4 mb-6 reveal">
                <div class="line-accent"></div>
                <span class="uppercase tracking-[0.4em] text-xs text-[#6E6E73]">Architectural Precision</span>
            </div>
            <h1 class="text-5xl md:text-8xl lg:text-[100px] leading-[1.1] mb-12 reveal" style="transition-delay: 200ms;">
                We Design Visual <br> Systems That <br> <span class="italic text-[#C6A75E]">Command Attention.</span>
            </h1>
            <p class="text-[#6E6E73] max-w-xl text-lg md:text-xl font-light mb-12 reveal" style="transition-delay: 400ms;">
                Visual Architect is a strategic design firm. We build precise visual structures for brands that refuse to settle for the ordinary.
            </p>
            <div class="flex flex-col sm:flex-row gap-6 reveal relative z-20" style="transition-delay: 600ms;">
                <a href="https://wa.me/2349045208583" target="_blank" rel="noopener noreferrer" class="btn-premium px-10 py-5 text-sm uppercase tracking-widest font-semibold text-center">
                    Chat on WhatsApp
                </a>
                <a href="mailto:Chiemelab166@gmail.com" class="btn-outline px-10 py-5 text-sm uppercase tracking-widest font-semibold text-center">
                    Email Us
                </a>
            </div>
        </div>

        <!-- Abstract Architectural Accents -->
        <div class="absolute top-0 right-0 w-1/3 h-full overflow-hidden opacity-10 pointer-events-none hidden lg:block">
            <svg viewBox="0 0 100 100" class="w-full h-full text-[#6E6E73]">
                <line x1="10" y1="0" x2="10" y2="100" stroke="currentColor" stroke-width="0.1" />
                <line x1="30" y1="0" x2="30" y2="100" stroke="currentColor" stroke-width="0.1" />
                <line x1="50" y1="0" x2="50" y2="100" stroke="currentColor" stroke-width="0.1" />
                <circle cx="50" cy="50" r="40" fill="none" stroke="currentColor" stroke-width="0.05" />
                <path d="M10 20 L90 80" stroke="#C6A75E" stroke-width="0.1" stroke-dasharray="2,2" />
            </svg>
        </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="about" class="py-24 md:py-40 px-6 md:px-24 bg-[#0B0B0D]">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
            <div class="relative group reveal">
                <div class="absolute -top-4 -left-4 w-24 h-24 border-t border-l border-[#C6A75E]"></div>
                <div class="absolute -bottom-4 -right-4 w-24 h-24 border-b border-r border-[#6E6E73]"></div>
                <div class="overflow-hidden bg-[#111]">
                    <img src="38846.jpg" alt="Founder" class="w-full h-auto object-cover grayscale transition-all duration-700 group-hover:grayscale-0">
                </div>
            </div>
            <div class="reveal" style="transition-delay: 200ms;">
                <h2 class="text-4xl md:text-5xl mb-8">The Philosophy of Intentionality</h2>
                <div class="space-y-6 text-[#6E6E73] text-lg leading-relaxed font-light">
                    <p>At Visual Architect, we don't just create graphics; we engineer brand environments. Led by a vision for structural clarity and aesthetic authority, our work is defined by the intersection of geometry, strategy, and soul.</p>
                    <p>Every line is calculated. Every color is deliberate. We believe that true luxury is found in the restraint of the design and the precision of the delivery.</p>
                </div>
                <div class="mt-12 flex items-center space-x-6">
                    <div class="w-16 h-[1px] bg-[#C6A75E]"></div>
                    <span class="font-serif italic text-2xl text-[#F5F5F2]">Founding Director</span>
                </div>
            </div>
        </div>
    </section>

    <!-- SERVICES SECTION -->
    <section id="services" class="py-24 md:py-40 px-6 md:px-24 blueprint-bg">
        <div class="text-center mb-24 reveal">
            <span class="uppercase tracking-[0.4em] text-xs text-[#C6A75E] block mb-4">Core Competencies</span>
            <h2 class="text-4xl md:text-6xl">Architectural Services</h2>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-px bg-[#222]">
            <div class="service-card p-12 flex flex-col reveal"><i data-lucide="layers" class="w-8 h-8 text-[#C6A75E] mb-8"></i><h3 class="text-2xl mb-4">Brand Identity</h3><p class="text-[#6E6E73] font-light">Systemic branding that establishes authority through comprehensive guidelines.</p></div>
            <div class="service-card p-12 flex flex-col reveal"><i data-lucide="pen-tool" class="w-8 h-8 text-[#C6A75E] mb-8"></i><h3 class="text-2xl mb-4">Graphic Design</h3><p class="text-[#6E6E73] font-light">Precise editorial layouts and high-stakes visual communication assets.</p></div>
            <div class="service-card p-12 flex flex-col reveal"><i data-lucide="film" class="w-8 h-8 text-[#C6A75E] mb-8"></i><h3 class="text-2xl mb-4">Motion & Video</h3><p class="text-[#6E6E73] font-light">Cinematic movement that brings architectural design to life.</p></div>
        </div>
    </section>

    <!-- PORTFOLIO SECTION -->
    <section id="portfolio" class="py-24 md:py-40 px-6 md:px-24">
        <div class="flex flex-col md:flex-row justify-between items-end mb-16 gap-8 reveal">
            <div>
                <span class="uppercase tracking-[0.4em] text-xs text-[#6E6E73] block mb-4">The Archive</span>
                <h2 class="text-4xl md:text-6xl">Selected Works</h2>
            </div>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
            <div class="portfolio-item group cursor-pointer reveal">
                <div class="overflow-hidden mb-6 bg-[#111] aspect-[4/5]"><img src="https://images.unsplash.com/photo-1549490349-8643362247b5?auto=format&fit=crop&q=80&w=800" alt="Work 1" class="w-full h-full object-cover"></div>
                <h4 class="text-2xl mb-1">Aurelius Identity</h4>
            </div>
            <div class="portfolio-item group cursor-pointer reveal" style="transition-delay: 150ms;">
                <div class="overflow-hidden mb-6 bg-[#111] aspect-[4/5]"><img src="https://images.unsplash.com/photo-1515462277125-26977e1f488d?auto=format&fit=crop&q=80&w=800" alt="Work 2" class="w-full h-full object-cover"></div>
                <h4 class="text-2xl mb-1">Noir Motion</h4>
            </div>
        </div>
    </section>

    <!-- FINAL CTA -->
    <section class="py-32 md:py-48 px-6 md:px-24 bg-[#C6A75E]/5 text-center border-t border-[#6E6E73]/10">
        <div class="max-w-3xl mx-auto reveal">
            <h2 class="text-5xl md:text-7xl mb-12">Let’s Build Something Exceptional.</h2>
            <div class="flex flex-col sm:flex-row justify-center gap-6 relative z-20">
                <a href="https://wa.me/2349045208583" target="_blank" rel="noopener noreferrer" class="btn-premium px-12 py-6 text-sm uppercase tracking-widest font-semibold">
                    Start a Project (WhatsApp)
                </a>
                <a href="mailto:Chiemelab166@gmail.com" class="btn-outline px-12 py-6 text-sm uppercase tracking-widest font-semibold">
                    Email Our Team
                </a>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="py-16 px-6 md:px-24 bg-[#0B0B0D] border-t border-[#6E6E73]/10">
        <div class="flex flex-col md:flex-row justify-between items-center gap-12">
            <div class="text-center md:text-left">
                <div class="text-xl font-bold uppercase mb-4">Visual Architect</div>
                <p class="text-[#6E6E73] text-sm uppercase tracking-widest">Designing visual systems that command authority.</p>
            </div>
            <div class="flex space-x-8">
                <a href="https://wa.me/2349045208583" target="_blank" class="text-[#6E6E73] hover:text-[#C6A75E] transition"><i data-lucide="message-circle" class="w-6 h-6"></i></a>
                <a href="mailto:Chiemelab166@gmail.com" class="text-[#6E6E73] hover:text-[#C6A75E] transition"><i data-lucide="mail" class="w-6 h-6"></i></a>
            </div>
        </div>
    </footer>

    <script>
        lucide.createIcons();
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => { if (entry.isIntersecting) entry.target.classList.add('active'); });
        }, { threshold: 0.1 });
        document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
    </script>
</body>
</html>


