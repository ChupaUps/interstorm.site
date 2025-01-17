<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interstorm</title>
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            font-family: Arial, sans-serif;
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
            overflow: hidden;
        }
        .logo {
            position: absolute;
            top: 20px;
            left: 20px;
            width: 100px; /* Adjust as needed */
        }
        .content {
            z-index: 1;
            padding: 20px;
        }
        .content h1 {
            font-size: 2em;
            margin-bottom: 20px;
        }
        .content button {
            padding: 15px 30px;
            font-size: 1em;
            color: #000;
            background-color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
        }
        .content button:hover {
            background-color: #ddd;
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
        @media (max-width: 768px) {
            .content h1 {
                font-size: 1.5em;
            }
            .content button {
                padding: 10px 20px;
                font-size: 0.9em;
            }
            .logo {
                width: 80px; /* Adjust as needed */
            }
            .background-image {
                width: 100%;
                height: auto;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <img src="logo.png" alt="Logo" class="logo">
        <div class="content">
            <h1>Помогаем производственным предприятиям зарабатывать больше</h1>
            <button onclick="window.location.href='https://interstorm.ru'">Перейти на главную страницу</button>
        </div>
        <img src="image.webp" alt="Background" class="background-image">
    </div>
</body>
</html>
