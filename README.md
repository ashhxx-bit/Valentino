<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine Mr.Techyy nerd?</title>
    <style>
        body {
            text-align: center;
            font-family: 'Arial', sans-serif;
            background-color: #ffdde1;
            color: #d6336c;
            overflow: hidden;
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
        .love-letter {
            display: none;
            font-size: 1.3em;
            color: #333;
            margin-top: 20px;
            padding: 20px;
            background: #fff;
            border-radius: 10px;
            width: 80%;
            max-width: 500px;
            margin-left: auto;
            margin-right: auto;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
        }
        /* Heart animation */
        @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100vh); opacity: 0; }
        }
        .heart {
            position: absolute;
            bottom: -10px;
            font-size: 2em;
            color: red;
            animation: float 5s linear infinite;
        }
    </style>
</head>
<body>

    <h1>Will You Be My Valentine Mr.Techyy nerdd? ❤️</h1>
    <p>You're my favorite headache . Say yes? 😊</p>
    
    <button class="heart-button" onclick="showLove()">YES!</button>

    <div class="love-letter" id="loveLetter">
        <p>Dear Love,</p>
        <p>you make my day complete and i love youuu for that . u are my happy place alwayssss. 💖</p>
        <p>Will you be my Valentine? ❤️</p>
    </div>

    <audio id="bg-music" loop>
        <source src="https://www.bensound.com/bensound-music/bensound-romantic.mp3" type="audio/mp3">
    </audio>

    <script>
        function showLove() {
            document.getElementById("loveLetter").style.display = "block";
            document.getElementById("bg-music").play();
        }

        // Create floating hearts
        function createHeart() {
            const heart = document.createElement("div");
            heart.classList.add("heart");
            heart.innerHTML = "❤️";
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.animationDuration = Math.random() * 3 + 2 + "s";
            document.body.appendChild(heart);
            setTimeout(() => { heart.remove(); }, 5000);
        }
        setInterval(createHeart, 500);
    </script>

</body>
</html>
