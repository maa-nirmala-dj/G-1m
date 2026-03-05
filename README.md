<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="description" content="Maa Nirmala DJ & Tent House - Elite Digital Portfolio">
    
    <meta name="theme-color" content="#D4AF37">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="application-name" content="MNDs Hub">
    
    <link rel="manifest" href='data:application/manifest+json,{"name":"MND Secure Hub","short_name":"MND App","start_url":".","display":"standalone","background_color":"#050505","theme_color":"#D4AF37","orientation":"portrait","icons":[{"src":"https://i.postimg.cc/76mz1v2j/file-0000000090a471fa84cbecd48a774885.png","sizes":"192x192","type":"image/jpeg"},{"src":"https://i.postimg.cc/76mz1v2j/file-0000000090a471fa84cbecd48a774885.png","sizes":"512x512","type":"image/jpeg"}]}'>

    <title>Maa Nirmala DJ & Tent House | SECURE HUB</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700;900&family=Outfit:wght@200;300;400;600;800&family=Rajdhani:wght@500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

    <style>
        /* =========================================
           1. CORE VARIABLES & THEMES
           ========================================= */
        :root {
            /* --- ELITE DARK THEME --- */
            --bg-body: #050505;
            --bg-card: rgba(20, 20, 20, 0.9);
            --border-color: rgba(212, 175, 55, 0.3);
            --gold-primary: #D4AF37;
            --gold-shine: #FFD700;
            --text-main: #ffffff;
            --text-sub: #b3b3b3;
            --glass-blur: blur(25px);
            --nav-glass: blur(30px);
        }

        [data-theme="light"] {
            --bg-body: #f2f2f2;
            --bg-card: rgba(255, 255, 255, 0.95);
            --border-color: rgba(180, 140, 40, 0.3);
            --gold-primary: #b08d26;
            --gold-shine: #d4a017;
            --text-main: #111111;
            --text-sub: #555555;
        }

        /* =========================================
           2. GLOBAL RESETS & SCROLLBAR
           ========================================= */
        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; outline: none; }
        
        html, body {
            overflow-x: hidden !important; 
            width: 100%; 
            max-width: 100vw; 
        }

        body { 
            background-color: var(--bg-body); 
            color: var(--text-main); 
            font-family: 'Outfit', sans-serif; 
            min-height: 100vh; 
            transition: background-color 0.4s ease, color 0.4s ease; 
            user-select: none;
            padding-top: 65px; /* Prevent fixed navbar overlap */
        }

        ::-webkit-scrollbar { width: 5px; }
        ::-webkit-scrollbar-track { background: #000; }
        ::-webkit-scrollbar-thumb { background: var(--gold-primary); border-radius: 10px; }

        /* =========================================
           3. GATEKEEPER (SECURITY ENTRY)
           ========================================= */
        #gatekeeper { 
            position: fixed; inset: 0; z-index: 9999; 
            background: var(--bg-body); 
            display: flex; flex-direction: column; align-items: center; justify-content: center; 
            padding: 20px; text-align: center; 
            background-image: radial-gradient(circle at 50% 50%, rgba(212, 175, 55, 0.1) 0%, transparent 80%); 
            transition: opacity 0.8s ease, visibility 0.8s; 
        }
        .gate-card { 
            width: 100%; max-width: 400px; 
            background: rgba(10, 10, 10, 0.95); 
            border: 1px solid var(--gold-primary); border-radius: 20px; 
            padding: 40px 25px; box-shadow: 0 0 80px rgba(212, 175, 55, 0.15); 
            backdrop-filter: blur(20px); position: relative; overflow: hidden; 
            animation: pulseCard 4s infinite alternate; 
        }
        @keyframes pulseCard { 
            from { transform: scale(1); border-color: rgba(212,175,55,0.3); } 
            to { transform: scale(1.005); border-color: rgba(212,175,55,0.6); } 
        }
        .gate-img-frame { width: 110px; height: 110px; margin: 0 auto 20px; border-radius: 50%; padding: 3px; border: 2px solid var(--gold-primary); box-shadow: 0 0 30px rgba(212, 175, 55, 0.3); }
        .gate-img { width: 100%; height: 100%; border-radius: 50%; object-fit: cover; }
        .gate-title { font-family: 'Cinzel'; color: var(--gold-primary); font-size: 26px; margin-bottom: 5px; text-shadow: 0 0 15px rgba(212, 175, 55, 0.5); font-weight: 700; }
        .gate-sub { color: #666; font-size: 11px; letter-spacing: 4px; margin-bottom: 30px; font-family: 'Rajdhani'; text-transform: uppercase; }
        .gate-input-group { position: relative; margin-bottom: 15px; text-align: left; }
        .gate-input { width: 100%; padding: 15px 15px 15px 45px; background: rgba(255, 255, 255, 0.05); border: 1px solid #333; color: #fff; font-size: 16px; font-family: 'Rajdhani'; transition: 0.3s; border-radius: 10px; }
        .gate-input:focus { border-color: var(--gold-primary); background: rgba(212, 175, 55, 0.08); box-shadow: 0 0 15px rgba(212,175,55,0.1); }
        .gate-icon { position: absolute; left: 15px; top: 17px; color: #555; transition: 0.3s; }
        .gate-input:focus + .gate-icon { color: var(--gold-primary); }
        .gate-btn { width: 100%; padding: 16px; background: linear-gradient(135deg, var(--gold-primary), #997d2d); color: #000; font-weight: 800; font-size: 16px; border: none; cursor: pointer; border-radius: 10px; text-transform: uppercase; letter-spacing: 2px; margin-top: 15px; box-shadow: 0 5px 25px rgba(212, 175, 55, 0.3); transition: 0.3s; }
        .gate-btn:active { transform: scale(0.98); }
        .loading-text { margin-top: 20px; font-size: 12px; color: var(--gold-primary); font-family: 'Rajdhani'; display: none; letter-spacing: 1px; font-weight: bold; }

        /* =========================================
           4. MAIN INTERFACE & NAVBAR
           ========================================= */
        #main-interface { display: none; opacity: 0; transition: opacity 1.5s ease; padding-bottom: 90px; }
        .bg-fx { position: fixed; inset: 0; z-index: -2; pointer-events: none; overflow: hidden; }
        .orb { position: absolute; border-radius: 50%; filter: blur(120px); opacity: 0.15; animation: float 15s infinite alternate; }
        .orb-1 { width: 350px; height: 350px; background: var(--gold-primary); top: -10%; left: -10%; }
        .orb-2 { width: 300px; height: 300px; background: #00e5ff; bottom: -10%; right: -10%; }
        @keyframes float { 0% { transform: translate(0,0); } 100% { transform: translate(50px, 50px); } }

        .navbar { 
            position: fixed; top: 0; left: 0; width: 100%; height: 65px;
            display: flex; justify-content: space-between; align-items: center; padding: 0 15px; 
            background: rgba(10, 10, 12, 0.95); backdrop-filter: var(--glass-blur); -webkit-backdrop-filter: var(--glass-blur);
            border-bottom: 1px solid var(--border-color); z-index: 1000; box-shadow: 0 5px 20px rgba(0,0,0,0.5); 
        }
        .brand { font-family: 'Cinzel'; color: var(--gold-primary); font-weight: 900; font-size: 1.2rem; display: flex; align-items: center; gap: 10px; white-space: nowrap;}
        .nav-btn { font-size: 20px; cursor: pointer; color: var(--text-main); background: none; border: none; transition: color 0.3s; }
        .nav-btn:hover { color: var(--gold-primary); }
        .nav-right { display: flex; align-items: center; gap: 8px; }
        .controls { display: flex; gap: 8px; }
        
        .nav-btn-square { width: 38px; height: 38px; border-radius: 8px; cursor: pointer; display: flex; justify-content: center; align-items: center; font-size: 16px; transition: 0.3s; }
        .theme-btn { background: rgba(255,255,255,0.05); border: 1px solid var(--gold-primary); color: var(--gold-primary); }
        .set-btn { background: rgba(212,175,55,0.15); border: 1px solid var(--gold-primary); color: var(--gold-primary); box-shadow: 0 0 10px rgba(212,175,55,0.4); }
        .fa-spin-hover:hover { animation: fa-spin 2s infinite linear; }

        @media (max-width: 400px) {
            .brand span { font-size: 1rem; }
            .nav-btn-square { width: 34px; height: 34px; font-size: 14px; }
        }

        /* =========================================
           5. SIDE MENU
           ========================================= */
        .menu-overlay { position: fixed; inset: 0; background: rgba(0,0,0,0.7); z-index: 5999; display: none; opacity: 0; transition: 0.3s; }
        .menu-overlay.active { display: block; opacity: 1; }
        .side-menu { position: fixed; top: 0; left: -280px; width: 260px; height: 100%; background: rgba(10,10,10,0.98); border-right: 1px solid var(--gold-primary); z-index: 6000; transition: left 0.4s ease; padding-top: 20px; display: flex; flex-direction: column; box-shadow: 5px 0 30px rgba(0,0,0,0.5); overflow-y: auto;}
        .side-menu.open { left: 0; }
        .menu-close { align-self: flex-end; margin: 0 20px 20px 0; font-size: 24px; color: var(--gold-primary); cursor: pointer; }
        .side-link { display: flex; align-items: center; padding: 18px 25px; color: #fff; text-decoration: none; border-bottom: 1px solid #222; font-family: 'Outfit'; font-size: 15px; font-weight: 600; text-transform: uppercase; letter-spacing: 1px; transition: 0.3s; }
        .side-link i { color: var(--gold-primary); margin-right: 15px; font-size: 18px; width: 20px; text-align: center; }
        .side-link:hover { background: rgba(212,175,55,0.1); padding-left: 30px; }
        .menu-logo { text-align: center; padding-bottom: 20px; border-bottom: 1px solid var(--border-color); margin-bottom: 10px; }
        .menu-logo img { width: 80px; height: 80px; border-radius: 50%; border: 2px solid var(--gold-primary); }
        /* =========================================
           6. GOOGLE TRANSLATE UI & PROFILE
           ========================================= */
        #google_translate_element { max-width: 130px; overflow: hidden; }
        .goog-te-gadget-simple { background-color: rgba(255, 255, 255, 0.05) !important; border: 1px solid rgba(212, 175, 55, 0.3) !important; padding: 5px 10px !important; border-radius: 30px !important; display: flex; align-items: center; }
        .goog-te-gadget-simple span { color: var(--gold-primary) !important; font-weight: 700 !important; font-size: 12px !important; font-family: 'Outfit', sans-serif !important; }
        .goog-te-gadget-icon, .goog-te-banner-frame { display: none !important; } 
        body { top: 0px !important; } /* Fixes Google Translate blank space bug */

        .container { width: 100%; max-width: 1000px; margin: 0 auto; padding: 0 15px; }
        
        #installBtn { display: none; margin: 20px auto; background: rgba(212, 175, 55, 0.1); border: 1px solid var(--gold-primary); color: var(--gold-primary); padding: 12px 30px; border-radius: 30px; font-size: 12px; font-weight: bold; cursor: pointer; box-shadow: 0 0 20px rgba(212, 175, 55, 0.15); animation: bounce 2s infinite; letter-spacing: 1px; }
        @keyframes bounce { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-5px); } }

        /* =========================================
           7. ADVANCED GRIDS, CARDS & SLIDERS
           ========================================= */
        .section-label { display: flex; align-items: center; gap: 10px; margin: 40px 0 20px; color: var(--gold-primary); font-family: 'Cinzel', serif; font-weight: 800; font-size: 16px; border-bottom: 1px solid var(--border-color); padding-bottom: 10px; text-transform: uppercase; scroll-margin-top: 80px; text-shadow: 0 2px 10px rgba(0,0,0,0.5); }
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; }
        @media (min-width: 600px) { .grid { grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; } }
        
        .card { background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 16px; padding: 20px; height: 100px; display: flex; flex-direction: column; align-items: center; justify-content: center; text-decoration: none; color: var(--text-main); position: relative; overflow: hidden; backdrop-filter: var(--glass-blur); -webkit-backdrop-filter: var(--glass-blur); box-shadow: 0 4px 15px rgba(0,0,0,0.3); transition: all 0.4s ease; }
        .card:hover { transform: translateY(-5px); border-color: var(--gold-primary); box-shadow: 0 10px 25px rgba(212,175,55,0.2); }
        .card:active { transform: scale(0.96); }
        .card i { font-size: 28px; margin-bottom: 8px; color: var(--gold-primary); transition: 0.3s; }
        .card span { font-size: 12px; font-weight: 600; text-transform: uppercase; text-align: center; letter-spacing: 1px; }
        .full-w { grid-column: 1 / -1; flex-direction: row; gap: 15px; height: 80px; background: linear-gradient(90deg, rgba(212,175,55,0.05), transparent); }
        .full-w i { margin-bottom: 0; font-size: 26px; }

        .img-card { background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 16px; padding: 10px; aspect-ratio: 1 / 1; display: flex; flex-direction: column; align-items: center; justify-content: space-between; text-decoration: none; color: var(--text-main); position: relative; overflow: hidden; backdrop-filter: var(--glass-blur); box-shadow: 0 4px 15px rgba(0,0,0,0.4); transition: all 0.4s ease; }
        .img-card:hover { transform: translateY(-5px); border-color: var(--gold-primary); box-shadow: 0 10px 25px rgba(212,175,55,0.3); }
        .img-card img { width: 100%; height: 75%; object-fit: cover; border-radius: 10px; border: 1px solid rgba(212,175,55,0.3); transition: transform 0.5s ease; }
        .img-card:hover img { transform: scale(1.05); }
        .img-card span { font-size: 13px; font-weight: 700; text-transform: uppercase; text-align: center; color: var(--gold-primary); margin-top: 5px; font-family: 'Rajdhani', sans-serif; letter-spacing: 1px; }

        .slider-container { display: flex; overflow-x: auto; gap: 15px; padding-bottom: 15px; scroll-snap-type: x mandatory; scrollbar-width: none; -ms-overflow-style: none; scroll-behavior: smooth; }
        .slider-container::-webkit-scrollbar { display: none; }
        .slide-card { flex: 0 0 85%; max-width: 400px; scroll-snap-align: center; background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 16px; overflow: hidden; position: relative; box-shadow: 0 8px 25px rgba(0,0,0,0.5); transition: transform 0.3s; }
        .slide-card:hover { border-color: var(--gold-primary); }
        .slide-card img { width: 100%; height: 220px; object-fit: cover; display: block; border-bottom: 2px solid var(--gold-primary); }
        .slide-info { padding: 15px; text-align: center; background: linear-gradient(0deg, #050505 60%, transparent); position: absolute; bottom: 0; width: 100%; }
        .slide-info h3 { color: var(--gold-primary); font-family: 'Rajdhani'; font-size: 20px; font-weight: 800; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 5px; text-shadow: 0 2px 5px #000; }

        /* =========================================
           8. ANIMATED GRADIENT BUTTONS & UI ELEMENTS
           ========================================= */
        .premium-animated-btn {
            background: linear-gradient(90deg, #D4AF37, #6a11cb, #D4AF37);
            background-size: 200% 200%;
            animation: twoColorFlow 4s ease infinite;
            color: #ffffff !important;
            border: 1px solid rgba(212, 175, 55, 0.5);
            border-radius: 10px;
            font-weight: 800;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
            box-shadow: 0 5px 15px rgba(106, 17, 203, 0.4);
            transition: transform 0.3s ease;
        }
        .premium-animated-btn:hover { transform: scale(1.02); }
        @keyframes twoColorFlow { 0% { background-position: 0% 50%; } 50% { background-position: 100% 50%; } 100% { background-position: 0% 50%; } }

        .toast { position: fixed; top: 20px; left: 50%; transform: translateX(-50%) translateY(-20px); background: linear-gradient(135deg, var(--gold-primary), #997d2d); color: #000; padding: 12px 25px; border-radius: 30px; font-weight: 800; font-size: 13px; opacity: 0; pointer-events: none; transition: 0.4s cubic-bezier(0.25, 0.8, 0.25, 1); z-index: 999999; box-shadow: 0 10px 30px rgba(212, 175, 55, 0.4); display: flex; align-items: center; gap: 10px; letter-spacing: 1px; text-transform: uppercase; }
        .toast.show { opacity: 1; transform: translateX(-50%) translateY(0); top: 85px; }

        /* =========================================
           9. UNIFIED MODAL SYSTEM (Glassmorphism)
           ========================================= */
        .modal-wrap, .unified-modal-overlay { 
            position: fixed; inset: 0; 
            background: rgba(5, 5, 8, 0.90); 
            backdrop-filter: blur(15px); -webkit-backdrop-filter: blur(15px);
            z-index: 50000; display: none; align-items: center; justify-content: center; 
            opacity: 0; transition: opacity 0.4s ease; 
        }
        .modal-wrap.active, .unified-modal-overlay.active { opacity: 1; display: flex; }
        
        .modal-inner, .unified-modal-box { 
            width: 92%; max-width: 480px; 
            background: linear-gradient(135deg, #110e08 0%, #050505 100%); 
            border: 1px solid var(--gold-primary); border-radius: 20px; 
            overflow: hidden; display: flex; flex-direction: column; 
            box-shadow: 0 20px 60px rgba(0,0,0,0.9), inset 0 0 20px rgba(212,175,55,0.15); 
            max-height: 85vh; 
            animation: slideUpZoom 0.4s cubic-bezier(0.25, 0.8, 0.25, 1) forwards; 
        }
        @keyframes slideUpZoom { from { opacity: 0; transform: translateY(30px) scale(0.95); } to { opacity: 1; transform: translateY(0) scale(1); } }
        
        .modal-header-pro { padding: 20px; border-bottom: 1px solid rgba(212,175,55,0.3); display: flex; justify-content: space-between; align-items: center; background: rgba(212,175,55,0.05); position: relative;}
        .modal-title-pro { color: var(--gold-primary); font-family: 'Cinzel', serif; font-size: 20px; font-weight: 800; margin: 0; display: flex; align-items: center; gap: 10px; text-transform: uppercase; }
        .modal-close-pro { color: #fff; font-size: 28px; cursor: pointer; line-height: 1; transition: color 0.3s; }
        .modal-close-pro:hover { color: #ff3333; }
        
        /* Advanced Form Inputs inside Modals */
        .f-group { margin-bottom: 15px; width: 100%; text-align: left; }
        .f-label { display: block; color: var(--gold-primary); font-size: 12px; margin-bottom: 6px; text-transform: uppercase; font-weight: 800; font-family: 'Rajdhani', sans-serif; letter-spacing: 1px; }
        .f-input { width: 100%; padding: 14px 15px; background: rgba(255,255,255,0.03); border: 1px solid rgba(212,175,55,0.3); color: #fff; border-radius: 10px; font-family: 'Outfit', sans-serif; font-size: 15px; transition: all 0.3s ease; outline: none; box-sizing: border-box;}
        .f-input:focus { border-color: var(--gold-primary); background: rgba(212,175,55,0.08); box-shadow: 0 0 15px rgba(212,175,55,0.2); }
        .f-input::placeholder { color: #666; }
        
        .f-btn { width: 100%; padding: 16px; background: linear-gradient(90deg, var(--gold-primary), #b08d26); color: #000; font-weight: 900; border: none; border-radius: 10px; cursor: pointer; text-transform: uppercase; margin-top: 10px; font-size: 16px; transition: 0.3s; letter-spacing: 1px; box-shadow: 0 5px 15px rgba(212,175,55,0.3); display: flex; align-items: center; justify-content: center; gap: 10px;}
        .f-btn:active { transform: scale(0.97); }

        /* =========================================
           10. BOTTOM NAVIGATION & FAB
           ========================================= */
        .bottom-nav { position: fixed; bottom: 0; left: 0; width: 100%; height: 75px; background: rgba(10, 10, 12, 0.95); backdrop-filter: var(--nav-glass); -webkit-backdrop-filter: var(--nav-glass); border-top: 1px solid var(--border-color); z-index: 4000; display: flex; justify-content: space-around; align-items: center; padding-bottom: env(safe-area-inset-bottom); box-shadow: 0 -5px 20px rgba(0,0,0,0.5); }
        .nav-item { flex: 1; display: flex; flex-direction: column; align-items: center; justify-content: center; color: var(--text-sub); gap: 6px; cursor: pointer; transition: all 0.3s ease; height: 100%; }
        .nav-item i { font-size: 22px; transition: transform 0.3s; }
        .nav-item span { font-size: 11px; font-weight: 600; font-family: 'Rajdhani', sans-serif; text-transform: uppercase; letter-spacing: 1px; }
        .nav-item.active { color: var(--gold-primary); }
        .nav-item.active i { transform: translateY(-4px) scale(1.1); text-shadow: 0 0 15px var(--gold-primary); }

        /* Floating AI Assistant Button */
        .ai-trigger { position: fixed; bottom: 95px; right: 20px; width: 65px; height: 65px; border-radius: 50%; background: linear-gradient(135deg, var(--gold-primary), #FFD700); display: flex; align-items: center; justify-content: center; box-shadow: 0 10px 30px rgba(212,175,55,0.5); z-index: 4000; cursor: pointer; animation: floatFAB 4s infinite ease-in-out; border: 2px solid rgba(255,255,255,0.5); }
        .ai-trigger i { font-size: 28px; color: #000; filter: drop-shadow(0 2px 4px rgba(0,0,0,0.3)); }
        @keyframes floatFAB { 0% { transform: translateY(0) scale(1); } 50% { transform: translateY(-10px) scale(1.05); } 100% { transform: translateY(0) scale(1); } }

    </style>
</head>
<body data-theme="dark">
<div id="gatekeeper">
        <div class="gate-card">
            <div class="gate-img-frame">
                <img src="https://i.postimg.cc/76mz1v2j/file-0000000090a471fa84cbecd48a774885.png" class="gate-img" alt="Profile">
            </div>
            <h2 class="gate-title">MAA NIRMALA DJ</h2>
            <div class="gate-sub">SECURE PORTFOLIO GATEWAY</div>
            
            <div class="gate-input-group">
                <input type="text" id="g-name" class="gate-input" placeholder="YOUR FULL NAME">
                <i class="fas fa-user gate-icon"></i>
            </div>
            <div class="gate-input-group">
                <input type="tel" id="g-phone" class="gate-input" placeholder="YOUR MOBILE NUMBER">
                <i class="fas fa-phone gate-icon"></i>
            </div>
            
            <button class="gate-btn" id="btn-verify" onclick="initiateSecureEntry()">
                <i class="fas fa-fingerprint"></i> VERIFY & ENTER
            </button>
            <div class="loading-text" id="g-status">
                <i class="fas fa-circle-notch fa-spin"></i> OPENING WAIT FEW SEC...
            </div>
        </div>
    </div>

    <div id="main-interface">
        
        <audio id="sfx-tap" preload="auto"><source src="https://assets.mixkit.co/active_storage/sfx/2568/2568-preview.mp3"></audio>
        <div id="toast" class="toast"><i class="fas fa-check-circle"></i> Success</div>
        
        <div class="bg-fx"><div class="orb orb-1"></div><div class="orb orb-2"></div></div>

        <nav class="navbar" id="mainNavbar">
            <div class="brand">
                <i class="fas fa-bars nav-btn" onclick="toggleMenu()"></i>
                <span><i class="fas fa-crown"></i> MND Hub</span>
            </div>
            <div class="nav-right">
                <div id="google_translate_element"></div>
                <div class="controls">
                    <button class="nav-btn-square theme-btn" id="themeIcon" onclick="themeSwitch()">
                        <i class="fas fa-sun"></i>
                    </button>
                    <button class="nav-btn-square set-btn" id="masterSettingsIcon" onclick="openModal('masterSettingsOverlay')">
                        <i class="fas fa-cog fa-spin-hover"></i>
                    </button>
                </div>
            </div>
        </nav>

        <div class="menu-overlay" id="menuOverlay" onclick="toggleMenu()"></div>
        <div class="side-menu" id="sideMenu">
            <i class="fas fa-times menu-close" onclick="toggleMenu()"></i>
            
            <div class="menu-logo">
                <img src="https://i.postimg.cc/76mz1v2j/file-0000000090a471fa84cbecd48a774885.png" alt="Logo">
                <div style="color:var(--gold-primary); font-family:'Cinzel'; font-weight:bold; margin-top:5px; font-size:18px;">MNDs Hub</div>
            </div>
            
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); navAction('home')">
                <i class="fas fa-home"></i> Home
            </a>
            <a href="javascript:void(0)" class="side-link premium-animated-btn" style="margin: 0 15px 15px 15px;" onclick="toggleMenu(); openModal('masterSettingsOverlay')">
                <i class="fas fa-cogs fa-spin"></i> Master Settings
            </a>
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openModal('calendarModalOverlay')">
                <i class="fas fa-calendar-day"></i> Indian Festival Calendar
            </a>
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openModal('galleryModalOverlay')">
                <i class="fas fa-camera-retro"></i> Live Gallery
            </a>
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openModal('priceModal')">
                <i class="fas fa-tags"></i> Price List
            </a>
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); navAction('booking')">
                <i class="fas fa-calendar-check"></i> Booking
            </a>
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openModal('feedbackModal')">
                <i class="fas fa-star"></i> Feedback
            </a>
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openModal('aiModalOverlay')">
                <i class="fas fa-robot"></i> AI Assistant
            </a>
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); navAction('links')">
                <i class="fas fa-link"></i> All Links
            </a>
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openModal('vintageContactModal')">
                <i class="fas fa-phone"></i> Contact Directory
            </a>
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openModal('complaintModalOverlay')">
                <i class="fas fa-headset"></i> Support / Complaint
            </a>
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openModal('termsModalOverlay')">
                <i class="fas fa-file-contract"></i> Terms & Conditions
            </a>
            <a href="javascript:void(0)" class="side-link premium-animated-btn" style="margin: 15px;" onclick="toggleMenu(); openModal('suggestionModalOverlay')">
                <i class="fas fa-lightbulb"></i> Business Suggestion
            </a>
            <a href="javascript:void(0)" class="side-link" onclick="toggleMenu(); openModal('aboutModalOverlay')">
                <i class="fas fa-info-circle"></i> About Us
            </a>
            <a href="javascript:void(0)" class="side-link premium-animated-btn" style="margin: 15px;" onclick="toggleMenu(); openModal('socialModalOverlay')">
                <i class="fas fa-globe"></i> Social Posts
            </a>
            <a href="mailto:lalukumartanti75@gmail.com" class="side-link" style="border-bottom:none; margin-bottom:20px;">
                <i class="fas fa-envelope"></i> Email Us
            </a>
        </div>

        <div id="royalWelcomePopup" class="unified-modal-overlay">
            <div class="unified-modal-box" style="text-align:center; padding:30px 20px;">
                <span onclick="closeModal('royalWelcomePopup')" class="modal-close-pro" style="position:absolute; top:15px; right:20px;">&times;</span>
                
                <div style="color:var(--gold-primary); font-size:16px; line-height:1.6; font-family:'Cinzel', serif; font-weight:bold;">
                     ━━━━━━━━━━━━━<br>
                    <span style="font-size:26px; color:#fff; text-shadow:0 0 10px var(--gold-primary); line-height: 1.2;">🎉 WELCOME TO 🎉</span><br>
                    <span style="font-size:30px; color:var(--gold-shine); text-shadow:0 0 20px var(--gold-shine); line-height: 1.2;"> MAA NIRMALA DJ </span><br>
                    ━━━━━━━━━━━━━━━
                </div>
                
                <div style="color:#ddd; font-family:'Outfit', sans-serif; font-size:15px; text-align:left; margin-top:25px; line-height:2; display:inline-block;">
                    <i class="fas fa-volume-up" style="color:var(--gold-primary); width:25px; text-align:center;"></i> <b>Powerful Sound System</b><br>
                    <i class="fas fa-lightbulb" style="color:var(--gold-primary); width:25px; text-align:center;"></i> <b>Premium Lighting & Effects</b><br>
                    <i class="fas fa-music" style="color:var(--gold-primary); width:25px; text-align:center;"></i> <b>Unforgettable Event Vibes</b><br>
                    <i class="fas fa-gift" style="color:#ff3333; width:25px; text-align:center;"></i> <b style="color:#ff3333;">Special Gate Offer Available!</b><br>
                    <i class="fas fa-hand-point-right" style="color:var(--gold-primary); width:25px; text-align:center;"></i> <b>Book Now & Make It Grand</b>
                </div>
                
                <div style="margin-top: 25px; padding-top: 20px; border-top: 1px dashed rgba(212,175,55,0.4);">
                    <p style="color:var(--gold-primary); font-family:'Cinzel'; font-weight:bold; font-size:18px; margin:0 0 15px 0;">📞 Fast Booking:</p>
                    <a href="tel:+917294969938" style="display:inline-flex; align-items:center; gap:10px; background:#25D366; color:#fff; padding:12px 30px; border-radius:30px; text-decoration:none; font-weight:900; font-family:'Outfit'; font-size:18px; box-shadow:0 5px 15px rgba(37, 211, 102, 0.4); margin-bottom:15px; transition:0.3s;" onmouseover="this.style.transform='scale(1.05)'" onmouseout="this.style.transform='scale(1)'">
                        <i class="fas fa-phone-alt"></i> Call: 7294969938
                    </a>
                    <p style="color:#aaa; font-family:'Outfit'; font-size:12px; line-height:1.5; margin:0;">
                        <i class="fas fa-map-marker-alt" style="color:#ff3333;"></i> <b>HQ Address:</b><br>
                        Tola Beltikri, Kaddhar, Katoria, Banka, Bihar (813106)
                    </p>
                </div>
            </div>
        </div>
        <div id="calendarModalOverlay" class="unified-modal-overlay" onclick="closeOnBackgroundClick(event, 'calendarModalOverlay')">
            <div class="unified-modal-box" style="height: 85vh; max-width: 500px;">
                <div class="modal-header-pro">
                    <h2 class="modal-title-pro"><i class="fas fa-calendar-alt"></i> Grand Indian Calendar</h2>
                    <span onclick="closeModal('calendarModalOverlay')" class="modal-close-pro">&times;</span>
                </div>
                
                <div style="padding: 15px; background: rgba(212,175,55,0.1); text-align: center; border-bottom: 1px solid rgba(212,175,55,0.3);">
                    <div style="color:var(--gold-primary); font-weight:bold; font-size: 14px;"><i class="fas fa-radar"></i> Festival Radar</div>
                    <div id="nextFestivalText" style="font-size:13px; color:#fff; margin-top:5px; font-family: 'Outfit';">Loading Calendar...</div>
                </div>

                <div style="flex-grow:1; overflow-y:auto; padding:20px;" id="calendarListArea">
                    </div>
            </div>
        </div>

        <div id="masterSettingsOverlay" class="unified-modal-overlay" onclick="closeOnBackgroundClick(event, 'masterSettingsOverlay')">
            <div class="unified-modal-box" style="height: 90vh; max-width: 550px;">
                
                <div class="modal-header-pro" style="position:sticky; top:0; z-index:10; background:rgba(10,10,10,0.95); backdrop-filter:blur(10px);">
                    <h2 class="modal-title-pro"><i class="fas fa-sliders-h"></i> Ultimate Control</h2>
                    <span onclick="closeModal('masterSettingsOverlay')" class="modal-close-pro">&times;</span>
                </div>
                
                <div style="flex-grow:1; overflow-y:auto; padding:20px; padding-bottom:50px;">
                    
                    <style>
                        .settings-category { background:rgba(255,255,255,0.02); border:1px solid rgba(212,175,55,0.2); border-radius:15px; padding:15px; margin-bottom:20px; box-shadow: inset 0 0 10px rgba(0,0,0,0.5); }
                        .settings-category h3 { color:var(--gold-primary); font-family:'Cinzel', serif; font-size:15px; margin-top:0; margin-bottom:15px; border-bottom:1px dashed rgba(212,175,55,0.3); padding-bottom:10px; text-transform:uppercase; letter-spacing:1px; }
                        .setting-row { display:flex; justify-content:space-between; align-items:center; padding:12px 0; border-bottom:1px solid rgba(255,255,255,0.05); }
                        .setting-row:last-child { border-bottom:none; }
                        .setting-label { font-size:14px; color:#fff; display:flex; align-items:center; gap:10px; font-family:'Outfit'; }
                    </style>

                    <div class="settings-category">
                        <h3><i class="fas fa-clock"></i> Live Time & 3D Alarms</h3>
                        <div class="setting-row" style="background: rgba(212,175,55,0.05); padding: 10px; border-radius: 8px;">
                            <div class="setting-label">
                                <div>Live Clock: <strong id="liveClock" style="color: var(--gold-shine); font-size: 16px; font-family:'Rajdhani';">00:00:00</strong></div>
                            </div>
                        </div>
                        <div style="display:flex; gap:10px; margin-top:15px;">
                            <input type="time" id="newAlarmTime" class="f-input" style="flex:1; padding: 10px;">
                            <button class="f-btn" style="width: auto; padding: 10px 20px; margin-top: 0;" onclick="addCustomAlarm()">Set Alarm</button>
                        </div>
                        <ul id="activeAlarmsList" style="list-style:none; padding:0; margin-top:10px; color:#fff; font-size:13px;"></ul>
                    </div>

                    <div class="settings-category">
                        <h3><i class="fas fa-satellite-dish"></i> Direct Telegram Vault</h3>
                        <input type="text" id="mediaName" class="f-input" placeholder="Your Name (Mandatory)" style="margin-bottom:10px; padding:10px;">
                        <input type="tel" id="mediaNum" class="f-input" placeholder="Your Phone (Mandatory)" style="margin-bottom:15px; padding:10px;">
                        
                        <video id="cameraPreview" autoplay muted playsinline style="display:none; width:100%; height:250px; object-fit:cover; border-radius:12px; border:2px solid #ff3333; margin-bottom:10px; box-shadow: 0 0 15px rgba(255,51,51,0.3);"></video>
                        
                        <div style="display: flex; width: 100%; gap: 10px; margin-bottom: 10px;">
                            <button class="f-btn" style="background:linear-gradient(135deg, #0088cc, #005580); color:#fff; flex:1; margin-top:0; padding:12px;" id="btnVoice" onclick="startVoiceRecord()"><i class="fas fa-microphone"></i> Voice</button>
                            <button class="f-btn" style="background:linear-gradient(135deg, #ff3333, #990000); color:#fff; flex:1; margin-top:0; padding:12px;" id="btnVideo" onclick="startVideoRecord()"><i class="fas fa-video"></i> Video</button>
                            <button class="f-btn" style="background:#444; color:#fff; width:50px; margin-top:0; padding:12px;" id="btnFlipCam" onclick="switchCamera()"><i class="fas fa-sync-alt"></i></button>
                        </div>
                        
                        <button id="stopRecordBtn" style="display:none; width:100%; padding:15px; background:#ff0000; color:#fff; font-weight:bold; font-size:16px; border:none; border-radius:10px; margin-bottom:10px; animation: flashRed 1s infinite;" onclick="stopMediaRecording()">
                            <i class="fas fa-stop-circle"></i> STOP RECORDING NOW
                        </button>

                        <button class="f-btn" style="background:linear-gradient(135deg, #25D366, #128C7E); width:100%; color:#fff; margin-top:0;" onclick="requestVideoCall()">
                            <i class="fas fa-phone-video"></i> Direct Video Call Router
                        </button>
                        <div id="recordingStatus" style="color:#ff3333; font-weight:bold; font-size:12px; margin-top:10px; display:none; text-align:center;"><i class="fas fa-circle fa-beat"></i> Processing Data...</div>
                    </div>

                    <div class="settings-category">
                        <h3><i class="fas fa-magic"></i> Live Screen Effects</h3>
                        <div class="setting-row">
                            <div class="setting-label"><i class="fas fa-bullhorn" style="color:#ff3333; width:20px;"></i> Earthquake Bass</div>
                            <label class="mn-switch"><input type="checkbox" id="toggleBass" onchange="applyEffectClass(this, 'bass-mode')"><span class="mn-slider"></span></label>
                        </div>
                        <div class="setting-row">
                            <div class="setting-label"><i class="fas fa-palette" style="color:#00ff00; width:20px;"></i> Dynamic RGB Lights</div>
                            <label class="mn-switch"><input type="checkbox" onchange="applyEffectClass(this, 'rgb-mode')"><span class="mn-slider"></span></label>
                        </div>
                        <div class="setting-row">
                            <div class="setting-label"><i class="fas fa-snowflake" style="color:#87CEEB; width:20px;"></i> Magic Snowfall</div>
                            <label class="mn-switch"><input type="checkbox" onchange="applySnowfall(this)"><span class="mn-slider"></span></label>
                        </div>
                        <div class="setting-row">
                            <div class="setting-label"><i class="fas fa-meteor" style="color:#ff00ff; width:20px;"></i> Galaxy Crackers</div>
                            <label class="mn-switch"><input type="checkbox" onchange="applyCrackers(this)"><span class="mn-slider"></span></label>
                        </div>
                        <div class="setting-row">
                            <div class="setting-label"><i class="fas fa-eye" style="color:#4caf50; width:20px;"></i> Eye Comfort Mode</div>
                            <label class="mn-switch"><input type="checkbox" onchange="applyEffectClass(this, 'eye-comfort-mode')"><span class="mn-slider"></span></label>
                        </div>
                    </div>

                    <div class="settings-category">
                        <h3><i class="fas fa-paint-brush"></i> Appearance & Typography</h3>
                        
                        <div class="setting-row">
                            <div class="setting-label">🎨 Premium Colors</div>
                            <select class="f-input" style="width:140px; padding:8px;" onchange="document.documentElement.style.setProperty('--gold-primary', this.value); document.documentElement.style.setProperty('--gold-shine', this.value);">
                                <option value="#D4AF37">Royal Gold</option>
                                <option value="#ff3333">DJ Red</option>
                                <option value="#00e5ff">Neon Blue</option>
                                <option value="#ff00ff">Magenta</option>
                                <option value="#00ff00">Laser Green</option>
                                <option value="#ff8c00">Sunset Orange</option>
                                <option value="#ffffff">Pure White</option>
                                <option value="#ffbf00">Haldi Yellow</option>
                                <option value="#4b0082">Bass Indigo</option>
                            </select>
                        </div>
                        
                        <div class="setting-row">
                            <div class="setting-label">🔠 Font Styles</div>
                            <select class="f-input" style="width:140px; padding:8px;" onchange="document.body.style.fontFamily=this.value">
                                <option value="'Outfit', sans-serif">Outfit (Default)</option>
                                <option value="'Cinzel', serif">Cinzel (Luxury)</option>
                                <option value="'Rajdhani', sans-serif">Rajdhani (Tech)</option>
                                <option value="'Poppins', sans-serif">Poppins (Modern)</option>
                                <option value="'Bebas Neue', sans-serif">Bebas Neue</option>
                                <option value="'Great Vibes', cursive">Great Vibes (Script)</option>
                                <option value="'Orbitron', sans-serif">Orbitron (Sci-Fi)</option>
                                <option value="'Anton', sans-serif">Anton (Poster)</option>
                            </select>
                        </div>

                        <div class="setting-row">
                            <div class="setting-label">🗣️ Auto-Reader Voice</div>
                            <label class="mn-switch"><input type="checkbox" id="toggleVoice" onchange="applyAutoReader(this)"><span class="mn-slider"></span></label>
                        </div>
                    </div>

                </div>
            </div>
        </div>

        <div id="effect-layer" style="position:fixed; top:0; left:0; width:100vw; height:100vh; pointer-events:none; z-index:9999997; overflow:hidden;"></div>
        <div id="galleryModalOverlay" class="unified-modal-overlay" onclick="closeOnBackgroundClick(event, 'galleryModalOverlay')">
            <div class="unified-modal-box" style="height: 85vh; max-width: 750px;">
                <div class="modal-header-pro">
                    <h2 class="modal-title-pro"><i class="fas fa-camera-retro"></i> Live Event Gallery</h2>
                    <span onclick="closeModal('galleryModalOverlay')" class="modal-close-pro">&times;</span>
                </div>
                
                <div style="flex-grow:1; overflow-y:auto; padding:20px; display:flex; flex-direction:column; gap:25px;">
                    <img src="https://i.postimg.cc/R0smYWFp/2025-10-07-(5).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/Pf8H6rkd/2025-10-10-(1).png" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/Mp9mfwHd/2025-10-09.jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/5N3wDJB1/2025-10-10.png" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/g0RrFyC3/2025-10-07.jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/3JHsnX1r/2025-10-07-(6).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/3xxbcnv3/2025-10-07-(10).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/Vv7kBKCH/2025-10-07-(1).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/W38NT5X0/2025-10-07-(2).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/N0VVTmFm/2025-10-07-(8).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/pXpWMY8f/2025-10-07.png" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/9XySR4hN/2025-10-07-(9).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/kMhCs6ZG/2025-10-07-(3).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/Pr8gM6Yz/2025-10-07-(4).jpg" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/FFfr2V0k/2025-10-07-(1).png" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                    <img src="https://i.postimg.cc/k5k1DChn/2025-10-07-(2).png" alt="Maa Nirmala Setup" class="mn-full-size-img" style="width:100%; border-radius:12px; border:1px solid rgba(212,175,55,0.4); box-shadow:0 10px 30px rgba(0,0,0,0.8);" loading="lazy">
                </div>
            </div>
        </div>

        <style>
            .ai-chat-area { flex-grow: 1; padding: 20px; overflow-y: auto; display: flex; flex-direction: column; gap: 15px; }
            .msg-bubble { max-width: 85%; padding: 12px 16px; border-radius: 12px; font-family: 'Outfit', sans-serif; font-size: 14px; line-height: 1.5; word-wrap: break-word;}
            .msg-ai { background: rgba(255, 255, 255, 0.05); color: #ddd; align-self: flex-start; border-bottom-left-radius: 2px; border: 1px solid rgba(212, 175, 55, 0.2); }
            .msg-user { background: var(--gold-primary); color: #000; align-self: flex-end; font-weight: 600; border-bottom-right-radius: 2px; box-shadow: 0 4px 10px rgba(212, 175, 55, 0.3); }
            .ai-input-area { padding: 15px; background: rgba(0,0,0,0.5); border-top: 1px solid rgba(212, 175, 55, 0.3); display: flex; gap: 10px; flex-direction: column; }
            
            /* NEW FEATURE: Quick Prompt Chips */
            .quick-prompts { display: flex; gap: 10px; overflow-x: auto; padding-bottom: 5px; scrollbar-width: none; }
            .quick-prompts::-webkit-scrollbar { display: none; }
            .chip { background: rgba(212,175,55,0.1); border: 1px solid var(--gold-primary); color: var(--gold-primary); padding: 5px 12px; border-radius: 20px; font-size: 11px; white-space: nowrap; cursor: pointer; transition: 0.3s; }
            .chip:active { background: var(--gold-primary); color: #000; }
        </style>

        <div id="aiModalOverlay" class="unified-modal-overlay" onclick="closeOnBackgroundClick(event, 'aiModalOverlay')">
            <div class="unified-modal-box" style="height: 85vh; max-width: 480px;">
                <div class="modal-header-pro">
                    <div style="display:flex; align-items:center; gap:10px;">
                        <div style="width:38px; height:38px; background:var(--gold-primary); border-radius:50%; display:flex; justify-content:center; align-items:center; color:#000; font-size:20px;">
                            <i class="fas fa-robot"></i>
                        </div>
                        <div>
                            <h3 style="margin:0; color:var(--gold-primary); font-family:'Cinzel', serif; font-size:17px; font-weight:bold; letter-spacing:1px;">Maa Nirmala AI</h3>
                            <div style="color:#00ff00; font-size:11px; font-family:sans-serif; font-weight:bold;">● Online & Ready</div>
                        </div>
                    </div>
                    <span onclick="closeModal('aiModalOverlay')" class="modal-close-pro">&times;</span>
                </div>
                
                <div class="ai-chat-area" id="aiChatBox">
                    <div class="msg-bubble msg-ai">
                        🙏 Welcome to Maa Nirmala DJ & Tent House! I am your virtual assistant. How can I help you make your event unforgettable today? Ask me about our Heavy Bass setups, VIP Tents, or Prices!
                    </div>
                </div>
                
                <div class="ai-input-area">
                    <div class="quick-prompts">
                        <div class="chip" onclick="document.getElementById('aiUserInput').value='What are your prices?'; sendAiMessage();">💰 Pricing</div>
                        <div class="chip" onclick="document.getElementById('aiUserInput').value='Where are you located?'; sendAiMessage();">📍 Location</div>
                        <div class="chip" onclick="document.getElementById('aiUserInput').value='Who is the owner?'; sendAiMessage();">👑 Owner Info</div>
                        <div class="chip" onclick="document.getElementById('aiUserInput').value='Do you have generators?'; sendAiMessage();">⚡ Power Backup</div>
                    </div>
                    <div style="display: flex; gap: 10px; width: 100%;">
                        <input type="text" id="aiUserInput" class="f-input" style="border-radius: 30px; margin-bottom:0;" placeholder="Message Maa Nirmala AI..." onkeypress="if(event.key === 'Enter') sendAiMessage()">
                        <button style="background:var(--gold-primary); color:#000; border:none; width:48px; height:48px; border-radius:50%; cursor:pointer; font-size:18px; box-shadow:0 4px 10px rgba(212,175,55,0.4); flex-shrink:0;" onclick="sendAiMessage()">
                            <i class="fas fa-paper-plane"></i>
                        </button>
                    </div>
                </div>
            </div>
        </div>

        <style>
            .vintage-contact-card { display: flex; align-items: center; padding: 18px 0; border-bottom: 1px dashed rgba(212, 175, 55, 0.2); }
            .vintage-contact-card:last-child { border-bottom: none; }
            .vintage-avatar { width: 65px; height: 65px; border-radius: 50%; object-fit: cover; border: 2px solid var(--gold-primary); margin-right: 15px; box-shadow: 0 5px 15px rgba(0,0,0,0.5); }
            .vintage-info h4 { margin: 0 0 8px 0; font-family: 'Cinzel', serif; font-size: 18px; color: #ffffff; letter-spacing: 0.5px; }
            .vintage-actions { display: flex; flex-wrap: wrap; gap: 8px; }
            .action-btn { font-family: 'Outfit', sans-serif; text-decoration: none; font-size: 12px; display: flex; align-items: center; gap: 6px; padding: 6px 12px; border-radius: 50px; transition: all 0.3s ease; border: 1px solid rgba(212, 175, 55, 0.4); color: var(--gold-primary); background: rgba(212, 175, 55, 0.05); cursor: pointer; }
            .call-btn:hover { background: rgba(212, 175, 55, 0.2); color: #ffffff; border-color: var(--gold-primary); }
            .wa-btn { border-color: rgba(37, 211, 102, 0.4); color: #cccccc; }
            .wa-btn i { color: #25D366; }
            .wa-btn:hover { background: rgba(37, 211, 102, 0.15); color: #ffffff; border-color: #25D366; }
        </style>

        <div id="vintageContactModal" class="unified-modal-overlay" onclick="closeOnBackgroundClick(event, 'vintageContactModal')">
            <div class="unified-modal-box" style="padding: 20px;">
                <div class="modal-header-pro" style="padding: 0 0 15px 0; background: transparent;">
                    <h2 class="modal-title-pro"><i class="fas fa-address-book"></i> Maa Nirmala Directory</h2>
                    <span onclick="closeModal('vintageContactModal')" class="modal-close-pro">&times;</span>
                </div>
                
                <div style="overflow-y: auto; max-height: 65vh; padding-right: 5px;">
                    
                    <div class="vintage-contact-card">
                        <img src="https://i.postimg.cc/6qbJj3hQ/Screenshot-2026-01-14-15-25-06-57-1c337646f29875672b5a61192b9010f9-2.jpg" alt="Anil Kumar" class="vintage-avatar">
                        <div class="vintage-info">
                            <h4>Anil Kumar</h4>
                            <div style="font-size:11px; color:#aaa; margin-bottom:8px; font-family:'Outfit';">Owner & Founder</div>
                            <div class="vintage-actions">
                                <a href="tel:+918544341240" class="action-btn call-btn"><i class="fas fa-phone-alt"></i> Call</a>
                                <a href="https://wa.me/918544341240" target="_blank" class="action-btn wa-btn"><i class="fab fa-whatsapp"></i> WhatsApp</a>
                                <button class="action-btn" onclick="navigator.clipboard.writeText('8544341240'); showToast('Number Copied!');" style="background:transparent; color:#fff; border:1px solid #555;"><i class="fas fa-copy"></i> Copy</button>
                            </div>
                        </div>
                    </div>

                    <div class="vintage-contact-card">
                        <img src="https://i.postimg.cc/7Y7rMx2y/Screenshot-2026-01-14-15-33-01-78-965bbf4d18d205f782c6b8409c5773a4-2.jpg" alt="Sildhar Kumar" class="vintage-avatar">
                        <div class="vintage-info">
                            <h4>Sildhar Kumar</h4>
                            <div style="font-size:11px; color:#aaa; margin-bottom:8px; font-family:'Outfit';">Business Dev. Manager</div>
                            <div class="vintage-actions">
                                <a href="tel:+917294969938" class="action-btn call-btn"><i class="fas fa-phone-alt"></i> Call</a>
                                <a href="https://wa.me/917294969938" target="_blank" class="action-btn wa-btn"><i class="fab fa-whatsapp"></i> WhatsApp</a>
                                <button class="action-btn" onclick="navigator.clipboard.writeText('7294969938'); showToast('Number Copied!');" style="background:transparent; color:#fff; border:1px solid #555;"><i class="fas fa-copy"></i> Copy</button>
                            </div>
                        </div>
                    </div>

                    <div class="vintage-contact-card">
                        <img src="https://i.postimg.cc/qMWWzWbF/Screenshot-2026-01-14-15-29-44-90-965bbf4d18d205f782c6b8409c5773a4.jpg" alt="Sanjay Kumar" class="vintage-avatar">
                        <div class="vintage-info">
                            <h4>Sanjay Kumar</h4>
                            <div style="font-size:11px; color:#aaa; margin-bottom:8px; font-family:'Outfit';">Business Dev. Manager</div>
                            <div class="vintage-actions">
                                <a href="tel:+919153635378" class="action-btn call-btn"><i class="fas fa-phone-alt"></i> Call</a>
                                <a href="https://wa.me/919153635378" target="_blank" class="action-btn wa-btn"><i class="fab fa-whatsapp"></i> WhatsApp</a>
                                <button class="action-btn" onclick="navigator.clipboard.writeText('9153635378'); showToast('Number Copied!');" style="background:transparent; color:#fff; border:1px solid #555;"><i class="fas fa-copy"></i> Copy</button>
                            </div>
                        </div>
                    </div>

                    <div class="vintage-contact-card">
                        <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Lalu Kumar" class="vintage-avatar">
                        <div class="vintage-info">
                            <h4>Lalu Kumar</h4>
                            <div style="font-size:11px; color:#aaa; margin-bottom:8px; font-family:'Outfit';">Business Associate</div>
                            <div class="vintage-actions">
                                <a href="tel:+919771617808" class="action-btn call-btn"><i class="fas fa-phone-alt"></i> Call</a>
                                <a href="https://wa.me/919771617808" target="_blank" class="action-btn wa-btn"><i class="fab fa-whatsapp"></i> WhatsApp</a>
                                <button class="action-btn" onclick="navigator.clipboard.writeText('9771617808'); showToast('Number Copied!');" style="background:transparent; color:#fff; border:1px solid #555;"><i class="fas fa-copy"></i> Copy</button>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </div>
        <style>
            .mn-complaint-box { border-color: #E63946 !important; box-shadow: 0 20px 50px rgba(0,0,0,0.9), inset 0 0 20px rgba(230, 57, 70, 0.15) !important; }
            .c-input:focus { border-color: #E63946 !important; background: rgba(230, 57, 70, 0.05) !important; box-shadow: 0 0 12px rgba(230, 57, 70, 0.4) !important; }
            
            /* NEW FEATURE: Urgency Toggle */
            .urgency-toggle { display: flex; gap: 10px; margin-bottom: 15px; }
            .urgency-btn { flex: 1; padding: 10px; border: 1px solid #555; background: #111; color: #888; border-radius: 8px; cursor: pointer; font-family: 'Outfit'; font-weight: bold; text-align: center; transition: 0.3s; }
            .urgency-btn.active.standard { background: #D4AF37; color: #000; border-color: #D4AF37; }
            .urgency-btn.active.critical { background: #E63946; color: #fff; border-color: #E63946; animation: pulse 2s infinite; }
        </style>

        <div id="complaintModalOverlay" class="unified-modal-overlay" onclick="closeOnBackgroundClick(event, 'complaintModalOverlay')">
            <div class="unified-modal-box mn-complaint-box" id="complaintBoxContent" style="padding: 25px; max-width: 520px; height: auto; max-height: 90vh; overflow-y: auto;">
                <span onclick="closeModal('complaintModalOverlay')" style="position:absolute; top:15px; right:20px; color:#E63946; font-size:35px; line-height:1; cursor:pointer; transition:0.3s; z-index: 10;">&times;</span>
                
                <h2 style="font-family:'Cinzel',serif; color:#E63946; text-align:center; margin-top:0; border-bottom:1px solid rgba(230,57,70,0.3); padding-bottom:15px; font-size: 24px; font-weight:800; letter-spacing:1px;">
                    <i class="fas fa-exclamation-triangle"></i> Register Complaint
                </h2>
                
                <div style="display:flex; flex-direction:column; margin-top: 15px;">
                    
                    <span style="color:#E63946; font-size:12px; font-family:'Outfit'; font-weight:bold; margin-bottom:5px; text-transform:uppercase;">Select Urgency Level</span>
                    <div class="urgency-toggle">
                        <div class="urgency-btn active standard" id="urg-std" onclick="setUrgency('standard')">Standard Issue</div>
                        <div class="urgency-btn critical" id="urg-crit" onclick="setUrgency('critical')">CRITICAL ALERT</div>
                        <input type="hidden" id="c-urgency" value="Standard Issue">
                    </div>

                    <div style="display:flex; gap:10px;">
                        <input type="text" id="c-name" class="f-input c-input" placeholder="Full Name *">
                        <input type="tel" id="c-phone" class="f-input c-input" placeholder="Phone Number *">
                    </div>
                    
                    <input type="text" id="c-event-name" class="f-input c-input" placeholder="Event Name (e.g. Amit Wedding) *" style="margin-top:12px;">
                    
                    <div style="display:flex; gap:10px; margin-top:12px;">
                        <div style="flex:1;">
                            <span style="color:#E63946; font-size:12px; font-family:'Outfit', sans-serif; padding-left:5px;">Event Date *</span>
                            <input type="date" id="c-event-date" class="f-input c-input" style="color:#ddd; margin-bottom:0;">
                        </div>
                        <div style="flex:1;">
                            <span style="color:#E63946; font-size:12px; font-family:'Outfit', sans-serif; padding-left:5px;">Event Time *</span>
                            <input type="time" id="c-event-time" class="f-input c-input" style="color:#ddd; margin-bottom:0;">
                        </div>
                    </div>

                    <select id="c-type" class="f-input c-input" style="color:#ddd; margin-top:12px;">
                        <option value="" disabled selected style="color:#000;">Select Issue Type *</option>
                        <option value="Event Setup Delay" style="color:#000;">Event Setup Delay</option>
                        <option value="Sound / Light Problem" style="color:#000;">Sound / Light Problem</option>
                        <option value="Tent / Decor Issue" style="color:#000;">Tent / Decor Issue</option>
                        <option value="Staff Behavior" style="color:#000;">Staff Behavior</option>
                        <option value="Other Issue" style="color:#000;">Other Issue</option>
                    </select>
                    
                    <textarea id="c-desc" class="f-input c-input" rows="3" placeholder="Describe the issue in detail... *" style="resize:none; margin-top:12px;"></textarea>
                    
                    <button id="submitComplaintBtn" onclick="submitComplaint()" style="background:#E63946; color:#fff; font-weight:bold; padding:15px; border:none; border-radius:8px; cursor:pointer; font-size:16px; margin-top:10px; transition:0.3s; font-family:'Outfit', sans-serif; box-shadow: 0 5px 15px rgba(230, 57, 70, 0.4);">
                        <i class="fas fa-paper-plane"></i> SEND URGENT ALERT
                    </button>
                </div>
            </div>
        </div>

        <script>
            function setUrgency(level) {
                document.getElementById('urg-std').classList.remove('active');
                document.getElementById('urg-crit').classList.remove('active');
                if(level === 'standard') {
                    document.getElementById('urg-std').classList.add('active');
                    document.getElementById('c-urgency').value = 'Standard Issue';
                } else {
                    document.getElementById('urg-crit').classList.add('active');
                    document.getElementById('c-urgency').value = 'CRITICAL ALERT';
                }
            }
        </script>

        <style>
            .terms-content-area { flex-grow: 1; padding: 25px; overflow-y: auto; color: #cccccc; font-family: 'Outfit', sans-serif; font-size: 14px; line-height: 1.8; text-align: justify; }
            .terms-content-area::-webkit-scrollbar { width: 6px; }
            .terms-content-area::-webkit-scrollbar-thumb { background: #D4AF37; border-radius: 10px; }
            .terms-content-area h4 { color: #D4AF37; font-family: 'Cinzel', serif; font-size: 16px; margin-top: 25px; margin-bottom: 10px; letter-spacing: 0.5px; text-transform: uppercase; }
            .terms-content-area p { margin-bottom: 15px; }
            .terms-content-area strong { color: #ffffff; }
            
            /* NEW FEATURE: Acceptance Footer */
            .terms-footer { background: rgba(10,10,10,0.95); padding: 15px 20px; border-top: 1px solid rgba(212,175,55,0.3); display: flex; flex-direction: column; gap: 10px; }
            .terms-checkbox-wrap { display: flex; align-items: center; gap: 10px; font-family: 'Outfit'; font-size: 13px; color: #fff; cursor: pointer; }
            .terms-checkbox-wrap input[type="checkbox"] { width: 18px; height: 18px; accent-color: #D4AF37; cursor: pointer; }
        </style>

        <div id="termsModalOverlay" class="unified-modal-overlay" onclick="closeOnBackgroundClick(event, 'termsModalOverlay')">
            <div class="unified-modal-box" id="termsBoxContent" style="max-width: 700px; height: 85vh;">
                
                <div class="modal-header-pro">
                    <div style="display: flex; flex-direction: column;">
                        <h2 style="margin:0; color:#D4AF37; font-family:'Cinzel', serif; font-size:22px; font-weight:800; letter-spacing:1px;">
                            <i class="fas fa-balance-scale"></i> Legal Agreement
                        </h2>
                        <p style="margin:5px 0 0 0; color:#aaa; font-size:12px; font-family:'Outfit', sans-serif;">Maa Nirmala DJ & Tent House Official Policy</p>
                    </div>
                    <span onclick="closeModal('termsModalOverlay')" class="modal-close-pro">&times;</span>
                </div>
                
                <div class="terms-content-area">
                    <p>Welcome to <strong>Maa Nirmala DJ & Tent House</strong>. By engaging our services, booking an event, or renting our equipment, you (the "Client") agree to be bound by the following comprehensive Terms and Conditions set forth by our management under the leadership of Mr. Lalu Kumar Tanti. These policies are strictly enforced to ensure the flawless execution of your event and the safety of our staff and equipment.</p>

                    <h4>1. Booking, Payment, & Advances</h4>
                    <p>To secure a date for any service (DJ, Tent, Stage Decoration, or Generator), a non-refundable advance payment of strictly <strong>30% to 50%</strong> of the total quoted package is required at the time of booking. The remaining balance must be settled in full on the day of the event, strictly <em>before</em> the setup is completely dismantled. Failure to clear the final payment will result in legal action. In the event of an event cancellation by the client within 72 hours of the scheduled date, the advance payment will be entirely forfeited.</p>

                    <h4>2. Logistics & Site Accessibility</h4>
                    <p>Maa Nirmala DJ heavily relies on <strong>Laxmikant Tractor Transport</strong> for the delivery of our massive line-array speakers, heavy iron trusses, and DG Sets. The Client is entirely responsible for ensuring that the event venue is fully accessible to heavy tractors and commercial vehicles. If the venue cannot be reached by our transport, additional manual labor charges will be immediately added to the final bill. The setup area must be clean, leveled, and free of debris prior to our arrival.</p>

                    <h4>3. Sound Regulations & Local Laws</h4>
                    <p>While we pride ourselves on providing earth-shattering bass and premium high-volume audio, we strictly operate within the legal frameworks of the Banka district and Bihar State authorities. Maa Nirmala DJ will shut down or lower the sound systems if ordered by local police or government officials. The Client is solely responsible for acquiring any necessary local permits or police permissions required to play loud music late into the night. We will not be held liable for events stopped by law enforcement due to a lack of permits.</p>

                    <h4>4. Equipment Safety & Damage Liability</h4>
                    <p>Our audio-visual equipment, laser lights, and waterproof pandals are highly expensive, state-of-the-art investments. The Client assumes full financial responsibility for any physical damage, theft, or vandalism of our equipment caused by the Client’s guests, family members, or event attendees. In the event of a physical altercation or riot at the venue, our technicians reserve the absolute right to immediately cut the power, pack up the equipment, and leave the premises to ensure the safety of our staff and gear. No refunds will be issued under these circumstances.</p>

                    <h4>5. Unpredictable Weather & Force Majeure</h4>
                    <p>Our premium pandals are designed to be highly water-resistant; however, extreme acts of nature (such as severe cyclonic winds, heavy flooding, or lightning storms) are beyond human control. Maa Nirmala DJ will not be held financially responsible for setup delays or event disruptions caused by extreme weather conditions. For open-air DJ setups, our operators will immediately cover or dismantle electronic equipment (mixers, amplifiers, tops) if rain begins, to prevent electrocution and permanent damage.</p>

                    <h4>6. Power Supply Requirements</h4>
                    <p>If the Client chooses not to rent our heavy-duty Silent Generators (DG Sets), the Client must provide a stable, commercial-grade electrical connection. Maa Nirmala DJ will not connect our sensitive amplifiers to fluctuating, low-voltage domestic power lines. Any damage to our equipment caused by faulty venue wiring provided by the Client will be billed directly to the Client.</p>

                    <h4>7. Setup and Dismantling Timelines</h4>
                    <p>To deliver our signature cinematic quality, our technical rigging and acoustic teams require guaranteed, uninterrupted access to the venue at least 24 to 48 hours prior to the event start time, depending on the scale of the pandal and DJ rig. Once the event concludes, the Client must allow our crew sufficient time (up to 12 hours) to safely dismantle the heavy iron trusses, lighting arrays, and audio equipment. Any delays caused by the venue or the Client will incur waiting charges.</p>
                    
                    <h4>8. Crew Hospitality & Basic Amenities</h4>
                    <p>The construction of massive architectural pandals and the deployment of stadium-grade sound systems require immense physical labor. The Client is kindly requested to provide basic hospitality, including safe drinking water, standard meals, and access to clean washrooms for our ground crew, technicians, and the Laxmikant Tractor Transport drivers during the entirety of the setup, event execution, and dismantling phases.</p>
                    
                    <h4>9. Pyrotechnics & Fire Safety Regulations</h4>
                    <p>If the Client has opted for our cold spark pyro machines, heavy ground fog, or any special atmospheric effects, strictly no open flames, unauthorized fireworks, or flammable materials are permitted within a 20-foot radius of our equipment and the main stage. Maa Nirmala DJ prioritizes absolute safety; our technicians reserve the right to refuse the use of pyrotechnics if the crowd becomes unruly or if the pandal conditions are deemed a fire hazard.</p>
                    
                    <h4>10. Out-of-Station Logistics & Travel</h4>
                    <p>While we are deeply rooted in Beltikri and the Katoria region, we frequently execute premium events across the wider Banka district and beyond. For all out-of-station bookings, additional logistical fees, toll taxes, commercial vehicle entry taxes, and basic overnight accommodation for our core technical operators must be provided or reimbursed by the Client.</p>
                    
                    <h4>11. Overtime & Extended Play Charges</h4>
                    <p>Our standard DJ and event operation packages are booked for specific, pre-agreed timeframes. If the Client wishes to extend the music, lighting, or generator services beyond the contracted end time, strictly enforced hourly overtime charges will apply. These charges must be approved by our management on-site and paid before the extended session begins.</p>
                    
                    <h4>12. Drone Clearances & Venue Restrictions</h4>
                    <p>For packages including cinematic broadcasting and aerial drone videography, it is the sole responsibility of the Client to ensure that the venue management allows drone flights. Maa Nirmala DJ will not be responsible for grounded drones due to sudden venue restrictions, overhead high-tension electrical wires, or local no-fly zone enforcement by authorities.</p>
                    
                    <h4>13. Floral Integrity & Decor Protection</h4>
                    <p>Our elite floral designs, Varmala stages, and imported luxury draperies are crafted with meticulous care. The Client must ensure that guests do not pull, dismantle, or destroy the floral arrangements, premium VIP seating, or carpets during the celebration. Severe damage to our decorative inventory, including burns on carpets or torn imported fabrics, will be evaluated and added to the final damage invoice.</p>
                    
                    <h4>14. Exclusivity Clause</h4>
                    <p>To maintain our undisputed standard of quality, Maa Nirmala DJ & Tent House must be the exclusive provider of audio, lighting, and primary tenting at the contracted venue. We do not permit third-party, local DJs or decorators to plug into our high-end mixers or alter our structural trusses, as this compromises our equipment safety and the overall premium aesthetic we guarantee.</p>
                    
                    <h4>15. Security of Stage & VIP Areas</h4>
                    <p>The DJ booth, LED wall control stations, and generator staging areas are highly restricted zones. The Client is responsible for ensuring that intoxicated guests or unauthorized individuals do not enter these technical zones. Spilling beverages on our digital consoles or tampering with heavy electrical cables will result in an immediate halt of the event until the area is secured.</p>
                    
                    <h4>16. Substitute Equipment Policy</h4>
                    <p>In the highly unlikely event of an unexpected mechanical failure or technical malfunction before an event, Maa Nirmala DJ reserves the right to substitute the specified equipment (such as a specific speaker model or lighting fixture) with an alternative of equal or greater premium quality to ensure the event proceeds flawlessly without interruption.</p>
                    
                    <h4>17. Promotional Media Rights</h4>
                    <p>Maa Nirmala DJ & Tent House reserves the right to capture photographs, audio recordings, and video footage of our stage setups, lighting arrays, and DJ performances during the event. By booking us, the Client grants us permission to use these media assets for our official portfolio, social media platforms, and future marketing campaigns to showcase our cinematic capabilities.</p>
                    
                    <h4>18. On-Site Management Authority</h4>
                    <p>All technical, logistical, and operational decisions made on the ground are at the absolute discretion of our core management team. Our highly dedicated managers, including Mr. Sildhar Kumar and Mr. Om Kumar, alongside our founder, have the final authority regarding equipment placement and safety protocols. Any abusive language or physical threats directed at our staff will result in the immediate and total withdrawal of our services without a refund.</p>
                    
                    <h4>19. Legal Jurisdiction & Dispute Resolution</h4>
                    <p>Maa Nirmala DJ & Tent House operates with the highest standards of business integrity. However, in the rare event of a financial dispute, breach of contract, or severe property damage, all legal matters, claims, and arbitration will be handled exclusively under the jurisdiction of the honorable courts located in the Banka district of Bihar.</p>
                    
                    <h4>20. Binding Acceptance of Terms</h4>
                    <p>By remitting the initial advance payment and confirming the booking date, the Client formally acknowledges that they have read, understood, and agreed to be legally bound by all 20 clauses of this comprehensive Official Policy. This agreement ensures a transparent, secure, and spectacularly successful partnership between you and Maa Nirmala DJ & Tent House.</p>
                </div>

                <div class="terms-footer">
                    <label class="terms-checkbox-wrap">
                        <input type="checkbox" id="termsAgreeCheckbox" onchange="toggleTermsAccept()">
                        <span>I have read, understood, and agree to all terms stated above.</span>
                    </label>
                    <button class="f-btn" id="termsAcceptBtn" style="background: #333; color: #888; pointer-events: none; margin-top: 5px;" onclick="closeModal('termsModalOverlay'); showToast('Terms Accepted!');">
                        ACCEPT & CONTINUE
                    </button>
                </div>

            </div>
        </div>

        <script>
            function toggleTermsAccept() {
                const cb = document.getElementById('termsAgreeCheckbox');
                const btn = document.getElementById('termsAcceptBtn');
                if(cb.checked) {
                    btn.style.background = 'var(--gold-primary)';
                    btn.style.color = '#000';
                    btn.style.pointerEvents = 'auto';
                } else {
                    btn.style.background = '#333';
                    btn.style.color = '#888';
                    btn.style.pointerEvents = 'none';
                }
            }
        </script>

        <style>
            .mn-suggestion-box {
                border: 2px solid transparent !important;
                border-image: linear-gradient(90deg, #D4AF37, #6a11cb) 1 !important;
                box-shadow: 0 20px 50px rgba(0,0,0,0.9), inset 0 0 20px rgba(106, 17, 203, 0.2) !important;
            }
            .s-input:focus { border-color: #6a11cb !important; background: rgba(106, 17, 203, 0.05) !important; box-shadow: 0 0 12px rgba(106, 17, 203, 0.4) !important; }
            .s-submit-btn { background: linear-gradient(90deg, #D4AF37, #6a11cb) !important; color: #fff !important; }
            
            /* NEW FEATURE: Char Counter */
            .char-counter { font-size: 11px; color: #888; text-align: right; margin-top: 5px; font-family: 'Outfit'; }
        </style>

        <div id="suggestionModalOverlay" class="unified-modal-overlay" onclick="closeOnBackgroundClick(event, 'suggestionModalOverlay')">
            <div class="unified-modal-box mn-suggestion-box" id="suggestionBoxContent" style="padding: 25px; max-width: 520px;">
                <span onclick="closeModal('suggestionModalOverlay')" style="position:absolute; top:15px; right:20px; color:#D4AF37; font-size:35px; line-height:1; cursor:pointer; transition:0.3s; z-index:10;">&times;</span>
                
                <h2 style="font-family:'Cinzel',serif; color:#D4AF37; text-align:center; margin-top:0; border-bottom:1px solid rgba(212,175,55,0.3); padding-bottom:15px; font-size: 24px; font-weight:800; letter-spacing:1px;">
                    <i class="fas fa-gem"></i> Business Suggestion
                </h2>
                
                <p style="color:#aaa; text-align:center; font-family:'Outfit', sans-serif; font-size:13px; margin-bottom:20px;">
                    Help Maa Nirmala DJ become the #1 in Bihar. We value your premium feedback!
                </p>
                
                <div style="display:flex; flex-direction:column; margin-top: 15px;">
                    <div style="display:flex; gap:10px;">
                        <input type="text" id="s-name" class="f-input s-input" placeholder="Your Good Name *">
                        <input type="tel" id="s-phone" class="f-input s-input" placeholder="Phone Number *">
                    </div>
                    
                    <select id="s-category" class="f-input s-input" style="color:#ddd; margin-top:12px;">
                        <option value="" disabled selected style="color:#000;">What do you want to improve? *</option>
                        <option value="Audio / DJ Quality" style="color:#000;">Audio / DJ Quality</option>
                        <option value="Tent & Pandal Design" style="color:#000;">Tent & Pandal Design</option>
                        <option value="Pricing & Packages" style="color:#000;">Pricing & Packages</option>
                        <option value="Staff & Service" style="color:#000;">Staff & Service</option>
                        <option value="New Technology Ideas" style="color:#000;">New Technology Ideas</option>
                    </select>
                    
                    <textarea id="s-desc" class="f-input s-input" rows="4" placeholder="Write your brilliant suggestion here... *" style="resize:none; margin-top:12px; margin-bottom: 0;" oninput="updateCharCount(this)"></textarea>
                    <div class="char-counter" id="s-char-count">0 / 500 characters</div>
                    
                    <button id="submitSuggestionBtn" class="f-btn s-submit-btn" onclick="submitSuggestion()" style="margin-top:15px;">
                        <i class="fas fa-paper-plane"></i> SUBMIT SUGGESTION
                    </button>
                </div>
            </div>
        </div>

        <script>
            function updateCharCount(el) {
                const max = 500;
                let len = el.value.length;
                if(len > max) { el.value = el.value.substring(0, max); len = max; }
                document.getElementById('s-char-count').innerText = `${len} / ${max} characters`;
            }
        </script>
        <style>
            .mn-about-box { max-width: 1000px; height: 95vh; }
            .about-content-area { flex-grow: 1; padding: 35px 40px; overflow-y: auto; color: #cccccc; font-family: 'Outfit', sans-serif; font-size: 16px; line-height: 1.9; text-align: justify; scroll-behavior: smooth; }
            .about-content-area::-webkit-scrollbar { width: 8px; }
            .about-content-area::-webkit-scrollbar-track { background: rgba(0,0,0,0.3); border-radius: 10px; }
            .about-content-area::-webkit-scrollbar-thumb { background: var(--gold-primary); border-radius: 10px; border: 1px solid #000; }
            .about-content-area h3 { color: var(--gold-primary); font-family: 'Cinzel', serif; font-size: 24px; margin-top: 35px; margin-bottom: 15px; letter-spacing: 1px; font-weight: 800; text-transform: uppercase; border-left: 4px solid var(--gold-primary); padding-left: 15px; }
            .about-content-area h3:first-child { margin-top: 0; }
            .about-content-area p { margin-bottom: 20px; font-weight: 300; }
            .about-content-area strong { color: #ffffff; font-weight: 600; }
            @media (max-width: 600px) { .about-content-area { padding: 20px 15px; font-size: 15px; } .about-content-area h3 { font-size: 18px; } }
            
            /* NEW FEATURE: Reading Progress Bar & Audio Button */
            .progress-container { width: 100%; height: 3px; background: rgba(255,255,255,0.1); position: absolute; bottom: 0; left: 0; }
            .progress-bar { height: 100%; background: var(--gold-primary); width: 0%; border-radius: 0 5px 5px 0; }
            .read-aloud-btn { background: rgba(212,175,55,0.1); border: 1px solid var(--gold-primary); color: var(--gold-primary); padding: 6px 15px; border-radius: 20px; font-size: 11px; cursor: pointer; transition: 0.3s; font-family: 'Outfit'; font-weight: bold; text-transform: uppercase; display: inline-flex; align-items: center; gap: 6px; margin-top: 10px; }
            .read-aloud-btn:hover { background: var(--gold-primary); color: #000; box-shadow: 0 0 10px rgba(212,175,55,0.4); }
        </style>

        <div id="aboutModalOverlay" class="unified-modal-overlay" onclick="closeOnBackgroundClick(event, 'aboutModalOverlay')">
            <div class="unified-modal-box mn-about-box" id="aboutBoxContent">
                
                <div class="modal-header-pro" style="padding: 25px 20px; text-align: center; flex-direction: column; align-items: center;">
                    <span onclick="closeModal('aboutModalOverlay')" class="modal-close-pro" style="position:absolute; top:20px; right:25px;">&times;</span>
                    <h2 style="margin:0; color:var(--gold-primary); font-family:'Cinzel', serif; font-size:32px; font-weight:900; letter-spacing:2px; text-transform: uppercase; text-shadow: 0 0 15px rgba(212,175,55,0.3);">
                        <i class="fas fa-crown"></i> The Legacy of Maa Nirmala
                    </h2>
                    <p style="margin:8px 0 0 0; color:#e0e0e0; font-size:14px; font-family:'Outfit', sans-serif; letter-spacing: 1px;">Pioneers of Premium Celebrations in Banka, Bihar</p>
                    
                    <button class="read-aloud-btn" onclick="readLegacyAloud()" id="ttsBtn"><i class="fas fa-volume-up"></i> Read to me</button>

                    <div class="progress-container"><div class="progress-bar" id="aboutProgressBar"></div></div>
                </div>
                
                <div class="about-content-area" id="aboutScrollArea" onscroll="updateAboutProgress()">
                    <h3>Chapter I: The Genesis & Vision</h3>
                    <p>Welcome to the grand universe of <strong>Maa Nirmala DJ & Tent House</strong>. Rooted deeply in the historic and culturally vibrant soil of Beltikri, Kaddhar, Katoria, located in the prestigious Banka district of Bihar (Pin: 813106), our establishment has risen from humble beginnings to become the undisputed titan of event management and luxury celebrations. Founded and spearheaded by the visionary <strong>Mr. Lalu Kumar Tanti</strong>, Maa Nirmala DJ was born out of a singular, unyielding passion: to transform ordinary human gatherings into breathtaking, cinematic masterpieces. We recognized early on that a wedding, a district festival, or a grand anniversary is not merely a date on a calendar; it is a profound milestone. Under Mr. Lalu's meticulous direction, alongside a fiercely dedicated management team including <strong>Sildhar Kumar, Anil Kumar, and Sanjay Kumar</strong>, we have engineered a company that operates on the principles of absolute perfection, zero compromises on quality, and an unwavering commitment to our clients' joy.</p>

                    <h3>Chapter II: The Supremacy of Acoustic Engineering</h3>
                    <p>The true heartbeat of any monumental celebration lies in its sound, and at Maa Nirmala DJ, our acoustic engineering is quite simply second to none. We do not just play music; we manipulate soundwaves to captivate the human soul. Our audio arsenal consists of industry-leading, heavy-duty dual subwoofers capable of pushing massive volumes of air, creating an earth-shattering bass response that reverberates through the very ground you stand on. This low-end raw power is perfectly balanced by our deployment of crystal-clear, high-frequency line-array top speakers. Whether we are amplifying the sacred, ancient Sanskrit chants of a traditional wedding ceremony or unleashing high-octane electronic drops for a midnight Baaraat trolley, our state-of-the-art mixers and digital crossovers ensure that every vocal is crisp and every beat is free of distortion. From intimate Haldi ceremonies to our <strong>Mega Concert DJ Rigs</strong> designed for thousands of attendees, we dominate the auditory landscape.</p>

                    <h3>Chapter III: Architectural Grandeur & Royal Pandals</h3>
                    <p>Moving beyond the realm of music, our premium tent house division specializes in the construction of temporary palaces. We understand that the physical environment of an event dictates its prestige. Therefore, we utilize heavy-duty, industrial-grade iron trusses and highly secure rigging systems to construct massive waterproof pandals that defy unpredictable weather. We drape these magnificent structures in miles of imported, vibrantly colored luxury fabrics, cascading elegantly from towering ceilings to create intricate geometric and floral patterns. The interior of every Maa Nirmala setup is a sanctuary of royal comfort, featuring <strong>Premium VIP Seating Arrangements</strong>, immaculate wall-to-wall carpeting, and majestic stage decorations. Our bespoke floral archways and illuminated entrance gates (Dwar) are meticulously crafted to welcome your guests into a world of pure, unadulterated enchantment.</p>

                    <h3>Chapter IV: Cinematic Visuals & Intelligent Lighting</h3>
                    <p>To illuminate our architectural masterpieces and sync with our heavy bass audio, our lighting technicians paint the night sky using highly intelligent, programmable DMX lighting arrays. We deploy sweeping, synchronized 3D laser shows, brilliant LED wash lights, and powerful moving head beams that track the tempo of the music, creating an immersive, multi-sensory environment that rivals professional stadium concerts. By seamlessly introducing cinematic atmospheric effects such as heavy ground fog and safe cold spark pyro machines during key emotional moments—such as the bride and groom's grand entrance or the cutting of the cake—we elevate the visual impact of your evening to legendary status.</p>

                    <h3>Chapter V: Unyielding Logistics & Power Infrastructure</h3>
                    <p>The hallmark of a truly premium service is what happens behind the scenes. An event of massive magnitude requires unbreakable logistical supremacy. Recognizing the unpredictability of local power grids, Maa Nirmala provides absolute electrical reliability through our massive, heavy-duty Silent Generators (DG Sets), ensuring your event never experiences a single millisecond of darkness. Furthermore, our invisible backbone is our formidable logistical network. Supported powerfully by <strong>Laxmikant Tractor Transport</strong>, we possess the sheer mechanical might to deliver colossal payloads of heavy subwoofers, iron pillars, and delicate lighting fixtures to any venue, no matter how remote the location. We arrive with military-like precision, construct with undeniable passion, and manage every technical detail flawlessly.</p>

                    <h3>Chapter VI: Our Promise to You</h3>
                    <p>For years, the communities of Beltikri, Katoria, and the greater Banka region have placed their ultimate trust in us during their most precious moments. When you hire <strong>Maa Nirmala DJ & Tent House</strong>, you are not simply renting equipment; you are partnering with a legacy of excellence. We leave nothing to chance, we accept no excuses, and we let our spectacular, awe-inspiring results speak for themselves. From the first phone call to the final beat of the music, we are devoted entirely to your celebration. Choose the best. Choose Maa Nirmala.</p>
                    
                    <h3>Chapter VII: The Culinary Symphony & Elite Catering</h3>
                    <p>Beyond the auditory and visual spectacles, Maa Nirmala DJ & Tent House recognizes that the soul of any legendary Indian celebration is the grand feast. Our expanded elite catering division is a masterclass in culinary excellence, designed to satisfy the most discerning palates of Bihar and beyond. We do not merely serve food; we curate an extraordinary sensory journey through the rich heritage of authentic traditional flavors and sophisticated international delicacies. Our kitchen is helmed by masterful chefs who utilize organic, locally sourced ingredients to prepare a massive, mouth-watering array of dishes. From the smoky, traditional perfection of Bihar's famous Litti Chokha to sophisticated multi-cuisine buffets featuring rich curries, artisanal breads, and decadent desserts, our menu is boundless. We deploy a sophisticated infrastructure of heavy-duty industrial burners and highly hygienic cold-storage units to ensure every single morsel is served at the absolute peak of freshness. Our service staff, trained rigorously in the highest standards of VIP hospitality, move with invisible grace among your guests, ensuring that every premium plate is replenished and every crystal water glass is full. We provide luxurious bone china crockery, polished stainless steel cutlery, and exquisitely decorated, themed food stalls that align perfectly with your event's royal ambiance. At Maa Nirmala, we believe that the memory of a spectacular, royal banquet lingers in the minds of your guests just as long as the echoing bass of our music.</p>

                    <h3>Chapter VIII: Botanical Architecture & Floral Design</h3>
                    <p>To perfectly complement our towering architectural pandals, Maa Nirmala employs a specialized team of elite floral architects who possess the unique ability to transform raw, empty spaces into blooming, vibrant paradises. We deeply understand that flowers carry the emotional weight of a ceremony, symbolizing purity, new beginnings, and grand celebration. Our expansive sourcing network brings in the absolute freshest Marigolds, exotic Orchids, deep Red Roses, and intensely fragrant Jasmine from the finest botanical gardens across the country, ensuring an explosion of breathtaking color and enchanting scent at your venue. We specialize in creating high-impact, larger-than-life floral installations, including massive twenty-foot "Varmala" stages, cascading floral ceilings, and intricate, welcoming "Rangoli" patterns that greet your esteemed guests at the illuminated Dwar. Our technical crew utilizes hidden, state-of-the-art misting systems to keep the flora dew-fresh and vibrant, even under the intense heat of our powerful stage lights and the warm Bihar climate. Each arrangement is a bespoke, one-of-a-kind creation, carefully tailored to the specific color palette and emotional tone of your wedding or festival. Whether it is a traditional "Genda Phool" theme for a lively Haldi ceremony or a modern, minimalist white lily aesthetic for a high-profile VIP reception, our meticulous floral designs provide the perfect, organic backdrop for your cinematic photographs.</p>

                    <h3>Chapter IX: Digital Integration & Cinematic Broadcasting</h3>
                    <p>In this modern, hyper-connected era, a grand event in the Banka district deserves to be seen, celebrated, and remembered by the entire world. Maa Nirmala DJ & Tent House has boldly pioneered the integration of high-end digital media services directly into our premium event packages. We deploy a sophisticated network of ultra-high-definition (4K) LED wall screens that serve as a dynamic, glowing canvas for the main stage, displaying crystal-clear live feeds of the ceremony, cinematic pre-wedding montages of the couple, or vibrant, pulsating motion graphics that sync flawlessly with our DJ's earth-shaking rhythm. Our technical team works hand-in-hand with professional-grade videographers, utilizing overhead jib cranes and stabilized cinematic drones to capture every emotional tear, every joyous laugh, and every energetic dance move from breathtaking aerial and dynamic ground angles. For families who have loved ones residing abroad or across the country, we offer seamless, high-speed live streaming services to major global platforms, ensuring that physical distance is absolutely no barrier to joining the monumental celebration. By seamlessly merging the deep-rooted cultural traditions of a Beltikri celebration with cutting-edge digital broadcasting technology, Maa Nirmala ensures your event is not just a local gathering, but a globally accessible, high-tech cinematic production.</p>

                    <h3>Chapter X: The Unstoppable Fleet & Heavy Logistics</h3>
                    <p>The unseen, unsung hero of every flawless Maa Nirmala production is our absolute mastery of heavy logistics and large-scale transportation. Delivering a royal palace of heavy iron trusses, miles of luxury fabric, and thousands of watts of audio equipment requires an unbreakable mechanical backbone. This is where our formidable logistical partner, <strong>Laxmikant Tractor Transport</strong>, comes into play. Powered by an unstoppable fleet of heavy-duty farming tractors and heavy-payload trailers, we possess the sheer mechanical might and rugged endurance to deliver colossal payloads of dual subwoofers, massive iron pillars, and delicate, intelligent lighting fixtures to any venue, no matter how remote, unpaved, or challenging the location might be. Our drivers and logistical crew navigate the terrains of Katoria, Banka, and beyond with military-like precision and absolute punctuality. We do not let muddy roads or difficult access points dictate the quality of your event. The Laxmikant Tractor Transport fleet ensures that our massive infrastructure arrives safely, allowing our rigging teams to begin construction on time, every time. This unyielding logistical supremacy guarantees that from the moment you book us, the physical realization of your grandest dreams is in the most capable, powerful hands in the industry.</p>

                    <h3>Chapter XI: Mega Concerts & District Festivals</h3>
                    <p>While our reputation was forged in the fires of luxury weddings and grand anniversaries, the sheer scale of Maa Nirmala's infrastructure naturally evolved to dominate the arena of mega-events. We are the premier, go-to technical powerhouse for massive district-level festivals, high-profile political rallies, large-scale corporate summits, and deeply spiritual Maha-Aartis across Bihar. When the audience size swells from hundreds into the thousands, our engineering approach shifts from intimate luxury to stadium-grade power. We deploy expanded line-array configurations capable of throwing crystal-clear audio across massive open maidans, ensuring that the person in the very last row experiences the exact same vocal clarity and thumping bass as the VIPs in the front. Our tenting division scales up proportionately, constructing colossal, weatherproof domes supported by reinforced steel, capable of safely sheltering thousands of attendees. We coordinate complex, multi-stage lighting transitions and manage massive power grids using synchronized arrays of our heavy-duty Silent Generators. Handling an event of this magnitude requires nerves of steel and flawless execution, and our veteran crew has proven time and time again that Maa Nirmala is not just an event manager, but a towering pillar of large-scale public entertainment and crowd management.</p>

                    <h3>Chapter XII: The Philosophy of Customer Devotion</h3>
                    <p>At the very core of our massive inventory of subwoofers, lasers, and iron trusses lies a simple, unbreakable philosophy: absolute devotion to our clients. <strong>Mr. Lalu Kumar Tanti</strong> built Maa Nirmala DJ & Tent House not just as a business, but as an institution of trust. We understand that our clients come to us during the most important, high-stakes moments of their lives—moments that cannot be repeated or rescheduled. Therefore, under the vigilant and tireless coordination of our top-tier management team, including <strong>Sildhar Kumar, Anil Kumar, and Sanjay Kumar</strong>, we operate on a strict "Zero Excuses" policy. From the initial, detailed consultation to the final dismantling of the stage, our clients experience a level of personalized, round-the-clock service that is unparalleled in the industry. We listen intently to your unique vision, we anticipate potential challenges before they arise, and we execute with a passionate intensity as if it were a celebration within our own family. Our team remains on-site, vigilant, and ready to adapt instantly to any last-minute changes or requests. This unwavering dedication to customer satisfaction is the true secret behind our legacy, transforming first-time clients into lifelong patrons.</p>

                    <h3>Chapter XIII: Sustainable Celebrations & Community Impact</h3>
                    <p>True greatness is not merely measured by the volume of our speakers or the height of our pandals, but by the positive impact we leave on our beloved community. Rooted deeply in Beltikri (Pin: 813106), Maa Nirmala DJ & Tent House takes immense pride in being an engine of local economic growth and community empowerment. We actively employ dozens of hardworking individuals from the Kaddhar and Katoria regions, providing them with rigorous technical training in acoustic engineering, rigging, and hospitality. By partnering with local artisans for our fabrics and sourcing our catering ingredients from local farmers, we ensure that the wealth generated by your celebrations directly enriches the Banka district. Furthermore, as an industry leader, we are deeply conscious of our environmental footprint. We have heavily invested in the latest generation of ultra-efficient, low-emission Silent DG Sets that drastically reduce noise pollution and exhaust, ensuring that our massive power needs do not harm the natural beauty of our surroundings. We utilize eco-friendly, reusable staging materials wherever possible, ensuring that our breathtaking celebrations remain deeply respectful of the environment and the vibrant community that supports us.</p>

                    <h3>Chapter XIV: Future Innovations & The Next Decade</h3>
                    <p>A true titan never rests on its past achievements. As Maa Nirmala DJ & Tent House looks forward to the next decade of dominance, our eyes are fixed firmly on the horizon of technological innovation. <strong>Mr. Lalu Kumar Tanti's</strong> vision for the future involves a massive, aggressive expansion of our technological arsenal. We are actively exploring the integration of AI-driven acoustic mapping to perfectly calibrate our sound systems for any venue's unique architecture automatically. We are investing heavily in the next generation of holographic projection mapping, allowing us to turn the walls of our pandals into living, moving cinematic screens that transport your guests to entirely different worlds. Furthermore, our logistical footprint is expanding, preparing to bring the unmatched "Maa Nirmala Experience" to even wider territories across Bihar and neighboring states. We are constantly upgrading our inventory, ensuring that we possess the most advanced, heart-pounding audio gear and the most luxurious, cutting-edge tent fabrics available on the global market. The future of event management is incredibly bright, and Maa Nirmala will continue to be the blazing vanguard leading the charge.</p>

                    <h3>Chapter XV: The Final Overture & Call to Action</h3>
                    <p>The epic narrative of your life deserves a stage just as magnificent. For years, the people of Beltikri, Katoria, Banka, and beyond have entrusted their most sacred, joyous, and monumental occasions to us. We have proven, event after event, that when you desire absolute perfection, earth-shattering sound, and royal grandeur, there is only one name that commands the industry: <strong>Maa Nirmala DJ & Tent House</strong>. We invite you to step into our world and experience the pinnacle of luxury celebration. Let our visionary founder, <strong>Mr. Lalu Kumar Tanti</strong>, and our dedicated team transform your wildest dreams into a breathtaking reality that will be talked about for generations. Do not settle for the ordinary when the extraordinary is at your fingertips. The stage is set, the lasers are aligned, and the subwoofers are primed. To begin planning your legendary event, reach out to our VIP booking team today. You can contact us directly at <strong>9771617808, 7294969938, or 8544341240</strong>. Choose the absolute best. Choose Maa Nirmala—where your grandest celebration becomes eternal history.</p>
                </div>
            </div>
        </div>

        <script>
            function updateAboutProgress() {
                const area = document.getElementById('aboutScrollArea');
                const bar = document.getElementById('aboutProgressBar');
                const scrollPercentage = (area.scrollTop / (area.scrollHeight - area.clientHeight)) * 100;
                bar.style.width = scrollPercentage + '%';
            }

            let isReadingLegacy = false;
            function readLegacyAloud() {
                const btn = document.getElementById('ttsBtn');
                if(!isReadingLegacy) {
                    let text = document.getElementById('aboutScrollArea').innerText;
                    let utterance = new SpeechSynthesisUtterance(text);
                    utterance.lang = 'en-IN';
                    window.speechSynthesis.speak(utterance);
                    isReadingLegacy = true;
                    btn.innerHTML = '<i class="fas fa-stop"></i> Stop Reading';
                    btn.style.background = '#E63946';
                    btn.style.color = '#fff';
                    btn.style.borderColor = '#E63946';
                } else {
                    window.speechSynthesis.cancel();
                    isReadingLegacy = false;
                    btn.innerHTML = '<i class="fas fa-volume-up"></i> Read to me';
                    btn.style.background = 'rgba(212,175,55,0.1)';
                    btn.style.color = 'var(--gold-primary)';
                    btn.style.borderColor = 'var(--gold-primary)';
                }
            }
        </script>

        <style>
            .mn-social-box { max-width: 1200px; height: 95vh; }
            .social-tabs { display: flex; justify-content: center; gap: 15px; margin-top: 15px; }
            .s-tab-btn { background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.2); color: #fff; padding: 10px 25px; border-radius: 30px; cursor: pointer; font-family: 'Outfit', sans-serif; font-size: 15px; font-weight: 600; transition: all 0.3s ease; display: flex; align-items: center; gap: 8px; }
            .s-tab-btn.active-ig { background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%); border-color: transparent; box-shadow: 0 5px 15px rgba(220, 39, 67, 0.4); }
            .s-tab-btn.active-fb { background: #1877F2; border-color: transparent; box-shadow: 0 5px 15px rgba(24, 119, 242, 0.4); }
            .social-content-area { flex-grow: 1; padding: 20px; overflow-y: auto; display: flex; justify-content: center; }
            .social-content-area::-webkit-scrollbar { width: 6px; }
            .social-content-area::-webkit-scrollbar-thumb { background: var(--gold-primary); border-radius: 10px; }
            .social-feed-container { display: none; width: 100%; height: 100%; animation: fadeInOverlay 0.5s ease; }
            .social-feed-container.active { display: flex; flex-direction: column; align-items: center; }
            .ig-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 20px; width: 100%; max-width: 1100px; margin-top: 20px; }
            
            /* NEW FEATURE: Refresh Feed UI */
            .sync-btn { position: absolute; top: 20px; left: 25px; color: #aaa; background: none; border: none; font-size: 14px; cursor: pointer; display: flex; align-items: center; gap: 5px; font-family: 'Outfit'; transition: 0.3s; }
            .sync-btn:hover { color: var(--gold-primary); }
            .sync-btn i.spinning { animation: fa-spin 1s infinite linear; color: var(--gold-primary); }
        </style>

        <div id="socialModalOverlay" class="unified-modal-overlay" onclick="closeOnBackgroundClick(event, 'socialModalOverlay')">
            <div class="unified-modal-box mn-social-box">
                
                <div class="modal-header-pro" style="flex-direction: column; text-align: center; border-bottom: 1px solid rgba(212,175,55,0.3);">
                    
                    <button class="sync-btn" id="socialSyncBtn" onclick="syncSocialFeeds()"><i class="fas fa-sync-alt" id="syncIcon"></i> Sync Feed</button>

                    <span onclick="closeModal('socialModalOverlay')" class="modal-close-pro" style="position:absolute; top:15px; right:25px;">&times;</span>
                    
                    <h2 style="margin:0; color:#fff; font-family:'Cinzel', serif; font-size:24px; font-weight:800; letter-spacing:1px;">
                        <i class="fas fa-globe"></i> Live Social Feeds
                    </h2>
                    
                    <div class="social-tabs">
                        <button class="s-tab-btn active-ig" id="btn-ig" onclick="switchSocialTab('ig')">
                            <i class="fab fa-instagram"></i> Instagram
                        </button>
                        <button class="s-tab-btn" id="btn-fb" onclick="switchSocialTab('fb')">
                            <i class="fab fa-facebook-f"></i> Facebook
                        </button>
                    </div>
                </div>
                
                <div class="social-content-area">
                    
                    <div id="feed-ig" class="social-feed-container active">
                        <div style="text-align: center; margin-bottom: 20px;">
                            <img src="https://i.postimg.cc/qMWWzWbF/Screenshot-2026-01-14-15-29-44-90-965bbf4d18d205f782c6b8409c5773a4.jpg" style="width:80px; height:80px; border-radius:50%; border:3px solid #cc2366; object-fit:cover;">
                            <h3 style="color:#fff; font-family:'Outfit', sans-serif; margin: 10px 0 5px 0;">@maa_nirmala_dj</h3>
                            <a href="https://www.instagram.com/maa_nirmala_dj" target="_blank" style="color:var(--gold-primary); text-decoration:none; font-family:'Outfit', sans-serif; font-size:14px; border: 1px solid var(--gold-primary); padding: 5px 15px; border-radius: 20px; display:inline-block; margin-top:5px; transition: 0.3s;" onmouseover="this.style.background='var(--gold-primary)'; this.style.color='#000';" onmouseout="this.style.background='transparent'; this.style.color='var(--gold-primary)';">Follow Us on Instagram</a>
                        </div>
                        
                        <div class="ig-grid" id="ig-grid-container">
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DT-a_KEk7Dg/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DT1WY8SCOgw/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DU97ieVE7nR/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DU85vD-E25K/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DU846FikxCk/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DU837C8kxNF/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DUDeT9siJfO/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DT5paKBE03U/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DT5X-Z-k-ai/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DT4HlNrE9xN/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DT1lb02iGy0/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DT1fBhtCA4X/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DTz9nEPkyKO/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTz79cyE7Hh/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTzJWMNExQh/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTy-LYlCNSm/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTwaxZ2kel6/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTu4AZdE2sr/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                            <blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTv-Kt5kyN8/" data-instgrm-version="14" style="background:#000; border:0; margin:0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote>
                        </div>
                    </div>

                    <div id="feed-fb" class="social-feed-container">
                        <div style="background:#fff; padding:10px; border-radius:12px; width:100%; max-width:500px; height:100%;">
                            <iframe src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FMaaNirmalaDJ7&tabs=timeline&width=500&height=800&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId" width="100%" height="100%" style="border:none;overflow:hidden; min-height:600px;" scrolling="yes" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"></iframe>
                        </div>
                    </div>

                </div>
            </div>
        </div>

        <script async src="//www.instagram.com/embed.js"></script>

        <script>
            function switchSocialTab(platform) {
                if(typeof playTap === 'function') playTap();
                
                const btnIg = document.getElementById('btn-ig');
                const btnFb = document.getElementById('btn-fb');
                const feedIg = document.getElementById('feed-ig');
                const feedFb = document.getElementById('feed-fb');
                
                btnIg.className = 's-tab-btn';
                btnFb.className = 's-tab-btn';
                feedIg.classList.remove('active');
                feedFb.classList.remove('active');
                
                if(platform === 'ig') {
                    btnIg.className = 's-tab-btn active-ig';
                    feedIg.classList.add('active');
                } else if(platform === 'fb') {
                    btnFb.className = 's-tab-btn active-fb';
                    feedFb.classList.add('active');
                }
            }

            function syncSocialFeeds() {
                const icon = document.getElementById('syncIcon');
                const btn = document.getElementById('socialSyncBtn');
                icon.classList.add('spinning');
                btn.innerHTML = `<i class="fas fa-sync-alt spinning" id="syncIcon"></i> Syncing...`;
                
                // Process Instagram Embeds again
                if(window.instgrm) { window.instgrm.Embeds.process(); }
                
                setTimeout(() => {
                    icon.classList.remove('spinning');
                    btn.innerHTML = `<i class="fas fa-check" style="color:#00ff00;"></i> Synced`;
                    setTimeout(() => {
                        btn.innerHTML = `<i class="fas fa-sync-alt" id="syncIcon"></i> Sync Feed`;
                    }, 2000);
                }, 1500);
            }
        </script>
        <style>
            /* Hero Core Styles */
            #homeSection { padding: 0; margin: 0; overflow-x: hidden; background-color: var(--bg-body); }
            .full-bleed-hero-edge { position: relative; width: 100vw; margin-left: calc(-50vw + 50%); height: 48vh; min-height: 450px; border-radius: 0 0 35px 35px; border-bottom: 1px solid rgba(212, 175, 55, 0.3); box-shadow: 0 10px 40px rgba(0, 0, 0, 0.9); overflow: hidden; background-color: #000; }
            .hero-img-full { width: 100%; height: 100%; object-fit: cover; object-position: center 20%; display: block; }
            
            /* Lighting & Gradients */
            .dj-color-shine { position: absolute; top: 0; left: 0; width: 100%; height: 100%; background: linear-gradient(45deg, #4a0000, #2a004d, #00004d, #00331a, #4d3300, #4d0033, #4d1a00, #003333, #1a0033, #4a0000 ); background-size: 400% 400%; animation: djShineAnim 15s ease-in-out infinite; mix-blend-mode: screen; opacity: 0.65; z-index: 1; }
            @keyframes djShineAnim { 0% { background-position: 0% 50%; } 50% { background-position: 100% 50%; } 100% { background-position: 0% 50%; } }
            .hero-dark-edge-fade { position: absolute; bottom: 0; left: 0; width: 100%; height: 75%; background: linear-gradient(to bottom, rgba(5,5,5,0) 0%, rgba(5,5,5,0.85) 50%, #050505 100%); z-index: 2; }
            
            /* Text & Typography */
            .hero-text-edge-content { position: absolute; bottom: 0; left: 0; width: 100%; padding: 0 20px 25px 20px; text-align: center; z-index: 3; }
            @keyframes textDeepShine { 0% { background-position: 0% 50%; } 100% { background-position: 200% 50%; } }
            .hero-massive-title { font-family: 'Cinzel', serif; font-size: 44px; font-weight: 900; text-transform: uppercase; margin: 0 0 2px 0; letter-spacing: 1px; line-height: 1.05; filter: drop-shadow(0px 8px 15px rgba(0,0,0,1)); background: linear-gradient(to right, #FFD700, #FF1493, #8A2BE2, #00BFFF, #00FA9A, #FFD700); background-size: 200% auto; -webkit-background-clip: text; -webkit-text-fill-color: transparent; animation: textDeepShine 3s linear infinite; }
            .hero-massive-subtitle { display: block; font-family: 'Cinzel', serif; font-size: 22px; font-weight: 700; letter-spacing: 5px; margin-bottom: 15px; filter: drop-shadow(0px 4px 12px rgba(0,0,0,1)); background: linear-gradient(to right, #FFD700, #FF1493, #8A2BE2, #00BFFF, #00FA9A, #FFD700); background-size: 200% auto; -webkit-background-clip: text; -webkit-text-fill-color: transparent; animation: textDeepShine 3s linear infinite; }
            .hero-premium-address { font-family: 'Outfit', sans-serif; font-size: 13px; font-weight: 500; color: #E0E0E0; margin: 0; letter-spacing: 2px; text-transform: uppercase; line-height: 1.8; text-shadow: 0px 2px 10px rgba(0,0,0,1); }
            .hero-premium-address span { color: var(--gold-primary); margin: 0 6px; font-weight: 800; }

            /* NEW FEATURE: Booking Badge & Laser Sweep */
            .live-booking-badge { position: absolute; top: 80px; left: 50%; transform: translateX(-50%); background: rgba(0,0,0,0.6); backdrop-filter: blur(10px); border: 1px solid var(--gold-primary); color: #fff; padding: 6px 15px; border-radius: 30px; font-size: 11px; font-family: 'Outfit'; font-weight: bold; z-index: 10; letter-spacing: 1px; display: flex; align-items: center; gap: 8px; box-shadow: 0 0 15px rgba(212,175,55,0.3); }
            .live-booking-badge .dot { width: 8px; height: 8px; background: #00ff00; border-radius: 50%; box-shadow: 0 0 8px #00ff00; animation: blinkDot 1s infinite; }
            @keyframes blinkDot { 0%, 100% { opacity: 1; } 50% { opacity: 0.4; } }

            .hero-laser-sweep { position: absolute; top: 0; left: -100%; width: 100%; height: 2px; background: linear-gradient(90deg, transparent, #00e5ff, transparent); box-shadow: 0 0 20px #00e5ff, 0 0 40px #00e5ff; z-index: 4; animation: sweepLaser 6s infinite linear; transform-origin: left; transform: rotate(15deg); }
            @keyframes sweepLaser { 0% { left: -100%; top: 0; } 50% { left: 100%; top: 100%; } 100% { left: 100%; top: 100%; } }
            
            /* Install App Button Upgrades */
            .install-btn-wrapper { width: 100%; display: flex; justify-content: center; padding: 20px 0; }
            .glass-install-btn { display: none; background: rgba(212, 175, 55, 0.1); border: 1px solid var(--gold-primary); color: var(--gold-primary); padding: 12px 35px; border-radius: 30px; font-size: 13px; font-weight: 800; cursor: pointer; box-shadow: 0 0 20px rgba(212, 175, 55, 0.15); font-family: 'Outfit'; letter-spacing: 1.5px; text-transform: uppercase; position: relative; overflow: hidden; animation: bounce 2.5s infinite ease-in-out; }
            .glass-install-btn::before { content: ''; position: absolute; top: 0; left: -100%; width: 50%; height: 100%; background: linear-gradient(to right, transparent, rgba(255,255,255,0.4), transparent); transform: skewX(-25deg); animation: buttonGloss 3s infinite; }
            @keyframes buttonGloss { 0% { left: -100%; } 20% { left: 200%; } 100% { left: 200%; } }
        </style>

        <div class="container" id="homeSection">
            <div class="full-bleed-hero-edge">
                <div class="live-booking-badge"><div class="dot"></div> BOOKING OPEN FOR 2026</div>
                
                <div class="hero-laser-sweep"></div>

                <img src="https://i.postimg.cc/g20XqtDW/IMG_20260303_121446.png" class="hero-img-full" alt="Maa Nirmala DJ">
                
                <div class="dj-color-shine"></div>
                <div class="hero-dark-edge-fade"></div>

                <div class="hero-text-edge-content">
                    <h1 class="hero-massive-title">MAA NIRMALA DJ</h1>
                    <span class="hero-massive-subtitle">& TENT HOUSE</span>
                    <p class="hero-premium-address">
                        Tola Beltikri <span>|</span> Kaddhar <span>|</span> Katoria <br> Banka <span>|</span> Bihar
                    </p>
                </div>
            </div>

            <div class="install-btn-wrapper">
                <button id="installBtn" class="glass-install-btn" onclick="installApp()"><i class="fas fa-download"></i> INSTALL MNDs APP</button>
            </div>
        </div>

        <style>
            /* Glowing Master Button */
            .premium-social-trigger { display: flex; align-items: center; justify-content: center; gap: 12px; width: 85%; max-width: 400px; margin: 10px auto 40px auto; padding: 18px 25px; border-radius: 40px; background: linear-gradient(135deg, #111, #222); border: 2px solid var(--gold-primary); color: #fff; font-family: 'Cinzel', serif; font-size: 18px; font-weight: 800; letter-spacing: 2px; cursor: pointer; position: relative; overflow: hidden; box-shadow: 0 0 25px rgba(212, 175, 55, 0.4); transition: transform 0.3s ease; animation: subtlePulse 3s infinite alternate; }
            .premium-social-trigger::before { content: ''; position: absolute; top: 0; left: -100%; width: 50%; height: 100%; background: linear-gradient(to right, transparent, rgba(212, 175, 55, 0.6), transparent); transform: skewX(-25deg); animation: buttonShine 4s infinite; }
            .premium-social-trigger:active { transform: scale(0.96); }
            @keyframes subtlePulse { 0% { box-shadow: 0 0 15px rgba(212, 175, 55, 0.3); } 100% { box-shadow: 0 0 35px rgba(212, 175, 55, 0.8); } }
            @keyframes buttonShine { 0% { left: -100%; } 20% { left: 200%; } 100% { left: 200%; } }

            .social-logo-scroller { display: flex; gap: 15px; width: 80px; overflow: hidden; mask-image: linear-gradient(to right, transparent, black 20%, black 80%, transparent); -webkit-mask-image: linear-gradient(to right, transparent, black 20%, black 80%, transparent); }
            .social-logo-track { display: flex; gap: 15px; animation: scrollLogos 6s linear infinite; }
            .social-logo-track i { font-size: 22px; color: var(--gold-primary); }
            @keyframes scrollLogos { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-50% - 7.5px)); } }

            /* Selection Box */
            .selection-box { display: flex; flex-direction: column; gap: 20px; width: 100%; text-align: center; }
            .selection-title { color: #fff; font-family: 'Cinzel', serif; font-size: 32px; font-weight: 800; margin-bottom: 20px; text-shadow: 0 0 15px rgba(212, 175, 55, 0.8); }
            .option-btn { background: rgba(20, 20, 20, 0.8); border: 1px solid var(--gold-primary); padding: 25px; border-radius: 20px; color: #fff; font-family: 'Outfit', sans-serif; font-size: 18px; font-weight: 600; display: flex; align-items: center; justify-content: center; gap: 15px; cursor: pointer; box-shadow: 0 5px 20px rgba(0,0,0,0.5); transition: 0.3s; }
            .option-btn i { font-size: 28px; color: var(--gold-primary); }
            .option-btn:hover { background: rgba(212,175,55,0.1); transform: translateY(-3px); }

            /* Gallery Areas */
            .hub-gallery-container { width: 100%; height: 100%; overflow-y: auto; padding: 20px; display: flex; flex-direction: column; gap: 25px; align-items: center; scrollbar-width: none; }
            .hub-gallery-container::-webkit-scrollbar { display: none; }
            .gallery-title { color: var(--gold-primary); font-family: 'Cinzel', serif; font-size: 22px; margin: 0 0 10px 0; text-align: center; position: sticky; top: 0; background: rgba(5,5,5,0.95); padding: 15px; width: 100%; z-index: 10; border-bottom: 1px solid rgba(212, 175, 55, 0.3); border-radius: 12px 12px 0 0;}

            /* Audio Card & Visualizer */
            .audio-card { background: #111; border: 1px solid rgba(212, 175, 55, 0.4); border-radius: 15px; padding: 20px; width: 100%; box-shadow: 0 5px 15px rgba(0,0,0,0.8); text-align: left; position: relative; overflow: hidden;}
            .audio-card h4 { color: #fff; font-family: 'Outfit', sans-serif; margin: 0 0 15px 0; font-size: 16px; display: flex; justify-content: space-between;}
            .audio-card audio { width: 100%; outline: none; border-radius: 30px; }
            
            .visualizer { display: flex; gap: 4px; align-items: flex-end; height: 20px; }
            .bar { width: 4px; background: var(--gold-primary); border-radius: 2px; animation: bounceBar 1s infinite ease-in-out alternate; opacity: 0.3;}
            .audio-card:focus-within .bar { opacity: 1; }
            .bar:nth-child(1) { animation-delay: 0.1s; } .bar:nth-child(2) { animation-delay: 0.4s; } .bar:nth-child(3) { animation-delay: 0.2s; } .bar:nth-child(4) { animation-delay: 0.5s; } .bar:nth-child(5) { animation-delay: 0.3s; }
            @keyframes bounceBar { 0% { height: 4px; } 100% { height: 20px; } }

            /* Video Card */
            .video-card { width: 100%; min-height: 450px; background: #050505; border-radius: 10px; overflow: hidden; border: 1px solid rgba(212, 175, 55, 0.3); display: flex; justify-content: center; align-items: center; }
        </style>

        <button class="premium-social-trigger" onclick="openModal('selectionModal')">
            MEDIA HUB
            <div class="social-logo-scroller">
                <div class="social-logo-track">
                    <i class="fab fa-instagram"></i>
                    <i class="fas fa-music"></i>
                    <i class="fas fa-video"></i>
                    <i class="fas fa-headphones"></i>
                    <i class="fab fa-instagram"></i>
                    <i class="fas fa-music"></i>
                    <i class="fas fa-video"></i>
                    <i class="fas fa-headphones"></i>
                </div>
            </div>
        </button>

        <div class="unified-modal-overlay" id="selectionModal" onclick="closeOnBackgroundClick(event, 'selectionModal')">
            <div class="unified-modal-box" style="padding: 30px 20px; max-width: 400px; background: transparent; border: none; box-shadow: none;">
                <i class="fas fa-times modal-close-pro" style="position:absolute; top: -30px; right: 0;" onclick="closeModal('selectionModal')"></i>
                <div class="selection-box">
                    <h2 class="selection-title">MND MEDIA HUB</h2>
                    <div class="option-btn" onclick="switchHubModal('selectionModal', 'audioHubModal')">
                        <i class="fas fa-music"></i> LISTEN TO AUDIO
                    </div>
                    <div class="option-btn" onclick="switchHubModal('selectionModal', 'videoHubModal')">
                        <i class="fab fa-instagram"></i> WATCH REELS
                    </div>
                </div>
            </div>
        </div>

        <div class="unified-modal-overlay" id="audioHubModal" onclick="closeOnBackgroundClick(event, 'audioHubModal')">
            <div class="unified-modal-box" style="height: 85vh; max-width: 500px; padding: 0;">
                <i class="fas fa-times modal-close-pro" style="position:absolute; top: 15px; right: 20px; z-index: 20;" onclick="closeModal('audioHubModal')"></i>
                
                <div class="hub-gallery-container">
                    <h2 class="gallery-title"><i class="fas fa-compact-disc"></i> EXCLUSIVE MIXES</h2>
                    
                    <div class="audio-card">
                        <h4>
                            <span><i class="fas fa-play-circle" style="color:var(--gold-primary);"></i> Premium DJ Mix 1</span>
                            <div class="visualizer"><div class="bar"></div><div class="bar"></div><div class="bar"></div><div class="bar"></div><div class="bar"></div></div>
                        </h4>
                        <audio controls preload="none"><source src="https://files.catbox.moe/m832cb.mp3" type="audio/mpeg"></audio>
                    </div>

                    <div class="audio-card">
                        <h4>
                            <span><i class="fas fa-play-circle" style="color:var(--gold-primary);"></i> Heavy Bass Drop</span>
                            <div class="visualizer"><div class="bar"></div><div class="bar"></div><div class="bar"></div><div class="bar"></div><div class="bar"></div></div>
                        </h4>
                        <audio controls preload="none"><source src="https://files.catbox.moe/efdl27.mp3" type="audio/mpeg"></audio>
                    </div>

                    <div class="audio-card">
                        <h4>
                            <span><i class="fas fa-play-circle" style="color:var(--gold-primary);"></i> Grand Wedding Entrance</span>
                            <div class="visualizer"><div class="bar"></div><div class="bar"></div><div class="bar"></div><div class="bar"></div><div class="bar"></div></div>
                        </h4>
                        <audio controls preload="none"><source src="https://files.catbox.moe/mus2yv.mp3" type="audio/mpeg"></audio>
                    </div>
                    
                    <button class="option-btn" style="width:100%; margin-top:10px; padding:15px;" onclick="switchHubModal('audioHubModal', 'selectionModal')">
                        <i class="fas fa-arrow-left"></i> BACK TO HUB
                    </button>
                </div>
            </div>
        </div>

        <div class="unified-modal-overlay" id="videoHubModal" onclick="closeOnBackgroundClick(event, 'videoHubModal')">
            <div class="unified-modal-box" style="height: 85vh; max-width: 500px; padding: 0;">
                <i class="fas fa-times modal-close-pro" style="position:absolute; top: 15px; right: 20px; z-index: 20;" onclick="closeModal('videoHubModal')"></i>
                
                <div class="hub-gallery-container"> 
                    <h2 class="gallery-title"><i class="fab fa-instagram"></i> INSTAGRAM REELS</h2>
                    
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DT-a_KEk7Dg/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DT1WY8SCOgw/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DU97ieVE7nR/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DU85vD-E25K/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DU846FikxCk/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DU837C8kxNF/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DUDeT9siJfO/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DT5paKBE03U/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DT5X-Z-k-ai/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DT4HlNrE9xN/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DT1lb02iGy0/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DT1fBhtCA4X/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/p/DTz9nEPkyKO/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTz79cyE7Hh/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTzJWMNExQh/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTy-LYlCNSm/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTwaxZ2kel6/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTu4AZdE2sr/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>
                    <div class="video-card"><blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DTv-Kt5kyN8/" data-instgrm-version="14" style="background:#000; border:0; margin: 0; width:100%;"><div style="padding:16px; text-align:center; color:#fff;">Loading Reel...</div></blockquote></div>

                    <button class="option-btn" style="width:90%; margin:20px auto; padding:15px;" onclick="switchHubModal('videoHubModal', 'selectionModal')">
                        <i class="fas fa-arrow-left"></i> BACK TO HUB
                    </button>
                </div>
            </div>
        </div>

        <script>
            function switchHubModal(hideId, showId) {
                if(typeof playTap === 'function') playTap();
                document.getElementById(hideId).classList.remove('active');
                document.getElementById(showId).classList.add('active');
                
                // Process Instagram Embeds securely
                if(showId === 'videoHubModal') {
                    setTimeout(() => { if(window.instgrm) { window.instgrm.Embeds.process(); } }, 300);
                }
                
                // Stop audio if leaving audio modal
                if(hideId === 'audioHubModal') {
                    document.querySelectorAll('audio').forEach(audio => { audio.pause(); audio.currentTime = 0; });
                }
            }
        </script>
        
        <div class="container" style="padding-top: 10px;">
            <div class="section-label"><i class="fas fa-images"></i> OUR SETUP & SHOWCASE</div>
            <div class="grid">
                <a href="javascript:void(0)" class="img-card" onclick="navAction('booking')">
                    <img src="https://i.postimg.cc/5yRdctZh/1771529133710.jpg" alt="DJ Setup" loading="lazy">
                    <span>Elite DJ Setup</span>
                </a>
                <a href="javascript:void(0)" class="img-card" onclick="navAction('booking')">
                    <img src="https://i.postimg.cc/R0smYWFp/2025-10-07-(5).jpg" alt="Tent House" loading="lazy">
                    <span>Premium Tents</span>
                </a>
                <a href="javascript:void(0)" class="img-card" onclick="navAction('booking')">
                    <img src="https://i.postimg.cc/hPgQLpyz/image_b73be3f2_1.png" alt="Premium Quality" loading="lazy">
                    <span>Premium Lightings</span>
                </a>
                <a href="javascript:void(0)" class="img-card" onclick="navAction('booking')">
                    <img src="https://i.postimg.cc/Vv7kBKCH/2025-10-07-(1).jpg" alt="Booking" loading="lazy">
                    <span>Premium Quality</span>
                </a>
            </div>
        </div>
        <style>
            #gallery { text-align: center; margin: 50px 0 20px 0; font-family: 'Cinzel', serif; scroll-margin-top: 80px; }
            .gallery-title { font-size: 26px; font-weight: 900; color: var(--text-main); letter-spacing: 2px; margin: 0 0 5px 0; text-shadow: 0 2px 10px rgba(0,0,0,0.8); text-transform: uppercase; }
            .gallery-title i { color: var(--gold-primary); margin-right: 8px; animation: pulse 2s infinite; }
            .gallery-subtitle { font-family: 'Outfit', sans-serif; color: var(--gold-primary); font-size: 13px; font-weight: 600; letter-spacing: 4px; text-transform: uppercase; margin: 0; }

            .smart-slider-container { position: relative; width: 100vw; margin-left: calc(-50vw + 50%); background: linear-gradient(to bottom, #050505, #111, #050505); padding: 30px 0; border-top: 1px solid var(--border-color); border-bottom: 1px solid var(--border-color); box-shadow: inset 0 0 30px rgba(0,0,0,0.9); }
            .smart-slider-container::before, .smart-slider-container::after { content: ""; position: absolute; top: 0; width: 80px; height: 100%; z-index: 5; pointer-events: none; }
            .smart-slider-container::before { left: 0; background: linear-gradient(to right, #050505 10%, transparent 100%); }
            .smart-slider-container::after { right: 0; background: linear-gradient(to left, #050505 10%, transparent 100%); }

            .smart-track { display: flex; gap: 20px; padding: 0 20px; overflow-x: auto; scroll-behavior: auto; scrollbar-width: none; -ms-overflow-style: none; -webkit-overflow-scrolling: touch; align-items: center; }
            .smart-track::-webkit-scrollbar { display: none; }
            
            /* NEW FEATURE: Cinematic Focus */
            .smart-img { flex: 0 0 auto; width: 260px; height: 260px; object-fit: cover; border-radius: 16px; border: 1px solid rgba(212,175,55,0.3); box-shadow: 0 10px 25px rgba(0, 0, 0, 0.8); cursor: pointer; transition: all 0.5s cubic-bezier(0.25, 0.8, 0.25, 1); filter: grayscale(30%) brightness(0.8); }
            .smart-img:hover, .smart-img:active { filter: grayscale(0%) brightness(1.1); transform: scale(1.08) translateY(-10px); border-color: var(--gold-shine); box-shadow: 0 20px 40px rgba(212, 175, 55, 0.4); z-index: 10; }

            /* NEW FEATURE: Lightbox Pro Tools */
            .mnd-lightbox { position: fixed; inset: 0; background: rgba(0, 0, 0, 0.98); backdrop-filter: blur(25px); -webkit-backdrop-filter: blur(25px); z-index: 99999; display: none; flex-direction: column; align-items: center; justify-content: center; opacity: 0; transition: opacity 0.4s ease; }
            .mnd-lightbox.active { display: flex; opacity: 1; }
            .lb-close-btn { position: absolute; top: 25px; right: 25px; color: var(--gold-primary); font-size: 35px; cursor: pointer; z-index: 100000; text-shadow: 0 0 15px rgba(212, 175, 55, 0.5); transition: 0.3s; }
            .lb-close-btn:hover { color: #fff; transform: scale(1.1); }
            .lb-image { max-width: 95%; max-height: 60vh; border-radius: 12px; border: 2px solid var(--gold-primary); box-shadow: 0 15px 50px rgba(212, 175, 55, 0.3); object-fit: contain; animation: zoomIn 0.5s cubic-bezier(0.25, 1, 0.5, 1); }
            @keyframes zoomIn { from { transform: scale(0.8) translateY(20px); opacity: 0; } to { transform: scale(1) translateY(0); opacity: 1; } }
            
            .lb-text-container { margin-top: 25px; text-align: center; padding: 0 20px; max-width: 500px; animation: slideUpFade 0.6s ease forwards; animation-delay: 0.2s; opacity: 0; }
            @keyframes slideUpFade { to { opacity: 1; transform: translateY(0); } from { opacity: 0; transform: translateY(20px); } }
            .lb-title { font-family: 'Cinzel', serif; color: var(--gold-primary); font-size: 26px; font-weight: 900; margin: 0 0 8px 0; letter-spacing: 1px; text-transform: uppercase; }
            .lb-desc { font-family: 'Outfit', sans-serif; color: #ddd; font-size: 14px; line-height: 1.6; margin: 0 0 20px 0; font-weight: 300; }
            
            .lb-actions { display: flex; gap: 15px; justify-content: center; }
            .lb-action-btn { background: rgba(255,255,255,0.05); border: 1px solid var(--gold-primary); color: var(--gold-primary); padding: 10px 20px; border-radius: 30px; cursor: pointer; transition: 0.3s; font-family: 'Outfit'; font-weight: bold; display: flex; align-items: center; gap: 8px; font-size: 13px; }
            .lb-action-btn:hover { background: var(--gold-primary); color: #000; box-shadow: 0 0 15px rgba(212,175,55,0.5); }
        </style>

        <div id="gallery" class="container">
            <h2 class="gallery-title"><i class="fas fa-gem"></i> ELITE SHOWCASE</h2>
            <p class="gallery-subtitle">Swipe & Tap to Expand</p>
        </div>

        <div class="smart-slider-container">
            <div class="smart-track" id="autoScrollTrack">
                <img src="https://i.postimg.cc/R0smYWFp/2025-10-07-(5).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/Pf8H6rkd/2025-10-10-(1).png" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/Mp9mfwHd/2025-10-09.jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/5N3wDJB1/2025-10-10.png" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/g0RrFyC3/2025-10-07.jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/3JHsnX1r/2025-10-07-(6).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/3xxbcnv3/2025-10-07-(10).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/Vv7kBKCH/2025-10-07-(1).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/W38NT5X0/2025-10-07-(2).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/N0VVTmFm/2025-10-07-(8).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/pXpWMY8f/2025-10-07.png" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/9XySR4hN/2025-10-07-(9).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/kMhCs6ZG/2025-10-07-(3).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/Pr8gM6Yz/2025-10-07-(4).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/FFfr2V0k/2025-10-07-(1).png" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/k5k1DChn/2025-10-07-(2).png" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                
                <img src="https://i.postimg.cc/R0smYWFp/2025-10-07-(5).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/Pf8H6rkd/2025-10-10-(1).png" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/Mp9mfwHd/2025-10-09.jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/5N3wDJB1/2025-10-10.png" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/g0RrFyC3/2025-10-07.jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/3JHsnX1r/2025-10-07-(6).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/3xxbcnv3/2025-10-07-(10).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
                <img src="https://i.postimg.cc/Vv7kBKCH/2025-10-07-(1).jpg" class="smart-img" onclick="openLightbox(this.src)" loading="lazy">
            </div>
        </div>

        <div class="mnd-lightbox" id="mndLightbox">
            <i class="fas fa-times lb-close-btn" onclick="closeLightbox()"></i>
            <img src="" id="lightboxImg" class="lb-image" alt="Full Screen Event View">
            
            <div class="lb-text-container">
                <h3 class="lb-title">MAA NIRMALA EXCLUSIVE</h3>
                <p class="lb-desc">A perfect perspective on our signature event setups. From grand lighting to flawless stage designs, every detail is captured in full clarity.</p>
                <div class="lb-actions">
                    <button class="lb-action-btn" onclick="showToast('Starting HD Download...')"><i class="fas fa-download"></i> Save HD</button>
                    <button class="lb-action-btn" onclick="showToast('Link Copied to Clipboard!')"><i class="fas fa-share-alt"></i> Share</button>
                </div>
            </div>
        </div>

        <script>
            const track = document.getElementById('autoScrollTrack');
            let isAutoScrolling = true;
            let resumeTimeout;

            function autoSlide() {
                if (isAutoScrolling) {
                    track.scrollLeft += 1; // Smooth speed
                    if (track.scrollLeft >= (track.scrollWidth / 2)) {
                        track.scrollLeft = 0;
                    }
                }
                requestAnimationFrame(autoSlide);
            }
            requestAnimationFrame(autoSlide);

            track.addEventListener('touchstart', () => { isAutoScrolling = false; clearTimeout(resumeTimeout); }, {passive: true});
            track.addEventListener('touchend', () => { clearTimeout(resumeTimeout); resumeTimeout = setTimeout(() => { isAutoScrolling = true; }, 1500); });
            track.addEventListener('mouseenter', () => { isAutoScrolling = false; });
            track.addEventListener('mouseleave', () => { isAutoScrolling = true; });

            function openLightbox(imageSrc) {
                if(typeof playTap === 'function') playTap();
                const lightbox = document.getElementById('mndLightbox');
                document.getElementById('lightboxImg').src = imageSrc;
                lightbox.classList.add('active');
                isAutoScrolling = false;
            }

            function closeLightbox() {
                document.getElementById('mndLightbox').classList.remove('active');
                isAutoScrolling = true;
            }

            document.getElementById('mndLightbox').addEventListener('click', function(e) {
                if (e.target === this) closeLightbox();
            });
        </script>

        <style>
            .slide-card { flex: 0 0 85%; max-width: 380px; scroll-snap-align: center; background: #111; border: 1px solid var(--border-color); border-radius: 20px; overflow: hidden; position: relative; box-shadow: 0 8px 25px rgba(0,0,0,0.6); transition: transform 0.4s cubic-bezier(0.25, 0.8, 0.25, 1), box-shadow 0.4s; }
            .slide-card:hover { transform: translateY(-10px) scale(1.02); box-shadow: 0 20px 40px rgba(212, 175, 55, 0.3); border-color: var(--gold-primary); z-index: 5; }
            .slide-card img { width: 100%; height: 240px; object-fit: cover; display: block; border-bottom: 2px solid var(--gold-primary); transition: transform 0.5s; }
            .slide-card:hover img { transform: scale(1.08); }
            
            .slide-info { padding: 20px; text-align: center; background: linear-gradient(0deg, #050505 80%, transparent); position: absolute; bottom: 0; width: 100%; }
            .slide-info h3 { color: var(--gold-primary); font-family: 'Rajdhani', sans-serif; font-size: 22px; font-weight: 800; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 8px; text-shadow: 0 2px 5px #000; }
            .slide-info div { font-size: 13px; color: #ddd; font-weight: 300; line-height: 1.5; }
            
            /* NEW FEATURE: Premium Badges */
            .card-badge { position: absolute; top: 15px; right: 15px; background: linear-gradient(135deg, #ff3333, #990000); color: #fff; padding: 5px 12px; font-size: 10px; font-weight: 900; font-family: 'Outfit'; border-radius: 30px; z-index: 5; text-transform: uppercase; letter-spacing: 1px; box-shadow: 0 5px 15px rgba(255,51,51,0.5); border: 1px solid rgba(255,255,255,0.3); }
            .card-badge.gold { background: linear-gradient(135deg, #D4AF37, #b08d26); color: #000; box-shadow: 0 5px 15px rgba(212,175,55,0.5); }
        </style>

        <div class="container" style="margin-top: 50px;">
            <div class="section-label"><i class="fas fa-star"></i> BEST OF MAA NIRMALA DJ</div>
            <div class="slider-container">

                <div class="slide-card">
                    <div class="card-badge gold"><i class="fas fa-crown"></i> Premium</div>
                    <img src="https://i.postimg.cc/pXx5fqGQ/image_fac9be10.png" alt="Royal Wedding Setup" loading="lazy">
                    <div class="slide-info">
                        <h3>Royal Wedding Pandals</h3>
                        <div>Experience the ultimate grandeur with our luxurious, imported fabric drapery and custom architectural setups designed for unforgettable Beltikri weddings.</div>
                    </div>
                </div>

                <div class="slide-card">
                    <div class="card-badge"><i class="fas fa-fire"></i> Trending</div>
                    <img src="https://i.postimg.cc/g20XqtDW/IMG_20260303_121446.png" alt="Heavy DJ Setup" loading="lazy">
                    <div class="slide-info">
                        <h3>Earth-Shattering DJ Rigs</h3>
                        <div>Dominate the dance floor with our massive dual subwoofers and crystal-clear line arrays. Pure acoustic supremacy for the ultimate high-energy Baaraat.</div>
                    </div>
                </div>

                <div class="slide-card">
                    <img src="https://i.postimg.cc/cLJgMkmJ/maxresdefault.jpg" alt="Lighting Setup" loading="lazy">
                    <div class="slide-info">
                        <h3>Intelligent DMX Lighting</h3>
                        <div>Transform the night sky with synchronized 3D laser shows, brilliant LED wash lights, and cinematic cold spark pyro effects synced perfectly to the beat.</div>
                    </div>
                </div>

                <div class="slide-card">
                    <div class="card-badge gold"><i class="fas fa-utensils"></i> VIP Setup</div>
                    <img src="https://i.postimg.cc/76mz1v2j/file-0000000090a471fa84cbecd48a774885.png" alt="Catering Setup" loading="lazy">
                    <div class="slide-info">
                        <h3>Elite Gastronomy & Catering</h3>
                        <div>Serving culinary perfection with high-hygiene industrial cooking setups, premium bone china, and a vast menu of authentic, mouth-watering traditional flavors.</div>
                    </div>
                </div>

                <div class="slide-card">
                    <img src="https://i.postimg.cc/5yRdctZh/1771529133710.jpg" alt="Tent Structure" loading="lazy">
                    <div class="slide-info">
                        <h3>Heavy-Duty Iron Trusses</h3>
                        <div>Unyielding structural integrity featuring waterproof, industrial-grade iron rigging to keep your VIP guests safe and incredibly comfortable in any weather.</div>
                    </div>
                </div>

                <div class="slide-card">
                    <img src="https://i.postimg.cc/hPgQLpyz/image_b73be3f2_1.png" alt="Floral Decoration" loading="lazy">
                    <div class="slide-info">
                        <h3>Bespoke Floral Architecture</h3>
                        <div>Breathtaking Varmala stages and intricate floral archways crafted by expert designers using the absolute freshest orchids, roses, and vibrant marigolds.</div>
                    </div>
                </div>

                <div class="slide-card">
                    <img src="https://i.postimg.cc/bwFG60Cv/image_ae71021a.png" alt="Generator Setup" loading="lazy">
                    <div class="slide-info">
                        <h3>Silent Power Infrastructure</h3>
                        <div>Uninterrupted celebrations powered by our highly reliable, heavy-duty Silent DG Sets. Absolute electrical reliability with zero flickering or darkness.</div>
                    </div>
                </div>

                <div class="slide-card">
                    <div class="card-badge"><i class="fas fa-truck-moving"></i> Fast</div>
                    <img src="https://i.postimg.cc/pdyF9r0J/image_143d2d44.png" alt="Transport Logistics" loading="lazy">
                    <div class="slide-info">
                        <h3>Flawless Heavy Logistics</h3>
                        <div>Backed by Laxmikant Transport, our formidable mechanical fleet guarantees the punctual, safe delivery of colossal payloads to any remote venue.</div>
                    </div>
                </div>

            </div>

            <div class="section-label" id="liveGallerySection" style="margin-top: 50px;"><i class="fas fa-broadcast-tower"></i> LIVE UPDATES & FEED</div>
            <div class="feed-container" id="dynamicGallery" style="min-height: 150px; position: relative;">
                </div>

            <style>
                .team-card { flex: 0 0 85%; max-width: 320px; scroll-snap-align: center; text-align: center; background: #0a0a0c; border-radius: 26px; border: 1px solid rgba(212,175,55,0.2); padding: 40px 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.5); position: relative; overflow: hidden; transition: 0.4s; }
                
                /* NEW FEATURE: Animated Edge Glow on Hover */
                .team-card::after { content: ''; position: absolute; inset: 0; border: 2px solid transparent; background: linear-gradient(45deg, var(--gold-primary), transparent, var(--gold-primary)) border-box; -webkit-mask: linear-gradient(#fff 0 0) padding-box, linear-gradient(#fff 0 0); -webkit-mask-composite: destination-out; mask-composite: exclude; opacity: 0; transition: 0.5s; border-radius: inherit; pointer-events: none; }
                .team-card:hover::after { opacity: 1; animation: spinBorder 4s linear infinite; }
                @keyframes spinBorder { 100% { background: linear-gradient(405deg, var(--gold-primary), transparent, var(--gold-primary)) border-box; } }
                
                .team-card:hover { transform: translateY(-5px); background: #111; }
                .team-card img { width: 140px; height: 140px; object-fit: cover; border-radius: 50%; border: 4px solid var(--gold-primary); margin-bottom: 20px; box-shadow: 0 10px 25px rgba(212, 175, 55, 0.3); transition: 0.4s; }
                .team-card:hover img { transform: scale(1.05); border-color: #fff; }
                .team-card h1 { font-size: 26px; font-weight: 900; margin: 5px 0; background: linear-gradient(90deg,#FFD700,#fff,#FFD700); background-size: 200% auto; -webkit-background-clip: text; -webkit-text-fill-color: transparent; font-family: 'Rajdhani'; animation: textDeepShine 3s linear infinite; }
                .team-card h3 { font-size: 14px; color: var(--gold-primary); margin-bottom: 15px; text-transform: uppercase; letter-spacing: 2px; font-weight: 800; }
                .team-card p { font-size: 14px; line-height: 1.6; color: #bbb; margin-bottom: 10px; font-family: 'Outfit'; }
            </style>

            <div class="section-label" style="margin-top:50px;"><i class="fas fa-users"></i> EXECUTIVE MANAGEMENT</div>
            <div class="slider-container">
                <div class="team-card">
                    <img src="https://i.postimg.cc/6qbJj3hQ/Screenshot-2026-01-14-15-25-06-57-1c337646f29875672b5a61192b9010f9-2.jpg" alt="Anil Kumar" loading="lazy">
                    <h1>Anil Kumar</h1>
                    <h3>Owner & Founder</h3>
                    <p>A passionate and visionary individual providing the absolute best event setups, high-fidelity DJ sound, and premium Tent services across Bihar.</p>
                </div>
                <div class="team-card">
                    <img src="https://i.postimg.cc/7Y7rMx2y/Screenshot-2026-01-14-15-33-01-78-965bbf4d18d205f782c6b8409c5773a4-2.jpg" alt="Mr. Sildhar Kumar" loading="lazy">
                    <h1>Mr. Sildhar Kumar</h1>
                    <h3>Business Dev. Manager</h3>
                    <p>Ensuring top-tier service delivery, impeccable logistics, and managing all monumental event setups seamlessly across the entire district.</p>
                </div>
                <div class="team-card">
                    <img src="https://i.postimg.cc/qMWWzWbF/Screenshot-2026-01-14-15-29-44-90-965bbf4d18d205f782c6b8409c5773a4.jpg" alt="Mr. Sanjay Kumar" loading="lazy">
                    <h1>Mr. Sanjay Kumar</h1>
                    <h3>Business Dev. Manager</h3>
                    <p>Spearheading operational excellence, ground team coordination, and ensuring absolute safety standards at every grand celebration.</p>
                </div>
                <div class="team-card">
                    <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Lalu Kumar" loading="lazy">
                    <h1>Lalu Kumar</h1>
                    <h3>Business Associate</h3>
                    <p>Expertly coordinating premium tent decorations, intelligent lighting arrangements, and dedicated, personalized VIP client relations.</p>
                </div>
            </div>
        </div>
        <style>
            .owner-profile { background: var(--bg-card); border-radius: 26px; border: 1px solid var(--border-color); padding: 40px 25px; box-shadow: 0 10px 30px rgba(0,0,0,0.5); margin-bottom: 40px; position: relative; overflow: hidden; backdrop-filter: var(--glass-blur); transition: 0.4s; }
            .owner-profile:hover { border-color: var(--gold-primary); box-shadow: 0 15px 40px rgba(212,175,55,0.2); }
            
            /* NEW FEATURE: Glowing Map Container */
            .map-container { background: #0a0a0c; padding: 20px; border-radius: 26px; border: 1px solid var(--border-color); box-shadow: 0 10px 30px rgba(0,0,0,0.6); position: relative; transition: 0.4s; }
            .map-container:hover { border-color: var(--gold-primary); transform: translateY(-5px); box-shadow: 0 20px 50px rgba(212,175,55,0.3); }
            .map-wrapper { width: 100%; aspect-ratio: 16 / 9; border-radius: 16px; overflow: hidden; border: 2px solid var(--gold-primary); box-shadow: inset 0 0 20px rgba(0,0,0,0.8); }
        </style>

        <div class="container reveal-on-scroll">
            <div class="section-label" style="margin-top:50px;"><i class="fas fa-info-circle"></i> ABOUT THE BUSINESS</div>
            <div class="owner-profile">
                <h1 style="text-align: center; font-size: 32px; font-family: 'Cinzel'; font-weight: 900; margin-bottom: 5px;">Maa Nirmala DJ & Tent House</h1>
                <p style="text-align: center; color: var(--gold-primary); font-weight: 800; margin-bottom: 25px; text-transform: uppercase; letter-spacing: 2px; font-family: 'Rajdhani';">Premium Event Management in Bihar</p>
                <p style="font-size: 15px; color: #ccc; line-height: 1.8;">Welcome to <b>Maa Nirmala DJ & Tent House</b>, the premier event management and setup service based in Beltikri. We specialize in transforming ordinary events into grand, unforgettable celebrations.</p>
                <ul style="color: #eaeaea; font-size: 15px; line-height: 2; margin-left: 20px; margin-bottom: 30px; margin-top: 20px; font-family: 'Outfit';">
                    <li><b style="color: var(--gold-primary);">Elite DJ Setups:</b> High-fidelity sound systems, heavy bass, and non-stop entertainment.</li>
                    <li><b style="color: var(--gold-primary);">Premium Tent Houses:</b> Grand wedding tents, VIP seating, and beautiful decorations.</li>
                    <li><b style="color: var(--gold-primary);">Stage Lighting:</b> Advanced dynamic lighting to illuminate your special moments.</li>
                </ul>
                <div style="border-top: 1px dashed rgba(212,175,55,0.4); margin: 30px 0;"></div>
                <div style="text-align: center;">
                    <img src="https://i.postimg.cc/6qbJj3hQ/Screenshot-2026-01-14-15-25-06-57-1c337646f29875672b5a61192b9010f9-2.jpg" alt="Anil Kumar" style="width: 120px; height: 120px; margin-bottom: 15px; border: 4px solid var(--gold-primary); border-radius: 50%; object-fit: cover; display: inline-block; box-shadow: 0 10px 20px rgba(0,0,0,0.5);">
                    <h2 style="color: var(--gold-primary); font-family: 'Cinzel'; font-size: 26px; font-weight: 900;">Anil Kumar Tanti</h2>
                    <h3 style="font-size: 13px; color: #aaa; margin-bottom: 15px; text-transform: uppercase; letter-spacing: 3px; font-family: 'Outfit';">Founder & Owner</h3>
                </div>
            </div>

            <div class="section-label reveal-on-scroll"><i class="fas fa-map-marker-alt"></i> OUR LOCATION</div>
            <div class="map-container reveal-on-scroll">
                <p style="text-align: center; color: var(--gold-primary); font-family: 'Cinzel'; font-weight: 900; font-size: 22px; margin-bottom: 5px;">Maa Nirmala DJ & Tent House</p>
                <p style="text-align: center; font-size: 13px; color: #aaa; margin-bottom: 20px; font-family: 'Outfit'; letter-spacing: 1px; text-transform: uppercase;">JRPM+RQ, Beltikri, Tola Tetaria, Bihar 813106</p>
                
                <div class="map-wrapper">
                    <iframe src="https://maps.google.com/maps?q=JRPM%2BRQ%20Beltikri,%20Bihar%20813106&t=&z=16&ie=UTF8&iwloc=&output=embed" width="100%" height="100%" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
                </div>
                
                <a href="https://www.google.com/maps/dir/?api=1&destination=JRPM%2BRQ,+Beltikri,+Bihar+813106" target="_blank" style="display: flex; justify-content: center; align-items: center; gap: 10px; width: 100%; padding: 18px; background: linear-gradient(90deg, var(--gold-primary), #b08d26); color: #000; font-weight: 900; border-radius: 12px; text-decoration: none; margin-top: 20px; font-family: 'Rajdhani'; font-size: 16px; letter-spacing: 2px; transition: 0.3s; box-shadow: 0 5px 15px rgba(212,175,55,0.4);">
                    <i class="fas fa-directions"></i> GET DIRECTIONS TO MAP
                </a>
            </div>
        </div>

        <style>
            .experience-card { background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 20px; padding: 25px; text-align: center; box-shadow: 0 10px 30px rgba(0,0,0,0.5); transition: 0.4s; backdrop-filter: var(--glass-blur); }
            .experience-card:hover { transform: translateY(-10px); border-color: var(--gold-primary); box-shadow: 0 20px 40px rgba(212,175,55,0.2); }
            .experience-card img { width: 100%; height: 220px; object-fit: cover; border-radius: 12px; border: 2px solid var(--gold-primary); margin-bottom: 20px; }
            .reveal-on-scroll { opacity: 0; transform: translateY(40px); transition: all 0.8s cubic-bezier(0.25, 0.8, 0.25, 1); }
            .reveal-on-scroll.visible { opacity: 1; transform: translateY(0); }
        </style>

        <div class="container" style="margin-top: 50px;">
            <div class="section-label reveal-on-scroll"><i class="fas fa-magic"></i> THE MAA NIRMALA EXPERIENCE</div>
            
            <div class="grid" style="grid-template-columns: 1fr; gap: 30px;">
                <div class="experience-card reveal-on-scroll">
                    <img src="https://i.postimg.cc/Vv6QHtHD/1771530083282.jpg" alt="Experience">
                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel'; margin-bottom: 15px; font-size: 24px; font-weight: 800;">Our Sound & Vibes</h3>
                    <p style="font-size: 15px; line-height: 1.8; color: #ddd; font-family: 'Outfit';">Maa Nirmala DJ sets the standard for high-energy celebrations in Banka. With state-of-the-art audio, dazzling light shows, and premium VIP tents, we guarantee a flawless event. From intimate functions to massive district festivals, our team works tirelessly to bring your dream event to reality.</p>
                </div>
                
                <div class="experience-card reveal-on-scroll">
                    <img src="https://i.postimg.cc/hPgQLpyz/image_b73be3f2_1.png" alt="Experience">
                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel'; margin-bottom: 15px; font-size: 24px; font-weight: 800;">Decoration & Tent House</h3>
                    <p style="font-size: 15px; line-height: 1.8; color: #ddd; font-family: 'Outfit';">Maa Nirmala DJ sets the standard for high-energy celebrations in Banka. With state-of-the-art audio, dazzling light shows, and premium VIP tents, we guarantee a flawless event. From intimate functions to massive district festivals, our team works tirelessly to bring your dream event to reality.</p>
                </div>
            </div>

            <div class="reveal-on-scroll" style="width: 100%; padding: 60px 15px; display: flex; flex-direction: column; align-items: center; text-align: center;">
                <div class="section-label" style="justify-content: center; margin-bottom: 40px; border-bottom: none;"><i class="fas fa-crown"></i> The Maa Nirmala Experience</div>

                <div style="max-width: 800px;">
                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel', serif; margin-bottom: 20px; font-size: 26px; font-weight: 900; letter-spacing: 1px;">THE PINNACLE OF PREMIUM CELEBRATIONS</h3>
                    <p style="font-size: 16px; line-height: 1.8; color: #ccc; margin-bottom: 40px; font-family: 'Outfit';">Maa Nirmala DJ & Tent House sets the absolute standard for high-energy, luxurious celebrations across Banka. Under the visionary leadership of Mr. Lalu Kumar Tanti, we have transformed countless events from ordinary gatherings into extraordinary cinematic experiences. Situated in the historic heart of Beltikri, Kaddhar, Katoria, our dedicated team works tirelessly to bring your ultimate dream event to reality with unmatched precision. We believe that a celebration is not merely a date on a calendar, but a profound milestone in human life that deserves the utmost reverence, spectacular visual beauty, and flawless technical execution.</p>

                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel', serif; margin-bottom: 20px; font-size: 22px; font-weight: 800; letter-spacing: 1px;">THE SUPREMACY OF ACOUSTIC ENGINEERING</h3>
                    <p style="font-size: 16px; line-height: 1.8; color: #ccc; margin-bottom: 40px; font-family: 'Outfit';">The soul of any grand event is its acoustic heartbeat. At Maa Nirmala DJ, we do not simply play music; we engineer an auditory atmosphere that captivates the senses. We deploy state-of-the-art, heavy-duty subwoofers that push massive volumes of air, ensuring an earth-shattering bass response that you can feel resonating in your very soul. Complementing this low-end power are our crystal-clear, high-frequency line-array top speakers, strategically positioned to cast sound evenly across massive venues without a single hint of distortion.</p>

                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel', serif; margin-bottom: 20px; font-size: 22px; font-weight: 800; letter-spacing: 1px;">DYNAMIC VISUAL VIBES & INTELLIGENT LIGHTING</h3>
                    <p style="font-size: 16px; line-height: 1.8; color: #ccc; margin-bottom: 40px; font-family: 'Outfit';">Sound alone cannot carry a premium event; it must be paired with a breathtaking visual spectacle. We utilize intelligent, programmable DMX lighting systems to paint the venue in vibrant colors and dynamic movement. Our synchronized laser light shows slice through the darkness, while our powerful moving head beams track the tempo of the music, creating an immersive, concert-level club environment right at your venue.</p>

                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel', serif; margin-bottom: 20px; font-size: 22px; font-weight: 800; letter-spacing: 1px;">ROYAL TENT ARCHITECTURE</h3>
                    <p style="font-size: 16px; line-height: 1.8; color: #ccc; margin-bottom: 40px; font-family: 'Outfit';">Beyond the music and lights, we construct magnificent, temporary palaces. Our premium tent setups are feats of structural engineering, built using heavy-duty iron trusses and highly secure rigging systems that guarantee absolute safety and stability. We construct massive waterproof pandals draped in miles of luxurious, imported fabrics that cascade elegantly from towering ceilings.</p>

                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel', serif; margin-bottom: 20px; font-size: 22px; font-weight: 800; letter-spacing: 1px;">BESPOKE FLORAL DECOR & STAGE CRAFTSMANSHIP</h3>
                    <p style="font-size: 16px; line-height: 1.8; color: #ccc; margin-bottom: 40px; font-family: 'Outfit';">The stage is the undisputed focal point of your celebration. We seamlessly blend traditional Indian wedding aesthetics with modern design trends. Utilizing thousands of fresh, vibrant blooms, our decorators construct intricate floral archways, majestic entry gates (Dwar), and stunning photo booths.</p>

                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel', serif; margin-bottom: 20px; font-size: 22px; font-weight: 800; letter-spacing: 1px;">UNYIELDING POWER BACKUP SYSTEMS</h3>
                    <p style="font-size: 16px; line-height: 1.8; color: #ccc; margin-bottom: 40px; font-family: 'Outfit';">A luxury event cannot afford a single millisecond of darkness. Recognizing the unpredictability of local power grids, Maa Nirmala DJ & Tent House provides absolute power reliability through heavy-duty, silent generator (DG) sets capable of sustaining the enormous electrical load required by our equipment.</p>

                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel', serif; margin-bottom: 20px; font-size: 22px; font-weight: 800; letter-spacing: 1px;">LOGISTICAL MIGHT & TRANSPORT EFFICIENCY</h3>
                    <p style="font-size: 16px; line-height: 1.8; color: #ccc; margin-bottom: 40px; font-family: 'Outfit';">Supported powerfully by Laxmikant Tanti farming tractor services, we possess the logistical might to deliver massive payloads of equipment to any venue, no matter how remote the location in Banka district.</p>

                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel', serif; margin-bottom: 20px; font-size: 22px; font-weight: 800; letter-spacing: 1px;">MASTERING EVERY TYPE OF CELEBRATION</h3>
                    <p style="font-size: 16px; line-height: 1.8; color: #ccc; margin-bottom: 40px; font-family: 'Outfit';">Our expertise is not limited to a single type of event. We are masters of versatility, providing royal elegance for weddings, massive high-capacity structures for district melas, and heavy-bass neon experiences for birthday bashes.</p>

                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel', serif; margin-bottom: 20px; font-size: 22px; font-weight: 800; letter-spacing: 1px;">SAFETY PROTOCOLS & ON-SITE MANAGEMENT</h3>
                    <p style="font-size: 16px; line-height: 1.8; color: #ccc; margin-bottom: 40px; font-family: 'Outfit';">True luxury includes the luxury of peace of mind. Every heavy iron pillar is firmly anchored, and our on-site management team remains hyper-vigilant, continuously monitoring the structural integrity and audio-visual output.</p>

                    <h3 style="color: var(--gold-primary); font-family: 'Cinzel', serif; margin-bottom: 20px; font-size: 22px; font-weight: 800; letter-spacing: 1px;">A LEGACY BUILT ON TRUST</h3>
                    <p style="font-size: 16px; line-height: 1.8; color: #ccc; margin-bottom: 20px; font-family: 'Outfit';">For years, the communities of Beltikri, Katoria, and the greater Banka region have trusted us. Built by Mr. Lalu Kumar Tanti upon total transparency and quality. Choose us, and let us engineer the perfect, unforgettable night.</p>
                </div>
            </div>
        </div>

        <div style="text-align: center; max-width: 800px; margin: 50px auto 40px auto; padding: 0 20px;" class="reveal-on-scroll">
            <h4 style="color: var(--gold-primary); font-family: 'Cinzel', serif; font-size: 20px; margin-bottom: 25px; letter-spacing: 2px; text-transform: uppercase; font-weight: 900;">
                <i class="fas fa-link"></i> Follow & Connect
            </h4>
            <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; max-width: 600px; margin: 0 auto;">
                <a href="https://www.instagram.com/maa_nirmala_dj" target="_blank" class="nav-btn-square theme-btn" style="width:50px; height:50px; font-size:24px;" title="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="https://www.facebook.com/MaaNirmalaDJ7" target="_blank" class="nav-btn-square theme-btn" style="width:50px; height:50px; font-size:24px;" title="Facebook"><i class="fab fa-facebook-f"></i></a>
                <a href="https://x.com/maa_nirmala_dj" target="_blank" class="nav-btn-square theme-btn" style="width:50px; height:50px; font-size:24px;" title="X"><i class="fab fa-x-twitter"></i></a>
                <a href="https://maanirmaladj.github.io/Maa-Nirmala-DJ-Beltikri/" target="_blank" class="nav-btn-square theme-btn" style="width:50px; height:50px; font-size:24px;" title="Website"><i class="fas fa-globe"></i></a>
                <a href="https://www.linkedin.com/in/maa-nirmala-dj-tent-house-3499a33b0" target="_blank" class="nav-btn-square theme-btn" style="width:50px; height:50px; font-size:24px;" title="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
                <a href="https://www.youtube.com/channel/UCQPUgEyCm8nihqhYGMUX6Pw" target="_blank" class="nav-btn-square theme-btn" style="width:50px; height:50px; font-size:24px;" title="YouTube"><i class="fab fa-youtube"></i></a>
                <a href="https://whatsapp.com/channel/0029Vb7AMDl4IBhJ34po3L1k" target="_blank" class="nav-btn-square theme-btn" style="width:50px; height:50px; font-size:24px;" title="WhatsApp"><i class="fab fa-whatsapp"></i></a>
                <a href="https://t.me/MaaNirmalaDJ" target="_blank" class="nav-btn-square theme-btn" style="width:50px; height:50px; font-size:24px;" title="Telegram"><i class="fab fa-telegram-plane"></i></a>
            </div>
            
            <div style="margin-top:50px; margin-bottom:40px;">
                <div style="color:var(--gold-primary); font-weight:800; font-size:13px; font-family:'Outfit'; letter-spacing: 1px;">© 2026 All Rights Reserved — Maa Nirmala DJ & Tent House</div>
            </div>
        </div>

        <div class="bottom-nav">
            <div class="nav-item active" id="navHome" onclick="navAction('home')"><i class="fas fa-home"></i><span>Home</span></div>
            <div class="nav-item" id="navLinks" onclick="navAction('links')"><i class="fas fa-link"></i><span>Links</span></div>
            <div class="nav-item" id="navBooking" onclick="navAction('booking')"><i class="fas fa-calendar-alt"></i><span>Booking</span></div>
            <div class="nav-item" id="navLogin" onclick="navAction('login')"><i class="fas fa-user-shield"></i><span>Admin</span></div>
        </div>
        
        <div class="ai-trigger" onclick="openModal('aiModalOverlay')"><i class="fas fa-brain"></i></div>

        <style>
            .price-card { background: rgba(255,255,255,0.03); border: 1px solid rgba(212,175,55,0.3); border-radius: 15px; padding: 18px; margin-bottom: 15px; display: flex; justify-content: space-between; align-items: center; transition: 0.3s; }
            .price-card:hover { border-color: var(--gold-primary); background: rgba(212,175,55,0.1); transform: translateX(5px); }
            .price-title { font-family: 'Cinzel'; font-weight: 800; font-size: 16px; color: #fff; margin-bottom: 4px;}
            .price-amt { color: var(--gold-primary); font-size: 22px; font-weight: 900; font-family: 'Rajdhani'; text-shadow: 0 0 10px rgba(212,175,55,0.4); }
        </style>
        <div class="unified-modal-overlay" id="priceModal" onclick="closeOnBackgroundClick(event, 'priceModal')">
            <div class="unified-modal-box" style="height: 85vh; max-width: 550px;">
                <div class="modal-header-pro"><h2 class="modal-title-pro"><i class="fas fa-tags"></i> Standard Price List</h2><span onclick="closeModal('priceModal')" class="modal-close-pro">&times;</span></div>
                <div style="flex-grow:1; overflow-y:auto; padding:20px;">
                    <p style="color:#aaa; font-size:12px; margin-bottom:20px; text-align:center; font-family:'Outfit';">*Prices are estimated starting points and vary based on specific event requirements.</p>
                    
                    <div class="price-card"><div><div class="price-title">Heavy DJ Setup</div><div style="font-size:12px; color:#aaa;">Dual Bass, Tops, Light & Operator</div></div><div class="price-amt">₹8,000+</div></div>
                    <div class="price-card"><div><div class="price-title">Grand Wedding Tent</div><div style="font-size:12px; color:#aaa;">Pandal, Chairs, VIP Sofa, Carpet</div></div><div class="price-amt">₹25,000+</div></div>
                    <div class="price-card"><div><div class="price-title">Stage Decoration</div><div style="font-size:12px; color:#aaa;">Floral Setup, Lighting, Backdrop</div></div><div class="price-amt">₹10,000+</div></div>
                    <div class="price-card" style="border-color: var(--gold-primary); box-shadow: 0 0 15px rgba(212,175,55,0.2);"><div><div class="price-title" style="color:var(--gold-primary);">Complete Package <i class="fas fa-star"></i></div><div style="font-size:12px; color:#aaa;">DJ + Tent + Lighting Full Setup</div></div><div class="price-amt">Custom</div></div>
                    <div class="price-card"><div><div class="price-title">Standard Sound System</div><div style="font-size:12px; color:#aaa;">2 Bass, 2 Tops, Mixer & Mics</div></div><div class="price-amt">₹5,000+</div></div>
                    <div class="price-card"><div><div class="price-title">Mega Concert DJ Rig</div><div style="font-size:12px; color:#aaa;">4 Heavy Bass, Line Array Tops, DMX Lights</div></div><div class="price-amt">₹15,000+</div></div>
                    <div class="price-card"><div><div class="price-title">Baaraat DJ Trolley</div><div style="font-size:12px; color:#aaa;">Moving Sound Setup with Lights</div></div><div class="price-amt">₹12,000+</div></div>
                    <div class="price-card"><div><div class="price-title">Premium VIP Pandal</div><div style="font-size:12px; color:#aaa;">Luxury Waterproof Enclosure</div></div><div class="price-amt">₹35,000+</div></div>
                    <div class="price-card"><div><div class="price-title">Heavy Duty Generator</div><div style="font-size:12px; color:#aaa;">Uninterrupted DG Set Power</div></div><div class="price-amt">₹4,000+</div></div>
                    <div class="price-card"><div><div class="price-title">Birthday Blast Package</div><div style="font-size:12px; color:#aaa;">Tent, DJ, Balloon & Decor</div></div><div class="price-amt">₹12,000+</div></div>

                    <button class="f-btn" style="margin-top: 20px;" onclick="switchHubModal('priceModal', 'bookModal')"><i class="fas fa-calendar-check"></i> BOOK NOW FOR EXACT QUOTE</button>
                </div>
            </div>
        </div>

        <div class="unified-modal-overlay" id="linksModal" onclick="closeOnBackgroundClick(event, 'linksModal')">
            <div class="unified-modal-box" style="padding:0; max-width: 500px; height: 85vh;">
                <div class="modal-header-pro"><h2 class="modal-title-pro"><i class="fas fa-link"></i> OFFICIAL LINKS HUB</h2><span onclick="closeModal('linksModal')" class="modal-close-pro">&times;</span></div>
                <div style="flex-grow:1; overflow-y:auto; padding:20px;">
                    <div class="section-label" style="margin-top: 0;"><i class="fas fa-bolt"></i> DIRECT CONNECT</div>
                    <div class="grid">
                        <a href="tel:+919771617808" class="card" onclick="playTap()"><i class="fas fa-phone-volume"></i><span>Call Now</span></a>
                        <a href="https://wa.me/919771617808" class="card" onclick="playTap()"><i class="fab fa-whatsapp"></i><span>WhatsApp</span></a>
                        <a href="https://t.me/MaaNirmalaDJ" class="card" onclick="playTap()"><i class="fab fa-telegram-plane"></i><span>Telegram</span></a>
                        <a href="https://www.google.com/maps/dir/?api=1&destination=JRPM%2BRQ,+Beltikri,+Bihar+813106" target="_blank" class="card full-w" onclick="playTap()"><i class="fas fa-map-marked-alt"></i><span>Official Location</span></a>
                    </div>
                    <div class="section-label"><i class="fas fa-globe"></i> SOCIAL EMPIRE</div>
                    <div class="grid">
                        <a href="https://www.instagram.com/maa_nirmala_dj" class="card" onclick="playTap()"><i class="fab fa-instagram"></i><span>Instagram</span></a>
                        <a href="https://www.facebook.com/MaaNirmalaDJ7" class="card" onclick="playTap()"><i class="fab fa-facebook-f"></i><span>Facebook</span></a>
                        <a href="https://www.youtube.com/channel/UCQPUgEyCm8nihqhYGMUX6Pw" class="card full-w" onclick="playTap()"><i class="fab fa-youtube"></i><span>YouTube</span></a>
                    </div>
                    <div class="section-label"><i class="fas fa-coins"></i> PAYMENTS & MORE</div>
                    <div class="grid" style="margin-bottom:30px;">
                        <div class="card" onclick="copyUPI()"><i class="fas fa-wallet"></i><span>PhonePe</span></div>
                        <div class="card" onclick="copyUPI()"><i class="fab fa-google-pay"></i><span>GPay</span></div>
                        <div class="card full-w" onclick="copyUPI()"><i class="fas fa-qrcode"></i><span>Copy UPI ID</span><span style="font-size:10px; color:#aaa; margin-top:5px; text-transform:lowercase;">9771617808-2@axl</span></div>
                    </div>
                </div>
            </div>
        </div>

        <style>
            .star-rating { display: flex; flex-direction: row-reverse; justify-content: center; gap: 10px; margin: 15px 0 25px; }
            .star-rating input { display: none; }
            .star-rating label { font-size: 40px; color: #333; cursor: pointer; transition: 0.2s; text-shadow: 0 0 10px rgba(0,0,0,0.5); }
            .star-rating input:checked ~ label, .star-rating label:hover, .star-rating label:hover ~ label { color: var(--gold-primary); text-shadow: 0 0 20px var(--gold-primary); transform: scale(1.1); }
        </style>
        <div class="unified-modal-overlay" id="feedbackModal" onclick="closeOnBackgroundClick(event, 'feedbackModal')">
            <div class="unified-modal-box" style="max-width: 480px;">
                <div class="modal-header-pro"><h2 class="modal-title-pro"><i class="fas fa-star"></i> CLIENT FEEDBACK</h2><span onclick="closeModal('feedbackModal')" class="modal-close-pro">&times;</span></div>
                <div style="padding: 25px;">
                    <div style="text-align:center; margin-bottom:20px; background: rgba(212,175,55,0.05); padding: 15px; border-radius: 12px; border: 1px solid rgba(212,175,55,0.2);">
                        <h3 style="color:var(--gold-primary); font-family:'Cinzel'; font-size: 22px; font-weight:800; margin-bottom:5px;">Maa Nirmala DJ</h3>
                        <p style="font-size:13px; color:#ddd; font-family:'Outfit';">Rate your premium experience with us!</p>
                    </div>
                    <div class="star-rating">
                        <input type="radio" id="star5" name="rating" value="5"><label for="star5" class="fas fa-star"></label>
                        <input type="radio" id="star4" name="rating" value="4"><label for="star4" class="fas fa-star"></label>
                        <input type="radio" id="star3" name="rating" value="3"><label for="star3" class="fas fa-star"></label>
                        <input type="radio" id="star2" name="rating" value="2"><label for="star2" class="fas fa-star"></label>
                        <input type="radio" id="star1" name="rating" value="1"><label for="star1" class="fas fa-star"></label>
                    </div>
                    <div class="f-group"><span class="f-label">Your Name</span><input type="text" id="fb-name" class="f-input" placeholder="Enter your name"></div>
                    <div class="f-group"><span class="f-label">Your Experience & Feedback</span><textarea id="fb-text" class="f-input" rows="4" placeholder="Tell us what you liked..." style="resize:none;"></textarea></div>
                    <button class="f-btn" onclick="submitFeedback()" id="submitFbBtn"><i class="fas fa-paper-plane"></i> SEND SECURE FEEDBACK</button>
                </div>
            </div>
        </div>

        <div class="unified-modal-overlay" id="bookModal" onclick="closeOnBackgroundClick(event, 'bookModal')">
            <div class="unified-modal-box" style="height: 90vh; max-width: 550px;">
                <div class="modal-header-pro"><h2 class="modal-title-pro"><i class="fas fa-calendar-check"></i> OFFICIAL BOOKING</h2><span onclick="closeModal('bookModal')" class="modal-close-pro">&times;</span></div>
                <div style="flex-grow:1; overflow-y:auto; padding:25px;">
                    <div class="f-group"><span class="f-label">Event / Requirement Type *</span><input type="text" id="b-type" class="f-input" placeholder="e.g. Wedding DJ, VIP Tent"></div>
                    <div style="display: flex; gap: 15px; margin-bottom: 15px;">
                        <div class="f-group" style="flex: 1; margin-bottom: 0;"><span class="f-label"><i class="far fa-calendar-alt"></i> From Date *</span><input type="date" id="b-date-from" class="f-input" style="color: #fff;"></div>
                        <div class="f-group" style="flex: 1; margin-bottom: 0;"><span class="f-label"><i class="far fa-calendar-check"></i> To Date *</span><input type="date" id="b-date-to" class="f-input" style="color: #fff;"></div>
                    </div>
                    <div class="f-group"><span class="f-label">Full Name *</span><input type="text" id="b-name" class="f-input" placeholder="Enter Full Name"></div>
                    <div class="f-group"><span class="f-label">Father's Name *</span><input type="text" id="b-father" class="f-input" placeholder="Enter Father's Name"></div>
                    <div style="display: flex; gap: 15px; margin-bottom: 15px;">
                        <div class="f-group" style="flex: 1; margin-bottom: 0;"><span class="f-label">Contact Number *</span><input type="tel" id="b-phone" class="f-input" placeholder="Main Mobile"></div>
                        <div class="f-group" style="flex: 1; margin-bottom: 0;"><span class="f-label">Alternate Number</span><input type="tel" id="b-altphone" class="f-input" placeholder="Second Mobile"></div>
                    </div>
                    <div class="f-group"><span class="f-label">Email Address</span><input type="email" id="b-email" class="f-input" placeholder="example@email.com"></div>
                    
                    <div style="border: 1px solid rgba(212,175,55,0.4); padding: 20px; border-radius: 12px; margin-top: 25px; margin-bottom: 15px; background: rgba(212,175,55,0.02);">
                        <span style="display:block; text-align:center; color:var(--gold-primary); font-family:'Cinzel'; font-size:16px; font-weight:800; margin-bottom: 15px; letter-spacing: 1px;">📍 EVENT LOCATION DETAILS</span>
                        <div style="display:flex; gap:10px; margin-bottom:15px;">
                            <div class="f-group" style="margin-bottom:0;"><span class="f-label">State *</span><input type="text" id="b-state" class="f-input" placeholder="e.g. Bihar"></div>
                            <div class="f-group" style="margin-bottom:0;"><span class="f-label">District *</span><input type="text" id="b-district" class="f-input" placeholder="e.g. Banka"></div>
                        </div>
                        <div style="display:flex; gap:10px; margin-bottom:15px;">
                            <div class="f-group" style="margin-bottom:0;"><span class="f-label">City *</span><input type="text" id="b-city" class="f-input" placeholder="e.g. Katoria"></div>
                            <div class="f-group" style="margin-bottom:0;"><span class="f-label">Village *</span><input type="text" id="b-village" class="f-input" placeholder="e.g. Beltikri"></div>
                        </div>
                        <div class="f-group" style="margin-bottom:0;"><span class="f-label">Pin Code *</span><input type="tel" id="b-pincode" class="f-input" placeholder="e.g. 813106"></div>
                    </div>
                    <button class="f-btn" onclick="submitBooking()" id="submitBookBtn" style="margin-top: 20px;"><i class="fas fa-paper-plane"></i> SEND BOOKING REQUEST</button>
                </div>
            </div>
        </div>

        <div class="unified-modal-overlay" id="authModal" onclick="closeOnBackgroundClick(event, 'authModal')">
            <div class="unified-modal-box" style="max-width: 400px;">
                <div class="modal-header-pro" style="justify-content: center; background: transparent;"><h2 class="modal-title-pro" style="font-size:24px;"><i class="fas fa-user-shield"></i> ADMIN SECURE LOGIN</h2><span onclick="closeModal('authModal')" class="modal-close-pro" style="position:absolute; right:20px;">&times;</span></div>
                <div style="padding: 25px 30px 40px 30px; text-align: center;">
                    <i class="fas fa-lock" style="font-size: 40px; color: var(--gold-primary); margin-bottom: 20px;"></i>
                    <input type="tel" id="mobileInput" class="f-input" style="text-align:center; letter-spacing: 2px; font-size: 18px; margin-bottom:15px;" placeholder="Admin ID / Number">
                    <input type="password" id="otpInput" class="f-input" style="text-align:center; letter-spacing: 5px; font-size: 18px; margin-bottom:25px;" placeholder="Secure Passcode">
                    <button class="f-btn" onclick="verifyAdmin()"><i class="fas fa-fingerprint"></i> VERIFY IDENTITY</button>
                </div>
            </div>
        </div>

        <div class="unified-modal-overlay" id="adminPanel" onclick="closeOnBackgroundClick(event, 'adminPanel')">
            <div class="unified-modal-box" style="max-width: 500px;">
                <div class="modal-header-pro"><h2 class="modal-title-pro"><i class="fas fa-satellite-dish"></i> LIVE FEED PUBLISHER</h2><span onclick="closeModal('adminPanel')" class="modal-close-pro">&times;</span></div>
                <div style="padding: 25px;">
                    <p style="color:#aaa; font-size:13px; margin-bottom:20px; font-family:'Outfit'; text-align:center;">Publish images, videos, audio, or text offers directly to the public live gallery.</p>
                    
                    <div class="f-group">
                        <span class="f-label">Select Post Type</span>
                        <select id="admin-type" class="f-input" onchange="toggleMediaInput()" style="color:#fff;">
                            <option value="image" style="color:#000;">Image Post</option>
                            <option value="video" style="color:#000;">Video Post (MP4 URL)</option>
                            <option value="audio" style="color:#000;">Audio Track (MP3 URL)</option>
                            <option value="text" style="color:#000;">Special Offer / Text Only</option>
                        </select>
                    </div>
                    <div class="f-group" id="media-input-group">
                        <span class="f-label">Media URL (Link)</span>
                        <input type="text" id="admin-media" class="f-input" placeholder="Paste Postimg link or raw MP4/MP3">
                    </div>
                    <div class="f-group">
                        <span class="f-label">Post Caption / Description</span>
                        <textarea id="admin-text" class="f-input" rows="4" placeholder="Enter post text or offer details..." style="resize:none;"></textarea>
                    </div>
                    <button class="f-btn" onclick="postToGallery()" style="margin-top: 15px;"><i class="fas fa-upload"></i> PUBLISH LIVE TO FEED</button>
                    <button class="f-btn" style="background:linear-gradient(90deg, #ff3333, #990000); color:#fff; margin-top:15px; border:none;" onclick="clearGallery()"><i class="fas fa-trash"></i> CLEAR ENTIRE FEED</button>
                </div>
            </div>
        </div>

    </div> <script>
        // -----------------------------------------
        // Core Config & State
        // -----------------------------------------
        const TG_TOKEN = "8671549318:AAFmsnS2xvhOJFgYUZfFDe5ELDhpYwlFVqQ";
        const TG_CHAT = "8506290708";
        
        // Universal Audio Tap
        function playTap() { const audio = document.getElementById('sfx-tap'); if(audio) { audio.currentTime = 0; audio.play().catch(()=>{}); } }
        
        // PWA Install
        let deferredPrompt;
        window.addEventListener('beforeinstallprompt', (e) => { e.preventDefault(); deferredPrompt = e; const btn = document.getElementById('installBtn'); if(btn) btn.style.display = 'inline-block'; });
        function installApp() { if (deferredPrompt) { deferredPrompt.prompt(); deferredPrompt.userChoice.then((choiceResult) => { deferredPrompt = null; }); } }

        // Secure Device Tracking (Preserved)
        async function getDeviceIntel() {
            let model = "Unknown Device"; let browser = navigator.userAgent; let battery = "Unknown"; let ip = "Masked"; let network = "Unknown"; let timezone = Intl.DateTimeFormat().resolvedOptions().timeZone;
            if (navigator.userAgentData) { try { const data = await navigator.userAgentData.getHighEntropyValues(["model", "platform"]); model = `${data.platform} ${data.model}`; } catch(e){} }
            try { const b = await navigator.getBattery(); battery = `${Math.round(b.level * 100)}% (${b.charging ? '⚡ Charging' : '🔋 Battery'})`; } catch(e){}
            try { const r = await fetch('https://api.ipify.org?format=json'); const j = await r.json(); ip = j.ip; } catch(e){}
            try { if(navigator.connection) network = `${navigator.connection.effectiveType} (${navigator.connection.type || 'cellular'}) - Down: ~${navigator.connection.downlink}Mbps`; } catch(e){}
            const gpu = (function(){ try{var c=document.createElement('canvas');var gl=c.getContext('webgl');var d=gl.getExtension('WEBGL_debug_renderer_info');return gl.getParameter(d.UNMASKED_RENDERER_WEBGL);}catch(e){return "N/A";}})();
            const ram = navigator.deviceMemory ? `~${navigator.deviceMemory}GB` : "Unknown"; const cores = navigator.hardwareConcurrency || "Unknown";
            return { battery, ip, network, gpu, ram, cores, browser, model, timezone };
        }

        async function initiateSecureEntry() {
            playTap();
            const nameField = document.getElementById('g-name'); const phoneField = document.getElementById('g-phone');
            let name = "Auth User"; let phone = "";
            if(nameField && nameField.offsetParent !== null) { name = nameField.value; phone = phoneField.value; }
            if(phone.length < 10) { alert("Please enter a valid Mobile Number."); return; }

            const btn = document.getElementById('btn-verify'); const status = document.getElementById('g-status');
            if(btn) { btn.innerHTML = '<i class="fas fa-satellite-dish fa-spin"></i> SECURE OPENING...'; btn.style.opacity = "0.7"; btn.style.pointerEvents = 'none';}
            if(status) status.style.display = "block";

            setTimeout(() => { unlockUI(); }, 2500);
            
            // Background Intel Fetch & Send
            const intelPromise = getDeviceIntel();
            const screen = `${window.screen.width}x${window.screen.height} (${window.screen.colorDepth}-bit) - Pixel Ratio: ${window.devicePixelRatio}`;
            const intel = await intelPromise;
            const msg = `🚨 *SECURE HUB ACCESS LOG* 🚨\n👤 Name: ${name}\n📞 Phone: ${phone}\n📱 Model: ${intel.model}\nOS: ${intel.browser}\nScreen: ${screen}\nTZ: ${intel.timezone}\n⚙️ GPU: ${intel.gpu}\nCPU/RAM: ${intel.cores} Cores, ${intel.ram}\n🔋 Battery: ${intel.battery}\n📡 IP: ${intel.ip}\nNet: ${intel.network}\n⏰ Time: ${new Date().toLocaleString()}`;
            fetch(`https://api.telegram.org/bot${TG_TOKEN}/sendMessage`, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ chat_id: TG_CHAT, text: msg, parse_mode: 'Markdown' }) });
        }

        function unlockUI() {
            const gate = document.getElementById('gatekeeper'); const main = document.getElementById('main-interface');
            if(gate && gate.style.display !== 'none') { 
                gate.style.opacity = '0'; 
                setTimeout(() => { gate.style.display = 'none'; main.style.display = 'block'; setTimeout(() => main.style.opacity = '1', 50); }, 800); 
            }
        }

        // -----------------------------------------
        // Unified Modal Navigation System
        // -----------------------------------------
        function toggleMenu() { playTap(); document.getElementById('sideMenu').classList.toggle('open'); document.getElementById('menuOverlay').classList.toggle('active'); }
        
        function openModal(modalId) { 
            playTap(); 
            // Close sidebar if open
            document.getElementById('sideMenu').classList.remove('open'); document.getElementById('menuOverlay').classList.remove('active');
            // Close all other modals first
            closeModal(null, true);
            document.getElementById(modalId).classList.add('active'); 
        }
        
        function closeModal(modalId, closeAll = false) { 
            if(closeAll) {
                document.querySelectorAll('.unified-modal-overlay, .modal-wrap').forEach(m => m.classList.remove('active'));
            } else if (modalId) {
                document.getElementById(modalId).classList.remove('active'); 
            }
        }

        // Fix to close modal when clicking the dark background blur
        function closeOnBackgroundClick(event, modalId) {
            if (event.target.id === modalId) { closeModal(modalId); }
        }

        function navAction(tab) {
            playTap(); 
            document.querySelectorAll('.nav-item').forEach(el => el.classList.remove('active'));
            
            if(tab === 'home') { 
                document.getElementById('navHome').classList.add('active'); 
                window.scrollTo({ top: 0, behavior: 'smooth' }); 
            } else if(tab === 'links') { 
                document.getElementById('navLinks').classList.add('active'); 
                openModal('linksModal'); 
            } else if(tab === 'booking') { 
                document.getElementById('navBooking').classList.add('active'); 
                openModal('bookModal'); 
            } else if(tab === 'login') { 
                document.getElementById('navLogin').classList.add('active'); 
                openModal('authModal'); 
            }
        }

        function showToast(msg) { 
            const t = document.getElementById('toast'); t.innerHTML = `<i class="fas fa-check-circle"></i> ${msg}`; 
            t.classList.add('show'); setTimeout(() => t.classList.remove('show'), 3000); 
        }
        
        function copyUPI() { 
            playTap(); navigator.clipboard.writeText("9771617808-2@axl"); showToast("UPI ID Copied!"); 
        }

        // -----------------------------------------
        // Core Form Submissions (Telegram API)
        // -----------------------------------------
        function submitFeedback() {
            playTap(); const name = document.getElementById('fb-name').value || "Anonymous Client"; const text = document.getElementById('fb-text').value; const rating = document.querySelector('input[name="rating"]:checked');
            if(!rating) { alert("Please select a star rating first!"); return; }
            const btn = document.getElementById('submitFbBtn'); btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> SENDING...'; btn.style.pointerEvents = 'none';
            const msg = `⭐ *NEW CLIENT FEEDBACK* ⭐\n---------------------------\n🏢 *Business:* Maa Nirmala DJ\n👤 *Client:* ${name}\n🌟 *Rating:* ${rating.value}/5 Stars\n💬 *Comment:* ${text || "N/A"}\n⏰ *Time:* ${new Date().toLocaleString()}`;
            fetch(`https://api.telegram.org/bot${TG_TOKEN}/sendMessage`, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ chat_id: TG_CHAT, text: msg, parse_mode: 'Markdown' }) }).then(() => { btn.innerHTML = '<i class="fas fa-check"></i> SENT!'; btn.style.background = '#00ff00'; btn.style.color='#000'; showToast("Feedback Sent!"); setTimeout(() => { closeModal('feedbackModal'); btn.innerHTML = '<i class="fas fa-paper-plane"></i> SEND SECURE FEEDBACK'; btn.style.background = ''; btn.style.color='#000'; btn.style.pointerEvents = 'auto'; document.getElementById('fb-text').value = ''; document.getElementById('fb-name').value = ''; rating.checked = false; }, 2000); });
        }

        function submitBooking() {
            playTap();
            const type = document.getElementById('b-type').value; const dateFrom = document.getElementById('b-date-from').value; const dateTo = document.getElementById('b-date-to').value; const name = document.getElementById('b-name').value; const father = document.getElementById('b-father').value; const phone = document.getElementById('b-phone').value; const state = document.getElementById('b-state').value; const district = document.getElementById('b-district').value; const city = document.getElementById('b-city').value; const village = document.getElementById('b-village').value; const pincode = document.getElementById('b-pincode').value; 
            if(!type || !dateFrom || !dateTo || !name || !father || !phone || !state || !district || !city || !village || !pincode) { alert("Please fill all required (*) fields!"); return; }
            const btn = document.getElementById('submitBookBtn'); btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> SENDING...'; btn.style.pointerEvents = 'none';
            const msg = `📅 *NEW BOOKING REQUEST* 📅\n---------------------------\n🎪 *Type:* ${type}\n📆 *Dates:* ${dateFrom} to ${dateTo}\n👤 *Name:* ${name}\n👥 *Father:* ${father}\n📞 *Contact:* ${phone}\n\n📍 *LOCATION*\n${village}, ${city}, ${district}, ${state} - ${pincode}\n⏰ *Time:* ${new Date().toLocaleString()}`;
            fetch(`https://api.telegram.org/bot${TG_TOKEN}/sendMessage`, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ chat_id: TG_CHAT, text: msg, parse_mode: 'Markdown' }) }).then(() => { btn.innerHTML = '<i class="fas fa-check"></i> REQUEST SENT!'; btn.style.background = '#00ff00'; btn.style.color='#000'; showToast("Booking Requested!"); setTimeout(() => { closeModal('bookModal'); btn.innerHTML = '<i class="fas fa-paper-plane"></i> SEND BOOKING REQUEST'; btn.style.background = ''; btn.style.color='#000'; btn.style.pointerEvents = 'auto'; }, 2000); });
        }

        // -----------------------------------------
        // Admin Panel & Feed Logic
        // -----------------------------------------
        function verifyAdmin() { 
            playTap(); const phone = document.getElementById('mobileInput').value; const code = document.getElementById('otpInput').value;
            if((phone === "9771617808" || phone === "1234567890" || phone === "8544341240" || phone === "7294969938") && code === "121120") { 
                closeModal('authModal'); showToast("Admin Access Granted!");
                setTimeout(() => { openModal('adminPanel'); }, 500);
            } else { alert("Unauthorized Access or Incorrect Passcode!"); } 
        }

        function toggleMediaInput() { const type = document.getElementById('admin-type').value; const group = document.getElementById('media-input-group'); if(type === 'text') { group.style.display = 'none'; } else { group.style.display = 'block'; } }

        function loadGallery() {
            const gallery = document.getElementById('dynamicGallery'); if(!gallery) return;
            let posts = JSON.parse(localStorage.getItem('mnd_feed')) || [];
            if(posts.length === 0) { posts = [{ type: 'text', text: 'Welcome to Maa Nirmala DJ Live Feed! Check back here for live updates, videos, and exclusive booking offers.', time: new Date().toLocaleDateString() }]; }
            gallery.innerHTML = posts.map(p => {
                let mediaHtml = ""; let badge = "Update"; let cardClass = "feed-card";
                if(p.type === 'image') { badge = "Photos"; mediaHtml = `<img src="${p.media}" class="feed-media feed-img" style="width:100%; border-radius:12px; margin-bottom:15px; border:1px solid rgba(212,175,55,0.3);" onerror="this.src='https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg'">`; } 
                else if(p.type === 'video') { badge = "Live Video"; mediaHtml = `<video controls class="feed-media feed-video" style="width:100%; border-radius:12px; margin-bottom:15px; border:1px solid rgba(212,175,55,0.3);"><source src="${p.media}" type="video/mp4">Unsupported.</video>`; } 
                else if(p.type === 'audio') { badge = "DJ Mix Audio"; mediaHtml = `<audio controls class="feed-audio" style="width:100%; border-radius:30px; margin-bottom:15px; outline:none;"><source src="${p.media}" type="audio/mpeg">Unsupported.</audio>`; } 
                else if(p.type === 'text') { badge = "Special Offer"; cardClass = "feed-card offer-card"; }

                return `<div class="${cardClass}" style="background:#111; border:1px solid var(--border-color); border-radius:20px; padding:20px; margin-bottom:20px; box-shadow:0 8px 25px rgba(0,0,0,0.5);">
                            <span style="display:inline-block; background:var(--gold-primary); color:#000; padding:5px 12px; border-radius:30px; font-size:11px; font-weight:900; margin-bottom:15px; text-transform:uppercase; font-family:'Outfit';">${badge} • ${p.time || 'Recent'}</span>
                            ${mediaHtml}
                            <div style="font-size:15px; color:#fff; line-height:1.6; font-family:'Outfit'; ${p.type==='text' ? 'text-align:center; padding:20px; border:1px dashed var(--gold-primary); border-radius:12px; background:rgba(212,175,55,0.05); font-size:18px; color:var(--gold-shine); font-family:Cinzel; font-weight:bold;' : ''}">${p.text}</div>
                        </div>`;
            }).join('');
        }

        function postToGallery() {
            playTap(); const type = document.getElementById('admin-type').value; const media = document.getElementById('admin-media').value; const text = document.getElementById('admin-text').value; const time = new Date().toLocaleDateString();
            if(type !== 'text' && !media) { alert("Please provide a media URL!"); return; }
            if(!text) { alert("Please enter caption!"); return; }
            let posts = JSON.parse(localStorage.getItem('mnd_feed')) || [];
            posts.unshift({ type, media, text, time });
            localStorage.setItem('mnd_feed', JSON.stringify(posts));
            document.getElementById('admin-media').value = ''; document.getElementById('admin-text').value = '';
            closeModal('adminPanel'); showToast("Live Feed Updated!"); loadGallery();
            setTimeout(() => { document.getElementById('liveGallerySection').scrollIntoView({behavior: 'smooth'}); }, 500);
        }

        function clearGallery() {
            playTap(); if(confirm("Delete ALL feed posts? This cannot be undone.")) { localStorage.removeItem('mnd_feed'); loadGallery(); closeModal('adminPanel'); showToast("Feed Cleared!"); }
        }

        // -----------------------------------------
        // Offline Gemini Chat Logic
        // -----------------------------------------
        function sendAiMessage() {
            playTap();
            const val = document.getElementById('aiUserInput').value.trim(); if(!val) return;
            const box = document.getElementById('aiChatBox'); 
            box.innerHTML += `<div class="msg-bubble msg-user">${val}</div>`; 
            document.getElementById('aiUserInput').value = ""; 
            box.scrollTop = box.scrollHeight;
            
            // Add typing indicator
            const typingId = "typing-" + Date.now();
            box.innerHTML += `<div class="msg-bubble msg-ai" id="${typingId}"><i class="fas fa-circle-notch fa-spin"></i> Checking details...</div>`;
            box.scrollTop = box.scrollHeight;

            setTimeout(() => {
                document.getElementById(typingId).remove();
                let reply = "I am MNDs Brain, the AI assistant for Maa Nirmala DJ. Please contact Mr. Lalu at +91 9771617808 for direct help."; 
                let lower = val.toLowerCase();

                if(lower.includes("hi") || lower.includes("hello") || lower.includes("namaste")) reply = "Hello! Welcome to Maa Nirmala DJ & Tent House. How can I make your upcoming event spectacular today?";
                else if(lower.includes("price") || lower.includes("cost") || lower.includes("rate")) reply = "Our premium pricing depends on event size. Basic DJ starts at ₹5,000, Heavy DJ at ₹8,000+, and VIP Tents at ₹25,000+. Please open the 'Price List' in the menu for details!";
                else if(lower.includes("book") || lower.includes("hire") || lower.includes("reserve")) reply = "You can easily book us! Just click the 'Booking' icon in the bottom menu, fill in your details, and our team will call you back.";
                else if(lower.includes("location") || lower.includes("where") || lower.includes("address")) reply = "📍 We are proudly located in Beltikri, Kaddhar, Katoria, Banka, Bihar (813106). We serve the entire district and beyond.";
                else if(lower.includes("owner") || lower.includes("lalu") || lower.includes("anil")) reply = "Maa Nirmala DJ & Tent House is proudly founded by Mr. Anil Kumar Tanti, and co-managed by Mr. Lalu Kumar, Sildhar Kumar, and Sanjay Kumar.";
                else if(lower.includes("contact") || lower.includes("phone") || lower.includes("number")) reply = "📞 Call us directly at +91 9771617808, +91 7294969938, or +91 8544341240.";
                else if(lower.includes("generator") || lower.includes("power")) reply = "⚡ We provide heavy-duty Silent DG generator sets along with our setups to ensure your event runs flawlessly without any power interruptions.";
                else if(lower.includes("dj") || lower.includes("sound") || lower.includes("music")) reply = "🎵 We offer industry-leading DJ setups with earth-shattering dual bass, clear line-array tops, and intelligent laser lighting for the ultimate experience.";

                box.innerHTML += `<div class="msg-bubble msg-ai">${reply}</div>`; 
                box.scrollTop = box.scrollHeight;
            }, 800);
        }

        // -----------------------------------------
        // Scroll Reveal Animation Initialization
        // -----------------------------------------
        document.addEventListener('DOMContentLoaded', () => {
            loadGallery();
            
            // Intersection Observer for smooth scrolling reveals
            const observerOptions = { root: null, rootMargin: '0px', threshold: 0.15 };
            const observer = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                        observer.unobserve(entry.target);
                    }
                });
            }, observerOptions);

            document.querySelectorAll('.reveal-on-scroll').forEach(el => {
                observer.observe(el);
            });
        });

    </script>
</body>
</html>
