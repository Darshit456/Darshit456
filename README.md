<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Darshit Gohil - GitHub Profile Demo</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans', Helvetica, Arial, sans-serif;
            background-color: #0d1117;
            color: #e6edf3;
            line-height: 1.5;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: #161b22;
            border-radius: 8px;
            padding: 32px;
            border: 1px solid #30363d;
        }
        
        .header {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #2E9EF7, #7C3AED);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .typing-text {
            background-color: #21262d;
            padding: 12px 24px;
            border-radius: 6px;
            font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
            color: #2E9EF7;
            border: 1px solid #30363d;
            display: inline-block;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.7; }
        }
        
        .section {
            margin-bottom: 40px;
        }
        
        .section h2 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #f0f6fc;
            border-bottom: 2px solid #21262d;
            padding-bottom: 8px;
        }
        
        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .about-item {
            background-color: #21262d;
            padding: 16px;
            border-radius: 6px;
            border-left: 4px solid #2E9EF7;
        }
        
        .about-item strong {
            color: #58a6ff;
        }
        
        .tech-category {
            margin-bottom: 24px;
        }
        
        .tech-category h3 {
            color: #7c3aed;
            margin-bottom: 12px;
            font-size: 1.1rem;
        }
        
        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 16px;
        }
        
        .badge {
            background: linear-gradient(90deg, #2E9EF7, #7C3AED);
            color: white;
            padding: 6px 12px;
            border-radius: 4px;
            font-size: 0.85rem;
            font-weight: 600;
            text-decoration: none;
            display: inline-block;
            transition: transform 0.2s;
        }
        
        .badge:hover {
            transform: translateY(-2px);
        }
        
        .project-card {
            background-color: #21262d;
            border: 1px solid #30363d;
            border-radius: 8px;
            padding: 24px;
            margin-bottom: 24px;
            transition: border-color 0.3s;
        }
        
        .project-card:hover {
            border-color: #58a6ff;
        }
        
        .project-title {
            font-size: 1.4rem;
            color: #58a6ff;
            margin-bottom: 12px;
            text-decoration: none;
        }
        
        .project-subtitle {
            color: #8b949e;
            font-style: italic;
            margin-bottom: 16px;
        }
        
        .project-badges {
            display: flex;
            gap: 8px;
            margin-bottom: 16px;
            flex-wrap: wrap;
        }
        
        .status-badge {
            padding: 4px 8px;
            border-radius: 12px;
            font-size: 0.75rem;
            font-weight: 600;
        }
        
        .status-completed {
            background-color: #238636;
            color: white;
        }
        
        .status-development {
            background-color: #bf8700;
            color: white;
        }
        
        .feature-list {
            list-style: none;
            margin-bottom: 16px;
        }
        
        .feature-list li {
            margin-bottom: 8px;
            padding-left: 20px;
            position: relative;
        }
        
        .feature-list li:before {
            content: "•";
            color: #2E9EF7;
            font-weight: bold;
            position: absolute;
            left: 0;
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            text-align: center;
        }
        
        .stat-card {
            background-color: #21262d;
            border: 1px solid #30363d;
            border-radius: 8px;
            padding: 20px;
            height: 200px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #21262d 0%, #30363d 100%);
        }
        
        .stat-placeholder {
            color: #8b949e;
            font-style: italic;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 16px;
            flex-wrap: wrap;
        }
        
        .social-link {
            background: linear-gradient(45deg, #2E9EF7, #7C3AED);
            color: white;
            padding: 12px 24px;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        
        .social-link:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(46, 158, 247, 0.3);
        }
        
        .highlight-box {
            background: linear-gradient(135deg, #21262d 0%, #2E9EF7 0%, #7C3AED 100%);
            background-size: 200% 200%;
            border: 2px solid transparent;
            border-radius: 8px;
            padding: 20px;
            text-align: center;
            margin: 30px 0;
            animation: gradientShift 3s ease infinite;
        }
        
        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        
        .yaml-code {
            background-color: #0d1117;
            border: 1px solid #21262d;
            border-radius: 8px;
            padding: 24px;
            font-family: 'Fira Code', 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
            font-size: 1rem;
            line-height: 1.6;
            overflow-x: auto;
            color: #e6edf3;
            position: relative;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }
        
        .yaml-code::before {
            content: "yaml";
            position: absolute;
            top: 8px;
            right: 12px;
            background-color: #21262d;
            color: #8b949e;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 0.75rem;
            font-weight: 600;
        }
        
        .yaml-key {
            color: #ff7b72;
            font-weight: 600;
        }
        
        .yaml-string {
            color: #a5d6ff;
            font-weight: 500;
        }
        
        .yaml-array {
            color: #ffa657;
        }
        
        .yaml-comment {
            color: #8b949e;
            font-style: italic;
        }
        
        .yaml-value {
            color: #79c0ff;
        }
        
        /* Animated job roles */
        .job-roles {
            display: inline-block;
            position: relative;
            min-width: 300px;
        }
        
        .job-role {
            display: inline-block;
            opacity: 0;
            animation: slideInFade 0.8s ease-in-out forwards;
            font-weight: 600;
            background: linear-gradient(45deg, #2E9EF7, #7C3AED, #10B981);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            background-size: 300% 300%;
            animation: slideInFade 0.8s ease-in-out forwards, gradientMove 3s ease-in-out infinite;
        }
        
        .job-role:nth-child(1) { animation-delay: 0s; }
        .job-role:nth-child(2) { animation-delay: 0.2s; }
        .job-role:nth-child(3) { animation-delay: 0.4s; }
        .job-role:nth-child(4) { animation-delay: 0.6s; }
        
        @keyframes slideInFade {
            0% {
                opacity: 0;
                transform: translateY(20px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes gradientMove {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        
        .yaml-section {
            margin-bottom: 16px;
        }
        
        .yaml-section:last-child {
            margin-bottom: 0;
        }
        
        .profile-views {
            text-align: center;
            margin-top: 30px;
        }
        
        .profile-views img {
            border-radius: 4px;
        }
        
        hr {
            border: none;
            height: 1px;
            background: linear-gradient(90deg, transparent, #30363d, transparent);
            margin: 40px 0;
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 16px;
            }
            
            .header h1 {
                font-size: 2rem;
            }
            
            .social-links {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <h1>👋 Hi there! I'm Darshit Gohil</h1>
            <div class="typing-text">
                Full Stack .NET Developer | Problem Solver & Code Enthusiast | Building Smart Solutions
            </div>
        </div>

        <!-- About Section -->
        <div class="section">
            <h2>🚀 About Me</h2>
            <p style="margin-bottom: 20px; color: #c9d1d9;">
                <strong>Software Engineer</strong> passionate about creating innovative solutions that make a difference. 
                Currently focusing on <strong>Full Stack .NET Development</strong> while expanding expertise in <strong>DevOps</strong> and <strong>Machine Learning</strong>.
            </p>
            
            <div class="about-grid">
                <div class="about-item">
                    <strong>🔭 Currently Working On:</strong> SmartCity360 - GIS-based urban planning platform with ML predictions
                </div>
                <div class="about-item">
                    <strong>🌟 Recently Completed:</strong> Healthspan Vista - Comprehensive Hospital Management System
                </div>
                <div class="about-item">
                    <strong>🎯 Seeking Opportunities:</strong> Full Stack .NET Developer and related roles
                </div>
                <div class="about-item">
                    <strong>🎮 Fun Fact:</strong> I love coding, playing online video games, and video editing
                </div>
            </div>
        </div>

        <hr>

        <!-- Tech Stack Section -->
        <div class="section">
            <h2>🛠️ Tech Stack</h2>
            
            <div class="tech-category">
                <h3>Languages</h3>
                <div class="badges">
                    <span class="badge">C#</span>
                    <span class="badge">Java</span>
                    <span class="badge">Python</span>
                    <span class="badge">JavaScript</span>
                    <span class="badge">C</span>
                    <span class="badge">C++</span>
                </div>
            </div>
            
            <div class="tech-category">
                <h3>Frontend Technologies</h3>
                <div class="badges">
                    <span class="badge">React</span>
                    <span class="badge">HTML5</span>
                    <span class="badge">CSS3</span>
                    <span class="badge">Tailwind CSS</span>
                    <span class="badge">Axios</span>
                </div>
            </div>
            
            <div class="tech-category">
                <h3>Backend & Database</h3>
                <div class="badges">
                    <span class="badge">.NET Core</span>
                    <span class="badge">SQL Server</span>
                    <span class="badge">PostgreSQL</span>
                    <span class="badge">Microservices</span>
                </div>
            </div>
            
            <div class="tech-category">
                <h3>Tools & DevOps</h3>
                <div class="badges">
                    <span class="badge">Docker</span>
                    <span class="badge">Git</span>
                    <span class="badge">GitHub</span>
                    <span class="badge">Azure</span>
                    <span class="badge">Postman</span>
                    <span class="badge">CI/CD</span>
                </div>
            </div>
        </div>

        <hr>

        <!-- Featured Projects Section -->
        <div class="section">
            <h2>🏆 Featured Projects</h2>
            
            <div class="project-card">
                <a href="#" class="project-title">🏥 Healthspan Vista - Hospital Management System</a>
                <div class="project-subtitle">Your Complete Healthcare Horizon ✨</div>
                
                <div class="project-badges">
                    <span class="status-badge status-completed">Completed</span>
                    <span class="badge">React 19.0.0</span>
                    <span class="badge">.NET 8.0</span>
                </div>
                
                <ul class="feature-list">
                    <li><strong>🔐 Vista Security:</strong> JWT-based authentication with role-based access control</li>
                    <li><strong>👥 Multi-Role System:</strong> Admin, Doctor, and Patient dashboards</li>
                    <li><strong>📊 Real-time Analytics:</strong> Comprehensive medical records and appointment management</li>
                    <li><strong>🎨 Modern UI:</strong> Beautiful, responsive design with smooth animations</li>
                </ul>
                
                <div style="color: #8b949e; font-size: 0.9rem;">
                    <strong>Tech Stack:</strong> React 19, .NET 8, SQL Server, Tailwind CSS, JWT Authentication
                </div>
            </div>
            
            <div class="project-card">
                <a href="#" class="project-title">🏙️ SmartCity360 - Urban Planning Platform</a>
                <div class="project-subtitle">GIS-based urban planning with ML predictions 🌍</div>
                
                <div class="project-badges">
                    <span class="status-badge status-development">In Development</span>
                    <span class="badge">Microservices</span>
                    <span class="badge">ML Powered</span>
                </div>
                
                <ul class="feature-list">
                    <li><strong>🗺️ Interactive GIS Maps:</strong> Real-time visualization using Leaflet.js</li>
                    <li><strong>🤖 ML Predictions:</strong> Population growth forecasting and resource optimization</li>
                    <li><strong>🏗️ Microservices Architecture:</strong> Scalable backend with .NET 8 and Python FastAPI</li>
                    <li><strong>☁️ Cloud-Ready:</strong> Docker containerization with Azure deployment</li>
                </ul>
                
                <div style="color: #8b949e; font-size: 0.9rem;">
                    <strong>Tech Stack:</strong> React, .NET 8, Python FastAPI, PostgreSQL + PostGIS, Docker, Azure
                </div>
            </div>
        </div>

        <hr>

        <!-- GitHub Stats Section -->
        <div class="section">
            <h2>📊 GitHub Statistics</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-placeholder">GitHub Stats Widget<br/>Shows: commits, PRs, issues, stars</div>
                </div>
                <div class="stat-card">
                    <div class="stat-placeholder">Top Languages<br/>C#, JavaScript, Python, Java</div>
                </div>
                <div class="stat-card">
                    <div class="stat-placeholder">Contribution Streak<br/>115 contributions in last year</div>
                </div>
                <div class="stat-card">
                    <div class="stat-placeholder">Activity Graph<br/>Contribution timeline</div>
                </div>
            </div>
        </div>

        <hr>

        <!-- Current Focus Section -->
        <div class="section">
            <h2>🌟 Current Focus Areas</h2>
            <div class="yaml-code">
<div class="yaml-section"><span class="yaml-key">career_goals:</span>
  <span class="yaml-key">primary:</span> <span class="yaml-string">"Full Stack .NET Developer"</span>
  <span class="yaml-key">secondary:</span> 
    <span class="yaml-value">- <span class="job-role">"DevOps Engineer"</span></span>
    <span class="yaml-value">- <span class="job-role">"Python Developer"</span></span>
    <span class="yaml-value">- <span class="job-role">"ML Engineer"</span></span></div>
  
<div class="yaml-section"><span class="yaml-key">current_learning:</span>
  <span class="yaml-value">- Advanced DevOps practices with Azure</span>
  <span class="yaml-value">- Machine Learning model deployment</span>
  <span class="yaml-value">- Microservices architecture patterns</span>
  <span class="yaml-value">- Cloud-native development</span></div>
  
<div class="yaml-section"><span class="yaml-key">seeking:</span>
  <span class="yaml-value">- Full Stack .NET Developer roles</span>
  <span class="yaml-value">- Software Engineering positions</span>
  <span class="yaml-value">- Remote/Hybrid opportunities</span>
  <span class="yaml-value">- Collaborative team environments</span></div>

<div class="yaml-section"><span class="yaml-comment"># 🎯 Ready to contribute to innovative projects!</span></div>
            </div>
        </div>

        <hr>

        <!-- Problem Solving Section -->
        <div class="section">
            <h2>🏅 Problem Solving & DSA</h2>
            <div style="text-align: center; margin-bottom: 20px;">
                <a href="https://leetcode.com/u/Darshit345/" class="badge" style="font-size: 1rem; padding: 12px 24px;">
                    LeetCode Profile
                </a>
            </div>
            <p style="text-align: center; color: #8b949e;">
                Actively solving <strong>Data Structures & Algorithms</strong> problems to strengthen problem-solving skills and prepare for technical interviews.
            </p>
        </div>

        <hr>

        <!-- Connect Section -->
        <div class="section">
            <h2>📫 Let's Connect!</h2>
            <div class="social-links">
                <a href="https://in.linkedin.com/in/darshit-gohil-04a878241" class="social-link">LinkedIn</a>
                <a href="https://www.instagram.com/darshit5597" class="social-link">Instagram</a>
                <a href="https://leetcode.com/u/Darshit345/" class="social-link">LeetCode</a>
                <a href="mailto:darshitgohil456@gmail.com" class="social-link">Email</a>
            </div>
        </div>

        <!-- Highlight Box -->
        <div class="highlight-box">
            <h3 style="margin-bottom: 16px;">💡 "Building the future, one line of code at a time" 💡</h3>
            <p style="font-style: italic;">Open to exciting Full Stack .NET Developer opportunities!</p>
        </div>

        <!-- Profile Views -->
        <div class="profile-views">
            <div style="background: linear-gradient(90deg, #2E9EF7, #7C3AED); color: white; padding: 8px 16px; border-radius: 4px; display: inline-block;">
                Profile Views: 1,234
            </div>
        </div>
    </div>
</body>
</html>
