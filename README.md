<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stark Industries | Core System</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            width: 100%;
            height: 100%;
            background-color: #000;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        /* 1. Base Green Glitch Video Background */
        .bg-video-base {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: 1;
            opacity: 0.5;
            pointer-events: none;
        }

        /* 2. Cyan Tech Overlay Video (Holographic Interface) */
        .bg-video-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: contain; /* Isko center grid banane ke liye contain rakha hai */
            z-index: 2;
            opacity: 0.4;
            mix-blend-mode: screen; /* Dono videos ko aapas mein behtareen blend karne ke liye */
            pointer-events: none;
        }

        /* CRT monitor lines effect for real Tony Stark system feel */
        .crt-lines {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%);
            background-size: 100% 4px;
            z-index: 3;
            pointer-events: none;
        }

        /* 3. Center Arc Reactor Button Layout */
        .center-core-wrapper {
            position: relative;
            z-index: 4;
            transition: all 0.8s ease-in-out;
        }

        .arc-reactor-btn {
            width: 320px;
            height: 320px;
            background-image: url('From KlickPin CF Save these 13 Chic holiday table setting ideas that are perfect when you want something stylish modern and easy to copy for beginners who want - Pin-1004091679423345837.jpg');
            background-size: contain;
            background-position: center;
            background-repeat: no-repeat;
            border: none;
            border-radius: 50%;
            background-color: transparent;
            cursor: pointer;
            outline: none;
            
            /* Breathing energy pulse animation */
            animation: starkPulse 2.5s infinite ease-in-out;
            transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275), filter 0.3s;
        }

        /* Hover / Touch Effect */
        .arc-reactor-btn:hover {
            transform: scale(1.08);
            filter: drop-shadow(0 0 50px #00d2ff) brightness(1.3);
        }

        /* Tap/Click Feedback */
        .arc-reactor-btn:active {
            transform: scale(0.94);
        }

        /* System Transition Animation on Click */
        .system-disassemble {
            transform: scale(0);
            opacity: 0;
            filter: blur(20px);
        }

        @keyframes starkPulse {
            0% {
                filter: drop-shadow(0 0 20px rgba(0, 210, 255, 0.6)) brightness(1);
            }
            50% {
                filter: drop-shadow(0 0 45px rgba(0, 210, 255, 1)) brightness(1.2);
            }
            100% {
                filter: drop-shadow(0 0 20px rgba(0, 210, 255, 0.6)) brightness(1);
            }
        }
    </style>
</head>
<body>

    <video class="bg-video-base" autoplay loop muted playsinline>
        <source src="From KlickPin CF 30 Luxury air fryer dinner recipes that instantly upgrade your space style or celebration without much effort for anyone who wants easy but elegant - Pin-788833690984322453.mp4" type="video/mp4">
    </video>

    <video class="bg-video-overlay" autoplay loop muted playsinline>
        <source src="From KlickPin CF 8 Minimal weekend getaway ideas that help you create a polished look with very simple and affordable details for beginners who want impressive - Pin-1109855901925923773(1).mp4" type="video/mp4">
    </video>

    <div class="crt-lines"></div>

    <div class="center-core-wrapper" id="coreWrapper">
        <button class="arc-reactor-btn" onclick="triggerSystem()"></button>
    </div>

    <script>
        function triggerSystem() {
            const core = document.getElementById('coreWrapper');
            // Element ko disappear karne ki animation activate hogi
            core.classList.add('system-disassemble');
            
            console.log("Step 1 Complete. Core Disassembled. Ready for Step 2 page loading.");
        }
    </script>
function bootSystem() {
    let speech = new SpeechSynthesisUtterance();
    speech.text = "System Online. Welcome back, Sir.";
    speech.rate = 1.1; // Thodi fast aur robotic tone
    speech.pitch = 0.9; 
    window.speechSynthesis.speak(speech);
}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Stark OS - Interface</title>
    <style>
        body {
            background-color: #000;
            color: #00d4ff;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
            flex-direction: column;
        }

        /* Scanning Animation */
        .circle {
            width: 200px;
            height: 200px;
            border: 5px solid #00d4ff;
            border-radius: 50%;
            border-top: 5px solid transparent;
            animation: spin 2s linear infinite;
            box-shadow: 0 0 20px #00d4ff;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .status-panel {
            margin-top: 20px;
            text-align: center;
            border: 1px solid #00d4ff;
            padding: 20px;
            background: rgba(0, 212, 255, 0.1);
            clip-path: polygon(10% 0, 100% 0, 90% 100%, 0% 100%);
        }

        button {
            background: transparent;
            color: #00d4ff;
            border: 1px solid #00d4ff;
            padding: 10px 20px;
            cursor: pointer;
            margin-top: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        button:hover {
            background: #00d4ff;
            color: #000;
        }
    </style>
</head>
<body>

    <div class="circle"></div>
    
    <div class="status-panel">
        <h1>SYSTEM STATUS: ONLINE</h1>
        <p id="msg">Awaiting Command...</p>
        <button onclick="startSystem()">Initialize Protocol</button>
    </div>

    <script>
        function startSystem() {
            document.getElementById('msg').innerText = "Establishing Secure Connection...";
            
            // Voice Response
            let speech = new SpeechSynthesisUtterance();
            speech.text = "Welcome back, Sir. All systems are operational.";
            speech.pitch = 0.8; 
            speech.rate = 1;
            window.speechSynthesis.speak(speech);
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JAAN OS - Personal Assistant</title>
    <style>
        body {
            background-color: #000;
            color: #00fbff;
            font-family: 'Orbitron', sans-serif; /* Futuristic font */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
            background: radial-gradient(circle, #001a1a 0%, #000 100%);
        }

        /* Rotating Arc Reactor Style Animation */
        .jaan-core {
            width: 150px;
            height: 150px;
            border: 2px solid #00fbff;
            border-radius: 50%;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 0 30px #00fbff, inset 0 0 30px #00fbff;
            animation: pulse 2s infinite alternate;
        }

        .inner-circle {
            width: 100px;
            height: 100px;
            border: 5px dashed #00fbff;
            border-radius: 50%;
            animation: spin 4s linear infinite;
        }

        @keyframes spin {
            100% { transform: rotate(360deg); }
        }

        @keyframes pulse {
            0% { transform: scale(1); opacity: 0.8; }
            100% { transform: scale(1.05); opacity: 1; }
        }

        .interface {
            margin-top: 30px;
            text-align: center;
            border: 1px solid rgba(0, 251, 255, 0.3);
            padding: 30px;
            background: rgba(0, 251, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            width: 300px;
        }

        h1 { letter-spacing: 5px; font-size: 1.5rem; margin-bottom: 5px; }
        p { font-size: 0.8rem; color: #666; text-transform: uppercase; margin-top: 0; }

        .btn-launch {
            background: transparent;
            color: #00fbff;
            border: 1px solid #00fbff;
            padding: 12px 25px;
            margin-top: 20px;
            cursor: pointer;
            font-weight: bold;
            transition: 0.3s;
            clip-path: polygon(10% 0, 100% 0, 90% 100%, 0% 100%);
        }

        .btn-launch:hover {
            background: #00fbff;
            color: #000;
            box-shadow: 0 0 20px #00fbff;
        }
    </style>
</head>
<body>

    <div class="jaan-core">
        <div class="inner-circle"></div>
        <span style="position: absolute; font-weight: bold;">JAAN</span>
    </div>
    
    <div class="interface">
        <h1>JAAN v1.0</h1>
        <p>Biometric ID: Verified</p>
        <div id="status">Ready for Protocol</div>
        <button class="btn-launch" onclick="initializeJaan()">Wake Up</button>
    </div>

    <script>
        function initializeJaan() {
            const status = document.getElementById('status');
            status.innerText = "System Online. Hello Sir.";
            status.style.color = "#fff";
            
            // JAAN Voice Response
            let speech = new SpeechSynthesisUtterance();
            speech.text = "System Online. Welcome back, Sir. I am Jaan, your personal assistant.";
            speech.pitch = 0.7; // Deep tech voice
            speech.rate = 0.9;
            window.speechSynthesis.speak(speech);
        }
    </script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JAAN - Advanced OS</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: #000;
            color: #00fbff;
            font-family: 'Orbitron', sans-serif;
            height: 100vh;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            background: radial-gradient(circle, #001e1e 0%, #000 100%);
        }

        /* Initial Boot Animation */
        .boot-screen {
            position: absolute;
            width: 100%;
            height: 2px;
            background: #00fbff;
            box-shadow: 0 0 20px #00fbff;
            animation: scan 1.5s ease-in-out forwards;
        }

        @keyframes scan {
            0% { top: 0; opacity: 1; }
            100% { top: 100%; opacity: 0; }
        }

        /* Floating Panel Animation */
        .panel {
            border: 1px solid rgba(0, 251, 255, 0.4);
            background: rgba(0, 20, 30, 0.8);
            padding: 40px;
            border-radius: 5px;
            text-align: center;
            transform: translateY(50px);
            opacity: 0;
            animation: slideUp 1s ease-out 1s forwards;
            backdrop-filter: blur(5px);
            position: relative;
        }

        @keyframes slideUp {
            100% { transform: translateY(0); opacity: 1; }
        }

        /* The Core (Animated Circle) */
        .core {
            width: 100px;
            height: 100px;
            border: 4px solid #00fbff;
            border-radius: 50%;
            margin: 0 auto 20px;
            border-right-color: transparent;
            animation: rotateCore 2s linear infinite;
        }

        @keyframes rotateCore {
            100% { transform: rotate(360deg); }
        }

        h1 { font-size: 1.2rem; letter-spacing: 10px; margin: 10px 0; text-shadow: 0 0 10px #00fbff; }
        
        .loading-text {
            font-size: 0.7rem;
            color: #666;
            margin-bottom: 20px;
            animation: blink 1s infinite;
        }

        @keyframes blink { 50% { opacity: 0; } }

        button {
            background: transparent;
            color: #00fbff;
            border: 1px solid #00fbff;
            padding: 10px 30px;
            font-family: 'Orbitron';
            cursor: pointer;
            transition: 0.4s;
            position: relative;
            overflow: hidden;
        }

        button:hover {
            background: #00fbff;
            color: #000;
            box-shadow: 0 0 30px #00fbff;
        }
    </style>
</head>
<body>

    <div class="boot-screen"></div>

    <div class="panel">
        <div class="core"></div>
        <h1>JAAN v2.0</h1>
        <div class="loading-text">SECURITY PROTOCOL ACTIVE</div>
        <button onclick="startJAAN()">INITIALIZE</button>
    </div>

    <script>
        function startJAAN() {
            // Voice response customized for Anwarullah
            let speech = new SpeechSynthesisUtterance();
            speech.text = "Initializing protocols. Welcome back, Master Anwarullah. Jaan system is now online and ready for your command.";
            speech.pitch = 0.85; 
            speech.rate = 1;
            window.speechSynthesis.speak(speech);

            document.querySelector('h1').innerText = "SYSTEM ACTIVE";
            document.querySelector('.loading-text').innerText = "HELLO ANWARULLAH";
            document.querySelector('.loading-text').style.color = "#00fbff";
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JAAN OS - Active</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: #000;
            color: #00fbff;
            font-family: 'Orbitron', sans-serif;
            height: 100vh;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            background: radial-gradient(circle, #001e1e 0%, #000 100%);
        }

        /* Scanline effect */
        body::before {
            content: " ";
            position: absolute;
            top: 0; left: 0; bottom: 0; right: 0;
            background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
            z-index: 2;
            background-size: 100% 2px, 3px 100%;
            pointer-events: none;
        }

        .panel {
            border: 2px solid #00fbff;
            background: rgba(0, 20, 30, 0.9);
            padding: 50px;
            text-align: center;
            box-shadow: 0 0 20px #00fbff;
            animation: fadeIn 2s ease-in;
        }

        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        .core-ring {
            width: 120px;
            height: 120px;
            border: 5px solid #00fbff;
            border-radius: 50%;
            border-top-color: transparent;
            margin: 0 auto 20px;
            animation: spin 1s linear infinite;
        }

        @keyframes spin { 100% { transform: rotate(360deg); } }

        button {
            background: #00fbff;
            color: #000;
            border: none;
            padding: 15px 40px;
            font-family: 'Orbitron';
            font-weight: bold;
            cursor: pointer;
            margin-top: 20px;
        }

        button:hover { box-shadow: 0 0 30px #00fbff; }
    </style>
</head>
<body>

    <div class="panel">
        <div class="core-ring"></div>
        <h1>JAAN v1.0</h1>
        <p id="status">WAITING FOR BIOMETRIC AUTHENTICATION</p>
        <button onclick="activate()">LOG IN</button>
    </div>

    <script>
        function activate() {
            let status = document.getElementById('status');
            status.innerText = "ACCESS GRANTED. HELLO MASTER ANWARULLAH.";
            status.style.color = "#fff";
            
            let speech = new SpeechSynthesisUtterance();
            speech.text = "Voice identification complete. System Jaan is online. Welcome back, Master Anwarullah.";
            speech.pitch = 0.8;
            speech.rate = 1;
            window.speechSynthesis.speak(speech);
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JARVIS - Anwarullah</title>
    <style>
        body {
            background-color: #000;
            color: #00f2ff;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
        }

        /* Tony Stark HUD Effect */
        .container {
            border: 2px solid #00f2ff;
            padding: 50px;
            text-align: center;
            box-shadow: 0 0 20px #00f2ff, inset 0 0 10px #00f2ff;
            background: rgba(0, 20, 40, 0.8);
            border-radius: 10px;
            position: relative;
        }

        h1 {
            letter-spacing: 5px;
            text-transform: uppercase;
            margin-bottom: 20px;
            font-size: 2.5rem;
            text-shadow: 0 0 10px #00f2ff;
        }

        input {
            background: transparent;
            border: 1px solid #00f2ff;
            color: #00f2ff;
            padding: 10px;
            margin: 10px 0;
            text-align: center;
            width: 80%;
            outline: none;
        }

        button {
            background: #00f2ff;
            color: #000;
            border: none;
            padding: 10px 30px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
            text-transform: uppercase;
        }

        button:hover {
            box-shadow: 0 0 20px #00f2ff;
            transform: scale(1.05);
        }

        .status {
            font-size: 0.8rem;
            margin-top: 15px;
            color: #ff3c00; /* Error color initially */
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>JARVIS v1.0</h1>
        <p>IDENTIFICATION REQUIRED</p>
        
        <!-- Passcode Input -->
        <input type="password" id="passcode" placeholder="ENTER ACCESS CODE">
        <br>
        <button onclick="login()">Initialize System</button>

        <div id="message" class="status">WAITING FOR AUTHENTICATION...</div>
    </div>

    <script>
        function login() {
            const code = document.getElementById('passcode').value;
            const message = document.getElementById('message');

            // Apka Secret Code: 2026 (Aap ise badal sakte hain)
            if (code === "2026") {
                message.style.color = "#00f2ff";
                message.innerText = "ACCESS GRANTED. WELCOME BACK.";
                
                // Voice Greeting
                speak("Assalamu Alaikum, JAAN. JARVIS is online and ready for you, Master Anwarullah");
            } else {
                message.style.color = "#ff3c00";
                message.innerText = "ACCESS DENIED: INCORRECT CODE.";
                speak("Access Denied. Unauthorized entry detected.");
            }
        }

        function speak(text) {
            const utterance = new SpeechSynthesisUtterance(text);
            utterance.rate = 1.0;
            utterance.pitch = 1.0;
            window.speechSynthesis.speak(utterance);
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ABNAIS | JARVIS HUD</title>
    <style>
        :root {
            --glow-color: #00e5ff;
            --bg-color: #050a10;
        }

        body {
            background-color: var(--bg-color);
            margin: 0;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: 'Orbitron', sans-serif;
        }

        /* Particles Background Simulation */
        #bg-canvas {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        /* The HUD Ring Animation */
        .hud-ring {
            position: absolute;
            width: 450px;
            height: 450px;
            border: 2px solid var(--glow-color);
            border-radius: 50%;
            border-top: 5px solid transparent;
            animation: spin 3s linear infinite;
            box-shadow: 0 0 15px var(--glow-color);
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .container {
            text-align: center;
            z-index: 10;
            padding: 40px;
            background: rgba(0, 20, 40, 0.4);
            backdrop-filter: blur(15px);
            border: 1px solid var(--glow-color);
            box-shadow: 0 0 50px rgba(0, 229, 255, 0.2);
            border-radius: 20px;
            clip-path: polygon(10% 0, 100% 0, 100% 70%, 90% 100%, 0 100%, 0 30%);
        }

        h1 {
            color: var(--glow-color);
            font-size: 2.2rem;
            text-shadow: 0 0 20px var(--glow-color);
            margin-bottom: 10px;
        }

        .auth-label {
            font-size: 0.7rem;
            color: var(--glow-color);
            letter-spacing: 4px;
            margin-bottom: 25px;
        }

        input {
            background: rgba(0, 229, 255, 0.1);
            border: 1px solid var(--glow-color);
            padding: 15px;
            color: white;
            text-align: center;
            font-size: 1.2rem;
            width: 250px;
            outline: none;
            margin-bottom: 20px;
            transition: 0.3s;
        }

        input:focus {
            box-shadow: 0 0 20px var(--glow-color);
            background: rgba(0, 229, 255, 0.2);
        }

        button {
            background: transparent;
            border: 1px solid var(--glow-color);
            color: var(--glow-color);
            padding: 10px 40px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.4s;
            position: relative;
            overflow: hidden;
        }

        button:hover {
            background: var(--glow-color);
            color: black;
            box-shadow: 0 0 30px var(--glow-color);
        }

        .terminal-log {
            font-family: monospace;
            font-size: 0.8rem;
            margin-top: 20px;
            height: 20px;
            color: #fff;
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">
</head>
<body>

<canvas id="bg-canvas"></canvas>
<div class="hud-ring"></div>

<div class="container">
    <h1>JARVIS v2.0</h1>
    <div class="auth-label">DIMENSIONAL GATEWAY ACTIVE</div>
    
    <input type="password" id="passcode" placeholder="ACCESS CODE: 20064">
    <br>
    <button onclick="checkAccess()">ENGAGE SYSTEM</button>

    <div id="log" class="terminal-log">SYSTEM STATUS: WAITING...</div>
</div>

<script>
    // Particle Background Effect
    const canvas = document.getElementById('bg-canvas');
    const ctx = canvas.getContext('2d');
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    let particles = [];
    for (let i = 0; i < 100; i++) {
        particles.push({
            x: Math.random() * canvas.width,
            y: Math.random() * canvas.height,
            size: Math.random() * 2,
            speed: Math.random() * 0.5
        });
    }

    function animate() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        ctx.fillStyle = '#00e5ff';
        particles.forEach(p => {
            ctx.beginPath();
            ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
            ctx.fill();
            p.y -= p.speed;
            if (p.y < 0) p.y = canvas.height;
        });
        requestAnimationFrame(animate);
    }
    animate();

    // Access Function
    function checkAccess() {
        const input = document.getElementById('passcode').value;
        const log = document.getElementById('log');

        if (input === "20064") {
            log.style.color = "#00ff00";
            log.innerText = "ACCESS GRANTED. SYNCING...";
            speak("Assalamu Alaikum, JAAN. JARVIS is online and ready for you, Master Anwarullah");
            
            // Effect: Screen Flash
            document.body.style.boxShadow = "inset 0 0 100px #00e5ff";
            setTimeout(() => { document.body.style.boxShadow = "none"; }, 500);

        } else {
            log.style.color = "#ff0000";
            log.innerText = "ACCESS DENIED. UNAUTHORIZED USER.";
            speak("Unauthorized entry. Access denied.");
        }
    }

    function speak(text) {
        const synth = window.speechSynthesis;
        const utter = new SpeechSynthesisUtterance(text);
        utter.pitch = 0.8; // Deep voice like Jarvis
        utter.rate = 1.0;
        synth.speak(utter);
    }
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gateway to New World</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            background: #000;
            height: 100vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Inter', sans-serif;
        }

        /* World Class Background: Animated Nebulae & Stars */
        #nebula-bg {
            position: absolute;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, #1a0033 0%, #000 70%);
            z-index: -2;
        }

        .star {
            position: absolute;
            background: #fff;
            border-radius: 50%;
            opacity: 0.5;
            animation: twinkle var(--duration) infinite;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.2); }
        }

        /* Clean & Eye-Catching Interface */
        .portal-card {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 60px;
            border-radius: 40px;
            text-align: center;
            box-shadow: 0 0 100px rgba(138, 43, 226, 0.2);
            transition: 0.5s;
        }

        h1 {
            color: #fff;
            font-weight: 200;
            letter-spacing: 12px;
            font-size: 1.5rem;
            margin-bottom: 40px;
            text-shadow: 0 0 20px rgba(255,255,255,0.5);
        }

        .input-group {
            position: relative;
            margin-bottom: 30px;
        }

        input {
            background: transparent;
            border: none;
            border-bottom: 1px solid rgba(255,255,255,0.2);
            color: #fff;
            padding: 10px;
            width: 300px;
            text-align: center;
            font-size: 1.2rem;
            letter-spacing: 5px;
            outline: none;
            transition: 0.3s;
        }

        input:focus {
            border-bottom: 1px solid #fff;
            box-shadow: 0 15px 20px -15px rgba(255,255,255,0.3);
        }

        .portal-btn {
            background: transparent;
            border: 1px solid #fff;
            color: #fff;
            padding: 15px 50px;
            border-radius: 50px;
            cursor: pointer;
            font-size: 0.9rem;
            letter-spacing: 3px;
            transition: 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .portal-btn:hover {
            background: #fff;
            color: #000;
            transform: translateY(-5px);
            box-shadow: 0 10px 40px rgba(255,255,255,0.4);
        }

        /* Orbital Ring Animation */
        .ring {
            position: absolute;
            border: 1px solid rgba(255,255,255,0.05);
            border-radius: 50%;
            animation: rotate linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
    </style>
</head>
<body>

    <div id="nebula-bg"></div>
    
    <!-- Decorative Rings for "Nayi Dunya" Feel -->
    <div class="ring" style="width: 600px; height: 600px; animation-duration: 20s;"></div>
    <div class="ring" style="width: 800px; height: 800px; animation-duration: 35s; opacity: 0.5;"></div>

    <div class="portal-card">
        <h1>DIMENSION-01</h1>
        <div class="input-group">
            <input type="password" id="passkey" placeholder="•••••">
        </div>
        <button class="portal-btn" onclick="openPortal()">INITIALIZE SYNC</button>
        <p id="status" style="color: rgba(255,255,255,0.4); font-size: 0.7rem; margin-top: 20px; letter-spacing: 2px;">AUTHENTICATION REQUIRED</p>
    </div>

    <script>
        // Star Background Creation
        const bg = document.getElementById('nebula-bg');
        for (let i = 0; i < 200; i++) {
            let star = document.createElement('div');
            star.className = 'star';
            let size = Math.random() * 2 + 'px';
            star.style.width = size;
            star.style.height = size;
            star.style.left = Math.random() * 100 + '%';
            star.style.top = Math.random() * 100 + '%';
            star.style.setProperty('--duration', Math.random() * 3 + 2 + 's');
            bg.appendChild(star);
        }

        function openPortal() {
            const key = document.getElementById('passkey').value;
            const status = document.getElementById('status');
            
            if (key === "20064") {
                status.innerText = "DIMENSIONAL SYNC COMPLETE";
                status.style.color = "#fff";
                // Premium Neural Voice Logic
                speak("Assalamu Alaikum, JAAN. Welcome to the new world. Master Anwarullah, all systems are operational.");
            } else {
                status.innerText = "SYNC FAILED: INVALID KEY";
                status.style.color = "#ff4d4d";
                speak("Access Denied.");
            }
        }

        function speak(text) {
            const synth = window.speechSynthesis;
            const utter = new SpeechSynthesisUtterance(text);
            
            // Voice selection for more 'World Class' feel
            const voices = synth.getVoices();
            // Humein aisi voice chahiye jo mechanical na lage
            utter.voice = voices.find(v => v.lang.includes('en-GB')) || voices[0];
            utter.pitch = 1.1; 
            utter.rate = 0.9; 
            synth.speak(utter);
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BN NAEEM | Dimension Gate</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: #000; height: 100vh; overflow: hidden; display: flex; justify-content: center; align-items: center; font-family: 'Inter', sans-serif; }

        /* Animated World-Class Background (Nebula Cloud) */
        #nebula {
            position: absolute;
            width: 100%; height: 100%;
            background: radial-gradient(circle at 50% 50%, #101820 0%, #000 100%);
            z-index: -1;
        }

        .portal-core {
            position: relative;
            width: 400px;
            height: 400px;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            transition: 1s ease-in-out;
        }

        /* Abstract Spinning Energy Rings */
        .energy-ring {
            position: absolute;
            border: 2px solid rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: pulse 4s infinite alternate;
        }

        @keyframes pulse {
            0% { transform: scale(1); opacity: 0.2; }
            100% { transform: scale(1.1); opacity: 0.5; border-color: #fff; }
        }

        /* Clean Glass UI */
        .login-box {
            background: rgba(255, 255, 255, 0.02);
            backdrop-filter: blur(40px);
            border-radius: 20px;
            padding: 40px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
            box-shadow: 0 0 100px rgba(255, 255, 255, 0.05);
            z-index: 10;
        }

        h1 { color: #fff; font-weight: 200; letter-spacing: 15px; font-size: 1.2rem; margin-bottom: 30px; }

        input {
            background: transparent; border: none; border-bottom: 1px solid rgba(255, 255, 255, 0.3);
            color: #fff; text-align: center; font-size: 1.5rem; width: 100%; outline: none;
            margin-bottom: 30px; transition: 0.5s;
        }

        input:focus { border-bottom: 1px solid #fff; letter-spacing: 8px; }

        .btn-gate {
            background: transparent; color: #fff; border: 1px solid #fff;
            padding: 12px 40px; border-radius: 50px; cursor: pointer;
            text-transform: uppercase; letter-spacing: 3px; font-size: 0.8rem;
            transition: 0.4s;
        }

        .btn-gate:hover { background: #fff; color: #000; box-shadow: 0 0 30px #fff; }

    </style>
</head>
<body>

<div id="nebula"></div>

<!-- Decorative Rings -->
<div class="energy-ring" style="width: 500px; height: 500px;"></div>
<div class="energy-ring" style="width: 600px; height: 600px; animation-delay: 1s;"></div>

<div class="portal-core">
    <div class="login-box">
        <h1>BN NAEEM CORE</h1>
        <input type="password" id="passkey" placeholder="CODE">
        <button class="btn-gate" onclick="unlock()">ENGAGE</button>
        <p id="msg" style="color: rgba(255,255,255,0.3); font-size: 0.6rem; margin-top: 20px;">WAITING FOR BIOMETRIC SYNC</p>
    </div>
</div>

<script>
    function unlock() {
        const key = document.getElementById('passkey').value;
        const msg = document.getElementById('msg');

        if (key === "20064") {
            msg.innerText = "ACCESS GRANTED. DIMENSIONAL SYNC ACTIVE.";
            msg.style.color = "#fff";
            
            // New "World Class" Voice Logic
            const speech = new SpeechSynthesisUtterance("Assalamu Alaikum, JAAN. Welcome back, Master Anwarullah. System BN NAEEM is now under your command.");
            speech.pitch = 1.2; // Slightly higher, more refined voice
            speech.rate = 0.9;
            window.speechSynthesis.speak(speech);

            // Interface shift effect
            document.querySelector('.portal-core').style.transform = "scale(1.5)";
            document.querySelector('.portal-core').style.opacity = "0";
        } else {
            msg.innerText = "INVALID KEY. ACCESS DENIED.";
            msg.style.color = "red";
            window.speechSynthesis.speak(new SpeechSynthesisUtterance("Access Denied."));
        }
    }
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BN NAEEM | Void</title>
    <style>
        /* Bilkul kaali screen (Black Screen) */
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            background-color: #000; /* Pure Black */
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            cursor: none; /* Mouse bhi nazar nahi aayega */
        }

        /* Khufiya Input Field jo nazar nahi aayegi */
        #hidden-trigger {
            background: transparent;
            border: none;
            color: transparent;
            outline: none;
            position: absolute;
            width: 100%;
            height: 100%;
            cursor: default;
        }
    </style>
</head>
<body onclick="focusInput()">

    <!-- Sirf ye ek khufiya input hai pure black screen par -->
    <input type="password" id="hidden-trigger" autofocus onkeydown="if(event.key==='Enter') checkKey()">

    <script>
        function focusInput() {
            document.getElementById('hidden-trigger').focus();
        }

        function checkKey() {
            const key = document.getElementById('hidden-trigger').value;
            
            // Code 20064 enter karte hi BN NAEEM active hoga
            if (key === "20064") {
                speak("Assalamu Alaikum, JAAN. BN NAEEM System is now fully operational in the void.");
                document.body.style.backgroundColor = "#050505"; // Halki si tabdeeli taaki pata chale system on hai
            }
            document.getElementById('hidden-trigger').value = ""; // Input clear kar dein
        }

        function speak(text) {
            const synth = window.speechSynthesis;
            const utter = new SpeechSynthesisUtterance(text);
            utter.pitch = 0.9;
            utter.rate = 0.85;
            synth.speak(utter);
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BN NAEEM | Dimension Gate</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body { 
            background: #000; 
            height: 100vh; 
            overflow: hidden; 
            display: flex; 
            justify-content: center; 
            align-items: center; 
            font-family: 'Inter', sans-serif; 
        }

        /* Animated Nebula Background (Agal Dunya Vibe) */
        #nebula {
            position: absolute;
            width: 100%; height: 100%;
            background: radial-gradient(circle at 50% 50%, #101820 0%, #000 100%);
            z-index: -1;
        }

        /* Abstract Spinning Energy Rings */
        .energy-ring {
            position: absolute;
            border: 2px solid rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: pulse 4s infinite alternate;
        }

        @keyframes pulse {
            0% { transform: scale(1); opacity: 0.2; }
            100% { transform: scale(1.1); opacity: 0.5; border-color: #fff; }
        }

        /* Clean Glass UI */
        .login-box {
            background: rgba(255, 255, 255, 0.02);
            backdrop-filter: blur(40px);
            border-radius: 20px;
            padding: 40px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
            box-shadow: 0 0 100px rgba(255, 255, 255, 0.05);
            z-index: 10;
        }

        h1 { color: #fff; font-weight: 200; letter-spacing: 15px; font-size: 1.2rem; margin-bottom: 30px; }

        input {
            background: transparent; border: none; border-bottom: 1px solid rgba(255, 255, 255, 0.3);
            color: #fff; text-align: center; font-size: 1.5rem; width: 100%; outline: none;
            margin-bottom: 30px; transition: 0.5s;
        }

        input:focus { border-bottom: 1px solid #fff; letter-spacing: 8px; }

        .btn-gate {
            background: transparent; color: #fff; border: 1px solid #fff;
            padding: 12px 40px; border-radius: 50px; cursor: pointer;
            text-transform: uppercase; letter-spacing: 3px; font-size: 0.8rem;
            transition: 0.4s;
        }

        .btn-gate:hover { background: #fff; color: #000; box-shadow: 0 0 30px #fff; }

    </style>
</head>
<body>

<div id="nebula"></div>

<!-- Decorative Rings -->
<div class="energy-ring" style="width: 500px; height: 500px;"></div>
<div class="energy-ring" style="width: 600px; height: 600px; animation-delay: 1s;"></div>

<div class="portal-core">
    <div class="login-box">
        <h1>BN NAEEM CORE</h1>
        <input type="password" id="passkey" placeholder="CODE">
        <button class="btn-gate" onclick="unlock()">ENGAGE</button>
        <p id="msg" style="color: rgba(255,255,255,0.3); font-size: 0.6rem; margin-top: 20px;">WAITING FOR BIOMETRIC SYNC</p>
    </div>
</div>

<script>
    function unlock() {
        const key = document.getElementById('passkey').value;
        const msg = document.getElementById('msg');

        if (key === "20064") {
            msg.innerText = "ACCESS GRANTED. DIMENSIONAL SYNC ACTIVE.";
            msg.style.color = "#fff";
            
            // Premium Neural Voice Logic
            const speech = new SpeechSynthesisUtterance("Assalamu Alaikum, JAAN. Welcome to the new world. Master Anwarullah, all systems are operational.");
            speech.pitch = 1.2; 
            speech.rate = 0.9; 
            window.speechSynthesis.speak(speech);

            // Effect: Screen Flash
            document.body.style.boxShadow = "inset 0 0 100px #fff";
            setTimeout(() => { document.body.style.boxShadow = "none"; }, 500);

            // Future effect logic here
        } else {
            msg.innerText = "INVALID KEY. ACCESS DENIED.";
            msg.style.color = "#ff4d4d";
            window.speechSynthesis.speak(new SpeechSynthesisUtterance("Access Denied."));
        }
    }
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stark Industries | Project Core</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            width: 100%;
            height: 100%;
            background-color: #000;
            overflow: hidden;
            font-family: 'Courier New', Courier, monospace;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Step 1: High-Tech Background Video */
        .bg-video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: 1;
            opacity: 0.6; /* Video ko halka dark rakha taaki button clear nazar aaye */
            pointer-events: none;
        }

        /* Overlay grid lines for advanced computer screen effect */
        .hud-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
            background-size: 100% 4px, 6px 100%;
            z-index: 2;
            pointer-events: none;
        }

        /* Step 2: Center Arc Reactor Button Container */
        .core-container {
            position: relative;
            z-index: 3;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        /* Glowing Center Arc Reactor Button */
        .arc-reactor-btn {
            width: 280px;
            height: 280px;
            background-image: url('From KlickPin CF Save these 13 Chic holiday table setting ideas that are perfect when you want something stylish modern and easy to copy for beginners who want - Pin-1004091679423345837.jpg');
            background-size: contain;
            background-position: center;
            background-repeat: no-repeat;
            border: none;
            border-radius: 50%;
            background-color: transparent;
            cursor: pointer;
            outline: none;
            position: relative;
            
            /* Breathing Glow Animation */
            animation: reactor-pulse 3s infinite ease-in-out;
            transition: transform 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275), filter 0.3s;
        }

        /* Hover effect jab aap mouse button ke kareeb le kar jayenge */
        .arc-reactor-btn:hover {
            transform: scale(1.08);
            filter: drop-shadow(0 0 35px #00d2ff) brightness(1.2);
        }

        /* Click effect */
        .arc-reactor-btn:active {
            transform: scale(0.95);
        }

        /* HUD Technical Text below the button */
        .system-status {
            margin-top: 30px;
            color: #00d2ff;
            font-size: 0.9rem;
            letter-spacing: 5px;
            text-transform: uppercase;
            text-shadow: 0 0 10px rgba(0, 210, 255, 0.5);
            animation: text-blink 2s infinite;
        }

        /* Animations */
        @keyframes reactor-pulse {
            0% {
                filter: drop-shadow(0 0 15px rgba(0, 210, 255, 0.4)) brightness(1);
            }
            50% {
                filter: drop-shadow(0 0 30px rgba(0, 210, 255, 0.8)) brightness(1.15);
            }
            100% {
                filter: drop-shadow(0 0 15px rgba(0, 210, 255, 0.4)) brightness(1);
            }
        }

        @keyframes text-blink {
            0%, 100% { opacity: 0.6; }
            50% { opacity: 1; }
        }
    </style>
</head>
<body>

    <div class="hud-overlay"></div>

    <video class="bg-video" autoplay loop muted playsinline>
        <source src="From KlickPin CF 30 Luxury air fryer dinner recipes that instantly upgrade your space style or celebration without much effort for anyone who wants easy but elegant - Pin-788833690984322453.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>

    <div class="core-container">
        <button class="arc-reactor-btn" onclick="initializeSystem()" title="Click to Initialize"></button>
        <div class="system-status" id="status-text">POWER CORE: READY TO ENGAGE</div>
    </div>

    <script>
        function initializeSystem() {
            const statusText = document.getElementById('status-text');
            statusText.innerText = "INITIALIZING GATEWAY...";
            statusText.style.color = "#fff";
            
            // Yahan se agla page trigger hoga jab hum Step 2 par kaam karenge
            console.log("Button clicked! Ready for Step 2 login page linkage.");
            
            // Temporary click feedback animation
            document.querySelector('.arc-reactor-btn').style.animation = 'none';
            document.querySelector('.arc-reactor-btn').style.filter = 'drop-shadow(0 0 50px #fff) brightness(1.5)';
        }
    </script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stark Core Project</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            width: 100%;
            height: 100%;
            background-color: #000;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Video Background */
        .hud-bg-video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: 1;
            pointer-events: none;
        }

        /* Center Button Container */
        .main-interface-container {
            position: relative;
            z-index: 2;
        }

        /* Clickable Center Arc Reactor Button */
        .arc-reactor-trigger {
            width: 320px;
            height: 320px;
            background-image: url('From KlickPin CF Save these 13 Chic holiday table setting ideas that are perfect when you want something stylish modern and easy to copy for beginners who want - Pin-1004091679423345837.jpg');
            background-size: contain;
            background-position: center;
            background-repeat: no-repeat;
            border: none;
            border-radius: 50%;
            background-color: transparent;
            cursor: pointer;
            outline: none;
            
            /* Clean breathing neon glow animation */
            animation: corePulse 3s infinite ease-in-out;
            transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        /* Hover effect when pointer moves over the button */
        .arc-reactor-trigger:hover {
            transform: scale(1.06);
            filter: drop-shadow(0 0 30px #00d2ff) brightness(1.2);
        }

        /* Click feedback */
        .arc-reactor-trigger:active {
            transform: scale(0.96);
        }

        @keyframes corePulse {
            0% {
                filter: drop-shadow(0 0 15px rgba(0, 210, 255, 0.5));
            }
            50% {
                filter: drop-shadow(0 0 35px rgba(0, 210, 255, 0.9)) brightness(1.1);
            }
            100% {
                filter: drop-shadow(0 0 15px rgba(0, 210, 255, 0.5));
            }
        }
    </style>
</head>
<body>

    <video class="hud-bg-video" autoplay loop muted playsinline>
        <source src="From KlickPin CF 8 Minimal weekend getaway ideas that help you create a polished look with very simple and affordable details for beginners who want impressive - Pin-1109855901925923773.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>

    <div class="main-interface-container">
        <button class="arc-reactor-trigger" onclick="loadNextPage()"></button>
    </div>

    <script>
        function loadNextPage() {
            // Abhi yeh console par feedback dega. 
            // Jab aap agla design aur name denge, toh hum yahan redirect logic lagayenge.
            console.log("Core Activated. Triggering Step 2.");
        }
    </script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stark Core Project</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            width: 100%;
            height: 100%;
            background-color: #000;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* 1. Background Video Setup */
        .hud-bg-video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: 1;
            pointer-events: none;
        }

        /* 2. Center Button Wrapper */
        .main-interface-container {
            position: relative;
            z-index: 2;
        }

        /* 3. High-Tech Arc Reactor Button */
        .arc-reactor-trigger {
            width: 300px;
            height: 300px;
            /* Aapki di hui Arc Reactor image ka path */
            background-image: url('From KlickPin CF Save these 13 Chic holiday table setting ideas that are perfect when you want something stylish modern and easy to copy for beginners who want - Pin-1004091679423345837.jpg');
            background-size: contain;
            background-position: center;
            background-repeat: no-repeat;
            border: none;
            border-radius: 50%;
            background-color: transparent;
            cursor: pointer;
            outline: none;
            
            /* Breathing pulse effect */
            animation: corePulse 3s infinite ease-in-out;
            transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        /* Touch or Hover effect */
        .arc-reactor-trigger:hover {
            transform: scale(1.05);
            filter: drop-shadow(0 0 40px #00d2ff) brightness(1.3);
        }

        .arc-reactor-trigger:active {
            transform: scale(0.95);
        }

        @keyframes corePulse {
            0% {
                filter: drop-shadow(0 0 15px rgba(0, 210, 255, 0.6));
            }
            50% {
                filter: drop-shadow(0 0 35px rgba(0, 210, 255, 1)) brightness(1.1);
            }
            100% {
                filter: drop-shadow(0 0 15px rgba(0, 210, 255, 0.6));
            }
        }
    </style>
</head>
<body>

    <video class="hud-bg-video" autoplay loop muted playsinline>
        <source src="From KlickPin CF 8 Minimal weekend getaway ideas that help you create a polished look with very simple and affordable details for beginners who want impressive - Pin-1109855901925923773.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>

    <div class="main-interface-container">
        <button class="arc-reactor-trigger" onclick="loadNextPage()"></button>
    </div>

    <script>
        function loadNextPage() {
            // Jab aap agla design aur name denge, toh hum is click par use open karenge
            console.log("Core Activated. Waiting for Step 2 data.");
        }
    </script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stark Industries | Core System</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            width: 100%;
            height: 100%;
            background-color: #000;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        /* 1. Base Green Glitch Video Background */
        .bg-video-base {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: 1;
            opacity: 0.5;
            pointer-events: none;
        }

        /* 2. Cyan Tech Overlay Video (Holographic Interface) */
        .bg-video-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: contain; /* Isko center grid banane ke liye contain rakha hai */
            z-index: 2;
            opacity: 0.4;
            mix-blend-mode: screen; /* Dono videos ko aapas mein behtareen blend karne ke liye */
            pointer-events: none;
        }

        /* CRT monitor lines effect for real Tony Stark system feel */
        .crt-lines {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%);
            background-size: 100% 4px;
            z-index: 3;
            pointer-events: none;
        }

        /* 3. Center Arc Reactor Button Layout */
        .center-core-wrapper {
            position: relative;
            z-index: 4;
            transition: all 0.8s ease-in-out;
        }

        .arc-reactor-btn {
            width: 320px;
            height: 320px;
            background-image: url('From KlickPin CF Save these 13 Chic holiday table setting ideas that are perfect when you want something stylish modern and easy to copy for beginners who want - Pin-1004091679423345837.jpg');
            background-size: contain;
            background-position: center;
            background-repeat: no-repeat;
            border: none;
            border-radius: 50%;
            background-color: transparent;
            cursor: pointer;
            outline: none;
            
            /* Breathing energy pulse animation */
            animation: starkPulse 2.5s infinite ease-in-out;
            transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275), filter 0.3s;
        }

        /* Hover / Touch Effect */
        .arc-reactor-btn:hover {
            transform: scale(1.08);
            filter: drop-shadow(0 0 50px #00d2ff) brightness(1.3);
        }

        /* Tap/Click Feedback */
        .arc-reactor-btn:active {
            transform: scale(0.94);
        }

        /* System Transition Animation on Click */
        .system-disassemble {
            transform: scale(0);
            opacity: 0;
            filter: blur(20px);
        }

        @keyframes starkPulse {
            0% {
                filter: drop-shadow(0 0 20px rgba(0, 210, 255, 0.6)) brightness(1);
            }
            50% {
                filter: drop-shadow(0 0 45px rgba(0, 210, 255, 1)) brightness(1.2);
            }
            100% {
                filter: drop-shadow(0 0 20px rgba(0, 210, 255, 0.6)) brightness(1);
            }
        }
    </style>
</head>
<body>

    <video class="bg-video-base" autoplay loop muted playsinline>
        <source src="From KlickPin CF 30 Luxury air fryer dinner recipes that instantly upgrade your space style or celebration without much effort for anyone who wants easy but elegant - Pin-788833690984322453.mp4" type="video/mp4">
    </video>

    <video class="bg-video-overlay" autoplay loop muted playsinline>
        <source src="From KlickPin CF 8 Minimal weekend getaway ideas that help you create a polished look with very simple and affordable details for beginners who want impressive - Pin-1109855901925923773(1).mp4" type="video/mp4">
    </video>

    <div class="crt-lines"></div>

    <div class="center-core-wrapper" id="coreWrapper">
        <button class="arc-reactor-btn" onclick="triggerSystem()"></button>
    </div>

    <script>
        function triggerSystem() {
            const core = document.getElementById('coreWrapper');
            // Element ko disappear karne ki animation activate hogi
            core.classList.add('system-disassemble');
            
            console.log("Step 1 Complete. Core Disassembled. Ready for Step 2 page loading.");
        }
    </script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stark Industries | Ultimate Core</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            width: 100%;
            height: 100%;
            background-color: #000;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Courier New', Courier, monospace;
            position: relative;
        }

        /* 1. Base Green Glitch Video Background */
        .bg-video-base {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: 1;
            opacity: 0.4;
            pointer-events: none;
        }

        /* 2. Cyan Tech Overlay Video (Holographic Sync) */
        .bg-video-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: contain;
            z-index: 2;
            opacity: 0; /* Shuru mein hidden rahegi */
            mix-blend-mode: screen;
            pointer-events: none;
            transition: opacity 1.5s ease-in-out;
        }

        /* CRT Scanlines Overlay */
        .crt-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.3) 50%);
            background-size: 100% 4px;
            z-index: 3;
            pointer-events: none;
        }

        /* Main Master Interface Container */
        .master-interface-wrapper {
            position: relative;
            z-index: 4;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            transform: scale(0.8); /* Shuru mein thoda bikhra/chota hoga */
            opacity: 0.7;
            transition: all 1.2s cubic-bezier(0.19, 1, 0.22, 1);
        }

        /* Touch karne par jab system assemble ho jaye */
        .system-assembled {
            transform: scale(1);
            opacity: 1;
        }

        /* Center Arc Reactor Button */
        .arc-reactor-core {
            width: 260px;
            height: 260px;
            background-image: url('From KlickPin CF Save these 13 Chic holiday table setting ideas that are perfect when you want something stylish modern and easy to copy for beginners who want - Pin-1004091679423345837.jpg');
            background-size: contain;
            background-position: center;
            background-repeat: no-repeat;
            border: none;
            border-radius: 50%;
            background-color: transparent;
            cursor: pointer;
            outline: none;
            animation: idlePulse 3s infinite ease-in-out;
            transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275), filter 0.4s;
        }

        .arc-reactor-core:hover {
            transform: scale(1.05);
            filter: drop-shadow(0 0 40px #00d2ff) brightness(1.2);
        }

        /* System Login Panel (Smooth fade-in after assembly) */
        .login-panel {
            margin-top: 25px;
            opacity: 0;
            transform: translateY(20px);
            transition: all 1s ease-in-out;
            pointer-events: none;
            text-align: center;
        }

        .login-panel.show {
            opacity: 1;
            transform: translateY(0);
            pointer-events: auto;
        }

        .stark-input {
            background: transparent;
            border: 1px solid rgba(0, 210, 255, 0.3);
            border-radius: 4px;
            padding: 10px 20px;
            color: #00d2ff;
            font-size: 1.1rem;
            text-align: center;
            outline: none;
            letter-spacing: 5px;
            box-shadow: inset 0 0 10px rgba(0, 210, 255, 0.1);
            transition: all 0.3s ease;
        }

        .stark-input:focus {
            border-color: #00d2ff;
            box-shadow: 0 0 15px rgba(0, 210, 255, 0.4), inset 0 0 10px rgba(0, 210, 255, 0.2);
        }

        .status-message {
            margin-top: 15px;
            color: #00d2ff;
            font-size: 0.8rem;
            letter-spacing: 3px;
            text-transform: uppercase;
            text-shadow: 0 0 8px rgba(0, 210, 255, 0.5);
        }

        /* Animations */
        @keyframes idlePulse {
            0%, 100% { filter: drop-shadow(0 0 15px rgba(0, 210, 255, 0.5)) brightness(1); }
            50% { filter: drop-shadow(0 0 35px rgba(0, 210, 255, 0.9)) brightness(1.15); }
        }
    </style>
</head>
<body onclick="assembleSystem()">

    <video class="bg-video-base" autoplay loop muted playsinline>
        <source src="From KlickPin CF 30 Luxury air fryer dinner recipes that instantly upgrade your space style or celebration without much effort for anyone who wants easy but elegant - Pin-788833690984322453.mp4" type="video/mp4">
    </video>

    <video class="bg-video-overlay" id="techOverlay" loop muted playsinline>
        <source src="From KlickPin CF 8 Minimal weekend getaway ideas that help you create a polished look with very simple and affordable details for beginners who want impressive - Pin-1109855901925923773(1).mp4" type="video/mp4">
    </video>

    <div class="crt-overlay"></div>

    <div class="master-interface-wrapper" id="interfaceWrapper">
        <button class="arc-reactor-core" onclick="event.stopPropagation(); assembleSystem();" title="Touch to Assemble System"></button>
        
        <div class="login-panel" id="loginPanel">
            <input type="password" id="passkey" class="stark-input" placeholder="CODE" onkeydown="if(event.key==='Enter') verifyAccess()">
            <div class="status-message" id="statusText">SYSTEM STATUS: OFFLINE</div>
        </div>
    </div>

    <script>
        let isAssembled = false;

        // Step 1: Touch Screen or Button to Assemble Everything
        function assembleSystem() {
            if (isAssembled) return;
            
            isAssembled = true;
            
            // Elements trigger karna
            const wrapper = document.getElementById('interfaceWrapper');
            const overlayVideo = document.getElementById('techOverlay');
            const loginPanel = document.getElementById('loginPanel');
            const statusText = document.getElementById('statusText');

            // 1. Play the second overlay video and fade it in
            overlayVideo.play();
            overlayVideo.style.opacity = "0.4";

            // 2. Scale up and assemble interface
            wrapper.classList.add('system-assembled');

            // 3. Smoothly show login box
            setTimeout(() => {
                loginPanel.classList.add('show');
                statusText.innerText = "ARC REACTOR SYNCED. ENTER CODE.";
                document.getElementById('passkey').focus();
            }, 800);
        }

        // Step 2: Password verification and voice logic
        function verifyAccess() {
            const codeInput = document.getElementById('passkey');
            const statusText = document.getElementById('statusText');

            if (codeInput.value === "20064") {
                statusText.innerText = "ACCESS GRANTED. GATEWAY OPEN.";
                statusText.style.color = "#fff";
                statusText.style.textShadow = "0 0 10px #fff";

                // Premium Intelligent Voice Logic
                const speech = new SpeechSynthesisUtterance("Assalamu Alaikum, JAAN. All systems are assembled and fully operational. Welcome back.");
                speech.pitch = 1.0; 
                speech.rate = 0.9; 
                window.speechSynthesis.speak(speech);

                // Click effect feedback
                document.querySelector('.arc-reactor-core').style.filter = 'drop-shadow(0 0 60px #fff) brightness(1.5)';
                
                // Yahan se aap apna agla page link kar sakte hain jo click par open hona hai
                setTimeout(() => {
                    console.log("Redirecting to the next page...");
                }, 2000);

            } else {
                statusText.innerText = "ACCESS DENIED. SECURITY ALERT.";
                statusText.style.color = "#ff3b30";
                statusText.style.textShadow = "0 0 10px #ff3b30";
                
                const errorSpeech = new SpeechSynthesisUtterance("Access Denied.");
                window.speechSynthesis.speak(errorSpeech);
                
                codeInput.value = ""; // Clear password on failure
            }
        }
    </script>

</body>
</html>
</body>
</html>
