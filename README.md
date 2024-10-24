<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohamed Salih M - Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            color: #fff;
            background: url('https://example.com/your-tech-background.jpg') no-repeat center center fixed;
            background-size: cover;
        }

        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: rgba(0, 0, 0, 0.8);
            padding: 20px;
        }

        nav ul {
            list-style: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 15px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
        }

        section {
            padding: 50px;
            background: rgba(0, 0, 0, 0.7);
            margin: 20px;
            border-radius: 10px;
        }

        h1 {
            border-bottom: 2px solid #fff;
            padding-bottom: 10px;
        }

        .skills-container {
            display: flex;
            flex-direction: column;
        }

        .skill {
            margin: 10px 0;
        }

        .progress-bar {
            background: #ccc;
            border-radius: 5px;
            overflow: hidden;
            height: 20px;
        }

        .progress {
            background: #fff;
            height: 100%;
        }

        #chatbot {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 300px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
            overflow: hidden;
        }

        #chatbox {
            height: 150px;
            overflow-y: auto;
            padding: 10px;
            border-bottom: 1px solid #ccc;
            background: #f9f9f9;
        }

        .input-container {
            display: flex;
            padding: 5px;
            background-color: #fff;
        }

        #userInput {
            flex: 1;
            border: 1px solid #ccc;
            border-radius: 4px;
            padding: 5px;
        }

        button {
            background-color: #000;
            color: white;
            border: none;
            border-radius: 4px;
            padding: 5px 10px;
            cursor: pointer;
        }

        button:hover {
            background-color: #444;
        }

        .message {
            margin: 2px 0;
        }

        .user {
            text-align: right;
            color: #000;
        }

        .bot {
            text-align: left;
            color: #333;
        }

        .preset-questions {
            margin: 10px 0;
            display: flex;
            flex-direction: column;
        }

        .preset-questions button {
            margin: 5px 0;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 4px;
            padding: 8px;
            cursor: pointer;
        }

        .preset-questions button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="logo">Mohamed Salih M</div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- About Section -->
    <section id="about">
        <h1>About Me</h1>
        <p>Hello! I'm Mohamed Salih M, an aspiring engineer currently pursuing my Bachelor's in Computer Science and Engineering at Madras Institute of Technology. I have a deep interest in IoT and PCB design. I am always eager to learn new technologies and apply them creatively.</p>
    </section>
    
    <!-- Education Section -->
    <section id="education">
        <h1>Education</h1>
        <p>I have completed my Diploma at Seshasyee Institute Of Technology in Electrical and Electronics Engineering.</p>
    </section>
    
    <!-- Skills Section -->
    <section id="skills">
        <h1>Skills</h1>
        <div class="skills-container">
            <div class="skill">
                <h3>IoT Project Design</h3>
                <div class="progress-bar"><div class="progress" style="width: 90%;"></div></div>
            </div>
            <div class="skill">
                <h3>PCB Design</h3>
                <div class="progress-bar"><div class="progress" style="width: 90%;"></div></div>
            </div>
            <div class="skill">
                <h3>C, C++</h3>
                <div class="progress-bar"><div class="progress" style="width: 75%;"></div></div>
            </div>
            <div class="skill">
                <h3>Communication & Teamwork</h3>
                <div class="progress-bar"><div class="progress" style="width: 85%;"></div></div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h1>Projects</h1>
        <div class="project-item">
            <h3>IoT-Based Smart Home System</h3>
            <p>Developed a smart home automation system using IoT technology to control home appliances through a mobile app.</p>
        </div>
        <div class="project-item">
            <h3>PCB for Custom Electronics</h3>
            <p>Designed and developed PCB layouts for custom electronic circuits using software like Eagle CAD.</p>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h1>Contact Me</h1>
        <form action="#" method="POST">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>

            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>

            <label for="message">Message:</label>
            <textarea id="message" name="message" required></textarea>

            <button type="submit">Send Message</button>
        </form>
        <div class="social-links">
            <a href="#"><i class="fab fa-linkedin"></i></a>
            <a href="#"><i class="fab fa-github"></i></a>
        </div>
    </section>

    <div id="chatbot">
        <div id="chatbox"></div>
        <div class="input-container">
            <input type="text" id="userInput" placeholder="Type a message..." />
            <button onclick="sendMessage()">Send</button>
        </div>
        <div class="preset-questions">
            <button onclick="presetMessage('What is your favorite project?')">What is your favorite project?</button>
            <button onclick="presetMessage('Can you tell me more about your skills?')">Can you tell me more about your skills?</button>
            <button onclick="presetMessage('What are your career goals?')">What are your career goals?</button>
            <button onclick="presetMessage('How do you handle challenges?')">How do you handle challenges?</button>
        </div>
    </div>

    <script>
        async function sendMessage() {
            const input = document.getElementById("userInput");
            const message = input.value;
            const chatbox = document.getElementById("chatbox");

            // Display user message
            chatbox.innerHTML += `<div class="message user">User: ${message}</div>`;
            input.value = '';

            // Fetch response from OpenAI
            const response = await getBotResponse(message);
            chatbox.innerHTML += `<div class="message bot">Bot: ${response}</div>`;
            chatbox.scrollTop = chatbox.scrollHeight; // Auto scroll to the bottom
        }

        function presetMessage(message) {
            document.getElementById("userInput").value = message;
            sendMessage();
        }

        async function getBotResponse(message) {
            // Example responses for preset messages (you can customize this)
            const responses = {
                "What is your favorite project?": "My favorite project is the IoT-Based Smart Home System because it integrates multiple technologies.",
                "Can you tell me more about your skills?": "I have skills in IoT Project Design, PCB Design, and programming in C and C++.",
                "What are your career goals?": "My goal is to work in a dynamic engineering role focused on IoT solutions.",
                "How do you handle challenges?": "I approach challenges analytically and work collaboratively with my team to find solutions."
            };

            return responses[message] || "I'm not sure about that. Can you ask something else?";
        }
    </script>
</body>
</html>
