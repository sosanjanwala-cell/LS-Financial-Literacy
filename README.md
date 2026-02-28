[index.html](https://github.com/user-attachments/files/25618472/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LS FinLit - Empowering Kids to Be Money Smart</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            line-height: 1.6;
            color: #1a1a1a;
            background: #fafafa;
        }

        /* Navigation */
        .navbar {
            background: rgba(45, 80, 22, 0.95);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(255, 215, 0, 0.1);
            padding: 1.2rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 8px 32px rgba(45, 80, 22, 0.12);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            font-weight: 700;
            color: white;
            text-decoration: none;
            letter-spacing: -0.5px;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2.5rem;
            align-items: center;
        }

        .nav-menu a {
            color: rgba(255, 255, 255, 0.9);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-menu a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: #ffd700;
            transition: width 0.3s ease;
        }

        .nav-menu a:hover { color: #ffd700; }
        .nav-menu a:hover::after { width: 100%; }

        .contact-btn {
            background: linear-gradient(135deg, #ffd700 0%, #ffed4e 100%);
            color: #2d5016 !important;
            padding: 0.7rem 1.8rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            box-shadow: 0 4px 15px rgba(255,215,0,0.3);
            transition: all 0.3s ease;
        }

        .contact-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(255,215,0,0.4);
        }

        .contact-btn::after { display: none !important; }

        /* Hero */
        .hero {
            background: linear-gradient(135deg, #2d5016 0%, #4a7c59 50%, #2d5016 100%);
            color: white;
            padding: 6rem 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 200"><path d="M0,100 C150,200 350,0 500,100 C650,200 850,0 1000,100 L1000,200 L0,200 Z" fill="rgba(255,215,0,0.1)"/></svg>');
            background-size: cover;
            opacity: 0.3;
        }

        .hero-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            position: relative;
            z-index: 1;
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
            line-height: 1.2;
            letter-spacing: -1px;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 2.5rem;
            opacity: 0.95;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            animation: fadeInUp 1s ease 0.2s both;
        }

        .cta-button {
            background: linear-gradient(135deg, #ffd700 0%, #ffed4e 100%);
            color: #2d5016;
            padding: 1.2rem 3rem;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.4s ease;
            text-decoration: none;
            display: inline-block;
            animation: fadeInUp 1s ease 0.4s both;
            box-shadow: 0 8px 30px rgba(255, 215, 0, 0.3);
            position: relative;
            overflow: hidden;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 40px rgba(255, 215, 0, 0.4);
        }

        /* Mission & Vision */
        .mission-vision {
            padding: 6rem 0;
            background: white;
        }

        .section-title {
            text-align: center;
            font-family: 'Playfair Display', serif;
            font-size: 2.8rem;
            font-weight: 700;
            color: #2d5016;
            margin-bottom: 3.5rem;
            letter-spacing: -1px;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: linear-gradient(90deg, #ffd700, #ffed4e);
            border-radius: 2px;
        }

        .mission-vision-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            margin-top: 4rem;
        }

        .mission-card, .vision-card {
            background: white;
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(45, 80, 22, 0.08);
            border: 1px solid rgba(45, 80, 22, 0.05);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .mission-card::before, .vision-card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0;
            height: 4px;
            background: linear-gradient(90deg, #ffd700, #ffed4e);
        }

        .mission-card:hover, .vision-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 30px 80px rgba(45, 80, 22, 0.12);
        }

        .mission-card h3, .vision-card h3 {
            color: #2d5016;
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
        }

        .mission-card p, .vision-card p {
            color: #4a5568;
            font-size: 1.1rem;
            line-height: 1.8;
        }

        /* Course Previews */
        .courses {
            padding: 6rem 0;
            background: linear-gradient(135deg, #fafafa 0%, #f8f9fa 100%);
        }

        .course-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2.5rem;
            margin-top: 4rem;
        }

        .course-card {
            background: white;
            border-radius: 24px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(45, 80, 22, 0.08);
            border: 1px solid rgba(45, 80, 22, 0.05);
            transition: all 0.4s ease;
        }

        .course-card:hover {
            transform: translateY(-12px);
            box-shadow: 0 30px 80px rgba(45, 80, 22, 0.15);
        }

        .course-image {
            background: linear-gradient(135deg, #2d5016 0%, #4a7c59 100%);
            height: 220px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.5rem;
        }

        .course-content { padding: 2.5rem; }

        .course-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            font-weight: 600;
            color: #2d5016;
            margin-bottom: 1rem;
        }

        .course-description {
            color: #4a5568;
            margin-bottom: 2rem;
            font-size: 1.05rem;
            line-height: 1.7;
        }

        .course-btn {
            background: linear-gradient(135deg, #ffd700 0%, #ffed4e 100%);
            color: #2d5016;
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 600;
            font-size: 0.95rem;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            box-shadow: 0 6px 20px rgba(255, 215, 0, 0.25);
        }

        .course-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 30px rgba(255, 215, 0, 0.35);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Impact */
        .impact {
            background: linear-gradient(135deg, #2d5016 0%, #4a7c59 50%, #2d5016 100%);
            color: white;
            padding: 6rem 0;
            position: relative;
            overflow: hidden;
        }

        .impact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 3rem;
            text-align: center;
            position: relative;
            z-index: 1;
        }

        .impact-stat {
            padding: 2rem;
            background: rgba(255,255,255,0.05);
            border-radius: 20px;
            border: 1px solid rgba(255,215,0,0.1);
            transition: all 0.3s ease;
        }

        .impact-stat:hover { transform: translateY(-5px); background: rgba(255,255,255,0.1); }

        .impact-number {
            font-family: 'Playfair Display', serif;
            font-size: 4rem;
            font-weight: 700;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #ffd700, #ffed4e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .impact-text { font-size: 1.2rem; font-weight: 500; opacity: 0.95; }

        /* Testimonials */
        .testimonials { padding: 6rem 0; background: white; }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 3rem;
            margin-top: 4rem;
        }

        .testimonial {
            background: white;
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(45,80,22,0.08);
            border: 1px solid rgba(45,80,22,0.05);
            transition: all 0.4s ease;
            position: relative;
        }

        .testimonial::before {
            content: '"';
            position: absolute;
            top: -10px;
            left: 30px;
            font-size: 6rem;
            color: #ffd700;
            font-family: 'Playfair Display', serif;
            opacity: 0.3;
            line-height: 1;
        }

        .testimonial:hover { transform: translateY(-5px); }

        .testimonial-text {
            font-style: italic;
            margin-bottom: 2rem;
            color: #4a5568;
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .testimonial-author { font-weight: 600; color: #2d5016; font-size: 1.05rem; }

        /* Footer */
        .footer {
            background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
            color: white;
            padding: 3rem 0;
            text-align: center;
        }

        .footer p { color: #aaa; font-size: 0.95rem; }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .social-links a {
            background: linear-gradient(135deg, #ffd700, #ffed4e);
            color: #2d5016;
            padding: 0.6rem;
            border-radius: 50%;
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 1.1rem;
            width: 42px;
            height: 42px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .social-links a:hover { transform: translateY(-3px); }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @media (max-width: 768px) {
            .nav-menu { display: none; }
            .hero h1 { font-size: 2rem; }
            .hero p { font-size: 1.1rem; }
            .mission-vision-grid { grid-template-columns: 1fr; gap: 2rem; }
            .section-title { font-size: 2rem; }
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="nav-container">
            <a href="index.html" class="logo">LS FinLit</a>
            <ul class="nav-menu">
                <li><a href="courses.html">Courses</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#contact" class="contact-btn">Contact</a></li>
            </ul>
        </div>
    </nav>

    <section class="hero">
        <div class="hero-container">
            <h1>Empowering Kids to Be Money Smart — One Lesson at a Time</h1>
            <p>Learn through stories, games, and engaging videos that make financial literacy fun and accessible for every child.</p>
            <a href="courses.html" class="cta-button">Start Learning Today</a>
        </div>
    </section>

    <section class="mission-vision" id="about">
        <div class="container">
            <h2 class="section-title">Our Purpose</h2>
            <div class="mission-vision-grid">
                <div class="mission-card">
                    <h3>🎯 Our Mission</h3>
                    <p>To empower children with financial skills that most Americans lack through age-appropriate lessons, games, and engaging content.</p>
                </div>
                <div class="vision-card">
                    <h3>🌟 Our Vision</h3>
                    <p>A generation of young leaders who are responsible and reasonable with money, equipped to make smart financial decisions for life.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="courses" id="courses">
        <div class="container">
            <h2 class="section-title">Featured Courses</h2>
            <div class="course-grid">
                <div class="course-card">
                    <div class="course-image">💰</div>
                    <div class="course-content">
                        <h3 class="course-title">Understanding Money</h3>
                        <p class="course-description">Discover what money really is, why it has value, and how inflation affects your purchasing power over time.</p>
                        <a href="courses.html?module=0&lesson=0" class="course-btn">Start Learning</a>
                    </div>
                </div>
                <div class="course-card">
                    <div class="course-image">📊</div>
                    <div class="course-content">
                        <h3 class="course-title">Budgeting & Banking</h3>
                        <p class="course-description">Learn how to build a budget that actually works, and how to use bank accounts to manage your money with confidence.</p>
                        <a href="courses.html?module=1&lesson=0" class="course-btn">Start Learning</a>
                    </div>
                </div>
                <div class="course-card">
                    <div class="course-image">🏦</div>
                    <div class="course-content">
                        <h3 class="course-title">Saving & Investing</h3>
                        <p class="course-description">Explore the power of compound interest, how to set savings goals, and why starting to invest early changes everything.</p>
                        <a href="courses.html?module=2&lesson=0" class="course-btn">Start Learning</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="impact">
        <div class="container">
            <div class="impact-grid">
                <div class="impact-stat">
                    <div class="impact-number">6</div>
                    <div class="impact-text">Core Financial Modules</div>
                </div>
                <div class="impact-stat">
                    <div class="impact-number">12</div>
                    <div class="impact-text">In-Depth Lessons</div>
                </div>
                <div class="impact-stat">
                    <div class="impact-number">100%</div>
                    <div class="impact-text">Free to Access</div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" style="padding: 5rem 0; background: white;">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 2rem; margin-top: 4rem; text-align:center;">
                <div style="padding: 2rem; background: #fafafa; border-radius: 16px; border: 1px solid rgba(45,80,22,0.08);">
                    <div style="font-size:2rem; margin-bottom:1rem;">📧</div>
                    <h4 style="font-family:'Playfair Display',serif; color:#2d5016; margin-bottom:0.5rem;">Email</h4>
                    <p style="color:#4a5568;">info.lsfinanciallit@gmail.com</p>
                </div>
                <div style="padding: 2rem; background: #fafafa; border-radius: 16px; border: 1px solid rgba(45,80,22,0.08);">
                    <div style="font-size:2rem; margin-bottom:1rem;">📞</div>
                    <h4 style="font-family:'Playfair Display',serif; color:#2d5016; margin-bottom:0.5rem;">Phone</h4>
                    <p style="color:#4a5568;">(913) 260-0283</p>
                    <p style="color:#4a5568;">(913) 439-8543</p>
                </div>
                <div style="padding: 2rem; background: #fafafa; border-radius: 16px; border: 1px solid rgba(45,80,22,0.08);">
                    <div style="font-size:2rem; margin-bottom:1rem;">📍</div>
                    <h4 style="font-family:'Playfair Display',serif; color:#2d5016; margin-bottom:0.5rem;">Location</h4>
                    <p style="color:#4a5568;">Overland Park, KS</p>
                </div>
            </div>
        </div>
    </section>

    <footer class="footer">
        <div class="container">
            <div class="social-links">
                <a href="#">📘</a>
                <a href="#">🐦</a>
                <a href="#">📷</a>
                <a href="#">💼</a>
            </div>
            <p>📧 info.lsfinanciallit@gmail.com &nbsp;|&nbsp; 📞 (913) 260-0283 &nbsp;|&nbsp; Overland Park, KS</p>
            <p style="margin-top:0.75rem; opacity:0.5;"></p>
        </div>
    </footer>

    <script>
        window.addEventListener('scroll', function() {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 50) {
                navbar.style.background = 'linear-gradient(135deg, #2d5016 0%, #4a7c59 100%)';
            }
        });
    </script>

</body>
</html>
