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
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            font-family: 'Montserrat', sans-serif;
            overflow: hidden;
            background-color: #000;
            color: #fff;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
            position: relative;
            text-align: center;
            z-index: 3;
        }
        
        .header {
            font-size: clamp(2.5rem, 8vw, 4.5rem);
            color: #3137fd;
            margin-bottom: clamp(15px, 3vw, 30px);
            font-weight: 700;
            cursor: pointer;
            transition: color 0.5s;
            line-height: 1.1;
            letter-spacing: -0.03em;
            z-index: 3;
            text-shadow: 0 0 10px rgba(49, 55, 253, 0.7);
        }
        
        .content {
            z-index: 3;
            padding: clamp(15px, 4vw, 30px);
            max-width: 95%;
            width: 100%;
        }
        
        .content h1 {
            font-size: clamp(1.75rem, 5vw, 2.5rem);
            margin-bottom: clamp(15px, 2.5vw, 25px);
            display: inline-block;
            border-right: 2px solid #3137fd;
            white-space: nowrap;
            overflow: hidden;
            animation: typing 2.5s steps(45, end), blink 0.5s step-end infinite alternate;
            line-height: 1.3;
            max-width: 100%;
        }
        
        .content h2 {
            font-size: clamp(1.1rem, 3.5vw, 1.6rem);
            margin: clamp(10px, 2vw, 20px) 0 clamp(20px, 3vw, 30px);
            font-weight: 400;
            line-height: 1.5;
            opacity: 0.95;
            max-width: 100%;
            padding: 0 5px;
        }
        
        .content button {
            padding: clamp(12px, 2.5vw, 18px) clamp(25px, 5vw, 40px);
            font-size: clamp(1rem, 2.5vw, 1.2rem);
            color: #fff;
            background: linear-gradient(120deg, #3137fd, #5a5fff);
            border: none;
            border-radius: 50px;
            cursor: pointer;
            margin-top: clamp(15px, 3vw, 25px);
            font-family: 'Montserrat', sans-serif;
            font-weight: 600;
            letter-spacing: 0.5px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(49, 55, 253, 0.4);
            z-index: 3;
            max-width: 95%;
            width: auto;
        }
        
        .content button:hover {
            background: linear-gradient(120deg, #262cd5, #4a4fe5);
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(49, 55, 253, 0.6);
        }
        
        .content button:active {
            transform: translateY(1px);
        }
        
        .background-image {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 120%;
            height: 120%;
            transform: translate(-50%, -50%);
            object-fit: cover;
            z-index: 0;
            opacity: 0.15;
            filter: blur(2px);
        }
        
        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.85);
            z-index: 1;
            opacity: 0;
            transition: opacity 5s;
            pointer-events: none;
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
                text-shadow: 0 0 5px #00ffff, 0 0 10px #00ffff, 0 0 20px #00ffff, 0 0 40px #00ffff;
            }
            50% {
                text-shadow: 0 0 10px #00ffff, 0 0 20px #00ffff, 0 0 30px #00ffff, 0 0 50px #00ffff;
            }
        }
        
        .neon-text {
            animation: neon 1.5s ease-in-out infinite alternate;
            color: #00ffff;
            text-shadow: 0 0 5px #00ffff, 0 0 10px #00ffff, 0 0 20px #00ffff, 0 0 40px #00ffff;
        }
        
        @keyframes glow {
            0% {
                filter: drop-shadow(0 0 5px #00ffff) drop-shadow(0 0 10px #00ffff);
            }
            100% {
                filter: drop-shadow(0 0 10px #00ffff) drop-shadow(0 0 25px #00ffff);
            }
        }
        
        .glow {
            animation: glow 1s ease-in-out infinite alternate;
        }
        
        /* Адаптация для мобильных устройств */
        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            
            .header {
                margin-bottom: 15px;
            }
            
            .content h1 {
                margin-bottom: 15px;
                animation-duration: 3s;
            }
            
            .content h2 {
                margin: 10px 0 20px;
            }
            
            .content button {
                margin-top: 20px;
                padding: 12px 25px;
            }
        }
        
        /* Адаптация для очень маленьких экранов */
        @media (max-width: 480px) {
            .header {
                white-space: normal;
                word-break: break-word;
                line-height: 1.2;
            }
            
            .content h1 {
                white-space: normal;
                border-right: none;
                width: 100%;
                text-align: center;
                padding: 0 5px;
            }
            
            .content h2 {
                font-size: clamp(1rem, 4vw, 1.3rem);
            }
            
            .content button {
                width: 100%;
                max-width: 400px;
                padding: 14px;
            }
        }
        
        /* Адаптация для больших экранов */
        @media (min-width: 1440px) {
            .container {
                padding: 30px;
            }
            
            .content {
                max-width: 800px;
            }
        }
        
        /* Анимация появления контента */
        .fade-in {
            animation: fadeIn 1.5s ease-out forwards;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header fade-in" id="header" style="animation-delay: 0.3s">INTERSTORM</div>
        <div class="content fade-in" style="animation-delay: 0.6s">
            <h1>ИНТЕРШТОРМ Мир меняет не ИИ, а люди.</h1>
            <h2>Выстраиваем операционную эффективность в мире, где единственная константа – это изменения.</h2>
            <button id="mainButton">Перейти на главную страницу</button>
        </div>
        <img src="https://images.unsplash.com/photo-1550751863-8843f969c258?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1200&q=80" alt="Background" class="background-image">
        <div class="overlay" id="overlay"></div>
        <canvas id="lightningCanvas" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: 2;"></canvas>
    </div>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const overlay = document.getElementById('overlay');
            const header = document.getElementById('header');
            const canvas = document.getElementById('lightningCanvas');
            const ctx = canvas.getContext('2d');
            const mainButton = document.getElementById('mainButton');
            const content = document.querySelector('.content');

            // Установка размеров холста
            function resizeCanvas() {
                canvas.width = window.innerWidth;
                canvas.height = window.innerHeight;
            }
            
            resizeCanvas();
            
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
                
                // Рисуем 1-3 молнии в зависимости от размера экрана
                const lightningCount = window.innerWidth < 768 ? 1 : Math.floor(Math.random() * 2) + 1;
                
                for (let i = 0; i < lightningCount; i++) {
                    // Позиционируем молнии в верхней части экрана
                    let x = Math.random() * canvas.width;
                    let y = Math.random() * (canvas.height / 3);
                    let length = Math.random() * 150 + 100;
                    
                    // На мобильных устройствах делаем молнии короче
                    if (window.innerWidth < 768) {
                        length = Math.random() * 100 + 70;
                    }
                    
                    let angle = Math.PI / 2 + (Math.random() - 0.5) * Math.PI / 8;
                    let colorStop1 = '#ffffff'; // Белый
                    let colorStop2 = '#00ffff'; // Неоново-синий
                    drawLightning(x, y, length, angle, 4, colorStop1, colorStop2);
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

            // Функция для воспроизведения звука грома (заглушка)
            function playThunderSound() {
                // В реальном проекте здесь будет воспроизведение звука
                console.log("Thunder sound would play here");
            }

            // Запуск анимации через 5 секунд и повтор каждые 20 секунд
            setTimeout(() => {
                startAnimationCycle();
                playThunderSound();
                setInterval(() => {
                    startAnimationCycle();
                    playThunderSound();
                }, 20000);
            }, 5000);

            // Обработка изменения размера окна
            window.addEventListener('resize', () => {
                resizeCanvas();
                
                // На мобильных устройствах убираем анимацию набора текста для лучшей производительности
                if (window.innerWidth < 480) {
                    const h1 = document.querySelector('.content h1');
                    h1.style.animation = 'none';
                    h1.style.whiteSpace = 'normal';
                    h1.style.borderRight = 'none';
                    h1.style.width = 'auto';
                }
            });
            
            // Добавляем плавное появление контента
            setTimeout(() => {
                document.querySelectorAll('.fade-in').forEach(el => {
                    el.style.opacity = 1;
                });
            }, 300);
        });
    </script>
</body>
</html>
