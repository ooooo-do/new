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
