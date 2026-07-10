<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0">
<title>Rasoi Restaurant & Cafe | Nalkheda</title>
<meta name="description" content="Rasoi Restaurant & Cafe - Authentic Indian cuisine in Nalkheda. Butter Chicken, Biryani, Tandoori, and more. Order online or visit us!">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
<style>
:root {
    --primary: #e67e22;
    --primary-dark: #d35400;
    --primary-light: #f39c12;
    --bg-dark: #0f0a08;
    --bg-section: #1a0f0a;
    --bg-card: rgba(255,255,255,0.04);
    --border: rgba(255,255,255,0.08);
    --text: #ffffff;
    --text-muted: rgba(255,255,255,0.6);
    --text-dim: rgba(255,255,255,0.4);
    --danger: #e74c3c;
    --success: #27ae60;
    --max-width: 1200px;
}
* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; -webkit-text-size-adjust: 100%; }
body { font-family: 'Inter', -apple-system, sans-serif; background: var(--bg-dark); color: var(--text); line-height: 1.6; overflow-x: hidden; -webkit-font-smoothing: antialiased; }

::-webkit-scrollbar { width: 8px; }
::-webkit-scrollbar-track { background: var(--bg-dark); }
::-webkit-scrollbar-thumb { background: var(--primary); border-radius: 4px; }

@keyframes fadeInUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }
@keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
@keyframes float { 0%,100% { transform: translateY(0); } 50% { transform: translateY(-10px); } }
@keyframes pulse { 0%,100% { transform: scale(1); } 50% { transform: scale(1.05); } }
@keyframes heroGlow { 0%, 100% { opacity: 0.3; transform: scale(1); } 50% { opacity: 0.6; transform: scale(1.1); } }

.animate { opacity: 0; }
.animate.visible { animation: fadeInUp 0.6s ease forwards; }
.animate-delay-1 { animation-delay: 0.1s; }
.animate-delay-2 { animation-delay: 0.2s; }
.animate-delay-3 { animation-delay: 0.3s; }
.animate-delay-4 { animation-delay: 0.4s; }

.header {
    position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
    background: rgba(15,10,8,0.95); backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--border); transition: all 0.3s;
}
.header.scrolled { background: rgba(15,10,8,0.98); box-shadow: 0 4px 30px rgba(0,0,0,0.5); }
.nav-container {
    max-width: var(--max-width); margin: 0 auto;
    display: flex; justify-content: space-between; align-items: center;
    padding: 16px 24px;
}
.logo { display: flex; align-items: center; gap: 12px; text-decoration: none; }
.logo-icon {
    width: 44px; height: 44px; border-radius: 12px;
    background: linear-gradient(135deg, var(--primary), var(--primary-dark));
    display: flex; align-items: center; justify-content: center;
    font-size: 22px; box-shadow: 0 4px 15px rgba(230,126,34,0.3);
}
.logo-text { display: flex; flex-direction: column; }
.logo-text h1 { font-size: 20px; font-weight: 800; color: var(--text); line-height: 1.2; }
.logo-text span { font-size: 11px; color: var(--primary); letter-spacing: 2px; text-transform: uppercase; font-weight: 600; }

.nav-links { display: flex; gap: 8px; list-style: none; }
.nav-links a {
    color: var(--text-muted); text-decoration: none; font-size: 14px; font-weight: 500;
    padding: 8px 16px; border-radius: 8px; transition: all 0.3s;
}
.nav-links a:hover, .nav-links a.active { color: var(--primary); background: rgba(230,126,34,0.1); }

.nav-cta {
    background: linear-gradient(135deg, var(--primary), var(--primary-dark));
    color: #fff; border: none; padding: 10px 24px; border-radius: 10px;
    font-size: 14px; font-weight: 700; cursor: pointer; transition: all 0.3s;
    box-shadow: 0 4px 15px rgba(230,126,34,0.3); font-family: inherit; text-decoration: none; display: inline-flex; align-items: center; gap: 6px;
}
.nav-cta:hover { transform: translateY(-2px); box-shadow: 0 6px 20px rgba(230,126,34,0.4); }

