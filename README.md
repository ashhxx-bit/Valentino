.......
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body {
            text-align: center;
            font-family: 'Arial', sans-serif;
            background-color: #ffdde1;
            color: #d6336c;
        }
        h1 {
            font-size: 3em;
            margin-top: 50px;
        }
        p {
            font-size: 1.5em;
        }
        .heart-button {
            display: inline-block;
            padding: 15px 30px;
            font-size: 1.5em;
            color: white;
            background: #d6336c;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: 0.3s;
        }
        .heart-button:hover {
            background: #ff4d6d;
        }
    </style>
</head>
<body>
    <h1>Will You Be My Valentine? ❤️</h1>
    <p>You're my favorite person in the world. Say yes? 😊</p>
    <button class="heart-button" onclick="showLove()">YES!</button>

    <script>
        function showLove() {
            document.body.innerHTML = "<h1>YAY! ❤️ I love you! 😍</h1>";
        }
    </script>
</body>
</html>
