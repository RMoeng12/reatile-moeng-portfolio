<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reatile Moeng | SA Developer & Automation Specialist</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #002366;
            --secondary: #FFD700;
            --accent: #FF6600;
            --light: #f8f9fa;
            --dark: #212529;
            --gray: #6c757d;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f0f2f5;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary) 0%, #001a4d 100%);
            color: white;
            padding: 1.5rem 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--secondary);
        }
        
        .logo span {
            color: white;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--secondary);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 35, 102, 0.85), rgba(0, 26, 77, 0.9)), url('https://images.unsplash.com/photo-1499951360447-b19be8fe80f5?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') center/cover no-repeat;
            color: white;
            padding: 5rem 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .hero p {
            font-size: 1.5rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            text-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);
        }
        
        .highlight {
            color: var(--secondary);
            font-weight: 700;
        }
        
        .cta-button {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            border: 2px solid var(--accent);
            margin-top: 1rem;
        }
        
        .cta-button:hover {
            background-color: transparent;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .cta-button.secondary {
            background-color: transparent;
            border: 2px solid white;
            margin-left: 15px;
        }
        
        .cta-button.secondary:hover {
            background-color: white;
            color: var(--primary);
        }
        
        /* About Section */
        .about {
            padding: 5rem 0;
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary);
            font-size: 2.5rem;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--secondary);
            margin: 10px auto;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 3rem;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h2 {
            color: var(--primary);
            margin-bottom: 1.5rem;
            font-size: 2rem;
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .skill-tag {
            background-color: var(--primary);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* Projects Section */
        .projects {
            padding: 5rem 0;
            background-color: #f8f9fa;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2.5rem;
        }
        
        .project-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .project-image {
            height: 200px;
            overflow: hidden;
        }
        
        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .project-card:hover .project-image img {
            transform: scale(1.05);
        }
        
        .project-content {
            padding: 1.5rem;
        }
        
        .project-content h3 {
            color: var(--primary);
            margin-bottom: 0.75rem;
            font-size: 1.5rem;
        }
        
        .project-content p {
            color: var(--gray);
            margin-bottom: 1.25rem;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
        }
        
        .tech-tag {
            background-color: #e9ecef;
            color: var(--dark);
            padding: 3px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        .project-links {
            display: flex;
            gap: 1rem;
        }
        
        .project-link {
            flex: 1;
            text-align: center;
            padding: 8px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
        }
        
        .demo-link {
            background-color: var(--primary);
            color: white;
            border: 2px solid var(--primary);
        }
        
        .code-link {
            background-color: transparent;
            color: var(--primary);
            border: 2px solid var(--primary);
        }
        
        .demo-link:hover {
            background-color: #001a4d;
        }
        
        .code-link:hover {
            background-color: var(--primary);
            color: white;
        }
        
        /* Contact Section */
        .contact {
            padding: 5rem 0;
            background-color: white;
        }
        
        .contact-container {
            display: flex;
            gap: 3rem;
        }
        
        .contact-info {
            flex: 1;
        }
        
        .contact-info h3 {
            color: var(--primary);
            margin-bottom: 1.5rem;
            font-size: 1.8rem;
        }
        
        .contact-info p {
            margin-bottom: 2rem;
            font-size: 1.1rem;
        }
        
        .contact-methods {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }
        
        .contact-method {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
        }
        
        .contact-form {
            flex: 1;
            background-color: #f8f9fa;
            padding: 2rem;
            border-radius: 10px;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--dark);
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }
        
        .form-group textarea {
            min-height: 150px;
            resize: vertical;
        }
        
        .submit-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 30px;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .submit-btn:hover {
            background-color: #001a4d;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0 1.5rem;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .footer-col h4 {
            color: var(--secondary);
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-col h4::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            height: 2px;
            width: 50px;
            background-color: var(--secondary);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.75rem;
        }
        
        .footer-links a {
            color: #adb5bd;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--secondary);
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: #343a40;
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .social-link:hover {
            background-color: var(--secondary);
            color: var(--dark);
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            margin-top: 2rem;
            border-top: 1px solid #343a40;
            color: #6c757d;
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content,
            .contact-container {
                flex-direction: column;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
        }
        
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 1rem;
            }
            
            nav ul {
                justify-content: center;
            }
            
            .cta-button {
                display: block;
                margin: 10px auto;
                width: 80%;
                max-width: 300px;
            }
            
            .cta-button.secondary {
                margin-left: 0;
            }
        }
        
        @media (max-width: 576px) {
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav ul li {
                margin: 5px 10px;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">Reatile<span>Moeng</span></div>
            <nav>
                <ul>
                    <li><a href="#about">About</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Automating Efficiency for SA Businesses</h1>
            <p>I build tools that save South African companies <span class="highlight">R200k+ yearly</span> by automating manual processes and streamlining operations.</p>
            <a href="#projects" class="cta-button">View My Projects</a>
            <a href="#contact" class="cta-button secondary">Get In Touch</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <h2>Reatile Moeng</h2>
                    <p>I'm a Full-Stack Developer specializing in creating custom solutions for South African businesses. With expertise in both frontend and backend technologies, I build systems that automate manual processes, reduce operational costs, and drive efficiency.</p>
                    <p>My passion is solving uniquely South African challenges through technology - from load shedding solutions to payment integrations tailored for our market.</p>
                    <p>I believe in building tools that make a tangible difference to a company's bottom line, with a focus on measurable ROI and sustainable growth.</p>
                    
                    <h3>My Skills</h3>
                    <div class="skills">
                        <span class="skill-tag">JavaScript</span>
                        <span class="skill-tag">React</span>
                        <span class="skill-tag">Node.js</span>
                        <span class="skill-tag">Python</span>
                        <span class="skill-tag">PayFast API</span>
                        <span class="skill-tag">EskomSePush API</span>
                        <span class="skill-tag">Xero Integration</span>
                        <span class="skill-tag">Responsive Design</span>
                        <span class="skill-tag">Database Design</span>
                        <span class="skill-tag">SAAS Development</span>
                    </div>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1580894742597-87bc8789db3d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Reatile Moeng">
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                <!-- Project 1 -->
                <div class="project-card">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1613665813446-82a78c468a1d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="SolarQuote Pro">
                    </div>
                    <div class="project-content">
                        <h3>SolarQuote Pro</h3>
                        <p>An automated solar proposal system that generates accurate quotes for installers in under 5 minutes, reducing manual work by 85%.</p>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Node.js</span>
                            <span class="tech-tag">PVWatts API</span>
                            <span class="tech-tag">PDF Generation</span>
                        </div>
                        <div class="project-links">
                            <a href="https://github.com/RMoeng12/solarquote-pro" class="project-link demo-link">View Demo</a>
                            <a href="https://github.com/RMoeng12/solarquote-pro" class="project-link code-link">Source Code</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1604594849809-dfedbc827105?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="PayFast Integration Demo">
                    </div>
                    <div class="project-content">
                        <h3>PayFast Integration Suite</h3>
                        <p>A comprehensive solution for SA e-commerce businesses to easily integrate PayFast payments with custom features and reporting.</p>
                        <div class="project-tech">
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">PayFast API</span>
                            <span class="tech-tag">Express.js</span>
                            <span class="tech-tag">MongoDB</span>
                        </div>
                        <div class="project-links">
                            <a href="https://github.com/RMoeng12/payfast-demo" class="project-link demo-link">View Demo</a>
                            <a href="https://github.com/RMoeng12/payfast-demo" class="project-link code-link">Source Code</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Load Shedding Shield">
                    </div>
                    <div class="project-content">
                        <h3>Load Shedding Shield</h3>
                        <p>A real-time load shedding tracker with automated alerts and backup system recommendations tailored to South African businesses.</p>
                        <div class="project-tech">
                            <span class="tech-tag">EskomSePush API</span>
                            <span class="tech-tag">React Native</span>
                            <span class="tech-tag">Firebase</span>
                            <span class="tech-tag">Push Notifications</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link demo-link">View Demo</a>
                            <a href="#" class="project-link code-link">Source Code</a>
                        </div>
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
                    <h3>Let's Work Together</h3>
                    <p>Have a project in mind? Want to automate your business processes? Feel free to reach out and let's discuss how we can work together to create solutions that drive efficiency and growth.</p>
                    
                    <div class="contact-methods">
                        <div class="contact-method">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h4>Email</h4>
                                <p>reatile.moeng@example.com</p>
                            </div>
                        </div>
                        
                        <div class="contact-method">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h4>Location</h4>
                                <p>South Africa</p>
                            </div>
                        </div>
                        
                        <div class="contact-method">
                            <div class="contact-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <h4>Phone</h4>
                                <p>+27 12 345 6789</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" id="name" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" required></textarea>
                        </div>
                        
                        <button type="submit" class="submit-btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-col">
                    <h4>Reatile Moeng</h4>
                    <p>Full-Stack Developer specializing in creating custom solutions for South African businesses.</p>
                    <div class="social-links">
                        <a href="#" class="social-link"><i class="fab fa-github"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                
                <div class="footer-col">
                    <h4>Quick Links</h4>
                    <ul class="footer-links">
                        <li><a href="#about">About Me</a></li>
                        <li><a href="#projects">Projects</a></li>
                        <li><a href="#contact">Contact</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Services</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h4>Services</h4>
                    <ul class="footer-links">
                        <li><a href="#">Web Development</a></li>
                        <li><a href="#">API Integration</a></li>
                        <li><a href="#">Business Automation</a></li>
                        <li><a href="#">E-commerce Solutions</a></li>
                        <li><a href="#">SAAS Development</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h4>Newsletter</h4>
                    <p>Subscribe to get updates on my latest projects and articles.</p>
                    <form>
                        <div class="form-group">
                            <input type="email" placeholder="Enter your email" required>
                        </div>
                        <button type="submit" class="submit-btn">Subscribe</button>
                    </form>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 Reatile Moeng. All Rights Reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
