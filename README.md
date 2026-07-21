# Chidera-O
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Advanced GitHub Website</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>My Advanced GitHub Website</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#features">Features</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section id="home">
    <h2>Welcome</h2>
    <p>This is a modern, responsive website hosted on GitHub Pages.</p>
  </section>

  <section id="features">
    <h2>Features</h2>
    <div class="card">
      <h3>Responsive Design</h3>
      <p>Looks great on desktop, tablet, and mobile.</p>
    </div>
    <div class="card">
      <h3>Interactive Elements</h3>
      <p>Buttons, forms, and animations powered by JavaScript.</p>
    </div>
    <div class="card">
      <h3>Custom Styling</h3>
      <p>Modern layout with CSS grid and flexbox.</p>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Me</h2>
    <form id="contactForm">
      <label for="name">Name:</label>
      <input type="text" id="name" required>

      <label for="email">Email:</label>
      <input type="email" id="email" required>

      <label for="message">Message:</label>
      <textarea id="message" required></textarea>

      <button type="submit">Send</button>
    </form>
    <p id="formResponse"></p>
  </section>

  <footer>
    <p>&copy; 2026 My Advanced GitHub Website</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
body {
  font-family: 'Segoe UI', sans-serif;
  margin: 0;
  padding: 0;
  background: #f9f9f9;
  color: #333;
}

header {
  background: #222;
  color: #fff;
  padding: 1rem;
}

header h1 {
  margin: 0;
}

nav ul {
  list-style: none;
  padding: 0;
  display: flex;
  gap: 1rem;
}

nav ul li a {
  color: #fff;
  text-decoration: none;
}

section {
  padding: 2rem;
}

.card {
  background: #fff;
  padding: 1rem;
  margin: 1rem 0;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

form {
  display: flex;
  flex-direction: column;
  max-width: 400px;
}

form label {
  margin-top: 10px;
}

form input, form textarea {
  padding: 8px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

form button {
  margin-top: 15px;
  padding: 10px;
  background: #222;
  color: #fff;
  border: none;
  cursor: pointer;
}

form button:hover {
  background: #444;
}

footer {
  background: #222;
  color: #fff;
  text-align: center;
  padding: 1rem;
}
// Handle form submission
document.getElementById("contactForm").addEventListener("submit", function(event) {
  event.preventDefault();

  const name = document.getElementById("name").value;
  const email = document.getElementById("email").value;
  const message = document.getElementById("message").value;

  // For demo purposes, just show a response message
  document.getElementById("formResponse").textContent =
    `Thank you, ${name}! Your message has been received.`;

  // Clear form
  this.reset();
});
