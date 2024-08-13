<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GUZUENTERPRISES</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        nav ul {
            list-style: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin: 0 10px;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
        }
        section {
            padding: 20px;
        }
        footer {
            text-align: center;
            padding: 10px 0;
            background-color: #4CAF50;
            color: white;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        form {
            max-width: 600px;
            margin: auto;
        }
        input, textarea {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            border: 1px solid #ccc;
        }
        button {
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <header>
        <h1>GUZUENTERPRISES</h1>
        <p>A Digital Marketing & AI Marketing Agency</p>
    </header>

    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#blog">Blog</a></li>
            <li><a href="#portfolio">Portfolio</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="about">
        <h2>About Us</h2>
        <p>GUZUENTERPRISES is a digital marketing and AI marketing agency offering services such as website development, graphic design, advertising, and more.</p>
    </section>

    <section id="blog">
        <h2>Blog</h2>
        <p>Stay tuned for our latest updates and insights on digital marketing and AI trends.</p>
    </section>

    <section id="portfolio">
        <h2>Portfolio</h2>
        <p>Check out our recent projects and success stories.</p>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <form id="contactForm">
            <input type="text" name="name" placeholder="Your Name" required>
            <input type="email" name="email" placeholder="Your Email" required>
            <textarea name="message" placeholder="Your Message" required></textarea>
            <button type="submit">Send</button>
        </form>
        <p id="responseMessage"></p>
    </section>

    <footer>
        <p>&copy; 2024 GUZUENTERPRISES. All rights reserved.</p>
    </footer>

    <script>
        document.getElementById('contactForm').addEventListener('submit', function(event) {
            event.preventDefault();
            
            const formData = new FormData(event.target);
            const data = {};
            formData.forEach((value, key) => data[key] = value);

            fetch('/send-email', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify(data),
            })
            .then(response => response.json())
            .then(data => {
                document.getElementById('responseMessage').textContent = data.message;
            })
            .catch(error => {
                document.getElementById('responseMessage').textContent = 'An error occurred while sending your message.';
            });
        });
    </script>
</body>
</html>
- 👋 Hi, I’m @josiahguzu
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
josiahguzu/josiahguzu is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
