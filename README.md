# MDAP-EX_01-Portfolio
## Date:12/08/25

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nithila Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- HEADER -->
    <header>
        <nav>
            <h1 class="logo">Sketchora</h1>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- HERO -->
    <section class="hero">
        <div class="hero-content">
            <h2>Hello, I'm <span>Nithila</span></h2>
            <p>Artist • Designer • Creative Mind</p>
            <a href="#portfolio" class="btn">View My Work</a>
        </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="about">
        <h2>About Me</h2>
        <p>I'm an artist passionate about creating beautiful and meaningful designs through my brand Sketchora. I love blending creativity with attention to detail.</p>
    </section>

    <!-- PORTFOLIO -->
    <section id="portfolio" class="portfolio">
        <h2>My Work</h2>
        <div class="portfolio-grid">
            <div class="card"><img src="https://via.placeholder.com/300" alt="Art 1"></div>
            <div class="card"><img src="https://via.placeholder.com/300" alt="Art 2"></div>
            <div class="card"><img src="https://via.placeholder.com/300" alt="Art 3"></div>
            <div class="card"><img src="https://via.placeholder.com/300" alt="Art 4"></div>
        </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="contact">
        <h2>Contact Me</h2>
        <form>
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" required></textarea>
            <button type="submit" class="btn">Send</button>
        </form>
    </section>

    <!-- FOOTER -->
    <footer>
        <p>© 2025 Sketchora | Designed by Nithila</p>
    </footer>

</body>
</html>
<link rel="stylesheet" href="style.css">
/* Reset default browser styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #f4f4f4;
  color: #333;
}

/* Header */
header {
  background: #333;
  color: #fff;
  padding: 20px 0;
  text-align: center;
}

header h1 {
  margin-bottom: 10px;
  font-size: 2.5rem;
}

header p {
  font-size: 1.2rem;
  color: #ccc;
}

/* Navigation */
nav {
  background: #444;
  display: flex;
  justify-content: center;
}

nav ul {
  list-style: none;
  display: flex;
}

nav ul li {
  margin: 0 15px;
}

nav ul li a {
  color: #fff;
  text-decoration: none;
  font-weight: bold;
}

nav ul li a:hover {
  color: #ff9800;
}

/* Sections */
section {
  padding: 40px;
  max-width: 900px;
  margin: auto;
  background: #fff;
  margin-top: 20px;
  border-radius: 8px;
}

section h2 {
  margin-bottom: 20px;
  color: #333;
}

section p {
  margin-bottom: 15px;
  color: #555;
}

/* Portfolio Grid */
.portfolio {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

.portfolio img {
  width: 100%;
  border-radius: 8px;
  transition: transform 0.3s ease-in-out;
}

.portfolio img:hover {
  transform: scale(1.05);
}

/* Contact Form */
form {
  display: flex;
  flex-direction: column;
}

form input, form textarea {
  margin-bottom: 15px;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

form button {
  padding: 10px;
  background: #333;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

form button:hover {
  background: #ff9800;
}

/* Footer */
footer {
  text-align: center;
  padding: 20px;
  background: #333;
  color: #fff;
  margin-top: 20px;
}

footer p {
  font-size: 0.9rem;
}

/* Responsive */
@media (max-width: 600px) {
  header h1 {
    font-size: 2rem;
  }
  nav ul {
    flex-direction: column;
  }
  nav ul li {
    margin: 10px 0;
  }
}


 style.css

 /* ===== RESET ===== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* ===== BODY ===== */
body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #f5f5f5;
  color: #333;
}

/* ===== HEADER ===== */
header {
  background: #222;
  color: #fff;
  padding: 20px 0;
  text-align: center;
}

header h1 {
  font-size: 2rem;
  margin-bottom: 10px;
}

header nav a {
  color: #fff;
  text-decoration: none;
  margin: 0 15px;
  font-weight: bold;
}

header nav a:hover {
  color: #ff9800;
}

/* ===== SECTIONS ===== */
section {
  padding: 50px 20px;
  max-width: 1100px;
  margin: auto;
}

#about, #projects, #contact {
  background: #fff;
  margin-bottom: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  padding: 30px;
}

/* ===== ABOUT ===== */
#about h2 {
  color: #ff9800;
  margin-bottom: 15px;
}

#about p {
  font-size: 1rem;
  line-height: 1.6;
}

/* ===== PROJECTS ===== */
#projects h2 {
  color: #ff9800;
  margin-bottom: 15px;
}

.project {
  background: #fafafa;
  padding: 15px;
  margin-bottom: 15px;
  border-left: 5px solid #ff9800;
  border-radius: 5px;
}

.project h3 {
  margin-bottom: 8px;
}

.project p {
  font-size: 0.95rem;
}

/* ===== CONTACT ===== */
#contact h2 {
  color: #ff9800;
  margin-bottom: 15px;
}

form label {
  display: block;
  margin: 10px 0 5px;
  font-weight: bold;
}

form input,
form textarea {
  width: 100%;
  padding: 10px;
  margin-bottom: 15px;
  border-radius: 5px;
  border: 1px solid #ccc;
}

form textarea {
  resize: vertical;
  min-height: 120px;
}

form button {
  background: #ff9800;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s ease;
}

form button:hover {
  background: #e68a00;
}

/* ===== FOOTER ===== */
footer {
  background: #222;
  color: white;
  text-align: center;
  padding: 15px;
  font-size: 0.9rem;
}


## OUTPUT
<img width="1810" height="997" alt="Screenshot 2025-08-12 105701" src="https://github.com/user-attachments/assets/caf0e415-63ac-4a52-b67b-f3a67886e5b5" />
<img width="1879" height="962" alt="Screenshot 2025-08-12 105726" src="https://github.com/user-attachments/assets/2100fcba-0657-4b05-8180-a230d6060e5a" />
<img width="1875" height="956" alt="Screenshot 2025-08-12 105752" src="https://github.com/user-attachments/assets/35b5a578-a43a-45db-bfe0-9874f644d6fb" />





## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
