<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Incredible Nature | Discover the Beauty of India</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Poppins:wght@300;400;600&display=swap');
        
        :root {
            --primary: #006400;
            --accent: #FF9933;
            --light: #f8f9fa;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f4f7f4;
        }
        
        header {
            background: linear-gradient(rgba(0, 100, 0, 0.85), rgba(0, 100, 0, 0.85)), url('https://picsum.photos/id/1015/1920/1080') center/cover no-repeat;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
        }
        
        .hero-content {
            max-width: 900px;
            padding: 0 20px;
            z-index: 2;
        }
        
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 4.5rem;
            margin-bottom: 20px;
            text-shadow: 0 4px 10px rgba(0,0,0,0.6);
        }
        
        .subtitle {
            font-size: 1.8rem;
            margin-bottom: 30px;
            font-weight: 300;
        }
        
        .cta-button {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 15px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.2rem;
            transition: all 0.3s;
            box-shadow: 0 10px 20px rgba(255, 153, 51, 0.3);
        }
        
        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(255, 153, 51, 0.4);
        }
        
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255,255,255,0.95);
            z-index: 1000;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 40px;
        }
        
        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            color: var(--primary);
            font-weight: 700;
        }
        
        .nav-links a {
            margin-left: 30px;
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--accent);
        }
        
        section {
            padding: 100px 0;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 40px;
        }
        
        h2 {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            text-align: center;
            margin-bottom: 60px;
            color: var(--primary);
        }
        
        .intro {
            background: white;
            text-align: center;
            padding: 80px 20px;
        }
        
        .intro p {
            max-width: 800px;
            margin: 0 auto;
            font-size: 1.3rem;
            color: #555;
        }
        
        .destinations {
            background: #f8f9fa;
        }
        
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
            gap: 40px;
        }
        
        .card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.4s, box-shadow 0.4s;
        }
        
        .card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }
        
        .card img {
            width: 100%;
            height: 280px;
            object-fit: cover;
        }
        
        .card-content {
            padding: 30px;
        }
        
        .card h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        .tag {
            display: inline-block;
            background: #e8f5e9;
            color: var(--primary);
            padding: 5px 15px;
            border-radius: 30px;
            font-size: 0.9rem;
            margin-bottom: 15px;
        }
        
        .facts {
            background: linear-gradient(135deg, #006400, #228B22);
            color: white;
            text-align: center;
        }
        
        .facts-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
        }
        
        .fact-item {
            padding: 30px;
        }
        
        .fact-number {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 10px;
            color: var(--accent);
        }
        
        .gallery {
            background: white;
        }
        
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 15px;
            height: 300px;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        .gallery-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(transparent, rgba(0,0,0,0.8));
            color: white;
            padding: 30px 20px 20px;
            font-size: 1.1rem;
        }
        
        footer {
            background: #1a1a1a;
            color: #ddd;
            text-align: center;
            padding: 80px 20px 40px;
        }
        
        .footer-content {
            max-width: 1000px;
            margin: 0 auto;
        }
        
        .footer-links {
            margin: 40px 0;
        }
        
        .footer-links a {
            color: #bbb;
            margin: 0 15px;
            text-decoration: none;
        }
        
        .footer-links a:hover {
            color: var(--accent);
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 3rem;
            }
            .subtitle {
                font-size: 1.4rem;
            }
            .nav-container {
                padding: 0 20px;
            }
        }
    </style>
