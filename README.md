<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hotel 0771 - Changurabhata, Kushapur Chowk</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: #fff;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #ffd700;
        }

        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%23667eea" width="1200" height="600"/><circle fill="%23ffd700" opacity="0.1" cx="300" cy="200" r="200"/><circle fill="%23764ba2" opacity="0.1" cx="900" cy="400" r="150"/></svg>');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease-out;
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .cta-button {
            display: inline-block;
            background: #ffd700;
            color: #333;
            padding: 1rem 2.5rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s;
            animation: fadeInUp 1s ease-out 0.4s both;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(255,215,0,0.4);
        }

        /* Sections */
        section {
            padding: 5rem 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        /* About */
        .about {
            background: #f8f9fa;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text p {
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
            color: #666;
        }

        .address-box {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            text-align: center;
        }

        .address-box i {
            font-size: 2rem;
            color: #667eea;
            margin-bottom: 1rem;
        }

        /* Rooms */
        .rooms-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .room-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .room-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0,0,0,0.15);
        }

        .room-image {
            height: 250px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 4rem;
        }

        .room-info {
            padding: 2rem;
        }

        .room-info h3 {
            margin-bottom: 1rem;
            color: #333;
        }

        .room-price {
            font-size: 1.5rem;
            font-weight: 700;
            color: #ffd700;
            margin: 1rem 0;
        }

        /* Gallery */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .gallery-item {
            height: 250px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        /* Contact */
        .contact {
            background: #333;
            color: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .contact-item i {
            background: #667eea;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
        }

        .contact-form {
            background: rgba(255,255,255,0.1);
            padding: 2.5rem;
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: none;
            border-radius: 10px;
            background: rgba(255,255,255,0.9);
            font-family: inherit;
        }

        .form-group textarea {
            height: 120px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background: #222;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }

            .nav-links {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background: #667eea;
                flex-direction: column;
                justify-content: flex-start;
                align-items: center;
                padding-top: 2rem;
                transition: 0.3s;
            }

            .nav-links.active {
                left: 0;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            section {
                padding: 3rem 0;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">
                <i class="fas fa-hotel"></i> Hotel Paradise
            </div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#rooms">Rooms</a></li>
                <li><a href="#gallery">Gallery</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="menu-toggle">
                <i class="fas fa-bars"></i>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Welcome to Hotel Paradise</h1>
            <p>Your Home Away From Home in Changurabhata</p>
            <a href="#rooms" class="cta-button">Book Now</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2>About Us</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Hotel Paradise offers comfortable accommodation and excellent hospitality in the heart of Changurabhata. We provide a perfect blend of modern amenities and traditional warmth.</p>
                    <p>Our hotel is strategically located beside Dhelabai Chatrwas at Kushapur Chowk, making it easily accessible and convenient for all travelers.</p>
                    <p>Whether you're here for business or pleasure, we ensure a memorable stay with our clean rooms, friendly service, and delicious food.</p>
                </div>
                <div class="address-box">
                    <i class="fas fa-map-marker-alt"></i>
                    <h3>Our Location</h3>
                    <p><strong>Changurabhata, Kushapur Chowk</strong><br>
                    Beside Dhelabai Chatrwas<br>
                    <i class="fas fa-phone"></i> +91 12345 67890<br>
                    <i class="fas fa-envelope"></i> info@hotelparadise.com</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Rooms Section -->
    <section id="rooms">
        <div class="container">
            <h2>Our Rooms</h2>
            <div class="rooms-grid">
                <div class="room-card">
                    <div class="room-image">
                        <i class="fas fa-bed"></i>
                    </div>
                    <div class="room-info">
                        <h3>Standard Room</h3>
                        <p>Comfortable room with AC, TV, and modern amenities. Perfect for solo travelers or couples.</p>
                        <div class="room-price">₹1500/night</div>
                        <a href="#contact" class="cta-button" style="font-size: 0.9rem; padding: 0.7rem 1.5rem;">Book Now</a>
                    </div>
                </div>
                <div class="room-card">
                    <div class="room-image">
                        <i class="fas fa-bed-double"></i>
                    </div>
                    <div class="room-info">
                        <h3>Deluxe Room</h3>
                        <p>Spacious room with king-size bed, balcony, and premium amenities for a luxurious stay.</p>
                        <div class="room-price">₹2200/night</div>
                        <a href="#contact" class="cta-button" style="font-size: 0.9rem; padding: 0.7rem 1.5rem;">Book Now</a>
                    </div>
                </div>
                <div class="room-card">
                    <div class="room-image">
                        <i class="fas fa-users"></i>
                    </div>
                    <div class="room-info">
                        <h3>Family Suite</h3>
                        <p>Large suite perfect for families with 2 bedrooms, living area, and kitchenette.</p>
                        <div class="room-price">₹3500/night</div>
                        <a href="#contact" class="cta-button" style="font-size: 0.9rem; padding: 0.7rem 1.5rem;">Book Now</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="about">
        <div class="container">
            <h2>Gallery</h2>
            <div class="gallery-grid">
                <div class="gallery-item"><i class="fas fa-camera"></i></div>
                <div class="gallery-item"><i class="fas fa-bed"></i></div>
                <div class="gallery-item"><i class="fas fa-utensils"></i></div>
                <div class="gallery-item"><i class="fas fa-swimming-pool"></i></div>
                <div class="gallery-item"><i class="fas fa-wifi"></i></div>
                <div class="gallery-item"><i class="fas fa-parking"></i></div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2>Contact Us</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>
                            <h4>Address</h4>
                            <p>Changurabhata, Kushapur Chowk<br>Beside Dhelabai Chatrwas</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <div>
                            <h4>Phone</h4>
                            <p>+91 12345 67890<br>+91 98765 43210</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-clock"></i>
                        <div>
                            <h4>Hours</h4>
                            <p>24/7 Open<br>Check-in: 12 PM<br>Check-out: 11 AM</p>
                        </div>
                    </div>
                </div>
                <form class="contact-form">
                    <div class="form-group">
                        <input type="text" placeholder="Your Name" required>
                    </div>
                    <div class="form-group">
                        <input type="email" placeholder="Your Email" required>
                    </div>
                    <div class="form-group">
                        <input type="tel" placeholder="Phone Number">
                    </div>
                    <div class="form-group">
                        <textarea placeholder="Your Message" required></textarea>
                    </div>
                    <button type="submit" class="cta-button" style="width: 100%; background: #ffd700; color: #333; border: none;">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2024 Hotel Paradise. Changurabhata, Kushapur Chowk. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const menuToggle = document.querySelector('.menu-toggle');
        const navLinks = document.querySelector('.nav-links');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Smooth scrolling
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
                navLinks.classList.remove('active');
            });
        });

        // Form submission
        document.querySelector('.contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! We will contact you soon.');
            this.reset();
        });

        // Navbar background on scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(102, 126, 234, 0.95)';
                header.style.backdropFilter = 'blur(10px)';
            } else {
                header.style.background = 'linear-gradient(135deg, #667eea
