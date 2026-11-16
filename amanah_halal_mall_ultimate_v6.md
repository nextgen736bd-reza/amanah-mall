<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Amanah Halal Mall | আমানাহ - ১০০% হালাল ও সুন্নাহ মার্কেটপ্লেস</title>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;500;600;700&family=Amiri:ital,wght@0,400;0,700;1,400&family=Aref+Ruqaa:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --emerald-deep: #022c22;
            --emerald-primary: #064e3b;
            --emerald-mid: #047857;
            --emerald-light: #ecfdf5;
            --gold-rich: #b45309;
            --gold-bright: #d97706;
            --gold-foil: #f59e0b;
            --gold-cream: #fef3c7;
            --ivory-bg: #faf9f6;
            --surface: #ffffff;
            --text-dark: #0f172a;
            --text-muted: #475569;
            --border-subtle: #e2e8f0;
        }
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Hind Siliguri', sans-serif; }
        body { background-color: var(--ivory-bg); color: var(--text-dark); line-height: 1.5; overflow-x: hidden; }

        /* Top Bar */
        .top-bar {
            background: var(--emerald-deep); color: #fde68a; font-size: 0.83rem; padding: 6px 4%;
            display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 8px;
            border-bottom: 1px solid rgba(245, 158, 11, 0.35);
        }
        .bismillah-top { font-family: 'Amiri', serif; font-size: 1.12rem; color: #fbbf24; display: flex; align-items: center; gap: 12px; }
        .prayer-pill { background: rgba(255,255,255,0.1); border: 1px solid rgba(251, 191, 36, 0.4); padding: 2px 10px; border-radius: 14px; font-size: 0.78rem; color: #ecfdf5; cursor: pointer; }
        .top-bar-links { display: flex; gap: 12px; align-items: center; flex-wrap: wrap; }
        .top-bar-links button, .top-bar-links a { background: none; border: none; color: #ecfdf5; cursor: pointer; font-size: 0.82rem; text-decoration: none; }
        .top-bar-links button:hover, .top-bar-links a:hover { color: #fbbf24; text-decoration: underline; }
        .kafan-urgent-btn { background: #dc2626 !important; color: #ffffff !important; padding: 3px 10px !important; border-radius: 14px; font-weight: 700; }

        /* Live News Ticker */
        .live-ticker-strip { background: #022c22; border-bottom: 2px solid var(--gold-foil); color: #fffbeb; padding: 7px 4%; font-size: 0.86rem; display: flex; align-items: center; gap: 15px; overflow: hidden; }
        .ticker-badge { background: #dc2626; color: white; padding: 2px 8px; border-radius: 4px; font-weight: 700; font-size: 0.75rem; flex-shrink: 0; }
        .ticker-content marquee { font-weight: 500; color: #fde68a; }

        /* Header */
        header { background: var(--surface); position: sticky; top: 0; z-index: 150; box-shadow: 0 4px 16px rgba(2, 44, 34, 0.08); }
        .header-main { max-width: 1440px; margin: 0 auto; padding: 10px 4%; display: flex; align-items: center; justify-content: space-between; gap: 12px; flex-wrap: wrap; }
        
        .brand-logo { display: flex; align-items: center; gap: 10px; cursor: pointer; text-decoration: none; }
        .logo-emblem { width: 45px; height: 45px; flex-shrink: 0; }
        .logo-text-wrap { display: flex; flex-direction: column; }
        .logo-arabic { font-family: 'Aref Ruqaa', serif; font-size: 1.2rem; color: var(--gold-bright); font-weight: 700; }
        .logo-english { font-size: 1.2rem; font-weight: 700; color: var(--emerald-primary); display: flex; align-items: center; gap: 5px; }
        .logo-tag { background: var(--gold-cream); color: var(--gold-rich); font-size: 0.65rem; padding: 1px 6px; border-radius: 10px; border: 1px solid #fcd34d; font-weight: 700; }

        .search-box { flex: 1; min-width: 230px; max-width: 480px; display: flex; border: 2px solid var(--emerald-primary); border-radius: 10px; overflow: hidden; background: #f8fafc; }
        .search-box input { flex: 1; border: none; padding: 8px 12px; font-size: 0.93rem; background: transparent; outline: none; }
        .voice-btn { background: transparent; border: none; padding: 0 10px; cursor: pointer; font-size: 1.1rem; color: var(--emerald-primary); }
        .search-box button.search-submit { background: linear-gradient(135deg, var(--emerald-primary), var(--emerald-mid)); color: white; border: none; padding: 0 18px; cursor: pointer; font-weight: 600; }

        .header-actions { display: flex; align-items: center; gap: 8px; flex-wrap: wrap; }
        .icon-pill-btn { background: #f8fafc; color: var(--emerald-primary); border: 1px solid #cbd5e1; padding: 7px 11px; border-radius: 8px; font-weight: 600; cursor: pointer; font-size: 0.85rem; }
        .affiliate-btn { background: var(--gold-cream); color: #78350f; border: 1px solid var(--gold-foil); padding: 7px 12px; border-radius: 8px; font-weight: 700; cursor: pointer; font-size: 0.85rem; }
        .cart-btn { background: var(--emerald-primary); color: white; border: 1px solid var(--gold-foil); padding: 7px 14px; border-radius: 8px; font-weight: 600; cursor: pointer; display: flex; align-items: center; gap: 6px; }
        .cart-count { background: var(--gold-foil); color: var(--emerald-deep); font-size: 0.76rem; padding: 1px 6px; border-radius: 50%; font-weight: 800; }

        /* Daraz & Amazon Menubar */
        .daraz-menubar { background: linear-gradient(90deg, #064e3b 0%, #047857 50%, #064e3b 100%); border-bottom: 2px solid var(--gold-foil); padding: 0 4%; }
        .menubar-inner { max-width: 1440px; margin: 0 auto; display: flex; align-items: center; gap: 4px; overflow-x: auto; white-space: nowrap; }
        .menu-link { background: transparent; border: none; color: #ecfdf5; padding: 9px 14px; font-size: 0.88rem; font-weight: 600; cursor: pointer; }
        .menu-link:hover, .menu-link.active { background: rgba(2, 44, 34, 0.55); color: #fbbf24; border-bottom: 3px solid #fbbf24; }

        /* Big Amazon/Daraz Slider Hero */
        .big-slider-hero { max-width: 1440px; margin: 1.2rem auto; padding: 0 4%; display: flex; gap: 1.2rem; align-items: stretch; flex-wrap: wrap; }
        .main-slider-box { flex: 2; min-width: 300px; height: 350px; background: linear-gradient(135deg, #022c22, #064e3b); border-radius: 14px; position: relative; overflow: hidden; border: 2px solid var(--gold-foil); display: flex; align-items: center; padding: 2.5rem; color: white; box-shadow: 0 10px 25px rgba(0,0,0,0.15); }
        .slider-text h2 { font-size: 2.1rem; color: #fbbf24; margin-bottom: 8px; font-family: 'Amiri', serif; }
        .slider-text p { font-size: 1.05rem; color: #d1fae5; margin-bottom: 1.2rem; }
        .slider-btn { background: var(--gold-foil); color: var(--emerald-deep); border: none; padding: 10px 24px; border-radius: 8px; font-weight: 700; cursor: pointer; font-size: 1rem; }
        
        .side-promo-box { flex: 1; min-width: 250px; display: flex; flex-direction: column; gap: 1rem; }
        .promo-card { background: white; border: 1px solid var(--border-subtle); border-radius: 12px; padding: 1rem; display: flex; align-items: center; gap: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.05); }
        .promo-card img { width: 75px; height: 75px; object-fit: cover; border-radius: 8px; }

        /* Workspace */
        .store-workspace { max-width: 1440px; margin: 1.5rem auto 3rem; padding: 0 4%; display: flex; gap: 1.5rem; align-items: flex-start; }
        .catalog-content { flex: 1; min-width: 0; }
        
        .controls { background: var(--surface); border: 1px solid var(--border-subtle); border-radius: 10px; padding: 10px 15px; margin-bottom: 1.2rem; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px; }
        .result-info { font-size: 0.95rem; font-weight: 700; color: var(--emerald-primary); }

        /* Product Grid */
        .product-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(225px, 1fr)); gap: 1.2rem; }
        .p-card { background: var(--surface); border-radius: 12px; border: 1px solid var(--border-subtle); overflow: hidden; display: flex; flex-direction: column; justify-content: space-between; transition: 0.25s; position: relative; }
        .p-card:hover { transform: translateY(-4px); box-shadow: 0 12px 24px rgba(6, 78, 59, 0.12); border-color: var(--gold-foil); }
        .p-img-wrap { width: 100%; height: 180px; background: #f1f5f9; position: relative; overflow: hidden; cursor: pointer; }
        .p-img-wrap img { width: 100%; height: 100%; object-fit: cover; transition: 0.35s; }
        .p-card:hover .p-img-wrap img { transform: scale(1.06); }
        .halal-ribbon { position: absolute; top: 8px; left: 8px; background: var(--emerald-primary); color: #fef3c7; font-size: 0.7rem; font-weight: 600; padding: 2px 7px; border-radius: 5px; }
        .p-info { padding: 11px; }
        .p-title { font-size: 0.96rem; font-weight: 700; color: var(--text-dark); margin: 3px 0 5px; cursor: pointer; display: -webkit-box; -webkit-line-clamp: 2; -webkit-box-orient: vertical; overflow: hidden; }
        .p-price-row { display: flex; align-items: baseline; gap: 7px; margin-top: 5px; }
        .p-price { font-size: 1.15rem; font-weight: 700; color: var(--emerald-primary); }
        .p-old-price { font-size: 0.82rem; color: #94a3b8; text-decoration: line-through; }
        .p-actions { padding: 0 11px 11px; display: flex; gap: 7px; }
        .btn-cart { flex: 1; background: var(--emerald-light); color: var(--emerald-primary); border: 1px solid var(--emerald-primary); padding: 6px; border-radius: 7px; font-weight: 600; font-size: 0.83rem; cursor: pointer; }
        .btn-buy { flex: 1; background: var(--emerald-primary); color: white; border: none; padding: 6px; border-radius: 7px; font-weight: 600; font-size: 0.83rem; cursor: pointer; }

        /* Modals */
        .overlay { display: none; position: fixed; inset: 0; background: rgba(2, 44, 34, 0.72); z-index: 380; align-items: center; justify-content: center; padding: 1rem; }
        .modal-box { background: white; border-radius: 14px; width: 100%; max-width: 580px; max-height: 90vh; overflow-y: auto; padding: 1.4rem; position: relative; border-top: 4px solid var(--gold-foil); }
        .modal-close { position: absolute; top: 12px; right: 14px; background: #f1f5f9; border: none; width: 30px; height: 30px; border-radius: 50%; font-size: 1.2rem; cursor: pointer; }
        .modal-title { font-size: 1.25rem; font-weight: 700; color: var(--emerald-primary); margin-bottom: 0.9rem; padding-bottom: 7px; border-bottom: 1px solid var(--border-subtle); }
        .f-group { margin-bottom: 10px; }
        .f-group label { display: block; font-size: 0.86rem; font-weight: 600; margin-bottom: 3px; color: var(--emerald-deep); }
        .f-group input, .f-group select, .f-group textarea { width: 100%; padding: 8px 11px; border: 1px solid #cbd5e1; border-radius: 8px; font-size: 0.92rem; outline: none; }
        .btn-submit { width: 100%; background: linear-gradient(135deg, var(--emerald-primary), var(--emerald-mid)); color: white; border: none; padding: 11px; border-radius: 8px; font-size: 0.98rem; font-weight: 700; cursor: pointer; margin-top: 6px; }

        /* Cart Drawer */
        .cart-drawer { position: fixed; top: 0; right: -100%; width: 100%; max-width: 420px; height: 100vh; background: white; z-index: 420; box-shadow: -5px 0 25px rgba(0,0,0,0.18); transition: right 0.3s ease; display: flex; flex-direction: column; }
        .cart-drawer.open { right: 0; }
        .cart-header { padding: 1rem 1.2rem; background: var(--emerald-primary); color: #fef3c7; display: flex; justify-content: space-between; align-items: center; border-bottom: 2px solid var(--gold-foil); }
        .cart-items { flex: 1; overflow-y: auto; padding: 1rem; }
        .cart-footer { padding: 1rem 1.2rem; background: #f8fafc; border-top: 1px solid var(--border-subtle); }
        .toast { position: fixed; bottom: 24px; left: 50%; transform: translateX(-50%); background: var(--emerald-deep); color: #fef3c7; border: 1px solid var(--gold-foil); padding: 9px 20px; border-radius: 30px; font-size: 0.9rem; z-index: 500; display: none; }

        @media print {
            body * { visibility: hidden; }
            #printableMemoArea, #printableMemoArea * { visibility: visible; }
            #printableMemoArea { position: fixed; left: 0; top: 0; width: 100%; background: white; padding: 20px; }
        }

        footer { background: var(--emerald-deep); color: #d1fae5; padding: 2.5rem 4% 1.5rem; margin-top: 3rem; border-top: 4px solid var(--gold-foil); }
        .footer-grid { max-width: 1440px; margin: 0 auto; display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1.8rem; margin-bottom: 1.8rem; }
        .footer-col h3 { color: #fbbf24; margin-bottom: 8px; font-size: 1.1rem; }
        .footer-col p, .footer-col li { font-size: 0.88rem; color: #a7f3d0; margin-bottom: 5px; list-style: none; }
        .disclaimer-box { background: rgba(0,0,0,0.3); padding: 10px; border-radius: 8px; border: 1px solid rgba(251,191,36,0.3); font-size: 0.8rem; color: #fde68a; margin-top: 8px; }
        .footer-bottom { text-align: center; border-top: 1px solid rgba(251, 191, 36, 0.25); padding-top: 1rem; font-size: 0.86rem; color: #fde68a; }
    </style>
</head>
<body>

<!-- Top Bar -->
<div class="top-bar">
    <div class="bismillah-top">
        <span>بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ</span>
        <span class="prayer-pill" onclick="openPrayerModal()">🕌 নামাজের সময়সূচী (শরীয়তপুর/ঢাকা)</span>
    </div>
    <div class="top-bar-links">
        <button class="kafan-urgent-btn" onclick="alert('জরুরি কাফন সেবা হটলাইন: 01827978200 (২৪/৭ চালু)')">🚨 জরুরি কাফন সেবা</button>
        <button onclick="openCustomizeModal()" class="icon-pill-btn" style="background:rgba(255,255,255,0.1); color:#fef3c7; border:1px solid rgba(245,158,11,0.3);">⚙️ কাস্টমাইজ</button>
        <a href="https://wa.me/8801827978200" target="_blank">📞 +880 1827-978200</a>
        <button onclick="openAdminModal()">🔐 অ্যাডমিন (PIN: 7860)</button>
    </div>
</div>

<!-- Live News Ticker -->
<div class="live-ticker-strip">
    <div class="ticker-badge">🔴 লাইভ নোটিশ</div>
    <div class="ticker-content">
        <marquee behavior="scroll" direction="left" scrollamount="4">
            🌙 নামাজের সময় (শরীয়তপুর): ফজর ০৪:৫৮ AM | যোহর ১১:৫২ AM | আসর ০৩:৪০ PM | মাগরিব (ইফতার) ০৫:১৪ PM | ইশা ০৬:৩২ PM &nbsp;|&nbsp; 🌤️ আবহাওয়া: ২৪°C অনুকূল ও পরিষ্কার &nbsp;|&nbsp; ⚡ বিশেষ অফার: ১,৫০০ টাকার অর্ডারে ফ্রি হোম ডেলিভারি এবং প্রতি অর্ডারে ২০ টাকা এতিম তহবিলে সাদাকাহ!
        </marquee>
    </div>
</div>

<!-- Header -->
<header>
    <div class="header-main">
        <div class="brand-logo" onclick="resetHome()">
            <svg class="logo-emblem" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                <defs>
                    <linearGradient id="goldGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                        <stop offset="0%" stop-color="#fbbf24"/><stop offset="100%" stop-color="#92400e"/>
                    </linearGradient>
                    <linearGradient id="emGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                        <stop offset="0%" stop-color="#065f46"/><stop offset="100%" stop-color="#022c22"/>
                    </linearGradient>
                </defs>
                <polygon points="50,3 63,22 85,15 78,37 97,50 78,63 85,85 63,78 50,97 37,78 15,85 22,63 3,50 22,37 15,15 37,22" fill="url(#goldGrad)"/>
                <circle cx="50" cy="50" r="34" fill="url(#emGrad)" stroke="#fef3c7" stroke-width="2"/>
                <text x="50" y="57" text-anchor="middle" fill="#fef3c7" font-family="Amiri, serif" font-size="21" font-weight="bold">أمانة</text>
            </svg>
            <div class="logo-text-wrap">
                <span class="logo-arabic">أمانة • আমানাহ</span>
                <span class="logo-english">AMANAH <span class="logo-tag">v6 ULTIMATE</span></span>
            </div>
        </div>

        <div class="search-box">
            <input type="text" id="searchInput" placeholder="পণ্য খুঁজুন বা মাইকে বলুন..." onkeyup="applyFilters()">
            <button class="voice-btn" onclick="startVoiceSearch()">🎤</button>
            <button class="search-submit" onclick="applyFilters()">🔍</button>
        </div>

        <div class="header-actions">
            <button class="icon-pill-btn" onclick="openAffiliateModal()">💼 এফিলিয়েট</button>
            <button class="cart-btn" onclick="toggleCart()">🛒 কার্ট <span class="cart-count" id="headerCartCount">0</span></button>
        </div>
    </div>

    <!-- Menubar -->
    <nav class="daraz-menubar">
        <div class="menubar-inner">
            <button class="menu-link active" onclick="selectCategory('all', this)">🏠 হোম (৩০+ পণ্য)</button>
            <button class="menu-link" onclick="selectCategory('food', this)">🍯 সুন্নাহ ফুড ও মধু</button>
            <button class="menu-link" onclick="selectCategory('grocery', this)">🛒 মুদি বাজার ও মশলা</button>
            <button class="menu-link" onclick="selectCategory('organic', this)">🌿 অর্গানিক ও সুপারফুড</button>
            <button class="menu-link" onclick="filterHotDeals(this)">🔥 ডিসকাউন্ট অফার</button>
        </div>
    </nav>
</header>

<!-- Big Amazon/Daraz Style Banner Slider & Side Promos -->
<section class="big-slider-hero">
    <div class="main-slider-box" id="mainSliderBanner">
        <div class="slider-text">
            <span style="background:rgba(251,191,36,0.2); color:#fbbf24; padding:3px 10px; border-radius:12px; font-size:0.82rem; font-weight:700;">🌟 স্পেশাল হালাল কালেকশন</span>
            <h2>খাঁটি মধু ও আজওয়া খেজুর মেগা সেল</h2>
            <p>ল্যাব-টেস্টেড ১০০% বিশুদ্ধ সুন্নাহ খাবার সরাসরি কৃষকের খামার থেকে আপনার ঠিকানায়।</p>
            <button class="slider-btn" onclick="selectCategory('food')">এখনই কিনুন ➔</button>
        </div>
    </div>
    <div class="side-promo-box">
        <div class="promo-card">
            <img src="https://images.pexels.com/photos/1638280/pexels-photo-1638280.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Honey">
            <div>
                <h4 style="font-size:0.92rem; color:var(--emerald-primary);">চাকভাঙা সুন্দরবনের মধু</h4>
                <p style="font-size:0.8rem; color:#b45309; font-weight:700;">বিশেষ ছাড়: ৫৫১ ৳</p>
                <button onclick="quickBuy(1)" style="font-size:0.75rem; padding:2px 8px; background:#064e3b; color:white; border:none; border-radius:4px; cursor:pointer; margin-top:4px;">অর্ডার</button>
            </div>
        </div>
        <div class="promo-card">
            <img src="https://images.pexels.com/photos/3993245/pexels-photo-3993245.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Dates">
            <div>
                <h4 style="font-size:0.92rem; color:var(--emerald-primary);">মদিনার আজওয়া খেজুর</h4>
                <p style="font-size:0.8rem; color:#b45309; font-weight:700;">প্রিমিয়াম গ্রেড: ১,২৫০ ৳</p>
                <button onclick="quickBuy(2)" style="font-size:0.75rem; padding:2px 8px; background:#064e3b; color:white; border:none; border-radius:4px; cursor:pointer; margin-top:4px;">অর্ডার</button>
            </div>
        </div>
    </div>
</section>

<!-- Store Workspace -->
<div class="store-workspace">
    <aside style="width: 255px; flex-shrink: 0; background: white; border: 1px solid var(--border-subtle); border-radius: 12px; padding: 1rem; position: sticky; top: 115px;">
        <h3 style="font-size: 0.95rem; color: var(--emerald-primary); margin-bottom: 10px; border-bottom: 1px solid #e2e8f0; padding-bottom: 6px;">📂 বিভাগসমূহ</h3>
        <div style="display: flex; flex-direction: column; gap: 5px;">
            <button onclick="selectCategory('all', this)" style="background:none; border:none; text-align:left; padding:6px; cursor:pointer; font-weight:600; font-size:0.88rem; border-radius:6px; color:#064e3b;" class="active">সকল পণ্য (৩০+)</button>
            <button onclick="selectCategory('food', this)" style="background:none; border:none; text-align:left; padding:6px; cursor:pointer; font-size:0.88rem; border-radius:6px;">সুন্নাহ ফুড ও মধু</button>
            <button onclick="selectCategory('grocery', this)" style="background:none; border:none; text-align:left; padding:6px; cursor:pointer; font-size:0.88rem; border-radius:6px;">মুদি বাজার ও মশলা</button>
            <button onclick="selectCategory('organic', this)" style="background:none; border:none; text-align:left; padding:6px; cursor:pointer; font-size:0.88rem; border-radius:6px;">অর্গানিক ও সুপারফুড</button>
        </div>
        <div style="margin-top: 1.5rem; background: var(--gold-cream); padding: 10px; border-radius: 8px; border: 1px solid var(--gold-foil);">
            <h4 style="font-size: 0.85rem; color: #78350f; margin-bottom: 4px;">⚡ ফ্ল্যাশ সেল কাউন্টডাউন</h4>
            <div id="flashCountdown" style="font-size: 1.1rem; font-weight: 800; color: #b45309;">05:41:20</div>
        </div>
    </aside>

    <section class="catalog-content">
        <div class="controls">
            <div class="result-info" id="resultCount">মোট ৩০টি যাচাইকৃত পণ্য দেখানো হচ্ছে</div>
            <select id="sortSelect" onchange="applyFilters()" style="padding: 6px 10px; border: 1px solid #cbd5e1; border-radius: 8px; background: white; font-size: 0.85rem;">
                <option value="default">সাজান: জনপ্রিয়</option>
                <option value="low">দাম: কম থেকে বেশি</option>
                <option value="high">দাম: বেশি থেকে কম</option>
            </select>
        </div>
        <div class="product-grid" id="productGrid"></div>
    </section>
</div>

<!-- Cart Drawer -->
<div class="cart-drawer" id="cartDrawer">
    <div class="cart-header">
        <h3>🛒 আপনার শপিং কার্ট</h3>
        <button onclick="toggleCart()" style="background:none; border:none; color:#fef3c7; font-size:1.5rem; cursor:pointer;">&times;</button>
    </div>
    <div class="cart-items" id="cartItemsContainer"></div>
    <div class="cart-footer">
        <div style="display:flex; justify-content:space-between; font-weight:700; font-size:1.05rem; margin-bottom:10px;">
            <span>মোট মূল্য:</span>
            <span id="drawerSubTotal" style="color:var(--emerald-primary);">0 ৳</span>
        </div>
        <button class="btn-submit" onclick="openCheckout()">অর্ডার কনফার্ম করুন ➔</button>
    </div>
</div>

<!-- Checkout Modal -->
<div class="overlay" id="checkoutModal">
    <div class="modal-box">
        <button class="modal-close" onclick="closeModal('checkoutModal')">&times;</button>
        <h2 class="modal-title">অর্ডার কনফার্মেশন (ক্যাশ অন ডেলিভারি)</h2>
        <form onsubmit="confirmOrder(event)">
            <div id="checkoutSummary" style="background:#f8fafc; padding:10px; border-radius:8px; margin-bottom:10px; font-size:0.88rem;"></div>
            <div class="f-group"><label>গ্রাহকের নাম *</label><input type="text" id="cName" required></div>
            <div class="f-group"><label>মোবাইল নম্বর *</label><input type="tel" id="cPhone" required></div>
            <div class="f-group"><label>পূর্ণ ঠিকানা (জেলা সহ) *</label><textarea id="cAddress" rows="2" required></textarea></div>
            <button type="submit" class="btn-submit">✅ হোয়াটসঅ্যাপে অর্ডার পাঠান ও ক্যাশ মেমো দেখুন</button>
        </form>
    </div>
</div>

<!-- Printable Memo Modal -->
<div class="overlay" id="memoModal">
    <div class="modal-box">
        <button class="modal-close" onclick="closeModal('memoModal')">&times;</button>
        <div id="printableMemoArea"></div>
        <button onclick="window.print()" class="btn-submit" style="background:#022c22; color:#fbbf24; margin-top:12px;">🖨️ ক্যাশ মেমো প্রিন্ট করুন</button>
    </div>
</div>

<!-- Prayer Times Modal -->
<div class="overlay" id="prayerModal">
    <div class="modal-box">
        <button class="modal-close" onclick="closeModal('prayerModal')">&times;</button>
        <h2 class="modal-title">🕌 নামাজের সময়সূচী ও কিবলা দিক</h2>
        <p style="margin-bottom:8px; font-size:0.9rem;">🧭 কিবলা দিক: ২৭৭° পশ্চিম-উত্তর-পশ্চিম (শরীয়তপুর/ঢাকা)</p>
        <table style="width:100%; border-collapse:collapse; font-size:0.92rem;">
            <tr style="background:#ecfdf5;"><th style="padding:8px; border:1px solid #cbd5e1;">ওয়াক্ত</th><th style="padding:8px; border:1px solid #cbd5e1;">সময়</th></tr>
            <tr><td style="padding:8px; border:1px solid #cbd5e1;">ফজর (সেহরি শেষ)</td><td style="padding:8px; border:1px solid #cbd5e1;">০৪:৫৮ AM</td></tr>
            <tr><td style="padding:8px; border:1px solid #cbd5e1;">যোহর</td><td style="padding:8px; border:1px solid #cbd5e1;">১১:৫২ AM</td></tr>
            <tr><td style="padding:8px; border:1px solid #cbd5e1;">আসর</td><td style="padding:8px; border:1px solid #cbd5e1;">০৩:৪০ PM</td></tr>
            <tr><td style="padding:8px; border:1px solid #cbd5e1;">মাগরিব (ইফতার)</td><td style="padding:8px; border:1px solid #cbd5e1;">০৫:১৪ PM</td></tr>
            <tr><td style="padding:8px; border:1px solid #cbd5e1;">ইশা</td><td style="padding:8px; border:1px solid #cbd5e1;">০৬:৩২ PM</td></tr>
        </table>
    </div>
</div>

<!-- Affiliate Modal -->
<div class="overlay" id="affiliateModal">
    <div class="modal-box">
        <button class="modal-close" onclick="closeModal('affiliateModal')">&times;</button>
        <h2 class="modal-title">💼 এফিলিয়েট ও রেফারেল কমিশন সিস্টেম</h2>
        <p style="font-size:0.88rem; color:var(--text-muted); margin-bottom:10px;">আপনার লিংক শেয়ার করে ১০% কমিশন আয় করুন!</p>
        <div class="f-group"><label>আপনার নাম ও হোয়াটসঅ্যাপ নম্বর</label><input type="text" placeholder="নাম ও 01XXXXXXXXX"></div>
        <div class="f-group"><label>আপনার ইউনিক এফিলিয়েট লিংক</label><input type="text" readonly value="https://amanah-halal-mall.vercel.app/?ref=PARTNER" style="background:#f1f5f9; font-weight:700;"></div>
        <button onclick="alert('রেফারেল লিংক তৈরি হয়েছে!'); closeModal('affiliateModal');" class="btn-submit">লিংক কপি করুন</button>
    </div>
</div>

<!-- Customization Modal -->
<div class="overlay" id="customizeModal">
    <div class="modal-box">
        <button class="modal-close" onclick="closeModal('customizeModal')">&times;</button>
        <h2 class="modal-title">⚙️ প্রডাক্ট ও স্টোর কাস্টমাইজেশন</h2>
        <p style="font-size:0.86rem; color:var(--text-muted); margin-bottom:10px;">নতুন পণ্য বা মূল্য পরিবর্তন করতে নিচের ফর্মটি ব্যবহার করুন:</p>
        <div class="f-group"><label>নতুন পণ্যের নাম</label><input type="text" id="custProdName" placeholder="পণ্যের নাম ও পরিমাণ"></div>
        <div class="f-group"><label>মূল্য (টাকা)</label><input type="number" id="custProdPrice" placeholder="যেমন: ৫০০"></div>
        <div class="f-group"><label>ক্যাটাগরি</label><select id="custProdCat"><option value="food">সুন্নাহ ফুড</option><option value="grocery">মুদি বাজার</option><option value="organic">অর্গানিক</option></select></div>
        <button onclick="addNewProduct()" class="btn-submit">পণ্য যুক্ত করুন</button>
    </div>
</div>

<!-- Admin Modal -->
<div class="overlay" id="adminModal">
    <div class="modal-box" style="text-align:center;">
        <button class="modal-close" onclick="closeModal('adminModal')">&times;</button>
        <h2 class="modal-title">🔐 অ্যাডমিন ড্যাশবোর্ড</h2>
        <div id="adminPinBox">
            <p style="margin-bottom:10px;">অ্যাডমিন পিন দিন (ডিফল্ট: <strong>7860</strong>):</p>
            <input type="password" id="adminPin" placeholder="PIN" style="width:200px; text-align:center; padding:8px; border:1px solid #cbd5e1; border-radius:6px; margin-bottom:10px;"><br>
            <button onclick="unlockAdmin()" class="btn-buy" style="padding:8px 20px;">আনলক</button>
        </div>
        <div id="adminPanelContent" style="display:none; text-align:left;">
            <p style="color:var(--emerald-mid); font-weight:700;">✅ অ্যাডমিন আনলক সফল!</p>
            <div style="background:#f8fafc; padding:10px; border-radius:8px; margin-top:10px; font-size:0.88rem;">
                <p><strong>৫% প্ল্যাটফর্ম কমিশন ক্যালকুলেটর:</strong></p>
                <input type="number" id="calcAmt" placeholder="বিক্রয় মূল্য" oninput="calcComm()" style="margin-top:5px; padding:6px; width:100%;">
                <p style="margin-top:5px;">কমিশন: <span id="commOut">0</span> ৳ | ভেন্ডর পাবে: <span id="vendorOut">0</span> ৳</p>
            </div>
        </div>
    </div>
</div>

<div class="toast" id="toastMsg">সফলভাবে কার্টে যুক্ত হয়েছে!</div>

<footer>
    <div class="footer-grid">
        <div class="footer-col">
            <h3>أمانة • Amanah Halal Mall</h3>
            <p>বিশ্বস্ত ভেন্ডর ও সচেতন ক্রেতাদের আমানতদারিতার প্ল্যাটফর্ম। প্রতিটি পণ্য শরীয়াহ অডিটেড ও ল্যাব-টেস্টেড।</p>
            <div class="disclaimer-box">
                <strong>⚠️ ডিসক্লেমার ও কপিরাইট আইন:</strong> সাইটের সমস্ত কনটেন্ট এবং ভেন্ডর প্রডাক্টের শতভাগ হালাল গ্যারান্টি প্রদান করা হয়। কপিরাইট আইন ২০২৬ সংরক্ষিত।
            </div>
        </div>
        <div class="footer-col">
            <h3>যোগাযোগ ও সাপোর্ট</h3>
            <p>📍 হাব: শরীয়তপুর ও ঢাকা, বাংলাদেশ</p>
            <p>📞 হোয়াটসঅ্যাপ: +880 1827-978200</p>
            <p>✅ পেমেন্ট: ক্যাশ অন ডেলিভারি / বিকাশ</p>
        </div>
    </div>
    <div class="footer-bottom">
        جَزَاكَ اللَّهُ خَيْرًا • &copy; ২০২৬ Amanah Halal Marketplace. সর্বস্বত্ব সংরক্ষিত।
    </div>
</footer>

<script>
    const products = [
        {id: 1, cat: 'food', name: 'সুন্দরবনের খাঁটি চাকভাঙা মধু (৫০০ গ্রাম)', price: 550, oldPrice: 650, rating: '4.8', img: 'https://images.pexels.com/photos/1638280/pexels-photo-1638280.jpeg?auto=compress&cs=tinysrgb&w=400'},
        {id: 2, cat: 'food', name: 'মদিনার প্রিমিয়াম আজওয়া খেজুর (১ কেজি)', price: 1250, oldPrice: 1400, rating: '4.9', img: 'https://images.pexels.com/photos/3993245/pexels-photo-3993245.jpeg?auto=compress&cs=tinysrgb&w=400'},
        {id: 3, cat: 'food', name: 'কাঠের ঘানিভাঙা সরিষার তেল (১ লিটার)', price: 320, oldPrice: 360, rating: '5.0', img: 'https://images.pexels.com/photos/33783/olive-oil-salad-dressing-cooking-olive.jpg?auto=compress&cs=tinysrgb&w=400'},
        {id: 4, cat: 'food', name: 'পদ্মার চরের খাঁটি গাওয়া ঘি (৫০০ গ্রাম)', price: 750, oldPrice: 850, rating: '4.9', img: 'https://images.pexels.com/photos/4110256/pexels-photo-4110256.jpeg?auto=compress&cs=tinysrgb&w=400'},
        {id: 5, cat: 'food', name: 'মরিয়ম ভিআইপি প্রিমিয়াম খেজুর (১ কেজি)', price: 980, oldPrice: 1100, rating: '4.8', img: 'https://images.pexels.com/photos/3993245/pexels-photo-3993245.jpeg?auto=compress&cs=tinysrgb&w=400'},
        {id: 6, cat: 'grocery', name: 'অর্গানিক লাল চাল - ঢেঁকিছাঁটা (৫ কেজি)', price: 580, oldPrice: 650, rating: '5.0', img: 'https://images.pexels.com/photos/4110253/pexels-photo-4110253.jpeg?auto=compress&cs=tinysrgb&w=400'},
        {id: 7, cat: 'grocery', name: 'দেশি ছোট দানার খাঁটি মসুর ডাল (২ কেজি)', price: 310, oldPrice: 350, rating: '4.8', img: 'https://images.pexels.com/photos/4110255/pexels-photo-4110255.jpeg?auto=compress&cs=tinysrgb&w=400'},
        {id: 8, cat: 'grocery', name: 'হিমালয়ান পিংক সল্ট / সৈন্ধব লবণ (১ কেজি)', price: 220, oldPrice: 260, rating: '5.0', img: 'https://images.pexels.com/photos/4198018/pexels-photo-4198018.jpeg?auto=compress&cs=tinysrgb&w=400'},
        {id: 9, cat: 'organic', name: 'অর্গানিক চিয়া সিড - সুপারফুড (৫০০ গ্রাম)', price: 380, oldPrice: 450, rating: '4.9', img: 'https://images.pexels.com/photos/4110251/pexels-photo-4110251.jpeg?auto=compress&cs=tinysrgb&w=400'},
        {id: 10, cat: 'organic', name: 'দেশি কালোজিরা দানা - পরিষ্কার (৫০০ গ্রাম)', price: 240, oldPrice: 280, rating: '4.8', img: 'https://images.pexels.com/photos/4198023/pexels-photo-4198023.jpeg?auto=compress&cs=tinysrgb&w=400'}
    ];

    let cart = [];
    let currentCat = 'all';

    function renderProducts() {
        const grid = document.getElementById('productGrid');
        grid.innerHTML = '';
        let query = document.getElementById('searchInput').value.toLowerCase();
        let filtered = currentCat === 'all' ? products : products.filter(p => p.cat === currentCat);
        if(query) {
            filtered = filtered.filter(p => p.name.toLowerCase().includes(query));
        }
        
        document.getElementById('resultCount').innerText = `মোট ${filtered.length}টি যাচাইকৃত পণ্য দেখানো হচ্ছে`;

        filtered.forEach(p => {
            grid.innerHTML += `
                <div class="p-card">
                    <div class="p-img-wrap">
                        <span class="halal-ribbon">১০০% হালাল</span>
                        <img src="${p.img}" alt="${p.name}">
                    </div>
                    <div class="p-info">
                        <div class="p-title">${p.name}</div>
                        <div style="font-size:0.76rem; color:#d97706; font-weight:700;">★ ${p.rating} (ল্যাব-টেস্টেড)</div>
                        <div class="p-price-row">
                            <span class="p-price">${p.price} ৳</span>
                            <span class="p-old-price">${p.oldPrice} ৳</span>
                        </div>
                    </div>
                    <div class="p-actions">
                        <button class="btn-cart" onclick="addToCart(${p.id})">🛒 কার্ট</button>
                        <button class="btn-buy" onclick="quickBuy(${p.id})">অর্ডার</button>
                    </div>
                </div>
            `;
        });
    }

    function selectCategory(cat, btn) {
        currentCat = cat;
        if(btn) {
            document.querySelectorAll('.menubar-inner button').forEach(b => b.classList.remove('active'));
            btn.classList.add('active');
        }
        renderProducts();
    }

    function applyFilters() { renderProducts(); }

    function startVoiceSearch() {
        if (!('webkitSpeechRecognition' in window) && !('SpeechRecognition' in window)) {
            alert('আপনার ব্রাউজার ভয়েস সার্চ সাপোর্ট করে না।');
            return;
        }
        const recognition = new (window.SpeechRecognition || window.webkitSpeechRecognition)();
        recognition.lang = 'bn-BD';
        recognition.onstart = () => showToast('🎤 বলুন কী খুঁজতে চান...');
        recognition.onresult = (event) => {
            document.getElementById('searchInput').value = event.results[0][0].transcript;
            renderProducts();
        };
        recognition.start();
    }

    function addToCart(id) {
        let item = products.find(p => p.id === id);
        let found = cart.find(c => c.id === id);
        if(found) found.qty++;
        else cart.push({...item, qty: 1});
        updateCartDrawer();
        showToast("কার্টে সফলভাবে যুক্ত হয়েছে!");
    }

    function updateCartDrawer() {
        let container = document.getElementById('cartItemsContainer');
        container.innerHTML = '';
        let subtotal = 0, count = 0;
        cart.forEach(c => {
            subtotal += c.price * c.qty;
            count += c.qty;
            container.innerHTML += `
                <div style="display:flex; justify-content:space-between; margin-bottom:8px; border-bottom:1px solid #e2e8f0; padding-bottom:6px; font-size:0.88rem;">
                    <div>${c.name} (${c.qty}টি)</div>
                    <div style="font-weight:700; color:#064e3b;">${c.price * c.qty} ৳</div>
                </div>
            `;
        });
        document.getElementById('headerCartCount').innerText = count;
        document.getElementById('drawerSubTotal').innerText = subtotal + ' ৳';
    }

    function toggleCart() { document.getElementById('cartDrawer').classList.toggle('open'); }
    function showToast(msg) {
        let t = document.getElementById('toastMsg');
        t.innerText = msg; t.style.display = 'block';
        setTimeout(() => t.style.display = 'none', 2500);
    }

    function openPrayerModal() { document.getElementById('prayerModal').style.display = 'flex'; }
    function openAffiliateModal() { document.getElementById('affiliateModal').style.display = 'flex'; }
    function openCustomizeModal() { document.getElementById('customizeModal').style.display = 'flex'; }
    function openAdminModal() { document.getElementById('adminModal').style.display = 'flex'; }
    function closeModal(id) { document.getElementById(id).style.display = 'none'; }

    function openCheckout() {
        if(cart.length === 0) { alert('আপনার কার্ট খালি!'); return; }
        let summary = cart.map(c => `• ${c.name} - ${c.qty}টি (${c.price*c.qty} ৳)`).join('<br>');
        document.getElementById('checkoutSummary').innerHTML = summary;
        document.getElementById('checkoutModal').style.display = 'flex';
        toggleCart();
    }

    function addNewProduct() {
        let name = document.getElementById('custProdName').value;
        let price = document.getElementById('custProdPrice').value;
        let cat = document.getElementById('custProdCat').value;
        if(!name || !price) { alert('সব তথ্য পূরণ করুন!'); return; }
        products.unshift({id: Date.now(), cat, name, price: Number(price), oldPrice: Number(price)+100, rating: '5.0', img: 'https://images.pexels.com/photos/1638280/pexels-photo-1638280.jpeg?auto=compress&cs=tinysrgb&w=400'});
        renderProducts();
        closeModal('customizeModal');
        showToast('নতুন পণ্য সফলভাবে যুক্ত হয়েছে!');
    }

    function unlockAdmin() {
        if(document.getElementById('adminPin').value === '7860') {
            document.getElementById('adminPinBox').style.display = 'none';
            document.getElementById('adminPanelContent').style.display = 'block';
        } else { alert('ভুল পিন!'); }
    }

    function calcComm() {
        let amt = Number(document.getElementById('calcAmt').value);
        document.getElementById('commOut').innerText = (amt * 0.05).toFixed(1);
        document.getElementById('vendorOut').innerText = (amt * 0.95).toFixed(1);
    }

    function confirmOrder(e) {
        e.preventDefault();
        let name = document.getElementById('cName').value;
        let phone = document.getElementById('cPhone').value;
        let addr = document.getElementById('cAddress').value;
        let subtotal = cart.reduce((sum, i) => sum + (i.price * i.qty), 0);
        let total = subtotal + 120;

        let memoHtml = `
            <div style="font-family: 'Hind Siliguri', sans-serif; padding:15px; color:#0f172a;">
                <h2 style="text-align:center; color:#064e3b; margin-bottom:4px;">أمانة • Amanah Halal Mall</h2>
                <p style="text-align:center; font-size:0.85rem; color:#475569;">অফিশিয়াল ক্যাশ মেমো ও পার্সেল স্লিপ</p>
                <hr style="margin:10px 0; border:1px dashed #cbd5e1;">
                <p><strong>গ্রাহক:</strong> ${name} | <strong>মোবাইল:</strong> ${phone}</p>
                <p><strong>ঠিকানা:</strong> ${addr}</p>
                <hr style="margin:10px 0; border:1px dashed #cbd5e1;">
                <table style="width:100%; border-collapse:collapse; font-size:0.88rem;">
                    <tr style="background:#f1f5f9;"><th style="text-align:left; padding:5px;">পণ্য</th><th>পরিমাণ</th><th>দাম</th></tr>
                    ${cart.map(c => `<tr><td style="padding:5px;">${c.name}</td><td style="text-align:center;">${c.qty}</td><td style="text-align:right;">${c.price*c.qty} ৳</td></tr>`).join('')}
                </table>
                <hr style="margin:10px 0; border:1px dashed #cbd5e1;">
                <p style="text-align:right;"><strong>ডেলিভারি চার্জ:</strong> ১২০ ৳</p>
                <p style="text-align:right; font-size:1.1rem; color:#064e3b;"><strong>সর্বমোট:</strong> ${total} ৳</p>
                <p style="text-align:center; margin-top:15px; font-size:0.8rem; color:#047857;">জَزَاكَ اللَّهُ خَيْرًا • কেনাকাটার জন্য শুকরিয়া!</p>
            </div>
        `;
        document.getElementById('printableMemoArea').innerHTML = memoHtml;
        closeModal('checkoutModal');
        document.getElementById('memoModal').style.display = 'flex';

        let msg = `আসসালামু আলাইকুম! নতুন অর্ডার:%0Aগ্রাহক: ${name}%0Aমোবাইল: ${phone}%0Aঠিকানা: ${addr}%0Aমোট: ${total} ৳ (COD)`;
        window.open(`https://wa.me/8801827978200?text=${msg}`, '_blank');
    }

    function quickBuy(id) { addToCart(id); openCheckout(); }
    function filterHotDeals(btn) {
        document.querySelectorAll('.menubar-inner button').forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        let grid = document.getElementById('productGrid');
        grid.innerHTML = '';
        products.slice(0, 4).forEach(p => {
            grid.innerHTML += `<div class="p-card"><div class="p-img-wrap"><img src="${p.img}"></div><div class="p-info"><div class="p-title">${p.name}</div><div class="p-price">${p.price} ৳</div></div><div class="p-actions"><button class="btn-buy" onclick="quickBuy(${p.id})">অর্ডার</button></div></div>`;
        });
    }

    renderProducts();
</script>
</body>
</html>