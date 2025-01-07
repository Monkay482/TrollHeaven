<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Troll Heaven</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background-color: #f0f8ff;
            color: #333;
        }
        header {
            background-color: #ff6347;
            color: white;
            text-align: center;
            padding: 1rem;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #333;
            padding: 0.5rem 0;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 1rem;
        }
        nav a:hover {
            text-decoration: underline;
        }
        .container {
            padding: 2rem;
            text-align: center;
        }
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
            margin-top: 2rem;
        }
        .gallery img {
            width: 100%;
            border-radius: 8px;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1rem;
            position: absolute;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Troll Heaven</h1>
        <p>The ultimate place for fun and laughter!</p>
    </header>
    <nav>
        <a href="#home">Home</a>
        <a href="#gallery">Gallery</a>
        <a href="#troll">Troll Yourself</a>
    </nav>

    <div class="container" id="home">
        <h2>Let the trolling begin!</h2>
        <p>Welcome to the funniest corner of the internet. Ready to laugh out loud?</p>
    </div>

    <div class="container" id="gallery">
        <h2>Gallery of Laughs</h2>
        <div class="gallery">
            <img src="https://via.placeholder.com/150" alt="Meme 1">
            <img src="https://via.placeholder.com/150" alt="Meme 2">
            <img src="https://via.placeholder.com/150" alt="Meme 3">
            <img src="https://via.placeholder.com/150" alt="Meme 4">
        </div>
    </div>

    <div class="container" id="troll">
        <h2>Troll Yourself</h2>
        <form>
            <label for="name">Enter your name:</label><br>
            <input type="text" id="name" name="name" required><br><br>
            <label for="joke">What makes you laugh?</label><br>
            <input type="text" id="joke" name="joke" required><br><br>
            <button type="button" onclick="trollUser()">Troll Me!</button>
        </form>
        <p id="output" style="margin-top: 1rem; font-weight: bold;"></p>
    </div>

    <footer>
        <p>Created by Monkay - &copy; 2025 Troll Heaven. All rights reserved.</p>
    </footer>

    <script>
        function trollUser() {
            const name = document.getElementById('name').value;
            const joke = document.getElementById('joke').value;

            if (name && joke) {
                document.getElementById('output').textContent = `Haha ${name}, you just trolled yourself by saying: "${joke}"!`;
            } else {
                document.getElementById('output').textContent = 'Please fill out all fields to get trolled!';
            }
        }
    </script>
</body>
</html>
