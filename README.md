# Tima-surprise
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Special Surprise</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
            margin: 0;
            padding: 20px;
        }
        #bear-section {
            display: block;
        }
        #rose-section {
            display: none;
            background-image: url('https://i.imgur.com/4Q8Z8Z8.jpg'); /* Free rose background image; replace if needed */
            background-size: cover;
            background-position: center;
            height: 100vh;
            color: white;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        img {
            max-width: 300px;
            margin: 20px;
        }
        button {
            padding: 10px 20px;
            margin: 10px;
            font-size: 16px;
            cursor: pointer;
        }
        #yes-btn {
            background-color: #4CAF50;
            color: white;
            border: none;
        }
        #no-btn {
            background-color: #f44336;
            color: white;
            border: none;
        }
    </style>
</head>
<body>
    <div id="bear-section">
        <h1>Look at this cute bear!</h1>
        <img src="https://i.imgur.com/animated-bear-hug.gif" alt="Animated bear hugging annoyed friend"> <!-- Replace with your preferred GIF if this doesn't work -->
        <p>M9l9a mni 🙂</p>
        <button id="yes-btn">Yes</button>
        <button id="no-btn">No</button>
    </div>
    
    <div id="rose-section">
        <h1>I love you so much Tima</h1>
        <p>💖💖💖</p>
    </div>

    <script>
        let clickCount = 0;
        const maxClicks = 5; // Number of failed "Yes" clicks before it works

        document.getElementById('yes-btn').addEventListener('click', function() {
            clickCount++;
            if (clickCount < maxClicks) {
                alert('Oops, try again! 😏');
            } else {
                document.getElementById('bear-section').style.display = 'none';
                document.getElementById('rose-section').style.display = 'flex';
            }
        });

        document.getElementById('no-btn').addEventListener('click', function() {
            alert('Aww, come on! Try Yes. 😉');
        });
    </script>
</body>
</html>
