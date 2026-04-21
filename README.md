<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ELEVATE | Premium Real Estate</title>
    
    <!-- Premium Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500&family=Playfair+Display:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">

    <style>
        :root {
            --white: #ffffff;
            --black: #111111;
            --brand-blue: #003594; 
            --grey-text: #666666;
            --light-grey: #f9f9f9;
            --max-width: 1200px; /* Expanded for full page center-constraining */
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            background-color: var(--white);
            font-family: 'Inter', sans-serif;
            color: var(--black);
            line-height: 1.6;
            padding: 0; /* Removed padding to make it full page */
            overflow-x: hidden;
        }

        .page-wrapper {
            width: 100%;
            margin: 0 auto;
            background-color: var(--white);
        }

        img { width: 100%; display: block; object-fit: cover; }
        .section { padding: 60px 0; }
        .container-sm { max-width: 600px; margin: 0 auto; text-align: center; padding: 0 20px; }
        .container { max-width: var(--max-width); margin: 0 auto; }

        /* Typography */
        .serif { font-family: 'Playfair Display', serif; }
        .overline {
            font-size: 10px;
            letter-spacing: 3px;
            text-transform: uppercase;
            color: var(--brand-blue);
            margin-bottom: 12px;
            display: block;
            font-weight: 500;
        }
        
        h1 { font-size: 38px; font-weight: 400; margin-bottom: 20px; letter-spacing: 1px; }
        h2 { font-size: 32px; font-weight: 400; font-style: italic; }
        .price { color: var(--brand-blue); font-weight: 500; font-size: 13px; margin: 10px 0; }

        /* Buttons & Links w/ Hover Animations */
        .btn {
            display: inline-block;
            text-decoration: none;
            font-size: 11px;
            letter-spacing: 2px;
            padding: 16px 35px;
            text-transform: uppercase;
            transition: all 0.4s ease;
            cursor: pointer;
            border: 1px solid transparent;
        }
        .btn-black { background: var(--black); color: var(--white); border-color: var(--black); }
        .btn-black:hover { background: var(--white); color: var(--black); }
        
        .btn-blue { background: var(--brand-blue); color: var(--white); border-color: var(--brand-blue); }
        .btn-blue:hover { background: var(--white); color: var(--brand-blue); }
        
        .view-link {
            font-size: 10px;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: var(--brand-blue);
            text-decoration: none; /* Removed underline to animate it */
            font-weight: 600;
            border-bottom: 1px solid var(--brand-blue);
            padding-bottom: 2px;
            transition: all 0.3s ease;
        }
        .view-link:hover {
            color: var(--black);
            border-bottom-color: var(--black);
        }

        /* HEADER */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 25px 40px;
            border-bottom: 1px solid #eee;
            max-width: var(--max-width);
            margin: 0 auto;
        }
        .logo { font-size: 16px; letter-spacing: 5px; font-weight: 600; }
        .header-vol { font-size: 9px; letter-spacing: 2px; color: #999; text-transform: uppercase; }

        /* HERO */
        .hero-img { height: 70vh; min-height: 500px; overflow: hidden; width: 100%; }
        .hero-img img { height: 100%; width: 100%; object-fit: cover; }
        .hero-content { padding: 80px 40px; }
        .hero-desc { color: var(--grey-text); font-size: 14px; margin-bottom: 30px; line-height: 1.8; }

        /* STATS */
        .stats-wrapper { border-top: 1px solid #eee; border-bottom: 1px solid #eee; background: #fafafa; }
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            max-width: var(--max-width);
            margin: 0 auto;
        }
        .stat-item { padding: 40px 30px; text-align: center; border-right: 1px solid #eee; }
        .stat-item:last-child { border-right: none; }
        .stat-label { font-size: 9px; letter-spacing: 2px; text-transform: uppercase; color: #999; margin-bottom: 5px; }
        .stat-value { font-size: 15px; font-weight: 500; }

        /* LISTINGS */
        .listings-section { padding: 100px 0; max-width: var(--max-width); margin: 0 auto; }
        .listing-row {
            display: flex;
            align-items: center;
            margin-top: 80px;
            gap: 60px;
            padding: 0 40px;
        }
        .listing-row.reverse { flex-direction: row-reverse; }
        .listing-img { flex: 1.2; height: 400px; overflow: hidden; }
        .listing-img img { height: 100%; width: 100%; object-fit: cover; transition: transform 0.6s ease; }
        .listing-img:hover img { transform: scale(1.05); } /* Image hover animation */
        
        .listing-text { flex: 1; }
        .listing-text h3 { font-size: 24px; font-weight: 400; margin-bottom: 15px; }
        .listing-text p { font-size: 13px; color: var(--grey-text); line-height: 1.7; margin-bottom: 15px; }

        /* MARKET SECTION */
        .market-section {
            background-color: var(--brand-blue);
            color: white;
            display: flex;
            align-items: center;
            padding: 0;
            width: 100%;
        }
        .market-content { flex: 1; padding: 100px 80px; }
        .market-content h2 { font-size: 34px; margin-bottom: 25px; font-style: normal; }
        .market-content hr { width: 40px; border: none; border-top: 2px solid white; margin-bottom: 25px; }
        .market-content p { font-size: 13px; opacity: 0.8; margin-bottom: 30px; line-height: 1.8; }
        .market-img { flex: 1; height: 500px; overflow: hidden; }

        /* AGENT PROFILE */
        .agent-section { padding: 100px 40px; }
        .agent-photo { width: 100px; height: 100px; border-radius: 50%; margin: 0 auto 20px; transition: transform 0.4s ease; }
        .agent-photo:hover { transform: scale(1.1); }
        .agent-quote {
            font-family: 'Playfair Display', serif;
            font-style: italic;
            font-size: 18px;
            color: var(--grey-text);
            max-width: 500px;
            margin: 30px auto;
        }

        /* CONTACT FORM */
        .contact-section { padding: 80px 40px; background: #fafafa; border-top: 1px solid #eee; }
        .contact-form { max-width: 500px; margin: 40px auto 0; display: flex; flex-direction: column; gap: 15px; }
        .form-group input, .form-group textarea {
            width: 100%; padding: 15px; font-family: 'Inter', sans-serif; font-size: 13px;
            border: 1px solid #ddd; background: var(--white); transition: border-color 0.3s ease;
        }
        .form-group input:focus, .form-group textarea:focus { border-color: var(--black); outline: none; }
        .form-group textarea { height: 120px; resize: vertical; }

        /* FOOTER */
        footer {
            padding: 80px 40px;
            text-align: center;
            background: var(--white);
            border-top: 1px solid #eee;
        }
        .footer-address { font-size: 11px; color: #999; margin: 25px 0; line-height: 2; }
        .social-links { margin-bottom: 30px; }
        .social-links a { 
            text-decoration: none; color: var(--black); font-size: 10px; 
            letter-spacing: 2px; font-weight: 600; margin: 0 15px; text-transform: uppercase;
            transition: color 0.3s ease;
        }
        .social-links a:hover { color: var(--brand-blue); }
        .legal { font-size: 9px; color: #ccc; max-width: 500px; margin: 0 auto; }

        /* ENTRANCE ANIMATIONS */
        .animate-entrance {
            opacity: 0;
            transform: translateY(40px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }
        .animate-entrance.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Mobile */
        @media (max-width: 768px) {
            .listing-row, .listing-row.reverse, .market-section { flex-direction: column; padding: 0 20px; }
            .listing-img, .listing-text, .market-content, .market-img { width: 100%; flex: none; height: auto; }
            .listing-row { gap: 30px; margin-top: 50px; text-align: center; }
            .market-content { text-align: center; padding: 60px 20px; }
            .market-content hr { margin: 0 auto 25px; }
            .stats-grid { grid-template-columns: 1fr; }
            .stat-item { border-right: none; border-bottom: 1px solid #eee; padding: 25px; }
            h1 { font-size: 30px; }
            header { flex-direction: column; gap: 15px; }
        }
    </style>
</head>
<body>

<div class="page-wrapper">
    
    <!-- HEADER -->
    <header>
        <div class="logo">ELEVATE.</div>
        <div class="header-vol">VOL. IV — NEW EXCLUSIVES</div>
    </header>

    <!-- HERO SECTION -->
    <section>
        <div class="hero-img animate-entrance">
            <img src="https://images.unsplash.com/photo-1613490493576-7fde63acd811?auto=format&fit=crop&q=80&w=1200" alt="The Glass Pavilion">
        </div>
        <div class="container-sm hero-content animate-entrance">
            <span class="overline">FLAGSHIP PROPERTY</span>
            <h1 class="serif">The Glass Pavilion</h1>
            <p class="hero-desc">
                Suspended above the canyon with panoramic, unobstructed views of the city. This architectural masterpiece redefines indoor-outdoor living with seamless glass walls and imported Italian stone.
            </p>
            <a href="#" class="btn btn-black">EXPLORE THE ESTATE</a>
        </div>
    </section>

    <!-- STATS -->
    <div class="stats-wrapper animate-entrance">
        <div class="stats-grid">
            <div class="stat-item">
                <p class="stat-label">Asking Price</p>
                <p class="stat-value" style="color: var(--brand-blue);">$8,950,000</p>
            </div>
            <div class="stat-item">
                <p class="stat-label">Architecture</p>
                <p class="stat-value">6 Bed / 8 Bath</p>
            </div>
            <div class="stat-item">
                <p class="stat-label">Interior Space</p>
                <p class="stat-value">12,400 SqFt</p>
            </div>
        </div>
    </div>

    <!-- NEWLY LISTED -->
    <section class="listings-section">
        <div class="container-sm animate-entrance">
            <h2 class="serif">Newly Listed</h2>
        </div>

        <!-- Listing 1 -->
        <div class="listing-row animate-entrance">
            <div class="listing-img">
                <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&q=80&w=800" alt="88 Park Avenue">
            </div>
            <div class="listing-text">
                <span class="overline" style="font-size: 8px;">APT 4B</span>
                <h3 class="serif">88 Park Avenue</h3>
                <p>A rare, fully renovated loft featuring 14-foot ceilings and exposed original brickwork.</p>
                <p class="price">$2,450,000</p>
                <a href="#" class="view-link">VIEW DETAILS</a>
            </div>
        </div>

        <!-- Listing 2 -->
        <div class="listing-row reverse animate-entrance">
            <div class="listing-img">
                <img src="https://images.unsplash.com/photo-1556912172-45b7abe8b7e1?auto=format&fit=crop&q=80&w=800" alt="Oakwood Manor Interior">
            </div>
            <div class="listing-text">
                <span class="overline" style="font-size: 8px;">SUBURBAN ESTATE</span>
                <h3 class="serif">Oakwood Manor</h3>
                <p>Tucked behind private gates, this colonial revival sits on 2 pristine acres with a private tennis court.</p>
                <p class="price">$4,100,000</p>
                <a href="#" class="view-link">VIEW DETAILS</a>
            </div>
        </div>

        <!-- Listing 3 -->
        <div class="listing-row animate-entrance">
            <div class="listing-img">
                <img src="https://images.unsplash.com/photo-1584622650111-993a426fbf0a?auto=format&fit=crop&q=80&w=800" alt="Malibu Terrace">
            </div>
            <div class="listing-text">
                <span class="overline" style="font-size: 8px;">PENTHOUSE</span>
                <h3 class="serif">Malibu Terrace</h3>
                <p>Floor-to-ceiling windows meet the Pacific Ocean. Complete with a private rooftop spa.</p>
                <p class="price">$6,800,000</p>
                <a href="#" class="view-link">VIEW DETAILS</a>
            </div>
        </div>
    </section>

    <!-- MARKET REPORT -->
    <section class="market-section animate-entrance">
        <div class="market-content">
            <h2 class="serif">The State<br>of the Market.</h2>
            <hr>
            <p>Strategic pricing is paramount this quarter. As inventory gently rises, the properties that command premium offers are those with flawless presentation and aggressive digital marketing.</p>
            <a href="#" class="view-link" style="color: white; border-bottom: 1px solid white;">READ THE REPORT</a>
        </div>
        <div class="market-img">
            <img src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?auto=format&fit=crop&q=80&w=800" style="height: 100%;">
        </div>
    </section>

    <!-- AGENT SECTION -->
    <section class="agent-section container-sm animate-entrance">
        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&q=80&w=200" alt="James Harrison" class="agent-photo">
        <h4 class="serif" style="font-size: 20px;">James Harrison</h4>
        <p class="overline" style="margin-top: 5px; color: #999;">PRINCIPAL BROKER & FOUNDER</p>
        <p class="agent-quote">"Curating the finest properties for discerning clients. Let's discuss the architecture of your next move."</p>
        <a href="#" class="btn btn-blue">SCHEDULE A PRIVATE TOUR</a>
    </section>

    <!-- CONTACT FORM SECTION -->
    <section class="contact-section animate-entrance">
        <div class="container-sm">
            <span class="overline">GET IN TOUCH</span>
            <h2 class="serif" style="margin-bottom: 10px;">Contact Us</h2>
            <p style="font-size: 13px; color: var(--grey-text);">Reach out to discuss your real estate portfolio.</p>
            
            <form class="contact-form">
                <div class="form-group">
                    <input type="text" placeholder="Full Name" required>
                </div>
                <div class="form-group">
                    <input type="email" placeholder="Email Address" required>
                </div>
                <div class="form-group">
                    <textarea placeholder="Your Message" required></textarea>
                </div>
                <button type="submit" class="btn btn-black">SEND MESSAGE</button>
            </form>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="animate-entrance">
        <div class="logo">ELEVATE.</div>
        <p class="footer-address">
            100 Corporate Drive, Suite 200, Los Angeles, CA 90001<br>
            DRE #01234567 | 555.123.4567
        </p>
        <div class="social-links">
            <a href="#">INSTAGRAM</a>
            <a href="#">LINKEDIN</a>
            <a href="#">WEBSITE</a>
        </div>
        <p class="legal">
            © Equal Housing Opportunity. This email was sent to you because you opted in. <br>
            <a href="#" style="color: #ccc;">Update Preferences</a> | <a href="#" style="color: #ccc;">Unsubscribe</a>
        </p>
    </footer>

</div>

<!-- Intersection Observer Script for Entrance Animations -->
<script>
    document.addEventListener("DOMContentLoaded", function() {
        const observerOptions = {
            root: null,
            rootMargin: "0px",
            threshold: 0.15 
        };

        const observer = new IntersectionObserver((entries, observer) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);

        document.querySelectorAll('.animate-entrance').forEach((el) => {
            observer.observe(el);
        });
    });
</script>

</body>
</html>
