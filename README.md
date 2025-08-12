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

style.css
/* General Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background: #fff;
    color: #333;
}

/* Header */
header {
    background: black;
    color: gold;
    padding: 1rem 2rem;
}

header nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header .logo {
    font-size: 1.5rem;
}

header ul {
    display: flex;
    list-style: none;
}

header ul li {
    margin-left: 20px;
}

header ul li a {
    color: gold;
    text-decoration: none;
    font-weight: bold;
}

/* Hero */
.hero {
    background: url('https://via.placeholder.com/1200x500') no-repeat center center/cover;
    height: 500px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: white;
}

.hero-content h2 {
    font-size: 2.5rem;
}

.hero-content span {
    color: gold;
}

.btn {
    background: gold;
    color: black;
    padding: 10px 20px;
    display: inline-block;
    margin-top: 15px;
    text-decoration: none;
    font-weight: bold;
    border-radius: 5px;
}

/* About */
.about {
    padding: 3rem 2rem;
    text-align: center;
}

/* Portfolio */
.portfolio {
    padding: 3rem 2rem;
    text-align: center;
}

.portfolio-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 15px;
    margin-top: 20px;
}

.portfolio-grid img {
    width: 100%;
    border-radius: 10px;
}

/* Contact */
.contact {
    padding: 3rem 2rem;
    text-align: center;
}

.contact form {
    max-width: 500px;
    margin: auto;
    display: flex;
    flex-direction: column;
}

.contact input,
.contact textarea {
    margin-bottom: 15px;
    padding: 10px;
    border: 1px solid #ccc;
}

.contact button {
    border: none;
    cursor: pointer;
}

/* Footer */
footer {
    background: black;
    color: gold;
    text-align: center;
    padding: 1rem;
    margin-top: 20px;
}


## OUTPUT
<img width="1810" height="997" alt="Screenshot 2025-08-12 105701" src="https://github.com/user-attachments/assets/caf0e415-63ac-4a52-b67b-f3a67886e5b5" />
<img width="1879" height="962" alt="Screenshot 2025-08-12 105726" src="https://github.com/user-attachments/assets/2100fcba-0657-4b05-8180-a230d6060e5a" />
<img width="1875" height="956" alt="Screenshot 2025-08-12 105752" src="https://github.com/user-attachments/assets/35b5a578-a43a-45db-bfe0-9874f644d6fb" />





## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
