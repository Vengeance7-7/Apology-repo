# Apology-repo
For her
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Apology & Love</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: url('https://www.shutterstock.com/search/heart-background') no-repeat center center fixed;
            background-size: cover;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
            color: white;
        }

        .container {
            text-align: center;
            padding: 40px;
            background-color: rgba(0, 0, 0, 0.7);
            border-radius: 10px;
            width: 90%;
            max-width: 500px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            opacity: 0;
            animation: fadeIn 2s forwards;
        }

        h1 {
            font-size: 36px;
            color: #ffcccb;
            animation: bounce 2s infinite;
        }

        p {
            font-size: 18px;
            line-height: 1.5;
            margin-top: 20px;
            animation: fadeInText 2s 1s forwards;
        }

        button {
            margin-top: 20px;
            padding: 15px 25px;
            font-size: 18px;
            background-color: #ff6699;
            border: none;
            border-radius: 5px;
            color: white;
            cursor: pointer;
            opacity: 0;
            animation: fadeInButton 2s 1.5s forwards;
            transition: transform 0.3s ease-in-out;
        }

        button:hover {
            transform: scale(1.1);
        }

        .toggle-container {
            margin-top: 20px;
        }

        .toggle-container label {
            font-size: 20px;
            font-weight: bold;
        }

        .toggle-buttons {
            display: flex;
            justify-content: center;
            margin-top: 10px;
        }

        .toggle-buttons input {
            margin: 0 15px;
        }

        .name-container input {
            padding: 10px;
            font-size: 16px;
            width: 70%;
            margin-top: 20px;
            border-radius: 5px;
        }

        .name-container button {
            margin-top: 20px;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @keyframes fadeInText {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @keyframes fadeInButton {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @keyframes bounce {
            0% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
            100% {
                transform: translateY(0);
            }
        }

        /* Styles for the hidden sections */
        .section {
            display: none;
        }

        .section.active {
            display: block;
        }

        #personal-message {
            font-size: 24px;
            color: #ffcccb;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <!-- First Section: Name Input -->
    <div class="container section active" id="section-1">
        <h1>I'm Sorry... Can We Talk?</h1>
        <p>I've been thinking about this for a while, and I need to express how much I care. My actions might've hurt you, and that wasn't my intention. Please know how deeply I regret it, and I hope we can make things better.</p>
        <button onclick="goToSection(2)">Next</button>
    </div>

    <!-- Second Section: Apology -->
    <div class="container section" id="section-2">
        <h1>Heartfelt Apology</h1>
        <p>I want to hear what’s on your heart, no matter what. I care deeply and I want to make it right.</p>
        <button onclick="goToSection(3)">Next</button>
    </div>

    <!-- Third Section: Name Entry -->
    <div class="container section" id="section-3">
        <h1>What's Your Name?</h1>
        <p>Please enter your name to continue:</p>
        <div class="name-container">
            <input type="text" id="userName" placeholder="Enter your name">
            <button onclick="submitName()">Submit</button>
        </div>
    </div>

    <!-- Fourth Section: Displaying Creator's Message -->
    <div class="container section" id="section-4">
        <h1>Creator's Love</h1>
        <p id="personal-message"></p>
        <button onclick="goToSection(5)">Next</button>
    </div>

    <!-- Fifth Section: Song Embed -->
    <div id="song" class="section">
        <iframe allow="autoplay *; encrypted-media *; fullscreen *; clipboard-write" frameborder="0" height="450" style="width:100%;max-width:660px;overflow:hidden;border-radius:10px;" sandbox="allow-forms allow-popups allow-same-origin allow-scripts allow-storage-access-by-user-activation allow-top-navigation-by-user-activation" src="https://embed.music.apple.com/us/album/die-with-a-smile-single/1762656724?app=music&at=10lw9d&ct=top5&itscg=30200&itsct=music_link&autoplay=true"></iframe>
    </div>

    <script>
        function goToSection(sectionNumber) {
            // Hide all sections
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => section.classList.remove('active'));

            // Show the selected section
            const activeSection = document.getElementById('section-' + sectionNumber);
            activeSection.classList.add('active');
        }

        function submitName() {
            const userName = document.getElementById("userName").value;

            if (userName) {
                const message = `The creator loves you to the multiverse, ${userName}!`;
                document.getElementById("personal-message").textContent = message;
                goToSection(4); // Go to the next section displaying the message
            } else {
                alert("Please enter your name!");
            }
        }
    </script>
</body>
</html>