.mobile-menu-btn {
    display: none; background: none; border: none; color: var(--text);
    font-size: 24px; cursor: pointer; padding: 8px; border-radius: 8px; transition: background 0.3s;
}
.mobile-menu-btn:hover { background: rgba(255,255,255,0.05); }
.mobile-menu-btn:active { background: rgba(255,255,255,0.1); }

/* ===== NEW HERO SECTION ===== */
.hero {
    min-height: 100vh; display: flex; align-items: center;
    background: var(--bg-dark);
    position: relative; overflow: hidden; padding-top: 80px;
}
.hero-bg-pattern {
    position: absolute; inset: 0;
    background-image: 
        radial-gradient(circle at 20% 50%, rgba(230,126,34,0.08) 0%, transparent 50%),
        radial-gradient(circle at 80% 20%, rgba(211,84,0,0.06) 0%, transparent 40%),
        radial-gradient(circle at 60% 80%, rgba(243,156,18,0.05) 0%, transparent 45%);
    pointer-events: none;
}
.hero-particles {
    position: absolute; inset: 0; pointer-events: none; overflow: hidden;
}
.hero-particle {
    position: absolute; border-radius: 50%; background: var(--primary);
    opacity: 0.15; animation: float 6s ease-in-out infinite;
}
.hero-particle:nth-child(1) { width: 4px; height: 4px; top: 20%; left: 10%; animation-delay: 0s; }
.hero-particle:nth-child(2) { width: 6px; height: 6px; top: 60%; left: 15%; animation-delay: 1s; }
.hero-particle:nth-child(3) { width: 3px; height: 3px; top: 30%; left: 80%; animation-delay: 2s; }
.hero-particle:nth-child(4) { width: 5px; height: 5px; top: 70%; left: 70%; animation-delay: 0.5s; }
.hero-particle:nth-child(5) { width: 4px; height: 4px; top: 15%; left: 50%; animation-delay: 1.5s; }
.hero-particle:nth-child(6) { width: 7px; height: 7px; top: 80%; left: 40%; animation-delay: 2.5s; }
.hero-particle:nth-child(7) { width: 3px; height: 3px; top: 45%; left: 90%; animation-delay: 3s; }
.hero-particle:nth-child(8) { width: 5px; height: 5px; top: 85%; left: 25%; animation-delay: 1.2s; }

.hero-container {
    max-width: var(--max-width); margin: 0 auto;
    display: grid; grid-template-columns: 1fr 1fr; gap: 60px;
    padding: 60px 24px; align-items: center; position: relative; z-index: 1;
}
.hero-content { position: relative; }
.hero-badge-top {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(230,126,34,0.12); border: 1px solid rgba(230,126,34,0.25);
    padding: 8px 18px; border-radius: 50px; font-size: 13px;
    color: var(--primary); font-weight: 600; margin-bottom: 24px;
    animation: fadeInUp 0.6s ease forwards; animation-delay: 0.1s; opacity: 0;
}
.hero-badge-top .pulse-dot {
    width: 8px; height: 8px; border-radius: 50%; background: var(--primary);
    animation: pulse 2s infinite;
}
.hero-content h1 {
    font-size: 64px; font-weight: 900; line-height: 1.05;
    margin-bottom: 20px; letter-spacing: -2px;
    animation: fadeInUp 0.6s ease forwards; animation-delay: 0.2s; opacity: 0;
}
.hero-content h1 span { 
    background: linear-gradient(135deg, var(--primary), var(--primary-light));
    -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
}
.hero-content p {
    font-size: 18px; color: var(--text-muted); margin-bottom: 32px;
    max-width: 480px; line-height: 1.7;
    animation: fadeInUp 0.6s ease forwards; animation-delay: 0.3s; opacity: 0;
}
.hero-location {
    display: inline-flex; align-items: center; gap: 8px;
    background: var(--bg-card); border: 1px solid var(--border);
    padding: 10px 20px; border-radius: 50px; font-size: 14px;
    color: var(--text-muted); margin-bottom: 32px;
    animation: fadeInUp 0.6s ease forwards; animation-delay: 0.35s; opacity: 0;
}
.hero-buttons { 
    display: flex; gap: 16px; flex-wrap: wrap;
    animation: fadeInUp 0.6s ease forwards; animation-delay: 0.4s; opacity: 0;
}
.btn-primary {
    background: linear-gradient(135deg, var(--primary), var(--primary-dark));
    color: #fff; border: none; padding: 14px 32px; border-radius: 12px;
    font-size: 16px; font-weight: 700; cursor: pointer; transition: all 0.3s;
    box-shadow: 0 4px 20px rgba(230,126,34,0.3); text-decoration: none; display: inline-flex; align-items: center; gap: 8px;
    position: relative; overflow: hidden;
}
.btn-primary::after {
    content: ''; position: absolute; inset: 0;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
    transform: translateX(-100%); transition: transform 0.5s;
}
.btn-primary:hover { transform: translateY(-3px); box-shadow: 0 8px 30px rgba(230,126,34,0.4); }
.btn-primary:hover::after { transform: translateX(100%); }
.btn-secondary {
    background: transparent; color: var(--text); border: 2px solid var(--border);
    padding: 14px 32px; border-radius: 12px; font-size: 16px; font-weight: 600;
    cursor: pointer; transition: all 0.3s; text-decoration: none; display: inline-flex; align-items: center; gap: 8px;
}
.btn-secondary:hover { border-color: var(--primary); color: var(--primary); background: rgba(230,126,34,0.05); }

