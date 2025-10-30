<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vipin Nagar - Developer Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Animation */
        .header {
            text-align: center;
            padding: 60px 20px;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            margin-bottom: 40px;
            animation: fadeInDown 1s ease-out;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .header h1 {
            font-size: 3.5em;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from {
                text-shadow: 0 0 20px rgba(102, 126, 234, 0.5);
            }
            to {
                text-shadow: 0 0 30px rgba(118, 75, 162, 0.8);
            }
        }

        .experience-badge {
            display: inline-block;
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            font-size: 1.1em;
            font-weight: bold;
            margin-top: 20px;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
        }

        .section {
            background: rgba(255, 255, 255, 0.95);
            padding: 40px;
            margin-bottom: 30px;
            border-radius: 20px;
            animation: fadeInUp 1s ease-out;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        h2 {
            font-size: 2.5em;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-align: center;
        }

        h3 {
            font-size: 1.8em;
            color: #667eea;
            margin-bottom: 15px;
        }

        .about-text {
            font-size: 1.2em;
            line-height: 1.8;
            color: #555;
        }

        .tech-stack {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .tech-item {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            font-weight: bold;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .tech-item:hover {
            transform: translateY(-10px) rotate(2deg);
            box-shadow: 0 15px 30px rgba(102, 126, 234, 0.4);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .project-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(102, 126, 234, 0.3);
        }

        .project-icon {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4em;
            color: white;
        }

        .project-info {
            padding: 20px;
        }

        .project-info h4 {
            font-size: 1.3em;
            color: #667eea;
            margin-bottom: 10px;
        }

        .project-info p {
            color: #666;
            font-size: 0.95em;
        }

        .platform-badge {
            display: inline-block;
            padding: 5px 15px;
            margin: 5px;
            border-radius: 20px;
            font-size: 0.85em;
            font-weight: bold;
        }

        .web-badge {
            background: #4CAF50;
            color: white;
        }

        .ios-badge {
            background: #000;
            color: white;
        }

        .android-badge {
            background: #3DDC84;
            color: white;
        }

        .skills-img {
            text-align: center;
            margin: 30px 0;
        }

        .skills-img img {
            max-width: 100%;
            border-radius: 15px;
            animation: fadeIn 2s ease-in;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .trophy-section {
            text-align: center;
        }

        .trophy-section img {
            max-width: 100%;
            border-radius: 15px;
            margin: 20px 0;
        }

        .achievements {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 20px;
            flex-wrap: wrap;
        }

        .achievements img {
            width: 150px;
            height: 150px;
            transition: transform 0.3s ease;
        }

        .achievements img:hover {
            transform: scale(1.2) rotate(10deg);
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 2em;
            }
            
            h2 {
                font-size: 1.8em;
            }
            
            .section {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <h1>Vipin Nagar</h1>
            <p style="font-size: 1.3em; color: #666; margin-top: 10px;">Full Stack Developer | MERN Stack Expert | Mobile App Developer</p>
            <div class="experience-badge">
                📅 March 2023 - Present | 2+ Years Experience
            </div>
        </div>

        <!-- About Me Section -->
        <div class="section">
            <h2>👨‍💻 About Me</h2>
            <p class="about-text">
                Hi there! I'm a passionate and dedicated developer with expertise in the MERN stack and mobile application development for both iOS and Android. With a strong foundation in full-stack web development and a knack for creating intuitive and dynamic mobile apps, I strive to deliver high-quality, user-centric solutions.
            </p>
        </div>

        <!-- Tech Stack Section -->
        <div class="section">
            <h2>🚀 Tech Stack</h2>
            <div class="tech-stack">
                <div class="tech-item">
                    <div style="font-size: 2em; margin-bottom: 10px;">🌐</div>
                    <div>MERN Stack</div>
                    <small>MongoDB, Express.js, React.js, Node.js</small>
                </div>
                <div class="tech-item">
                    <div style="font-size: 2em; margin-bottom: 10px;">📱</div>
                    <div>Mobile Development</div>
                    <small>React Native, Swift, Kotlin</small>
                </div>
                <div class="tech-item">
                    <div style="font-size: 2em; margin-bottom: 10px;">💻</div>
                    <div>Programming</div>
                    <small>JavaScript, TypeScript</small>
                </div>
                <div class="tech-item">
                    <div style="font-size: 2em; margin-bottom: 10px;">🔧</div>
                    <div>Tools & APIs</div>
                    <small>RESTful APIs, GraphQL, Git, Docker</small>
                </div>
            </div>
        </div>

        <!-- Web Projects Section -->
        <div class="section">
            <h2>🌐 Web Applications</h2>
            <p style="text-align: center; color: #666; margin-bottom: 30px;">Full-stack web applications built with MERN stack</p>
            <div class="projects-grid">
                <a href="YOUR_PROJECT_1_URL" target="_blank" style="text-decoration: none;">
                    <div class="project-card">
                        <div class="project-icon">🚀</div>
                        <div class="project-info">
                            <h4>Project Name 1</h4>
                            <p>E-commerce platform with real-time updates and payment integration</p>
                            <span class="platform-badge web-badge">Web</span>
                        </div>
                    </div>
                </a>
                <a href="YOUR_PROJECT_2_URL" target="_blank" style="text-decoration: none;">
                    <div class="project-card">
                        <div class="project-icon">📊</div>
                        <div class="project-info">
                            <h4>Project Name 2</h4>
                            <p>Analytics dashboard with data visualization and reporting</p>
                            <span class="platform-badge web-badge">Web</span>
                        </div>
                    </div>
                </a>
                <a href="YOUR_PROJECT_3_URL" target="_blank" style="text-decoration: none;">
                    <div class="project-card">
                        <div class="project-icon">💬</div>
                        <div class="project-info">
                            <h4>Project Name 3</h4>
                            <p>Social networking platform with real-time chat features</p>
                            <span class="platform-badge web-badge">Web</span>
                        </div>
                    </div>
                </a>
            </div>
        </div>

        <!-- Mobile Apps Section -->
        <div class="section">
            <h2>📱 Mobile Applications</h2>
            <p style="text-align: center; color: #666; margin-bottom: 30px;">Cross-platform and native mobile apps for iOS & Android</p>
            <div class="projects-grid">
                <a href="YOUR_IOS_APP_1_URL" target="_blank" style="text-decoration: none;">
                    <div class="project-card">
                        <div class="project-icon">🍎</div>
                        <div class="project-info">
                            <h4>iOS App Name 1</h4>
                            <p>Feature-rich iOS application with seamless user experience</p>
                            <span class="platform-badge ios-badge">iOS</span>
                        </div>
                    </div>
                </a>
                <a href="YOUR_ANDROID_APP_1_URL" target="_blank" style="text-decoration: none;">
                    <div class="project-card">
                        <div class="project-icon">🤖</div>
                        <div class="project-info">
                            <h4>Android App Name 1</h4>
                            <p>High-performance Android app with modern design</p>
                            <span class="platform-badge android-badge">Android</span>
                        </div>
                    </div>
                </a>
                <a href="YOUR_CROSS_PLATFORM_APP_URL" target="_blank" style="text-decoration: none;">
                    <div class="project-card">
                        <div class="project-icon">📲</div>
                        <div class="project-info">
                            <h4>Cross-Platform App</h4>
                            <p>React Native app for both iOS and Android platforms</p>
                            <span class="platform-badge ios-badge">iOS</span>
                            <span class="platform-badge android-badge">Android</span>
                        </div>
                    </div>
                </a>
            </div>
        </div>

        <!-- GitHub Trophies Section -->
        <div class="section trophy-section">
            <h2>🏆 GitHub Trophies 🏆</h2>
            <a href="https://github.com/vipinnagar8700" target="_blank">
                <img src="https://github-profile-trophy.vercel.app/?username=vipinnagar8700&row=2&column=6&margin-w=20&margin-h=20&theme=darkhub" alt="GitHub Trophies">
            </a>
        </div>

        <!-- GitHub Achievements Section -->
        <div class="section trophy-section">
            <h2>🏆 GitHub Achievements 🏆</h2>
            <div class="achievements">
                <a href="https://github.com/vipinnagar8700" target="_blank">
                    <img src="https://github.githubassets.com/assets/pull-shark-default-498c279a747d.png" alt="Pull Shark Achievement">
                </a>
                <a href="https://github.com/vipinnagar8700" target="_blank">
                    <img src="https://github.githubassets.com/assets/yolo-default-be0bbff04951.png" alt="YOLO Achievement">
                </a>
            </div>
        </div>

        <!-- Languages and Tools Section -->
        <div class="section">
            <h2>🛠️ Languages and Tools 🛠️</h2>
            <div class="skills-img">
                <img src="https://skillicons.dev/icons?i=js,html,css,react,redux,angular,solidjs,svelte,nodejs,express,typescript,flutter,jquery,materialui,tailwind,sass,firebase,mongodb,mysql,redis,aws,heroku,md,graphql,github,git,githubactions,docker,nginx,babel,webpack,linux,vscode,figma,postman&perline=12" alt="Tech Stack">
            </div>
        </div>
    </div>
</body>
</html>
