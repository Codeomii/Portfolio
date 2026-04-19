<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Om Patel - AI Engineer & Data Specialist Portfolio">
    <title>Om Patel | AI & Data Systems</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@400;600;700&family=Fira+Code:wght@400;500&family=Inter:wght@300;400;600;800&display=swap');

        :root {
            --primary: #00ffcc;
            --bg-dark: #050608;
            --card-bg: rgba(13, 17, 23, 0.7);
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-dark);
            color: #f8fafc;
            overflow-x: hidden;
        }

        /* Perspective Background */
        #bgCanvas {
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            z-index: -1;
            background: linear-gradient(to bottom, #050608, #0a0c12);
        }

        /* Neon Glow Text */
        .hero-name {
            font-family: 'Fredoka', sans-serif;
            background: linear-gradient(135deg, #fff 30%, var(--primary) 100%);
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: drop-shadow(0 0 20px rgba(0, 255, 204, 0.3));
        }

        /* Modern Pop Card */
        .pop-card {
            background: var(--card-bg);
            border: 1px solid rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(12px);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .pop-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary);
            box-shadow: 0 15px 35px rgba(0, 255, 204, 0.15);
        }

        /* Reveal Animation */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        .cursor {
            display: inline-block;
            width: 3px;
            background-color: var(--primary);
            animation: blink 1s step-end infinite;
        }

        @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }
    </style>
