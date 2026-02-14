<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ishu/Mummy ❤️ Valentine's Day Special</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400;600;700&display=swap');
        
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            height: 100vh;
            background: linear-gradient(-45deg, #ff9a9e, #fecfef, #fad0c4, #ffd1ff, #ff9a9e);
            background-size: 400% 400%;
            animation: gradientShift 12s ease infinite;
            font-family: 'Poppins', sans-serif;
            overflow: hidden;
            position: relative;
            cursor: none;
        }
        
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            25% { background-position: 100% 50%; }
            50% { background-position: 100% 100%; }
            75% { background-position: 0% 100%; }
            100% { background-position: 0% 50%; }
        }
        
        .container {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            text-align: center;
            z-index: 10;
            position: relative;
        }
        
        .name-title {
            font-family: 'Dancing Script', cursive;
            font-size: clamp(3.5em, 8vw, 7em);
            background: linear-gradient(45deg, #ff1493, #ff69b4, #ff1493);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 0 40px rgba(255, 20, 147, 0.6);
            animation: glowPulse 2.5s ease-in-out infinite alternate;
            cursor: pointer;
            transition: all 0.4s ease;
            user-select: none;
            margin-bottom: 1rem;
        }
        
        .name-title:hover {
            transform: scale(1.15) rotate(3deg);
            filter: drop-shadow(0 0 60px #ff1493);
        }
        
        .messages {
            max-width: 600px;
            margin: 2rem 0;
        }
        
        .message-1, .message-2 {
            font-size: clamp(1.4em, 4vw, 2.4em);
            color: white;
            margin: 1rem 0;
            text-shadow: 0 0 20px rgba(255,255,255,0.8);
            animation: fadeInUp 2s ease-out forwards;
            opacity: 0;
            font-weight: 300;
        }
        
        .message-1 { animation-delay: 0.8s; }
        .message-2 { animation-delay: 1.4s; font-family: 'Dancing Script', cursive; font-size: clamp(1.6em, 4.5vw, 2.8em); }
        
        .music-controls {
            background: rgba(255, 105, 180, 0.2);
            backdrop-filter: blur(15px);
            border: 2px solid rgba(255, 20, 147, 0.4);
            border-radius: 50px;
            padding: 1rem 2.5rem;
            margin-top: 2rem;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
            color: white;
            font-size: 1.3em;
            box-shadow: 0 10px 40px rgba(255, 20, 147, 0.3);
        }
        
        .music-controls:hover {
            background: rgba(255, 105, 180, 0.4);
            transform: translateY(-5px);
            box-shadow: 0 15px 50px rgba(255, 20, 147, 0.5);
        }
        
        .music-status {
            font-size: 1.2em;
            color: #ff69b4;
            margin-top: 1rem;
            font-weight: 600;
            display: none;
            text-shadow: 0 0 15px #ff69b4;
        }
        
        /* Animations */
        @keyframes glowPulse {
            from { filter: drop-shadow(0 0 30px rgba(255,105,180,0.8)); }
            to { filter: drop-shadow(0 0 60px rgba(255,20,147,1)); }
        }
        
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(40px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Stars falling */
        .star {
            position: absolute;
            font-size: 1.6em;
            color: #ffd700;
            animation: fallStars linear infinite;
            text-shadow: 0 0 20px #ffd700;
            pointer-events: none;
            z-index: 1;
        }
        
        @keyframes fallStars {
            0% { transform: translateY(-100vh) rotate(0deg) scale(0); opacity: 1; }
            50% { opacity: 1; }
            100% { transform: translateY(100vh) rotate(720deg) scale(1); opacity: 0; }
        }
        
        /* Floating hearts */
        .heart {
            position: absolute;
            font-size: 2.2em;
            animation: floatHearts 8s infinite ease-in-out;
            pointer-events: none;
            z-index: 2;
        }
        
        @keyframes floatHearts {
            0% { 
                transform: translateY(100vh) translateX(0) rotate(0deg) scale(0);
                opacity: 0;
            }
            10% { opacity: 1; transform: scale(1); }
            90% { opacity: 1; }
            100% { 
                transform: translateY(-100vh) translateX(50px) rotate(360deg) scale(1.2);
                opacity: 0;
            }
        }
        
        /* Custom cursor */
        .cursor-heart {
            position: fixed;
            pointer-events: none;
            z-index: 1000;
            font-size: 24px;
            transition: transform 0.1s ease;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .name-title { font-size: 4em; }
            .message-1, .message-2 { font-size: 1.6em; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="name-title" onclick="toggleRaabta()" title="Click me for Raabta 🎵">
            Ishu / Mummy 💖✨
        </h1>
        
        <div class="messages">
            <div class="message-1">Tu meri duniya, mera jahaan hai! 🌟</div>
            <div class="message-2">Happy Valentine's Day meri jaan! 😍💕</div>
        </div>
        
        <div class="music-controls" onclick="toggleRaabta()" id="musicBtn">
            🎵 Raabta Play (41s से) 🎵
        </div>
        
        <div class="music-status" id="musicStatus">
            ✨ Raabta (41s) बज रहा है... 💖
        </div>
    </div>

    <!-- Raabta Audio - Tera uploaded MP3 file -->
    <audio id="raabtaAudio" loop preload="metadata">
        <!-- MP3 file Tiiny.host/GitHub pe upload karne ke baad yahan link daal dena -->
        <!-- For now placeholder - real file ka URL replace karna -->
        <!-- src="Raabta-Agent-Vinod-320-Kbps.mp3" -->
    </audio>

    <script>
        const audio = document.getElementById('raabtaAudio');
        const musicBtn = document.getElementById('musicBtn');
        const musicStatus = document.getElementById('musicStatus');
        let isPlaying = false;
        
        // Continuous stars falling (25 stars)
        function createStar() {
            const star = document.createElement('div');
            star.className = 'star';
            const stars = ['⭐', '✨', '🌟', '💫', '⭐'];
            star.textContent = stars[Math.floor(Math.random() * stars.length)];
            star.style.left = Math.random() * 100 + 'vw';
            star.style.animationDuration = (Math.random() * 6 + 5) + 's';
            document.body.appendChild(star);
            setTimeout(() => star.remove(), 11000);
        }
        setInterval(createStar, 120);
        
        // Floating hearts + emojis
        function createHeart() {
            const heart = document.createElement('div');
            heart.className = 'heart';
            const emojis = ['💖', '💕', '💗', '💝', '🌹', '😍', '🥰', '💖', '✨'];
            heart.textContent = emojis[Math.floor(Math.random() * emojis.length)];
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = (Math.random() * 4 + 6) + 's';
            heart.style.animationDelay = Math.random() * 2 + 's';
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 10000);
        }
        setInterval(createHeart, 400);
        
        // 🔥 RAABTA SONG EXACTLY 41 SECONDS से START 🔥
        function toggleRaabta() {
            if (isPlaying) {
                audio.pause();
                audio.currentTime = 0;
                musicBtn.textContent = '🎵 Raabta Play (41s से) 🎵';
                musicStatus.style.display = 'none';
                isPlaying = false;
            } else {
                // EXACTLY 41 SECONDS से start!
                audio.currentTime = 41;
                audio.volume = 0.65;
                audio.loop = true;
                audio.play().then(() => {
                    musicBtn.textContent = '⏸️ Raabta Pause';
                    musicStatus.style.display = 'block';
                    musicStatus.textContent = '✨ Raabta (41s से) बज रहा है... 💖';
                    isPlaying = true;
                }).catch(e => {
                    musicStatus.textContent = '📱 Tap allow audio pehle';
                    musicStatus.style.display = 'block';
                });
            }
        }
        
        // Mouse heart trail effect
        document.addEventListener('mousemove', (e) => {
            const trail = document.createElement('div');
            trail.className = 'cursor-heart';
            trail.textContent = '💕';
            trail.style.left = e.clientX + 'px';
            trail.style.top = e.clientY + 'px';
            document.body.appendChild(trail);
            setTimeout(() => trail.remove(), 800);
        });
        
        // Touch effect for mobile
        document.addEventListener('touchmove', (e) => {
            e.preventDefault();
        });
        
        // Auto glow animation start
        setTimeout(() => {
            document.querySelector('.name-title').style.animation = 'glowPulse 2.5s ease-in-out infinite alternate';
        }, 500);
    </script>
</body>
</html>
