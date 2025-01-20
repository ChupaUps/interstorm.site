<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interstorm</title>
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            font-family: 'Montserrat', sans-serif;
            overflow: hidden;
        }
        .container {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #000;
            color: #fff;
            text-align: center;
            position: relative;
        }
        .header {
            font-size: 4em;
            color: #3137fd;
            margin-bottom: 20px;
            font-weight: 700;
            cursor: pointer;
            transition: color 0.5s;
        }
        .content {
            z-index: 1;
            padding: 20px;
        }
        .content h1 {
            font-size: 2em;
            margin-bottom: 20px;
            display: inline-block;
            border-right: 2px solid #3137fd;
            white-space: nowrap;
            overflow: hidden;
            animation: typing 2s steps(30, end), blink 0.5s step-end infinite alternate;
        }
        .content button {
            padding: 15px 30px;
            font-size: 1em;
            color: #fff;
            background-color: #3137fd;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
            font-family: 'Montserrat', sans-serif;
        }
        .content button:hover {
            background-color: #262cd5;
        }
        .background-image {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 100%;
            height: auto;
            transform: translate(-50%, -50%);
            object-fit: contain;
            z-index: 0;
            opacity: 0.6;
        }
        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 1;
            opacity: 0;
            transition: opacity 5s;
        }
        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }
        @keyframes blink {
            to { border-color: transparent; }
        }
        @keyframes neon {
            0%, 100% {
                text-shadow: 0 0 5px #00ffff, 0 0 10px #00ffff, 0 0 20px #00ffff, 0 0 40px #00ffff, 0 0 80px #00ffff, 0 0 90px #00ffff, 0 0 100px #00ffff;
            }
            50% {
                text-shadow: 0 0 10px #00ffff, 0 0 20px #00ffff, 0 0 30px #00ffff, 0 0 50px #00ffff, 0 0 90px #00ffff, 0 0 110px #00ffff, 0 0 130px #00ffff;
            }
        }
        .neon-text {
            animation: neon 1.5s ease-in-out infinite alternate;
            color: #00ffff;
            text-shadow: 0 0 5px #00ffff, 0 0 10px #00ffff, 0 0 20px #00ffff, 0 0 40px #00ffff, 0 0 80px #00ffff, 0 0 90px #00ffff, 0 0 100px #00ffff;
        }
        @media (max-width: 768px) {
            .header {
                font-size: 3em;
            }
            .content h1 {
                font-size: 1.5em;
            }
            .content button {
                padding: 10px 20px;
                font-size: 0.9em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header" id="header">INTERSTORM</div>
        <div class="content">
            <h1>Помогаем производственным предприятиям зарабатывать больше</h1>
            <button onclick="window.location.href='https://interstorm.ru'">Перейти на главную страницу</button>
        </div>
        <img src="image.webp" alt="Background" class="background-image">
        <div class="overlay" id="overlay"></div>
        <canvas id="lightningCanvas" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: 2;"></canvas>
    </div>
    <script>
        const overlay = document.getElementById('overlay');
        const header = document.getElementById('header');
        const container = document.querySelector('.container');
        const canvas = document.getElementById('lightningCanvas');
        const ctx = canvas.getContext('2d');

        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        header.addEventListener('click', () => {
            window.location.href = 'https://interstorm.ru';
        });

        function drawLightning(x, y, length, angle, depth, colorStop1, colorStop2) {
            if (depth === 0) return;
            ctx.beginPath();
            ctx.moveTo(x, y);
            let endX = x + length * Math.cos(angle);
            let endY = y + length * Math.sin(angle);
            ctx.lineTo(endX, endY);

            // Градиентная окраска молнии
            let gradient = ctx.createLinearGradient(x, y, endX, endY);
            gradient.addColorStop(0, colorStop1);
            gradient.addColorStop(1, colorStop2);
            ctx.strokeStyle = gradient;

            ctx.lineWidth = Math.random() * 3 + 1;
            ctx.stroke();

            let branchAngle = Math.PI / 6;
            let branchLength = length * (Math.random() * 0.5 + 0.5);
            drawLightning(endX, endY, branchLength, angle - branchAngle, depth - 1, colorStop1, colorStop2);
            drawLightning(endX, endY, branchLength, angle + branchAngle, depth - 1, colorStop1, colorStop2);
        }

        function createLightning() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            for (let i = 0; i < 5; i++) {
                let x = Math.random() * canvas.width;
                let y = Math.random() * canvas.height / 2;
                let length = Math.random() * 200 + 100;
                let angle = Math.PI / 2;
                let colorStop1 = '#ffffff'; // Белый
                let colorStop2 = '#00ffff'; // Неоново-синий
                drawLightning(x, y, length, angle, 5, colorStop1, colorStop2);
            }
        }

        function startAnimationCycle() {
            overlay.style.opacity = 1;
            header.classList.add('neon-text');
            createLightning();
            setTimeout(() => {
                header.classList.remove('neon-text');
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                overlay.style.opacity = 0;
            }, 5000);
        }

        function playThunderSound() {
            let audio = new Audio('thunder.mp3');
            audio.play();
        }

        setTimeout(() => {
            startAnimationCycle();
            playThunderSound();
            setInterval(() => {
                startAnimationCycle();
                playThunderSound();
            }, 20000);
        }, 7000);

        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        });
    </script>
</body>
</html>
