<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hotel 0771 | Premium Accommodation | Changurabhata, Kushalpur Chowk</title>
    <meta name="description" content="Hotel 0771 - 4 Deluxe AC Rooms (₹1500) & Non-AC Rooms (₹1000). Located at Changurabhata, Kushalpur Chowk beside Dhelabai Chatrwas, Raipur. Book your stay now!">
    <meta name="keywords" content="Hotel 0771, Changurabhata, Kushalpur Chowk, Raipur hotel, AC rooms, budget hotel">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #1e40af;
            --primary-dark: #1e3a8a;
            --secondary: #3b82f6;
            --accent: #f59e0b;
            --accent-dark: #d97706;
            --dark: #111827;
            --gray-900: #111827;
            --gray-800: #1f2937;
            --gray-700: #374151;
            --gray-600: #4b5563;
            --gray-500: #6b7280;
            --gray-200: #e5e7eb;
            --gray-100: #f3f4f6;
            --white: #ffffff;
            --shadow-lg: 0 20px 25px -5px rgba(0, 0,0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
            --shadow-xl: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
            --border-radius: 16px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.7;
            color: var(--gray-700);
            background: var(--white);
            overflow-x: hidden;
        }

        /* ===========================================
           HEADER & NAVIGATION
        =========================================== */
        .header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            z-index: 1000;
            box-shadow: 0 10px 40px -10px rgba(0, 0, 0, 0.1);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .nav-container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 1.875rem;
            font-weight: 800;
            color: var(--primary);
            text-decoration: none;
            letter-spacing: -0.05em;
        }

        .logo i {
            font-size: 2.25rem;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 3rem;
            align-items: center;
        }

        .nav-link {
            color: var(--gray-700);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            letter-spacing: 0.025em;
            position: relative;
            transition: all 0.3s ease;
            padding: 0.5rem 0;
        }

        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 3px;
            bottom: 0;
            left: 50%;
            background: linear-gradient(135deg, var(--accent), var(--accent-dark));
            transition: all 0.3s ease;
            border-radius: 2px;
        }

        .nav-link:hover::after,
        .nav-link.active::after {
            width: 100%;
            left: 0;
        }

        .nav-link:hover {
            color: var(--primary);
        }

        .mobile-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--gray-700);
            cursor: pointer;
            padding: 0.5rem;
        }

        /* ===========================================
           HERO SECTION
        =========================================== */
        .hero {
            min-height: 100vh;
            background: linear-gradient(135deg, 
                rgba(30, 64, 175, 0.95) 0%, 
                rgba(59, 130, 246, 0.9) 50%,
                rgba(16, 185, 129, 0.85) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--white);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><radialGradient id="a" cx="50%" cy="50%"><stop offset="0%" stop-color="%23ffffff" stop-opacity="0.1"/><stop offset="100%" stop-color="%23ffffff" stop-opacity="0"/></radialGradient></defs><circle cx="20" cy="20" r="10" fill="url(%23a)"><animate attributeName="r" values="10;15;10" dur="3s" repeatCount="indefinite"/></circle><circle cx="80" cy="80" r="8" fill="url(%23a)"><animate attributeName="r" values="8;12;8" dur="4s" repeatCount="indefinite"/></circle></svg>');
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .hero-content {
            max-width: 900px;
            padding: 0 2rem;
            position: relative;
            z-index: 2;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            padding: 0.5rem 1.5rem;
            border-radius: 50px;
            font-size: 0.875rem;
            font-weight: 600;
            letter-spacing: 0.05em;
            margin-bottom: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .hero-title {
            font-size: clamp(3rem, 6vw, 5rem);
            font-weight: 800;
            margin-bottom: 1.5rem;
            letter-spacing: -0.02em;
            line-height: 1.1;
        }

        .hero-subtitle {
            font-size: 1.375rem;
            margin-bottom: 3rem;
            opacity: 0.95;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn-primary {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            background: linear-gradient(135deg, var(--accent) 0%, var(--accent-dark) 100%);
            color: var(--dark);
            padding: 1.25rem 3rem;
            text-decoration: none;
            border-radius: var(--border-radius);
            font-weight: 600;
            font-size: 1.125rem;
            box-shadow: 0 20px 40px rgba(245, 158, 11, 0.4);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            border: none;
        }

        .btn-primary:hover {
            transform: translateY(-4px);
            box-shadow: 0 30px 60px rgba(245, 158, 11, 0.5);
        }

        .btn-secondary {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            color: var(--white);
            padding: 1.125rem 2.5rem;
            text-decoration: none;
            border-radius: var(--border-radius);
            font-weight: 500;
            font-size: 1rem;
            border: 2px solid rgba(255, 255, 255, 0.3);
            transition: all 0.3s ease;
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-2px);
        }

        /* ===========================================
           CONTAINER & SECTIONS
        =========================================== */
        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .section {
            padding: 8rem 0;
        }

        .section-title {
            text-align: center;
            font-size: clamp(2.25rem, 5vw, 3.5rem);
            font-weight: 800;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 4.5rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 5px;
            background: linear-gradient(135deg, var(--accent), var(--accent-dark));
            bottom: -25px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 3px;
        }

        /* ===========================================
           ABOUT SECTION
        =========================================== */
        .about-section {
            background: linear-gradient(135deg, var(--gray-100) 0%, var(--white) 100%);
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 6rem;
            align-items: center;
        }

        .about-content {
            font-size: 1.125rem;
            line-height: 1.8;
        }

        .about-content p {
            color: var(--gray-600);
            margin-bottom: 1.75rem;
        }

        .about-highlight {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-weight: 700;
        }

        .location-card {
            background: var(--white);
            padding: 3.5rem 3rem;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-xl);
            text-align: center;
            border: 1px solid var(--gray-100);
            position: relative;
            overflow: hidden;
        }

        .location-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(135deg, var(--accent), var(--accent-dark));
        }

        .location-icon {
            font-size: 4rem;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 2rem;
            display: block;
        }

        .location-title {
            font-size: 1.75rem;
            font-weight: 700;
            color: var(--gray-900);
            margin-bottom: 1.5rem;
        }

        .location-address {
            color: var(--gray-600);
            font-size: 1.1rem;
            line-height: 1.7;
            margin-bottom: 2rem;
        }

        .phone-link {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--accent);
            text-decoration: none;
            padding: 1rem 2rem;
            background: rgba(245, 158, 11, 0.1);
            border-radius: 12px;
            transition: all 0.3s ease;
        }

        .phone-link:hover {
            background: rgba(245, 158, 11, 0.2);
            transform: translateY(-2px);
        }

        /* ===========================================
           ROOMS SECTION
        =========================================== */
        .rooms-grid {
            display:
