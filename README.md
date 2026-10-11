# Sameer-Enterprises--555
Sameer Enterprises 
```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sameer Enterprises | Furniture & Electronics Showcase | Udaipura</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Plus Jakarta Sans -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            50: '#ecfdf5',
                            100: '#d1fae5',
                            200: '#a7f3d0',
                            300: '#6ee7b7',
                            400: '#34d399',
                            500: '#10b981',
                            600: '#059669',
                            700: '#047857',
                            800: '#065f46',
                            900: '#064e3b',
                            950: '#022c22'
                        },
                        amber: {
                            400: '#fbbf24',
                            500: '#f59e0b',
                            600: '#d97706'
                        }
                    }
                }
            }
        }
    </script>
    <style>
        .glass-header {
            background: rgba(255, 255, 255, 0.96);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
        }
        .mint-gradient {
            background: linear-gradient(135deg, #f0fdf4 0%, #ecfdf5 50%, #ffffff 100%);
        }
        .card-hover-effect {
            transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .card-hover-effect:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 25px -5px rgba(5, 150, 105, 0.12), 0 8px 10px -6px rgba(5, 150, 105, 0.08);
        }
        .doodle-card {
            transition: all 0.22s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .doodle-card:hover {
            transform: translateY(-4px) scale(1.02);
            border-color: #059669;
            background-color: #d1fae5;
        }
        .scrollbar-none::-webkit-scrollbar {
            display: none;
        }
        .scrollbar-none {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 font-sans antialiased selection:bg-brand-600 selection:text-white min-h-screen flex flex-col justify-between">

    <div class="bg-brand-950 text-white text-xs py-2.5 px-4 sticky top-0 z-50 border-b border-brand-800/60 shadow-sm">
        <div class="max-w-7xl mx-auto flex flex-col sm:flex-row items-center justify-between gap-2">
            <div class="flex items-center gap-2 text-amber-400 font-extrabold">
                <span class="flex h-2.5 w-2.5 relative">
                  <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-amber-400 opacity-75"></span>
                  <span class="relative inline-flex rounded-full h-2.5 w-2.5 bg-amber-500"></span>
                </span>
                <i data-lucide="sparkles" class="w-4 h-4 text-amber-400"></i>
                <span class="tracking-wide uppercase text-[11px] text-white">0% Interest Financing Available</span>
            </div>

            <div class="flex items-center gap-4 text-xs text-brand-200 font-semibold">
                <a href="tel:9993190090" class="hover:text-amber-300 font-bold flex items-center gap-1.5 transition">
                    <i data-lucide="phone" class="w-3.5 h-3.5 text-amber-400"></i>
                    <span>+91 9993190090</span>
                </a>
                <span class="hidden sm:inline text-brand-700">|</span>
                <span class="hidden sm:inline text-brand-200">Jawahar Chowk, Udaipura (M.P.)</span>
            </div>
        </div>
    </div>

    <header class="sticky top-[37px] z-40 glass-header border-b border-brand-100 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            
            <a href="javascript:void(0)" onclick="switchPage('home')" class="flex items-center gap-3.5 group">
                <div class="w-12 h-12 bg-gradient-to-tr from-brand-800 to-brand-600 text-white rounded-xl flex items-center justify-center font-black text-2xl shadow-md shadow-brand-900/20 group-hover:scale-105 transition-transform">
                    SE
                </div>
                <div>
                    <span class="text-xl sm:text-2xl font-black tracking-tight text-slate-900 block leading-none">SAMEER ENTERPRISES</span>
                    <span class="text-[10px] font-extrabold text-brand-700 tracking-[0.2em] uppercase mt-1 block">FURNITURE & ELECTRONICS</span>
                </div>
            </a>

            <!-- 2-Page View Switcher Navigation -->
            <nav class="hidden md:flex items-center gap-2 bg-brand-50/90 p-1.5 rounded-2xl border border-brand-100">
                <button onclick="switchPage('home')" id="nav-home" class="px-5 py-2.5 rounded-xl text-xs font-black transition bg-brand-700 text-white shadow-sm flex items-center gap-2">
                    <i data-lucide="home" class="w-4 h-4"></i>
                    <span>Home Showcase</span>
                </button>
                <button onclick="switchPage('catalog')" id="nav-catalog" class="px-5 py-2.5 rounded-xl text-xs font-bold transition text-slate-600 hover:text-slate-900 flex items-center gap-2">
                    <i data-lucide="grid" class="w-4 h-4"></i>
                    <span>Full Product Catalog</span>
                </button>
            </nav>

            <div class="hidden sm:flex items-center gap-3">
                <a href="https://wa.me/919993190090?text=Hi%20Sameer%20Enterprises,%20I%20want%20to%20inquire%20about%20your%20products." target="_blank" class="px-5 py-2.5 rounded-xl bg-brand-600 hover:bg-brand-700 text-white font-bold text-xs transition shadow-md shadow-brand-600/20 flex items-center gap-2">
                    <i data-lucide="message-circle" class="w-4 h-4"></i>
                    <span>WhatsApp Store</span>
                </a>
            </div>

            <button id="menuToggle" class="md:hidden p-2.5 rounded-xl bg-brand-50 text-brand-900 border border-brand-200">
                <i data-lucide="menu" class="w-6 h-6"></i>
            </button>
        </div>

        <!-- Mobile Drawer Menu -->
        <div id="mobileDrawer" class="hidden md:hidden border-b border-brand-100 bg-white px-6 py-5 space-y-3 shadow-xl">
            <button onclick="switchPage('home'); closeMobileMenu();" class="w-full text-left py-2.5 px-4 rounded-xl bg-brand-50 text-brand-900 font-extrabold text-xs flex items-center gap-2">
                <i data-lucide="home" class="w-4 h-4"></i>
                <span>Home Showcase</span>
            </button>
            <button onclick="switchPage('catalog'); closeMobileMenu();" class="w-full text-left py-2.5 px-4 rounded-xl text-slate-700 font-bold text-xs flex items-center gap-2">
                <i data-lucide="grid" class="w-4 h-4"></i>
                <span>Full Product Catalog</span>
            </button>
            <a href="https://wa.me/919993190090?text=Hi%20Sameer%20Enterprises,%20I%20want%20to%20inquire%20about%20your%20products." target="_blank" class="w-full py-3 bg-brand-600 text-white rounded-xl text-center font-bold text-xs flex items-center justify-center gap-2 shadow-sm">
                <i data-lucide="message-circle" class="w-4 h-4"></i>
                <span>Chat on WhatsApp (+91 9993190090)</span>
            </a>
        </div>
    </header>

    <div id="page-home">
        <!-- Hero Banner Section -->
        <section class="relative pt-10 lg:pt-16 pb-20 mint-gradient border-b border-brand-100">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid lg:grid-cols-12 gap-12 items-center">
                    
                    <div class="lg:col-span-7 space-y-6">
                        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-brand-100/90 border border-brand-200 text-brand-900 text-xs font-extrabold shadow-sm">
                            <i data-lucide="shield-check" class="w-4 h-4 text-brand-600"></i>
                            <span>Trusted Store in Udaipura</span>
                        </div>

                        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-black text-slate-900 tracking-tight leading-[1.12]">
                            Upgrade Your Home With Premier <span class="text-brand-700">Furniture</span> & <span class="text-amber-600">Electronics</span>
                        </h1>

                        <p class="text-slate-600 text-base sm:text-lg leading-relaxed font-medium max-w-2xl">
                            Visit Sameer Enterprises in Udaipura for top-quality home furniture, smart TVs, refrigerators, and essential home appliances under one roof.
                        </p>

                        <div class="pt-2 flex flex-col sm:flex-row items-stretch sm:items-center gap-4">
                            <button onclick="switchPage('catalog')" class="px-8 py-4 rounded-xl bg-brand-700 hover:bg-brand-800 text-white font-extrabold text-sm shadow-lg shadow-brand-700/25 transition flex items-center justify-center gap-3">
                                <span>Browse Full Catalog</span>
                                <i data-lucide="arrow-right" class="w-5 h-5"></i>
                            </button>
                            <a href="#location" class="px-8 py-4 rounded-xl bg-white hover:bg-brand-50 text-brand-900 font-bold text-sm transition flex items-center justify-center gap-3 border border-brand-200 shadow-sm">
                                <i data-lucide="map-pin" class="w-5 h-5 text-brand-600"></i>
                                <span>Visit Showroom</span>
                            </a>
                        </div>

                        <!-- Highlights Badges -->
                        <div class="pt-8 border-t border-brand-200/80 grid grid-cols-3 gap-4">
                            <div class="bg-white/80 backdrop-blur p-4 rounded-2xl border border-brand-100 text-center shadow-sm">
                                <p class="text-2xl sm:text-3xl font-black text-brand-800">0%</p>
                                <p class="text-xs text-slate-500 font-bold mt-1">Interest Financing</p>
                            </div>
                            <div class="bg-white/80 backdrop-blur p-4 rounded-2xl border border-brand-100 text-center shadow-sm">
                                <p class="text-2xl sm:text-3xl font-black text-brand-800">100%</p>
                                <p class="text-xs text-slate-500 font-bold mt-1">Genuine Brands</p>
                            </div>
                            <div class="bg-white/80 backdrop-blur p-4 rounded-2xl border border-brand-100 text-center shadow-sm">
                                <p class="text-2xl sm:text-3xl font-black text-brand-800">Fast</p>
                                <p class="text-xs text-slate-500 font-bold mt-1">Local Delivery</p>
                            </div>
                        </div>
                    </div>

                    <div class="lg:col-span-5">
                        <div class="relative bg-white p-3 rounded-3xl border border-brand-200 shadow-2xl shadow-brand-900/10">
                            <div class="relative h-[420px] rounded-2xl overflow-hidden">
                                <img src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?auto=format&fit=crop&w=1000&q=80" alt="Sameer Enterprises Showroom" class="w-full h-full object-cover">
                                <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent"></div>
                                <div class="absolute bottom-4 left-4 right-4 p-4 bg-white/95 backdrop-blur rounded-xl border border-brand-100 shadow-lg">
                                    <p class="text-[10px] font-extrabold text-brand-700 uppercase tracking-widest">Store Location</p>
                                    <h3 class="text-base font-black text-slate-900">Sameer Enterprises</h3>
                                    <p class="text-xs text-slate-600 mt-0.5">Jawahar Chowk, In front of Post Office, Udaipura, Dist. Raisen, M.P.</p>
                                </div>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <section id="categories" class="py-16 bg-white border-b border-slate-200/80">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-2xl mx-auto mb-10">
                    <span class="text-xs font-black uppercase tracking-widest text-brand-700">Top Categories</span>
                    <h2 class="text-3xl font-extrabold text-slate-900 mt-1">What We Sell</h2>
                    <p class="text-xs text-slate-500 mt-2">Tap any item or "And Many More..." to open our full catalog page!</p>
                </div>

                <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-7 gap-4" id="mainDoodleGrid">
                    <!-- 6 Main Doodle Cards + 1 "And Many More..." Redirect Card rendered via JS -->
                </div>
            </div>
        </section>

        <!-- Featured Offers Showcase on Home Page -->
        <section id="products" class="py-20 bg-slate-50">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex flex-col md:flex-row items-center justify-between gap-6 mb-12">
                    <div>
                        <span class="text-xs font-black uppercase tracking-widest text-brand-700">In-Store Highlights</span>
                        <h2 class="text-3xl font-extrabold text-slate-900 mt-1">Featured Bestsellers</h2>
                    </div>

                    <button onclick="switchPage('catalog')" class="px-6 py-3 rounded-xl bg-brand-700 hover:bg-brand-800 text-white font-extrabold text-xs transition flex items-center gap-2 shadow-sm">
                        <span>View All Items in Catalog</span>
                        <i data-lucide="chevron-right" class="w-4 h-4"></i>
                    </button>
                </div>

                <div id="homeFeaturedGrid" class="grid sm:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Bestseller product cards rendered dynamically via JS -->
                </div>
            </div>
        </section>

        <!-- Store Location and Contact Section -->
        <section id="location" class="py-20 bg-white border-t border-brand-100">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="bg-gradient-to-br from-brand-950 via-brand-900 to-slate-950 text-white rounded-3xl p-8 lg:p-12 shadow-2xl relative overflow-hidden">
                    <div class="grid lg:grid-cols-2 gap-12 items-center">
                        
                        <div class="space-y-6">
                            <span class="text-amber-400 text-xs font-extrabold uppercase tracking-widest">Visit Store</span>
                            <h2 class="text-3xl sm:text-4xl font-black leading-tight">Sameer Enterprises</h2>

                            <div class="space-y-4 text-brand-100">
                                <div class="flex items-start gap-4 p-4 rounded-2xl bg-white/10 border border-white/10">
                                    <div class="w-10 h-10 rounded-xl bg-amber-500/20 text-amber-400 flex items-center justify-center shrink-0">
                                        <i data-lucide="map-pin" class="w-5 h-5"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-bold text-white text-sm">Full Showroom Address</h4>
                                        <p class="text-xs text-brand-100 mt-1 leading-relaxed">
                                            Sameer Enterprises, Jawahar Chowk, In front of Post Office, Udaipura, Dist. Raisen, Madhya Pradesh.
                                        </p>
                                    </div>
                                </div>

                                <div class="flex items-start gap-4 p-4 rounded-2xl bg-white/10 border border-white/10">
                                    <div class="w-10 h-10 rounded-xl bg-amber-500/20 text-amber-400 flex items-center justify-center shrink-0">
                                        <i data-lucide="phone" class="w-5 h-5"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-bold text-white text-sm">Phone / WhatsApp Inquiry</h4>
                                        <p class="text-xs text-brand-100 mt-1 font-mono font-bold">+91 9993190090</p>
                                    </div>
                                </div>

                                <div class="flex items-start gap-4 p-4 rounded-2xl bg-white/10 border border-white/10">
                                    <div class="w-10 h-10 rounded-xl bg-amber-500/20 text-amber-400 flex items-center justify-center shrink-0">
                                        <i data-lucide="clock" class="w-5 h-5"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-bold text-white text-sm">Store Timings</h4>
                                        <p class="text-xs text-brand-100 mt-1">Monday – Sunday: 10:00 AM – 8:30 PM (Open Daily)</p>
                                    </div>
                                </div>
                            </div>

                            <div class="flex flex-wrap gap-3 pt-2">
                                <a href="tel:9993190090" class="px-6 py-3.5 rounded-xl bg-amber-500 hover:bg-amber-400 text-slate-950 font-extrabold text-xs transition flex items-center gap-2 shadow-md">
                                    <i data-lucide="phone-call" class="w-4 h-4"></i>
                                    <span>Call Store Directly</span>
                                </a>
                                <a href="https://wa.me/919993190090?text=Hello%20Sameer%20Enterprises,%20I%20want%20to%20visit%20your%20showroom%20at%20Jawahar%20Chowk,%20Udaipura." target="_blank" class="px-6 py-3.5 rounded-xl bg-brand-600 hover:bg-brand-500 text-white font-extrabold text-xs transition shadow-md flex items-center gap-2">
                                    <i data-lucide="message-circle" class="w-4 h-4"></i>
                                    <span>WhatsApp Inquiry</span>
                                </a>
                            </div>
                        </div>

                        <div class="bg-white text-slate-900 rounded-3xl p-8 text-center shadow-lg border border-brand-100">
                            <div class="w-16 h-16 rounded-full bg-brand-100 text-brand-800 flex items-center justify-center mx-auto mb-4">
                                <i data-lucide="percent" class="w-8 h-8"></i>
                            </div>
                            <h3 class="text-2xl font-black mb-2">0% Interest Financing</h3>
                            <p class="text-xs text-slate-600 max-w-xs mx-auto mb-6">Easy EMI options available on all furniture sets, Smart TVs, Refrigerators, and Home Appliances with minimal documentation.</p>
                            <div class="p-3.5 bg-brand-50 text-brand-950 font-bold text-xs rounded-xl border border-brand-200">
                                Visit Jawahar Chowk store for instant loan approval!
                            </div>
                        </div>

                    </div>
                </div>
            </div>
        </section>
    </div>

    <div id="page-catalog" class="hidden">
        <section class="py-12 bg-slate-50 border-b border-brand-100 min-h-screen">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                
                <div class="bg-white p-6 rounded-3xl border border-brand-100 shadow-sm mb-10">
                    <div class="flex flex-col lg:flex-row items-center justify-between gap-6">
                        <div>
                            <span class="text-xs font-black uppercase tracking-widest text-brand-700">Page 2 — Full Inventory</span>
                            <h1 class="text-3xl font-extrabold text-slate-900 mt-1">Complete Product Catalog</h1>
                            <p class="text-xs text-slate-500 mt-1">Browse our entire inventory of furniture, electronics, and home appliances.</p>
                        </div>

                        <!-- Real-time Search Input -->
                        <div class="w-full lg:w-96 relative">
                            <i data-lucide="search" class="w-4 h-4 absolute left-4 top-1/2 -translate-y-1/2 text-slate-400"></i>
                            <input type="text" id="catalogSearch" oninput="handleCatalogSearch()" placeholder="Search TV, Sofa, Fridge, Fan, Iron, Cycle..." class="w-full pl-11 pr-4 py-3 bg-slate-50 border border-slate-200 rounded-2xl text-xs font-semibold focus:outline-none focus:border-brand-600 focus:bg-white transition">
                        </div>
                    </div>

                    <!-- Category Filter Chips -->
                    <div class="mt-6 pt-6 border-t border-slate-100 flex items-center gap-2 overflow-x-auto pb-2 scrollbar-none" id="categoryChips">
                        <!-- Chips rendered dynamically via JS -->
                    </div>
                </div>

                <!-- Catalog Grid -->
                <div id="catalogGrid" class="grid sm:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Complete inventory rendered dynamically via JS -->
                </div>

            </div>
        </section>
    </div>

    <footer class="py-8 bg-slate-950 text-slate-400 text-center text-xs border-t border-slate-900">
        <p>© 2026 Sameer Enterprises. All rights reserved. Jawahar Chowk, In front of Post Office, Udaipura, Dist. Raisen (M.P.). Phone: +91 9993190090</p>
    </footer>

    <script>
        const storePhone = "919993190090";

        // Main 6 Featured Category Doodles for Home Page
        const main6Doodles = [
            { 
                id: "led", 
                name: "Smart LED TVs", 
                cat: "electronics", 
                svg: `<svg xmlns="http://www.w3.org/2000/svg" class="w-7 h-7" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="2" y="3" width="20" height="14" rx="2"/><line x1="8" y1="21" x2="16" y2="21"/><line x1="12" y1="17" x2="12" y2="21"/></svg>` 
            },
            { 
                id: "fridge", 
                name: "Refrigerators", 
                cat: "appliances", 
                svg: `<svg xmlns="http://www.w3.org/2000/svg" class="w-7 h-7" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="4" y="2" width="16" height="20" rx="2"/><line x1="4" y1="10" x2="20" y2="10"/><line x1="8" y1="5" x2="8" y2="7"/><line x1="8" y1="13" x2="8" y2="16"/></svg>` 
            },
            { 
                id: "wm", 
                name: "Washing Machines", 
                cat: "appliances", 
                svg: `<svg xmlns="http://www.w3.org/2000/svg" class="w-7 h-7" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="12" cy="13" r="5"/><path d="M12 10a3 3 0 0 1 3 3"/></svg>` 
            },
            { 
                id: "bed", 
                name: "Beds & Mattresses", 
                cat: "furniture", 
                svg: `<svg xmlns="http://www.w3.org/2000/svg" class="w-7 h-7" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M2 4v16M2 11h20M20 4v16M4 11V7a2 2 0 0 1 2-2h4a2 2 0 0 1 2 2v4"/></svg>` 
            },
            { 
                id: "almirah", 
                name: "Steel Almirahs", 
                cat: "furniture", 
                svg: `<svg xmlns="http://www.w3.org/2000/svg" class="w-7 h-7" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="4" y="3" width="16" height="18" rx="1"/><line x1="12" y1="3" x2="12" y2="21"/><line x1="10" y1="11" x2="10" y2="13"/><line x1="14" y1="11" x2="14" y2="13"/></svg>` 
            },
            { 
                id: "sofa", 
                name: "L-Shape Sofas", 
                cat: "furniture", 
                svg: `<svg xmlns="http://www.w3.org/2000/svg" class="w-7 h-7" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M19 9V6a2 2 0 0 0-2-2H7a2 2 0 0 0-2 2v3"/><path d="M3 11h18v4H3z"/><path d="M5 15v5M19 15v5"/></svg>` 
            }
        ];

        // Comprehensive Master Product Catalog Database with prices & images
        const fullCatalogProducts = [
            {
                id: 1,
                name: "Sony 55\" 4K Smart LED TV",
                category: "electronics",
                badge: "Sony Premium",
                price: "₹45,000*",
                image: "https://images.unsplash.com/photo-1593784991095-a205069470b6?auto=format&fit=crop&w=600&q=80",
                desc: "4K Ultra HD resolution, Google TV OS, Dolby Atmos audio & vivid color display."
            },
            {
                id: 2,
                name: "Premium L-Shape Sofa Set",
                category: "furniture",
                badge: "Bestseller",
                price: "₹25,000*",
                image: "https://images.unsplash.com/photo-1555041469-a586c61ea9bc?auto=format&fit=crop&w=600&q=80",
                desc: "High-density cushioning, termite-resistant solid wood frame & rich fabric finish."
            },
            {
                id: 3,
                name: "Samsung 350L Double Door Refrigerator",
                category: "appliances",
                badge: "350 Liters",
                price: "₹38,000*",
                image: "https://images.unsplash.com/photo-1584568694244-14fbdf83bd30?auto=format&fit=crop&w=600&q=80",
                desc: "Digital Inverter compressor, convertible cooling zones & high energy efficiency."
            },
            {
                id: 4,
                name: "LG 10kg Fully Automatic Washing Machine",
                category: "appliances",
                badge: "10kg Capacity",
                price: "₹28,990*",
                image: "https://images.unsplash.com/photo-1626806787461-102c1bfaaea1?auto=format&fit=crop&w=600&q=80",
                desc: "Smart Inverter motor, steam hygiene wash cycles & high speed turbo dryer."
            },
            {
                id: 5,
                name: "King Size Wooden Bed with Storage",
                category: "furniture",
                badge: "Solid Wood",
                price: "₹22,000*",
                image: "https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?auto=format&fit=crop&w=600&q=80",
                desc: "Solid teak-finish wood construction with heavy hydraulic box storage."
            },
            {
                id: 6,
                name: "Heavy Duty Steel Almirah",
                category: "furniture",
                badge: "Heavy Gauge",
                price: "₹14,500*",
                image: "https://images.unsplash.com/photo-1595428774223-ef52624120d2?auto=format&fit=crop&w=600&q=80",
                desc: "Rust-free powder coated heavy steel wardrobe with double internal safety locks."
            },
            {
                id: 7,
                name: "Ergonomic Wooden Study Table",
                category: "furniture",
                badge: "Study Special",
                price: "₹6,500*",
                image: "https://images.unsplash.com/photo-1518455027359-f3f8164ba6bd?auto=format&fit=crop&w=600&q=80",
                desc: "Spacious wooden study desk with built-in bookshelf, drawer & lock."
            },
            {
                id: 8,
                name: "High-Speed Ceiling Fan",
                category: "appliances",
                badge: "Copper Winding",
                price: "₹2,200*",
                image: "https://images.unsplash.com/photo-1618944847828-82e943c3bdb7?auto=format&fit=crop&w=600&q=80",
                desc: "100% copper winding motor with aerodynamically designed wide blades."
            },
            {
                id: 9,
                name: "Automatic Dry Iron",
                category: "small-appliances",
                badge: "Non-Stick",
                price: "₹850*",
                image: "https://images.unsplash.com/photo-1585842378081-5c0809b2922a?auto=format&fit=crop&w=600&q=80",
                desc: "Non-stick coated soleplate, thermal fuse protection & 360-degree swivel cord."
            },
            {
                id: 10,
                name: "Heavy Duty Immersion Rod",
                category: "small-appliances",
                badge: "Fast Heating",
                price: "₹450*",
                image: "https://images.unsplash.com/photo-1544816155-12df9643f363?auto=format&fit=crop&w=600&q=80",
                desc: "Shockproof nickel-plated copper heating element for quick water heating."
            },
            {
                id: 11,
                name: "Multi-Tier Kitchen & Storage Rack",
                category: "furniture",
                badge: "Modular",
                price: "₹1,850*",
                image: "https://images.unsplash.com/photo-1595428774223-ef52624120d2?auto=format&fit=crop&w=600&q=80",
                desc: "Heavy duty steel frame storage rack for kitchen utensils, microwave & appliances."
            },
            {
                id: 12,
                name: "Digital Receiver / Set-Top Box",
                category: "electronics",
                badge: "HD Quality",
                price: "₹1,200*",
                image: "https://images.unsplash.com/photo-1593784991095-a205069470b6?auto=format&fit=crop&w=600&q=80",
                desc: "High definition DTH receiver box with crystal clear reception & HDMI output."
            },
            {
                id: 13,
                name: "Heavy Duty Induction Cooktop (2000W)",
                category: "small-appliances",
                badge: "Feather Touch",
                price: "₹2,800*",
                image: "https://images.unsplash.com/photo-1556911220-e15b29be8c8f?auto=format&fit=crop&w=600&q=80",
                desc: "Feather touch control panel, preset Indian cooking modes & automatic shutoff."
            },
            {
                id: 14,
                name: "Storage Water Geyser (25L)",
                category: "appliances",
                badge: "25 Liters",
                price: "₹6,500*",
                image: "https://images.unsplash.com/photo-1584568694244-14fbdf83bd30?auto=format&fit=crop&w=600&q=80",
                desc: "Glass lined tank insulation, fast heating coil & 5-star energy saving rating."
            },
            {
                id: 15,
                name: "Desert Air Cooler",
                category: "appliances",
                badge: "High Air Throw",
                price: "₹7,500*",
                image: "https://images.unsplash.com/photo-1626806787461-102c1bfaaea1?auto=format&fit=crop&w=600&q=80",
                desc: "Heavy duty motor with honeycomb cooling pads & large water tank capacity."
            },
            {
                id: 16,
                name: "Fancy Gear Bicycle / Cycle",
                category: "furniture",
                badge: "Multi-Gear",
                price: "₹8,500*",
                image: "https://images.unsplash.com/photo-1485965120184-e220f721d03e?auto=format&fit=crop&w=600&q=80",
                desc: "Sturdy steel frame bicycle with front suspension, dual disc brakes & multi-gears."
            },
            {
                id: 17,
                name: "Premium Plastic & Cushioned Chairs",
                category: "furniture",
                badge: "Set of 2",
                price: "₹1,500*",
                image: "https://images.unsplash.com/photo-1580481072645-022f9a6d8310?auto=format&fit=crop&w=600&q=80",
                desc: "Heavy weight plastic molded chairs with comfortable ergonomic backrest design."
            },
            {
                id: 18,
                name: "Heavy Duty Mixer Grinder (750W)",
                category: "small-appliances",
                badge: "3 Stainless Jars",
                price: "₹3,200*",
                image: "https://images.unsplash.com/photo-1570222094114-d054a817e56b?auto=format&fit=crop&w=600&q=80",
                desc: "High speed 750W copper motor with 3 leakproof stainless steel grinding jars."
            }
        ];

        let selectedCatalogCategory = "all";

        function renderMainDoodles() {
            const container = document.getElementById('mainDoodleGrid');
            
            const mainCardsHtml = main6Doodles.map(item => `
                <div onclick="filterCatalogFromHome('${item.cat}')" class="doodle-card p-5 rounded-2xl bg-brand-50/80 border border-brand-100 text-center cursor-pointer group flex flex-col items-center justify-center">
                    <div class="w-12 h-12 rounded-2xl bg-brand-700 text-white flex items-center justify-center mb-3 shadow-sm group-hover:bg-brand-800 transition">
                        ${item.svg}
                    </div>
                    <p class="text-xs font-extrabold text-slate-800 group-hover:text-brand-900 leading-tight">${item.name}</p>
                </div>
            `).join('');

            const manyMoreCardHtml = `
                <div onclick="switchPage('catalog')" class="doodle-card p-5 rounded-2xl bg-gradient-to-br from-brand-800 to-brand-950 text-white text-center cursor-pointer hover:shadow-lg transition flex flex-col items-center justify-center group shadow-sm col-span-2 sm:col-span-1">
                    <div class="w-11 h-11 rounded-full bg-amber-400 text-slate-950 flex items-center justify-center font-black text-xl mb-2 group-hover:scale-110 transition">
                        +
                    </div>
                    <p class="text-xs font-black text-amber-300">And Many More...</p>
                    <p class="text-[10px] text-brand-200 mt-0.5">Click for Page 2 Full Catalog</p>
                </div>
            `;

            container.innerHTML = mainCardsHtml + manyMoreCardHtml;
        }

        // Render Featured Items on Home Page
        function renderHomeFeatured() {
            const container = document.getElementById('homeFeaturedGrid');
            const featuredList = fullCatalogProducts.slice(0, 6);
            container.innerHTML = featuredList.map(p => createProductCardHtml(p)).join('');
            lucide.createIcons();
        }

        function createProductCardHtml(p) {
            const productMsg = `Hello Sameer Enterprises, I am inquiring about: ${p.name} listed at ${p.price}. Please confirm availability at your store.`;
            const waUrl = `https://wa.me/${storePhone}?text=${encodeURIComponent(productMsg)}`;

            return `
                <div class="bg-white rounded-3xl overflow-hidden border border-brand-100 shadow-sm card-hover-effect flex flex-col justify-between group">
                    <div>
                        <div class="relative h-52 overflow-hidden bg-brand-50">
                            <img src="${p.image}" alt="${p.name}" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
                            <span class="absolute top-3 left-3 bg-brand-700 text-white font-extrabold text-[10px] uppercase tracking-wider px-3 py-1 rounded-lg shadow-sm">
                                ${p.badge}
                            </span>
                        </div>
                        <div class="p-6">
                            <h3 class="text-base font-bold text-slate-900 group-hover:text-brand-700 transition">${p.name}</h3>
                            <p class="text-xs text-slate-500 mt-2 leading-relaxed">${p.desc}</p>
                        </div>
                    </div>
                    <div class="p-6 pt-0">
                        <div class="flex flex-col mb-4 pb-3 border-b border-slate-100">
                            <div class="flex items-center justify-between">
                                <span class="text-[11px] font-bold text-slate-400 uppercase tracking-wider">Showroom Price</span>
                                <span class="text-sm font-black text-brand-800 bg-brand-50 px-2.5 py-1 rounded-md border border-brand-200">${p.price}</span>
                            </div>
                            
                            <!-- MANDATORY DUAL DISCLAIMER ON EVERY PRODUCT CARD -->
                            <div class="mt-2.5 pt-2 border-t border-slate-100 text-[10px] text-slate-500 font-semibold space-y-0.5">
                                <p class="flex items-center gap-1"><span class="text-amber-600 font-bold">*</span> Prices could be different in store</p>
                                <p class="flex items-center gap-1"><span class="text-amber-600 font-bold">*</span> Actual product could be different</p>
                            </div>
                        </div>
                        
                        <a href="${waUrl}" target="_blank" class="w-full py-3.5 rounded-2xl bg-brand-600 hover:bg-brand-700 text-white font-extrabold text-xs transition flex items-center justify-center gap-2 shadow-sm shadow-brand-600/20">
                            <i data-lucide="message-circle" class="w-4 h-4"></i>
                            <span>Inquire on WhatsApp</span>
                        </a>
                    </div>
                </div>
            `;
        }

        function switchPage(page) {
            const homePage = document.getElementById('page-home');
            const catalogPage = document.getElementById('page-catalog');
            const navHome = document.getElementById('nav-home');
            const navCatalog = document.getElementById('nav-catalog');

            if (page === 'home') {
                homePage.classList.remove('hidden');
                catalogPage.classList.add('hidden');

                navHome.className = "px-5 py-2.5 rounded-xl text-xs font-black transition bg-brand-700 text-white shadow-sm flex items-center gap-2";
                navCatalog.className = "px-5 py-2.5 rounded-xl text-xs font-bold transition text-slate-600 hover:text-slate-900 flex items-center gap-2";
                window.scrollTo({ top: 0, behavior: 'smooth' });
            } else {
                homePage.classList.add('hidden');
                catalogPage.classList.remove('hidden');

                navCatalog.className = "px-5 py-2.5 rounded-xl text-xs font-black transition bg-brand-700 text-white shadow-sm flex items-center gap-2";
                navHome.className = "px-5 py-2.5 rounded-xl text-xs font-bold transition text-slate-600 hover:text-slate-900 flex items-center gap-2";
                
                renderCategoryChips();
                renderCatalogGrid();
                window.scrollTo({ top: 0, behavior: 'smooth' });
            }
        }

        function filterCatalogFromHome(cat) {
            selectedCatalogCategory = cat;
            switchPage('catalog');
        }

        // Render Category Chips on Page 2 Catalog
        function renderCategoryChips() {
            const chipContainer = document.getElementById('categoryChips');
            const categories = [
                { id: "all", label: "All Items" },
                { id: "electronics", label: "Electronics" },
                { id: "furniture", label: "Furniture" },
                { id: "appliances", label: "Home Appliances" },
                { id: "small-appliances", label: "Small Appliances" }
            ];

            chipContainer.innerHTML = categories.map(c => `
                <button onclick="setCatalogCat('${c.id}')" class="px-4 py-2 rounded-xl text-xs font-extrabold whitespace-nowrap transition ${selectedCatalogCategory === c.id ? 'bg-brand-700 text-white shadow-sm' : 'bg-slate-100 text-slate-600 hover:bg-slate-200'}">
                    ${c.label}
                </button>
            `).join('');
        }

        function setCatalogCat(cat) {
            selectedCatalogCategory = cat;
            renderCategoryChips();
            renderCatalogGrid();
        }

        // Render Complete Page 2 Inventory Grid with Search & Category Filter
        function renderCatalogGrid() {
            const container = document.getElementById('catalogGrid');
            const query = document.getElementById('catalogSearch')?.value.toLowerCase() || "";

            let filtered = fullCatalogProducts;

            if (selectedCatalogCategory !== 'all') {
                filtered = filtered.filter(p => p.category === selectedCatalogCategory);
            }

            if (query) {
                filtered = filtered.filter(p => p.name.toLowerCase().includes(query) || p.desc.toLowerCase().includes(query));
            }

            if (filtered.length === 0) {
                container.innerHTML = `
                    <div class="col-span-full py-16 text-center text-slate-400 bg-white rounded-3xl border border-brand-100">
                        <i data-lucide="package-search" class="w-12 h-12 mx-auto mb-3 text-slate-300"></i>
                        <p class="font-bold text-slate-700">No matching items found</p>
                        <p class="text-xs mt-1">Try searching for sofa, bed, fridge, fan, iron, or cycle</p>
                    </div>
                `;
            } else {
                container.innerHTML = filtered.map(p => createProductCardHtml(p)).join('');
            }
            lucide.createIcons();
        }

        function handleCatalogSearch() {
            renderCatalogGrid();
        }

        function closeMobileMenu() {
            document.getElementById('mobileDrawer').classList.add('hidden');
        }

        document.getElementById('menuToggle').addEventListener('click', () => {
            document.getElementById('mobileDrawer').classList.toggle('hidden');
        });

        // Initialize Application
        window.onload = function() {
            renderMainDoodles();
            renderHomeFeatured();
            lucide.createIcons();
        };
    </script>
</body>
</html>
```
