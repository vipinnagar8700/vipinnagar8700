<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vipin Nagar - Full Stack Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: #0d1117;
            color: #c9d1d9;
            padding: 20px;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            pointer-events: none;
        }

        .particle {
            position: absolute;
            width: 3px;
            height: 3px;
            background: rgba(99, 102, 241, 0.4);
            border-radius: 50%;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
            animation: fadeIn 0.8s ease-in;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .header {
            text-align: center;
            padding: 80px 0 60px;
            animation: slideDown 1s ease-out;
            position: relative;
        }

        @keyframes slideDown {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .wave {
            animation: wave 2s ease-in-out infinite;
            display: inline-block;
            transform-origin: 70% 70%;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-20deg); }
        }

        .header h1 {
            font-size: 4em;
            margin-bottom: 15px;
            background: linear-gradient(90deg, #6366f1, #8b5cf6, #ec4899, #f59e0b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradient 4s ease infinite;
            background-size: 300% 300%;
        }

        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .subtitle {
            font-size: 1.8em;
            color: #8b949e;
            margin: 20px 0;
        }

        .typing-text {
            font-size: 1.8em;
            color: #6366f1;
            min-height: 60px;
            margin: 30px 0;
            font-weight: 600;
        }

        .social-badges {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
            margin: 40px 0;
        }

        .social-badge {
            padding: 12px 25px;
            background: linear-gradient(135deg, #0077B5, #005582);
            border-radius: 25px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            transition: all 0.3s ease;
            animation: popIn 0.8s ease-out backwards;
        }

        .social-badge.portfolio { background: linear-gradient(135deg, #FF5722, #E64A19); }
        .social-badge.twitter { background: linear-gradient(135deg, #1DA1F2, #0d8ecf); }
        .social-badge.email { background: linear-gradient(135deg, #D14836, #b03a2e); }

        .social-badge:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 30px rgba(99, 102, 241, 0.4);
        }

        .info-badges {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
            margin: 30px 0;
        }

        .info-badge {
            padding: 12px 25px;
            background: #21262d;
            border: 2px solid #6366f1;
            border-radius: 25px;
            transition: all 0.3s ease;
            cursor: pointer;
            font-weight: 600;
            animation: fadeInUp 0.8s ease-out backwards;
        }

        .info-badge:hover {
            background: #6366f1;
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 10px 20px rgba(99, 102, 241, 0.3);
        }

        .section {
            background: #161b22;
            border: 1px solid #30363d;
            border-radius: 15px;
            padding: 50px;
            margin: 40px 0;
            animation: slideIn 0.8s ease-out;
            transition: all 0.3s ease;
        }

        .section:hover {
            border-color: #6366f1;
            box-shadow: 0 0 40px rgba(99, 102, 241, 0.2);
            transform: translateY(-8px);
        }

        @keyframes slideIn {
            from { opacity: 0; transform: translateX(-50px); }
            to { opacity: 1; transform: translateX(0); }
        }

        .section h2 {
            color: #58a6ff;
            margin-bottom: 35px;
            font-size: 2.5em;
            position: relative;
            padding-bottom: 15px;
        }

        .section h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 4px;
            background: linear-gradient(90deg, #6366f1, #8b5cf6);
            animation: expandLine 1.5s ease-out forwards;
        }

        @keyframes expandLine {
            to { width: 150px; }
        }

        .timeline-table {
            width: 100%;
            border-collapse: collapse;
            margin: 30px 0;
            animation: fadeIn 1s ease-in;
        }

        .timeline-table td {
            padding: 20px;
            text-align: center;
            font-size: 1.2em;
            border: 2px solid #30363d;
            background: #21262d;
            transition: all 0.3s ease;
        }

        .timeline-table td:hover {
            background: #2d333b;
            border-color: #6366f1;
            transform: scale(1.05);
        }

        .about-text {
            font-size: 1.2em;
            line-height: 1.9;
            color: #c9d1d9;
            margin: 25px 0;
        }

        .about-list {
            list-style: none;
            margin: 25px 0;
        }

        .about-list li {
            padding: 15px 0 15px 40px;
            position: relative;
            font-size: 1.15em;
            animation: fadeInLeft 0.6s ease-out backwards;
        }

        @keyframes fadeInLeft {
            from { opacity: 0; transform: translateX(-20px); }
            to { opacity: 1; transform: translateX(0); }
        }

        .about-list li::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: #6366f1;
            font-size: 2em;
        }

        .tech-category {
            margin: 40px 0;
        }

        .tech-category h3 {
            color: #8b949e;
            margin-bottom: 25px;
            font-size: 1.8em;
            border-bottom: 2px solid #30363d;
            padding-bottom: 10px;
        }

        .tech-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin: 20px 0;
        }

        .tech-badge-img {
            height: 35px;
            transition: all 0.3s ease;
            animation: popIn 0.5s ease-out backwards;
            border-radius: 5px;
        }

        .tech-badge-img:hover {
            transform: translateY(-8px) scale(1.15);
            filter: brightness(1.3);
            box-shadow: 0 10px 25px rgba(99, 102, 241, 0.4);
        }

        @keyframes popIn {
            from { opacity: 0; transform: scale(0.5); }
            to { opacity: 1; transform: scale(1); }
        }

        .app-section-title {
            color: #58a6ff;
            font-size: 2em;
            text-align: center;
            margin: 50px 0 30px;
            padding: 20px;
            background: linear-gradient(135deg, #1e1e2e, #2a2a3e);
            border-radius: 15px;
            border: 2px solid #6366f1;
        }

        .app-table {
            width: 100%;
            margin: 30px 0;
        }

        .app-card {
            background: #21262d;
            padding: 35px;
            border-radius: 15px;
            border: 2px solid #30363d;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            cursor: pointer;
            animation: scaleIn 0.6s ease-out backwards;
            height: 100%;
            display: flex;
            flex-direction: column;
        }

        @keyframes scaleIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }

        .app-card:hover {
            border-color: #6366f1;
            transform: translateY(-15px) scale(1.03);
            box-shadow: 0 25px 50px rgba(99, 102, 241, 0.3);
        }

        .app-icon {
            font-size: 4em;
            margin-bottom: 20px;
            animation: bounce 2s ease infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .app-card h3 {
            color: #58a6ff;
            margin-bottom: 15px;
            font-size: 1.6em;
        }

        .app-card a {
            color: #58a6ff;
            text-decoration: none;
        }

        .app-card a:hover {
            text-decoration: underline;
        }

        .platform-badge {
            display: inline-block;
            padding: 8px 18px;
            background: #238636;
            border-radius: 15px;
            font-size: 0.95em;
            margin: 10px 5px 15px 0;
            font-weight: 600;
        }

        .app-description {
            color: #8b949e;
            margin: 20px 0;
            line-height: 1.7;
            font-size: 1.05em;
        }

        .tech-stack {
            margin: 20px 0;
            padding: 20px;
            background: #161b22;
            border-radius: 10px;
            border-left: 4px solid #6366f1;
        }

        .tech-stack strong {
            color: #58a6ff;
            display: block;
            margin-bottom: 10px;
        }

        .app-features {
            margin: 20px 0;
        }

        .app-features strong {
            color: #58a6ff;
            display: block;
            margin-bottom: 15px;
            font-size: 1.1em;
        }

        .app-features ul {
            list-style: none;
            padding: 0;
        }

        .app-features li {
            padding: 8px 0 8px 30px;
            position: relative;
            color: #c9d1d9;
        }

        .app-features li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: #6366f1;
            font-weight: bold;
            font-size: 1.3em;
        }

        .store-badge {
            margin-top: 20px;
        }

        .store-badge img {
            height: 55px;
            transition: all 0.3s ease;
        }

        .store-badge img:hover {
            transform: scale(1.1);
            filter: brightness(1.2);
        }

        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 25px;
            margin: 40px 0;
        }

        .stat-img {
            width: 100%;
            border-radius: 12px;
            border: 2px solid #30363d;
            transition: all 0.3s ease;
            animation: fadeInUp 0.8s ease-out backwards;
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .stat-img:hover {
            border-color: #6366f1;
            transform: scale(1.05);
            box-shadow: 0 15px 40px rgba(99, 102, 241, 0.3);
        }

        .tools-grid {
            text-align: center;
            margin: 30px 0;
        }

        .tools-grid img {
            max-width: 100%;
            border-radius: 15px;
            padding: 20px;
            background: #21262d;
            border: 2px solid #30363d;
            transition: all 0.3s ease;
        }

        .tools-grid img:hover {
            border-color: #6366f1;
            transform: scale(1.02);
            box-shadow: 0 10px 30px rgba(99, 102, 241, 0.2);
        }

        .code-block {
            background: #0d1117;
            padding: 30px;
            border-radius: 12px;
            border: 2px solid #30363d;
            margin: 30px 0;
            font-family: 'Courier New', monospace;
            overflow-x: auto;
            animation: fadeIn 1.2s ease-in;
            font-size: 0.95em;
            line-height: 1.6;
        }

        .code-block pre {
            color: #c9d1d9;
            white-space: pre-wrap;
        }

        .achievements-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .achievement-item {
            background: #21262d;
            padding: 25px;
            border-radius: 12px;
            border-left: 4px solid #6366f1;
            transition: all 0.3s ease;
            animation: slideIn 0.8s ease-out backwards;
        }

        .achievement-item:hover {
            transform: translateX(10px);
            box-shadow: 0 10px 30px rgba(99, 102, 241, 0.3);
        }

        .achievement-item h4 {
            color: #58a6ff;
            margin-bottom: 10px;
            font-size: 1.3em;
        }

        .quote {
            text-align: center;
            font-size: 1.8em;
            font-style: italic;
            color: #8b949e;
            margin: 60px 0;
            padding: 50px;
            background: #161b22;
            border: 2px solid #30363d;
            border-radius: 15px;
            animation: fadeIn 2s ease-in;
            position: relative;
        }

        .quote::before {
            content: '💡';
            font-size: 3em;
            display: block;
            margin-bottom: 20px;
        }

        .footer {
            text-align: center;
            padding: 60px 0;
            margin-top: 80px;
            border-top: 2px solid #30363d;
            animation: fadeIn 2.5s ease-in;
        }

        .footer h2 {
            color: #58a6ff;
            margin-bottom: 30px;
            font-size: 2.2em;
        }

        .footer-text {
            margin: 25px 0;
            font-size: 1.2em;
            color: #8b949e;
        }

        .connect-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin: 40px 0;
        }

        .connect-btn {
            padding: 15px 40px;
            background: linear-gradient(135deg, #6366f1, #8b5cf6);
            color: white;
            text-decoration: none;
            border-radius: 30px;
            transition: all 0.3s ease;
            animation: popIn 1s ease-out backwards;
            font-weight: 600;
            font-size: 1.15em;
        }

        .connect-btn:hover {
            transform: translateY(-8px) scale(1.1);
            box-shadow: 0 20px 40px rgba(99, 102, 241, 0.4);
        }

        .profile-views {
            margin: 30px 0;
        }

        .profile-views img {
            transition: all 0.3s ease;
        }

        .profile-views img:hover {
            transform: scale(1.1);
        }

        @media (max-width: 768px) {
            .header h1 { font-size: 2.5em; }
            .typing-text { font-size: 1.3em; }
            .section { padding: 30px 20px; }
            .section h2 { font-size: 1.8em; }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>
    
    <div class="container">
        <div class="header">
            <h1><span class="wave">👋</span> Hi there, I'm Vipin Nagar</h1>
            <p class="subtitle">Full Stack Developer | MERN Stack Expert | Mobile App Developer</p>
            <div class="typing-text" id="typingText"></div>
            
            <div class="social-badges">
                <a href="#" class="social-badge">💼 LinkedIn</a>
                <a href="#" class="social-badge portfolio">🌐 Portfolio</a>
                <a href="#" class="social-badge twitter">🐦 Twitter</a>
                <a href="mailto:YOUR_EMAIL" class="social-badge email">✉️ Email</a>
            </div>
        </div>

        <div class="section">
            <h2>💼 Professional Journey</h2>
            <table class="timeline-table">
                <tr>
                    <td>📅 Started<br><strong style="color: #58a6ff;">March 2022</strong></td>
                    <td>🎯 Focus Areas<br><strong style="color: #58a6ff;">MERN Stack, iOS, Android</strong></td>
                    <td>💪 Experience<br><strong style="color: #58a6ff;">3+ Years</strong></td>
                </tr>
            </table>
            
            <div class="info-badges">
                <div class="info-badge">📅 Started: March 2022</div>
                <div class="info-badge">🎯 MERN Stack & Mobile Development</div>
                <div class="info-badge">💪 3+ Years Experience</div>
                <div class="info-badge">📱 15+ Published Apps</div>
            </div>
        </div>

        <div class="section">
            <h2>👨‍💻 About Me</h2>
            <p class="about-text">Hi there! I'm a passionate and dedicated developer with expertise in the <strong>MERN stack</strong> and <strong>mobile application development</strong> for both iOS and Android. With a strong foundation in full-stack web development and a knack for creating intuitive and dynamic mobile apps, I strive to deliver high-quality, user-centric solutions.</p>
            <ul class="about-list">
                <li>🔭 Currently working on full-stack web and mobile applications</li>
                <li>🌱 Constantly learning and exploring new technologies</li>
                <li>💡 Love building products that solve real-world problems</li>
                <li>🎯 Focused on writing clean, maintainable, and scalable code</li>
                <li>📱 Published 15+ apps on Google Play Store and Apple App Store</li>
            </ul>
        </div>

        <div class="section">
            <h2>🚀 Tech Stack</h2>
            
            <div class="tech-category">
                <h3>Frontend Development</h3>
                <div class="tech-badges">
                    <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" class="tech-badge-img" alt="React">
                    <img src="https://img.shields.io/badge/Redux-593D88?style=for-the-badge&logo=redux&logoColor=white" class="tech-badge-img" alt="Redux">
                    <img src="https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white" class="tech-badge-img" alt="Angular">
                    <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" class="tech-badge-img" alt="JavaScript">
                    <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" class="tech-badge-img" alt="TypeScript">
                    <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" class="tech-badge-img" alt="HTML5">
                    <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" class="tech-badge-img" alt="CSS3">
                    <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" class="tech-badge-img" alt="Tailwind">
                    <img src="https://img.shields.io/badge/Material--UI-0081CB?style=for-the-badge&logo=material-ui&logoColor=white" class="tech-badge-img" alt="Material-UI">
                    <img src="https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white" class="tech-badge-img" alt="Sass">
                </div>
            </div>

            <div class="tech-category">
                <h3>Backend Development</h3>
                <div class="tech-badges">
                    <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" class="tech-badge-img" alt="Node.js">
                    <img src="https://img.shields.io/badge/Express.js-404D59?style=for-the-badge" class="tech-badge-img" alt="Express.js">
                    <img src="https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white" class="tech-badge-img" alt="GraphQL">
                </div>
            </div>

            <div class="tech-category">
                <h3>Mobile Development</h3>
                <div class="tech-badges">
                    <img src="https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" class="tech-badge-img" alt="React Native">
                    <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" class="tech-badge-img" alt="Flutter">
                    <img src="https://img.shields.io/badge/Swift-FA7343?style=for-the-badge&logo=swift&logoColor=white" class="tech-badge-img" alt="Swift">
                    <img src="https://img.shields.io/badge/Kotlin-0095D5?style=for-the-badge&logo=kotlin&logoColor=white" class="tech-badge-img" alt="Kotlin">
                </div>
            </div>

            <div class="tech-category">
                <h3>Database</h3>
                <div class="tech-badges">
                    <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" class="tech-badge-img" alt="MongoDB">
                    <img src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white" class="tech-badge-img" alt="MySQL">
                    <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" class="tech-badge-img" alt="Redis">
                    <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" class="tech-badge-img" alt="Firebase">
                </div>
            </div>

            <div class="tech-category">
                <h3>DevOps & Tools</h3>
                <div class="tech-badges">
                    <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" class="tech-badge-img" alt="Git">
                    <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" class="tech-badge-img" alt="Docker">
                    <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" class="tech-badge-img" alt="AWS">
                    <img src="https://img.shields.io/badge/Heroku-430098?style=for-the-badge&logo=heroku&logoColor=white" class="tech-badge-img" alt="Heroku">
                    <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" class="tech-badge-img" alt="Nginx">
                    <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" class="tech-badge-img" alt="GitHub Actions">
                </div>
            </div>

            <div class="tech-category">
                <h3>Design & Others</h3>
                <div class="tech-badges">
                    <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white" class="tech-badge-img" alt="Figma">
                    <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" class="tech-badge-img" alt="Postman">
                    <img src="https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white" class="tech-badge-img" alt="VS Code">
                </div>
            </div>
        </div>

        <div class="section">
            <h2>📱 Published Mobile Applications</h2>
            
            <h3 class="app-section-title">🏥 Healthcare & Wellness Apps</h3>
            
            <table class="app-table">
                <tr>
                    <td style="width: 50%; padding: 15px; vertical-align: top;">
                        <div class="app-card">
                            <div class="app-icon">🍃</div>
                            <h3><a href="https://play.google.com/store/apps/details?id=com.aaranyawellnessuser">Aaranya Wellness - Healer</a></h3>
                            <div class="platform-badge">Android</div>
                            <p class="app-description">Comprehensive wellness platform for healers providing non-invasive therapies using Acupressure and Sujok. Manages appointments, client records, and therapy sessions for 300+ wellness consultants.</p>
                            <div class="tech-stack">
                                <strong>Tech Stack:</strong> React Native, Redux, Firebase, Node.js
                            </div>
                            <div class="app-features">
                                <strong>Key Features:</strong>
                                <ul>
                                    <li>Appointment scheduling & management</li>
                                    <li>Client health tracking</li>
                                    <li>Therapy session records</li>
                                    <li>Real-time notifications</li>
                                </ul>
                            </div>
                            <div class="store-badge">
                                <a href="https://play.google.com/store/apps/details?id=com.aaranyawellnessuser">
                                    <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" alt="Get it on Google Play">
                                </a>
                            </div>
                        </div>
                    </td>
                    <td style="width: 50%; padding: 15px; vertical-align: top;">
                        <div class="app-card">
                            <div class="app-icon">🍃</div>
                            <h3><a href="https://play.google.com/store/apps/details?id=com.AaranyaWellness">Aaranya Wellness</a></h3>
                            <div class="platform-badge">Android</div>
                            <p class="app-description">Patient-facing wellness app for booking holistic healing therapies. Connects users with certified wellness consultants for treating muscular pain, stress, BP, diabetes through natural therapies.</p>
                            <div class="tech-stack">
                                <strong>Tech Stack:</strong> React Native, Redux, Firebase, REST API
                            </div>
                            <div class="app-features">
                                <strong>Key Features:</strong>
                                <ul>
                                    <li>Book therapy sessions</li>
                                    <li>Track wellness progress</li>
                                    <li>Access healing resources</li>
                                    <li>Personalized health plans</li>
                                </ul>
                            </div>
                            <div class="store-badge">
                                <a href="https://play.google.com/store/apps/details?id=com.AaranyaWellness">
                                    <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" alt="Get it on Google Play">
                                </a>
                            </div>
                        </div>
                    </td>
                </tr>
            </table>

            <table class="app-table">
                <tr>
                    <td style="width: 33.33%; padding: 15px; vertical-align: top;">
                        <div class="app-card">
                            <div class="app-icon">🍃</div>
                            <h3><a href="https://apps.apple.com/us/app/aaranya-wellness-healer/id6747748589">Aaranya Wellness - Healer (iOS)</a></h3>
                            <div class="platform-badge" style="background: #000;">iOS</div>
                            <p class="app-description">iOS version of the healer app with native performance and seamless UX for wellness consultants.</p>
                            <div class="tech-stack">
                                <strong>Tech:</strong> React Native, Redux, Firebase, Node.js
                            </div>
                            <div class="store-badge">
                                <a href="https://apps.apple.com/us/app/aaranya-wellness-healer/id6747748589">
                                    <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" alt="Download on App Store">
                                </a>
                            </div>
                        </div>
                    </td>
                    <td style="width: 33.33%; padding: 15px; vertical-align: top;">
                        <div class="app-card">
                            <div class="app-icon">🍃</div>
                            <h3><a href="https://apps.apple.com/us/app/aaranya-wellness/id6747888428">Aaranya Wellness (iOS)</a></h3>
                            <div class="platform-badge" style="background: #000;">iOS</div>
                            <p class="app-description">Patient app on iOS for booking natural healing therapies at workplace.</p>
                            <div class="tech-stack">
                                <strong>Tech:</strong> React Native, Redux, Firebase, Node.js
                            </div>
                            <div class="store-badge">
                                <a href="https://apps.apple.com/us/app/aaranya-wellness/id6747888428">
                                    <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" alt="Download on App Store">
                                </a>
                            </div>
                        </div>
                    </td>
                    <td style="width: 33.33%; padding: 15px; vertical-align: top;">
                        <div class="app-card">
                            <div class="app-icon">🍃</div>
                            <h3><a href="https://apps.apple.com/us/app/aaranya-healer/id6752554015">Aaranya Healer (iOS)</a></h3>
                            <div class="platform-badge" style="background: #000;">iOS</div>
                            <p class="app-description">Enhanced healer management app with advanced features for therapy tracking.</p>
                            <div class="tech-stack">
                                <strong>Tech:</strong> React Native, Redux, Firebase, Node.js
                            </div>
                            <div class="store-badge">
                                <a href="https://apps.apple.com/us/app/aaranya-healer/id6752554015">
                                    <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" alt="Download on App Store">
                                </a>
                            </div>
                        </div>
                    </td>
                </tr>
            </table>

            <h3 class="app-section-title">🛒 E-Commerce Solutions</h3>

            <table class="app-table">
                <tr>
                    <td style="width: 50%; padding: 15px; vertical-align: top;">
                        <div class="app-card">
                            <div class="app-icon">🛍️</div>
                            <h3><a href="https://play.google.com/store/apps/details?id=com.ondjangobay.customer">OndjangoBay - Customer</a></h3>
                            <div class="platform-badge">Android</div>
                            <p class="app-description">Full-featured e-commerce marketplace connecting buyers with verified vendors. Shop fashion, electronics, home essentials with secure payments and fast shipping.</p>
                            <div class="tech-stack">
                                <strong>Tech Stack:</strong> React Native, Redux Toolkit, Node.js, MongoDB
                            </div>
                            <div class="app-features">
                                <strong>Key Features:</strong>
                                <ul>
                                    <li>Browse thousands of products</li>
                                    <li>Secure multi-gateway payments</li>
                                    <li>Real-time order tracking</li>
                                    <li>Wishlist & personalized recommendations</li>
                                    <li>24/7 customer support</li>
                                </ul>
                            </div>
                            <div class="store-badge">
                                <a href="https://play.google.com/store/apps/details?id=com.ondjangobay.customer">
                                    <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" alt="Get it on Google Play">
                                </a>
                            </div>
                        </div>
                    </td>
                    <td style="width: 50%; padding: 15px; vertical-align: top;">
                        <div class="app-card">
                            <div class="app-icon">💼</div>
                            <h3><a href="https://play.google.com/store/apps/details?id=com.ondjangobay.vendor">OndjangoBay - Vendor</a></h3>
                            <div class="platform-badge">Android</div>
                            <p class="app-description">Powerful vendor management platform for online sellers. Manage products, track orders, monitor inventory, and analyze sales performance.</p>
                            <div class="tech-stack">
                                <strong>Tech Stack:</strong> React Native, Redux, Express.js, MongoDB
                            </div>
                            <div class="app-features">
                                <strong>Key Features:</strong>
                                <ul>
                                    <li>Product catalog management</li>
                                    <li>Real-time order notifications</li>
                                    <li>Inventory tracking & alerts</li>
                                    <li>Sales analytics dashboard</li>
                                    <li>Revenue reporting</li>
                                </ul>
                            </div>
                            <div class="store-badge">
                                <a href="https://play.google.com/store/apps/details?id=com.ondjangobay.vendor">
                                    <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" alt="Get it on Google Play">
                                </a>
                            </div>
                        </div>
                    </td>
                </tr>
            </table>

            <h3 class="app-section-title">📊 Enterprise & Productivity Apps</h3>

            <table class="app-table">
                <tr>
                    <td style="width: 50%; padding: 15px; vertical-align: top;">
                        <div class="app-card">
                            <div class="app-icon">🌾</div>
                            <h3><a href="https://play.google.com/store/apps/details?id=com.farmersurvey">Farmers Survey</a></h3>
                            <div class="platform-badge">Android</div>
                            <p class="app-description">Data collection platform for agricultural sector. Conduct surveys, gather feedback, and analyze farming practices with offline support.</p>
                            <div class="tech-stack">
                                <strong>Tech Stack:</strong> React Native, Firebase, Express.js
                            </div>
                            <div class="app-features">
                                <strong>Key Features:</strong>
                                <ul>
                                    <li>Custom survey creation</li>
                                    <li>Offline data collection</li>
                                    <li>Real-time response tracking</li>
                                    <li>Multi-language support</li>
                                    <li>Data visualization & export</li>
                                </ul>
                            </div>
                            <div class="store-badge">
                                <a href="https://play.google.com/store/apps/details?id=com.farmersurvey">
                                    <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" alt="Get it on Google Play">
                                </a>
                            </div>
                        </div>
                    </td>
                    <td style="width: 50%; padding: 15px; vertical-align: top;">
                        <div class="app-card">
                            <div class="app-icon">👥</div>
                            <h3><a href="https://play.google.com/store/apps/details?id=com.employeetrack">Employee Track</a></h3>
                            <div class="platform-badge">Android</div>
                            <p class="app-description">Comprehensive employee management solution for businesses. Track activities, monitor attendance, assign tasks, and manage projects.</p>
                            <div class="tech-stack">
                                <strong>Tech Stack:</strong> React Native, Redux, Node.js, MySQL
                            </div>
                            <div class="app-features">
                                <strong>Key Features:</strong>
                                <ul>
                                    <li>Attendance monitoring</li>
                                    <li>Task assignment & tracking</li>
                                    <li>Project progress management</li>
                                    <li>Performance analytics</li>
                                    <li>Issue reporting system</li>
                                </ul>
                            </div>
                            <div class="store-badge">
                                <a href="https://play.google.com/store/apps/details?id=com.employeetrack">
                                    <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" alt="Get it on Google Play">
                                </a>
                            </div>
                        </div>
                    </td>
                </tr>
            </table>
        </div>

        <div class="section">
            <h2>📊 GitHub Stats</h2>
            <div class="stats-container">
                <img src="https://github-readme-stats.vercel.app/api?username=vipinnagar8700&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true" class="stat-img" alt="GitHub Stats">
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=vipinnagar8700&layout=compact&langs_count=8&theme=tokyonight" class="stat-img" alt="Top Languages">
            </div>
            <div style="text-align: center; margin: 30px 0;">
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=vipinnagar8700&theme=tokyonight" class="stat-img" alt="GitHub Streak" style="max-width: 600px;">
            </div>
        </div>

        <div class="section">
            <h2>🏆 GitHub Trophies</h2>
            <div style="text-align: center;">
                <img src="https://github-profile-trophy.vercel.app/?username=vipinnagar8700&theme=darkhub&no-frame=true&row=1&column=7" alt="GitHub Trophies" style="max-width: 100%;">
            </div>
        </div>

        <div class="section">
            <h2>🛠️ Languages and Tools</h2>
            <div class="tools-grid">
                <img src="https://skillicons.dev/icons?i=js,html,css,react,redux,angular,solidjs,svelte,nodejs,express,typescript,flutter,jquery,materialui,tailwind,sass,firebase,mongodb,mysql,redis,aws,heroku,md,graphql,github,git,githubactions,docker,nginx,babel,webpack,linux,vscode,figma,postman&perline=12" alt="Languages and Tools">
            </div>
        </div>

        <div class="section">
            <h2>📈 Contribution Graph</h2>
            <div style="text-align: center;">
                <img src="https://github-readme-activity-graph.vercel.app/graph?username=vipinnagar8700&theme=react-dark&hide_border=true" alt="Contribution Graph" style="max-width: 100%; border-radius: 12px;">
            </div>
        </div>

        <div class="section">
            <h2>💼 What I Do</h2>
            <div class="code-block">
                <pre>
<span style="color: #ff79c6;">const</span> <span style="color: #50fa7b;">vipin</span> = {
    <span style="color: #8be9fd;">code</span>: [<span style="color: #f1fa8c;">"JavaScript"</span>, <span style="color: #f1fa8c;">"TypeScript"</span>, <span style="color: #f1fa8c;">"Swift"</span>, <span style="color: #f1fa8c;">"Kotlin"</span>, <span style="color: #f1fa8c;">"Python"</span>],
    <span style="color: #8be9fd;">technologies</span>: {
        <span style="color: #8be9fd;">frontEnd</span>: {
            <span style="color: #8be9fd;">js</span>: [<span style="color: #f1fa8c;">"React"</span>, <span style="color: #f1fa8c;">"Angular"</span>, <span style="color: #f1fa8c;">"Redux"</span>, <span style="color: #f1fa8c;">"jQuery"</span>],
            <span style="color: #8be9fd;">css</span>: [<span style="color: #f1fa8c;">"TailwindCSS"</span>, <span style="color: #f1fa8c;">"Material-UI"</span>, <span style="color: #f1fa8c;">"Sass"</span>, <span style="color: #f1fa8c;">"Bootstrap"</span>]
        },
        <span style="color: #8be9fd;">backEnd</span>: {
            <span style="color: #8be9fd;">js</span>: [<span style="color: #f1fa8c;">"Node.js"</span>, <span style="color: #f1fa8c;">"Express"</span>, <span style="color: #f1fa8c;">"GraphQL"</span>]
        },
        <span style="color: #8be9fd;">mobile</span>: [<span style="color: #f1fa8c;">"React Native"</span>, <span style="color: #f1fa8c;">"Flutter"</span>, <span style="color: #f1fa8c;">"Swift"</span>, <span style="color: #f1fa8c;">"Kotlin"</span>],
        <span style="color: #8be9fd;">databases</span>: [<span style="color: #f1fa8c;">"MongoDB"</span>, <span style="color: #f1fa8c;">"MySQL"</span>, <span style="color: #f1fa8c;">"Redis"</span>, <span style="color: #f1fa8c;">"Firebase"</span>],
        <span style="color: #8be9fd;">devOps</span>: [<span style="color: #f1fa8c;">"Docker"</span>, <span style="color: #f1fa8c;">"AWS"</span>, <span style="color: #f1fa8c;">"Nginx"</span>, <span style="color: #f1fa8c;">"GitHub Actions"</span>],
        <span style="color: #8be9fd;">tools</span>: [<span style="color: #f1fa8c;">"Git"</span>, <span style="color: #f1fa8c;">"Webpack"</span>, <span style="color: #f1fa8c;">"Babel"</span>, <span style="color: #f1fa8c;">"Postman"</span>, <span style="color: #f1fa8c;">"Figma"</span>]
    },
    <span style="color: #8be9fd;">architecture</span>: [<span style="color: #f1fa8c;">"Microservices"</span>, <span style="color: #f1fa8c;">"RESTful APIs"</span>, <span style="color: #f1fa8c;">"Single Page Applications"</span>, <span style="color: #f1fa8c;">"Progressive Web Apps"</span>],
    <span style="color: #8be9fd;">publishedApps</span>: {
        <span style="color: #8be9fd;">android</span>: <span style="color: #bd93f9;">6</span>,
        <span style="color: #8be9fd;">iOS</span>: <span style="color: #bd93f9;">3</span>,
        <span style="color: #8be9fd;">total</span>: <span style="color: #bd93f9;">9</span>
    },
    <span style="color: #8be9fd;">currentFocus</span>: <span style="color: #f1fa8c;">"Building scalable full-stack applications and mobile experiences"</span>
};
                </pre>
            </div>
        </div>

        <div class="section">
            <h2>🎯 Key Achievements</h2>
            <div class="achievements-list">
                <div class="achievement-item">
                    <h4>📱 9+ Published Apps</h4>
                    <p>Across iOS and Android platforms</p>
                </div>
                <div class="achievement-item">
                    <h4>🏥 Healthcare Solutions</h4>
                    <p>Serving 300+ wellness consultants</p>
                </div>
                <div class="achievement-item">
                    <h4>🛍️ E-Commerce Platform</h4>
                    <p>With dual-sided marketplace</p>
                </div>
                <div class="achievement-item">
                    <h4>🌾 AgriTech Innovation</h4>
                    <p>With offline-first data collection</p>
                </div>
                <div class="achievement-item">
                    <h4>👥 Enterprise Solutions</h4>
                    <p>For employee management</p>
                </div>
                <div class="achievement-item">
                    <h4>⭐ 3+ Years</h4>
                    <p>Of consistent full-stack development</p>
                </div>
            </div>
        </div>

        <div class="quote">
            "Code is like humor. When you have to explain it, it's bad." – Cory House
        </div>

        <div class="footer">
            <h2>🤝 Let's Connect</h2>
            <p class="footer-text">I'm always open to interesting conversations and collaboration opportunities!</p>
            <div class="connect-buttons">
                <a href="#" class="connect-btn">💼 LinkedIn - Connect</a>
                <a href="#" class="connect-btn">🐦 Twitter - Follow</a>
                <a href="mailto:YOUR_EMAIL" class="connect-btn">✉️ Email - Contact</a>
            </div>
            <div class="profile-views">
                <img src="https://komarev.com/ghpvc/?username=vipinnagar8700&color=blueviolet&style=for-the-badge" alt="Profile Views">
            </div>
            <p style="margin-top: 30px; color: #8b949e; font-size: 1.1em;">⭐️ From <a href="https://github.com/vipinnagar8700" style="color: #58a6ff; text-decoration: none;">vipinnagar8700</a></p>
        </div>
    </div>

    <script>
        // Typing animation
        const texts = [
            "Full Stack Developer",
            "MERN Stack Specialist",
            "iOS & Android Developer",
            "Building Amazing Products!"
        ];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingElement = document.getElementById('typingText');

        function type() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }

            if (!isDeleting && charIndex === currentText.length) {
                setTimeout(() => isDeleting = true, 2000);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
            }

            const speed = isDeleting ? 50 : 100;
            setTimeout(type, speed);
        }

        type();

        // Create particles
        const particlesContainer = document.getElementById('particles');
        for (let i = 0; i < 50; i++) {
            const particle = document.createElement('div');
            particle.className = 'particle';
            particle.style.left = Math.random() * 100 + '%';
            particle.style.top = Math.random() * 100 + '%';
            particle.style.animationDelay = Math.random() * 20 + 's';
            particle.style.animationDuration = (15 + Math.random() * 10) + 's';
            particlesContainer.appendChild(particle);
        }

        // Particle animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes float {
                0%, 100% { transform: translateY(0) translateX(0); opacity: 0; }
                10% { opacity: 1; }
                90% { opacity: 1; }
                100% { transform: translateY(-100vh) translateX(${Math.random() * 100 - 50}px); opacity: 0; }
            }
        `;
        document.head.appendChild(style);

        // Scroll animations
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.section, .app-card, .achievement-item').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>
