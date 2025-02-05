<!DOCTYPE html>
<html lang="ru">
<head>
<!-- Yandex.Metrika counter -->
<script type="text/javascript" >
   (function(m,e,t,r,i,k,a){m[i]=m[i]||function(){(m[i].a=m[i].a||[]).push(arguments)};
   m[i].l=1*new Date();
   for (var j = 0; j < document.scripts.length; j++) {if (document.scripts[j].src === r) { return; }}
   k=e.createElement(t),a=e.getElementsByTagName(t)[0],k.async=1,k.src=r,a.parentNode.insertBefore(k,a)})
   (window, document, "script", "https://mc.yandex.ru/metrika/tag.js", "ym");

   ym(99805595, "init", {
        clickmap:true,
        trackLinks:true,
        accurateTrackBounce:true
   });
</script>
<noscript><div><img src="https://mc.yandex.ru/watch/99805595" style="position:absolute; left:-9999px;" alt="" /></div></noscript>
<!-- /Yandex.Metrika counter -->
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
        .glow {
            animation: glow 1s ease-in-out infinite alternate;
        }
        @keyframes glow {
            0% {
                filter: drop-shadow(0 0 5px #00ffff) drop-shadow(0 0 10px #00ffff) drop-shadow(0 0 20px #00ffff);
            }
            100% {
                filter: drop-shadow(0 0 15px #00ffff) drop-shadow(0 0 30px #00ffff) drop-shadow(0 0 60px #00ffff);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header" id="header">INTERSTORM</div>
        <div class="content">
            <h1>Помогаем производственным предприятиям зарабатывать больше</h1>
            <button id="mainButton">Перейти на главную страницу</button>
        </div>
        <img src="image.webp" alt="Background" class="background-image">
        <div class="overlay" id="overlay"></div>
        <canvas id="lightningCanvas" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: 2;"></canvas>
    </div>
    <script>
        const overlay = document.getElementById('overlay');
        const header = document.getElementById('header');
        const canvas = document.getElementById('lightningCanvas');
        const ctx = canvas.getContext('2d');
        const mainButton = document.getElementById('mainButton');

        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        // Кликабельность заголовка
        header.addEventListener('click', () => {
            window.location.href = 'https://interstorm.ru';
        });

        // Переход на сайт при нажатии на кнопку
        mainButton.addEventListener('click', () => {
            window.location.href = 'https://interstorm.ru';
        });

        // Функция для рисования молнии
        function drawLightning(x, y, length, angle, depth, colorStop1, colorStop2) {
            if (depth === 0) return;

            ctx.beginPath();
            ctx.moveTo(x, y);

            // Конечная точка основной ветви
            let endX = x + length * Math.cos(angle);
            let endY = y + length * Math.sin(angle);

            // Создаем изгибы с помощью кривой Безье
            let controlX1 = x + (length / 3) * Math.cos(angle) + (Math.random() - 0.5) * length * 0.3;
            let controlY1 = y + (length / 3) * Math.sin(angle) + (Math.random() - 0.5) * length * 0.3;
            let controlX2 = x + (2 * length / 3) * Math.cos(angle) + (Math.random() - 0.5) * length * 0.3;
            let controlY2 = y + (2 * length / 3) * Math.sin(angle) + (Math.random() - 0.5) * length * 0.3;

            // Рисуем кривую Безье
            ctx.bezierCurveTo(controlX1, controlY1, controlX2, controlY2, endX, endY);

            // Градиентная окраска молнии
            let gradient = ctx.createLinearGradient(x, y, endX, endY);
            gradient.addColorStop(0, colorStop1);
            gradient.addColorStop(1, colorStop2);
            ctx.strokeStyle = gradient;

            ctx.lineWidth = Math.random() * 3 + 1;
            ctx.stroke();

            // Рекурсивно рисуем ветви
            if (depth > 1) {
                let branchCount = Math.floor(Math.random() * 3) + 1; // Количество ветвей
                for (let i = 0; i < branchCount; i++) {
                    let branchAngle = angle + (Math.random() - 0.5) * Math.PI / 4; // Угол ветви
                    let branchLength = length * (Math.random() * 0.5 + 0.3); // Длина ветви
                    drawLightning(endX, endY, branchLength, branchAngle, depth - 1, colorStop1, colorStop2);
                }
            }
        }

        // Функция для создания молний
        function createLightning() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            for (let i = 0; i < 3; i++) {
                let x = Math.random() * canvas.width;
                let y = Math.random() * canvas.height / 2;
                let length = Math.random() * 200 + 100;
                let angle = Math.PI / 2 + (Math.random() - 0.5) * Math.PI / 8;
                let colorStop1 = '#ffffff'; // Белый
                let colorStop2 = '#00ffff'; // Неоново-синий
                drawLightning(x, y, length, angle, 5, colorStop1, colorStop2);
            }
            canvas.classList.add('glow');
            setTimeout(() => {
                canvas.classList.remove('glow');
            }, 1000);
        }

        // Функция для запуска анимации
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

        // Функция для воспроизведения звука грома
        function playThunderSound() {
            let audio = new Audio('thunder.mp3');
            audio.play();
        }

        // Запуск анимации через 7 секунд и повтор каждые 20 секунд
        setTimeout(() => {
            startAnimationCycle();
            playThunderSound();
            setInterval(() => {
                startAnimationCycle();
                playThunderSound();
            }, 20000);
        }, 7000);

        // Обработка изменения размера окна
        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        });
    </script>
</body>
</html>