.hero-image { position: relative; perspective: 1000px; }
.hero-image-wrapper {
    position: relative; transform-style: preserve-3d;
    animation: float 5s ease-in-out infinite;
}
.hero-image img {
    width: 100%; max-width: 520px; border-radius: 24px;
    box-shadow: 0 30px 60px rgba(0,0,0,0.5);
    border: 1px solid rgba(255,255,255,0.05);
}
.hero-image-glow {
    position: absolute; inset: -20px;
    background: radial-gradient(circle, rgba(230,126,34,0.2) 0%, transparent 70%);
    border-radius: 30px; z-index: -1; animation: heroGlow 4s ease-in-out infinite;
}
.hero-floating-card {
    position: absolute; background: rgba(15,10,8,0.9); backdrop-filter: blur(10px);
    border: 1px solid var(--border); border-radius: 16px; padding: 16px 20px;
    display: flex; align-items: center; gap: 12px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.4);
    animation: float 4s ease-in-out infinite;
}
.hero-floating-card.review-card {
    top: -10px; right: -20px; animation-delay: 0.5s;
}
.hero-floating-card.delivery-card {
    bottom: 30px; left: -30px; animation-delay: 1s;
}
.hero-floating-card .card-icon {
    width: 40px; height: 40px; border-radius: 10px;
    background: linear-gradient(135deg, var(--primary), var(--primary-dark));
    display: flex; align-items: center; justify-content: center; font-size: 18px; flex-shrink: 0;
}
.hero-floating-card .card-text h4 { font-size: 13px; font-weight: 700; }
.hero-floating-card .card-text p { font-size: 11px; color: var(--text-dim); margin: 0; }
.hero-floating-card .card-stars { color: #f1c40f; font-size: 12px; }

.stats-bar {
    background: linear-gradient(135deg, rgba(230,126,34,0.1), rgba(211,84,0,0.05));
    border-top: 1px solid rgba(230,126,34,0.15);
    border-bottom: 1px solid rgba(230,126,34,0.15);
    padding: 40px 24px;
}
.stats-container {
    max-width: var(--max-width); margin: 0 auto;
    display: grid; grid-template-columns: repeat(4, 1fr); gap: 40px; text-align: center;
}
.stat-item h3 { font-size: 36px; font-weight: 800; color: var(--primary); margin-bottom: 8px; }
.stat-item p { font-size: 14px; color: var(--text-muted); }

.section { padding: 100px 24px; position: relative; }
.section-header { text-align: center; max-width: 600px; margin: 0 auto 60px; }
.section-header h2 { font-size: 14px; color: var(--primary); text-transform: uppercase; letter-spacing: 3px; font-weight: 700; margin-bottom: 16px; }
.section-header h3 { font-size: 40px; font-weight: 800; margin-bottom: 16px; line-height: 1.2; }
.section-header p { font-size: 18px; color: var(--text-muted); line-height: 1.7; }
.container { max-width: var(--max-width); margin: 0 auto; }

.about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: center; }
.about-image { position: relative; }
.about-image img { width: 100%; border-radius: 24px; box-shadow: 0 20px 50px rgba(0,0,0,0.4); }
.about-image::before { content: ''; position: absolute; top: 20px; left: 20px; width: 100%; height: 100%; border: 2px solid var(--primary); border-radius: 24px; z-index: -1; opacity: 0.3; }
.about-content h3 { font-size: 32px; font-weight: 800; margin-bottom: 20px; }
.about-content h3 span { color: var(--primary); }
.about-content p { color: var(--text-muted); margin-bottom: 20px; line-height: 1.8; font-size: 16px; }
.about-features { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 32px; }
.about-feature { display: flex; align-items: flex-start; gap: 12px; background: var(--bg-card); border: 1px solid var(--border); padding: 20px; border-radius: 16px; }
.about-feature .icon { width: 40px; height: 40px; border-radius: 10px; background: rgba(230,126,34,0.15); display: flex; align-items: center; justify-content: center; font-size: 18px; flex-shrink: 0; }
.about-feature h4 { font-size: 15px; font-weight: 700; margin-bottom: 4px; }
.about-feature p { font-size: 13px; color: var(--text-dim); margin: 0; }

