<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Portfolio of [Ashok Saini], a creative graphic designer specializing in branding and illustration.">
    <title>[Your Name] - Graphic Designer Portfolio</title>
    <style>
        body { font-family: 'Arial', sans-serif; margin: 0; padding: 0; color: #333; background: linear-gradient(135deg, #f4f4f4 0%, #e0e0e0 100%); line-height: 1.6; }
        header { background: #000; color: #fff; padding: 20px; text-align: center; position: sticky; top: 0; z-index: 100; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        header h1 { margin: 0; font-size: 2em; }
        nav { margin-top: 10px; }
        nav a { color: #fff; margin: 0 15px; text-decoration: none; transition: color 0.3s; }
        nav a:hover { color: #00bfff; }
        .hero { background: url('https://via.placeholder.com/1920x600?text=Hero+Background') no-repeat center/cover; padding: 100px 20px; text-align: center; color: #fff; position: relative; }
        .hero::before { content: ''; position: absolute; top: 0; left: 0; right: 0; bottom: 0; background: rgba(0,0,0,0.5); }
        .hero h1, .hero p { position: relative; z-index: 1; }
        .hero h1 { font-size: 3em; margin-bottom: 10px; }
        .hero p { font-size: 1.3em; }
        .section { padding: 60px 20px; max-width: 1200px; margin: 0 auto; }
        .about { background: #fff; border-radius: 8px; padding: 40px; margin: 20px 0; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }
        .portfolio { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        .portfolio img { width: 100%; height: 200px; object-fit: cover; border-radius: 8px; cursor: pointer; transition: transform 0.3s; box-shadow: 0 4px 8px rgba(0,0,0,0.1); }
        .portfolio img:hover { transform: scale(1.05); }
        .lightbox { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.8); justify-content: center; align-items: center; z-index: 1000; }
        .lightbox img { max-width: 90%; max-height: 90%; }
        .contact { background: #000; color: #fff; text-align: center; border-radius: 8px; padding: 40px; margin: 20px 0; }
        form { max-width: 500px; margin: 0 auto; }
        input, textarea { width: 100%; padding: 12px; margin: 10px 0; border: none; border-radius: 4px; font-size: 1em; }
        button { background: #00bfff; color: #fff; padding: 12px 24px; border: none; border-radius: 4px; cursor: pointer; font-size: 1em; transition: background 0.3s; }
        button:hover { background: #0099cc; }
        footer { background: #333; color: #fff; text-align: center; padding: 20px; }
        @media (max-width: 768px) { .hero h1 { font-size: 2em; } .portfolio { grid-template-columns: 1fr; } }
    </style>
</head>
<body>
    <header>
        <h1>[Your Name]</h1>
        <nav>
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#portfolio">Portfolio</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>
    
    <section id="home" class="hero">
        <h1>Welcome to My Portfolio</h1>
        <p>Creative Graphic Designer | Transforming Ideas into Visual Masterpieces</p>
        <a href="#portfolio"><button>Explore My Work</button></a>
    </section>
    
    <section id="about" class="section about">
        <h2>About Me</h2>
        <p>Hi, I'm [Your Name], a passionate graphic designer with [X] years of experience in branding, digital illustration, and UI/UX design. I love crafting visuals that resonate and inspire. My work has been featured in [mention any awards or clients if applicable].</p>
        <ul>
            <li><strong>Skills:</strong> Adobe Creative Suite (Photoshop, Illustrator, InDesign), Figma, Branding, Illustration</li>
            <li><strong>Experience:</strong> [Briefly list key projects, e.g., "Designed logos for 50+ clients" or "Illustrated for major publications"]</li>
        </ul>
    </section>
    
    <section id="portfolio" class="section">
        <h2>My Portfolio</h2>
        <div class="portfolio">
            <img src="https://via.placeholder.com/400x300?text=Branding+Design" alt="Branding Design" onclick="openLightbox(this.src)">
            <img src="https://via.placeholder.com/400x300?text=Illustration" alt="Illustration" onclick="openLightbox(this.src)">
            <img src="https://via.placeholder.com/400x300?text=UI+Design" alt="UI Design" onclick="openLightbox(this.src)">
            <img src="https://via.placeholder.com/400x300?text=Poster+Design" alt="Poster Design" onclick="openLightbox(this.src)">
            <!-- Replace these with your actual image URLs (e.g., from Imgur or your server) -->
        </div>
        <div id="lightbox" class="lightbox" onclick="closeLightbox()">
            <img id="lightbox-img" src="">
        </div>
    </section>
    
    <section id="contact" class="section contact">
        <h2>Contact Me</h2>
        <form id="contact-form">
            <input type="text" name="name" placeholder="Your Name" required>
            <input type="email" name="email" placeholder="Your Email" required>
            <textarea name="message" placeholder="Your Message" rows="5" required></textarea>
            <button type="submit">Send Message</button>
        </form>
        <p>Follow me: <a href="[Your Instagram URL]" style="color: #00bfff;">Instagram</a> | <a href="[Your LinkedIn URL]" style="color: #00bfff;">LinkedIn</a> | <a href="[Your Behance URL]" style="color: #00bfff;">Behance</a></p>
    </section>
    
    <footer>
        <p>&copy; 2023 [Your Name]. All rights reserved. | Built with passion.</p>
    </footer>

    <script>
        function openLightbox(src) {
            document.getElementById('lightbox-img').src = src;
            document.getElementById('lightbox').style.display = 'flex';
        }
        function closeLightbox() {
            document.getElementById('lightbox').style.display = 'none';
        }
        document.getElementById('contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you! Your message has been sent (demo only—integrate with a service like Formspree for real submissions).');
        });
    </script>
</body>
</html>
