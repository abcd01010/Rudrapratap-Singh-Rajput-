<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ITI Government College Khilchipur – COPA Department</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: "Segoe UI", Arial, sans-serif;
            background: #eef2f5;
            color: #222;
            line-height: 1.6;
        }

        /* Header / Hero Section */
        .hero {
            background: linear-gradient(to bottom right, #1666d3, #4ea1ff);
            color: #fff;
            padding: 80px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%230066cc" fill-opacity="0.1" d="M0,96L48,112C96,128,192,160,288,186.7C384,213,480,235,576,213.3C672,192,768,128,864,128C960,128,1056,192,1152,192C1248,192,1344,128,1392,96L1440,64L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
            background-size: cover;
            background-position: center;
        }

        .hero-content {
            position: relative;
            z-index: 1;
        }

        .hero h1 {
            margin: 0;
            font-size: 42px;
            letter-spacing: 1px;
            margin-bottom: 15px;
        }

        .hero p {
            font-size: 18px;
            margin-top: 10px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        /* Navigation */
        nav {
            background: #fff;
            padding: 12px;
            display: flex;
            justify-content: center;
            gap: 18px;
            border-bottom: 1px solid #ddd;
            position: sticky;
            top: 0;
            z-index: 10;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav a {
            text-decoration: none;
            color: #1666d3;
            font-weight: 600;
            padding: 8px 15px;
            border-radius: 4px;
            transition: all 0.3s ease;
        }

        nav a:hover {
            color: #0c47a3;
            background-color: #f0f7ff;
        }

        /* Sections */
        section {
            padding: 40px 25px;
            max-width: 1000px;
            margin: auto;
            background: #fff;
            border-radius: 10px;
            margin-top: 30px;
            box-shadow: 0px 4px 15px rgba(0,0,0,0.1);
            animation: fadeIn 0.5s ease;
        }

        h2 {
            text-align: center;
            color: #1666d3;
            margin-top: 0;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        h2::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: #1666d3;
            border-radius: 2px;
        }

        ul {
            line-height: 1.7;
            padding-left: 20px;
        }

        /* Cards */
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
            gap: 20px;
            margin-top: 25px;
        }

        .card {
            background: #f7faff;
            padding: 20px;
            border-radius: 8px;
            text-align: center;
            border: 1px solid #d7e4f7;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .card h3 {
            color: #1666d3;
            margin-bottom: 10px;
        }

        /* Gallery */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .gallery-item {
            height: 150px;
            background: #f0f7ff;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #1666d3;
            font-weight: 600;
            border: 1px dashed #1666d3;
        }

        /* Contact Form */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-top: 20px;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .contact-item i {
            color: #1666d3;
            font-size: 18px;
            width: 20px;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: inherit;
        }

        .contact-form button {
            background: #1666d3;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 600;
            transition: background 0.3s ease;
        }

        .contact-form button:hover {
            background: #0c47a3;
        }

        /* Footer */
        .footer {
            margin-top: 40px;
            background: #1666d3;
            padding: 25px 15px;
            text-align: center;
            color: #fff;
        }

        .footer-content {
            max-width: 1000px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            text-align: left;
        }

        .footer-section h3 {
            margin-bottom: 15px;
            font-size: 18px;
        }

        .footer-section a {
            color: #fff;
            text-decoration: none;
            display: block;
            margin-bottom: 8px;
        }

        .footer-section a:hover {
            text-decoration: underline;
        }

        .copyright {
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.2);
        }

        /* Back to Top Button */
        .back-to-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #1666d3;
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: 99;
        }

        .back-to-top.visible {
            opacity: 1;
        }

        /* Animations */
        @keyframes fadeIn {
            from {opacity: 0;}
            to {opacity: 1;}
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 32px;
            }
            
            nav {
                flex-wrap: wrap;
            }
            
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
        }
    </style>
</head>

<body>

<div class="hero">
    <div class="hero-content">
        <h1>ITI Government College Khilchipur</h1>
        <p>Creative learning for the next generation of COPA students</p>
    </div>
</div>

<nav>
    <a href="#home">Home</a>
    <a href="#copa">About COPA</a>
    <a href="#facilities">Facilities</a>
    <a href="#projects">Projects</a>
    <a href="#gallery">Gallery</a>
    <a href="#contact">Contact</a>
</nav>

<section id="home">
    <h2>Welcome</h2>
    <p>
        Our college provides a strong platform for skill-based education.  
        Students in the COPA department learn practical computer skills, programming basics and digital tools that help build careers in IT and office environments.
    </p>

    <div class="cards">
        <div class="card">
            <h3>Practical Training</h3>
            <p>Hands-on learning with real tools and updated software.</p>
        </div>

        <div class="card">
            <h3>Creative Skills</h3>
            <p>Website building, digital documents, design tasks and more.</p>
        </div>

        <div class="card">
            <h3>Industry Ready</h3>
            <p>Skills that prepare students for jobs and internships.</p>
        </div>
    </div>
</section>

<section id="copa">
    <h2>About COPA Trade</h2>
    <p>Students learn topics such as:</p>
    <ul>
        <li>Computer fundamentals and hardware basics</li>
        <li>MS Office (Word, Excel, PowerPoint) with advanced features</li>
        <li>Typing practice and accuracy improvement</li>
        <li>Internet browsing, email, online services</li>
        <li>HTML, CSS and simple Python programs</li>
        <li>Database basics</li>
        <li>Practical assignments and real projects</li>
    </ul>
</section>

<section id="facilities">
    <h2>Facilities</h2>
    <div class="cards">
        <div class="card"><h3>Computer Lab</h3><p>Modern systems with smooth performance.</p></div>
        <div class="card"><h3>Smart Classroom</h3><p>Projector-based teaching for better understanding.</p></div>
        <div class="card"><h3>Fast Internet</h3><p>High-speed connectivity for online learning.</p></div>
        <div class="card"><h3>Updated Software</h3><p>Regular updates and new tools for students.</p></div>
    </div>
</section>

<section id="projects">
    <h2>Student Projects</h2>
    <ul>
        <li>Portfolio websites</li>
        <li>Python mini apps</li>
        <li>Excel sheet automation</li>
        <li>Digital posters and presentations</li>
        <li>Database mini projects</li>
    </ul>
</section>

<section id="gallery">
    <h2>Gallery</h2>
    <p>Photos of students working on assignments, events and practical labs.</p>
    
    <div class="gallery-grid">
        <div class="gallery-item">Lab Session</div>
        <div class="gallery-item">Project Exhibition</div>
        <div class="gallery-item">Classroom</div>
        <div class="gallery-item">Student Work</div>
        <div class="gallery-item">Events</div>
        <div class="gallery-item">Workshops</div>
    </div>
</section>

<section id="contact">
    <h2>Contact</h2>
    
    <div class="contact-container">
        <div class="contact-info">
            <div class="contact-item">
                <i class="fas fa-map-marker-alt"></i>
                <div>
                    <strong>Address:</strong><br>
                    ITI Government College Khilchipur,<br>
                    Madhya Pradesh
                </div>
            </div>
            
            <div class="contact-item">
                <i class="fas fa-envelope"></i>
                <div>
                    <strong>Email:</strong><br>
                    official@example.com
                </div>
            </div>
            
            <div class="contact-item">
                <i class="fas fa-phone"></i>
                <div>
                    <strong>Phone:</strong><br>
                    +91-XXXXXXXXXX
                </div>
            </div>
        </div>
        
        <div class="contact-form">
            <h3>Send us a message</h3>
            <form>
                <input type="text" placeholder="Your Name" required>
                <input type="email" placeholder="Your Email" required>
                <textarea rows="5" placeholder="Your Message" required></textarea>
                <button type="submit">Send Message</button>
            </form>
        </div>
    </div>
</section>

<div class="footer">
    <div class="footer-content">
        <div class="footer-section">
            <h3>Quick Links</h3>
            <a href="#home">Home</a>
            <a href="#copa">About COPA</a>
            <a href="#facilities">Facilities</a>
            <a href="#projects">Projects</a>
        </div>
        
        <div class="footer-section">
            <h3>Contact Info</h3>
            <a href="mailto:official@example.com">official@example.com</a>
            <a href="tel:+91-XXXXXXXXXX">+91-XXXXXXXXXX</a>
            <a href="#">ITI Government College Khilchipur</a>
        </div>
        
        <div class="footer-section">
            <h3>Follow Us</h3>
            <a href="#"><i class="fab fa-facebook"></i> Facebook</a>
            <a href="#"><i class="fab fa-twitter"></i> Twitter</a>
            <a href="#"><i class="fab fa-instagram"></i> Instagram</a>
        </div>
    </div>
    
    <div class="copyright">
        © 2025 ITI Government College Khilchipur – COPA Department
    </div>
</div>

<div class="back-to-top" id="backToTop">
    <i class="fas fa-arrow-up"></i>
</div>

<script>
    // Back to top button functionality
    const backToTopButton = document.getElementById('backToTop');
    
    window.addEventListener('scroll', () => {
        if (window.pageYOffset > 300) {
            backToTopButton.classList.add('visible');
        } else {
            backToTopButton.classList.remove('visible');
        }
    });
    
    backToTopButton.addEventListener('click', () => {
        window.scrollTo({
            top: 0,
            behavior: 'smooth'
        });
    });
    
    // Smooth scrolling for navigation links
    document.querySelectorAll('nav a').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
            e.preventDefault();
            
            const targetId = this.getAttribute('href');
            const targetElement = document.querySelector(targetId);
            
            window.scrollTo({
                top: targetElement.offsetTop - 20,
                behavior: 'smooth'
            });
        });
    });
</script>

</body>
</html>