.menu-section { background: var(--bg-section); }
.menu-tabs { display: flex; justify-content: center; gap: 12px; margin-bottom: 48px; flex-wrap: wrap; }
.menu-tab { padding: 12px 28px; border-radius: 50px; border: 1px solid var(--border); background: var(--bg-card); color: var(--text-muted); font-size: 14px; font-weight: 600; cursor: pointer; transition: all 0.3s; font-family: inherit; -webkit-tap-highlight-color: transparent; }
.menu-tab:hover, .menu-tab.active { background: linear-gradient(135deg, var(--primary), var(--primary-dark)); border-color: var(--primary); color: #fff; box-shadow: 0 4px 15px rgba(230,126,34,0.3); }
.menu-tab:active { transform: scale(0.96); }
.menu-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 24px; }
.menu-card { background: var(--bg-card); border: 1px solid var(--border); border-radius: 20px; overflow: hidden; transition: all 0.3s; cursor: pointer; -webkit-tap-highlight-color: transparent; }
.menu-card:hover { transform: translateY(-8px); border-color: rgba(230,126,34,0.3); box-shadow: 0 20px 40px rgba(0,0,0,0.3); }
.menu-card:active { transform: scale(0.98); }
.menu-card-image { position: relative; height: 200px; overflow: hidden; }
.menu-card-image img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.5s; }
.menu-card:hover .menu-card-image img { transform: scale(1.1); }
.menu-card-badge { position: absolute; top: 12px; left: 12px; background: rgba(231,76,60,0.9); color: #fff; padding: 4px 12px; border-radius: 8px; font-size: 11px; font-weight: 700; }
.menu-card-body { padding: 20px; }
.menu-card-body h4 { font-size: 18px; font-weight: 700; margin-bottom: 8px; }
.menu-card-body p { font-size: 14px; color: var(--text-muted); margin-bottom: 16px; line-height: 1.5; }
.menu-card-footer { display: flex; justify-content: space-between; align-items: center; }
.menu-card-price { font-size: 20px; font-weight: 800; color: var(--primary); }
.menu-card-rating { font-size: 14px; color: #f1c40f; }
.menu-card-add { width: 36px; height: 36px; border-radius: 50%; background: linear-gradient(135deg, var(--primary), var(--primary-dark)); border: none; color: #fff; font-size: 18px; cursor: pointer; display: flex; align-items: center; justify-content: center; transition: all 0.3s; -webkit-tap-highlight-color: transparent; }
.menu-card-add:hover { transform: scale(1.1); }
.menu-card-add:active { transform: scale(0.9); }

.offers-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 24px; }
.offer-card-website { background: linear-gradient(135deg, rgba(230,126,34,0.1), rgba(211,84,0,0.04)); border: 1px solid rgba(230,126,34,0.15); border-radius: 20px; padding: 32px; position: relative; overflow: hidden; transition: all 0.3s; }
.offer-card-website:hover { border-color: rgba(230,126,34,0.3); transform: translateY(-4px); }
.offer-card-website .badge { display: inline-block; background: var(--primary); color: #fff; padding: 6px 14px; border-radius: 8px; font-size: 12px; font-weight: 800; margin-bottom: 16px; text-transform: uppercase; letter-spacing: 1px; }
.offer-card-website h4 { font-size: 22px; font-weight: 800; margin-bottom: 8px; }
.offer-card-website p { color: var(--text-muted); margin-bottom: 20px; font-size: 15px; }
.offer-card-website .code { display: inline-block; background: rgba(230,126,34,0.15); border: 2px dashed rgba(230,126,34,0.4); color: var(--primary); padding: 8px 20px; border-radius: 8px; font-size: 18px; font-weight: 800; letter-spacing: 2px; margin-bottom: 16px; cursor: pointer; transition: all 0.3s; -webkit-tap-highlight-color: transparent; user-select: all; }
.offer-card-website .code:hover { background: rgba(230,126,34,0.25); }
.offer-card-website .code:active { transform: scale(0.97); }

.gallery-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; }
.gallery-item { position: relative; border-radius: 16px; overflow: hidden; aspect-ratio: 1; cursor: pointer; -webkit-tap-highlight-color: transparent; }
.gallery-item img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.5s; }
.gallery-item:hover img { transform: scale(1.15); }
.gallery-overlay { position: absolute; inset: 0; background: rgba(0,0,0,0.6); display: flex; align-items: center; justify-content: center; opacity: 0; transition: all 0.3s; }
.gallery-item:hover .gallery-overlay { opacity: 1; }
.gallery-overlay span { font-size: 32px; }

.testimonials-section { background: var(--bg-section); }
.testimonials-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(350px, 1fr)); gap: 24px; }
.testimonial-card { background: var(--bg-card); border: 1px solid var(--border); border-radius: 20px; padding: 28px; transition: all 0.3s; }
.testimonial-card:hover { border-color: rgba(230,126,34,0.2); }
.testimonial-stars { color: #f1c40f; font-size: 18px; margin-bottom: 16px; }
.testimonial-text { font-size: 16px; color: var(--text-muted); line-height: 1.7; margin-bottom: 20px; }
.testimonial-author { display: flex; align-items: center; gap: 12px; }
.testimonial-author img { width: 48px; height: 48px; border-radius: 50%; object-fit: cover; border: 2px solid var(--primary); }
.testimonial-author h5 { font-size: 15px; font-weight: 700; }
.testimonial-author p { font-size: 13px; color: var(--text-dim); margin: 0; }

.contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: start; }
.contact-info h3 { font-size: 32px; font-weight: 800; margin-bottom: 16px; }
.contact-info h3 span { color: var(--primary); }
.contact-info > p { color: var(--text-muted); margin-bottom: 32px; line-height: 1.7; }
.contact-details { display: flex; flex-direction: column; gap: 20px; }
.contact-item { display: flex; align-items: flex-start; gap: 16px; background: var(--bg-card); border: 1px solid var(--border); padding: 20px; border-radius: 16px; }
.contact-item .icon { width: 48px; height: 48px; border-radius: 12px; background: rgba(230,126,34,0.15); display: flex; align-items: center; justify-content: center; font-size: 20px; flex-shrink: 0; }
.contact-item h4 { font-size: 15px; font-weight: 700; margin-bottom: 4px; }
.contact-item p { font-size: 14px; color: var(--text-muted); margin: 0; }
.contact-item a { color: var(--primary); text-decoration: none; font-size: 14px; }
.contact-item a:hover { text-decoration: underline; }

.contact-form { background: var(--bg-card); border: 1px solid var(--border); border-radius: 24px; padding: 40px; }
.contact-form h4 { font-size: 22px; font-weight: 800; margin-bottom: 24px; }
.form-group { margin-bottom: 20px; }
.form-group label { display: block; font-size: 14px; font-weight: 600; margin-bottom: 8px; color: var(--text-muted); }
.form-group input, .form-group textarea, .form-group select { width: 100%; background: rgba(255,255,255,0.05); border: 1px solid var(--border); border-radius: 12px; padding: 14px 16px; color: var(--text); font-size: 15px; font-family: inherit; outline: none; transition: all 0.3s; -webkit-appearance: none; appearance:
