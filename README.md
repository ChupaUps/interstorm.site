<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>INTERSTORM</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

        body {
            background: linear-gradient(to right, #003366, #006699);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: 'Montserrat', sans-serif;
            color: #ffffff;
        }
        .logo {
            max-width: 300px;
            margin-bottom: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .button {
            font-size: 24px;
            padding: 15px 30px;
            background: linear-gradient(to right, #ff7e5f, #feb47b);
            color: #ffffff;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.3s;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .button:hover {
            background: linear-gradient(to right, #feb47b, #ff7e5f);
            transform: translateY(-5px);
        }
        .button:active {
            transform: translateY(0);
        }
    </style>
    <link rel="icon" href="favicon.ico" type="image/x-icon">
</head>
<body>
    <img src="logo.png" alt="Interstorm Logo" class="logo">
    <button class="button" onclick="window.location.href='https://interstorm.ru'">Перейти на главную страницу INTERSTORM</button>
</body>
</html>
