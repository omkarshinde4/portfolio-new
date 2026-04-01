<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Omkar Shinde | Cybersecurity Engineer</title>

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">

<!-- AOS Animation -->
<link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet">

<style>
body {
    background: linear-gradient(135deg, #0a0a0a, #111);
    color: white;
    font-family: 'Segoe UI', sans-serif;
}

.navbar {
    background: rgba(0,0,0,0.5);
    backdrop-filter: blur(10px);
}

.hero {
    height: 100vh;
    display: flex;
    align-items: center;
    text-align: center;
}

.highlight {
    color: #00ffcc;
}

.glass {
    background: rgba(255,255,255,0.05);
    border-radius: 15px;
    padding: 20px;
    backdrop-filter: blur(10px);
    transition: 0.3s;
}

.glass:hover {
    transform: translateY(-10px);
    box-shadow: 0 0 20px #00ffcc;
}

.btn-custom {
    background: #00ffcc;
    color: black;
    border: none;
}

.section-title {
    margin-bottom: 30px;
    font-weight: bold;
}
</style>
</head>

<body>

<!-- NAVBAR -->
<nav class="navbar navbar-expand-lg navbar-dark fixed-top">
<div class="container">
<a class="navbar-brand" href="#">Omkar Shinde</a>
</div>
</nav>

<!-- HERO -->
<section class="hero">
<div class="container">
<h1>Hi, I'm <span class="highlight">Omkar Shinde</span></h1>
<h3><span id="typing"></span></h3>
<p>Building secure systems, solving real-world cyber threats.</p>

<a href="#projects" class="btn btn-custom m-2">View Work</a>
<a href="#contact" class="btn btn-outline-light m-2">Hire Me</a>
</div>
</section>

<!-- ABOUT -->
<section class="container py-5" data-aos="fade-up">
<h2 class="section-title">About Me</h2>
<div class="glass">
<p>
Cybersecurity enthusiast with strong expertise in cryptography, secure coding, and Python-based tools.
I focus on building real-world solutions that protect systems and data from evolving cyber threats.
</p>
</div>
</section>

<!-- SKILLS -->
<section class="container py-5" data-aos="fade-up">
<h2 class="section-title">Skills</h2>
<div class="row">
<div class="col-md-3"><div class="glass">Python</div></div>
<div class="col-md-3"><div class="glass">Cryptography</div></div>
<div class="col-md-3"><div class="glass">Web Dev</div></div>
<div class="col-md-3"><div class="glass">Security Tools</div></div>
</div>
</section>

<!-- PROJECTS -->
<section class="container py-5" id="projects" data-aos="fade-up">
<h2 class="section-title">Projects</h2>

<div class="row">

<div class="col-md-4">
<div class="glass">
<h4>Password Strength Checker</h4>
<p>Analyzes password security using Python.</p>
</div>
</div>

<div class="col-md-4">
<div class="glass">
<h4>Weather Web App</h4>
<p>Live weather app using API integration.</p>
</div>
</div>

<div class="col-md-4">
<div class="glass">
<h4>Encryption Tools</h4>
<p>Built Caesar Cipher & encryption programs.</p>
</div>
</div>

</div>
</section>

<!-- EXPERIENCE -->
<section class="container py-5" data-aos="fade-up">
<h2 class="section-title">Experience</h2>
<div class="glass">
<p><strong>Cyber Security Intern – Prodigy Infotech</strong></p>
<p>Worked on real-world cybersecurity challenges and built encryption tools.</p>
</div>
</section>

<!-- CONTACT -->
<section class="container py-5 text-center" id="contact" data-aos="fade-up">
<h2 class="section-title">Contact Me</h2>

<div class="glass">
<p>Email: shindeomkar6945@gmail.com</p>
<p>Phone: +91 8010419547</p>

<input type="text" class="form-control mb-2" placeholder="Your Name">
<input type="email" class="form-control mb-2" placeholder="Your Email">
<textarea class="form-control mb-2" placeholder="Your Message"></textarea>

<button class="btn btn-custom">Send Message</button>
</div>

</section>

<!-- SCRIPTS -->
<script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>
<script>
AOS.init();

// Typing Effect
const text = ["Cybersecurity Engineer", "Python Developer", "Security Analyst"];
let i = 0, j = 0, current = "", isDeleting = false;

function type() {
    current = text[i];
    
    if (!isDeleting) {
        document.getElementById("typing").textContent = current.substring(0, j++);
        if (j > current.length) {
            isDeleting = true;
            setTimeout(type, 1000);
            return;
        }
    } else {
        document.getElementById("typing").textContent = current.substring(0, j--);
        if (j === 0) {
            isDeleting = false;
            i = (i + 1) % text.length;
        }
    }
    setTimeout(type, isDeleting ? 50 : 100);
}
type();
</script>

</body>
</html>