</head>
<body class="selection:bg-[#00ffcc] selection:text-black">

    <canvas id="bgCanvas"></canvas>

    <nav class="fixed top-0 w-full z-50 border-b border-white/5 backdrop-blur-md">
        <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
            <div class="text-2xl font-bold tracking-tighter uppercase font-['Fredoka']">
                OM<span class="text-[#00ffcc]">.</span>PATEL
            </div>
            <div class="hidden md:flex gap-8 text-xs font-bold tracking-widest uppercase">
                <a href="#about" class="hover:text-[#00ffcc] transition-colors">About</a>
                <a href="#projects" class="hover:text-[#00ffcc] transition-colors">Projects</a>
                <a href="#contact" class="hover:text-[#00ffcc] transition-colors">Contact</a>
            </div>
            <button onclick="window.print()" class="px-5 py-2 rounded-full border border-[#00ffcc] text-[#00ffcc] text-xs font-bold hover:bg-[#00ffcc] hover:text-black transition-all">
                RESUME
            </button>
        </div>
    </nav>

    <section class="min-h-screen flex flex-col items-center justify-center text-center px-6">
        <div class="reveal active">
            <span class="px-4 py-1.5 rounded-full border border-white/10 bg-white/5 text-[10px] tracking-[0.3em] uppercase text-[#00ffcc] mb-6 inline-block">
                Systems Initialized
            </span>
            <h1 class="hero-name text-7xl md:text-9xl font-bold mb-6">OM PATEL</h1>
            <p class="text-xl md:text-2xl text-slate-400 font-light max-w-2xl mx-auto leading-relaxed">
                Building <span id="typewriter" class="text-white font-mono"></span><span class="cursor">&nbsp;</span>
            </p>
            <div class="mt-12 flex gap-6">
                <a href="#projects" class="px-8 py-4 bg-white text-black rounded-xl font-bold hover:bg-[#00ffcc] transition-all uppercase text-sm tracking-widest">
                    View Work
                </a>
            </div>
        </div>
    </section>

    <section id="projects" class="py-24 px-6 max-w-7xl mx-auto">
        <div class="mb-16 reveal">
            <h2 class="text-[#00ffcc] font-mono mb-2 uppercase tracking-widest text-sm">// Selected Repositories</h2>
            <h3 class="text-5xl font-bold">PROJECTS.</h3>
        </div>

        <div class="grid md:grid-cols-2 gap-8">
            <div class="pop-card p-8 rounded-3xl reveal">
                <div class="flex justify-between items-start mb-6">
                    <div class="w-12 h-12 bg-[#00ffcc]/10 rounded-xl flex items-center justify-center text-[#00ffcc]">
                        <i class="fa-solid fa-brain text-2xl"></i>
                    </div>
                    <span class="text-[10px] font-bold text-slate-500 uppercase tracking-widest">AI/ML</span>
                </div>
                <h4 class="text-2xl font-bold mb-4">Med-Scan OCR</h4>
                <p class="text-slate-400 mb-8 font-light">FastAPI and PaddleOCR based system for extracting medical data from reports with high accuracy.</p>
                <a href="#" class="text-xs font-bold uppercase tracking-widest flex items-center gap-2 hover:text-[#00ffcc]">
                    Source Code <i class="fa-solid fa-arrow-right-long"></i>
                </a>
            </div>

            <div class="pop-card p-8 rounded-3xl reveal">
                <div class="flex justify-between items-start mb-6">
                    <div class="w-12 h-12 bg-purple-500/10 rounded-xl flex items-center justify-center text-purple-400">
                        <i class="fa-solid fa-database text-2xl"></i>
                    </div>
                    <span class="text-[10px] font-bold text-slate-500 uppercase tracking-widest">DSA</span>
                </div>
                <h4 class="text-2xl font-bold mb-4">Daily POTD Engine</h4>
                <p class="text-slate-400 mb-8 font-light">Comprehensive collection of optimized LeetCode and GFG solutions with daily consistency tracking.</p>
                <a href="#" class="text-xs font-bold uppercase tracking-widest flex items-center gap-2 hover:text-purple-400">
                    Source Code <i class="fa-solid fa-arrow-right-long"></i>
                </a>
            </div>
        </div>
    </section>

    <footer id="contact" class="py-24 px-6 border-t border-white/5 bg-black/40">
        <div class="max-w-3xl mx-auto text-center reveal">
            <h3 class="text-4xl font-bold mb-8">Ready to start a <span class="text-[#00ffcc]">new project?</span></h3>
            <div class="flex flex-wrap justify-center gap-6">
                <a href="mailto:omp83075@gmail.com" class="text-slate-400 hover:text-white transition-colors">Email</a>
                <a href="https://linkedin.com/in/ompatel2610/" class="text-slate-400 hover:text-white transition-colors">LinkedIn</a>
                <a href="https://github.com/Codeomii" class="text-slate-400 hover:text-white transition-colors">GitHub</a>
            </div>
            <p class="mt-16 text-[10px] text-slate-600 uppercase tracking-[0.5em]">© 2026 Om Patel • Rohtak, India</p>
        </div>
    </footer>

    <script>
        // Typewriter Effect
        const phrases = ["Data Pipelines.", "ML Architectures.", "Optimized Logic.", "Scalable Systems."];
        let i = 0, j = 0, isDeleting = false;
        
        function type() {
            const target = document.getElementById('typewriter');
            const current = phrases[i];
            
            target.textContent = isDeleting ? current.substring(0, j--) : current.substring(0, j++);
            
            if (!isDeleting && j === current.length + 1) { isDeleting = true; setTimeout(type, 2000); }
            else if (isDeleting && j === 0) { isDeleting = false; i = (i + 1) % phrases.length; setTimeout(type, 500); }
            else { setTimeout(type, isDeleting ? 50 : 100); }
        }

        // Scroll Reveal
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('active'); });
        }, { threshold: 0.1 });

        document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

        // Background Animation (Simplified for performance)
        const canvas = document.getElementById('bgCanvas');
        const ctx = canvas.getContext('2d');
        let w, h;

        function resize() { w = canvas.width = window.innerWidth; h = canvas.height = window.innerHeight; }
        window.addEventListener('resize', resize);
        resize();

        function draw() {
            ctx.fillStyle = 'rgba(5, 6, 8, 0.2)';
            ctx.fillRect(0, 0, w, h);
            ctx.strokeStyle = 'rgba(0, 255, 204, 0.05)';
            ctx.lineWidth = 0.5;
            
            for(let i=0; i<30; i++) {
                ctx.beginPath();
                ctx.moveTo(w/2, -100);
                ctx.lineTo((w/30)*i, h+100);
                ctx.stroke();
            }
            requestAnimationFrame(draw);
        }

        type();
        draw();
    </script>
</body>
</html>
