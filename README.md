<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fashion Ecosystem | Masterclass & Resurse Digitale</title>
    <style>
        /* Culori Brand & Setări Globale */
        :root {
            --off-white: #FBFBF9;
            --charcoal: #1A1A1A;
            --champagne-gold: #D4AF37;
            --midnight-black: #0A0A0A;
            --text-muted: #7A7A7A;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Helvetica Neue', Arial, sans-serif;
            letter-spacing: 0.5px;
        }

        body {
            background-color: var(--off-white);
            color: var(--midnight-black);
            line-height: 1.7;
        }

        /* Navigație Premium (Kerning Larg) */
        header {
            background-color: var(--midnight-black);
            color: var(--off-white);
            padding: 25px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
        }

        .nav-container {
            width: 85%;
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 20px;
            font-weight: 300;
            text-transform: uppercase;
            letter-spacing: 6px; /* Kerning larg */
            color: var(--off-white);
        }

        .logo span {
            color: var(--champagne-gold);
            font-weight: 400;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            color: var(--off-white);
            text-decoration: none;
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 2px;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--champagne-gold);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(10, 10, 10, 0.75), rgba(26, 26, 26, 0.9)), url('https://images.unsplash.com/photo-1509631179647-0177331693ae?auto=format&fit=crop&w=1200&q=80') no-repeat center center/cover;
            height: 70vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--off-white);
            padding: 0 20px;
        }

        .hero-content h1 {
            font-size: 46px;
            font-weight: 200;
            text-transform: uppercase;
            letter-spacing: 8px;
            margin-bottom: 20px;
        }

        .hero-content p {
            font-size: 16px;
            color: #E0E0E0;
            max-width: 600px;
            margin: 0 auto 30px auto;
            font-weight: 300;
        }

        .btn-gold {
            display: inline-block;
            border: 1px solid var(--champagne-gold);
            color: var(--off-white);
            padding: 12px 35px;
            text-decoration: none;
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 3px;
            background: transparent;
            transition: all 0.4s ease;
        }

        .btn-gold:hover {
            background-color: var(--champagne-gold);
            color: var(--midnight-black);
            box-shadow: 0 0 15px rgba(212, 175, 55, 0.4);
        }

        /* Secțiuni Generale */
        .container {
            width: 85%;
            max-width: 1200px;
            margin: 100px auto;
        }

        .section-title {
            font-size: 28px;
            font-weight: 300;
            text-transform: uppercase;
            letter-spacing: 4px;
            margin-bottom: 50px;
            text-align: center;
            position: relative;
        }.section-title::after {
            content: '';
            display: block;
            width: 40px;
            height: 1px;
            background-color: var(--champagne-gold);
            margin: 15px auto 0 auto;
        }

        /* Grid-uri și Carduri */
        .grid-2 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
            gap: 50px;
            align-items: center;
            margin-bottom: 80px;
        }

        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card-premium {
            background-color: #ffffff;
            border: 1px solid #ECECEC;
            padding: 40px;
            transition: all 0.3s ease;
        }

        .card-premium:hover {
            border-color: var(--champagne-gold);
            transform: translateY(-5px);
        }

        .card-premium h3 {
            font-size: 18px;
            font-weight: 400;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 25px;
            color: var(--charcoal);
        }

        .card-premium h3 span {
            color: var(--champagne-gold);
            display: block;
            font-size: 12px;
            margin-bottom: 5px;
        }

        /* Placeholder-uri Imagini cu Stil */
        .image-placeholder {
            width: 100%;
            height: 400px;
            background-color: var(--charcoal);
            background-size: cover;
            background-position: center;
            position: relative;
            box-shadow: 0 15px 35px rgba(0,0,0,0.05);
        }

        .image-caption {
            position: absolute;
            bottom: 20px;
            left: 20px;
            background-color: rgba(10, 10, 10, 0.8);
            color: var(--off-white);
            padding: 5px 15px;
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        /* Axa Timpului Interactivă (Istorie) */
        .timeline {
            border-left: 1px solid var(--champagne-gold);
            margin-left: 20px;
            padding-left: 30px;
        }

        .timeline-item {
            position: relative;
            margin-bottom: 40px;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -36px;
            top: 5px;
            width: 10px;
            height: 10px;
            background-color: var(--midnight-black);
            border: 1px solid var(--champagne-gold);
            border-radius: 50%;
        }

        .timeline-year {
            font-weight: bold;
            color: var(--champagne-gold);
            font-size: 16px;
            margin-bottom: 5px;
        }

        /* Social Media Section & AI */
        .ai-box {
            background-color: var(--charcoal);
            color: var(--off-white);
            padding: 50px;
            border-left: 4px solid var(--champagne-gold);
        }

        .reel-idea {
            background: rgba(255,255,255,0.05);
            padding: 20px;
            margin-top: 25px;
            border: 1px dashed rgba(214, 175, 55, 0.4);
        }

        /* Stiluri pentru Monetizare / Produse */
        .product-badge {
            background-color: var(--midnight-black);
            color: var(--off-white);
            font-size: 10px;
            padding: 2px 8px;
            text-transform: uppercase;
            letter-spacing: 1px;
            display: inline-block;
            margin-bottom: 15px;
        }

        /* Footer */
        footer {
            background-color: var(--midnight-black);
            color: var(--text-muted);
            text-align: center;
            padding: 60px 0;
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 2px;
            border-top: 1px solid rgba(214, 175, 55, 0.1);
        }/* Responsivitate */
        @media (max-width: 768px) {
            .nav-container { flex-direction: column; gap: 15px; }
            .grid-2 { grid-template-columns: 1fr; }
            .hero-content h1 { font-size: 28px; }
            .image-placeholder { height: 250px; }
        }
    </style>
</head>
<body>

    <!-- Header / Navigație -->
    <header>
        <div class="nav-container">
            <div class="logo">FASHION<span>ECOSYSTEM</span></div>
            <nav>
                <ul>
                    <li><a href="#istorie">Istorie</a></li>
                    <li><a href="#ai-tech">AI & Tech</a></li>
                    <li><a href="#business">Business</a></li>
                    <li><a href="#structura">Cursuri</a></li>
                    <li><a href="#monetizare">Monetizare</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Zona Hero -->
    <section class="hero">
        <div class="hero-content">
            <h1>De la Corset la Cod</h1>
            <p>Platforma completă pentru înțelegerea istoriei, tehnologiei și strategiilor de business din spatele ecosistemului global de modă.</p>
            <a href="#structura" class="btn-gold">Explorează Modulele</a>
        </div>
    </section>

    <!-- 1. Istoria și Evoluția Modei -->
    <section id="istorie" class="container">
        <h2 class="section-title">1. Istoria și Evoluția Modei</h2>
        <div class="grid-2">
            <div>
                <p style="font-size: 18px; margin-bottom: 20px; font-weight: 300;">Evoluția Modei ca Oglindă Socială</p>
                <p>Explorăm tranziția de la opulența și constrângerile fizice ale secolului al XIX-lea, la minimalismul eliberator al anilor '90 și inovația tehnologică structurală de astăzi. Istoria modei nu este doar despre haine; ea reprezintă dinamica schimbărilor sociale, economice și politice ale fiecărei epoci.</p>
            </div>
            <!-- Infografic Interactiv / Axa timpului -->
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-year">Secolul XIX (Opulență)</div>
                    <p>Siluete exagerate, corsete rigide și straturi masive de materiale ce reflectau statutul social aristocratic.</p>
                </div>
                <div class="timeline-item">
                    <div class="timeline-year">Anii '90 (Minimalism)</div>
                    <p>Deconstrucție, linii curate, estetică anti-fashion și haine simple (Denim, slip dresses, culori neutre).</p>
                </div>
                <div class="timeline-item">
                    <div class="timeline-year">Prezent (Inovație)</div>
                    <p>Fuziunea dintre haine fizice și tehnologie purtabilă. Accent masiv pe sustenabilitate structurală.</p>
                </div>
            </div>
        </div>

        <div class="grid-2">
            <!-- Placeholder Imagine Capitale -->
            <div class="image-placeholder" style="background-image: url('https://images.unsplash.com/photo-1502602898657-3e91760cbb34?auto=format&fit=crop&w=600&q=80');">
                <div class="image-caption">Capitale: Turnul Eiffel la amurg</div>
            </div>
            <!-- Placeholder Imagine Textile -->
            <div class="image-placeholder" style="background-image: url('https://images.unsplash.com/photo-1544816155-12df9643f363?auto=format&fit=crop&w=600&q=80');">
                <div class="image-caption">Textile: Texturi macro - catifea & mătase</div>
            </div>
        </div>
    </section>

    <!-- 2. Viitorul: AI & Fashion Tech -->
    <section id="ai-tech" style="background-color: var(--midnight-black); padding: 20px 0;">
        <div class="container">
            <h2 class="section-title" style="color: var(--off-white);">2. Viitorul: AI & Fashion Tech</h2><div class="grid-2">
                <div class="ai-box">
                    <p style="margin-bottom: 20px;">Inteligența Artificială revoluționează verigile ecosistemului: de la algoritmi avansați care prezic tendințele viitoare globale (<strong>Trend Forecasting</strong>), până la designeri virtuali independenți.</p>
                    <p>Hainele digitale (<strong>Virtual Wearables</strong>) reprezintă noua frontieră a sustenabilității, eliminând deșeurile textile din faza de design și prototipare.</p>
                </div>
                <!-- Idee Social Media Box -->
                <div class="ai-box" style="border-left-color: var(--off-white);">
                    <span style="color: var(--champagne-gold); font-size: 11px; uppercase; tracking: 2px; font-weight: bold;">[ IDEE SOCIAL MEDIA / REEL ]</span>
                    <div class="reel-idea">
                        <p><strong>Concept Video:</strong> Tranziție rapidă cu un avatar 3D hiper-realist într-un cadru cyberpunk, care "îmbracă" instantaneu o serie de ținute conceptuale generate complet prin algoritmi generativi AI.</p>
                        <p style="font-size: 13px; color: var(--text-muted); margin-top: 10px;">Subtext recomandat: "Digital Couture is reducing 97% of physical waste."</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 3. Business & Marketing Fashion -->
    <section id="business" class="container">
        <h2 class="section-title">3. Business & Marketing Fashion</h2>
        <div class="grid-3">
            <div class="card-premium">
                <h3>Strategii de Branding</h3>
                <p>Un brand de modă de succes se bazează pe un <strong>storytelling de impact</strong>. Nu vinzi un produs textil, ci vinzi un stil de viață integrat, o poveste sau un ideal aspirațional în care consumatorul dorește să se regăsească.</p>
            </div>
            <div class="card-premium">
                <h3>Psihologia Consumatorului</h3>
                <p>De ce cumpărăm impulsiv? Înțelegerea profundă a „triggerelor” emoționale (precum exclusivitatea, apartenența la un grup sau frica de a pierde o oportunitate - FOMO) în procesul de achiziție.</p>
            </div>
            <div class="card-premium">
                <h3>SEO & Email Marketing</h3>
                <p>Cuvinte cheie strategice de integrat în SEO: <em>Sustainable Fashion, Luxury Aesthetic, Capsule Wardrobe, Digital Couture</em>. Strategia de email trebuie să fie „curated” – un newsletter cu layout curat, similar unei reviste private.</p>
            </div>
        </div>

        <div class="grid-2" style="margin-top: 50px;">
            <!-- Placeholder Imagine Modeling -->
            <div class="image-placeholder" style="background-image: url('https://images.unsplash.com/photo-1509631179647-0177331693ae?auto=format&fit=crop&w=600&q=80');">
                <div class="image-caption">Modeling: Catwalk-ul unei capitale a modei</div>
            </div>
            <!-- Placeholder Imagine Streetwear -->
            <div class="image-placeholder" style="background-image: url('https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=600&q=80');">
                <div class="image-caption">Streetwear: Ținută urbană la apus</div>
            </div>
        </div>
    </section>

    <!-- 4. Structura Cursului (Module E-Learning) -->
    <section id="structura" style="background-color: #F0F0ED; padding: 20px 0;">
        <div class="container">
            <h2 class="section-title">4. Structura Cursului (Module E-Learning)</h2>
            <div class="grid-3">
                <div class="card-premium" style="background: var(--off-white);">
                    <h3><span>Modulul 01</span>The Fundamentals</h3><p>Studiul aprofundat al teoriei culorilor, identificarea tipurilor de țesături naturale și sintetice, precum și bazele croiurilor clasice în designul vestimentar.</p>
                </div>
                <div class="card-premium" style="background: var(--off-white);">
                    <h3><span>Modulul 02</span>The Creative Process</h3>
                    <p>Urmărirea fluxului creativ complet: de la cercetare vizuală și structurarea unui moodboard coerent, la schița tehnică și producția produsului finit.</p>
                </div>
                <div class="card-premium" style="background: var(--off-white);">
                    <h3><span>Modulul 03</span>Industry Mastery</h3>
                    <p>Strategii practice despre cum să navighezi în industria modelingului internațional sau cum să lansezi și să scalezi un brand de modă sustenabil.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 6. Idei de Monetizare (Produs Digital) -->
    <section id="monetizare" class="container">
        <h2 class="section-title">6. Modele de Monetizare Digitală</h2>
        <div class="grid-3">
            <div class="card-premium">
                <span class="product-badge">Digital Products</span>
                <h3>E-Books & Ghiduri</h3>
                <p>Lansarea de e-book-uri nișate de tip "How-to-Style", ghiduri digitale de shopping sustenabil sau cursuri video complete pentru viitorii designeri.</p>
            </div>
            <div class="card-premium">
                <span class="product-badge">Membership</span>
                <h3>Fashion Insider Reports</h3>
                <p>Acces pe bază de abonament lunar la analize macro săptămânale legate de tendințele emergente, schimbările de producție și rapoarte de retail.</p>
            </div>
            <div class="card-premium">
                <span class="product-badge">Affiliate Marketing</span>
                <h3>Curated Recommendations</h3>
                <p>Monetizarea traficului prin recomandări directe și integrate de piese vestimentare sustenabile sau capsule estetice pe blog/site.</p>
            </div>
        </div>
    </section>

    <!-- Subsol (Branding Minimalist) -->
    <footer>
        <p>© 2026 FASHION ECOSYSTEM. Toate drepturile rezervate.</p>
        <p style="font-size: 10px; margin-top: 5px; color: var(--champagne-gold);">Designed for Digital Couture & Innovation</p>
    </footer>

</body>
</html>
