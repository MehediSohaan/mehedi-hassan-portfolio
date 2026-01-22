<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mehedi Hassan | SQA Engineer Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Roboto:wght@300;400;500&display=swap">
    <style>
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #0ea5e9;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #64748b;
            --light-gray: #e2e8f0;
            --success: #10b981;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }
        
        h1, h2, h3, h4, h5 {
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
            line-height: 1.3;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        section {
            padding: 100px 0;
        }
        
        .section-title {
            font-size: 2.5rem;
            margin-bottom: 3rem;
            text-align: center;
            position: relative;
            color: var(--dark);
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: 2px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 28px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            color: white;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(37, 99, 235, 0.2);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }
        
        .btn-outline:hover {
            background: var(--primary);
            color: white;
        }
        
        /* Header & Navigation */
        header {
            background-color: white;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
        }
        
        .logo span {
            color: var(--secondary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            gap: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: width 0.3s;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--dark);
        }
        
        /* Hero Section */
        .hero {
            padding: 180px 0 100px;
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -10%;
            width: 600px;
            height: 600px;
            background: linear-gradient(45deg, rgba(37, 99, 235, 0.1), rgba(14, 165, 233, 0.1));
            border-radius: 50%;
            z-index: 0;
        }
        
        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
            position: relative;
            z-index: 1;
        }
        
        .hero-text h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            color: var(--dark);
        }
        
        .hero-text h2 {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 20px;
            font-weight: 500;
        }
        
        .hero-text p {
            font-size: 1.1rem;
            color: var(--gray);
            margin-bottom: 30px;
        }
        
        .hero-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }
        
        .hero-image {
            text-align: center;
        }
        
        .profile-img-container {
            width: 100%;
            max-width: 400px;
            height: 400px;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(37, 99, 235, 0.2);
            margin: 0 auto;
            border: 5px solid white;
            background-color: #f8fafc;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .profile-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }
        
        .profile-placeholder {
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: white;
            font-size: 5rem;
            font-weight: bold;
        }
        
        .contact-info {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--gray);
        }
        
        .contact-item i {
            color: var(--primary);
        }
        
        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: start;
        }
        
        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .about-text p {
            margin-bottom: 20px;
            color: var(--gray);
        }
        
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .skill-category {
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .skill-category h4 {
            margin-bottom: 20px;
            color: var(--primary);
            font-size: 1.3rem;
        }
        
        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .skill-tag {
            background-color: #e0f2fe;
            color: var(--primary);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
        }
        
        .skill-tag.highlight {
            background-color: var(--primary);
            color: white;
        }
        
        /* Education & Experience */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 4px;
            background-color: var(--light-gray);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -2px;
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item:nth-child(odd) {
            left: 0;
        }
        
        .timeline-item:nth-child(even) {
            left: 50%;
        }
        
        .timeline-content {
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            position: relative;
        }
        
        .timeline-content h4 {
            color: var(--primary);
            margin-bottom: 5px;
        }
        
        .timeline-content .date {
            color: var(--gray);
            font-size: 0.9rem;
            margin-bottom: 10px;
            display: block;
        }
        
        .timeline-content p {
            color: var(--gray);
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: var(--primary);
            border: 4px solid white;
            border-radius: 50%;
            top: 20px;
            right: -10px;
            z-index: 1;
        }
        
        .timeline-item:nth-child(even)::after {
            left: -10px;
        }
        
        /* Projects Section */
        .projects {
            background-color: #f8fafc;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.12);
        }
        
        .project-header {
            padding: 20px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            color: white;
        }
        
        .project-header h3 {
            margin-bottom: 5px;
        }
        
        .project-type {
            font-size: 0.9rem;
            opacity: 0.9;
        }
        
        .project-body {
            padding: 20px;
        }
        
        .project-body p {
            color: var(--gray);
            margin-bottom: 15px;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 15px;
        }
        
        .tech-tag {
            background-color: #f1f5f9;
            color: var(--dark);
            padding: 5px 10px;
            border-radius: 15px;
            font-size: 0.8rem;
        }
        
        /* Languages & Achievements */
        .languages-achievements {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }
        
        .languages-list {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .language-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .language-name {
            font-weight: 500;
        }
        
        .language-level {
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        .achievement-card {
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .achievement-card h3 {
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .achievement-card p {
            color: var(--gray);
        }
        
        /* Contact Section */
        .contact {
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }
        
        .contact-info h3 {
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .contact-details {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .contact-detail {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 1.2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            border: 1px solid var(--light-gray);
            border-radius: 5px;
            font-size: 1rem;
            font-family: 'Roboto', sans-serif;
        }
        
        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: var(--primary);
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 15px;
        }
        
        .footer-links h4,
        .footer-contact h4 {
            margin-bottom: 20px;
            font-size: 1.2rem;
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--secondary);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .hero-text h1 {
                font-size: 3rem;
            }
            
            .hero-buttons {
                justify-content: center;
            }
            
            .contact-info {
                justify-content: center;
            }
            
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
            
            .timeline-item::after {
                left: 21px;
            }
            
            .timeline-item:nth-child(even)::after {
                left: 21px;
            }
            
            .profile-img-container {
                max-width: 350px;
                height: 350px;
            }
        }
        
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 70px;
                left: -100%;
                flex-direction: column;
                background-color: white;
                width: 100%;
                text-align: center;
                padding: 20px 0;
                box-shadow: 0 10px 10px rgba(0, 0, 0, 0.1);
                transition: left 0.3s;
                gap: 0;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .hero-text h1 {
                font-size: 2.5rem;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .profile-img-container {
                max-width: 300px;
                height: 300px;
            }
        }
        
        @media (max-width: 480px) {
            .hero-text h1 {
                font-size: 2rem;
            }
            
            .hero-text h2 {
                font-size: 1.4rem;
            }
            
            .profile-img-container {
                max-width: 250px;
                height: 250px;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container">
            <nav>
                <a href="#home" class="logo">Mehedi<span>Hassan</span></a>
                <div class="menu-toggle" id="menuToggle">
                    <i class="fas fa-bars"></i>
                </div>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#experience">Experience</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Mehedi Hassan</h1>
                    <h2>SQA Engineer</h2>
                    <p>Completed Computer Science graduate from IUBAT with a proven track record in SQA engineering at EWN Bangladesh Ltd. Highly skilled in collaborating with development teams, actively participating in bug analysis meetings, and prioritizing identified issues for swift resolution.</p>
                    <div class="hero-buttons">
                        <a href="#projects" class="btn">View My Work</a>
                        <a href="#contact" class="btn btn-outline">Contact Me</a>
                    </div>
                    <div class="contact-info">
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <span>01317770923</span>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <span>mehedisohaan@gmail.com</span>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <span>Uttor Badda, Linkroad, Dhaka</span>
                        </div>
                    </div>
                </div>
                <div class="hero-image">
                    <div class="profile-img-container">
                        <!-- Replace with your actual photo -->
                        <!-- <img src="MH.png" alt="Mehedi Hassan" class="profile-img"> -->
                        <div class="profile-placeholder">
                            MH
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About & Skills Section -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">About & Skills</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>Professional Summary</h3>
                    <p>I am a dedicated SQA Engineer with experience at EWN Bangladesh Limited, specializing in both manual and automated testing. My expertise includes API testing with Postman, mobile app testing (Android & iOS), and working with tools like JMeter, Jira, and ClickUp.</p>
                    <p>I have completed Salesforce Admin training and possess foundational knowledge in JavaScript, HTML, CSS, PHP, and MySQL. I'm passionate about ensuring software quality and delivering exceptional user experiences.</p>
                    
                    <div class="skills-container">
                        <div class="skill-category">
                            <h4>Testing Skills</h4>
                            <div class="skills-list">
                                <span class="skill-tag highlight">Manual Testing</span>
                                <span class="skill-tag highlight">Automation Testing</span>
                                <span class="skill-tag">API Testing (Postman)</span>
                                <span class="skill-tag">Android & iOS Apps Testing</span>
                                <span class="skill-tag">JMeter</span>
                                <span class="skill-tag">Jira & ClickUp</span>
                            </div>
                        </div>
                        
                        <div class="skill-category">
                            <h4>Technical Skills</h4>
                            <div class="skills-list">
                                <span class="skill-tag">Salesforce (Admin)</span>
                                <span class="skill-tag">Basic JavaScript</span>
                                <span class="skill-tag">HTML</span>
                                <span class="skill-tag">CSS</span>
                                <span class="skill-tag">PHP</span>
                                <span class="skill-tag">MySQL</span>
                                <span class="skill-tag">Project Management</span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="education">
                    <h3>Education</h3>
                    <div class="education-item" style="background-color: white; padding: 25px; border-radius: 10px; box-shadow: 0 5px 15px rgba(0,0,0,0.05); margin-top: 20px;">
                        <h4>BSc in Computer Science and Engineering</h4>
                        <p class="date">IUBAT - International University of Business Agriculture and Technology</p>
                        <p class="date">Graduated: 2021</p>
                        <p><strong>CGPA:</strong> 3.07 out of 4.00</p>
                    </div>
                    
                    <h3 style="margin-top: 40px;">Achievements & Awards</h3>
                    <div class="achievement-card" style="margin-top: 20px;">
                        <p>Certificate of Completion for Salesforce Training conducted by "Inovi Solution"</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="experience">
        <div class="container">
            <h2 class="section-title">Work Experience</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h4>Jr. SQA Engineer</h4>
                        <span class="date">EWN Bangladesh Limited | June 2023 - April 2025</span>
                        <p>Conducted extensive manual and automated testing for various web and mobile applications. Collaborated closely with development teams, actively participating in bug analysis meetings to discuss and prioritize identified issues for rapid resolution.</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h4>Project Associate (QC) - Part Time</h4>
                        <span class="date">Quantanite | December 2022</span>
                        <p>Verified accuracy and completeness of data entered into databases or systems. Conducted quality checks on data entry processes to identify errors or inconsistencies. Identified and corrected errors in data entry including typographical errors, formatting issues, and inaccuracies.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <h2 class="section-title">Projects & Work Experience</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-header">
                        <h3>KFUIMS</h3>
                        <div class="project-type">King Fahad University Learning Management System (Web)</div>
                    </div>
                    <div class="project-body">
                        <p>Comprehensive learning management system for King Fahad University with extensive testing to ensure functionality, usability, and performance.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Manual Testing</span>
                            <span class="tech-tag">Automation Testing</span>
                            <span class="tech-tag">Web Application</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-header">
                        <h3>Opus (Jobseeker)</h3>
                        <div class="project-type">Mobile Apps & Web</div>
                    </div>
                    <div class="project-body">
                        <p>Job seeking platform tested across mobile and web interfaces to ensure seamless user experience and functionality.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Mobile Testing</span>
                            <span class="tech-tag">Android & iOS</span>
                            <span class="tech-tag">Web Testing</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-header">
                        <h3>Limo</h3>
                        <div class="project-type">Ride Sharing Apps</div>
                    </div>
                    <div class="project-body">
                        <p>Ride-sharing application tested for performance, usability, and reliability under various conditions.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Mobile Testing</span>
                            <span class="tech-tag">Performance Testing</span>
                            <span class="tech-tag">Usability Testing</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-header">
                        <h3>Itmaan</h3>
                        <div class="project-type">Mobile Apps & Web</div>
                    </div>
                    <div class="project-body">
                        <p>Platform connecting businesses with freelancers offering digital services, tested across multiple platforms.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Cross-platform Testing</span>
                            <span class="tech-tag">API Testing</span>
                            <span class="tech-tag">Postman</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-header">
                        <h3>PetPat</h3>
                        <div class="project-type">Online service and grocery delivery platform for pets</div>
                    </div>
                    <div class="project-body">
                        <p>E-commerce platform for pet services and products, tested for functionality, payment processing, and user experience.</p>
                        <div class="project-tech">
                            <span class="tech-tag">E-commerce Testing</span>
                            <span class="tech-tag">Payment Gateway</span>
                            <span class="tech-tag">User Experience</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Languages & Reference Section -->
    <section id="languages" class="languages">
        <div class="container">
            <h2 class="section-title">Languages & Reference</h2>
            <div class="languages-achievements">
                <div>
                    <h3 style="margin-bottom: 20px; color: var(--dark);">Languages</h3>
                    <div class="languages-list">
                        <div class="language-item">
                            <span class="language-name">English</span>
                            <span class="language-level">Professional Proficiency</span>
                        </div>
                        <div class="language-item">
                            <span class="language-name">Bangla</span>
                            <span class="language-level">Native</span>
                        </div>
                    </div>
                </div>
                
                <div>
                    <h3 style="margin-bottom: 20px; color: var(--dark);">Reference</h3>
                    <div class="achievement-card">
                        <h3>Hossain Al Ikram</h3>
                        <p><strong>QA Lead | EWN Bangladesh Limited</strong></p>
                        <p>Email: ikram@ewnbd.com</p>
                        <p>Phone: 01735830528</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Contact Information</h3>
                    <div class="contact-details">
                        <div class="contact-detail">
                            <div class="contact-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <h4>Phone</h4>
                                <p>01317770923</p>
                            </div>
                        </div>
                        <div class="contact-detail">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h4>Email</h4>
                                <p>mehedisohaan@gmail.com</p>
                            </div>
                        </div>
                        <div class="contact-detail">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h4>Address</h4>
                                <p>Uttor Badda, Linkroad, Dhaka</p>
                            </div>
                        </div>
                        <div class="contact-detail">
                            <div class="contact-icon">
                                <i class="fab fa-linkedin"></i>
                            </div>
                            <div>
                                <h4>LinkedIn</h4>
                                <p>linkedin.com/in/mehedi-hassan-sohaan-72b706117/</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form id="contactForm">
                        <input type="text" placeholder="Your Name" required>
                        <input type="email" placeholder="Your Email" required>
                        <input type="text" placeholder="Subject" required>
                        <textarea placeholder="Your Message" rows="5" required></textarea>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <div class="footer-logo">Mehedi<span style="color: var(--secondary);">Hassan</span></div>
                    <p>SQA Engineer with expertise in manual and automated testing, mobile app testing, and quality assurance processes.</p>
                    <div class="social-links">
                        <a href="https://www.linkedin.com/in/mehedi-hassan-sohaan-72b706117/" target="_blank"><i class="fab fa-linkedin-in"></i></a>
                        <a href="mailto:mehedisohaan@gmail.com"><i class="fas fa-envelope"></i></a>
                        <a href="tel:01317770923"><i class="fas fa-phone"></i></a>
                    </div>
                </div>
                <div class="footer-links">
                    <h4>Quick Links</h4>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#experience">Experience</a></li>
                        <li><a href="#projects">Projects</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-contact">
                    <h4>Contact Info</h4>
                    <p><i class="fas fa-map-marker-alt" style="margin-right: 10px;"></i> Uttor Badda, Linkroad, Dhaka</p>
                    <p><i class="fas fa-phone" style="margin-right: 10px;"></i> 01317770923</p>
                    <p><i class="fas fa-envelope" style="margin-right: 10px;"></i> mehedisohaan@gmail.com</p>
                </div>
            </div>
            <div class="copyright">
                &copy; 2025 Mehedi Hassan. All rights reserved.
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const menuToggle = document.getElementById('menuToggle');
        const navLinks = document.getElementById('navLinks');
        
        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Close menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });

        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! I will get back to you soon.');
            this.reset();
        });

        // Smooth scroll for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Add active class to nav links on scroll
        window.addEventListener('scroll', () => {
            let current = '';
            const sections = document.querySelectorAll('section');
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if(pageYOffset >= (sectionTop - 100)) {
                    current = section.getAttribute('id');
                }
            });
            
            document.querySelectorAll('.nav-links a').forEach(link => {
                link.classList.remove('active');
                if(link.getAttribute('href') === `#${current}`) {
                    link.classList.add('active');
                }
            });
        });

        // Load photo after page loads
        window.addEventListener('load', function() {
            const profileContainer = document.querySelector('.profile-img-container');
            const placeholder = document.querySelector('.profile-placeholder');
            
            // Try to load the photo
            const img = new Image();
            img.src = 'MH.png';
            img.alt = 'Mehedi Hassan';
            img.className = 'profile-img';
            
            img.onload = function() {
                // Replace placeholder with actual photo
                placeholder.style.display = 'none';
                profileContainer.appendChild(img);
            };
            
            img.onerror = function() {
                // If photo fails to load, keep the placeholder
                console.log('Photo not found. Using placeholder instead.');
            };
        });
    </script>
</body>
</html>
