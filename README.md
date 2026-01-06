# tedd-portfolio
portfolio




<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Teddy Kavoi - CS Student (UoPeople) & Software Engineering Student (PLP)</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            line-height: 1.6; 
            color: #333; 
        }
        .container { 
            max-width: 1200px; 
            margin: 0 auto; 
            padding: 0 20px; 
        }
        header { 
            background: #0a2540; 
            color: white; 
            padding: 1rem 0; 
            position: fixed; 
            width: 100%; 
            top: 0; 
            z-index: 1000; 
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        nav ul { 
            list-style: none; 
            display: flex; 
            justify-content: center; 
        }
        nav li { margin: 0 1.5rem; }
        nav a { 
            color: white; 
            text-decoration: none; 
            font-weight: 600; 
            transition: color 0.3s;
        }
        nav a:hover { color: #ff6b6b; }
        .hero { 
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); 
            color: white; 
            padding: 140px 0 80px; 
            text-align: center; 
        }
        .hero h1 { 
            font-size: 3.5rem; 
            margin-bottom: 1rem; 
            font-weight: 700;
        }
        .hero p { 
            font-size: 1.25rem; 
            margin-bottom: 2.5rem; 
            max-width: 700px; 
            margin-left: auto; 
            margin-right: auto;
            line-height: 1.7;
        }
        .btn { 
            background: #ff6b6b; 
            color: white; 
            padding: 15px 35px; 
            text-decoration: none; 
            border-radius: 50px; 
            font-weight: 600; 
            display: inline-block; 
            margin: 0 15px; 
            transition: all 0.3s;
        }
        .btn:hover { 
            background: #ff5252; 
            transform: translateY(-2px);
        }
        section { padding: 90px 0; }
        h2 { 
            text-align: center; 
            font-size: 2.8rem; 
            margin-bottom: 3.5rem; 
            color: #0a2540;
            position: relative;
        }
        h2::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: #ff6b6b;
            margin: 20px auto;
        }
        .about { background: #f8f9fa; }
        .about-content { 
            max-width: 900px; 
            margin: 0 auto; 
            text-align: center; 
        }
        .about-content p {
            font-size: 1.15rem;
            margin-bottom: 1.5rem;
        }
        .skills-grid { 
            display: grid; 
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); 
            gap: 2.5rem; 
            margin-top: 3rem; 
        }
        .skill { 
            text-align: center; 
            padding: 2rem; 
            background: white; 
            border-radius: 20px; 
            box-shadow: 0 10px 30px rgba(0,0,0,0.1); 
            transition: all 0.3s;
        }
        .skill:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }
        .skill h3 {
            color: #0a2540;
            margin-bottom: 1rem;
            font-size: 1.4rem;
        }
        .projects { background: #f8f9fa; }
        .project-grid { 
            display: grid; 
            grid-template-columns: repeat(auto-fit, minmax(380px, 1fr)); 
            gap: 2.5rem; 
        }
        .project { 
            background: white; 
            border-radius: 20px; 
            overflow: hidden; 
            box-shadow: 0 15px 35px rgba(0,0,0,0.1); 
            transition: all 0.4s; 
        }
        .project:hover { 
            transform: translateY(-15px); 
            box-shadow: 0 25px 50px rgba(0,0,0,0.2);
        }
        .project img { 
            width: 100%; 
            height: 220px; 
            object-fit: cover; 
        }
        .project-content { 
            padding: 2rem; 
        }
        .project h3 { 
            margin-bottom: 1rem; 
            color: #0a2540; 
            font-size: 1.4rem;
        }
        .tech { 
            background: #e3f2fd; 
            padding: 8px 15px; 
            border-radius: 25px; 
            font-size: 0.85rem; 
            margin-right: 10px; 
            margin-bottom: 10px;
            display: inline-block;
        }
        .project-links {
            margin-top: 1.5rem;
        }
        .project-links a {
            color: #667eea;
            text-decoration: none;
            font-weight: 600;
            margin-right: 1rem;
        }
        .project-links a:hover {
            color: #764ba2;
        }
        .contact-section {
            text-align: center;
        }
        .contact-section p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 3rem;
        }
        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 800px;
            margin: 0 auto;
        }
        .contact-item {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        .contact-item:hover {
            transform: translateY(-5px);
        }
        footer { 
            background: #0a2540; 
            color: white; 
            text-align: center; 
            padding: 3rem 0; 
        }
        @media (max-width: 768px) { 
            .hero h1 { font-size: 2.5rem; } 
            nav ul { 
                flex-direction: column; 
                gap: 1rem;
                padding: 1rem 0;
            }
            nav li { margin: 0; }
            .hero { padding: 120px 0 60px; }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="container">
            <h1>Teddy Kavoi</h1>
            <p>Current <strong>Computer Science Student at University of the People (UoPeople)</strong> | <strong>Software Engineering Student at PLP (Kenya)</strong><br>Aspiring full-stack developer specializing in web apps, trading bots, and remote freelance work. Expected graduation: 2027</p>
            <a href="#projects" class="btn">View My Projects</a>
            <a href="#contact" class="btn">Get In Touch</a>
        </div>
    </section>

    <section id="about" class="about">
        <div class="container">
            <h2>About Me</h2>
            <div class="about-content">
                <p>I'm <strong>Teddy Kavoi</strong>, currently pursuing a <strong>Computer Science degree at University of the People (UoPeople)</strong> (expected graduation 2027) while undergoing intensive <strong>Software Engineering training at PLP</strong>, a leading tech school in Kenya.</p>
                <p>Based in Nairobi, my focus is building practical web applications, cryptocurrency trading automation tools, and integrating design with development. Skills developed through UoPeople coursework and PLP hands-on training include React, Python, modern GitHub workflows, and API integrations (Binance, TradingView).</p>
                <p>Actively freelancing on Fiverr and Upwork while developing this portfolio for junior developer roles and remote opportunities.</p>
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <h2>Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill">
                    <h3>Frontend Development</h3>
                    <p>JavaScript (React), HTML5, CSS3, Tailwind CSS, VS Code</p>
                </div>
                <div class="skill">
                    <h3>Backend & Tools</h3>
                    <p>Python, Node.js, Express, Git/GitHub, REST APIs (Binance, TradingView)</p>
                </div>
                <div class="skill">
                    <h3>Design Tools</h3>
                    <p>Adobe Illustrator, Figma, Canva, Premiere Pro</p>
                </div>
                <div class="skill">
                    <h3>Trading & Finance</h3>
                    <p>Technical Analysis, Trading Bots, MetaMask, Exness, Pandas</p>
                </div>
            </div>
        </div>
    </section>

    <section id="projects" class="projects">
        <div class="container">
            <h2>Featured Projects</h2>
            <div class="project-grid">
                <div class="project">
                    <img src="https://via.placeholder.com/400x220/667eea/ffffff?text=Portfolio+Site" alt="Personal Portfolio">
                    <div class="project-content">
                        <h3>Personal Portfolio Website</h3>
                        <p>Modern, responsive portfolio showcasing UoPeople & PLP training projects with smooth animations and mobile-first design.</p>
                        <p><strong>Tech Stack:</strong> <span class="tech">HTML5</span><span class="tech">CSS3</span><span class="tech">JavaScript</span></p>
                        <div class="project-links">
                            <a href="https://github.com/teddykavoi/portfolio" target="_blank">GitHub</a> | 
                            <a href="#" target="_blank">Live Demo</a>
                        </div>
                    </div>
                </div>
                <div class="project">
                    <img src="https://via.placeholder.com/400x220/764ba2/ffffff?text=Trading+Bot" alt="Trading Bot">
                    <div class="project-content">
                        <h3>Crypto Trading Bot</h3>
                        <p>Python automation bot for cryptocurrency trading analysis using TradingView APIs. Backtested strategies showing 25% simulated returns. Developed during PLP modules.</p>
                        <p><strong>Tech Stack:</strong> <span class="tech">Python</span><span class="tech">APIs</span><span class="tech">Pandas</span></p>
                        <div class="project-links">
                            <a href="https://github.com/teddykavoi/trading-bot" target="_blank">GitHub</a>
                        </div>
                    </div>
                </div>
                <div class="project">
                    <img src="https://via.placeholder.com/400x220/ff6b6b/ffffff?text=React+Dashboard" alt="React Dashboard">
                    <div class="project-content">
                        <h3>React Trading Dashboard</h3>
                        <p>Real-time cryptocurrency dashboard from UoPeople CS coursework. Live Binance API data visualization with interactive Chart.js charts.</p>
                        <p><strong>Tech Stack:</strong> <span class="tech">React</span><span class="tech">Chart.js</span><span class="tech">Binance API</span></p>
                        <div class="project-links">
                            <a href="https://github.com/teddykavoi/react-dashboard" target="_blank">GitHub</a> | 
                            <a href="#" target="_blank">Live Demo</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <h2>Let's Connect</h2>
            <div class="contact-section">
                <p><strong>Teddy Kavoi</strong> | CS Student at UoPeople (Class of 2027) | Software Engineering at PLP (Kenya)<br>Open to junior developer roles, freelance web projects, and remote opportunities.</p>
                
                <div class="contact-info">
                    <div class="contact-item">
                        <p><strong>📧 Email</strong><br>tkavoi6@gmail.com.com</p>
                    </div>
                    <div class="contact-item">
                        <p><strong>💼 LinkedIn</strong><br><a href="https://linkedin.com/in/teddykavoi" target="_blank">linkedin.com/in/teddykavoi</a></p>
                    </div>
                    <div class="contact-item">
                        <p><strong>🐙 GitHub</strong><br><a href="https://github.com/teddykavoi" target="_blank">github.com/teddykavoi</a></p>
                    </div>
                    <div class="contact-item">
                        <p><strong>📍 Location</strong><br>Nairobi, Kenya<br><em>(Remote OK)</em></p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2026 Teddy Kavoi. <strong>Computer Science Student at University of the People (UoPeople, Class of 2027)</strong> | <strong>Software Engineering Student at PLP, Kenya</strong>.<br>Building the future, one line of code at a time. 🚀</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ 
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add scroll effect to header
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(10, 37, 64, 0.95)';
                header.style.backdropFilter = 'blur(10px)';
            } else {
                header.style.background = '#0a2540';
                header.style.backdropFilter = 'none';
            }
        });
    </script>
</body>
</html>
