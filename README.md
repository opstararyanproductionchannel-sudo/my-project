<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hotel 0771 - Changurabhata, Kushalpur Chowk</title>
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
            background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
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
            font-size: 2rem;
            font-weight: 700;
            color: #fff;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2.5rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: #f39c12;
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-links a:hover {
            color: #f39c12;
        }

        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(44,62,80,0.85), rgba(52,152,219,0.85)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 700"><defs><radialGradient id="bg" cx="50%" cy="50%"><stop offset="0%" stop-color="%232c3e50"/><stop offset="70%" stop-color="%233498db"/><stop offset="100%" stop-color="%231a252f"/></radialGradient></defs><rect width="1200" height="700" fill="url(%23bg)"/><circle fill="%23f39c12" opacity="0.2" cx="200" cy="150" r="250"/><circle fill="%23e74c" opacity="0.15" cx="1000" cy="500" r="200"/><circle fill="%23349 8db" opacity="0.1" cx="600" cy="300" r="150"/></svg>');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 0;
        }

        .hero-content h1 {
            font-size: 4rem;
            margin-bottom: 1.5rem;
            animation: fadeInUp 1s ease-out;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero-content p {
            font-size: 1.4rem;
            margin-bottom: 2.5rem;
            animation: fadeInUp 1s ease-out 0.2s both;
            max-width: 600px;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #f39c12, #e67e22);
            color: white;
            padding: 1.2rem 3rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.2rem;
            transition: all 0.3s ease;
            box-shadow: 0 8px 25px rgba(243,156,18,0.3);
            animation: fadeInUp 1s ease-out 0.4s both;
            border: none;
            cursor: pointer;
        }

        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(243,156,18,0.4);
        }

        /* Sections */
        section {
            padding: 6rem 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        h2 {
            text-align: center;
            font-size: 3rem;
            margin-bottom: 3.5rem;
            color: #2c3e50;
            position: relative;
        }

        h2::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background: linear-gradient(45deg, #f39c12, #e67e22);
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }

        /* About */
        .about {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
            align-items: center;
        }

        .about-text p {
            font-size: 1.2rem;
            margin-bottom: 1.8rem;
            color: #555;
            line-height: 1.8;
        }

        .address-box {
            background: white;
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.1);
            text-align: center;
            border: 2px solid #f8f9fa;
            transition: all 0.3s ease;
        }

        .address-box:hover {
            transform: translateY(-10px);
            box-shadow: 0 30px 80px rgba(0,0,0,0.15);
        }

        .address-box i {
            font-size: 3rem;
            color: #3498db;
            margin-bottom: 1.5rem;
            display: block;
        }

        .address-box h3 {
            color: #2c3e50;
            margin-bottom: 1.5rem;
            font-size: 1.5rem;
        }

        /* Rooms */
        .rooms-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
            gap: 2.5rem;
        }

        .room-card {
            background: white;
            border-radius: 25px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0,0,0,0.1);
            transition: all 0.4s ease;
            border: 1px solid #f8f9fa;
        }

        .room-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 35px 80px rgba(0,0,0,0.15);
        }

        .room-image {
            height: 280px;
            background: linear-gradient(135deg, #3498db, #2980b9);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 4.5rem;
        }

        .room-info {
            padding: 2.5rem;
        }

        .room-info h3 {
            margin-bottom: 1rem;
            color: #2c3e50;
            font-size: 1.8rem;
        }

        .room-features {
            color: #7f8c8d;
            margin: 1.5rem 0;
            font-size: 0.95rem;
        }

        .room-price {
            font-size: 2rem;
            font-weight: 700;
            color: #f39c12;
            margin: 1.5rem 0;
        }

        /* Gallery */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .gallery-item {
            height: 280px;
            background: linear-gradient(135deg, #3498db, #2980b9);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3.5rem;
            cursor: pointer;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .gallery-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: left 0.5s;
        }

        .gallery-item:hover::before {
            left: 100%;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        /* Contact */
        .contact {
            background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);
            color: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 2.5rem;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 1.5rem;
        }

        .contact-item i {
            background: linear-gradient(45deg, #f39c12, #e67e22);
            width: 60px;
            height: 60px;
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.4rem;
            flex-shrink: 0;
            margin-top: 5px;
        }

        .contact-form {
            background: rgba(255,255,255,0.1);
            padding: 3rem;
            border-radius: 25px;
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255,255,255,0.2);
        }

        .form-group {
            margin-bottom: 2rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1.2rem;
            border: none;
            border-radius: 15px;
            background: rgba(255,255,255,0.95);
            font-family: inherit;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            box-shadow: 0 0 0 3px rgba(243,156,18,0.2);
            background: white;
        }

        .form-group textarea {
            height: 140px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background: #1a252f;
            color: #bdc3c7;
            text-align: center;
            padding: 3rem 0;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(40px);
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
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
                flex-direction: column;
                justify-content: flex-start;
                align-items: center;
                padding-top: 3rem;
                transition: 0.4s;
            }

            .nav-links.active {
                left: 0;
            }

            .hero-content h1 {
                font-size: 2.8rem;
            }

            .hero-content p {
                font-size: 1.2rem;
            }

            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
                gap: 3rem;
            }

            section {
                padding: 4rem 0;
            }

            h2 {
                font-size: 2.2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">
                <i class="fas fa-hotel"></i> Hotel 0771
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
            <h1>Welcome to Hotel 0771</h1>
            <p>Comfortable stay at Changurabhata, Kushalpur Chowk. Beside Dhelabai Chatrwas. Your perfect home away from home!</p>
            <a href="#rooms" class="cta-button">View Rooms</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2>About Hotel 0771</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Hotel 0771 offers comfortable and affordable accommodation in the heart of Changurabhata. Strategically located beside Dhelabai Chatrwas at Kushalpur Chowk, we provide easy access to all major locations.</p>
                    <p>Our hotel features 4 Deluxe AC Rooms and comfortable Non-AC rooms with modern amenities, clean environment, and friendly service. Perfect for business travelers, families, and tourists.</p>
                    <p>Experience Chhattisgarh hospitality with 24/7 service, delicious home-cooked meals, and excellent value for money.</p>
                </div>
                <div class="address-box">
                    <i class="fas fa-map-marker-alt"></i>
                    <h3>Visit Us</h3>
                    <p><strong>Changurabhata, Kushalpur Chowk</strong><br>
                    Beside Dhelabai Chatrwas<br>
                    Raipur, Chhattisgarh<br>
                    <i class="fas fa-phone" style="color: #3498db; margin: 0.5rem 0;"></i> 
                    <strong>+91 94790 2907</strong></p>
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
                        <i class="fas fa-snowflake"></i>
                    </div>
                    <div class="room-info">
                        <h3>Deluxe AC Room</h3>
                        <p>Luxurious AC room with modern amenities. We have <strong>4 Deluxe AC Rooms</strong> available.</p>
                        <ul class="room-features">
                            <li><i class="fas fa-check"></i> Air Conditioning</li>
                            <li><i class="fas fa-tv"></i> LED TV</li>
                            <li><i class="fas fa-bed"></i> Comfortable Bedding</li>
                            <li><i class="fas fa-wifi"></i> Free WiFi</li>
                        </ul>
                        <div class="room-price">₹1500/night</div>
                        <a href="#contact" class="cta-button" style="font-size: 1rem; padding: 0.9rem 2rem;">Book Now</a>
                    </div>
                </div>
                <div class="room-card">
                    <div class="room-image">
                        <i class="fas fa-bed"></i>
                    </div>
                    <div class="room-info">
                        <h3>Standard Non-AC Room</h3>
                        <p>Clean and comfortable non-AC room perfect for budget travelers.</p>
                        <ul class="room-features">
                            <li><i class="fas fa-fan"></i> Ceiling Fan</li>
                            <li><i class="fas fa-tv"></i> LED TV</li>
                            <li><i class="fas fa-bed"></i> Comfortable Bedding</li>
                            <li><i class="fas fa-wifi"></i> Free WiFi</li>
                        </ul>
                        <div class="