</head>
<body>
    <nav>
        <div class="nav-container">
            <div class="logo">🌿 Incredible Nature</div>
            <div class="nav-links">
                <a href="#destinations">Destinations</a>
                <a href="#facts">Nature Facts</a>
                <a href="#gallery">Gallery</a>
                <a href="#">Plan Your Trip</a>
            </div>
        </div>
    </nav>

    <header>
        <div class="hero-content">
            <h1>India's Eternal Beauty</h1>
            <p class="subtitle">From snow-capped Himalayas to sun-kissed beaches, lush backwaters to golden deserts — experience the breathtaking natural wonders of India</p>
            <a href="#destinations" class="cta-button">Explore Nature's Masterpieces</a>
        </div>
    </header>

    <section class="intro">
        <div class="container">
            <h2>Welcome to Nature's Own Country</h2>
            <p>India is a land of unparalleled natural diversity. Spanning snow peaks, dense rainforests, serene lakes, pristine beaches, and vast deserts, it offers a visual feast for every nature lover. With 10 biogeographic zones, over 500 wildlife sanctuaries, and countless scenic landscapes, India showcases the raw, vibrant beauty of Mother Earth in its most magnificent forms.</p>
        </div>
    </section>

    <section id="destinations" class="destinations">
        <div class="container">
            <h2>Iconic Natural Wonders</h2>
            <div class="grid">
                
                <!-- Kashmir -->
                <div class="card">
                    <img src="https://picsum.photos/id/1015/800/600" alt="Kashmir Valley">
                    <div class="card-content">
                        <span class="tag">Jammu & Kashmir</span>
                        <h3>Paradise on Earth - Kashmir</h3>
                        <p>Snow-capped Himalayan peaks, crystal-clear Dal Lake, lush green meadows, and blooming tulip gardens. Often called "Paradise on Earth" for its mesmerizing valleys and serene houseboats.</p>
                    </div>
                </div>
                
                <!-- Kerala Backwaters -->
                <div class="card">
                    <img src="https://picsum.photos/id/1016/800/600" alt="Kerala Backwaters">
                    <div class="card-content">
                        <span class="tag">Kerala</span>
                        <h3>Serene Backwaters of Kerala</h3>
                        <p>Glide through palm-fringed canals on a traditional houseboat. Lush greenery, coconut groves, and tranquil waters create "God's Own Country" — a tropical paradise of peace and natural harmony.</p>
                    </div>
                </div>
                
                <!-- Himalayas -->
                <div class="card">
                    <img src="https://picsum.photos/id/1018/800/600" alt="Himalayas">
                    <div class="card-content">
                        <span class="tag">Himachal & Uttarakhand</span>
                        <h3>Majestic Himalayas</h3>
                        <p>Home to some of the world's highest peaks, ancient glaciers, and vibrant valleys like Valley of Flowers. A trekker's dream and a photographer's paradise with breathtaking alpine scenery.</p>
                    </div>
                </div>
                
                <!-- Rajasthan Desert -->
                <div class="card">
                    <img src="https://picsum.photos/id/102/800/600" alt="Rajasthan Desert">
                    <div class="card-content">
                        <span class="tag">Rajasthan</span>
                        <h3>The Golden Thar Desert</h3>
                        <p>Endless golden sand dunes, camel safaris at sunset, and star-filled desert nights. The rugged beauty of the Rann of Kutch and Thar offers a dramatic contrast to India's green landscapes.</p>
                    </div>
                </div>
                
                <!-- Andaman Islands -->
                <div class="card">
                    <img src="https://picsum.photos/id/1033/800/600" alt="Andaman Beaches">
                    <div class="card-content">
                        <span class="tag">Andaman & Nicobar</span>
                        <h3>Turquoise Andaman Beaches</h3>
                        <p>Pr pristine coral reefs, white-sand beaches, and crystal-clear waters. Radhanagar Beach and other hidden coves offer some of Asia's most beautiful marine ecosystems.</p>
                    </div>
                </div>
                
                <!-- Western Ghats -->
                <div class="card">
                    <img src="https://picsum.photos/id/1040/800/600" alt="Western Ghats">
                    <div class="card-content">
                        <span class="tag">Karnataka & Kerala</span>
                        <h3>Lush Western Ghats</h3>
                        <p>UNESCO World Heritage rainforests, cascading waterfalls, tea plantations in Munnar, and rich biodiversity. A hotspot for endemic species and misty hill station escapes.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="facts" class="facts">
        <div class="container">
            <h2 style="color:white;">India's Natural Splendor at a Glance</h2>
            <div class="facts-grid">
                <div class="fact-item">
                    <div class="fact-number">8</div>
                    <p>UNESCO Natural World Heritage Sites</p>
                </div>
                <div class="fact-item">
                    <div class="fact-number">106</div>
                    <p>National Parks</p>
                </div>
                <div class="fact-item">
                    <div class="fact-number">500+</div>
                    <p>Wildlife Sanctuaries & Reserves</p>
                </div>
                <div class="fact-item">
                    <div class="fact-number">10</div>
                    <p>Biogeographic Zones</p>
                </div>
                <div class="fact-item">
                    <div class="fact-number">7,500+</div>
                    <p>Kilometers of Coastline</p>
                </div>
                <div class="fact-item">
                    <div class="fact-number">World's</div>
                    <p>Highest & Largest River Island (Majuli)</p>
                </div>
            </div>
        </div>
    </section>

    <section id="gallery" class="gallery">
        <div class="container">
            <h2>Visual Journey Through India's Nature</h2>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="https://picsum.photos/id/1015/800/600" alt="Kashmir">
                    <div class="gallery-overlay">Snowy Kashmir Valley</div>
                </div>
                <div class="gallery-item">
                    <img src="https://picsum.photos/id/1016/800/600" alt="Kerala">
                    <div class="gallery-overlay">Kerala Backwaters at Dawn</div>
                </div>
                <div class="gallery-item">
                    <img src="https://picsum.photos/id/1018/800/600" alt="Himalayas">
                    <div class="gallery-overlay">Himalayan Peaks & Valleys</div>
                </div>
                <div class="gallery-item">
                    <img src="https://picsum.photos/id/102/800/600" alt="Desert">
                    <div class="gallery-overlay">Golden Sand Dunes of Rajasthan</div>
                </div>
                <div class="gallery-item">
                    <img src="https://picsum.photos/id/1033/800/600" alt="Andaman">
                    <div class="gallery-overlay">Crystal Waters of Andaman</div>
                </div>
                <div class="gallery-item">
                    <img src="https://picsum.photos/id/1040/800/600" alt="Ghats">
                    <div class="gallery-overlay">Waterfalls in Western Ghats</div>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="footer-content">
            <div class="logo" style="color:white; font-size:2.5rem;">🌿 Incredible Nature</div>
            <p style="margin: 25px 0;">Celebrating the timeless natural beauty of India</p>
            
            <div class="footer-links">
                <a href="#">Home</a>
                <a href="#">Destinations</a>
                <a href="#">Wildlife</a>
                <a href="#">Eco Tourism</a>
                <a href="#">Contact</a>
            </div>
            
            <p>&copy; 2026 Incredible Nature India. Made with love for India's natural heritage.</p>
            <p style="margin-top: 20px; font-size: 0.9rem;">This is a beautiful static website template showcasing India's nature. Copy and save as .html to open in any browser.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                if (this.getAttribute('href') !== '#') {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth'
                        });
                    }
                }
            });
        });
        
        // Simple header scroll effect
        window.addEventListener('scroll', () => {
            const nav = document.querySelector('nav');
            if (window.scrollY > 100) {
                nav.style.background = 'rgba(255,255,255,0.98)';
            } else {
                nav.style.background = 'rgba(255,255,255,0.95)';
            }
        });
    </script>
</body>
</html>
