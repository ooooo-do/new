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
