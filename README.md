## Hi there 👋

<!--<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CKY Chain - Architecting the Quantum Future of Decentralization</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">

    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0A0A0F; /* Even darker base */
            color: #E0E0E0; /* Light gray for text */
            overflow-x: hidden;
        }
        ::-webkit-scrollbar { width: 6px; }
        ::-webkit-scrollbar-track { background: #1A1A2E; }
        ::-webkit-scrollbar-thumb { background: #7F5AF0; /* Vibrant Purple */ border-radius: 3px; }
        ::-webkit-scrollbar-thumb:hover { background: #9D7FEA; }

        .hero-bg-animation {
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            width: 100%; height: 100%;
            overflow: hidden;
            z-index: 0;
        }
        .hero-bg-animation svg {
            position: absolute;
            opacity: 0.1;
            animation: rotateParticles 120s linear infinite;
        }
        .hero-bg-animation svg path {
            fill: none;
            stroke-width: 0.5px;
        }
        @keyframes rotateParticles {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        .particle-1 { animation-delay: 0s; animation-duration: 120s; }
        .particle-2 { animation-delay: -30s; animation-duration: 150s; opacity: 0.05 !important; }


        .btn {
            padding: 0.75rem 1.5rem;
            border-radius: 0.5rem;
            font-weight: 600;
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            display: inline-flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            border: 1px solid transparent;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        .btn::before {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(120deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: all 0.6s cubic-bezier(0.25, 0.8, 0.25, 1);
            z-index: -1;
        }
        .btn:hover::before {
            left: 100%;
        }
        .btn-primary {
            background: linear-gradient(to right, #7F5AF0, #A855F7); /* Purple to Violet */
            color: white;
            box-shadow: 0 5px 15px rgba(127, 90, 240, 0.4);
        }
        .btn-primary:hover {
            box-shadow: 0 8px 25px rgba(127, 90, 240, 0.6);
            transform: translateY(-3px) scale(1.02);
        }
        .btn-secondary {
            background-color: rgba(52, 52, 71, 0.5); /* Darker, semi-transparent */
            color: #C0C0C0; /* Lighter gray */
            border-color: rgba(127, 90, 240, 0.5); /* Purple border */
        }
        .btn-secondary:hover {
            background-color: rgba(127, 90, 240, 0.3); /* Purple tint on hover */
            border-color: #7F5AF0;
            color: white;
            transform: translateY(-3px) scale(1.02);
        }

        .nav-link {
            transition: color 0.3s ease, transform 0.3s ease;
            position: relative;
        }
        .nav-link:hover {
            color: #9D7FEA; /* Lighter Purple */
            transform: translateY(-2px);
        }
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #9D7FEA;
            transition: width 0.3s ease;
        }
        .nav-link:hover::after {
            width: 100%;
        }
        .nav-link-active { /* Added for active link state */
            color: #9D7FEA !important;
            font-weight: 700;
        }
        .nav-link-active::after { /* Active link underline */
            width: 100%;
            background-color: #9D7FEA;
        }
        
        .pillar-card {
            background: rgba(26, 26, 46, 0.7); /* Darker card bg */
            border: 1px solid rgba(127, 90, 240, 0.3);
            border-radius: 1rem; /* rounded-2xl */
            padding: 2rem; /* p-8 */
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            backdrop-filter: blur(12px);
            position: relative;
            overflow: hidden;
            display: flex; /* Added for consistent height */
            flex-direction: column; /* Added for consistent height */
        }
        .pillar-card:hover {
            transform: translateY(-12px) scale(1.03);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4), 0 0 50px rgba(127, 90, 240, 0.5);
            border-color: #7F5AF0;
        }
        .pillar-icon-container {
            background: linear-gradient(145deg, rgba(127, 90, 240, 0.2), rgba(168, 85, 247, 0.2));
            border: 1px solid rgba(127, 90, 240, 0.3);
            box-shadow: 0 0 15px rgba(127, 90, 240, 0.3);
        }
        .pillar-card-content { /* Added for consistent height */
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }
        .pillar-card-content p {
            flex-grow: 1;
        }
        .pillar-card .btn { /* Button inside pillar card */
            margin-top: auto; /* Pushes button to the bottom */
        }


        .section-title-glow {
            text-shadow: 0 0 15px rgba(56, 189, 248, 0.5), 0 0 25px rgba(127, 90, 240, 0.3);
        }

        nav {
            background: rgba(10, 10, 15, 0.6);
            backdrop-filter: blur(15px);
            border-bottom: 1px solid rgba(127, 90, 240, 0.2);
        }
        #mobile-menu {
            transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out;
            background-color: rgba(10, 10, 15, 0.95); /* Darker for mobile menu */
            backdrop-filter: blur(15px);
        }

        .pulse-dot {
            display: inline-block;
            width: 8px;
            height: 8px;
            margin-right: 8px;
            border-radius: 50%;
            background-color: #22D3EE; /* Cyan for contrast */
            box-shadow: 0 0 0 0 rgba(34, 211, 238, 1);
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(34, 211, 238, 0.7); }
            70% { transform: scale(1); box-shadow: 0 0 0 10px rgba(34, 211, 238, 0); }
            100% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(34, 211, 238, 0); }
        }
        .section-container { /* Used for About section */
            background-color: rgba(26, 26, 46, 0.7);
            backdrop-filter: blur(12px);
            padding: 2rem;
            border-radius: 1rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.2);
            border: 1px solid rgba(127, 90, 240, 0.3);
        }
    </style>
</head>
<body class="antialiased">

    <nav class="fixed w-full z-50 top-0">
        <div class="max-w-screen-2xl mx-auto px-6 sm:px-8 lg:px-12">
            <div class="flex items-center justify-between h-24">
                <div class="flex-shrink-0">
                    <a href="#home" class="text-3xl font-bold transition-all duration-300 hover:opacity-80">
                        <span class="text-sky-400">CKY</span><span class="text-slate-100">Chain</span>
                    </a>
                </div>
                <div class="hidden md:flex items-center space-x-6">
                    <a href="#home" class="nav-link text-slate-200 hover:text-purple-400 text-base font-medium nav-link-active">Home</a>
                    <a href="#innovations" class="nav-link text-slate-200 hover:text-purple-400 text-base font-medium">Innovations</a>
                    <a href="#about" class="nav-link text-slate-200 hover:text-purple-400 text-base font-medium">About</a>
                    <button onclick="connectWallet()" class="btn btn-secondary !py-2.5 !px-5 text-sm ml-4">
                        <span class="pulse-dot"></span>Connect Wallet
                    </button>
                    <a href="#" class="btn btn-primary !py-2.5 !px-5 text-sm">Launch App</a>
                </div>
                <div class="md:hidden flex items-center">
                     <button onclick="connectWallet()" class="btn btn-secondary !py-2 !px-4 text-xs mr-3">
                        <span class="pulse-dot !w-1.5 !h-1.5 !mr-1.5"></span>Connect
                    </button>
                    <button id="mobile-menu-button" class="inline-flex items-center justify-center p-2 rounded-md text-slate-300 hover:text-white hover:bg-slate-700 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-purple-500" aria-expanded="false">
                        <span class="sr-only">Open main menu</span>
                        <svg class="block h-7 w-7" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" /></svg>
                        <svg class="hidden h-7 w-7" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" /></svg>
                    </button>
                </div>
            </div>
        </div>
        <div id="mobile-menu" class="md:hidden hidden opacity-0 transform -translate-y-4 border-t border-slate-700/50">
            <div class="px-4 pt-4 pb-6 space-y-3 sm:px-5">
                <a href="#home" class="nav-link-mobile text-slate-200 hover:bg-slate-700 hover:text-purple-400 block px-3 py-3 rounded-md text-lg font-medium nav-link-active">Home</a>
                <a href="#innovations" class="nav-link-mobile text-slate-200 hover:bg-slate-700 hover:text-purple-400 block px-3 py-3 rounded-md text-lg font-medium">Innovations</a>
                <a href="#about" class="nav-link-mobile text-slate-200 hover:bg-slate-700 hover:text-purple-400 block px-3 py-3 rounded-md text-lg font-medium">About</a>
                <div class="mt-6 pt-6 border-t border-slate-700">
                    <button onclick="connectWallet()" class="btn btn-secondary w-full mb-3 text-base"><span class="pulse-dot"></span>Connect Wallet</button>
                    <a href="#" class="btn btn-primary w-full text-base">Launch App</a>
                </div>
            </div>
        </div>
    </nav>

    <header id="home" class="min-h-screen flex items-center justify-center text-white relative overflow-hidden animated-gradient-bg">
        <div class="hero-bg-animation">
            <svg width="100%" height="100%" class="particle-1">
                <defs><filter id="glow"><feGaussianBlur stdDeviation="1.5" result="coloredBlur"/><feMerge><feMergeNode in="coloredBlur"/><feMergeNode in="SourceGraphic"/></feMerge></filter></defs>
                <path d="M0 50 Q100 0, 200 50 T400 50" stroke="rgba(127, 90, 240, 0.3)" filter="url(#glow)"/>
                <path d="M0 150 Q150 100, 300 150 T600 150" stroke="rgba(56, 189, 248, 0.3)" filter="url(#glow)"/>
            </svg>
             <svg width="100%" height="100%" class="particle-2">
                <path d="M50 0 Q0 100, 50 200 T50 400" stroke="rgba(168, 85, 247, 0.2)" filter="url(#glow)"/>
                <path d="M150 0 Q100 150, 150 300 T150 600" stroke="rgba(56, 189, 248, 0.2)" filter="url(#glow)"/>
            </svg>
        </div>

        <div class="relative z-10 max-w-screen-md mx-auto px-4 sm:px-6 lg:px-8 text-center py-24">
            <h1 class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl font-black tracking-tighter leading-tight">
                <span class="block bg-clip-text text-transparent bg-gradient-to-r from-sky-400 via-purple-400 to-pink-500">CKY CHAIN</span>
                <span class="block text-slate-100 mt-1 sm:mt-2 text-4xl sm:text-5xl md:text-6xl">The Quantum Nexus</span>
            </h1>
            <p class="mt-8 max-w-xl mx-auto text-lg sm:text-xl text-slate-300 leading-relaxed">
                Pioneering the next epoch of decentralized trust. CKY Chain delivers unparalleled performance, quantum-resistant security, and a revolutionary ecosystem for global innovation.
            </p>
            <div class="mt-12 flex flex-col sm:flex-row justify-center items-center space-y-5 sm:space-y-0 sm:space-x-6">
                <button onclick="connectWallet()" class="btn btn-primary text-lg w-full sm:w-auto !py-4 !px-8 shadow-2xl">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2.5" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1" /></svg>
                    Connect Wallet
                </button>
                <a href="#" class="btn btn-secondary text-lg w-full sm:w-auto !py-4 !px-8">Launch Platform</a>
            </div>
        </div>
    </header>

    <section id="innovations" class="py-24 sm:py-32 bg-opacity-20 bg-slate-800 relative future-tech-section">
        <div class="max-w-screen-xl mx-auto px-6 sm:px-8 lg:px-12">
            <div class="text-center mb-20">
                <h2 class="text-4xl sm:text-5xl font-bold text-white section-title-glow">Pillars of CKY Innovation</h2>
                <p class="mt-5 text-lg text-slate-400 max-w-2xl mx-auto">The core foundations driving the CKY Chain revolution, designed for unparalleled performance and a future-proof digital economy.</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
                <div class="pillar-card">
                    <div class="pillar-icon-container flex items-center justify-center h-20 w-20 rounded-xl text-amber-400 mb-8 flex-shrink-0">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10 section-icon" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M9 17.25v1.007a3 3 0 01-.879 2.122L7.5 21M9 17.25v-4.5M9 17.25H5.25M15 17.25v1.007a3 3 0 00.879 2.122L16.5 21m-2.25-3.75v-4.5m2.25 3.75H18.75M9 4.5v1.007a3 3 0 00.879 2.122L10.5 9M9 4.5V9m0-4.5h3.75m-3.75 0L7.5 3M15 4.5v1.007a3 3 0 01-.879 2.122L13.5 9m1.5-4.5V9m0-4.5H11.25m3.75 0L16.5 3M3.75 12.75h16.5M16.5 12.75a9 9 0 11-18 0 9 9 0 0118 0z" />
                        </svg>
                    </div>
                    <div class="pillar-card-content">
                        <h3 class="text-2xl font-semibold text-white mb-4">CKY Ultimate Exchange</h3>
                        <p class="text-slate-300 leading-relaxed mb-6">
                            Experience the world's most advanced, AI-enhanced digital asset exchange. Featuring quantum-resistant security, unparalleled liquidity across diverse asset classes, ultra-low latency, and the most comprehensive suite of trading tools for professionals and institutions.
                        </p>
                        <a href="#" class="btn btn-secondary !text-sm !py-2 !px-4 self-start">Discover Exchange Features</a>
                    </div>
                </div>

                <div class="pillar-card">
                    <div class="pillar-icon-container flex items-center justify-center h-20 w-20 rounded-xl text-sky-400 mb-8 flex-shrink-0">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10 section-icon" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M12 1.25C6.072 1.25 1.25 6.072 1.25 12S6.072 22.75 12 22.75 22.75 17.928 22.75 12 17.928 1.25 12 1.25zm0 1.5a9.25 9.25 0 100 18.5 9.25 9.25 0 000-18.5zm-4.125 8.5H12v4.125m5.625-5.625a1.5 1.5 0 10-3 0 1.5 1.5 0 003 0zm-8.25 0a1.5 1.5 0 10-3 0 1.5 1.5 0 003 0zM12 6.375a1.5 1.5 0 100-3 1.5 1.5 0 000 3z" />
                        </svg>
                    </div>
                     <div class="pillar-card-content">
                        <h3 class="text-2xl font-semibold text-white mb-4">Next-Gen Core Technology</h3>
                        <p class="text-slate-300 leading-relaxed mb-6">
                            CKY Chain's revolutionary protocol delivers superior node performance and scalability through custom consensus and parallel processing. Our modular architecture and proactive quantum-resistant cryptography ensure enduring security and future adaptability.
                        </p>
                         <a href="#" class="btn btn-secondary !text-sm !py-2 !px-4 self-start">Learn About Our Tech</a>
                    </div>
                </div>

                <div class="pillar-card">
                    <div class="pillar-icon-container flex items-center justify-center h-20 w-20 rounded-xl text-green-400 mb-8 flex-shrink-0">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10 section-icon" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M17.25 6.75L22.5 12l-5.25 5.25m-10.5 0L1.5 12l5.25-5.25m7.5-3l-4.5 16.5" />
                            <path stroke-linecap="round" stroke-linejoin="round" d="M12 21a9 9 0 100-18 9 9 0 000 18z" />
                             <path stroke-linecap="round" stroke-linejoin="round" d="M12 15a3 3 0 100-6 3 3 0 000 6z" />
                        </svg>
                    </div>
                    <div class="pillar-card-content">
                        <h3 class="text-2xl font-semibold text-white mb-4">Vibrant & Supportive Ecosystem</h3>
                        <p class="text-slate-300 leading-relaxed mb-6">
                           Fostering a dynamic network of dApps, developer tools, and community-driven projects. CKY Chain provides robust support, funding, and infrastructure for innovators building across DeFi, GameFi, NFTs, and beyond.
                        </p>
                        <a href="#" class="btn btn-secondary !text-sm !py-2 !px-4 self-start">Explore Ecosystem Projects</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="about" class="py-24 sm:py-32 bg-slate-900">
        <div class="max-w-screen-md mx-auto px-6 sm:px-8 lg:px-12 text-center">
            <h2 class="text-4xl sm:text-5xl font-bold text-white section-title-glow mb-8">About <span class="text-sky-400">CKY Chain</span></h2>
            <div class="section-container !max-w-2xl !mx-auto">
                <p class="text-lg text-slate-300 leading-relaxed">
                    CKY Chain is a revolutionary blockchain platform engineered for unparalleled scalability, quantum-resistant security, and a thriving developer-centric ecosystem. Our mission is to empower builders and users with the world's most advanced infrastructure for decentralized applications and the future of digital finance. We are committed to relentless innovation and fostering a global community dedicated to shaping the next generation of the internet.
                </p>
            </div>
        </div>
    </section>

    <section id="cta" class="py-24 sm:py-32 animated-gradient-bg">
        <div class="max-w-screen-md mx-auto px-6 sm:px-8 lg:px-12 text-center">
            <h2 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white">
                Step into the Future.
            </h2>
            <p class="mt-6 text-xl text-slate-200 leading-relaxed">
                Join the CKY Chain movement. Connect your wallet, launch our groundbreaking platform, and become part of a community building the quantum-ready decentralized world.
            </p>
            <div class="mt-12 flex flex-col sm:flex-row justify-center items-center space-y-5 sm:space-y-0 sm:space-x-6">
                 <button onclick="connectWallet()" class="btn btn-primary text-xl w-full sm:w-auto !py-4 !px-10 shadow-2xl">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1" /></svg>
                    Connect & Explore
                </button>
                <a href="#" class="btn btn-secondary text-xl w-full sm:w-auto !py-4 !px-10">Launch CKY App</a>
            </div>
        </div>
    </section>

    <footer class="bg-slate-900 border-t border-slate-700/50">
        <div class="max-w-screen-xl mx-auto py-16 px-6 sm:px-8 lg:px-12 text-center">
            <div class="flex justify-center space-x-8 mb-8">
                <a href="#" class="text-slate-400 hover:text-purple-400 transition-colors"><span class="sr-only">Twitter</span><svg class="h-7 w-7" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84" /></svg></a>
                <a href="#" class="text-slate-400 hover:text-purple-400 transition-colors"><span class="sr-only">GitHub</span><svg class="h-7 w-7" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.165 6.839 9.489.5.092.682-.217.682-.483 0-.237-.009-.868-.013-1.703-2.782.602-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.465-1.11-1.465-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.949 0-1.091.39-1.984 1.029-2.685-.103-.253-.446-1.27.098-2.647 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.336 1.909-1.296 2.747-1.026 2.747-1.026.546 1.377.202 2.394.1 2.647.64.701 1.028 1.594 1.028 2.685 0 3.848-2.338 4.692-4.568 4.942.359.308.678.92.678 1.852 0 1.338-.012 2.419-.012 2.746 0 .268.18.58.688.482A10.001 10.001 0 0022 12c0-5.523-4.477-10-10-10z" clip-rule="evenodd" /></svg></a>
                <a href="#" class="text-slate-400 hover:text-purple-400 transition-colors"><span class="sr-only">Discord</span><svg class="h-7 w-7" fill="currentColor" viewBox="0 0 24 24"><path d="M19.54 0c1.356 0 2.46 1.104 2.46 2.472v16.094c0 1.368-1.104 2.472-2.46 2.472H4.46C3.104 21.038 2 19.934 2 18.566V2.472C2 1.104 3.104 0 4.46 0h15.08zm-4.926 11.934c-.714 0-1.29.576-1.29 1.29s.576 1.29 1.29 1.29c.714 0 1.29-.576 1.29-1.29s-.576-1.29-1.29-1.29zm-4.74 0c-.714 0-1.29.576-1.29 1.29s.576 1.29 1.29 1.29c.714 0 1.29-.576 1.29-1.29s-.576-1.29-1.29-1.29zm8.882-4.062H5.244a.918.918 0 00-.918.93v8.276c0 .504.402.918.906.93h10.092c.828 0 1.836-.672 1.836-1.5V4.788c0-.504-.402-.918-.906-.918z"/></svg></a>
            </div>
            <p class="text-sm text-slate-500">
                &copy; <span id="currentYear"></span> CKY Chain Platform. All rights reserved. Architecting the Quantum Future.
            </p>
        </div>
    </footer>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/plugins/autoloader/prism-autoloader.min.js"></script>
    <script>
        Prism.plugins.autoloader.languages_path = 'https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/';

        // Mobile Menu Toggle
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        const openIcon = mobileMenuButton.querySelector('svg:first-child');
        const closeIcon = mobileMenuButton.querySelector('svg:last-child');

        mobileMenuButton.addEventListener('click', () => {
            const expanded = mobileMenuButton.getAttribute('aria-expanded') === 'true' || false;
            mobileMenuButton.setAttribute('aria-expanded', !expanded);
            openIcon.classList.toggle('hidden');
            closeIcon.classList.toggle('hidden');
            if (mobileMenu.classList.contains('hidden')) {
                mobileMenu.classList.remove('hidden', 'opacity-0', '-translate-y-4');
                mobileMenu.classList.add('opacity-100', 'translate-y-0');
            } else {
                mobileMenu.classList.add('opacity-0', '-translate-y-4');
                setTimeout(() => {
                    mobileMenu.classList.add('hidden');
                    mobileMenu.classList.remove('opacity-100', 'translate-y-0');
                }, 300);
            }
        });

        // Smooth scroll for navigation links & active link highlighting
        const navLinks = document.querySelectorAll('.nav-link');
        const mobileNavLinks = document.querySelectorAll('.nav-link-mobile');
        const sections = document.querySelectorAll('header[id], section[id]');

        function updateActiveLink() {
            let currentSectionId = 'home';
            const navHeight = document.querySelector('nav').offsetHeight + 20; 

            sections.forEach(section => {
                const sectionTop = section.offsetTop - navHeight;
                const sectionBottom = sectionTop + section.offsetHeight;
                if (window.scrollY >= sectionTop && window.scrollY < sectionBottom) {
                    currentSectionId = section.id;
                }
            });
            if ((window.innerHeight + window.scrollY) >= document.body.offsetHeight - 50) {
                if (sections.length > 0) {
                    currentSectionId = sections[sections.length - 1].id;
                }
            }

            navLinks.forEach(link => {
                link.classList.remove('nav-link-active');
                if (link.getAttribute('href') === `#${currentSectionId}`) {
                    link.classList.add('nav-link-active');
                }
            });
            mobileNavLinks.forEach(link => {
                link.classList.remove('nav-link-active');
                 if (link.getAttribute('href') === `#${currentSectionId}`) {
                    link.classList.add('nav-link-active');
                }
            });
        }

        window.addEventListener('scroll', updateActiveLink);
        document.addEventListener('DOMContentLoaded', () => {
            updateActiveLink();
            Prism.highlightAll();
        });

        function smoothScrollToTarget(targetId) {
            const targetElement = document.querySelector(targetId);
            if (targetElement) {
                const navHeight = document.querySelector('nav').offsetHeight;
                const targetPosition = targetElement.offsetTop - navHeight;
                window.scrollTo({
                    top: targetPosition,
                    behavior: 'smooth'
                });
            }
        }

        mobileNavLinks.forEach(link => {
            link.addEventListener('click', (e) => {
                if (link.getAttribute('href').startsWith('#')) {
                    e.preventDefault();
                    smoothScrollToTarget(link.getAttribute('href'));
                }
                if (!mobileMenu.classList.contains('hidden')) {
                    mobileMenuButton.click();
                }
            });
        });
        
        navLinks.forEach(link => {
            link.addEventListener('click', (e) => {
                if (link.getAttribute('href').startsWith('#')) {
                    e.preventDefault();
                    smoothScrollToTarget(link.getAttribute('href'));
                }
            });
        });

        document.getElementById('currentYear').textContent = new Date().getFullYear();

        // Placeholder for Connect Wallet functionality
        function connectWallet() {
            alert('Wallet connection functionality to be implemented.');
        }
    </script>

</body>
</html>

**zee254375/zee254375** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
