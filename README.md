<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AMINE EL ASSALY · modern profile + car game</title>
    <!-- Google Font & Font Awesome for clean icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0a0c10;
            font-family: 'Fira Code', monospace;
            color: #e6edf3;
            line-height: 1.6;
            padding: 2rem 1rem;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: #161b22;
            border-radius: 2rem;
            padding: 2rem 2rem 3rem;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.8), 0 0 0 1px rgba(14, 117, 182, 0.3);
            border: 1px solid #30363d;
        }

        /* modern glassmorphism touches */
        h1, h2, h3 {
            font-weight: 500;
            letter-spacing: -0.02em;
        }

        h1 {
            font-size: 3rem;
            background: linear-gradient(135deg, #0e75b6, #58a6ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 0.2rem;
        }

        .typing-svg-placeholder {
            background: #0d1117;
            padding: 0.8rem 1.5rem;
            border-radius: 60px;
            display: inline-block;
            margin: 0.8rem 0 1.5rem;
            border: 1px solid #30363d;
            box-shadow: 0 4px 12px rgba(0,0,0,0.5);
        }

        .typing-svg-placeholder svg {
            width: 100%;
            max-width: 600px;
            height: auto;
        }

        .badge-panel {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            justify-content: center;
            margin: 1.8rem 0 1rem;
        }

        .badge-panel img {
            border-radius: 12px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.6);
            transition: transform 0.2s ease;
        }

        .badge-panel img:hover {
            transform: scale(1.05);
        }

        .section-title {
            font-size: 2rem;
            font-weight: 600;
            margin: 2.5rem 0 1.5rem 0;
            border-left: 6px solid #0e75b6;
            padding-left: 1rem;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .section-title i {
            color: #0e75b6;
            font-size: 2rem;
        }

        .grid-connect {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin: 2rem 0;
        }

        .connect-btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: #21262d;
            padding: 0.8rem 1.8rem;
            border-radius: 40px;
            font-size: 1.2rem;
            font-weight: 500;
            color: white;
            text-decoration: none;
            border: 1px solid #3d444d;
            transition: all 0.2s;
            box-shadow: 0 6px 12px rgba(0,0,0,0.4);
        }

        .connect-btn:hover {
            background: #2d333c;
            border-color: #0e75b6;
            transform: translateY(-4px);
        }

        .tech-badge {
            display: inline-block;
            background: #1f242b;
            border-radius: 40px;
            padding: 0.4rem 1.2rem;
            margin: 0.4rem;
            font-size: 1.1rem;
            border: 1px solid #363c45;
            transition: 0.1s ease;
            box-shadow: 0 2px 6px rgba(0,0,0,0.5);
        }

        .tech-badge i {
            margin-right: 6px;
            color: #0e75b6;
        }

        .tech-cloud {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            background: #0d1117;
            padding: 2rem;
            border-radius: 60px;
            border: 1px solid #30363d;
        }

        .skill-progress {
            background: #161b22;
            padding: 1.6rem;
            border-radius: 48px;
            border: 1px solid #2d333b;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 16px;
        }

        .skill-progress span {
            background: #1a2634;
            padding: 0.6rem 1.6rem;
            border-radius: 30px;
            font-weight: 500;
            border: 1px solid #0e75b6;
            color: #b1c9e8;
        }

        .stats-container {
            display: flex;
            flex-wrap: wrap;
            gap: 24px;
            justify-content: center;
            margin: 2.5rem 0;
        }

        .stat-card {
            background: #0d1117;
            border-radius: 28px;
            padding: 1.2rem 1.8rem;
            border: 1px solid #2d333b;
            box-shadow: 0 12px 28px rgba(0,0,0,0.7);
            transition: all 0.2s;
        }

        .stat-card:hover {
            border-color: #0e75b6;
        }

        /* CAR GAME SECTION */
        .game-section {
            margin-top: 4rem;
            background: #0a0c10;
            border-radius: 48px;
            padding: 2rem 2rem 3rem;
            border: 2px solid #0e75b6;
            box-shadow: inset 0 0 20px rgba(14, 117, 182, 0.2), 0 20px 30px -10px black;
        }

        .game-header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-bottom: 1.5rem;
        }

        .game-title {
            font-size: 2.5rem;
            background: linear-gradient(145deg, #0e75b6, #c9d1d9);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .score-board {
            background: #1f2937;
            padding: 0.8rem 2rem;
            border-radius: 50px;
            font-size: 2rem;
            font-weight: 600;
            color: #ffd966;
            border: 1px solid #0e75b6;
        }

        .game-area {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        canvas#carCanvas {
            display: block;
            width: 100%;
            max-width: 800px;
            aspect-ratio: 16/9;
            background: #1e2a3a;
            border-radius: 28px;
            border: 3px solid #0e75b6;
            box-shadow: 0 30px 30px -10px black;
            cursor: none;
            margin: 1rem 0;
        }

        .game-controls {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
            justify-content: center;
            margin: 20px 0 5px;
            color: #9ca8b5;
        }

        .game-controls kbd {
            background: #242b33;
            border-radius: 8px;
            padding: 6px 14px;
            font-size: 1.5rem;
            border: 2px solid #0e75b6;
            color: white;
        }

        .restart-btn {
            background: #0e75b6;
            border: none;
            color: white;
            font-family: 'Fira Code', monospace;
            font-size: 1.3rem;
            font-weight: 600;
            padding: 0.8rem 2.5rem;
            border-radius: 60px;
            margin-top: 1.2rem;
            cursor: pointer;
            transition: 0.15s;
            box-shadow: 0 8px 0 #06314d;
            border: 1px solid #58a6ff;
        }

        .restart-btn:hover {
            background: #1a86cf;
            transform: translateY(-2px);
            box-shadow: 0 10px 0 #06314d;
        }

        .restart-btn:active {
            transform: translateY(4px);
            box-shadow: 0 4px 0 #06314d;
        }

        footer {
            text-align: center;
            margin-top: 3rem;
            opacity: 0.7;
        }

        /* Responsive */
        @media (max-width: 600px) {
            h1 { font-size: 2.4rem; }
        }
    </style>
</head>
<body>
<div class="container">
    
    <!-- HEADER with name and animated typing (SVG inline for reliability) -->
    <h1>👋 Hi, I'm AMINE EL ASSALY</h1>
    <div class="typing-svg-placeholder">
        <svg width="600" height="50" viewBox="0 0 600 50" fill="none" xmlns="http://www.w3.org/2000/svg">
            <style>
                @keyframes blink { 0%,100%{ opacity:1 } 50%{ opacity:0 } }
                .cursor { animation: blink 1s infinite; fill: #0e75b6; }
                .text-light { fill: #ccd6dd; font-size: 24px; font-family: 'Fira Code', monospace; }
            </style>
            <text x="20" y="35" class="text-light">A passionate Full Stack Developer <tspan fill="#0e75b6">|</tspan> From MOROCCO</text>
            <rect x="575" y="12" width="4" height="30" class="cursor" />
        </svg>
    </div>

    <!-- Profile views & trophy -->
    <p align="center" style="margin-bottom: 1.5rem;">
        <img src="https://komarev.com/ghpvc/?username=aminemoon&label=Profile%20views&color=0e75b6&style=flat-square" alt="views" style="border-radius: 20px;">
    </p>
    <div class="badge-panel">
        <img src="https://github-profile-trophy.vercel.app/?username=aminemoon&theme=onedark&no-frame=true&row=1&column=5" alt="trophy" style="max-width: 100%;">
    </div>

    <!-- About me section -->
    <div class="section-title"><i class="fas fa-user-astronaut"></i> 💡 About Me</div>
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px,1fr)); gap: 15px; background: #0d1117; padding: 2rem; border-radius: 48px;">
        <div><i class="fas fa-bolt" style="color: #0e75b6;"></i> 🔭 Working on <strong>Your Project Name</strong></div>
        <div><i class="fas fa-leaf" style="color: #0e75b6;"></i> 🌱 Learning <strong>Laravel framework</strong></div>
        <div><i class="fas fa-users" style="color: #0e75b6;"></i> 👯 Looking to collaborate on <strong>Hackathons</strong></div>
        <div><i class="fas fa-handshake" style="color: #0e75b6;"></i> 🤝 Seeking help with <strong>Your Need</strong></div>
        <div><i class="fas fa-pen" style="color: #0e75b6;"></i> 📝 Writing articles on <strong>My Blog</strong></div>
        <div><i class="fas fa-comment" style="color: #0e75b6;"></i> 💬 Ask me about <strong>Web Dev, Laravel</strong></div>
        <div><i class="fas fa-envelope" style="color: #0e75b6;"></i> 📫 Reach: <strong>contact@amine.dev</strong></div>
        <div><i class="fas fa-file" style="color: #0e75b6;"></i> 📄 Check my <strong>Resume</strong></div>
    </div>

    <!-- Projects -->
    <div class="section-title"><i class="fas fa-rocket"></i> 🚀 My Projects</div>
    <div style="display: flex; gap: 30px; flex-wrap: wrap; background: #0d1117; padding: 1.5rem 2rem; border-radius: 60px;">
        <span><i class="fas fa-store"></i> <a href="#" style="color: #58a6ff;">Front Office Ecommerce</a> (elassaly-amine.idsmobile.com)</span>
        <span><i class="fas fa-lock"></i> <a href="#" style="color: #58a6ff;">Back Office</a> (backoffice demo)</span>
    </div>

    <!-- Connect -->
    <div class="section-title"><i class="fas fa-globe"></i> 🌐 Connect with Me</div>
    <div class="grid-connect">
        <a href="#" class="connect-btn"><i class="fab fa-codepen"></i> CodePen</a>
        <a href="#" class="connect-btn"><i class="fab fa-linkedin"></i> LinkedIn</a>
        <a href="#" class="connect-btn"><i class="fab fa-youtube"></i> YouTube</a>
    </div>

    <!-- Languages & Tools badges (shields.io style) -->
    <div class="section-title"><i class="fas fa-code"></i> 🛠 Languages & Tools</div>
    <div style="text-align: center; margin: 1rem 0;">
        <span class="tech-badge"><i class="fab fa-cuttlefish"></i> C</span>
        <span class="tech-badge"><i class="fas fa-plus-circle"></i> C++</span>
        <span class="tech-badge"><i class="fab fa-html5"></i> HTML5</span>
        <span class="tech-badge"><i class="fab fa-css3-alt"></i> CSS3</span>
        <span class="tech-badge"><i class="fab fa-js"></i> JavaScript</span>
        <span class="tech-badge"><i class="fab fa-laravel"></i> Laravel</span>
        <span class="tech-badge"><i class="fab fa-php"></i> PHP</span>
        <span class="tech-badge"><i class="fab fa-node"></i> Node.js</span>
        <span class="tech-badge"><i class="fab fa-react"></i> React</span>
        <span class="tech-badge"><i class="fab fa-react"></i> React Native</span>
        <span class="tech-badge"><i class="fas fa-database"></i> MongoDB</span>
        <span class="tech-badge"><i class="fas fa-database"></i> PostgreSQL</span>
        <span class="tech-badge"><i class="fab fa-docker"></i> Docker</span>
        <span class="tech-badge"><i class="fab fa-linux"></i> Linux</span>
    </div>

    <!-- Skills progress (modern badges) -->
    <div class="section-title"><i class="fas fa-chart-line"></i> 📊 Skills Progress</div>
    <div class="skill-progress">
        <span>HTML 95%</span><span>CSS 90%</span><span>JS 85%</span><span>PHP 80%</span><span>Laravel 75%</span><span>React 70%</span><span>Node.js 65%</span>
    </div>

    <!-- Tech cloud with animated icons -->
    <div class="section-title"><i class="fas fa-cloud"></i> ☁️ Tech Cloud</div>
    <div class="tech-cloud">
        <img src="https://skillicons.dev/icons?i=html,css,js,php,laravel,nodejs,react,mongodb,postgres,docker,linux&perline=8" alt="tech stack">
    </div>

    <!-- GitHub stats cards (using placeholders / external) -->
    <div class="section-title"><i class="fas fa-chart-pie"></i> 📊 GitHub Stats</div>
    <div class="stats-container">
        <div class="stat-card"><img src="https://github-readme-stats.vercel.app/api/top-langs/?username=aminemoon&layout=compact&theme=radical" alt="top langs"></div>
        <div class="stat-card"><img src="https://github-readme-stats.vercel.app/api?username=aminemoon&show_icons=true&theme=radical" alt="stats"></div>
    </div>

    <!-- Contribution & visitors -->
    <div class="section-title"><i class="fas fa-fire"></i> 📈 Contribution & Visitors</div>
    <div class="stats-container" style="flex-direction: column; align-items: center;">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=aminemoon&theme=radical" alt="streak">
        <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=aminemoon&theme=radical" alt="summary" style="margin-top: 1rem;">
        <img src="https://visitor-badge.laobi.icu/badge?page_id=aminemoon.aminemoon" alt="visitor" style="margin-top: 1rem;">
    </div>

    <!-- ========== MODERN CAR GAME (embedded) ========== -->
    <div class="game-section">
        <div class="game-header">
            <span class="game-title"><i class="fas fa-car" style="color:#0e75b6;"></i> highway RACER · dodge cars</span>
            <div class="score-board" id="gameScore">0</div>
        </div>
        <div class="game-area">
            <canvas id="carCanvas" width="800" height="400"></canvas>
            <div class="game-controls">
                <span><kbd>←</kbd> move left</span>
                <span><kbd>→</kbd> move right</span>
                <span><i class="fas fa-rotate-right" style="color:#0e75b6;"></i> restart button below</span>
            </div>
            <button class="restart-btn" id="restartGame"><i class="fas fa-flag-checkered"></i> RESTART GAME</button>
            <p style="margin-top: 15px; font-size: 0.9rem;">⭐ avoid red cars · survive · modern arcade inside your profile</p>
        </div>
    </div>
    
    <footer>
        ⚡ Amine El Assaly · fullstack with style · car game included ⚡
    </footer>
</div>

<!-- GAME SCRIPT (modern js) -->
<script>
    (function() {
        const canvas = document.getElementById('carCanvas');
        const ctx = canvas.getContext('2d');
        const scoreSpan = document.getElementById('gameScore');

        // fixed dimensions
        const LANES = 3;
        const LANE_WIDTH = canvas.width / LANES;

        // player
        let player = {
            x: LANE_WIDTH * 1.5 - 30,  // middle lane
            y: canvas.height - 90,
            width: 50,
            height: 70,
            lane: 1  // 0=left,1=mid,2=right
        };

        // obstacles
        let obstacles = [];
        const OBSTACLE_WIDTH = 50;
        const OBSTACLE_HEIGHT = 70;
        const OBSTACLE_SPEED = 3.5;

        let score = 0;
        let gameActive = true;
        let animationFrame;
        let frameCounter = 0;
        const SPAWN_RATE = 40; // frames between spawns

        // control flags
        let leftPressed = false;
        let rightPressed = false;

        // reset everything
        function resetGame() {
            gameActive = true;
            obstacles = [];
            player.lane = 1;
            player.x = LANE_WIDTH * 1.5 - player.width/2; // 1.5 -> middle lane
            score = 0;
            scoreSpan.innerText = '0';
            frameCounter = 0;
        }

        // move player based on lanes
        function movePlayer() {
            if (!gameActive) return;
            if (leftPressed && player.lane > 0) {
                player.lane--;
            }
            if (rightPressed && player.lane < LANES - 1) {
                player.lane++;
            }
            // update x according to lane
            player.x = (player.lane * LANE_WIDTH) + (LANE_WIDTH/2) - player.width/2;
        }

        // spawn obstacle (red car)
        function spawnObstacle() {
            const lane = Math.floor(Math.random() * LANES);
            const x = (lane * LANE_WIDTH) + (LANE_WIDTH/2) - OBSTACLE_WIDTH/2;
            obstacles.push({
                x: x,
                y: -OBSTACLE_HEIGHT,
                width: OBSTACLE_WIDTH,
                height: OBSTACLE_HEIGHT,
                lane: lane
            });
        }

        // collision detection (rect overlap)
        function checkCollisions() {
            for (let obs of obstacles) {
                if (obs.x < player.x + player.width &&
                    obs.x + obs.width > player.x &&
                    obs.y < player.y + player.height &&
                    obs.y + obs.height > player.y) {
                    gameActive = false;
                    break;
                }
            }
        }

        // update game state
        function update() {
            if (!gameActive) return;

            // move obstacles down
            for (let i = obstacles.length-1; i >= 0; i--) {
                obstacles[i].y += OBSTACLE_SPEED;
                if (obstacles[i].y > canvas.height) {
                    obstacles.splice(i, 1);
                    score += 10;        // +10 for each passed car
                    scoreSpan.innerText = score;
                }
            }

            // spawn new obstacles
            frameCounter++;
            if (frameCounter % SPAWN_RATE === 0) {
                spawnObstacle();
            }

            // move player (lane change)
            movePlayer();

            // collision detection
            checkCollisions();
        }

        // DRAW everything with modern neon style
        function draw() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            // dark road with lane markers
            ctx.fillStyle = '#1a2a33';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            // lane dividers (dashed)
            ctx.strokeStyle = '#0e75b6';
            ctx.lineWidth = 4;
            ctx.setLineDash([20, 25]);
            for (let i = 1; i < LANES; i++) {
                ctx.beginPath();
                ctx.moveTo(i * LANE_WIDTH, 0);
                ctx.lineTo(i * LANE_WIDTH, canvas.height);
                ctx.strokeStyle = '#58a6ff';
                ctx.stroke();
            }
            ctx.setLineDash([]);

            // draw player (blue modern car)
            ctx.shadowColor = '#0e75b6';
            ctx.shadowBlur = 20;
            ctx.fillStyle = '#3b82f6';
            ctx.beginPath();
            ctx.roundRect(player.x, player.y, player.width, player.height, 12);
            ctx.fill();
            // windscreen
            ctx.fillStyle = '#a5d8ff';
            ctx.beginPath();
            ctx.roundRect(player.x+8, player.y+10, player.width-16, 18, 6);
            ctx.fill();
            // neon headlights
            ctx.fillStyle = '#fcd34d';
            ctx.beginPath();
            ctx.arc(player.x+8, player.y+player.height-12, 8, 0, 2*Math.PI);
            ctx.fill();
            ctx.beginPath();
            ctx.arc(player.x+player.width-8, player.y+player.height-12, 8, 0, 2*Math.PI);
            ctx.fill();

            // draw obstacles (aggressive red)
            ctx.shadowColor = '#ef4444';
            ctx.shadowBlur = 20;
            for (let obs of obstacles) {
                ctx.fillStyle = '#b91c1c';
                ctx.beginPath();
                ctx.roundRect(obs.x, obs.y, obs.width, obs.height, 10);
                ctx.fill();
                // dark windows
                ctx.fillStyle = '#2d1a1a';
                ctx.beginPath();
                ctx.roundRect(obs.x+10, obs.y+12, obs.width-20, 15, 5);
                ctx.fill();
            }

            // game over overlay
            if (!gameActive) {
                ctx.shadowBlur = 0;
                ctx.font = 'bold 40px "Fira Code", monospace';
                ctx.fillStyle = '#ffffffcc';
                ctx.shadowColor = '#0e75b6';
                ctx.shadowBlur = 20;
                ctx.fillText('GAME OVER', 180, 200);
                ctx.font = '20px monospace';
                ctx.fillText('press RESTART', 280, 280);
            }

            // reset shadow
            ctx.shadowBlur = 0;
            ctx.shadowColor = 'transparent';
        }

        // helper canvas roundRect
        CanvasRenderingContext2D.prototype.roundRect = function (x, y, w, h, r) {
            if (w < 2 * r) r = w / 2;
            if (h < 2 * r) r = h / 2;
            this.moveTo(x + r, y);
            this.lineTo(x + w - r, y);
            this.quadraticCurveTo(x + w, y, x + w, y + r);
            this.lineTo(x + w, y + h - r);
            this.quadraticCurveTo(x + w, y + h, x + w - r, y + h);
            this.lineTo(x + r, y + h);
            this.quadraticCurveTo(x, y + h, x, y + h - r);
            this.lineTo(x, y + r);
            this.quadraticCurveTo(x, y, x + r, y);
            this.closePath();
            return this;
        };

        // game loop
        function gameLoop() {
            update();
            draw();
            animationFrame = requestAnimationFrame(gameLoop);
        }

        // keyboard listeners
        window.addEventListener('keydown', (e) => {
            if (e.key === 'ArrowLeft') {
                leftPressed = true;
                e.preventDefault();
            } else if (e.key === 'ArrowRight') {
                rightPressed = true;
                e.preventDefault();
            }
        });
        window.addEventListener('keyup', (e) => {
            if (e.key === 'ArrowLeft') {
                leftPressed = false;
                e.preventDefault();
            } else if (e.key === 'ArrowRight') {
                rightPressed = false;
                e.preventDefault();
            }
        });

        // restart button
        document.getElementById('restartGame').addEventListener('click', () => {
            resetGame();
        });

        // start the loop
        resetGame();
        gameLoop();

        // prevent page scrolling with arrows when canvas focused (or anywhere)
        window.addEventListener('keydown', (e) => {
            if (e.key === 'ArrowLeft' || e.key === 'ArrowRight') {
                e.preventDefault();
            }
        }, {passive: false});
    })();
</script>
</body>
</html>

