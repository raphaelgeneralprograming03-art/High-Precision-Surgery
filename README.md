
<html lang="pt-BR" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SAMS + SROS | Traumatologia e Cirurgia de Alta Precisão</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        sci: {
                            950: '#020617',
                            900: '#090d16',
                            800: '#111827',
                            700: '#1f2937',
                            cyan: '#06b6d4',
                            emerald: '#10b981',
                            amber: '#f59e0b',
                            rose: '#f43f5e'
                        }
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; }
        .font-mono { font-family: 'JetBrains Mono', monospace; }
        .glass-panel {
            background: rgba(15, 23, 42, 0.75);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(56, 189, 248, 0.15);
        }
        .glow-cyan {
            box-shadow: 0 0 25px rgba(6, 182, 212, 0.25);
        }
        .glow-emerald {
            box-shadow: 0 0 25px rgba(16, 185, 129, 0.25);
        }
        /* Custom scrollbar for terminal */
        ::-webkit-scrollbar {
            width: 6px;
            height: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #020617;
        }
        ::-webkit-scrollbar-thumb {
            background: #1e293b;
            border-radius: 3px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #06b6d4;
        }
    </style>
</head>
<body class="bg-sci-950 text-slate-100 min-h-screen flex flex-col overflow-x-hidden">

    <!-- Header / Navbar -->
    <header class="glass-panel border-b border-cyan-500/20 px-6 py-4 flex flex-wrap items-center justify-between gap-4 sticky top-0 z-50">
        <div class="flex items-center space-x-3">
            <div class="relative flex items-center justify-center w-10 h-10 rounded-xl bg-cyan-950 border border-cyan-500/50 glow-cyan">
                <svg class="w-6 h-6 text-cyan-400 animate-pulse" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z"/>
                </svg>
            </div>
            <div>
                <h1 class="text-lg font-bold tracking-wider text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-emerald-400">SAMS + SROS SYSTEM</h1>
                <p class="text-xs text-slate-400 font-mono">Traumatologia & Cirurgia Nanométrica de Alta Precisão</p>
            </div>
        </div>

        <!-- System Status Pills -->
        <div class="flex items-center gap-3 text-xs font-mono flex-wrap">
            <div class="flex items-center gap-2 px-3 py-1.5 rounded-full bg-slate-900 border border-slate-700">
                <span id="sros-status-dot" class="w-2.5 h-2.5 rounded-full bg-emerald-500 animate-ping"></span>
                <span>SROS AI: <strong class="text-emerald-400">ATIVO (0.001µm)</strong></span>
            </div>
            <div class="flex items-center gap-2 px-3 py-1.5 rounded-full bg-slate-900 border border-slate-700">
                <span id="sams-status-dot" class="w-2.5 h-2.5 rounded-full bg-cyan-500"></span>
                <span>SAMS Amortecimento: <strong id="sams-status-text" class="text-cyan-400">100% BLINDADO</strong></span>
            </div>
            <div class="flex items-center gap-2 px-3 py-1.5 rounded-full bg-slate-900 border border-slate-700">
                <span class="w-2 h-2 rounded-full bg-purple-500"></span>
                <span>Sync Quântico: <strong class="text-purple-400">99.999%</strong></span>
            </div>
        </div>
    </header>

    <!-- Main Workspace -->
    <main class="flex-1 grid grid-cols-1 lg:grid-cols-12 gap-6 p-6 max-w-[1700px] mx-auto w-full">
        
        <!-- Left Sidebar: Control Panel & Environment -->
        <section class="lg:col-span-3 flex flex-col gap-6">
            
            <!-- Environment Selection -->
            <div class="glass-panel rounded-2xl p-5 shadow-xl">
                <h2 class="text-sm font-semibold tracking-wide text-cyan-400 uppercase mb-4 flex items-center gap-2">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
                    Ambiente Cirúrgico
                </h2>
                <div class="space-y-3">
                    <button onclick="setEnvironment('space')" id="env-space" class="w-full text-left p-3 rounded-xl border border-cyan-500/40 bg-cyan-500/10 transition-all hover:bg-cyan-500/20 flex items-center justify-between group">
                        <div>
                            <div class="font-semibold text-sm text-cyan-300">Ambulância Espacial</div>
                            <div class="text-xs text-slate-400">Gravidade zero / Turbulência orbital</div>
                        </div>
                        <span class="w-2 h-2 rounded-full bg-cyan-400"></span>
                    </button>
                    <button onclick="setEnvironment('warzone')" id="env-warzone" class="w-full text-left p-3 rounded-xl border border-slate-700 bg-slate-900/60 transition-all hover:border-amber-500/40 flex items-center justify-between group">
                        <div>
                            <div class="font-semibold text-sm text-slate-200 group-hover:text-amber-300">Zona de Combate</div>
                            <div class="text-xs text-slate-400">Tremores sísmicos 7.5 Richter</div>
                        </div>
                        <span class="w-2 h-2 rounded-full bg-slate-600" id="dot-warzone"></span>
                    </button>
                    <button onclick="setEnvironment('nano')" id="env-nano" class="w-full text-left p-3 rounded-xl border border-slate-700 bg-slate-900/60 transition-all hover:border-emerald-500/40 flex items-center justify-between group">
                        <div>
                            <div class="font-semibold text-sm text-slate-200 group-hover:text-emerald-300">Cirurgia Celular Pura</div>
                            <div class="text-xs text-slate-400">Reparo de DNA e Micro-vasos</div>
                        </div>
                        <span class="w-2 h-2 rounded-full bg-slate-600" id="dot-nano"></span>
                    </button>
                </div>
            </div>

            <!-- SAMS Control Unit -->
            <div class="glass-panel rounded-2xl p-5 shadow-xl border-cyan-500/30">
                <div class="flex items-center justify-between mb-4">
                    <h2 class="text-sm font-semibold tracking-wide text-cyan-400 uppercase flex items-center gap-2">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/></svg>
                        Mecanismo SAMS
                    </h2>
                    <span id="sams-badge" class="px-2.5 py-0.5 rounded text-xs font-mono font-bold bg-cyan-500/20 text-cyan-300 border border-cyan-500/40">LIGADO</span>
                </div>
                
                <div class="space-y-4">
                    <div class="flex items-center justify-between bg-slate-900/80 p-3 rounded-xl border border-slate-800">
                        <div>
                            <div class="text-xs font-medium text-slate-300">Anulação de Vibração</div>
                            <div class="text-[10px] text-slate-400 font-mono">Microbianas & Sísmicas</div>
                        </div>
                        <label class="relative inline-flex items-center cursor-pointer">
                            <input type="checkbox" id="samsToggle" checked onchange="toggleSAMS()" class="sr-only peer">
                            <div class="w-11 h-6 bg-slate-700 peer-focus:outline-none rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-cyan-500"></div>
                        </label>
                    </div>

                    <div>
                        <div class="flex justify-between text-xs mb-1 font-mono">
                            <span class="text-slate-400">Intensidade do Tremor Externo</span>
                            <span id="intensity-val" class="text-amber-400">65%</span>
                        </div>
                        <input type="range" id="motionIntensity" min="10" max="100" value="65" oninput="updateIntensity(this.value)" class="w-full h-2 bg-slate-800 rounded-lg appearance-none cursor-pointer accent-cyan-400">
                    </div>

                    <div>
                        <div class="flex justify-between text-xs mb-1 font-mono">
                            <span class="text-slate-400">Frequência Óptica SROS</span>
                            <span class="text-emerald-400">4.8 THz</span>
                        </div>
                        <input type="range" min="1" max="10" value="8" class="w-full h-2 bg-slate-800 rounded-lg appearance-none cursor-pointer accent-emerald-400">
                    </div>
                </div>
            </div>

            <!-- Action Triggers -->
            <div class="glass-panel rounded-2xl p-5 shadow-xl flex flex-col gap-3">
                <h2 class="text-sm font-semibold tracking-wide text-cyan-400 uppercase mb-1">Protocolos Clínicos</h2>
                <button onclick="triggerLaserBeam()" class="w-full py-3 px-4 rounded-xl bg-gradient-to-r from-cyan-600 to-emerald-600 hover:from-cyan-500 hover:to-emerald-500 text-white font-semibold text-sm shadow-lg shadow-cyan-900/30 transition-all flex items-center justify-center gap-2">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"/></svg>
                    Disparar Nanocauterização a Laser
                </button>
                <button onclick="recalibrateSystem()" class="w-full py-2.5 px-4 rounded-xl bg-slate-900 hover:bg-slate-800 border border-slate-700 text-slate-300 font-medium text-xs transition-all flex items-center justify-center gap-2">
                    <svg class="w-4 h-4 text-cyan-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15"/></svg>
                    Recalibrar Giroscópios SROS
                </button>
            </div>

        </section>

        <!-- Center: Canvas 2D Simulation Viewport -->
        <section class="lg:col-span-6 flex flex-col gap-6">
            <div class="glass-panel rounded-2xl p-4 shadow-2xl relative flex flex-col overflow-hidden border-cyan-500/30">
                
                <!-- Viewport Header HUD -->
                <div class="flex items-center justify-between pb-3 mb-3 border-b border-slate-800 text-xs font-mono">
                    <div class="flex items-center gap-2">
                        <span class="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span>
                        <span class="text-slate-300">VISÃO CELULAR EM TEMPO REAL (X1,000,000)</span>
                    </div>
                    <div class="flex items-center gap-4 text-slate-400">
                        <span>Alvo: <strong id="hud-target" class="text-cyan-400">TECIDO NERVIOSO #409</strong></span>
                        <span>Erro: <strong id="hud-error" class="text-emerald-400">0.000 µm</strong></span>
                    </div>
                </div>

                <!-- Canvas Container -->
                <div class="relative w-full aspect-[4/3] bg-slate-950 rounded-xl overflow-hidden border border-slate-800 shadow-inner">
                    <canvas id="simCanvas" class="w-full h-full block cursor-crosshair"></canvas>
                    
                    <!-- Holographic Target Reticle Overlay / Instructions -->
                    <div class="absolute bottom-4 left-4 pointer-events-none bg-slate-900/80 backdrop-blur-md px-3 py-2 rounded-lg border border-cyan-500/30 text-[11px] font-mono text-cyan-300">
                        <div>🖱️ Mova o cursor para guiar o SROS</div>
                        <div>⚡ Clique na tela para focar o micro-alvo</div>
                    </div>

                    <!-- Warning Banner if SAMS is OFF -->
                    <div id="sams-warning" class="absolute top-4 inset-x-4 pointer-events-none hidden transition-all duration-300">
                        <div class="bg-rose-950/90 border border-rose-500 text-rose-200 px-4 py-2 rounded-xl text-xs font-mono font-bold flex items-center justify-center gap-2 animate-bounce">
                            <svg class="w-4 h-4 text-rose-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"/></svg>
                            ALERTA: SAMS DESLIGADO! VIBRAÇÕES EXTERNAS COMPROMETENDO A PRECISÃO NANOMÉTRICA!
                        </div>
                    </div>
                </div>

                <!-- Simulation Quick Metrics Bar -->
                <div class="grid grid-cols-3 gap-3 mt-4 text-center font-mono">
                    <div class="bg-slate-900/60 p-2.5 rounded-xl border border-slate-800">
                        <div class="text-[10px] text-slate-400">Estabilidade do Bisturi</div>
                        <div id="metric-stability" class="text-sm font-bold text-cyan-400">100.0%</div>
                    </div>
                    <div class="bg-slate-900/60 p-2.5 rounded-xl border border-slate-800">
                        <div class="text-[10px] text-slate-400">Desvio Espacial</div>
                        <div id="metric-deviation" class="text-sm font-bold text-emerald-400">0.000 µm</div>
                    </div>
                    <div class="bg-slate-900/60 p-2.5 rounded-xl border border-slate-800">
                        <div class="text-[10px] text-slate-400">Reparo Celular</div>
                        <div id="metric-repair" class="text-sm font-bold text-purple-400">99.8%</div>
                    </div>
                </div>

            </div>
        </section>

        <!-- Right Sidebar: Telemetry, Patient Vitals & SROS AI Console -->
        <section class="lg:col-span-3 flex flex-col gap-6">
            
            <!-- Patient Vitals -->
            <div class="glass-panel rounded-2xl p-5 shadow-xl">
                <h2 class="text-sm font-semibold tracking-wide text-cyan-400 uppercase mb-4 flex items-center gap-2">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"/></svg>
                    Sinais Vitais do Paciente
                </h2>
                <div class="space-y-3 font-mono text-xs">
                    <div class="flex justify-between items-center bg-slate-900/80 p-2.5 rounded-xl border border-slate-800">
                        <span class="text-slate-400">Frequência Cardíaca</span>
                        <span class="text-emerald-400 font-bold">72 BPM</span>
                    </div>
                    <div class="flex justify-between items-center bg-slate-900/80 p-2.5 rounded-xl border border-slate-800">
                        <span class="text-slate-400">Estabilidade Neural</span>
                        <span class="text-cyan-400 font-bold">99.4%</span>
                    </div>
                    <div class="flex justify-between items-center bg-slate-900/80 p-2.5 rounded-xl border border-slate-800">
                        <span class="text-slate-400">Integridade Celular</span>
                        <span class="text-purple-400 font-bold">98.9%</span>
                    </div>
                    <div class="flex justify-between items-center bg-slate-900/80 p-2.5 rounded-xl border border-slate-800">
                        <span class="text-slate-400">Pressão Intracraniana</span>
                        <span class="text-amber-400 font-bold">11.2 mmHg</span>
                    </div>
                </div>
            </div>

            <!-- SROS AI Telemetry Log Console -->
            <div class="glass-panel rounded-2xl p-5 shadow-xl flex flex-col flex-1 min-h-[260px]">
                <h2 class="text-sm font-semibold tracking-wide text-cyan-400 uppercase mb-3 flex items-center gap-2">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 9l3 3-3 3m5 0h3M5 20h14a2 2 0 002-2V6a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"/></svg>
                    Console SROS AI Telemetry
                </h2>
                <div id="ai-console" class="flex-1 bg-slate-950/80 rounded-xl p-3 border border-slate-900 font-mono text-[11px] text-slate-300 space-y-1.5 overflow-y-auto max-h-[220px]">
                    <div class="text-slate-500">[00:00:01] SROS AI inicializado com sucesso.</div>
                    <div class="text-cyan-400">[00:00:03] SAMS miniaturizado ativado: 100% micro-vibrações anuladas.</div>
                    <div class="text-emerald-400">[00:00:05] Mapeamento óptico celular nanométrico concluído.</div>
                </div>
            </div>

        </section>

    </main>

    <!-- Footer -->
    <footer class="text-center py-4 text-xs text-slate-500 border-t border-slate-900 font-mono">
        SAMS (Smart Active Micro-Vibration Suppression) & SROS (Spatial Robotic Optical System) &bull; Simulação Cirúrgica Avançada v3.4
    </footer>

    <!-- JavaScript Simulation Engine -->
    <script>
        // --- Simulation State ---
        let state = {
            environment: 'space', // 'space', 'warzone', 'nano'
            samsActive: true,
            motionIntensity: 65,
            mouseX: 0,
            mouseY: 0,
            targetX: 0,
            targetY: 0,
            scalpelX: 0,
            scalpelY: 0,
            cells: [],
            particles: [],
            time: 0,
            laserActive: false,
            laserTimer: 0
        };

        // DOM Elements
        const canvas = document.getElementById('simCanvas');
        const ctx = canvas.getContext('2d');
        const samsToggleEl = document.getElementById('samsToggle');
        const samsBadgeEl = document.getElementById('sams-badge');
        const samsStatusTextEl = document.getElementById('sams-status-text');
        const samsWarningEl = document.getElementById('sams-warning');
        const hudErrorEl = document.getElementById('hud-error');
        const metricStabilityEl = document.getElementById('metric-stability');
        const metricDeviationEl = document.getElementById('metric-deviation');
        const aiConsole = document.getElementById('ai-console');

        // Initialize Audio (Web Audio API for Sci-Fi sound effects)
        let audioCtx = null;
        function initAudio() {
            if (!audioCtx) {
                audioCtx = new (window.AudioContext || window.webkitAudioContext)();
            }
        }

        function playSciFiBeep(freq = 440, type = 'sine', duration = 0.1) {
            try {
                initAudio();
                if (!audioCtx) return;
                const osc = audioCtx.createOscillator();
                const gain = audioCtx.createGain();
                osc.type = type;
                osc.frequency.value = freq;
                gain.gain.setValueAtTime(0.05, audioCtx.currentTime);
                gain.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime + duration);
                osc.connect(gain);
                gain.connect(audioCtx.destination);
                osc.start();
                osc.stop(audioCtx.currentTime + duration);
            } catch (e) {
                // Audio context policy ignored or not allowed
            }
        }

        // Initialize Cells and Grid
        function initCells() {
            state.cells = [];
            for (let i = 0; i < 40; i++) {
                state.cells.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    radius: 15 + Math.random() * 25,
                    vx: (Math.random() - 0.5) * 0.5,
                    vy: (Math.random() - 0.5) * 0.5,
                    health: 80 + Math.random() * 20,
                    type: Math.random() > 0.3 ? 'healthy' : 'damaged'
                });
            }
            state.targetX = canvas.width / 2;
            state.targetY = canvas.height / 2;
            state.scalpelX = state.targetX;
            state.scalpelY = state.targetY;
        }

        // Resize Canvas dynamically
        function resizeCanvas() {
            const rect = canvas.getBoundingClientRect();
            canvas.width = rect.width * window.devicePixelRatio;
            canvas.height = rect.height * window.devicePixelRatio;
            ctx.scale(window.devicePixelRatio, window.devicePixelRatio);
            if (state.cells.length === 0) initCells();
        }

        window.addEventListener('resize', resizeCanvas);

        // Control Handlers
        function setEnvironment(env) {
            state.environment = env;
            ['space', 'warzone', 'nano'].forEach(e => {
                const btn = document.getElementById(`env-${e}`);
                if (e === env) {
                    btn.className = "w-full text-left p-3 rounded-xl border border-cyan-500/40 bg-cyan-500/10 transition-all flex items-center justify-between group";
                } else {
                    btn.className = "w-full text-left p-3 rounded-xl border border-slate-700 bg-slate-900/60 transition-all hover:border-slate-500 flex items-center justify-between group";
                }
            });
            logAI(`Ambiente alterado para: ${env.toUpperCase()}. SROS reajustando matriz óptica.`);
            playSciFiBeep(600, 'triangle', 0.15);
        }

        function toggleSAMS() {
            state.samsActive = samsToggleEl.checked;
            if (state.samsActive) {
                samsBadgeEl.textContent = "LIGADO";
                samsBadgeEl.className = "px-2.5 py-0.5 rounded text-xs font-mono font-bold bg-cyan-500/20 text-cyan-300 border border-cyan-500/40";
                samsStatusTextEl.textContent = "100% BLINDADO";
                samsWarningEl.classList.add('hidden');
                logAI("SAMS reativado: Anulação de 100% de vibrações microbianas e sísmicas.");
                playSciFiBeep(880, 'sine', 0.2);
            } else {
                samsBadgeEl.textContent = "DESLIGADO";
                samsBadgeEl.className = "px-2.5 py-0.5 rounded text-xs font-mono font-bold bg-rose-500/20 text-rose-300 border border-rose-500/40";
                samsStatusTextEl.textContent = "VULNERÁVEL";
                samsWarningEl.classList.remove('hidden');
                logAI("ALERTA: SAMS desativado! Tremores sem amortecimento.");
                playSciFiBeep(220, 'sawtooth', 0.3);
            }
        }

        function updateIntensity(val) {
            state.motionIntensity = parseInt(val);
            document.getElementById('intensity-val').textContent = val + '%';
        }

        function triggerLaserBeam() {
            state.laserActive = true;
            state.laserTimer = 40;
            logAI("⚡ Disparo de Laser Nanométrico acionado pelo SROS no micro-alvo.");
            playSciFiBeep(1200, 'square', 0.25);
            
            // Add repair particles
            for (let i = 0; i < 25; i++) {
                state.particles.push({
                    x: state.scalpelX,
                    y: state.scalpelY,
                    vx: (Math.random() - 0.5) * 4,
                    vy: (Math.random() - 0.5) * 4,
                    life: 1.0,
                    color: '#10b981'
                });
            }
        }

        function recalibrateSystem() {
            logAI("🔄 Giroscópios SROS recalibrados. Alinhamento sub-micrométrico perfeito.");
            playSciFiBeep(750, 'sine', 0.2);
        }

        function logAI(message) {
            const timeStr = new Date().toTimeString().split(' ')[0];
            const div = document.createElement('div');
            div.className = "text-slate-300";
            div.innerHTML = `<span class="text-slate-500">[${timeStr}]</span> ${message}`;
            aiConsole.appendChild(div);
            aiConsole.scrollTop = aiConsole.scrollHeight;
        }

        // Canvas Mouse tracking
        canvas.addEventListener('mousemove', (e) => {
            const rect = canvas.getBoundingClientRect();
            state.mouseX = e.clientX - rect.left;
            state.mouseY = e.clientY - rect.top;
        });

        canvas.addEventListener('click', (e) => {
            const rect = canvas.getBoundingClientRect();
            state.targetX = e.clientX - rect.left;
            state.targetY = e.clientY - rect.top;
            playSciFiBeep(950, 'sine', 0.08);
            logAI(`Novo micro-alvo definido pelo cirurgião em X:${Math.round(state.targetX)} Y:${Math.round(state.targetY)}`);
        });

        // --- Main Animation & Simulation Loop ---
        function updateSimulation() {
            state.time += 0.03;

            // Calculate external tremor / vehicle motion offset
            let rawShakeX = 0;
            let rawShakeY = 0;
            const intensityFactor = state.motionIntensity / 50;

            if (state.environment === 'space') {
                rawShakeX = Math.sin(state.time * 8) * 15 * intensityFactor + Math.cos(state.time * 13) * 10 * intensityFactor;
                rawShakeY = Math.cos(state.time * 7) * 15 * intensityFactor + Math.sin(state.time * 11) * 10 * intensityFactor;
            } else if (state.environment === 'warzone') {
                // Seismic shocks
                const shock = Math.random() > 0.95 ? 35 : 5;
                rawShakeX = (Math.random() - 0.5) * shock * intensityFactor;
                rawShakeY = (Math.random() - 0.5) * shock * intensityFactor;
            } else if (state.environment === 'nano') {
                rawShakeX = Math.sin(state.time * 20) * 5 * intensityFactor;
                rawShakeY = Math.cos(state.time * 18) * 5 * intensityFactor;
            }

            // Apply SAMS dampening
            let finalShakeX = 0;
            let finalShakeY = 0;
            let precisionDeviation = 0;

            if (state.samsActive) {
                // 100% Damping -> Shake reduced to 0.000 µm
                finalShakeX = 0;
                finalShakeY = 0;
                precisionDeviation = 0.000;
                metricStability.textContent = "100.0%";
                metricStability.className = "text-sm font-bold text-cyan-400";
                metricDeviation.textContent = "0.000 µm";
                hudErrorEl.textContent = "0.000 µm";
            } else {
                // No SAMS -> Scalpel jumps wildly
                finalShakeX = rawShakeX;
                finalShakeY = rawShakeY;
                precisionDeviation = (Math.abs(rawShakeX) + Math.abs(rawShakeY)) * 12.4;
                metricStability.textContent = (Math.max(15, 100 - precisionDeviation / 5)).toFixed(1) + "%";
                metricStability.className = "text-sm font-bold text-rose-400";
                metricDeviation.textContent = precisionDeviation.toFixed(3) + " µm";
                hudErrorEl.textContent = precisionDeviation.toFixed(3) + " µm";
            }

            // Target position follows mouse with damping or erratic jumps
            let targetGoalX = state.mouseX || (canvas.clientWidth / 2);
            let targetGoalY = state.mouseY || (canvas.clientHeight / 2);

            if (state.mouseX === 0 && state.mouseY === 0) {
                targetGoalX = canvas.clientWidth / 2;
                targetGoalY = canvas.clientHeight / 2;
            }

            // Scalpel interpolation
            const lerp = 0.15;
            state.scalpelX += (targetGoalX - state.scalpelX) * lerp;
            state.scalpelY += (targetGoalY - state.scalpelY) * lerp;

            // Update cells
            state.cells.forEach(cell => {
                cell.x += cell.vx;
                cell.y += cell.vy;
                if (cell.x < 0 || cell.x > canvas.clientWidth) cell.vx *= -1;
                if (cell.y < 0 || cell.y > canvas.clientHeight) cell.vy *= -1;
            });

            // Update particles
            state.particles.forEach(p => {
                p.x += p.vx;
                p.y += p.vy;
                p.life -= 0.03;
            });
            state.particles = state.particles.filter(p => p.life > 0);

            if (state.laserActive) {
                state.laserTimer--;
                if (state.laserTimer <= 0) state.laserActive = false;
            }

            drawCanvas(finalShakeX, finalShakeY);
            requestAnimationFrame(updateSimulation);
        }

        function drawCanvas(shakeX, shakeY) {
            const width = canvas.clientWidth;
            const height = canvas.clientHeight;
            
            ctx.clearRect(0, 0, width, height);

            ctx.save();
            // Apply background tremor transform if SAMS is OFF
            ctx.translate(shakeX, shakeY);

            // Draw cellular background grid
            ctx.strokeStyle = 'rgba(6, 182, 212, 0.08)';
            ctx.lineWidth = 1;
            const gridSize = 40;
            for (let x = 0; x < width; x += gridSize) {
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, height);
                ctx.stroke();
            }
            for (let y = 0; y < height; y += gridSize) {
                ctx.beginPath();
                ctx.moveTo(0, y);
                ctx.lineTo(width, y);
                ctx.stroke();
            }

            // Draw biological tissue vessels / background veins
            ctx.strokeStyle = 'rgba(244, 63, 94, 0.15)';
            ctx.lineWidth = 12;
            ctx.beginPath();
            ctx.moveTo(0, height * 0.3);
            ctx.bezierCurveTo(width * 0.3, height * 0.1, width * 0.7, height * 0.7, width, height * 0.4);
            ctx.stroke();

            ctx.strokeStyle = 'rgba(16, 185, 129, 0.15)';
            ctx.lineWidth = 8;
            ctx.beginPath();
            ctx.moveTo(0, height * 0.7);
            ctx.bezierCurveTo(width * 0.4, height * 0.9, width * 0.6, height * 0.2, width, height * 0.8);
            ctx.stroke();

            // Draw cells
            state.cells.forEach(cell => {
                ctx.fillStyle = cell.type === 'healthy' ? 'rgba(16, 185, 129, 0.2)' : 'rgba(244, 63, 94, 0.25)';
                ctx.strokeStyle = cell.type === 'healthy' ? '#10b981' : '#f43f5e';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.arc(cell.x, cell.y, cell.radius, 0, Math.PI * 2);
                ctx.fill();
                ctx.stroke();

                // Nucleus
                ctx.fillStyle = cell.type === 'healthy' ? '#059669' : '#e11d48';
                ctx.beginPath();
                ctx.arc(cell.x, cell.y, cell.radius * 0.3, 0, Math.PI * 2);
                ctx.fill();
            });

            // Draw SAMS Forcefield Ripple (if ON)
            if (state.samsActive) {
                const ringRadius = 35 + Math.sin(state.time * 6) * 6;
                ctx.strokeStyle = 'rgba(6, 182, 212, 0.6)';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.arc(state.targetX, state.targetY, ringRadius, 0, Math.PI * 2);
                ctx.stroke();

                // Hexagon SAMS lock grid
                ctx.strokeStyle = 'rgba(6, 182, 212, 0.3)';
                ctx.beginPath();
                for (let i = 0; i < 6; i++) {
                    const angle = (i * Math.PI) / 3;
                    const hx = state.targetX + Math.cos(angle) * (ringRadius + 10);
                    const hy = state.targetY + Math.sin(angle) * (ringRadius + 10);
                    if (i === 0) ctx.moveTo(hx, hy);
                    else ctx.lineTo(hx, hy);
                }
                ctx.closePath();
                ctx.stroke();
            }

            // Draw Target Reticle
            ctx.strokeStyle = state.samsActive ? '#06b6d4' : '#f43f5e';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.arc(state.targetX, state.targetY, 15, 0, Math.PI * 2);
            ctx.moveTo(state.targetX - 22, state.targetY); ctx.lineTo(state.targetX - 8, state.targetY);
            ctx.moveTo(state.targetX + 8, state.targetY); ctx.lineTo(state.targetX + 22, state.targetY);
            ctx.moveTo(state.targetX, state.targetY - 22); ctx.lineTo(state.targetX, state.targetY - 8);
            ctx.moveTo(state.targetX, state.targetY + 8); ctx.lineTo(state.targetX, state.targetY + 22);
            ctx.stroke();

            // Draw Robotic Scalpel Arm & Nano-Blade
            const actualScalpelX = state.scalpelX + (state.samsActive ? 0 : shakeX);
            const actualScalpelY = state.scalpelY + (state.samsActive ? 0 : shakeY);

            // Robotic arm linkage lines
            ctx.strokeStyle = '#334155';
            ctx.lineWidth = 6;
            ctx.beginPath();
            ctx.moveTo(width / 2, 0);
            ctx.lineTo(actualScalpelX, actualScalpelY);
            ctx.stroke();

            // Scalpel Head
            ctx.fillStyle = '#06b6d4';
            ctx.beginPath();
            ctx.arc(actualScalpelX, actualScalpelY, 8, 0, Math.PI * 2);
            ctx.fill();

            // Nano-blade point
            ctx.strokeStyle = '#ffffff';
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.moveTo(actualScalpelX, actualScalpelY);
            ctx.lineTo(actualScalpelX + 12, actualScalpelY - 18);
            ctx.stroke();

            // Laser Beam (if active)
            if (state.laserActive) {
                ctx.strokeStyle = '#10b981';
                ctx.lineWidth = 4;
                ctx.shadowColor = '#10b981';
                ctx.shadowBlur = 15;
                ctx.beginPath();
                ctx.moveTo(actualScalpelX, actualScalpelY);
                ctx.lineTo(state.targetX, state.targetY);
                ctx.stroke();
                ctx.shadowBlur = 0; // reset
            }

            // Draw Repair Particles
            state.particles.forEach(p => {
                ctx.fillStyle = p.color;
                ctx.beginPath();
                ctx.arc(p.x, p.y, p.life * 3, 0, Math.PI * 2);
                ctx.fill();
            });

            ctx.restore();
        }

        // Initialize on load
        window.onload = function() {
            resizeCanvas();
            updateSimulation();
        };
    </script>
</body>
</html>
