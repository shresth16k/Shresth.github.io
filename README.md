
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Main Character Energy ✨</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Italiana&family=Montserrat:wght@300;400;500;600&family=Mr+Dafoe&display=swap" rel="stylesheet">
    
    <!-- Phosphor Icons -->
    <script src="https://unpkg.com/@phosphor-icons/web"></script>

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'sage': '#D3E4CD',
                        'cream': '#FDFCF6',
                        'blush': '#FFE5E5',
                        'clay': '#B4846C',
                        'charcoal': '#2D2D2D',
                        'lavender': '#E6E6FA',
                    },
                    fontFamily: {
                        'serif': ['Italiana', 'serif'],
                        'sans': ['Montserrat', 'sans-serif'],
                        'script': ['Mr Dafoe', 'cursive'],
                    },
                    animation: {
                        'float': 'float 6s ease-in-out infinite',
                        'spin-slow': 'spin 12s linear infinite',
                        'bounce-slow': 'bounce 2s infinite',
                        'pop-in': 'popIn 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-10px)' },
                        },
                        popIn: {
                            '0%': { opacity: '0', transform: 'scale(0.5)' },
                            '100%': { opacity: '1', transform: 'scale(1)' },
                        }
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Aesthetic Scrollbar */
        ::-webkit-scrollbar { width: 6px; }
        ::-webkit-scrollbar-track { background: #FDFCF6; }
        ::-webkit-scrollbar-thumb { background: #D3E4CD; border-radius: 10px; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }

        /* Tape & Polaroid */
        .tape { background-color: rgba(255, 255, 255, 0.6); box-shadow: 0 1px 3px rgba(0,0,0,0.1); backdrop-filter: blur(2px); transform: rotate(-2deg); position: absolute; z-index: 10; }
        .polaroid { background: white; padding: 12px 12px 35px 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.08); transition: transform 0.3s ease; }
        .polaroid:hover { transform: scale(1.02) rotate(1deg); z-index: 20; }

        /* Stickers */
        .sticker { position: absolute; cursor: move; user-select: none; touch-action: none; filter: drop-shadow(0 4px 6px rgba(0,0,0,0.1)); transition: transform 0.1s; }
        .sticker:active { transform: scale(1.1); }

        /* Confetti Animation */
        .confetti { position: fixed; width: 10px; height: 10px; background-color: #f00; animation: fall linear forwards; pointer-events: none; z-index: 999; }
        @keyframes fall { to { transform: translateY(100vh) rotate(720deg); } }

        /* Gift Box CSS */
        .gift-container { position: relative; width: 150px; height: 150px; cursor: pointer; transition: transform 0.3s; }
        .gift-container:active { transform: scale(0.95); }
        .gift-lid { position: absolute; top: -20px; left: -5px; width: 160px; height: 40px; background: #B4846C; border-radius: 4px; z-index: 20; transition: all 0.5s ease; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }
        .gift-lid::after { content: ''; position: absolute; left: 50%; transform: translateX(-50%); width: 20px; height: 100%; background: #FFE5E5; }
        .gift-box { position: absolute; bottom: 0; width: 150px; height: 130px; background: #D3E4CD; border-radius: 0 0 8px 8px; z-index: 10; overflow: hidden; box-shadow: 0 10px 20px rgba(0,0,0,0.05); }
        .gift-box::after { content: ''; position: absolute; left: 50%; transform: translateX(-50%); width: 20px; height: 100%; background: #FFE5E5; }
        .gift-bow { position: absolute; top: -50px; left: 50%; transform: translateX(-50%); width: 60px; height: 30px; z-index: 25; transition: all 0.5s ease; }
        .gift-bow::before, .gift-bow::after { content: ''; position: absolute; width: 30px; height: 30px; border: 4px solid #FFE5E5; border-radius: 50% 50% 0 50%; transform: rotate(45deg); top: 10px; }
        .gift-bow::after { transform: rotate(-45deg); left: 30px; border-radius: 50% 50% 50% 0; }

        /* Gift Open State */
        .gift-open .gift-lid { transform: translateY(-60px) rotate(-10deg); opacity: 0; }
        .gift-open .gift-bow { transform: translateX(-50%) translateY(-80px) rotate(-10deg); opacity: 0; }

        /* Cake Reveal */
        .cake-reveal { opacity: 0; transform: translateY(50px) scale(0.5); transition: all 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275); }
        .gift-open + .cake-reveal { opacity: 1; transform: translateY(-80px) scale(1); }

        body { background-image: radial-gradient(#D3E4CD 1px, transparent 1px); background-size: 20px 20px; }
    </style>
</head>
<body class="bg-cream text-charcoal font-sans overflow-hidden h-screen flex flex-col">

    <!-- Top Bar -->
    <header class="flex justify-between items-center p-5 z-50 bg-cream/80 backdrop-blur-sm sticky top-0 border-b border-sage/30">
        <div class="text-sm font-medium tracking-widest text-clay">19 & GLOWING</div>
        <h1 class="font-serif text-2xl tracking-wide">HER WORLD</h1>
        <button onclick="toggleMusic()" class="p-2 rounded-full hover:bg-sage/20 transition">
            <i class="ph ph-music-notes text-xl animate-pulse" id="musicIcon"></i>
        </button>
    </header>

    <!-- Main Content Area -->
    <main id="appContent" class="flex-1 overflow-y-auto relative no-scrollbar pb-24">
        
        <!-- SECTION 1: HOME -->
        <section id="home" class="page-section p-5 space-y-8 animate-fade-in">
            <div class="overflow-hidden whitespace-nowrap py-2 border-y border-sage/50 bg-white/50">
                <div class="inline-block animate-marquee text-xs font-bold tracking-[0.2em] text-clay uppercase">
                    Main Character Energy ✨ •  Level 19 Unlocked •  Romanticizing my life •  It Girl Era •
                </div>
            </div>

            <div class="relative mt-4">
                <div class="polaroid rotate-2 mx-auto max-w-[85%] relative bg-white">
                    <div class="aspect-[3/4] bg-gray-200 w-full overflow-hidden relative">
                         <img src="https://images.unsplash.com/photo-1516726817505-f5ed825624d8?q=80&w=600&auto=format&fit=crop" class="w-full h-full object-cover" alt="Main Character">
                         <div class="absolute inset-0 flex items-center justify-center text-gray-400 opacity-0 hover:opacity-100 transition duration-300 bg-black/20 text-xs font-bold uppercase tracking-widest">
                            Insert Us Here
                         </div>
                    </div>
                    <div class="font-script text-2xl text-center mt-3 text-clay transform -rotate-2">
                        Just iconic things 💋
                    </div>
                    <div class="tape w-24 h-6 -top-3 left-1/3"></div>
                </div>
            </div>

            <div class="text-center mt-8">
                <h2 class="font-serif text-3xl mb-2">Daily Affirmation</h2>
                <div id="affirmationBox" class="bg-white p-6 rounded-2xl border border-sage shadow-sm min-h-[100px] flex items-center justify-center relative overflow-hidden group">
                    <p id="affirmationText" class="text-lg font-medium italic text-gray-600">"Click for today's vibe"</p>
                    <div class="absolute -bottom-10 -right-10 w-24 h-24 bg-sage/30 rounded-full blur-xl group-hover:scale-150 transition duration-700"></div>
                </div>
                <button onclick="newAffirmation()" class="mt-4 px-8 py-3 bg-charcoal text-white rounded-full text-xs font-bold tracking-widest uppercase hover:bg-clay transition shadow-lg">
                    Claim Energy
                </button>
            </div>
        </section>

        <!-- SECTION 2: GALLERY -->
        <section id="gallery" class="page-section hidden p-4 pb-20">
            <h2 class="font-serif text-3xl text-center mb-6">The Aesthetic</h2>
            <div class="columns-2 gap-4 space-y-4">
                <div class="break-inside-avoid relative group">
                    <img src="https://images.unsplash.com/photo-1513201099705-a9746e1e201f?q=80&w=400&auto=format&fit=crop" class="rounded-xl w-full object-cover shadow-md" alt="Aesthetic">
                    <div class="absolute bottom-2 left-2 bg-white/80 px-2 py-1 rounded text-[10px] font-bold uppercase tracking-wide backdrop-blur-sm">POV: Us</div>
                </div>
                <div class="break-inside-avoid bg-sage/20 p-6 rounded-xl text-center flex flex-col justify-center items-center border border-sage">
                    <i class="ph ph-quotes text-3xl text-sage mb-2"></i>
                    <p class="font-serif text-lg leading-tight">"She was designed for the stars."</p>
                </div>
                <div class="break-inside-avoid relative mt-4">
                    <div class="polaroid rotate-1">
                        <img src="https://images.unsplash.com/photo-1492633423870-43d1cd2775eb?q=80&w=400&auto=format&fit=crop" class="w-full aspect-square object-cover grayscale hover:grayscale-0 transition" alt="Memory">
                        <p class="font-script text-xl text-center mt-2 text-gray-500">core memory</p>
                    </div>
                </div>
                <div class="break-inside-avoid relative mt-4">
                    <div class="polaroid -rotate-2 bg-blush/20">
                        <img src="https://images.unsplash.com/photo-1621789098261-d332d90a7479?q=80&w=400&auto=format&fit=crop" class="w-full aspect-[3/4] object-cover" alt="Fit check">
                        <p class="font-script text-xl text-center mt-2 text-pink-400">slay ✨</p>
                    </div>
                </div>
            </div>
            <div class="mt-8 text-center">
                 <p class="text-xs text-gray-400 tracking-widest uppercase">Scroll for more vibes</p>
                 <i class="ph ph-arrow-down text-gray-300 mt-2 animate-bounce"></i>
            </div>
        </section>

        <!-- SECTION 3: BIRTHDAY (NEW) -->
        <section id="birthday" class="page-section hidden p-0 h-full w-full flex flex-col items-center justify-center bg-gradient-to-b from-cream to-blush/30 overflow-hidden relative">
            
            <div id="gift-message-start" class="text-center mb-10 animate-float z-10">
                <span class="inline-block bg-white/60 backdrop-blur px-3 py-1 rounded-full text-[10px] font-bold tracking-widest text-clay mb-2">SPECIAL DELIVERY</span>
                <h2 class="font-serif text-4xl text-charcoal">Happy Birthday!</h2>
                <p class="font-script text-2xl text-sage mt-1">Make a wish...</p>
            </div>

            <!-- The Gift & Cake Container -->
            <div class="relative flex items-end justify-center h-[300px] w-full z-20">
                
                <!-- The Gift Box -->
                <div id="gift" class="gift-container animate-bounce-slow" onclick="openGift()">
                    <div class="gift-bow"></div>
                    <div class="gift-lid"></div>
                    <div class="gift-box"></div>
                </div>

                <!-- The Hidden Cake & Content -->
                <div class="cake-reveal absolute top-10 flex flex-col items-center">
                    <!-- Cute Cake SVG/Image -->
                    <div class="w-48 h-48 relative drop-shadow-xl">
                        <img src="https://images.unsplash.com/photo-1578985545062-69928b1d9587?q=80&w=500&auto=format&fit=crop" class="w-full h-full object-cover rounded-2xl border-4 border-white transform rotate-3" alt="Birthday Cake">
                        <div class="absolute -top-4 -right-4 bg-white p-2 rounded-full shadow-lg text-2xl animate-pulse">🎂</div>
                    </div>
                    
                    <div class="bg-white/90 backdrop-blur-md p-6 rounded-xl mt-6 text-center shadow-xl border border-white max-w-[280px]">
                        <h3 class="font-serif text-xl font-bold mb-2">Level 19 Unlocked 🔓</h3>
                        <p class="text-sm text-gray-600 leading-relaxed mb-4">
                            Another year hotter, smarter, and more iconic. The world isn't ready for your 19 era.
                        </p>
                        <button onclick="blowCandles(this)" class="bg-clay text-white px-6 py-2 rounded-full text-xs font-bold uppercase tracking-widest hover:bg-sage transition">
                            Blow Candles 🕯️
                        </button>
                    </div>
                </div>
            </div>

            <!-- Background Decorations -->
            <div class="absolute top-10 left-10 text-4xl opacity-20 animate-float" style="animation-delay: 1s">🎈</div>
            <div class="absolute bottom-32 right-10 text-4xl opacity-20 animate-float" style="animation-delay: 2s">✨</div>
            <div class="absolute top-1/2 left-5 text-2xl opacity-20 animate-float" style="animation-delay: 0.5s">🎀</div>

        </section>


        <!-- SECTION 4: CANVAS -->
        <section id="canvas" class="page-section hidden h-full w-full relative overflow-hidden bg-[#f0f0f0]">
            <div class="absolute top-4 left-4 z-10 bg-white/80 backdrop-blur px-4 py-2 rounded-full shadow-sm border border-gray-200">
                <p class="text-xs font-bold uppercase tracking-wider">Drag items to design ✨</p>
            </div>
            <div id="drag-area" class="w-full h-[80vh] relative touch-none">
                <div class="sticker left-[10%] top-[10%] w-40" data-x="0" data-y="0">
                     <div class="bg-white p-2 shadow-lg transform rotate-3">
                        <img src="https://images.unsplash.com/photo-1515378791036-0648a3ef77b2?q=80&w=300&auto=format&fit=crop" class="w-full pointer-events-none">
                        <p class="font-script text-center text-lg mt-1">Besties</p>
                     </div>
                </div>
                <div class="sticker left-[40%] top-[40%] bg-charcoal text-white p-4 rounded-full w-32 h-32 flex items-center justify-center text-center shadow-xl rotate-[-5deg]" data-x="0" data-y="0">
                    <p class="font-serif text-sm pointer-events-none">Start Romanticizing Your Life</p>
                </div>
                <div class="sticker left-[60%] top-[15%] text-5xl drop-shadow-md rotate-12" data-x="0" data-y="0">🦋</div>
                <div class="sticker left-[20%] top-[60%]" data-x="0" data-y="0">
                     <div class="w-24 h-24 bg-gradient-to-tr from-pink-300 to-blue-300 rounded-full border-4 border-white shadow-xl flex items-center justify-center animate-spin-slow">
                        <div class="w-8 h-8 bg-white rounded-full"></div>
                     </div>
                </div>
                <div class="sticker left-[70%] top-[70%] text-6xl text-yellow-400 drop-shadow-sm" data-x="0" data-y="0">✨</div>
            </div>
        </section>

        <!-- SECTION 5: MANIFEST -->
        <section id="manifest" class="page-section hidden p-6 pb-24">
            <h2 class="font-serif text-3xl mb-1">Manifestations</h2>
            <p class="text-xs text-gray-500 uppercase tracking-widest mb-6">Write it into existence</p>
            <div class="bg-white p-1 rounded-lg shadow-sm border border-gray-100 mb-6">
                <div class="bg-[#fffdde] p-6 rounded min-h-[300px] relative">
                    <div class="absolute top-0 right-0 p-4 opacity-50"><i class="ph ph-push-pin text-xl text-red-400"></i></div>
                    <h3 class="font-script text-2xl mb-4 text-gray-800">Bucket List...</h3>
                    <textarea id="journalInput" class="w-full bg-transparent border-none focus:ring-0 text-gray-700 font-serif text-lg leading-loose resize-none h-[250px]" placeholder="1. Go on a road trip with her&#10;2. Start a podcast&#10;3. Matcha dates every friday&#10;4. ..."></textarea>
                </div>
            </div>
            <button onclick="saveManifestation()" class="w-full py-4 bg-sage text-charcoal font-bold uppercase tracking-widest rounded-xl hover:bg-sage/80 transition flex items-center justify-center gap-2">
                <i class="ph ph-floppy-disk"></i> Save to Universe
            </button>
            <div id="saveMsg" class="text-center text-xs text-green-600 font-bold mt-2 opacity-0 transition">Saved! ✨</div>
        </section>

    </main>

    <!-- Bottom Navigation -->
    <nav class="fixed bottom-0 w-full bg-white/90 backdrop-blur-md border-t border-gray-100 px-4 py-4 flex justify-between items-center z-50 pb-8 safe-area-bottom">
        <button onclick="switchTab('home')" class="nav-btn active flex flex-col items-center gap-1 text-gray-400 hover:text-charcoal transition w-10 group">
            <i class="ph ph-house text-2xl group-[.active]:text-clay"></i>
            <span class="text-[8px] font-bold tracking-widest uppercase group-[.active]:text-clay">Home</span>
        </button>

        <button onclick="switchTab('gallery')" class="nav-btn flex flex-col items-center gap-1 text-gray-400 hover:text-charcoal transition w-10 group">
            <i class="ph ph-camera text-2xl group-[.active]:text-clay"></i>
            <span class="text-[8px] font-bold tracking-widest uppercase group-[.active]:text-clay">Pics</span>
        </button>

        <!-- Birthday Button (Center) -->
        <div class="relative -top-6">
             <button onclick="switchTab('birthday')" class="bg-gradient-to-r from-blush to-pink-200 text-charcoal rounded-full p-4 shadow-xl border-4 border-cream hover:scale-110 transition nav-btn group">
                <i class="ph ph-gift text-2xl animate-pulse"></i>
             </button>
        </div>

        <button onclick="switchTab('canvas')" class="nav-btn flex flex-col items-center gap-1 text-gray-400 hover:text-charcoal transition w-10 group">
            <i class="ph ph-star-four text-2xl group-[.active]:text-clay"></i>
            <span class="text-[8px] font-bold tracking-widest uppercase group-[.active]:text-clay">Art</span>
        </button>

        <button onclick="switchTab('manifest')" class="nav-btn flex flex-col items-center gap-1 text-gray-400 hover:text-charcoal transition w-10 group">
            <i class="ph ph-book-open text-2xl group-[.active]:text-clay"></i>
            <span class="text-[8px] font-bold tracking-widest uppercase group-[.active]:text-clay">Notes</span>
        </button>
    </nav>

    <!-- JS Logic -->
    <script>
        // --- Navigation ---
        function switchTab(tabId) {
            document.querySelectorAll('.page-section').forEach(el => el.classList.add('hidden'));
            document.getElementById(tabId).classList.remove('hidden');
            document.querySelectorAll('.nav-btn').forEach(btn => btn.classList.remove('active'));
            
            // Helper to highlight correct button (simple match)
            if(tabId === 'birthday') {
                 // Special handling for the center button if needed, but styling handles it mostly
            } else {
                const iconMap = { 'home': 'house', 'gallery': 'camera', 'canvas': 'star-four', 'manifest': 'book-open' };
                const iconClass = iconMap[tabId];
                // Simple logic to find active button visuals
            }
            document.getElementById('appContent').scrollTo(0,0);
        }

        // --- Affirmation ---
        const affirmations = ["Your vibe attracts your tribe.", "Main character energy only.", "You look iconic today.", "Everything works out in your favor.", "Radiating sun energy.", "Don't chase, attract."];
        function newAffirmation() {
            const textBox = document.getElementById('affirmationText');
            textBox.style.opacity = 0;
            setTimeout(() => {
                textBox.innerText = `"${affirmations[Math.floor(Math.random() * affirmations.length)]}"`;
                textBox.style.opacity = 1;
            }, 300);
        }

        // --- Birthday Logic ---
        function openGift() {
            const gift = document.getElementById('gift');
            
            // 1. Animate Box opening
            gift.classList.remove('animate-bounce-slow');
            gift.classList.add('gift-open');
            
            // 2. Trigger Confetti
            createConfetti();
            
            // 3. Hide the "Happy Birthday" initial text to clean up view
            const startMsg = document.getElementById('gift-message-start');
            startMsg.style.transition = "opacity 0.5s";
            startMsg.style.opacity = "0";
            setTimeout(() => startMsg.style.display = "none", 500);
        }

        function blowCandles(btn) {
            btn.innerText = "Wish Granted! ✨";
            btn.classList.remove('bg-clay', 'hover:bg-sage');
            btn.classList.add('bg-sage');
            createConfetti(); // More confetti!
        }

        function createConfetti() {
            const colors = ['#D3E4CD', '#FFE5E5', '#B4846C', '#FFD700', '#FF69B4'];
            for (let i = 0; i < 50; i++) {
                const conf = document.createElement('div');
                conf.classList.add('confetti');
                conf.style.left = Math.random() * 100 + 'vw';
                conf.style.top = -10 + 'px';
                conf.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                conf.style.animationDuration = (Math.random() * 3 + 2) + 's';
                document.body.appendChild(conf);
                
                // Cleanup
                setTimeout(() => conf.remove(), 5000);
            }
        }

        // --- Drag & Drop (Unified) ---
        const stickers = document.querySelectorAll('.sticker');
        stickers.forEach(sticker => {
            let isDragging = false, startX, startY, initialLeft, initialTop;

            const startDrag = (x, y) => {
                isDragging = true;
                startX = x;
                startY = y;
                initialLeft = sticker.offsetLeft;
                initialTop = sticker.offsetTop;
                sticker.style.zIndex = 100;
            };

            const moveDrag = (x, y) => {
                if (!isDragging) return;
                const deltaX = x - startX;
                const deltaY = y - startY;
                sticker.style.left = `${initialLeft + deltaX}px`;
                sticker.style.top = `${initialTop + deltaY}px`;
            };

            const endDrag = () => { isDragging = false; sticker.style.zIndex = ''; };

            // Touch
            sticker.addEventListener('touchstart', (e) => startDrag(e.touches[0].clientX, e.touches[0].clientY), {passive: true});
            window.addEventListener('touchmove', (e) => moveDrag(e.touches[0].clientX, e.touches[0].clientY), {passive: false});
            window.addEventListener('touchend', endDrag);

            // Mouse
            sticker.addEventListener('mousedown', (e) => startDrag(e.clientX, e.clientY));
            window.addEventListener('mousemove', (e) => moveDrag(e.clientX, e.clientY));
            window.addEventListener('mouseup', endDrag);
        });

        // --- Journal & Misc ---
        const journalInput = document.getElementById('journalInput');
        if (localStorage.getItem('manifestation_text')) journalInput.value = localStorage.getItem('manifestation_text');
        
        function saveManifestation() {
            localStorage.setItem('manifestation_text', journalInput.value);
            const msg = document.getElementById('saveMsg');
            msg.style.opacity = 1;
            setTimeout(() => msg.style.opacity = 0, 2000);
        }

        function toggleMusic() {
            const icon = document.getElementById('musicIcon');
            icon.classList.toggle('text-pink-400');
            icon.classList.toggle('animate-pulse');
        }

        // Init
        document.querySelector('.nav-btn').classList.add('active');
    </script>
</body>
</html>


