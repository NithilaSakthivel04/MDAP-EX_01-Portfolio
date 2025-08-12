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
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio — Sketchora</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
     :root{
      --bg:#0f1724;
      --card:#0b1220;
      --muted:#94a3b8;
      --gold:#d9a441;
      --glass: rgba(255,255,255,0.04);
      --accent: linear-gradient(135deg,#ffd57e,#ff9a48);
      color-scheme: dark;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      background: radial-gradient(1200px 600px at 10% 10%, rgba(217,164,65,0.06), transparent), var(--bg);
      color:#eef2ff;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }

   
    .container{max-width:1100px;margin:0 auto;padding:28px}
    header{display:flex;align-items:center;justify-content:space-between;padding:10px 0}

    .logo{display:flex;align-items:center;gap:12px;text-decoration:none;color:inherit}
    .logo-mark{width:46px;height:46px;border-radius:10px;background:var(--gold);display:flex;align-items:center;justify-content:center;color:#0b1220;font-weight:800;font-size:18px;box-shadow:0 6px 18px rgba(217,164,65,0.12)}
    .logo h1{margin:0;font-size:18px;letter-spacing:0.6px}
    nav ul{display:flex;gap:18px;list-style:none;margin:0;padding:0}
    nav a{color:var(--muted);text-decoration:none;font-weight:600}
    nav a:hover{color:#fff}

   
    .hero{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;margin-top:18px}
    .hero-left{padding:28px;background:linear-gradient(180deg,rgba(255,255,255,0.02),transparent);border-radius:14px;border:1px solid rgba(255,255,255,0.03)}
    .eyebrow{display:inline-block;background:var(--glass);padding:6px 10px;border-radius:999px;color:var(--muted);font-weight:600;margin-bottom:16px}
    h2{margin:0 0 12px;font-size:34px}
    p.lead{color:var(--muted);margin:0 0 18px}
    .cta-row{display:flex;gap:12px}
    .btn{padding:12px 16px;border-radius:10px;border:0;cursor:pointer;font-weight:700}
    .btn-primary{background:var(--gold);color:#08101a}
    .btn-ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted)}

    
    .carousel{position:relative;border-radius:12px;overflow:hidden;border:1px solid rgba(255,255,255,0.03)}
    .slides{display:flex;width:300%;transition:transform 0.6s ease}
    .slide{width:100%;flex:0 0 100%;display:grid;place-items:center;padding:24px;background:linear-gradient(180deg,rgba(10,10,10,0.08),transparent)}
    .slide img{width:100%;height:260px;object-fit:cover;border-radius:8px}

   
    .carousel-controls{display:flex;gap:8px;padding:12px;justify-content:center;background:rgba(0,0,0,0.2)}
    .carousel-controls label{width:10px;height:10px;border-radius:10px;background:rgba(255,255,255,0.18);display:inline-block;cursor:pointer}
    input[name="carousel"]{display:none}

    #c1:checked ~ .carousel .slides{transform:translateX(0%)}
    #c2:checked ~ .carousel .slides{transform:translateX(-100%)}
    #c3:checked ~ .carousel .slides{transform:translateX(-200%)}

    #c1:checked ~ .carousel .controls label[for="c1"],
    #c2:checked ~ .carousel .controls label[for="c2"],
    #c3:checked ~ .carousel .controls label[for="c3"]{
      background:var(--gold);
      box-shadow:0 6px 14px rgba(217,164,65,0.18);
    }

  
    section{margin-top:34px}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent); border-radius:12px; padding:18px; border:1px solid rgba(255,255,255,0.03)}

    .about{display:grid;grid-template-columns:1fr 320px;gap:18px;align-items:start}
    .skills{display:flex;flex-wrap:wrap;gap:8px;margin-top:12px}
    .skill{background:rgba(255,255,255,0.03);padding:8px 10px;border-radius:999px;color:var(--muted);font-weight:600}

    .portfolio-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-top:14px}
    .proj{position:relative;border-radius:10px;overflow:hidden}
    .proj img{width:100%;height:180px;object-fit:cover;display:block;transition:transform .4s}
    .proj:hover img{transform:scale(1.06)}
    .proj .overlay{position:absolute;inset:0;background:linear-gradient(180deg,transparent,rgba(0,0,0,0.6));display:flex;flex-direction:column;justify-content:flex-end;padding:12px;color:#fff}
    .tag{background:rgba(255,255,255,0.06);padding:6px 8px;border-radius:8px;font-weight:700;font-size:13px}

  
    .contact-grid{display:grid;grid-template-columns:1fr 360px;gap:16px}
    form label{display:block;font-weight:600;margin-bottom:6px}
    input[type=text],input[type=email],textarea{width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit}
    textarea{min-height:140px}

    footer{margin-top:28px;padding:18px 0;color:var(--muted);font-size:14px;text-align:center}

  
    @media (max-width:980px){
      .hero{grid-template-columns:1fr;}
      .about{grid-template-columns:1fr}
      .portfolio-grid{grid-template-columns:repeat(2,1fr)}
      .contact-grid{grid-template-columns:1fr}
    }
    @media (max-width:560px){
      h2{font-size:26px}
      .logo h1{font-size:16px}
      .portfolio-grid{grid-template-columns:1fr}
      .hero-left{padding:18px}
      .hero-right{order:-1}
    }

  </style>
</head>
<body>
  <div class="container">
    <header>
      <a class="logo" href="#">
        <div class="logo-mark">S</div>
        <div>
          <h1>Sketchora</h1>
          <div style="font-size:12px;color:var(--muted);margin-top:2px">Art & Illustration</div>
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
        <h2>Hello — I'm <span style="color:var(--gold)">Nithila</span>,
        <br />I sketch, paint & bring ideas to life.</h2>
        <p class="lead">I create illustrations, digital paintings and custom commissions for brands and individuals. Scroll down to see selected works and get in touch for commissions or collaborations.</p>

        <div class="cta-row">
          <a class="btn btn-primary" href="#contact">Hire me</a>
          <a class="btn btn-ghost" href="#portfolio">See work</a>
        </div>

        <div style="margin-top:18px;color:var(--muted);font-size:13px">Featured on: <strong style="color:#fff">Instagram</strong> &middot; YouTube</div>
      </div>

      
      <div class="hero-right">
        <input type="radio" id="c1" name="carousel" checked>
        <input type="radio" id="c2" name="carousel">
        <input type="radio" id="c3" name="carousel">

        <div class="carousel card">
          <div class="slides">
            <div class="slide"><img src="https://images.unsplash.com/photo-1503023345310-bd7c1de61c7d?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=4e3fd3a8e3a0b1bca2b6a8e6e8f1a0c2" alt="art1"></div>
            <div class="slide"><img src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=64b3f2d4c7b8be2e8395e9f3e0b7a1a5" alt="art2"></div>
            <div class="slide"><img src="https://images.unsplash.com/photo-1504198453319-5ce911bafcde?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=3c4d2b9e5e9a2a4f6b1b0c7d9e8f6a4d" alt="art3"></div>
          </div>
          <div class="controls carousel-controls">
            <label for="c1"></label>
            <label for="c2"></label>
            <label for="c3"></label>
          </div>
        </div>
      </div>
    </div>

   
    <section id="about" class="card about">
      <div>
        <h3 style="margin-top:0">About me</h3>
        <p style="color:var(--muted)">I'm a passionate artist who loves experimenting with color, texture and storytelling. I focus on character art, portraits and commercial illustrations — working digitally and with traditional media.
        </p>

        <div class="skills">
          <div class="skill">Digital Painting</div>
          <div class="skill">Sketching</div>
          <div class="skill">Character Design</div>
          <div class="skill">Commissions</div>
          <div class="skill">Brand Illustration</div>
        </div>

        <h4 style="margin-top:18px">Experience</h4>
        <ul style="color:var(--muted);margin-top:8px">
          <li>Commissioned portraits and illustrations for private clients</li>
          <li>Social media art & short tutorials on YouTube</li>
          <li>Packaging and small scale branding projects</li>
        </ul>
      </div>

      <div style="display:flex;flex-direction:column;gap:12px">
        <div class="card" style="padding:12px;border-radius:10px;text-align:center">
          <div style="font-size:12px;color:var(--muted)">Available for</div>
          <div style="font-size:20px;font-weight:800;margin-top:6px">Commissions & Collaborations</div>
          <a class="btn btn-primary" href="#contact" style="margin-top:10px">Book a slot</a>
        </div>

        <div class="card" style="padding:12px;border-radius:10px;text-align:center">
          <div style="font-size:12px;color:var(--muted)">Contact</div>
          <div style="font-weight:700;margin-top:6px">@sketchora.official</div>
          <div style="color:var(--muted);font-size:13px;margin-top:6px">Email: hello@sketchora.example</div>
        </div>
      </div>
    </section>

    
    <section id="portfolio">
      <h3>Selected Works</h3>
      <div class="portfolio-grid">
        <div class="proj card">
          <img src="https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=6e8b9b1a2b3c4d5e6f7a8b9c0d1e2f3a" alt="proj1">
          <div class="overlay"><div class="tag">Character</div><div style="font-weight:700;margin-top:6px">Dreamer — Digital</div></div>
        </div>
        <div class="proj card">
          <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=2a7b8c9d0e1f2a3b4c5d6e7f8g9h0i1j" alt="proj2">
          <div class="overlay"><div class="tag">Portrait</div><div style="font-weight:700;margin-top:6px">Golden Hour</div></div>
        </div>
        <div class="proj card">
          <img src="https://images.unsplash.com/photo-1500917293891-ef795e70e1f6?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=abcd1234efgh5678ijkl9012mnop3456" alt="proj3">
          <div class="overlay"><div class="tag">Illustration</div><div style="font-weight:700;margin-top:6px">City Stories</div></div>
        </div>

        <div class="proj card">
          <img src="https://images.unsplash.com/photo-1513883049090-d0b7439799bf?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=1234abcd5678efgh9012ijkl3456mnop" alt="proj4">
          <div class="overlay"><div class="tag">Sketch</div><div style="font-weight:700;margin-top:6px">Morning Lines</div></div>
        </div>
        <div class="proj card">
          <img src="https://images.unsplash.com/photo-1503264116251-35a269479413?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=99887766554433221100aabbccddeeff" alt="proj5">
          <div class="overlay"><div class="tag">Concept</div><div style="font-weight:700;margin-top:6px">Wild Garden</div></div>
        </div>
        <div class="proj card">
          <img src="https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6" alt="proj6">
          <div class="overlay"><div class="tag">Brand</div><div style="font-weight:700;margin-top:6px">Cozy Co. Icons</div></div>
        </div>

      </div>
    </section>

  
    <section id="services" class="card">
      <h3 style="margin-top:0">Services</h3>
      <div style="display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-top:12px">
        <div style="padding:12px;border-radius:10px;background:rgba(255,255,255,0.02)"><strong>Custom Portraits</strong><p style="color:var(--muted)">Digital or traditional portraits made to order.</p></div>
        <div style="padding:12px;border-radius:10px;background:rgba(255,255,255,0.02)"><strong>Character Design</strong><p style="color:var(--muted)">Characters for games, books and animation.</p></div>
        <div style="padding:12px;border-radius:10px;background:rgba(255,255,255,0.02)"><strong>Brand Illustrations</strong><p style="color:var(--muted)">Illustrations for packaging & social media.</p></div>
      </div>
    </section>

  
    <section id="contact">
      <h3>Contact</h3>
      <div class="contact-grid">
        <div class="card">
          <form action="#" onsubmit="return false;">
            <label for="name">Name</label>
            <input id="name" type="text" placeholder="Your name" required>

            <label for="email" style="margin-top:10px">Email</label>
            <input id="email" type="email" placeholder="you@example.com" required>

            <label for="message" style="margin-top:10px">Message</label>
            <textarea id="message" placeholder="Tell me about the project or request"></textarea>

            <div style="margin-top:12px;display:flex;gap:8px">
              <button class="btn btn-primary" type="submit">Send message</button>
              <button class="btn btn-ghost" type="reset">Reset</button>
            </div>
          </form>
        </div>

        <div class="card" style="padding:18px">
          <h4 style="margin-top:0">Let's talk</h4>
          <p style="color:var(--muted)">For commissions, collaborations or inquiries — DM on Instagram or email me at <strong>hello@sketchora.example</strong></p>

          <div style="margin-top:12px;display:flex;gap:10px">
            <a class="tag" href="#">Instagram</a>
            <a class="tag" href="#">YouTube</a>
            <a class="tag" href="#">Behance</a>
          </div>

        </div>
      </div>
    </section>

    <footer>
      © 2025 Sketchora • Designed by Nithila • Built with ❤️
    </footer>

  </div>
</body>
</html>

## OUTPUT
<img width="1810" height="997" alt="Screenshot 2025-08-12 105701" src="https://github.com/user-attachments/assets/caf0e415-63ac-4a52-b67b-f3a67886e5b5" />
<img width="1879" height="962" alt="Screenshot 2025-08-12 105726" src="https://github.com/user-attachments/assets/2100fcba-0657-4b05-8180-a230d6060e5a" />
<img width="1875" height="956" alt="Screenshot 2025-08-12 105752" src="https://github.com/user-attachments/assets/35b5a578-a43a-45db-bfe0-9874f644d6fb" />





## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
