<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LUXESTATE UZBEKISTAN — Premium Ko'chmas Mulk Agentligi</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Playfair+Display:ital,wght@0,600;0,700;1,400&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        gold: {
                            400: '#facc15',
                            500: '#eab308',
                            600: '#ca8a04',
                            700: '#a16207',
                        },
                        darknavy: '#0b1120',
                    },
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                        serif: ['Playfair Display', 'serif'],
                    }
                }
            }
        }
    </script>
    <style>
        .glass-header {
            background: rgba(11, 17, 32, 0.85);
            backdrop-filter: blur(12px);
        }
        .hero-gradient {
            background: linear-gradient(180deg, rgba(11, 17, 32, 0.4) 0%, rgba(11, 17, 32, 0.95) 100%);
        }
        .property-card {
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .property-card:hover {
            transform: translateY(-8px);
        }
        /* Modal transitions */
        .modal {
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }
        .modal-active {
            opacity: 1 !important;
            visibility: visible !important;
            pointer-events: auto !important;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800 dark:bg-darknavy dark:text-gray-100 font-sans transition-colors duration-300">

    <!-- Top Bar -->
    <div class="bg-gray-900 text-gray-300 text-xs py-2 px-6 border-b border-gray-800">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <div class="flex items-center space-x-6">
                <span><i class="fa-solid font-bold text-amber-500 fa-phone mr-2"></i>+998 (71) 200-88-88</span>
                <span><i class="fa-solid font-bold text-amber-500 fa-location-dot mr-2"></i>Toshkent sh., Amir Temur shoh ko'chasi, 108</span>
                <span class="hidden md:inline"><i class="fa-solid font-bold text-amber-500 fa-clock mr-2"></i>Dush-Shan: 09:00 - 20:00</span>
            </div>
            <div class="flex items-center space-x-4">
                <div class="flex items-center space-x-2">
                    <button onclick="setLanguage('uz')" class="hover:text-amber-400 font-bold px-1 rounded">UZ</button>|
                    <button onclick="setLanguage('ru')" class="hover:text-amber-400 font-bold px-1 rounded">RU</button>|
                    <button onclick="setLanguage('en')" class="hover:text-amber-400 font-bold px-1 rounded">EN</button>
                </div>
                <button onclick="toggleDarkMode()" class="p-1 rounded-full hover:bg-gray-800 text-amber-400">
                    <i class="fa-solid fa-moon text-sm" id="darkIcon"></i>
                </button>
            </div>
        </div>
    </div>

    <!-- Navigation Header -->
    <header class="sticky top-0 z-40 glass-header border-b border-gray-800 text-white shadow-xl">
        <div class="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">
            <a href="#" class="flex items-center space-x-3">
                <div class="w-10 h-10 bg-gradient-to-br from-amber-400 to-amber-600 rounded-lg flex items-center justify-center text-gray-900 font-bold text-xl shadow-lg shadow-amber-500/20">
                    L
                </div>
                <div>
                    <span class="font-serif text-2xl font-bold tracking-wider text-amber-400 uppercase">LUXESTATE</span>
                    <span class="block text-[9px] tracking-widest text-gray-400 uppercase">Uzbekistan Real Estate</span>
                </div>
            </a>

            <nav class="hidden md:flex items-center space-x-8 text-sm font-medium">
                <a href="#properties" class="hover:text-amber-400 transition" data-i18n="nav-properties">Katalog</a>
                <a href="#about" class="hover:text-amber-400 transition" data-i18n="nav-about">Biz haqimizda</a>
                <a href="#calculator" class="hover:text-amber-400 transition" data-i18n="nav-calc">Kalkulyator</a>
                <a href="#contact" class="hover:text-amber-400 transition" data-i18n="nav-contact">Aloqa</a>
            </nav>

            <div class="flex items-center space-x-4">
                <button onclick="toggleFavoritesModal()" class="relative p-2 text-gray-300 hover:text-amber-400 transition">
                    <i class="fa-solid fa-heart text-xl"></i>
                    <span id="favCount" class="absolute -top-1 -right-1 bg-amber-500 text-gray-900 text-xs font-bold rounded-full w-5 h-5 flex items-center justify-center">0</span>
                </button>
                <a href="#contact" class="hidden sm:inline-block bg-gradient-to-r from-amber-500 to-amber-600 hover:from-amber-600 hover:to-amber-700 text-gray-950 font-bold px-5 py-2.5 rounded-lg shadow-lg shadow-amber-500/20 transition transform hover:scale-105" data-i18n="nav-btn">
                    Konsultatsiya olish
                </a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative min-h-[85vh] flex items-center justify-center bg-cover bg-center text-white" style="background-image: url('https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?auto=format&fit=crop&w=1920&q=80');">
        <div class="absolute inset-0 hero-gradient"></div>
        <div class="relative max-w-5xl mx-auto px-6 text-center py-20">
            <span class="inline-block px-4 py-1.5 bg-amber-500/20 border border-amber-500/40 rounded-full text-amber-400 text-xs font-semibold uppercase tracking-widest mb-6">
                Eksklyuziv Uylar va Villalar
            </span>
            <h1 class="font-serif text-4xl sm:text-6xl font-extrabold tracking-tight mb-6 leading-tight" data-i18n="hero-title">
                O'zbekistonning Eng Muazzam va Zamonaviy Ko'chmas Mulklari
            </h1>
            <p class="text-gray-300 text-lg sm:text-xl max-w-3xl mx-auto mb-10 font-light" data-i18n="hero-subtitle">
                Toshkent, Samarqand va Buxoroning premium lyuks uylari, penthauslar hamda kottejlari to'plami.
            </p>

            <!-- Search Filter Bar -->
            <div class="bg-gray-900/90 backdrop-blur-md p-4 sm:p-6 rounded-2xl border border-gray-700 shadow-2xl max-w-4xl mx-auto">
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4">
                    <div>
                        <label class="block text-xs font-semibold text-gray-400 mb-1 text-left" data-i18n="filter-city">Shahar / Hudud</label>
                        <select id="filterCity" onchange="applyFilters()" class="w-full bg-gray-800 border border-gray-700 rounded-lg px-3 py-2.5 text-sm text-white focus:outline-none focus:border-amber-500">
                            <option value="all">Barcha Hududlar</option>
                            <option value="Toshkent">Toshkent Sh.</option>
                            <option value="Toshkent Vil.">Toshkent Vil.</option>
                            <option value="Samarqand">Samarqand</option>
                            <option value="Buxoro">Buxoro</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-xs font-semibold text-gray-400 mb-1 text-left" data-i18n="filter-type">Mulk Turi</label>
                        <select id="filterType" onchange="applyFilters()" class="w-full bg-gray-800 border border-gray-700 rounded-lg px-3 py-2.5 text-sm text-white focus:outline-none focus:border-amber-500">
                            <option value="all">Barchasi</option>
                            <option value="Penthaus">Penthaus</option>
                            <option value="Kottej">Kottej / Villa</option>
                            <option value="Kvartira">Apartament</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-xs font-semibold text-gray-400 mb-1 text-left" data-i18n="filter-price">Maksimal Narx</label>
                        <select id="filterPrice" onchange="applyFilters()" class="w-full bg-gray-800 border border-gray-700 rounded-lg px-3 py-2.5 text-sm text-white focus:outline-none focus:border-amber-500">
                            <option value="all">Cheklovsiz</option>
                            <option value="250000">$250,000 gacha</option>
                            <option value="500000">$500,000 gacha</option>
                            <option value="1000000">$1,000,000 gacha</option>
                        </select>
                    </div>
                    <div class="flex items-end">
                        <button onclick="applyFilters()" class="w-full bg-amber-500 hover:bg-amber-600 text-gray-950 font-bold py-2.5 px-4 rounded-lg transition duration-200 flex items-center justify-center space-x-2">
                            <i class="fa-solid fa-magnifying-glass"></i>
                            <span data-i18n="filter-search">Qidirish</span>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Main Catalog Section -->
    <section id="properties" class="py-20 px-6 max-w-7xl mx-auto">
        <div class="flex flex-col md:flex-row md:items-end justify-between mb-12">
            <div>
                <span class="text-amber-500 font-bold uppercase tracking-widest text-xs" data-i18n="section-subtitle">Tanlangan Uylar</span>
                <h2 class="font-serif text-3xl sm:text-4xl font-bold mt-2" data-i18n="section-title">Eksklyuziv Uylar Katalogi (10 ta Loyiha)</h2>
            </div>
            <p class="text-gray-500 dark:text-gray-400 text-sm max-w-md mt-4 md:mt-0" data-i18n="section-desc">
                Har bir obyekt me'moriy va muhandislik nuqtai nazaridan sinchiklab tekshirilgan va yuqori darajada bezatilgan.
            </p>
        </div>

        <!-- Property Grid -->
        <div id="propertyGrid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- JavaScript will populate 10 property cards here dynamically -->
        </div>
    </section>

    <!-- Calculator Section -->
    <section id="calculator" class="py-20 bg-gray-100 dark:bg-gray-900 border-y border-gray-200 dark:border-gray-800">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div>
                    <span class="text-amber-500 font-bold uppercase tracking-widest text-xs" data-i18n="calc-sub">Moliyaviy Kalkulyator</span>
                    <h2 class="font-serif text-3xl sm:text-4xl font-bold mt-2 mb-6" data-i18n="calc-title">Ipoteka va Bo'lib To'lash Hisoblagichi</h2>
                    <p class="text-gray-600 dark:text-gray-400 mb-8 leading-relaxed" data-i18n="calc-desc">
                        O'zbekistondagi eng yetakchi banklar va qurilish kompaniyalarining eksklyuziv bo'lib to'lash shartlari asosida oylik to'lovingizni aniq hisoblang.
                    </p>
                    
                    <div class="space-y-6 bg-white dark:bg-darknavy p-6 rounded-2xl border border-gray-200 dark:border-gray-800 shadow-xl">
                        <div>
                            <div class="flex justify-between text-sm font-semibold mb-2">
                                <span data-i18n="calc-total">Uy Narxi ($)</span>
                                <span id="priceVal" class="text-amber-500">$300,000</span>
                            </div>
                            <input type="range" id="inputPrice" min="50000" max="1500000" step="10000" value="300000" oninput="calculateMortgage()" class="w-full accent-amber-500">
                        </div>

                        <div>
                            <div class="flex justify-between text-sm font-semibold mb-2">
                                <span data-i18n="calc-down">Boshlang'ich To'lov ($)</span>
                                <span id="downVal" class="text-amber-500">$90,000 (30%)</span>
                            </div>
                            <input type="range" id="inputDown" min="10" max="70" step="5" value="30" oninput="calculateMortgage()" class="w-full accent-amber-500">
                        </div>

                        <div>
                            <div class="flex justify-between text-sm font-semibold mb-2">
                                <span data-i18n="calc-years">Muddati (Yil)</span>
                                <span id="yearVal" class="text-amber-500">10 Yil</span>
                            </div>
                            <input type="range" id="inputYear" min="1" max="20" step="1" value="10" oninput="calculateMortgage()" class="w-full accent-amber-500">
                        </div>
                    </div>
                </div>

                <!-- Calculator Output Box -->
                <div class="bg-gradient-to-br from-gray-900 to-darknavy p-8 rounded-3xl border border-amber-500/30 shadow-2xl text-white flex flex-col justify-between min-h-[400px]">
                    <div>
                        <h3 class="text-xl font-bold text-amber-400 mb-6 pb-4 border-b border-gray-800" data-i18n="calc-summary">Hisob-kitob Natijasi</h3>
                        <div class="space-y-6">
                            <div>
                                <span class="text-xs text-gray-400 uppercase tracking-wider" data-i18n="calc-monthly-label">Oylik To'lov Taxminan:</span>
                                <div class="text-4xl font-extrabold text-amber-400 mt-1" id="monthlyResult">$2,450 / oy</div>
                            </div>

                            <div class="grid grid-cols-2 gap-4 pt-4 border-t border-gray-800">
                                <div>
                                    <span class="text-xs text-gray-400" data-i18n="calc-loan-amount">Kredit Summasi:</span>
                                    <div class="text-lg font-bold" id="loanAmountResult">$210,000</div>
                                </div>
                                <div>
                                    <span class="text-xs text-gray-400" data-i18n="calc-interest-rate">Yillik Stavka:</span>
                                    <div class="text-lg font-bold text-green-400">7.5% (Eksklyuziv)</div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="mt-8">
                        <a href="#contact" class="block w-full text-center bg-amber-500 hover:bg-amber-600 text-gray-950 font-bold py-3 rounded-xl transition shadow-lg shadow-amber-500/20" data-i18n="calc-apply">
                            Shartnomani Rasmiylashtirish
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Company Stats / About Section -->
    <section id="about" class="py-20 max-w-7xl mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
            <div>
                <span class="text-amber-500 font-bold uppercase tracking-widest text-xs" data-i18n="about-sub">Nega Aynan LUXESTATE?</span>
                <h2 class="font-serif text-3xl sm:text-4xl font-bold mt-2 mb-6" data-i18n="about-title">O'zbekistondagi Ishonchli Premium Hamkoringiz</h2>
                <p class="text-gray-600 dark:text-gray-300 leading-relaxed mb-6" data-i18n="about-text">
                    Biz premium toifasidagi ko'chmas mulk bozorida 10 yildan ortiq tajribaga egamiz. Har bir mijozimizga shaxsiy va maxfiy yondashuv hamda yuridik kafolat taqdim etamiz.
                </p>
                
                <div class="grid grid-cols-2 gap-6 mt-8">
                    <div class="border-l-4 border-amber-500 pl-4">
                        <div class="text-3xl font-extrabold text-amber-500">150+</div>
                        <div class="text-xs text-gray-500 dark:text-gray-400 mt-1" data-i18n="stat-1">Sotilgan Lyuks Obyektlar</div>
                    </div>
                    <div class="border-l-4 border-amber-500 pl-4">
                        <div class="text-3xl font-extrabold text-amber-500">100%</div>
                        <div class="text-xs text-gray-500 dark:text-gray-400 mt-1" data-i18n="stat-2">Yuridik Toza Bitimlar</div>
                    </div>
                </div>
            </div>
            <div class="relative">
                <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1000&q=80" alt="LuxEstate Office" class="rounded-3xl shadow-2xl border border-gray-700">
                <div class="absolute -bottom-6 -left-6 bg-amber-500 text-gray-950 p-6 rounded-2xl shadow-xl hidden sm:block">
                    <i class="fa-solid fa-award text-3xl mb-2"></i>
                    <div class="font-bold text-sm">Best Luxury Agency 2025/2026</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-gray-900 text-white">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <div>
                    <span class="text-amber-500 font-bold uppercase tracking-widest text-xs" data-i18n="contact-sub">Bog'lanish</span>
                    <h2 class="font-serif text-3xl sm:text-4xl font-bold mt-2 mb-6" data-i18n="contact-title">Ekspertlarimiz Bilan Bog'laning</h2>
                    <p class="text-gray-400 mb-8" data-i18n="contact-desc">
                        Savollaringiz bormi yoki uy ko'rishni rejalashtirmoqchimisiz? Formani to'ldiring va biz siz bilan 15 daqiqa ichida bog'lanamiz.
                    </p>

                    <div class="space-y-4 text-sm">
                        <div class="flex items-center space-x-4">
                            <div class="w-12 h-12 bg-amber-500/10 rounded-xl flex items-center justify-center text-amber-500 text-lg">
                                <i class="fa-solid fa-phone"></i>
                            </div>
                            <div>
                                <div class="text-gray-400 text-xs">Telefon</div>
                                <div class="font-bold text-base">+998 (71) 200-88-88</div>
                            </div>
                        </div>

                        <div class="flex items-center space-x-4">
                            <div class="w-12 h-12 bg-amber-500/10 rounded-xl flex items-center justify-center text-amber-500 text-lg">
                                <i class="fa-brands fa-telegram"></i>
                            </div>
                            <div>
                                <div class="text-gray-400 text-xs">Telegram Bot & Operator</div>
                                <div class="font-bold text-base">@LuxEstateUz_bot</div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Contact Form -->
                <div class="bg-gray-800 p-8 rounded-3xl border border-gray-700">
                    <form onsubmit="handleFormSubmit(event)" class="space-y-4">
                        <div>
                            <label class="block text-xs font-medium text-gray-300 mb-1" data-i18n="form-name">Ismingiz</label>
                            <input type="text" required placeholder="Jahongir Alimov" class="w-full bg-gray-900 border border-gray-700 rounded-lg px-4 py-3 text-sm text-white focus:outline-none focus:border-amber-500">
                        </div>
                        <div>
                            <label class="block text-xs font-medium text-gray-300 mb-1" data-i18n="form-phone">Telefon Raqamingiz</label>
                            <input type="tel" required placeholder="+998 90 123 45 67" class="w-full bg-gray-900 border border-gray-700 rounded-lg px-4 py-3 text-sm text-white focus:outline-none focus:border-amber-500">
                        </div>
                        <div>
                            <label class="block text-xs font-medium text-gray-300 mb-1" data-i18n="form-message">Qiziqtirgan Mulk yoki Xabar</label>
                            <textarea rows="4" placeholder="Tashkent City penthausi bo'yicha ko'rish vaqti..." class="w-full bg-gray-900 border border-gray-700 rounded-lg px-4 py-3 text-sm text-white focus:outline-none focus:border-amber-500"></textarea>
                        </div>
                        <button type="submit" class="w-full bg-amber-500 hover:bg-amber-600 text-gray-950 font-bold py-3.5 rounded-xl transition shadow-lg shadow-amber-500/20" data-i18n="form-submit">
                            Arizani Yuborish
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-darknavy text-gray-400 text-xs py-8 border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-6 flex flex-col sm:flex-row justify-between items-center space-y-4 sm:space-y-0">
            <div>
                © 2026 LUXESTATE Uzbekistan. Barcha huquqlar himoyalangan.
            </div>
            <div class="flex space-x-6 text-sm">
                <a href="#" class="hover:text-amber-400"><i class="fa-brands fa-instagram"></i></a>
                <a href="#" class="hover:text-amber-400"><i class="fa-brands fa-telegram"></i></a>
                <a href="#" class="hover:text-amber-400"><i class="fa-brands fa-facebook"></i></a>
            </div>
        </div>
    </footer>

    <!-- PROPERTY DETAIL MODAL -->
    <div id="detailModal" class="modal opacity-0 invisible pointer-events-none fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/80 backdrop-blur-md">
        <div class="bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-100 rounded-3xl max-w-4xl w-full max-h-[90vh] overflow-y-auto border border-gray-700 shadow-2xl relative">
            <button onclick="closeDetailModal()" class="absolute top-4 right-4 z-10 w-10 h-10 bg-gray-800 text-white rounded-full flex items-center justify-center hover:bg-amber-500 hover:text-gray-950 transition">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>
            <div id="modalContent"></div>
        </div>
    </div>

    <!-- FAVORITES MODAL -->
    <div id="favModal" class="modal opacity-0 invisible pointer-events-none fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/80 backdrop-blur-md">
        <div class="bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-100 rounded-3xl max-w-2xl w-full p-6 border border-gray-700 shadow-2xl relative">
            <div class="flex justify-between items-center mb-6 pb-4 border-b border-gray-800">
                <h3 class="font-serif text-2xl font-bold" data-i18n="fav-title">Tanlangan Uylaringiz</h3>
                <button onclick="toggleFavoritesModal()" class="text-gray-400 hover:text-white">
                    <i class="fa-solid fa-xmark text-xl"></i>
                </button>
            </div>
            <div id="favList" class="space-y-4 max-h-[60vh] overflow-y-auto">
                <!-- Favorites items dynamic rendering -->
            </div>
        </div>
    </div>

    <!-- JavaScript Application Logic -->
    <script>
        // 10 Real Real-Estate Properties in Uzbekistan
        const properties = [
            {
                id: 1,
                title: "Tashkent City Gardens — Sky Penthouse",
                city: "Toshkent",
                type: "Penthaus",
                price: 750000,
                area: "340 m²",
                rooms: 5,
                floor: "24/25",
                img: "https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?auto=format&fit=crop&w=800&q=80",
                badge: "Tashkent City",
                desc: "Toshkent марказидаги энг ҳашамдор пентхаус. Ташент Сити паркига 360-даражали манзара, шахсий терраса, смарт-ҳум тизими ва панорама ойналар.",
                specs: ["Panoramic Windows", "Private Elevator", "Smart Home", "24/7 Security", "Underground Parking"]
            },
            {
                id: 2,
                title: "Mirabad Avenue — High-End Duplex",
                city: "Toshkent",
                type: "Kvartira",
                price: 480000,
                area: "220 m²",
                rooms: 4,
                floor: "8/9",
                img: "https://images.unsplash.com/photo-1600607687939-ce8a6c25118c?auto=format&fit=crop&w=800&q=80",
                badge: "Mirabad",
                desc: "Мирабод шоҳ кўчасида жойлашган 2 қаватли шинам дуплекс. Италия мебеллари ва немис сантехникаси билан тўлиқ жиҳозланган.",
                specs: ["Italian Design", "Central Heating", "Private Courtyard", "Concierge"]
            },
            {
                id: 3,
                title: "Qibray Luxury Residence — Eco Villa",
                city: "Toshkent Vil.",
                type: "Kottej",
                price: 890000,
                area: "650 m²",
                rooms: 7,
                floor: "3 Qavat",
                img: "https://images.unsplash.com/photo-1613977257363-707ba9348227?auto=format&fit=crop&w=800&q=80",
                badge: "Qibray / Chirchiq",
                desc: "Қибрайнинг солим табиати қўйнида жойлашган экологик вилла. Очиқ бассейн, фин саунаси ва 12 сотих кўкаламзорлаштирилган ҳовли.",
                specs: ["Swimming Pool", "Sauna", "12 Sotikh Yard", "BBQ Zone", "Solar Panels"]
            },
            {
                id: 4,
                title: "Chorvoq Lake View House",
                city: "Toshkent Vil.",
                type: "Kottej",
                price: 340000,
                area: "280 m²",
                rooms: 4,
                floor: "2 Qavat",
                img: "https://images.unsplash.com/photo-1512917774080-9991f1c4c750?auto=format&fit=crop&w=800&q=80",
                badge: "Chorvoq",
                desc: "Чорвоқ сув омбори ва тоғларга тўғридан-тўғри манзараси бўлган премиум дала ҳовли. Иситиладиган бассейн ва терраса.",
                specs: ["Mountain & Lake View", "Heated Pool", "Terrace", "Fireplace"]
            },
            {
                id: 5,
                title: "Samarkand Regency Estate",
                city: "Samarqand",
                type: "Kottej",
                price: 520000,
                area: "420 m²",
                rooms: 6,
                floor: "2 Qavat",
                img: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=800&q=80",
                badge: "Samarqand City",
                desc: "Самарқанднинг тарихий марказига яқин ҳудуддаги миллий ва замонавий меъморчилик уйғунлигидаги ҳашамдор резиденция.",
                specs: ["National Design", "Landscape Garden", "Marble Floors", "CCTV"]
            },
            {
                id: 6,
                title: "Bukhara Heritage Villa",
                city: "Buxoro",
                type: "Kottej",
                price: 290000,
                area: "310 m²",
                rooms: 5,
                floor: "2 Qavat",
                img: "https://images.unsplash.com/photo-1580587771525-78b9dba3b914?auto=format&fit=crop&w=800&q=80",
                badge: "Buxoro Central",
                desc: "Бухоро шаҳрининг элит ҳудудидаги классик услубдаги шинам вилла. Шоҳона безаклар ва миллий ҳовли тизими.",
                specs: ["Inner Courtyard", "Wine Cellar", "High Ceilings", "Smart Security"]
            },
            {
                id: 7,
                title: "Yashnabod Central Park Apartment",
                city: "Toshkent",
                type: "Kvartira",
                price: 210000,
                area: "145 m²",
                rooms: 3,
                floor: "11/16",
                img: "https://images.unsplash.com/photo-1567496898669-ee935f5f647a?auto=format&fit=crop&w=800&q=80",
                badge: "Yashnabod",
                desc: "Яшнабод туманидаги энг ривожланган турар-жой мажмуасида жойлашган шинам ва замонавий хонадон.",
                specs: ["Park View", "Children Playground", "Fitness Center", "High Speed Elevator"]
            },
            {
                id: 8,
                title: "Highland Resort Chimgan Villa",
                city: "Toshkent Vil.",
                type: "Kottej",
                price: 410000,
                area: "350 m²",
                rooms: 5,
                floor: "2 Qavat",
                img: "https://images.unsplash.com/photo-1542314831-068cd1dbfeeb?auto=format&fit=crop&w=800&q=80",
                badge: "Chimgon",
                desc: "Чимён тоғ тизмалари бағрида жойлашган шале услубидаги муҳташам тоғ вилласи. Қишки ва ёзги дам олиш учун идеал.",
                specs: ["Chalet Style", "Fireplace", "Ski Storage", "Sauna & Jacuzzi"]
            },
            {
                id: 9,
                title: "Infinity Tower Sky Apartment",
                city: "Toshkent",
                type: "Penthaus",
                price: 630000,
                area: "290 m²",
                rooms: 4,
                floor: "18/20",
                img: "https://images.unsplash.com/photo-1502672260266-1c1ef2d93688?auto=format&fit=crop&w=800&q=80",
                badge: "Yakkasaroy",
                desc: "Яккасарой туманидаги энг баланд ва замонавий муҳташам осмонўпар бинода жойлашган премиум апартамент.",
                specs: ["Infinity Pool Access", "Private Spa", "Smart Entry", "Valet Parking"]
            },
            {
                id: 10,
                title: "Beshagach Royal Residence",
                city: "Toshkent",
                type: "Kvartira",
                price: 360000,
                area: "180 m²",
                rooms: 4,
                floor: "6/12",
                img: "https://images.unsplash.com/photo-1600566753376-12c8ab7fb75b?auto=format&fit=crop&w=800&q=80",
                badge: "Chilanzar / Beshagach",
                desc: "Бешёғоч майдони ва Magic City боғи яқинида жойлашган премиум классдаги янги хонадон.",
                specs: ["Near Magic City", "Underground Parking", "Luxury Lobby", "Concierge Service"]
            }
        ];

        let favorites = [];

        // Dynamic Render Properties
        function renderProperties(list) {
            const grid = document.getElementById('propertyGrid');
            grid.innerHTML = '';

            list.forEach(item => {
                const isFav = favorites.includes(item.id);
                const card = document.createElement('div');
                card.className = "property-card bg-white dark:bg-gray-900 rounded-3xl overflow-hidden border border-gray-200 dark:border-gray-800 shadow-xl flex flex-col justify-between";
                card.innerHTML = `
                    <div>
                        <div class="relative h-64 overflow-hidden">
                            <img src="${item.img}" alt="${item.title}" class="w-full h-full object-cover transition-transform duration-500 hover:scale-110">
                            <span class="absolute top-4 left-4 bg-amber-500 text-gray-950 text-xs font-bold px-3 py-1.5 rounded-full shadow-lg">
                                ${item.badge}
                            </span>
                            <button onclick="toggleFav(${item.id})" class="absolute top-4 right-4 w-10 h-10 bg-gray-900/70 backdrop-blur-md rounded-full flex items-center justify-center text-amber-400 hover:bg-amber-500 hover:text-gray-950 transition">
                                <i class="${isFav ? 'fa-solid' : 'fa-regular'} fa-heart text-lg"></i>
                            </button>
                        </div>
                        <div class="p-6">
                            <div class="flex justify-between items-start mb-2">
                                <span class="text-xs text-amber-500 font-bold uppercase tracking-wider">${item.city} • ${item.type}</span>
                                <span class="text-xl font-extrabold text-amber-500">$${item.price.toLocaleString()}</span>
                            </div>
                            <h3 class="font-serif text-xl font-bold mb-3 leading-snug hover:text-amber-400 transition cursor-pointer" onclick="openDetailModal(${item.id})">${item.title}</h3>
                            <p class="text-gray-500 dark:text-gray-400 text-xs line-clamp-2 mb-4">${item.desc}</p>
                            
                            <div class="grid grid-cols-3 gap-2 py-3 border-y border-gray-100 dark:border-gray-800 text-xs text-gray-600 dark:text-gray-300">
                                <div class="flex items-center space-x-1.5">
                                    <i class="fa-solid fa-ruler-combined text-amber-500"></i>
                                    <span>${item.area}</span>
                                </div>
                                <div class="flex items-center space-x-1.5">
                                    <i class="fa-solid fa-bed text-amber-500"></i>
                                    <span>${item.rooms} Xona</span>
                                </div>
                                <div class="flex items-center space-x-1.5">
                                    <i class="fa-solid fa-building text-amber-500"></i>
                                    <span>${item.floor}</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="p-6 pt-0 flex space-x-3">
                        <button onclick="openDetailModal(${item.id})" class="flex-1 bg-gray-100 hover:bg-amber-500 hover:text-gray-950 dark:bg-gray-800 dark:hover:bg-amber-500 text-xs font-bold py-3 rounded-xl transition flex items-center justify-center space-x-2">
                            <i class="fa-solid fa-vr-cardboard"></i>
                            <span>3D Virtual Tur</span>
                        </button>
                        <a href="#contact" class="px-4 bg-amber-500 hover:bg-amber-600 text-gray-950 font-bold py-3 rounded-xl transition flex items-center justify-center">
                            <i class="fa-solid fa-paper-plane"></i>
                        </a>
                    </div>
                `;
                grid.appendChild(card);
            });
        }

        // Apply Filters
        function applyFilters() {
            const city = document.getElementById('filterCity').value;
            const type = document.getElementById('filterType').value;
            const price = document.getElementById('filterPrice').value;

            let filtered = properties.filter(item => {
                let matchCity = city === 'all' || item.city === city;
                let matchType = type === 'all' || item.type === type;
                let matchPrice = price === 'all' || item.price <= parseInt(price);
                return matchCity && matchType && matchPrice;
            });

            renderProperties(filtered);
        }

        // Calculator Logic
        function calculateMortgage() {
            const price = parseInt(document.getElementById('inputPrice').value);
            const downPercent = parseInt(document.getElementById('inputDown').value);
            const years = parseInt(document.getElementById('inputYear').value);

            const downAmount = price * (downPercent / 100);
            const loanAmount = price - downAmount;
            
            // Fixed interest rate for simulation (7.5% per annum)
            const annualRate = 0.075;
            const monthlyRate = annualRate / 12;
            const totalMonths = years * 12;

            const monthlyPayment = (loanAmount * monthlyRate * Math.pow(1 + monthlyRate, totalMonths)) / (Math.pow(1 + monthlyRate, totalMonths) - 1);

            document.getElementById('priceVal').innerText = `$${price.toLocaleString()}`;
            document.getElementById('downVal').innerText = `$${downAmount.toLocaleString()} (${downPercent}%)`;
            document.getElementById('yearVal').innerText = `${years} Yil`;

            document.getElementById('monthlyResult').innerText = `$${Math.round(monthlyPayment).toLocaleString()} / oy`;
            document.getElementById('loanAmountResult').innerText = `$${loanAmount.toLocaleString()}`;
        }

        // Favorites Logic
        function toggleFav(id) {
            if (favorites.includes(id)) {
                favorites = favorites.filter(item => item !== id);
            } else {
                favorites.push(id);
            }
            document.getElementById('favCount').innerText = favorites.length;
            applyFilters();
            renderFavorites();
        }

        function toggleFavoritesModal() {
            const modal = document.getElementById('favModal');
            modal.classList.toggle('modal-active');
            renderFavorites();
        }

        function renderFavorites() {
            const container = document.getElementById('favList');
            container.innerHTML = '';
            
            if (favorites.length === 0) {
                container.innerHTML = '<p class="text-gray-400 text-center py-6">Siz hali hech qanday uyni tanlamadingiz.</p>';
                return;
            }

            const favItems = properties.filter(p => favorites.includes(p.id));
            favItems.forEach(item => {
                const div = document.createElement('div');
                div.className = 'flex items-center justify-between bg-gray-800 p-3 rounded-xl border border-gray-700';
                div.innerHTML = `
                    <div class="flex items-center space-x-3">
                        <img src="${item.img}" class="w-16 h-12 object-cover rounded-lg">
                        <div>
                            <div class="font-bold text-sm text-white">${item.title}</div>
                            <div class="text-xs text-amber-500 font-bold">$${item.price.toLocaleString()}</div>
                        </div>
                    </div>
                    <button onclick="toggleFav(${item.id})" class="text-red-400 hover:text-red-500 p-2">
                        <i class="fa-solid fa-trash"></i>
                    </button>
                `;
                container.appendChild(div);
            });
        }

        // Property Detail / 3D Virtual Tour Modal
        function openDetailModal(id) {
            const item = properties.find(p => p.id === id);
            if (!item) return;

            const modalContent = document.getElementById('modalContent');
            modalContent.innerHTML = `
                <div class="relative h-80 sm:h-96">
                    <img src="${item.img}" class="w-full h-full object-cover">
                    <div class="absolute inset-0 bg-gradient-to-t from-gray-900 via-transparent to-transparent"></div>
                    <div class="absolute bottom-6 left-6 right-6 flex justify-between items-end">
                        <div>
                            <span class="bg-amber-500 text-gray-950 text-xs font-bold px-3 py-1 rounded-full uppercase">${item.badge}</span>
                            <h2 class="font-serif text-2xl sm:text-3xl font-bold text-white mt-2">${item.title}</h2>
                        </div>
                        <div class="text-2xl font-extrabold text-amber-400">$${item.price.toLocaleString()}</div>
                    </div>
                </div>
                <div class="p-6 sm:p-8 space-y-6">
                    <div>
                        <h4 class="text-xs uppercase font-bold text-amber-500 tracking-wider mb-2">3D Virtual Tur Interaktiv Ko'rinishi</h4>
                        <div class="relative w-full h-64 bg-gray-950 rounded-2xl flex items-center justify-center border border-gray-800 overflow-hidden group cursor-pointer">
                            <img src="${item.img}" class="w-full h-full object-cover opacity-40 group-hover:scale-105 transition duration-500">
                            <div class="absolute flex flex-col items-center">
                                <div class="w-16 h-16 bg-amber-500 rounded-full flex items-center justify-center text-gray-950 text-2xl shadow-xl shadow-amber-500/30 group-hover:scale-110 transition">
                                    <i class="fa-solid fa-play ml-1"></i>
                                </div>
                                <span class="text-xs text-white font-bold mt-3 tracking-widest uppercase">360° Virtual Sayohatni Boshlash</span>
                            </div>
                        </div>
                    </div>

                    <div>
                        <h4 class="text-sm font-bold text-gray-400 mb-2">Tavsif</h4>
                        <p class="text-sm leading-relaxed text-gray-300">${item.desc}</p>
                    </div>

                    <div>
                        <h4 class="text-sm font-bold text-gray-400 mb-3">Qulayliklar va Imkoniyatlar</h4>
                        <div class="flex flex-wrap gap-2">
                            ${item.specs.map(s => `<span class="bg-gray-800 border border-gray-700 text-amber-400 text-xs px-3 py-1.5 rounded-lg font-medium"><i class="fa-solid fa-check text-xs mr-1.5"></i>${s}</span>`).join('')}
                        </div>
                    </div>

                    <div class="pt-4 border-t border-gray-800 flex justify-end space-x-4">
                        <button onclick="closeDetailModal()" class="px-6 py-2.5 rounded-xl border border-gray-700 text-sm font-bold hover:bg-gray-800 transition">Yopish</button>
                        <a href="#contact" onclick="closeDetailModal()" class="px-6 py-2.5 rounded-xl bg-amber-500 hover:bg-amber-600 text-gray-950 text-sm font-bold transition shadow-lg shadow-amber-500/20">Ko'rishga Yozilish</a>
                    </div>
                </div>
            `;

            document.getElementById('detailModal').classList.add('modal-active');
        }

        function closeDetailModal() {
            document.getElementById('detailModal').classList.remove('modal-active');
        }

        // Dark Mode Toggle
        function toggleDarkMode() {
            document.documentElement.classList.toggle('dark');
            const icon = document.getElementById('darkIcon');
            if (document.documentElement.classList.contains('dark')) {
                icon.className = 'fa-solid fa-sun text-amber-400';
            } else {
                icon.className = 'fa-solid fa-moon text-amber-400';
            }
        }

        // Form Submission
        function handleFormSubmit(e) {
            e.preventDefault();
            alert("Arizangiz muvaffaqiyatli qabul qilindi! Tezz orada agentimiz siz bilan bog'lanadi.");
            e.target.reset();
        }

        // Multilingual Basic Dictionary
        const i18n = {
            uz: {
                "nav-properties": "Katalog",
                "nav-about": "Biz haqimizda",
                "nav-calc": "Kalkulyator",
                "nav-contact": "Aloqa",
                "nav-btn": "Konsultatsiya olish",
                "hero-title": "O'zbekistonning Eng Muazzam va Zamonaviy Ko'chmas Mulklari",
                "hero-subtitle": "Toshkent, Samarqand va Buxoroning premium lyuks uylari, penthauslar hamda kottejlari to'plami.",
                "filter-city": "Shahar / Hudud",
                "filter-type": "Mulk Turi",
                "filter-price": "Maksimal Narx",
                "filter-search": "Qidirish",
                "section-subtitle": "Tanlangan Uylar",
                "section-title": "Eksklyuziv Uylar Katalogi (10 ta Loyiha)",
                "section-desc": "Har bir obyekt me'moriy va muhandislik nuqtai nazaridan sinchiklab tekshirilgan va yuqori darajada bezatilgan.",
                "calc-sub": "Moliyaviy Kalkulyator",
                "calc-title": "Ipoteka va Bo'lib To'lash Hisoblagichi",
                "calc-total": "Uy Narxi ($)",
                "calc-down": "Boshlang'ich To'lov ($)",
                "calc-years": "Muddati (Yil)",
                "calc-summary": "Hisob-kitob Natijasi",
                "calc-monthly-label": "Oylik To'lov Taxminan:",
                "calc-loan-amount": "Kredit Summasi:",
                "calc-interest-rate": "Yillik Stavka:",
                "calc-apply": "Shartnomani Rasmiylashtirish",
                "about-sub": "Nega Aynan LUXESTATE?",
                "about-title": "O'zbekistondagi Ishonchli Premium Hamkoringiz",
                "about-text": "Biz premium toifasidagi ko'chmas mulk bozorida 10 yildan ortiq tajribaga egamiz. Har bir mijozimizga shaxsiy va maxfiy yondashuv hamda yuridik kafolat taqdim etamiz.",
                "stat-1": "Sotilgan Lyuks Obyektlar",
                "stat-2": "Yuridik Toza Bitimlar",
                "contact-sub": "Bog'lanish",
                "contact-title": "Ekspertlarimiz Bilan Bog'laning",
                "contact-desc": "Savollaringiz bormi yoki uy ko'rishni rejalashtirmoqchimisiz? Formani to'ldiring va biz siz bilan 15 daqiqa ichida bog'lanamiz.",
                "form-name": "Ismingiz",
                "form-phone": "Telefon Raqamingiz",
                "form-message": "Qiziqtirgan Mulk yoki Xabar",
                "form-submit": "Arizani Yuborish",
                "fav-title": "Tanlangan Uylaringiz"
            },
            ru: {
                "nav-properties": "Каталог",
                "nav-about": "О нас",
                "nav-calc": "Калькулятор",
                "nav-contact": "Контакты",
                "nav-btn": "Консультация",
                "hero-title": "Самая элитная недвижимость Узбекистана",
                "hero-subtitle": "Коллекция премиальных пентхаусов, вилл и элитных квартир в Ташкенте, Самарканде и Бухаре.",
                "filter-city": "Город / Регион",
                "filter-type": "Тип недвижимости",
                "filter-price": "Макс. цена",
                "filter-search": "Поиск",
                "section-subtitle": "Избранные объекты",
                "section-title": "Каталог элитной недвижимости (10 проектов)",
                "section-desc": "Каждый объект тщательно проверен с точки зрения архитектуры и юридической чистоты.",
                "calc-sub": "Финансовый калькулятор",
                "calc-title": "Калькулятор ипотеки и рассрочки",
                "calc-total": "Стоимость объекта ($)",
                "calc-down": "Первоначальный взнос ($)",
                "calc-years": "Срок (Лет)",
                "calc-summary": "Результат расчета",
                "calc-monthly-label": "Ежемесячный платеж:",
                "calc-loan-amount": "Сумма кредита:",
                "calc-interest-rate": "Годовая ставка:",
                "calc-apply": "Оформить заявку",
                "about-sub": "Почему LUXESTATE?",
                "about-title": "Ваш надежный премиум-партнер в Узбекистане",
                "about-text": "Более 10 лет опыта на рынке элитной недвижимости. Полная конфиденциальность и юридическая гарантия.",
                "stat-1": "Проданных премиум-объектов",
                "stat-2": "Чистые сделки",
                "contact-sub": "Контакты",
                "contact-title": "Свяжитесь с экспертами",
                "contact-desc": "Есть вопросы? Заполните форму, и мы свяжемся с вами в течение 15 минут.",
                "form-name": "Ваше имя",
                "form-phone": "Ваш телефон",
                "form-message": "Сообщение",
                "form-submit": "Отправить заявку",
                "fav-title": "Избранные объекты"
            },
            en: {
                "nav-properties": "Catalog",
                "nav-about": "About Us",
                "nav-calc": "Calculator",
                "nav-contact": "Contact",
                "nav-btn": "Get Consultation",
                "hero-title": "Uzbekistan's Most Exclusive & Luxury Real Estate",
                "hero-subtitle": "A curated collection of luxury penthouses, villas, and estates across Tashkent, Samarkand, and Bukhara.",
                "filter-city": "City / Location",
                "filter-type": "Property Type",
                "filter-price": "Max Price",
                "filter-search": "Search",
                "section-subtitle": "Featured Properties",
                "section-title": "Exclusive Property Catalog (10 Projects)",
                "section-desc": "Every project is thoroughly vetted for architectural superiority and legal clarity.",
                "calc-sub": "Financial Calculator",
                "calc-title": "Mortgage & Installment Calculator",
                "calc-total": "Property Value ($)",
                "calc-down": "Down Payment ($)",
                "calc-years": "Term (Years)",
                "calc-summary": "Calculation Summary",
                "calc-monthly-label": "Est. Monthly Payment:",
                "calc-loan-amount": "Loan Amount:",
                "calc-interest-rate": "Annual Rate:",
                "calc-apply": "Apply Now",
                "about-sub": "Why LUXESTATE?",
                "about-title": "Your Trusted Premium Partner in Uzbekistan",
                "about-text": "Over 10 years of experience in ultra-luxury real estate. We guarantee full privacy and legal assurance.",
                "stat-1": "Luxury Properties Sold",
                "stat-2": "Legal Guarantee",
                "contact-sub": "Contact Us",
                "contact-title": "Connect With Our Experts",
                "contact-desc": "Have questions or want to schedule a viewing? Fill out the form and we'll contact you within 15 mins.",
                "form-name": "Your Name",
                "form-phone": "Phone Number",
                "form-message": "Property Interest / Message",
                "form-submit": "Submit Application",
                "fav-title": "Saved Properties"
            }
        };

        function setLanguage(lang) {
            const dict = i18n[lang];
            if (!dict) return;

            document.querySelectorAll('[data-i18n]').forEach(el => {
                const key = el.getAttribute('data-i18n');
                if (dict[key]) {
                    el.innerText = dict[key];
                }
            });
        }

        // Init App
        document.addEventListener('DOMContentLoaded', () => {
            // Dark mode default
            document.documentElement.classList.add('dark');
            renderProperties(properties);
            calculateMortgage();
        });
    </script>
</body>
</html>
