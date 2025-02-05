
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
            overflow: hidden;
        }
        h1 {
            font-size: 3em;
            margin-top: 50px;
        }
        p {
            font-size: 1.5em;
        }
        .button-container {
            margin-top: 20px;
        }
        .heart-button, .no-button {
            display: inline-block;
            padding: 15px 30px;
            font-size: 1.5em;
            color: white;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: 0.3s;
            margin: 10px;
        }
        .heart-button {
            background: #d6336c;
        }
        .heart-button:hover {
            background: #ff4d6d;
        }
        .no-button {
            background: #333;
        }
        .no-button:hover {
            background: #555;
        }
        .love-message, .sad-message {
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
        .emoji {
            position: absolute;
            font-size: 2em;
            animation: float 4s ease-in-out infinite;
        }
        @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100vh); opacity: 0; }
        }
    </style>
</head>
<body>

    <h1>Will You Be My Valentine? ❤️</h1>
    <p>You have to choose...</p>

    <div class="button-container">
        <button class="heart-button" onclick="showLove()">YES!</button>
        <button class="no-button" onclick="showSad()">NO </button>
    </div>

    <div class="love-message" id="loveMessage">
        <p>Yay! 🎉 I knew you'd say YES! 💖</p>
        <p>I'M TECHYYY TOOOOOO SO I WIN ! AND OK FINE I love you! MWAHH PUCHII😘 btw that's how u be the boyfriend of this relationship hahahahhahahahahaha.....</p>
    </div>

    <div class="sad-message" id="sadMessage">
        <p>Oh no... 💔</p>
        <p>And OHHH FUCKKKK YOUUUUUUU ☺️☺️☺️☺️☺️☺️ </p>
    </div>

    <audio id="bg-music" loop>
        <source src="https://www.bensound.com/bensound-music/bensound-romantic.mp3" type="audio/mp3">
    </audio>
    
    <audio id="sad-music" loop>
        <source src="https://www.bensound.com/bensound-music/bensound-sad.mp3" type="audio/mp3">
    </audio>

    <script>
        function showLove() {
            document.getElementById("loveMessage").style.display = "block";
            document.getElementById("sadMessage").style.display = "none";
            document.getElementById("bg-music").play();
            document.getElementById("sad-music").pause();
            createFlirtyEmoji();  // Start creating 😏 emojis
        }

        function showSad() {
            document.getElementById("sadMessage").style.display = "block";
            document.getElementById("loveMessage").style.display = "none";
            document.getElementById("sad-music").play();
            document.getElementById("bg-music").pause();
            createSadEmoji();  // Start creating ☺️ emojis
        }

        // Create flirty 😏 emojis when "YES" is clicked
        function createFlirtyEmoji() {
            const emoji = document.createElement("div");
            emoji.classList.add("emoji");
            emoji.innerHTML = "😏";
            emoji.style.left = Math.random() * 100 + "vw";  // Random horizontal position
            emoji.style.animationDuration = Math.random() * 3 + 2 + "s";  // Random float speed
            document.body.appendChild(emoji);
            setTimeout(() => { emoji.remove(); }, 4000); // Remove emoji after animation
        }

        // Create sarcastic ☺️ emojis when "NO" is clicked
        function createSadEmoji() {
            const emoji = document.createElement("div");
            emoji.classList.add("emoji");
            emoji.innerHTML = "☺️";
            emoji.style.left = Math.random() * 100 + "vw";  // Random horizontal position
            emoji.style.animationDuration = Math.random() * 3 + 2 + "s";  // Random float speed
            document.body.appendChild(emoji);
            setTimeout(() => { emoji.remove(); }, 4000); // Remove emoji after animation
        }

        // Continuously create floating emojis after "YES" or "NO"
        setInterval(createFlirtyEmoji, 500);
        setInterval(createSadEmoji, 500);
    </script>

</body>
</html>
