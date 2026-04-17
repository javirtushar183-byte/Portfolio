<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tushar Javir | Portfolio</title>
    <style>
        :root {
            --bg-color: #080808;
            --card-bg: #121212;
            --accent-gradient: linear-gradient(90deg, #00eaff, #6a5af9);
            --text-main: #ffffff;
            --text-dim: #b0b0b0;
            --border-color: #333;
        }

        body {
            margin: 0;
            font-family: 'Segoe UI', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            scroll-behavior: smooth;
        }

        nav {
            display: flex;
            justify-content: space-between;
            padding: 20px 5%;
            position: sticky;
            top: 0;
            background: rgba(8, 8, 8, 0.9);
            backdrop-filter: blur(10px);
            z-index: 1000;
        }

        /* --- 3D ANIMATED FRAME WITH PHOTO --- */
        .profile-container {
            perspective: 1000px;
            width: 200px;
            height: 200px;
            margin: 0 auto 30px;
            position: relative;
        }

        .profile-3d-model {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            animation: floatModel 4s ease-in-out infinite;
        }

        /* ONLY CHANGE: circle → square */
        .user-photo {
            width: 160px;
            height: 160px;
            border-radius: 12px;
            position: absolute;
            top: 20px;
            left: 20px;
            object-fit: cover;
            border: 2px solid #00eaff;
            z-index: 2;
            box-shadow: 0 0 20px rgba(0, 234, 255, 0.5);
        }

        /* ONLY CHANGE: circle → square */
        .sphere-layer {
            position: absolute;
            width: 100%;
            height: 100%;
            border-radius: 12px;
            border: 1px solid rgba(0, 234, 255, 0.3);
            background: radial-gradient(circle, rgba(0, 234, 255, 0.05) 0%, transparent 70%);
            animation: rotateLayer 10s linear infinite;
        }

        .layer-1 { transform: rotateY(0deg); }
        .layer-2 { transform: rotateY(45deg); animation-duration: 8s; }
        .layer-3 { transform: rotateX(90deg); animation-duration: 12s; }

        @keyframes rotateLayer {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        @keyframes floatModel {
            0%, 100% { transform: translateY(0) rotateX(5deg); }
            50% { transform: translateY(-15px) rotateX(-5deg); }
        }

        /* --- UI ELEMENTS --- */
        .hero { text-align: center; padding: 60px 20px; }
        .hero h1 span { background: var(--accent-gradient); -webkit-background-clip: text; -webkit-text-fill-color: transparent; font-size: 3.5rem; }
        .hero p { color: var(--text-dim); font-size: 1.1rem; max-width: 800px; margin: 20px auto; line-height: 1.6; }
        
        section { padding: 60px 10%; }
        h2 { font-size: 2.2rem; margin-bottom: 10px; }
        .underline { width: 70px; height: 4px; background: var(--accent-gradient); margin-bottom: 40px; border-radius: 10px; }

        .card {
            background: var(--card-bg);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid var(--border-color);
            margin-bottom: 20px;
            transition: 0.3s;
            text-decoration: none;
            display: block;
            color: white;
        }
        .card:hover { border-color: #00eaff; transform: translateY(-5px); }

        .skill-tag {
            display: inline-block;
            background: rgba(0, 234, 255, 0.1);
            padding: 8px 15px;
            border-radius: 20px;
            margin: 5px;
            font-size: 0.9rem;
            border: 1px solid #00eaff;
        }

        .btn {
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            display: inline-block;
            transition: 0.3s;
            margin: 10px;
            border: none;
            cursor: pointer;
        }
        .btn-glow { background: var(--accent-gradient); color: black; }
        .btn-outline { border: 2px solid #00eaff; color: #00eaff; background: transparent; }

        .contact-container { max-width: 600px; margin: 0 auto; text-align: left; }
        input, textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            background: #1a1a1a;
            border: 1px solid #333;
            color: white;
            border-radius: 8px;
            box-sizing: border-box;
        }
        textarea { height: 120px; resize: none; }

        footer { text-align: center; padding: 40px; color: #555; border-top: 1px solid #1a1a1a; }
    </style>
</head>
<body>

    <!-- ✅ REST CODE EXACT SAME (no change) -->

    <nav>
        <div style="font-weight:bold;">TUSHAR JAVIR</div>
        <div>
            <a href="#home" style="color:white; text-decoration:none; margin-left:20px;">Home</a>
            <a href="#experience" style="color:white; text-decoration:none; margin-left:20px;">Experience</a>
            <a href="#projects" style="color:white; text-decoration:none; margin-left:20px;">Projects</a>
            <a href="#contact" style="color:white; text-decoration:none; margin-left:20px;">Contact</a>
        </div>
    </nav>

    <section id="home" class="hero">
        <div class="profile-container">
            <div class="profile-3d-model">
                <img src="1000016946.jpg" class="user-photo" alt="Tushar Javir">
                <div class="sphere-layer layer-1"></div>
                <div class="sphere-layer layer-2"></div>
                <div class="sphere-layer layer-3"></div>
            </div>
        </div>

        <h3>From India</h3>
        <h1>Hi, I'm <span>Tushar Javir</span></h1>
        <p>
            Data Analyst with expertise in SQL, Python, numpy, pandas, matplotlib, Excel, and data visualization tools. 
            Passionate about transforming raw data into actionable insights through advanced analytics and compelling visualizations. 
            Currently pursuing Bachelor of engineering at BSIOTR Wagholi Pune College.
        </p>
        <div style="margin-top: 30px;">
            <a href="https://github.com/javirtushar183-byte" target="_blank" class="btn btn-glow">GitHub</a>
            <a href="https://www.linkedin.com/in/tushar-javir-3b45132b2?utm_source=share_via&utm_content=profile&utm_medium=member_android" target="_blank" class="btn btn-outline">LinkedIn</a>
        </div>
    </section>

    <section id="skills">
        <h2>Skills & Expertise</h2>
        <div class="underline"></div>
        <div class="card">
            <div class="skill-tag">SQL</div>
            <div class="skill-tag">Python</div>
            <div class="skill-tag">Statistics</div>
            <div class="skill-tag">Pandas</div>
            <div class="skill-tag">NumPy</div>
            <div class="skill-tag">Matplotlib</div>
            <div class="skill-tag">Data Visualization</div>
            <div class="skill-tag">Power BI</div>
            <div class="skill-tag">Excel</div>
        </div>
    </section>

    <section id="experience">
        <h2>Experience & Job Simulations</h2>
        <div class="underline"></div>

        <a href="https://www.theforage.com/completion-certificates/ifobHAoMjQs9s6bKS/gMTdCXwDdLYoXZ3wG_ifobHAoMjQs9s6bKS_iAsJJqNKadKu8eazG_1761231970478_completion_certificate.pdf" target="_blank" class="card">
            <h3 style="color: #00eaff;">1) Tata - GenAI Powered Data Analytics</h3>
            <p>Job Simulation | Click to view Certificate</p>
        </a>

        <a href="https://www.theforage.com/completion-certificates/9PBTqmSxAf6zZTseP/io9DzWKe3PTsiS6GG_9PBTqmSxAf6zZTseP_iAsJJqNKadKu8eazG_1768445040887_completion_certificate.pdf" target="_blank" class="card">
            <h3 style="color: #00eaff;">2) Deloitte Australia - Data Analytics</h3>
            <p>Job Simulation | Click to view Certificate</p>
        </a>

        <a href="https://www.theforage.com/completion-certificates/32A6DqtsbF7LbKdcq/NkaC7knWtjSbi6aYv_32A6DqtsbF7LbKdcq_iAsJJqNKadKu8eazG_1775359250880_completion_certificate.pdf" target="_blank" class="card">
            <h3 style="color: #00eaff;">3) Quantium - Data Analytics</h3>
            <p>Job Simulation | Click to view Certificate</p>
        </a>
    </section>

    <section id="projects">
        <h2>Featured Projects</h2>
        <div class="underline"></div>

        <a href="https://github.com/javirtushar183-byte/HR-_ANLYTICS_DASHBOARD" target="_blank" class="card">
            <h3>1) HR Analytics Dashboard</h3>
            <p>Power BI dashboard for tracking workforce performance.</p>
        </a>

        <a href="https://github.com/javirtushar183-byte/Customer-Behaviour-analysis" target="_blank" class="card">
            <h3>2) Customer Behaviour Analysis Dashboard</h3>
            <p>Identifying buying patterns using Python and Pandas.</p>
        </a>

        <a href="https://github.com/javirtushar183-byte/Taxi-Fare-Dashboard" target="_blank" class="card">
            <h3>3) Taxi Fare Analytics Dashboard</h3>
            <p>Visualizing fare trends and pricing optimization.</p>
        </a>
    </section>

    <section id="contact" style="text-align: center;">
        <h2>Contact Me</h2>
        <div class="underline" style="margin: 0 auto 30px;"></div>
        
        <div class="contact-container">
            <p style="text-align: center; margin-bottom: 30px;">
                📧 javirtushar183@gmail.com <br>
                📞 +91 8668874963
            </p>

            <form action="https://formsubmit.co/javirtushar183@gmail.com" method="POST">
                <input type="text" name="name" placeholder="Your Name" required>
                <input type="email" name="email" placeholder="Your Email" required>
                <textarea name="message" placeholder="Message" required></textarea>
                <input type="hidden" name="_captcha" value="false">
                
                <div style="text-align: center;">
                    <button type="submit" class="btn btn-glow" style="width: 100%;">Send Message</button>
                </div>
            </form>
        </div>
    </section>

    <footer>
        © Tushar Javir | Data Analyst Portfolio 2026
    </footer>

</body>
</html>
