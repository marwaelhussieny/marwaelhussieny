<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Marwa Elhussieny - Data Engineer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Courier New', monospace;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 100%);
            color: #eee;
            padding: 40px 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
        }

        .header {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }

        .glitch {
            font-size: 3.5em;
            font-weight: bold;
            text-transform: uppercase;
            position: relative;
            color: #fff;
            letter-spacing: 3px;
            animation: glitch-text 3s infinite;
        }

        @keyframes glitch-text {
            0%, 100% { text-shadow: 0 0 10px #00ff88; }
            25% { text-shadow: -2px 0 #ff0088, 2px 0 #00ff88; }
            50% { text-shadow: 2px 0 #ff0088, -2px 0 #00ff88; }
            75% { text-shadow: -2px 0 #00ff88, 2px 0 #ff0088; }
        }

        .tagline {
            font-size: 1.2em;
            color: #00ff88;
            margin-top: 10px;
            opacity: 0;
            animation: fadeIn 1s ease-in forwards 0.5s;
        }

        @keyframes fadeIn {
            to { opacity: 1; }
        }

        .terminal {
            background: #000;
            border: 2px solid #00ff88;
            border-radius: 8px;
            padding: 20px;
            margin: 30px 0;
            box-shadow: 0 0 20px rgba(0, 255, 136, 0.3);
            position: relative;
            overflow: hidden;
        }

        .terminal::before {
            content: '● ● ●';
            position: absolute;
            top: 10px;
            left: 15px;
            color: #00ff88;
            font-size: 0.8em;
        }

        .terminal-content {
            margin-top: 30px;
            font-size: 0.95em;
            line-height: 1.8;
        }

        .prompt {
            color: #00ff88;
        }

        .command {
            color: #ff0088;
        }

        .output {
            color: #fff;
            margin-left: 20px;
        }

        .section {
            margin: 40px 0;
            padding: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-left: 4px solid #00ff88;
            border-radius: 4px;
            backdrop-filter: blur(10px);
            transform: translateX(-20px);
            opacity: 0;
            animation: slideIn 0.6s ease-out forwards;
        }

        .section:nth-child(odd) {
            border-left-color: #ff0088;
            animation-delay: 0.2s;
        }

        .section:nth-child(even) {
            animation-delay: 0.4s;
        }

        @keyframes slideIn {
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        h2 {
            color: #00ff88;
            margin-bottom: 20px;
            font-size: 1.8em;
            display: inline-block;
            border-bottom: 2px solid #00ff88;
            padding-bottom: 5px;
        }

        .project-grid {
            display: grid;
            gap: 20px;
            margin-top: 20px;
        }

        .project-card {
            background: rgba(0, 0, 0, 0.4);
            padding: 20px;
            border-radius: 8px;
            border: 1px solid transparent;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .project-card:hover {
            border-color: #00ff88;
            transform: translateY(-5px);
            box-shadow: 0 5px 20px rgba(0, 255, 136, 0.2);
        }

        .project-title {
            color: #ff0088;
            font-size: 1.2em;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .tech-tag {
            display: inline-block;
            background: rgba(0, 255, 136, 0.1);
            color: #00ff88;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.85em;
            margin: 5px 5px 5px 0;
            border: 1px solid #00ff88;
        }

        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }

        .skill-pill {
            background: linear-gradient(135deg, #ff0088 0%, #00ff88 100%);
            padding: 10px 20px;
            border-radius: 25px;
            font-weight: bold;
            transition: transform 0.3s ease;
            cursor: default;
        }

        .skill-pill:hover {
            transform: scale(1.1) rotate(2deg);
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 40px;
            flex-wrap: wrap;
        }

        .contact-link {
            color: #00ff88;
            text-decoration: none;
            padding: 12px 30px;
            border: 2px solid #00ff88;
            border-radius: 30px;
            transition: all 0.3s ease;
            font-weight: bold;
        }

        .contact-link:hover {
            background: #00ff88;
            color: #000;
            transform: scale(1.05);
        }

        .cursor {
            display: inline-block;
            width: 10px;
            height: 20px;
            background: #00ff88;
            animation: blink 0.8s infinite;
        }

        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0; }
        }

        @media (max-width: 768px) {
            .glitch { font-size: 2em; }
            .section { padding: 20px; }
            .contact-links { flex-direction: column; }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1 class="glitch">Marwa Elhussieny</h1>
            <p class="tagline">Data Engineer • Pipeline Builder • Cairo, Egypt</p>
        </div>

        <div class="terminal">
            <div class="terminal-content">
                <div><span class="prompt">marwa@data-eng:~$</span> <span class="command">whoami</span></div>
                <div class="output">Computer Science grad building production data systems</div>
                <div class="output">BSc CS • 3.57/4.0 • Processing 5M+ records daily</div>
                <br>
                <div><span class="prompt">marwa@data-eng:~$</span> <span class="command">cat current_focus.txt</span></div>
                <div class="output">→ ETL pipeline architecture</div>
                <div class="output">→ Spark optimization & distributed computing</div>
                <div class="output">→ AWS serverless data solutions</div>
                <div class="output">→ Real-time streaming with Kafka</div>
                <br>
                <div><span class="prompt">marwa@data-eng:~$</span> <span class="cursor"></span></div>
            </div>
        </div>

        <div class="section">
            <h2>Tech Stack</h2>
            <div class="skills-container">
                <div class="skill-pill">Python</div>
                <div class="skill-pill">SQL</div>
                <div class="skill-pill">Apache Spark</div>
                <div class="skill-pill">Apache Airflow</div>
                <div class="skill-pill">Kafka</div>
                <div class="skill-pill">AWS</div>
                <div class="skill-pill">Docker</div>
                <div class="skill-pill">PostgreSQL</div>
                <div class="skill-pill">Oracle</div>
                <div class="skill-pill">Power BI</div>
            </div>
        </div>

        <div class="section">
            <h2>Recent Projects</h2>
            <div class="project-grid">
                <div class="project-card">
                    <div class="project-title">Enterprise Data Warehouse</div>
                    <p>Kimball methodology implementation with star schema. Airflow orchestration processing 5M+ records. Incremental loading with data quality checks.</p>
                    <div style="margin-top: 10px;">
                        <span class="tech-tag">Airflow</span>
                        <span class="tech-tag">PostgreSQL</span>
                        <span class="tech-tag">ETL</span>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-title">Big Data Pipeline Optimization</div>
                    <p>Rewrote Spark transformations, optimized partitioning strategy. Achieved 70% performance improvement. Handles 2M+ daily records.</p>
                    <div style="margin-top: 10px;">
                        <span class="tech-tag">Apache Spark</span>
                        <span class="tech-tag">Python</span>
                        <span class="tech-tag">Optimization</span>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-title">AWS Serverless Architecture</div>
                    <p>Built serverless data pipeline with S3, Glue, Lambda, and Redshift. Infrastructure-as-code approach for reproducible deployments.</p>
                    <div style="margin-top: 10px;">
                        <span class="tech-tag">AWS</span>
                        <span class="tech-tag">Lambda</span>
                        <span class="tech-tag">Redshift</span>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-title">Analytics Dashboard Suite</div>
                    <p>Power BI dashboards with advanced DAX calculations. Real-time data refresh and actionable business metrics.</p>
                    <div style="margin-top: 10px;">
                        <span class="tech-tag">Power BI</span>
                        <span class="tech-tag">DAX</span>
                        <span class="tech-tag">Analytics</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>Currently Exploring</h2>
            <p style="line-height: 1.8;">
                Real-time data streaming with Apache Kafka • Advanced Spark optimization techniques • 
                ML pipeline integration • Kubernetes for data engineering workloads • 
                Stream processing architectures
            </p>
        </div>

        <div class="contact-links">
            <a href="https://linkedin.com/in/marwa-elhussieny" class="contact-link">LinkedIn</a>
            <a href="mailto:marwaelhussieny17@gmail.com" class="contact-link">Email</a>
            <a href="https://github.com/marwa-elhussieny" class="contact-link">GitHub</a>
        </div>

        <div style="text-align: center; margin-top: 60px; color: #666; font-size: 0.9em;">
            <p>Open to data engineering roles and collaborations</p>
            <p style="margin-top: 10px;">Cairo, Egypt • Remote-friendly</p>
        </div>
    </div>
</body>
</html>
