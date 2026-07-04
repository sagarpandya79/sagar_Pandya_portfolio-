# sagar_Pandya_portfolio-
my portfolio

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sagar Pandya | Premium Portfolio</title>
    
    <!-- Google Fonts for Premium Typography -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* CSS Variables for Theme */
        :root {
            --bg-color: #050814;
            --primary-color: #00f2fe;
            --secondary-color: #4facfe;
            --text-main: #ffffff;
            --text-muted: #94a3b8;
            --glass-bg: rgba(255, 255, 255, 0.03);
            --glass-border: rgba(255, 255, 255, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            overflow-x: hidden;
            background-image: radial-gradient(circle at 15% 50%, rgba(79, 172, 254, 0.1), transparent 25%),
                              radial-gradient(circle at 85% 30%, rgba(0, 242, 254, 0.1), transparent 25%);
        }

        /* Glassmorphism Utility */
        .glass-panel {
            background: var(--glass-bg);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid var(--glass-border);
            border-radius: 16px;
        }

        /* Navigation */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 5%;
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(5, 8, 20, 0.8);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--glass-border);
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Hero Section */
        .hero {
            display: flex;
            align-items: center;
            justify-content: space-between;
            min-height: 80vh;
            padding: 0 5%;
            gap: 40px;
        }

        .hero-content {
            flex: 1;
            animation: slideInLeft 1s ease forwards;
        }

        .hero-content h2 {
            font-size: 1.2rem;
            color: var(--primary-color);
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 20px;
        }

        .hero-content p {
            color: var(--text-muted);
            font-size: 1.1rem;
            margin-bottom: 30px;
            max-width: 600px;
        }

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
            animation: fadeIn 1.5s ease forwards;
        }

        .hero-image img {
            width: 320px;
            height: 320px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid transparent;
            background: linear-gradient(var(--bg-color), var(--bg-color)) padding-box, 
                        linear-gradient(to right, var(--primary-color), var(--secondary-color)) border-box;
            box-shadow: 0 0 30px rgba(0, 242, 254, 0.3);
            transition: transform 0.3s ease;
        }

        .hero-image img:hover {
            transform: scale(1.05);
        }

        /* Section Settings */
        .section-container {
            padding: 80px 5%;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 50px;
            position: relative;
        }

        .section-title::after {
            content: '';
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }

        /* Skills Section */
        .skills-wrapper {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }

        .skill-btn {
            padding: 12px 24px;
            font-size: 1rem;
            font-weight: 600;
            color: var(--text-main);
            border-radius: 30px;
            cursor: default;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .skill-btn:hover {
            transform: translateY(-5px);
            border-color: var(--primary-color);
            box-shadow: 0 0 20px rgba(0, 242, 254, 0.4);
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .project-card {
            padding: 30px;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(135deg, rgba(0,242,254,0.1), rgba(79,172,254,0.05));
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: rgba(0, 242, 254, 0.4);
            box-shadow: 0 10px 30px rgba(0, 242, 254, 0.15);
        }

        .project-card:hover::before {
            opacity: 1;
        }

        .project-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary-color);
            position: relative;
        }

        .project-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            position: relative;
        }

        /* Channels/Links Section */
        .channels-wrapper {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: #000;
            text-decoration: none;
            font-weight: 700;
            border-radius: 30px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: none;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 242, 254, 0.3);
        }
        
        .btn-outline {
            background: transparent;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
        }
        
        .btn-outline:hover {
            background: rgba(0, 242, 254, 0.1);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 30px;
            border-top: 1px solid var(--glass-border);
            color: var(--text-muted);
            margin-top: 50px;
        }

        /* Animations */
        @keyframes slideInLeft {
            from { opacity: 0; transform: translateX(-50px); }
            to { opacity: 1; transform: translateX(0); }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.9); }
            to { opacity: 1; transform: scale(1); }
        }

        /* Mobile Responsiveness */
        @media (max-width: 768px) {
            .hero {
                flex-direction: column-reverse;
                text-align: center;
                padding-top: 40px;
            }
            .hero-content h1 {
                font-size: 2.5rem;
            }
            .hero-image img {
                width: 250px;
                height: 250px;
            }
            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <!-- Navigation -->
    <nav>
        <div class="logo">SP</div>
        <a href="#contact" class="btn">Connect</a>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h2>Hello, I'm</h2>
            <h1>Sagar Pandya</h1>
            <p>A passionate Web Developer & Content Creator. Main hamesha nayi technologies sikhne aur unse badiya projects banane ke liye taiyar rehta hoon. Turning ideas into interactive reality.</p>
            <div style="display: flex; gap: 15px; margin-top: 20px;">
                <a href="#projects" class="btn">View Projects</a>
                <a href="#channels" class="btn btn-outline">My Channels</a>
            </div>
        </div>
        <div class="hero-image">
            <!-- Ensure your image is named 'sagar-pandya.jpg' in the same folder -->
            <img src="/sagarpandya.png" alt="Sagar Pandya">
        </div>
    </section>

    <!-- Skills Section -->
    <section class="section-container" id="skills">
        <h2 class="section-title">My Tech Stack</h2>
        <div class="skills-wrapper">
            <div class="glass-panel skill-btn">HTML5 & CSS3</div>
            <div class="glass-panel skill-btn">JavaScript</div>
            <div class="glass-panel skill-btn">PHP</div>
            <div class="glass-panel skill-btn">MySQL</div>
            <div class="glass-panel skill-btn">ASP.NET</div>
            <div class="glass-panel skill-btn">UI/UX Design</div>
            <div class="glass-panel skill-btn">Video Editing</div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="section-container" id="projects">
        <h2 class="section-title">Featured Projects</h2>
        <div class="projects-grid">
            <div class="glass-panel project-card">
                <h3>Applix (Apple Store)</h3>
                <p>PHP aur MySQL par adharit ek premium e-commerce UI/UX store project jise maine college development ke liye build kiya hai.</p>
            </div>
            <div class="glass-panel project-card">
                <h3>Security Utility Tool</h3>
                <p>Digital security aur robust logic ko dhyan mein rakhte hue banaya gaya ek Advanced Password Generator & Strength Checker.</p>
            </div>
        </div>
    </section>

    <!-- Channels Section -->
    <section class="section-container" id="channels">
        <h2 class="section-title">Content Creation</h2>
        <p style="text-align: center; color: var(--text-muted); margin-bottom: 30px;">Aap mere tech content aur development updates ko yahan follow kar sakte hain:</p>
        <div class="channels-wrapper">
            <a href="https://youtube.com/@sagarpulsecoding?si=FAzatZ8guZDYYHoM" target="_blank" class="glass-panel btn btn-outline">▶ SagarCodePulse</a>
            <a href="https://youtube.com/@sagarsurgegaming?si=bKskagxfB5W-HVEX" target="_blank" class="glass-panel btn btn-outline">▶ SagarSurge</a>
            <a href="https://github.com/sagarpandya79/" target="_blank" class="glass-panel btn btn-outline">🐙 GitHub</a>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <p>&copy; 2026 Sagar Pandya. Designed with passion.</p>
    </footer>

</body>
</html>
 
