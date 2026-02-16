<!DOCTYPE html>
<html lang="ru">
<head>
<!-- Yandex.Metrika counter -->
<script type="text/javascript">
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
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&display=swap" rel="stylesheet">
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
            background-color: #000;
            color: #fff;
            overflow: hidden;
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
            font-size: clamp(2.2rem, 8vw, 4.2rem);
            color: #3137fd;
            margin-bottom: clamp(15px, 3vw, 25px);
            font-weight: 700;
            cursor: pointer;
            line-height: 1.1;
            letter-spacing: -0.02em;
            z-index: 3;
            text-shadow: 0 0 8px rgba(49, 55, 253, 0.6);
            word-break: break-word;
            hyphens: auto;
        }

        .content {
            z-index: 3;
            padding: clamp(15px, 4vw, 25px);
            max-width: 95%;
            width: 100%;
        }

        .content h1 {
            font-size: clamp(1.6rem, 5.5vw, 2.3rem);
            margin-bottom: clamp(12px, 2.5vw, 20px);
            font-weight: 700;
            line-height: 1.3;
            word-break: break-word;
            hyphens: auto;
        }

        .content h2 {
            font-size: clamp(1.1rem, 3.8vw, 1.5rem);
            margin: clamp(10px, 2vw, 18px) 0 clamp(20px, 3vw, 25px);
            font-weight: 400;
            line-height: 1.45;
            opacity: 0.95;
            word-break: break-word;
            hyphens: auto;
        }

        .content button {
            padding: clamp(12px, 2.5vw, 16px) clamp(25px, 5vw, 35px);
            font-size: clamp(1rem, 2.8vw, 1.15rem);
            color: #fff;
            background: linear-gradient(120deg, #3137fd, #5a5fff);
            border: none;
            border-radius: 50px;
            cursor: pointer;
            margin-top: clamp(15px, 3vw, 22px);
            font-family: 'Montserrat', sans-serif;
            font-weight: 600;
            letter-spacing: 0.5px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 12px rgba(49, 55, 253, 0.4);
            z-index: 3;
            max-width: 95%;
            width: auto;
        }

        .content button:hover {
            background: linear-gradient(120deg, #262cd5, #4a4fe5);
            transform: translateY(-2px);
            box-shadow: 0 6px 18px rgba(49, 55, 253, 0.6);
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

        /* Адаптация для очень маленьких экранов */
        @media (max-width: 480px) {
            .header {
                font-size: clamp(1.8rem, 9vw, 2.8rem);
            }
            
            .content h1 {
                font-size: clamp(1.4rem, 6vw, 1.8rem);
            }
            
            .content h2 {
                font-size: clamp(1rem, 4.5vw, 1.3rem);
            }
            
            .content button {
                width: 100%;
                max-width: 380px;
            }
        }

        /* Адаптация для больших экранов */
        @media (min-width: 1440px) {
            .content {
                max-width: 800px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header" id="header">INTERSTORM</div>
        <div class="content">
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

            function resizeCanvas() {
                canvas.width = window.innerWidth;
                canvas.height = window.innerHeight;
            }
            resizeCanvas();

            header.addEventListener('click', () => {
                window.location.href = 'https://interstorm.ru';
            });

            mainButton.addEventListener('click', () => {
                window.location.href = 'https://interstorm.ru';
            });

            function drawLightning(x, y, length, angle, depth, colorStop1, colorStop2) {
                if (depth === 0) return;

                ctx.beginPath();
                ctx.moveTo(x, y);

                let endX = x + length * Math.cos(angle);
                let endY = y + length * Math.sin(angle);

                let controlX1 = x + (length / 3) * Math.cos(angle) + (Math.random() - 0.5) * length * 0.3;
                let controlY1 = y + (length / 3) * Math.sin(angle) + (Math.random() - 0.5) * length * 0.3;
                let controlX2 = x + (2 * length / 3) * Math.cos(angle) + (Math.random() - 0.5) * length * 0.3;
                let controlY2 = y + (2 * length / 3) * Math.sin(angle) + (Math.random() - 0.5) * length * 0.3;

                ctx.bezierCurveTo(controlX1, controlY1, controlX2, controlY2, endX, endY);

                let gradient = ctx.createLinearGradient(x, y, endX, endY);
                gradient.addColorStop(0, colorStop1);
                gradient.addColorStop(1, colorStop2);
                ctx.strokeStyle = gradient;

                ctx.lineWidth = Math.random() * 3 + 1;
                ctx.stroke();

                if (depth > 1) {
                    let branchCount = Math.floor(Math.random() * 3) + 1;
                    for (let i = 0; i < branchCount; i++) {
                        let branchAngle = angle + (Math.random() - 0.5) * Math.PI / 4;
                        let branchLength = length * (Math.random() * 0.5 + 0.3);
                        drawLightning(endX, endY, branchLength, branchAngle, depth - 1, colorStop1, colorStop2);
                    }
                }
            }

            function createLightning() {
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                const count = window.innerWidth < 768 ? 1 : Math.floor(Math.random() * 2) + 1;
                for (let i = 0; i < count; i++) {
                    let x = Math.random() * canvas.width;
                    let y = Math.random() * (canvas.height / 3);
                    let length = window.innerWidth < 768 ? Math.random() * 100 + 70 : Math.random() * 150 + 100;
                    let angle = Math.PI / 2 + (Math.random() - 0.5) * Math.PI / 8;
                    drawLightning(x, y, length, angle, 4, '#ffffff', '#00ffff');
                }
                canvas.classList.add('glow');
                setTimeout(() => canvas.classList.remove('glow'), 1000);
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

            // Запуск анимации молний (без анимации текста)
            setTimeout(() => {
                startAnimationCycle();
                setInterval(startAnimationCycle, 20000);
            }, 5000);

            window.addEventListener('resize', resizeCanvas);
        });
    </script>

    <style>
        /* Анимации только для молний и заголовка при эффекте */
        @keyframes neon {
            0%, 100% { text-shadow: 0 0 5px #00ffff, 0 0 10px #00ffff, 0 0 20px #00ffff; }
            50% { text-shadow: 0 0 10px #00ffff, 0 0 20px #00ffff, 0 0 30px #00ffff; }
        }
        .neon-text {
            animation: neon 1.5s ease-in-out infinite alternate;
            color: #00ffff;
        }
        @keyframes glow {
            0% { filter: drop-shadow(0 0 5px #00ffff) drop-shadow(0 0 10px #00ffff); }
            100% { filter: drop-shadow(0 0 10px #00ffff) drop-shadow(0 0 25px #00ffff); }
        }
        .glow { animation: glow 1s ease-in-out infinite alternate; }
    </style>
</body>
</html>
