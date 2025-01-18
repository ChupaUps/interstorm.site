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
        .lightning {
            position: absolute;
            width: 2px;
            height: 100%;
            background: #3137fd;
            opacity: 0;
            animation: lightning 0.1s ease-in-out infinite;
        }
        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }
        @keyframes blink {
            to { border-color: transparent; }
        }
        @keyframes lightning {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
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
        <div class="header" onclick="window.location.href='https://interstorm.ru'">INTERSTORM</div>
        <div class="content">
            <h1>Помогаем производственным предприятиям зарабатывать больше</h1>
            <button onclick="window.location.href='https://interstorm.ru'">Перейти на главную страницу</button>
        </div>
        <img src="image.webp" alt="Background" class="background-image">
        <div class="overlay" id="overlay"></div>
    </div>
    <script>
        const overlay = document.getElementById('overlay');
        const header = document.querySelector('.header');
        const container = document.querySelector('.container');

        function startAnimationCycle() {
            overlay.style.opacity = 1;
            setTimeout(() => {
                header.style.color = '#ffa500'; // Неоново-оранжевый цвет
                createLightning();
                setTimeout(() => {
                    header.style.color = '#3137fd'; // Возвращаем фирменный цвет
                    removeLightning();
                    overlay.style.opacity = 0;
                }, 5000);
            }, 5000);
        }

        function createLightning() {
            for (let i = 0; i < 10; i++) {
                const lightning = document.createElement('div');
                lightning.className = 'lightning';
                lightning.style.left = Math.random() * 100 + 'vw';
                lightning.style.top = Math.random() * 100 + 'vh';
                lightning.style.transform = `rotate(${Math.random() * 360}deg)`;
                lightning.style.animationDelay = `${Math.random() * 5}s`;
                container.appendChild(lightning);
            }
        }

        function removeLightning() {
            const lightnings = document.querySelectorAll('.lightning');
            lightnings.forEach(lightning => container.removeChild(lightning));
        }

        setInterval(startAnimationCycle, 20000);
    </script>
</body>
</html>
