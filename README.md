<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine, Vibha?</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <div class="container">
        <div class="intro">
            <h1>🎉 Hey Vibha! 🎉</h1>
            <p>I've been thinking about this for a while...</p>
            <p>So, I made this to ask you a very important question... 👀</p>
        </div>

        <div class="question">
            <h2>💌 WILL YOU BE MY VALENTINE? 💌</h2>
            <div class="options">
                <button class="yes-btn" onclick="answer('yes')">Yes! 💖</button>
                <button class="no-btn" onclick="answer('no')">Nope 😅</button>
            </div>
        </div>

        <div class="answer" id="answer"></div>
    </div>

    <script src="script.js"></script>
</body>
</html>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    background: #ffefff;
    color: #333;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    flex-direction: column;
}

.container {
    text-align: center;
    max-width: 600px;
    padding: 30px;
    border-radius: 15px;
    background-color: #fff;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.intro h1 {
    font-size: 2.5rem;
    color: #ff4081;
    margin-bottom: 10px;
}

.intro p {
    font-size: 1.2rem;
    color: #555;
    margin-bottom: 20px;
}

.question h2 {
    font-size: 2rem;
    margin-bottom: 20px;
    color: #ff4081;
}

.options button {
    font-size: 1.2rem;
    padding: 15px 25px;
    margin: 10px;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    transition: 0.3s ease-in-out;
}

.yes-btn {
    background-color: #4caf50;
    color: white;
}

.no-btn {
    background-color: #f44336;
    color: white;
}

.options button:hover {
    transform: scale(1.1);
}

.answer {
    font-size: 1.5rem;
    margin-top: 30px;
}
function answer(response) {
    const answerDiv = document.getElementById("answer");

    if (response === 'yes') {
        answerDiv.innerHTML = "💖 Yay! You said YES! 💖<br>Enjoy the music! 🎶";
        setTimeout(function() {
            window.location.href = "https://open.spotify.com/track/2G2YzndIA6jeWFPBXhUjh5";  // Redirect to 'Be My Baby' by The Ronettes on Spotify
        }, 3000); // Delay for 3 seconds before redirect
    } else {
        answerDiv.innerHTML = "😅 Oops! That's okay! You're still awesome! ❤️";
        setTimeout(function() {
            window.location.href = "https://www.youtube.com/watch?v=dQw4w9WgXcQ";  // Rickroll link
        }, 3000); // Delay for 3 seconds before redirect
    }
}
