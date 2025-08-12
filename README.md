# MDAP-EX_01-Portfolio
## Date:

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
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio — Sketchora</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <header>
      <a class="logo" href="#">
        <div class="logo-mark">S</div>
        <div>
          <h1>Sketchora</h1>
          <div class="subtitle">Art & Illustration</div>
        </div>
      </a>

      <nav>
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#portfolio">Portfolio</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>

    <!-- HERO -->
    <div class="hero">
      <div class="hero-left card">
        <span class="eyebrow">Freelance Artist</span>
        <h2>Hello — I'm <span class="gold">Nithila</span>,<br />I sketch, paint & bring ideas to life.</h2>
        <p class="lead">I create illustrations, digital paintings and custom commissions for brands and individuals.</p>
        <div class="cta-row">
          <a class="btn btn-primary" href="#contact">Hire me</a>
          <a class="btn btn-ghost" href="#portfolio">See work</a>
        </div>
      </div>

      <div class="hero-right">
        <img src="https://images.unsplash.com/photo-1503023345310-bd7c1de61c7d" alt="art1">
      </div>
    </div>

    <!-- ABOUT -->
    <section id="about" class="card">
      <h3>About me</h3>
      <p>I'm a passionate artist who loves experimenting with color, texture and storytelling.</p>
      <div class="skills">
        <div class="skill">Digital Painting</div>
        <div class="skill">Sketching</div>
        <div class="skill">Character Design</div>
      </div>
    </section>

    <!-- PORTFOLIO -->
    <section id="portfolio">
      <h3>Selected Works</h3>
      <div class="portfolio-grid">
        <div class="proj card">
          <img src="https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e" alt="proj1">
          <div class="overlay"><div class="tag">Character</div><div>Dreamer</div></div>
        </div>
      </div>
    </section>

    <!-- SERVICES -->
    <section id="services" class="card">
      <h3>Services</h3>
      <p>Custom Portraits, Character Design, Brand Illustrations</p>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <h3>Contact</h3>
      <form>
        <label>Name</label>
        <input type="text" required>
        <label>Email</label>
        <input type="email" required>
        <label>Message</label>
        <textarea></textarea>
        <button class="btn btn-primary" type="submit">Send</button>
      </form>
    </section>

    <footer>© 2025 Sketchora • Designed by Nithila</footer>
  </div>
</body>
</html>

style.css

:root {
  --bg: #0f1724;
  --card: #0b1220;
  --muted: #94a3b8;
  --gold: #d9a441;
  --glass: rgba(255,255,255,0.04);
}

body {
  margin: 0;
  font-family: Inter, sans-serif;
  background: var(--bg);
  color: #fff;
}

.container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 28px;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  text-decoration: none;
  color: inherit;
}

.logo-mark {
  background: var(--gold);
  padding: 10px;
  border-radius: 10px;
  font-weight: 800;
  color: #000;
}

.subtitle {
  font-size: 12px;
  color: var(--muted);
}

nav ul {
  display: flex;
  gap: 18px;
  list-style: none;
  padding: 0;
  margin: 0;
}

nav a {
  color: var(--muted);
  text-decoration: none;
  font-weight: 600;
}

nav a:hover {
  color: #fff;
}

.card {
  background: var(--glass);
  padding: 18px;
  border-radius: 10px;
}

.hero {
  display: grid;
  grid-template-columns: 1fr 420px;
  gap: 28px;
  align-items: center;
  margin-top: 20px;
}

.hero-right img {
  width: 100%;
  border-radius: 10px;
}

.eyebrow {
  display: inline-block;
  font-size: 12px;
  color: var(--muted);
}

.gold {
  color: var(--gold);
}

.btn {
  padding: 12px 16px;
  border-radius: 10px;
  font-weight: 700;
  text-decoration: none;
  display: inline-block;
}

.btn-primary {
  background: var(--gold);
  color: #000;
}

.btn-ghost {
  background: transparent;
  border: 1px solid var(--muted);
  color: var(--muted);
}

.skills {
  display: flex;
  gap: 8px;
  margin-top: 10px;
}

.skill {
  background: var(--glass);
  padding: 6px 10px;
  border-radius: 999px;
}

.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 14px;
}

.proj {
  position: relative;
}

.proj img {
  width: 100%;
  border-radius: 10px;
}

.overlay {
  position: absolute;
  bottom: 0;
  padding: 10px;
  background: rgba(0,0,0,0.5);
}

.tag {
  background: var(--glass);
  padding: 4px 8px;
  border-radius: 6px;
}


## OUTPUT
<img width="1810" height="997" alt="Screenshot 2025-08-12 105701" src="https://github.com/user-attachments/assets/caf0e415-63ac-4a52-b67b-f3a67886e5b5" />
<img width="1879" height="962" alt="Screenshot 2025-08-12 105726" src="https://github.com/user-attachments/assets/2100fcba-0657-4b05-8180-a230d6060e5a" />
<img width="1875" height="956" alt="Screenshot 2025-08-12 105752" src="https://github.com/user-attachments/assets/35b5a578-a43a-45db-bfe0-9874f644d6fb" />





## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
