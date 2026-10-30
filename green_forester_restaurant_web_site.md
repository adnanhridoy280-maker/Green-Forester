```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Green Forester | Organic Culinary & Fine Dining</title>
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            forest: {
              50: '#f0fdf4',
              100: '#dcfce7',
              500: '#22c55e',
              600: '#16a34a',
              700: '#15803d',
              800: '#166534',
              900: '#14532d',
              950: '#052e16',
            },
            sage: {
              300: '#86efac',
              400: '#4ade80',
              500: '#22c55e',
            },
            warmdark: {
              900: '#0a140d',
              800: '#122217',
              700: '#1c3323',
            }
          },
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            serif: ['Playfair Display', 'Georgia', 'serif'],
          }
        }
      }
    }
  </script>

  <!-- Google Fonts & Font Awesome Icons -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,600;0,700;1,400&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  
  <style>
    /* Custom Scrollbar */
    ::-webkit-scrollbar {
      width: 8px;
    }
    ::-webkit-scrollbar-track {
      background: #0a140d;
    }
    ::-webkit-scrollbar-thumb {
      background: #16a34a;
      border-radius: 4px;
    }

    .glass-nav {
      background: rgba(10, 20, 13, 0.85);
      backdrop-filter: blur(12px);
    }
    .light .glass-nav {
      background: rgba(255, 255, 255, 0.92);
      backdrop-filter: blur(12px);
    }

    /* Keyframe Animations */
    @keyframes fadeSlideUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes goldShimmer {
      0% { background-position: -200% 0; }
      100% { background-position: 200% 0; }
    }

    @keyframes kenBurns {
      0% { transform: scale(1); }
      50% { transform: scale(1.08); }
      100% { transform: scale(1); }
    }

    @keyframes pulseGlow {
      0%, 100% { box-shadow: 0 0 15px rgba(34, 197, 94, 0.4); }
      50% { box-shadow: 0 0 30px rgba(34, 197, 94, 0.8); }
    }

    .anim-fade-up {
      animation: fadeSlideUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
    }

    .shimmer-text {
      background: linear-gradient(90deg, #4ade80 0%, #ffffff 50%, #4ade80 100%);
      background-size: 200% auto;
      color: transparent;
      -webkit-background-clip: text;
      animation: goldShimmer 4s linear infinite;
    }

    .ken-burns {
      animation: kenBurns 25s ease-in-out infinite alternate;
    }

    .glow-pulse {
      animation: pulseGlow 2.5s infinite;
    }

    .feature-card {
      transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    }

    .feature-card:hover {
      transform: translateY(-8px);
    }
  </style>
</head>
<body class="bg-stone-50 text-stone-800 dark:bg-warmdark-900 dark:text-stone-100 font-sans transition-colors duration-300 relative">

  <!-- Floating One-Tap WhatsApp Button -->
  <a href="https://wa.me/8801890187776?text=Hello%20Green%20Forester!%20I%20would%20like%20to%20reserve%20a%20table%20or%20inquire%20about%20the%20menu." target="_blank" rel="noopener" class="fixed bottom-6 right-6 z-50 bg-emerald-600 hover:bg-emerald-500 text-white p-4 rounded-full shadow-2xl hover:scale-110 transition-all flex items-center justify-center gap-3 border-2 border-emerald-400 group" title="Chat on WhatsApp">
    <i class="fa-brands fa-whatsapp text-3xl"></i>
    <span class="max-w-0 overflow-hidden whitespace-nowrap group-hover:max-w-xs transition-all duration-300 ease-in-out text-sm font-bold pl-0 group-hover:pl-1">Quick Contact</span>
  </a>

  <!-- ================= HEADER / NAVBAR ================= -->
  <header class="fixed top-0 left-0 w-full z-50 transition-all duration-300 glass-nav border-b border-forest-500/20 dark:border-forest-900">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
      
      <!-- Brand Logo -->
      <a href="#" class="flex items-center gap-3 group">
        <div class="w-10 h-10 rounded-full bg-forest-600 flex items-center justify-center text-white shadow-lg shadow-forest-600/30 group-hover:scale-105 transition-transform">
          <i class="fa-solid fa-leaf text-xl"></i>
        </div>
        <span class="font-serif text-2xl font-bold tracking-tight text-forest-600 dark:text-forest-500">GREEN <span class="text-stone-800 dark:text-stone-100 font-normal">FORESTER</span></span>
      </a>

      <!-- Desktop Navigation Links -->
      <nav class="hidden md:flex items-center space-x-8 font-medium text-sm tracking-wide">
        <a href="#about" class="hover:text-forest-600 dark:hover:text-forest-500 transition-colors">OUR STORY</a>
        <a href="#chef" class="hover:text-forest-600 dark:hover:text-forest-500 transition-colors">OUR CHEF</a>
        <a href="#menu" class="hover:text-forest-600 dark:hover:text-forest-500 transition-colors">MENU</a>
        <a href="#specials" class="hover:text-forest-600 dark:hover:text-forest-500 transition-colors">SPECIALS</a>
        <a href="#reviews" class="hover:text-forest-600 dark:hover:text-forest-500 transition-colors">REVIEWS</a>
        <a href="#contact" class="hover:text-forest-600 dark:hover:text-forest-500 transition-colors">LOCATION</a>
      </nav>

      <!-- Header Action Buttons -->
      <div class="hidden md:flex items-center gap-4">
        <!-- Theme Toggle -->
        <button id="themeToggle" class="p-2.5 rounded-full bg-stone-200 dark:bg-warmdark-700 text-stone-700 dark:text-forest-400 hover:scale-110 transition-transform" title="Toggle Light/Dark Theme">
          <i class="fa-solid fa-moon dark:hidden"></i>
          <i class="fa-solid fa-sun hidden dark:inline"></i>
        </button>

        <!-- Cart Button -->
        <button id="openCartBtn" class="relative p-2.5 rounded-full bg-stone-200 dark:bg-warmdark-700 text-stone-800 dark:text-stone-100 hover:scale-110 transition-transform">
          <i class="fa-solid fa-utensils"></i>
          <span id="cartBadge" class="absolute -top-1 -right-1 bg-forest-600 text-white text-xs font-bold w-5 h-5 rounded-full flex items-center justify-center hidden">0</span>
        </button>

        <!-- Direct WhatsApp Call CTA -->
        <a href="tel:01890187776" class="px-5 py-2.5 rounded-full bg-forest-600 hover:bg-forest-700 text-white font-semibold text-sm shadow-md shadow-forest-600/20 hover:shadow-lg transition-all transform hover:-translate-y-0.5 flex items-center gap-2">
          <i class="fa-solid fa-phone"></i> 01890187776
        </a>
      </div>

      <!-- Mobile Controls -->
      <div class="flex items-center gap-2 md:hidden">
        <button id="mobileCartBtn" class="relative p-2 rounded-lg bg-stone-200 dark:bg-warmdark-700 text-stone-800 dark:text-stone-100">
          <i class="fa-solid fa-utensils"></i>
          <span id="mobileCartBadge" class="absolute -top-1 -right-1 bg-forest-600 text-white text-xs font-bold w-4 h-4 rounded-full flex items-center justify-center hidden">0</span>
        </button>
        <button id="themeToggleMobile" class="p-2 rounded-lg bg-stone-200 dark:bg-warmdark-700 text-stone-800 dark:text-forest-400">
          <i class="fa-solid fa-moon dark:hidden"></i>
          <i class="fa-solid fa-sun hidden dark:inline"></i>
        </button>
        <button id="mobileMenuBtn" class="p-2 rounded-lg bg-stone-200 dark:bg-warmdark-700 text-stone-800 dark:text-stone-100">
          <i class="fa-solid fa-bars text-xl"></i>
        </button>
      </div>

    </div>

    <!-- Mobile Dropdown Navigation -->
    <div id="mobileMenu" class="hidden md:hidden bg-stone-100 dark:bg-warmdark-800 border-b border-stone-200 dark:border-stone-700 px-4 pt-2 pb-6 space-y-3">
      <a href="#about" class="block py-2 text-stone-700 dark:text-stone-200 font-medium hover:text-forest-600">Our Story</a>
      <a href="#chef" class="block py-2 text-stone-700 dark:text-stone-200 font-medium hover:text-forest-600">Our Chef</a>
      <a href="#menu" class="block py-2 text-stone-700 dark:text-stone-200 font-medium hover:text-forest-600">Menu</a>
      <a href="#specials" class="block py-2 text-stone-700 dark:text-stone-200 font-medium hover:text-forest-600">Specials</a>
      <a href="#reviews" class="block py-2 text-stone-700 dark:text-stone-200 font-medium hover:text-forest-600">Reviews</a>
      <a href="#contact" class="block py-2 text-stone-700 dark:text-stone-200 font-medium hover:text-forest-600">Location & Hours</a>
      <a href="https://wa.me/8801890187776" class="block w-full text-center py-3 bg-forest-600 text-white rounded-xl font-semibold shadow-md">
        <i class="fa-brands fa-whatsapp"></i> Chat on WhatsApp (01890187776)
      </a>
    </div>
  </header>

  <!-- ================= HERO SECTION ================= -->
  <section class="relative min-h-screen flex items-center justify-center pt-20 overflow-hidden">
    <!-- Hero Background Image & Gradient Overlay -->
    <div class="absolute inset-0 z-0 overflow-hidden">
      <img src="https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&q=80&w=2000" alt="Green Forester Interior" class="w-full h-full object-cover ken-burns opacity-70">
      <div class="absolute inset-0 bg-gradient-to-r from-warmdark-900/95 via-warmdark-900/80 to-warmdark-900/95"></div>
      
      <!-- Interactive Leaf Particle Canvas -->
      <canvas id="heroParticleCanvas" class="absolute inset-0 pointer-events-none z-10"></canvas>
    </div>

    <div class="relative z-20 max-w-5xl mx-auto px-4 text-center text-white py-24">
      <span class="inline-block px-4 py-1.5 rounded-full bg-forest-500/20 text-forest-400 border border-forest-500/30 text-sm font-semibold tracking-widest uppercase mb-6 animate-pulse">
        🌱 100% Organic & Farm Fresh
      </span>
      
      <h1 class="font-serif text-4xl sm:text-6xl lg:text-7xl font-bold tracking-tight mb-6 leading-tight anim-fade-up">
        An Unforgettable Journey of <br>
        <span class="shimmer-text italic">Exquisite Organic Flavors</span>
      </h1>
      
      <p class="max-w-2xl mx-auto text-stone-300 text-base sm:text-lg mb-10 leading-relaxed font-light anim-fade-up" style="animation-delay: 0.2s;">
        Welcome to <strong>Green Forester</strong>. Experience artisanal wood-fired dishes, locally harvested organic produce, and farm-to-table botanical recipes prepared with passion.
      </p>

      <!-- Action CTA Buttons -->
      <div class="flex flex-col sm:flex-row items-center justify-center gap-4 sm:gap-6 anim-fade-up" style="animation-delay: 0.4s;">
        <a href="#menu" class="w-full sm:w-auto px-8 py-4 rounded-full bg-forest-600 hover:bg-forest-700 text-white font-semibold text-lg shadow-xl shadow-forest-600/30 hover:scale-105 transition-all flex items-center justify-center gap-3 glow-pulse">
          <i class="fa-solid fa-book-open"></i> Explore Organic Menu
        </a>
        <a href="https://wa.me/8801890187776?text=Hello%20Green%20Forester!%20I'd%20like%20to%20book%20a%20table." target="_blank" rel="noopener" class="w-full sm:w-auto px-8 py-4 rounded-full bg-stone-800/80 hover:bg-stone-800 border border-forest-500/40 text-white font-semibold text-lg backdrop-blur-md hover:scale-105 transition-all flex items-center justify-center gap-3">
          <i class="fa-brands fa-whatsapp text-emerald-400"></i> Tap To Call / WhatsApp
        </a>
      </div>

      <!-- Quick Highlights Bar Template -->
      <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mt-16 pt-10 border-t border-forest-800/60 text-stone-300 anim-fade-up" style="animation-delay: 0.6s;">
        <div class="feature-card flex flex-col items-center p-3 rounded-xl bg-warmdark-800/40 border border-forest-900/50">
          <i class="fa-solid fa-seedling text-forest-400 text-2xl mb-2"></i>
          <span class="font-semibold text-white">Farm-To-Table</span>
          <span class="text-xs text-stone-400">100% Organic Ingredients</span>
        </div>
        <div class="feature-card flex flex-col items-center p-3 rounded-xl bg-warmdark-800/40 border border-forest-900/50">
          <i class="fa-solid fa-clock text-forest-400 text-2xl mb-2"></i>
          <span class="font-semibold text-white">7:00 AM - 11:00 PM</span>
          <span class="text-xs text-stone-400">Mon - Sat (Sunday Closed)</span>
        </div>
        <div class="feature-card flex flex-col items-center p-3 rounded-xl bg-warmdark-800/40 border border-forest-900/50">
          <i class="fa-solid fa-fire-burner text-forest-400 text-2xl mb-2"></i>
          <span class="font-semibold text-white">Wood-Fired Grill</span>
          <span class="text-xs text-stone-400">Authentic Organic Charcoal</span>
        </div>
        <div class="feature-card flex flex-col items-center p-3 rounded-xl bg-warmdark-800/40 border border-forest-900/50">
          <i class="fa-solid fa-user-chef text-forest-400 text-2xl mb-2"></i>
          <span class="font-semibold text-white">Master Chef</span>
          <span class="text-xs text-stone-400">Abdul Abbaj Ali (12 yrs exp)</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ================= ABOUT / OUR STORY ================= -->
  <section id="about" class="py-20 bg-stone-100 dark:bg-warmdark-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-16 items-center">
        
        <!-- Image Grid -->
        <div class="grid grid-cols-2 gap-4 relative">
          <div class="space-y-4">
            <img src="https://images.unsplash.com/photo-1555396273-367ea4eb4db5?auto=format&fit=crop&q=80&w=800" alt="Chef preparing dish" class="rounded-2xl shadow-lg object-cover h-64 w-full transform hover:scale-105 transition-transform duration-300">
            <img src="https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&q=80&w=800" alt="Plated steak dish" class="rounded-2xl shadow-lg object-cover h-48 w-full transform hover:scale-105 transition-transform duration-300">
          </div>
          <div class="space-y-4 pt-8">
            <img src="https://images.unsplash.com/photo-1510812431401-41d2bd2722f3?auto=format&fit=crop&q=80&w=800" alt="Cocktails" class="rounded-2xl shadow-lg object-cover h-48 w-full transform hover:scale-105 transition-transform duration-300">
            <img src="https://images.unsplash.com/photo-1550966871-3ed3cdb5ed0c?auto=format&fit=crop&q=80&w=800" alt="Restaurant atmosphere" class="rounded-2xl shadow-lg object-cover h-64 w-full transform hover:scale-105 transition-transform duration-300">
          </div>
          <!-- Decorative Badge -->
          <div class="absolute inset-0 flex items-center justify-center pointer-events-none">
            <div class="bg-forest-600 text-white font-serif font-bold p-6 rounded-full shadow-2xl text-center w-36 h-36 flex flex-col justify-center items-center border-4 border-stone-100 dark:border-warmdark-800">
              <span class="text-2xl font-sans">100%</span>
              <span class="text-xs tracking-wider uppercase font-sans">Organic & Fresh</span>
            </div>
          </div>
        </div>

        <!-- Story Content -->
        <div class="space-y-6">
          <span class="text-forest-600 dark:text-forest-400 font-semibold uppercase tracking-widest text-sm">Our Philosophy</span>
          <h2 class="font-serif text-3xl sm:text-4xl font-bold tracking-tight text-stone-900 dark:text-white">
            Welcome to Green Forester
          </h2>
          <p class="text-stone-600 dark:text-stone-300 leading-relaxed">
            At Green Forester, we believe that dining should be a celebration of nature's purity. Our kitchen works directly with organic farms to source fresh, chemical-free ingredients every single day.
          </p>
          <p class="text-stone-600 dark:text-stone-300 leading-relaxed">
            From our signature wood-fired specials to handcrafted herbal beverages, every item on our menu is designed to nourish your body and delight your palate.
          </p>

          <div class="p-4 rounded-xl bg-forest-500/10 border border-forest-500/20 text-stone-800 dark:text-stone-200">
            <h4 class="font-bold flex items-center gap-2 text-forest-700 dark:text-forest-400">
              <i class="fa-solid fa-circle-info"></i> Operating Hours & Off Day
            </h4>
            <p class="text-sm mt-1">Open Monday to Saturday: <strong>7:00 AM – 11:00 PM</strong></p>
            <p class="text-sm text-red-500 dark:text-red-400 font-semibold mt-1">Weekly Off Day: Sunday (Closed)</p>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ================= EXECUTIVE CHEF SPOTLIGHT ================= -->
  <section id="chef" class="py-20 bg-stone-50 dark:bg-warmdark-900 border-t border-b border-stone-200 dark:border-warmdark-700">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        
        <!-- Chef Profile Details -->
        <div class="space-y-6">
          <span class="text-forest-600 dark:text-forest-400 font-semibold uppercase tracking-widest text-sm">Culinary Mastery</span>
          <h2 class="font-serif text-3xl sm:text-5xl font-bold text-stone-900 dark:text-white">Meet Executive Chef Abdul Abbaj Ali</h2>
          <p class="text-stone-600 dark:text-stone-300 text-lg leading-relaxed">
            With over <strong>12 years of rich culinary experience</strong> in fine dining and organic gastronomy, Chef Abdul Abbaj Ali brings extraordinary flair and dedication to Green Forester.
          </p>
          <p class="text-stone-600 dark:text-stone-300 leading-relaxed">
            Chef Abdul specializes in fusing traditional wood-fire grilling techniques with modern organic flavor profiles, creating balanced, aromatic, and unforgettable meals.
          </p>

          <div class="grid grid-cols-2 gap-4 pt-4">
            <div class="p-4 rounded-xl bg-white dark:bg-warmdark-800 shadow-md border border-stone-200 dark:border-stone-700">
              <span class="text-3xl font-bold text-forest-600 dark:text-forest-400 font-serif">12+</span>
              <span class="block text-xs text-stone-500 dark:text-stone-400 uppercase font-semibold">Years Experience</span>
            </div>
            <div class="p-4 rounded-xl bg-white dark:bg-warmdark-800 shadow-md border border-stone-200 dark:border-stone-700">
              <span class="text-3xl font-bold text-forest-600 dark:text-forest-400 font-serif">100%</span>
              <span class="block text-xs text-stone-500 dark:text-stone-400 uppercase font-semibold">Organic Recipes</span>
            </div>
          </div>
        </div>

        <!-- Chef Visual -->
        <div class="relative">
          <img src="https://images.unsplash.com/photo-1577219491135-ce391730fb2c?auto=format&fit=crop&q=80&w=1000" alt="Chef Abdul Abbaj Ali" class="rounded-3xl shadow-2xl border-4 border-forest-600/30 object-cover h-[450px] w-full">
          <div class="absolute bottom-6 left-6 right-6 p-6 rounded-2xl bg-warmdark-900/90 backdrop-blur-md text-white border border-forest-500/30">
            <h3 class="font-serif text-xl font-bold">Abdul Abbaj Ali</h3>
            <p class="text-xs text-forest-400 uppercase font-semibold">Executive Head Chef & Organic Specialist</p>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ================= INTERACTIVE DIGITAL MENU ================= -->
  <section id="menu" class="py-20 bg-stone-100 dark:bg-warmdark-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <!-- Section Header -->
      <div class="text-center max-w-3xl mx-auto mb-12">
        <span class="text-forest-600 dark:text-forest-400 font-semibold uppercase tracking-widest text-sm">Taste The Goodness</span>
        <h2 class="font-serif text-3xl sm:text-5xl font-bold text-stone-900 dark:text-white mt-2">Our Organic Menu</h2>
        <p class="text-stone-600 dark:text-stone-400 mt-4">Handcrafted by Chef Abdul Abbaj Ali. Select any item to create your custom tasting order.</p>
      </div>

      <!-- Filter Tabs -->
      <div class="flex flex-wrap items-center justify-center gap-3 mb-12">
        <button class="menu-tab active px-6 py-2.5 rounded-full font-medium text-sm transition-all bg-forest-600 text-white shadow-md shadow-forest-600/30" data-category="all">
          All Dishes
        </button>
        <button class="menu-tab px-6 py-2.5 rounded-full font-medium text-sm transition-all bg-stone-200 dark:bg-warmdark-700 text-stone-700 dark:text-stone-300 hover:bg-forest-600 hover:text-white" data-category="appetizers">
          Organic Starters
        </button>
        <button class="menu-tab px-6 py-2.5 rounded-full font-medium text-sm transition-all bg-stone-200 dark:bg-warmdark-700 text-stone-700 dark:text-stone-300 hover:bg-forest-600 hover:text-white" data-category="mains">
          Wood-Fired Mains
        </button>
        <button class="menu-tab px-6 py-2.5 rounded-full font-medium text-sm transition-all bg-stone-200 dark:bg-warmdark-700 text-stone-700 dark:text-stone-300 hover:bg-forest-600 hover:text-white" data-category="desserts">
          Natural Desserts
        </button>
        <button class="menu-tab px-6 py-2.5 rounded-full font-medium text-sm transition-all bg-stone-200 dark:bg-warmdark-700 text-stone-700 dark:text-stone-300 hover:bg-forest-600 hover:text-white" data-category="drinks">
          Herbal Drinks
        </button>
      </div>

      <!-- Menu Grid -->
      <div id="menuContainer" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Dynamic JS Content -->
      </div>

    </div>
  </section>

  <!-- ================= CHEF'S SPECIAL ================= -->
  <section id="specials" class="py-16 bg-forest-800 text-white relative overflow-hidden">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <div class="space-y-6">
          <span class="bg-white/20 px-4 py-1 rounded-full text-xs font-semibold uppercase tracking-widest">Signature Dish</span>
          <h2 class="font-serif text-3xl sm:text-5xl font-bold leading-tight">Chef Abdul's Wood-Fired Herb Lamb Chops</h2>
          <p class="text-forest-100 text-lg leading-relaxed">
            Marinated for 24 hours in fresh garden rosemary, garlic, and wild organic honey, slow-roasted over oak embers to tender perfection.
          </p>
          <div class="flex items-center gap-6 pt-2">
            <div>
              <span class="text-3xl font-serif font-bold">$38</span>
              <span class="text-forest-200 text-sm block">Fresh Daily Batch</span>
            </div>
            <a href="https://wa.me/8801890187776?text=I%20want%20to%20order%20Chef%20Abdul's%20Wood-Fired%20Herb%20Lamb%20Chops" target="_blank" class="px-6 py-3 rounded-full bg-white text-forest-900 font-bold hover:bg-forest-100 transition-colors shadow-lg flex items-center gap-2">
              <i class="fa-brands fa-whatsapp text-emerald-600"></i> Order via WhatsApp
            </a>
          </div>
        </div>
        <div class="relative">
          <img src="https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&q=80&w=1000" alt="Wood-Fired Lamb Chops" class="rounded-3xl shadow-2xl border-4 border-white/20 w-full object-cover h-96">
        </div>
      </div>
    </div>
  </section>

  <!-- ================= CUSTOMER REVIEWS & ADD REVIEW TOOL ================= -->
  <section id="reviews" class="py-20 bg-stone-50 dark:bg-warmdark-900">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="flex flex-col md:flex-row md:items-end justify-between mb-12 gap-6">
        <div>
          <span class="text-forest-600 dark:text-forest-400 font-semibold uppercase tracking-widest text-sm">Guest Feedback</span>
          <h2 class="font-serif text-3xl sm:text-5xl font-bold text-stone-900 dark:text-white mt-2">What Our Customers Say</h2>
        </div>
        
        <!-- Add Review Trigger Button -->
        <button id="openReviewModalBtn" class="px-6 py-3 rounded-full bg-forest-600 hover:bg-forest-700 text-white font-bold text-sm shadow-lg shadow-forest-600/30 flex items-center gap-2 self-start md:self-auto">
          <i class="fa-solid fa-pen-to-square"></i> Add Your Review
        </button>
      </div>

      <!-- Dynamic Reviews Grid -->
      <div id="reviewsContainer" class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- JS populates reviews here -->
      </div>

    </div>
  </section>

  <!-- ================= LOCATION & CONTACT ================= -->
  <section id="contact" class="py-20 bg-stone-100 dark:bg-warmdark-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        
        <!-- Contact Details -->
        <div class="space-y-8">
          <div>
            <span class="text-forest-600 dark:text-forest-400 font-semibold uppercase tracking-widest text-sm">Visit Green Forester</span>
            <h2 class="font-serif text-3xl sm:text-4xl font-bold text-stone-900 dark:text-white mt-1">Location & Schedule</h2>
          </div>

          <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
            <!-- Contact Box 1 -->
            <div class="bg-white dark:bg-warmdark-900 p-6 rounded-2xl shadow-md border border-stone-200 dark:border-stone-700">
              <i class="fa-solid fa-phone text-forest-600 text-2xl mb-3"></i>
              <h3 class="font-bold text-stone-900 dark:text-white text-lg mb-1">Direct Call / WhatsApp</h3>
              <p class="text-stone-600 dark:text-stone-400 text-sm leading-relaxed">
                Tel: <strong>01890187776</strong><br>
                WhatsApp: <strong>01890187776</strong>
              </p>
            </div>

            <!-- Contact Box 2 -->
            <div class="bg-white dark:bg-warmdark-900 p-6 rounded-2xl shadow-md border border-stone-200 dark:border-stone-700">
              <i class="fa-solid fa-location-dot text-forest-600 text-2xl mb-3"></i>
              <h3 class="font-bold text-stone-900 dark:text-white text-lg mb-1">Our Address</h3>
              <p class="text-stone-600 dark:text-stone-400 text-sm leading-relaxed">
                Green Forester Restaurant<br>
                12 Organic Avenue, Nature Zone
              </p>
            </div>
          </div>

          <!-- Schedule Table -->
          <div class="bg-white dark:bg-warmdark-900 p-6 rounded-2xl shadow-md border border-stone-200 dark:border-stone-700">
            <h3 class="font-bold text-stone-900 dark:text-white text-lg mb-4 flex items-center gap-2">
              <i class="fa-solid fa-clock text-forest-600"></i> Operating Hours
            </h3>
            <div class="space-y-3 text-sm">
              <div class="flex justify-between pb-2 border-b border-stone-100 dark:border-stone-800">
                <span class="text-stone-600 dark:text-stone-400">Monday – Saturday</span>
                <span class="font-bold text-forest-600 dark:text-forest-400">7:00 AM – 11:00 PM</span>
              </div>
              <div class="flex justify-between">
                <span class="text-stone-600 dark:text-stone-400">Sunday</span>
                <span class="font-bold text-red-500">OFF DAY (CLOSED)</span>
              </div>
            </div>
          </div>

        </div>

        <!-- Visual Map Placeholder -->
        <div class="h-96 rounded-3xl overflow-hidden shadow-2xl relative border border-stone-200 dark:border-stone-700">
          <img src="https://images.unsplash.com/photo-1526778548025-fa2f459cd5c1?auto=format&fit=crop&q=80&w=1000" alt="Map Location" class="w-full h-full object-cover">
          <div class="absolute inset-0 bg-warmdark-900/40 flex items-center justify-center">
            <a href="https://wa.me/8801890187776" target="_blank" class="px-6 py-3 bg-white text-stone-900 font-bold rounded-full shadow-lg hover:bg-forest-600 hover:text-white transition-all flex items-center gap-2">
              <i class="fa-brands fa-whatsapp text-emerald-600"></i> Get Directions via WhatsApp
            </a>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ================= FOOTER ================= -->
  <footer class="bg-warmdark-900 text-stone-400 py-16 border-t border-forest-900">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-10 mb-12">
        
        <div class="space-y-4">
          <span class="font-serif text-2xl font-bold tracking-tight text-forest-500">GREEN <span class="text-white font-normal">FORESTER</span></span>
          <p class="text-sm text-stone-400 leading-relaxed">Pure organic dining prepared by Executive Chef Abdul Abbaj Ali.</p>
          <p class="text-sm font-semibold text-stone-300"><i class="fa-solid fa-phone text-forest-400"></i> 01890187776</p>
        </div>

        <div>
          <h4 class="text-white font-bold mb-4">Quick Links</h4>
          <ul class="space-y-2 text-sm">
            <li><a href="#about" class="hover:text-forest-400">Our Story</a></li>
            <li><a href="#chef" class="hover:text-forest-400">Chef Profile</a></li>
            <li><a href="#menu" class="hover:text-forest-400">Organic Menu</a></li>
            <li><a href="#reviews" class="hover:text-forest-400">Customer Reviews</a></li>
          </ul>
        </div>

        <div>
          <h4 class="text-white font-bold mb-4">Timings</h4>
          <p class="text-sm">Mon - Sat: 7:00 AM - 11:00 PM</p>
          <p class="text-sm text-red-400 font-semibold mt-1">Sunday: OFF DAY</p>
        </div>

      </div>

      <div class="pt-8 border-t border-warmdark-700 text-xs text-center text-stone-500">
        <p>&copy; 2026 Green Forester Restaurant. All rights reserved.</p>
      </div>
    </div>
  </footer>

  <!-- ================= ADD REVIEW MODAL TOOL ================= -->
  <div id="reviewModal" class="fixed inset-0 z-50 hidden bg-black/70 backdrop-blur-sm flex items-center justify-center p-4">
    <div class="bg-white dark:bg-warmdark-800 max-w-lg w-full rounded-3xl p-8 shadow-2xl border border-stone-200 dark:border-stone-700 relative">
      <button id="closeReviewModalBtn" class="absolute top-6 right-6 text-stone-400 hover:text-stone-900 dark:hover:text-white text-xl">
        <i class="fa-solid fa-xmark"></i>
      </button>

      <h3 class="font-serif text-2xl font-bold text-stone-900 dark:text-white mb-2">Write a Review</h3>
      <p class="text-sm text-stone-500 dark:text-stone-400 mb-6">Share your dining experience at Green Forester.</p>

      <form id="addReviewForm" class="space-y-4">
        <div>
          <label class="block text-sm font-medium text-stone-700 dark:text-stone-300 mb-1">Your Name</label>
          <input type="text" id="reviewerName" required placeholder="John Doe" class="w-full px-4 py-2.5 rounded-xl border border-stone-300 dark:border-warmdark-700 bg-stone-50 dark:bg-warmdark-900 text-stone-900 dark:text-white">
        </div>

        <div>
          <label class="block text-sm font-medium text-stone-700 dark:text-stone-300 mb-1">Star Rating</label>
          <select id="reviewerRating" class="w-full px-4 py-2.5 rounded-xl border border-stone-300 dark:border-warmdark-700 bg-stone-50 dark:bg-warmdark-900 text-stone-900 dark:text-white">
            <option value="5">⭐⭐⭐⭐⭐ (5/5) Excellent</option>
            <option value="4">⭐⭐⭐⭐ (4/5) Very Good</option>
            <option value="3">⭐⭐⭐ (3/5) Good</option>
          </select>
        </div>

        <div>
          <label class="block text-sm font-medium text-stone-700 dark:text-stone-300 mb-1">Your Review</label>
          <textarea id="reviewerText" rows="3" required placeholder="The food and organic vibe were amazing..." class="w-full px-4 py-2.5 rounded-xl border border-stone-300 dark:border-warmdark-700 bg-stone-50 dark:bg-warmdark-900 text-stone-900 dark:text-white"></textarea>
        </div>

        <button type="submit" class="w-full py-3 rounded-xl bg-forest-600 hover:bg-forest-700 text-white font-bold transition-all">
          Submit Review
        </button>
      </form>
    </div>
  </div>

  <!-- ================= TASTING ORDER DRAWER ================= -->
  <div id="cartModal" class="fixed inset-0 z-50 hidden bg-black/60 backdrop-blur-sm flex justify-end">
    <div class="w-full max-w-md bg-white dark:bg-warmdark-900 h-full p-6 flex flex-col justify-between shadow-2xl">
      <div>
        <div class="flex justify-between items-center pb-4 border-b border-stone-200 dark:border-stone-800">
          <h3 class="font-serif text-2xl font-bold text-stone-900 dark:text-white">Your Selection</h3>
          <button id="closeCartBtn" class="text-stone-500 hover:text-stone-900 dark:hover:text-white text-xl">
            <i class="fa-solid fa-xmark"></i>
          </button>
        </div>

        <div id="cartItemsList" class="py-6 space-y-4 max-h-[60vh] overflow-y-auto"></div>
      </div>

      <div class="border-t border-stone-200 dark:border-stone-800 pt-4 space-y-4">
        <div class="flex justify-between text-lg font-bold text-stone-900 dark:text-white">
          <span>Total:</span>
          <span id="cartTotal">$0.00</span>
        </div>
        <button id="checkoutBtn" class="w-full py-3.5 rounded-xl bg-forest-600 hover:bg-forest-700 text-white font-bold text-center transition-all flex items-center justify-center gap-2">
          <i class="fa-brands fa-whatsapp"></i> Confirm Order via WhatsApp
        </button>
      </div>
    </div>
  </div>

  <!-- ================= JAVASCRIPT LOGIC ================= -->
  <script>
    // --- Sample Menu Data ---
    const menuData = [
      { id: '1', name: 'Organic Garden Salad', category: 'appetizers', price: 16, desc: 'Fresh organic greens, cherry tomatoes, cucumbers with lemon-basil vinaigrette.', image: 'https://images.unsplash.com/photo-1592417817098-8f3d6ef23a28?auto=format&fit=crop&q=80&w=600', badge: '100% Organic' },
      { id: '2', name: 'Wood-Fired Herb Lamb Chops', category: 'mains', price: 38, desc: 'Chef Abdul’s signature dish marinated in organic herbs and honey.', image: 'https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&q=80&w=600', badge: 'Chef Special' },
      { id: '3', name: 'Charcoal Grilled Salmon', category: 'mains', price: 34, desc: 'Wild-caught salmon served over saffron organic quinoa and steamed asparagus.', image: 'https://images.unsplash.com/photo-1519708227418-c8fd9a32b7a2?auto=format&fit=crop&q=80&w=600' },
      { id: '4', name: 'Wild Mushroom Pasta', category: 'mains', price: 28, desc: 'Handcrafted tagliatelle with wild forest mushrooms and garlic truffle glaze.', image: 'https://images.unsplash.com/photo-1621996346565-e3d5d6281358?auto=format&fit=crop&q=80&w=600', badge: 'Vegetarian' },
      { id: '5', name: 'Organic Berry Tart', category: 'desserts', price: 14, desc: 'Made with wild forest berries and organic coconut cream.', image: 'https://images.unsplash.com/photo-1519869325930-281384150729?auto=format&fit=crop&q=80&w=600' },
      { id: '6', name: 'Fresh Mint & Cucumber Cooler', category: 'drinks', price: 8, desc: 'Refreshing organic drink crushed with wild mint and fresh lime.', image: 'https://images.unsplash.com/photo-1514362545857-3bc16c4c7d1b?auto=format&fit=crop&q=80&w=600', badge: 'Popular' }
    ];

    // Initial Reviews Data
    let reviewsData = [
      { name: "Sophia Martinez", text: "Chef Abdul Abbaj Ali's lamb chops were unbelievable! Fresh organic taste.", rating: 5 },
      { name: "Tanvir Hossain", text: "Great atmosphere and super easy to order via WhatsApp at 01890187776.", rating: 5 },
      { name: "Emily Roberts", text: "Love the green organic vibe! The salad and herbal drinks were amazing.", rating: 5 }
    ];

    let cart = [];

    // Render Reviews
    function renderReviews() {
      const container = document.getElementById('reviewsContainer');
      container.innerHTML = reviewsData.map(r => `
        <div class="bg-white dark:bg-warmdark-800 p-6 rounded-2xl shadow-lg border border-stone-200 dark:border-stone-700/50 flex flex-col justify-between">
          <div class="space-y-3">
            <div class="flex text-amber-500 gap-1 text-sm">
              ${'★'.repeat(r.rating)}
            </div>
            <p class="text-stone-600 dark:text-stone-300 italic text-sm">"${r.text}"</p>
          </div>
          <div class="mt-4 pt-3 border-t border-stone-100 dark:border-stone-700/50 flex items-center gap-3">
            <div class="w-9 h-9 rounded-full bg-forest-600 text-white font-bold flex items-center justify-center text-sm">
              ${r.name.charAt(0)}
            </div>
            <div>
              <h4 class="font-bold text-stone-900 dark:text-white text-sm">${r.name}</h4>
              <span class="text-xs text-stone-500">Verified Guest</span>
            </div>
          </div>
        </div>
      `).join('');
    }

    // Render Menu Items
    function renderMenu(filterCategory = 'all') {
      const container = document.getElementById('menuContainer');
      container.innerHTML = '';

      const filtered = filterCategory === 'all' 
        ? menuData 
        : menuData.filter(item => item.category === filterCategory);

      filtered.forEach(item => {
        const card = document.createElement('div');
        card.className = 'bg-white dark:bg-warmdark-800 rounded-2xl overflow-hidden shadow-lg border border-stone-200 dark:border-stone-700/50 hover:shadow-2xl transition-all duration-300 flex flex-col justify-between group';
        
        card.innerHTML = `
          <div>
            <div class="relative overflow-hidden h-52">
              <img src="${item.image}" alt="${item.name}" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
              ${item.badge ? `<span class="absolute top-3 right-3 bg-forest-600 text-white text-xs font-bold px-3 py-1 rounded-full shadow-md">${item.badge}</span>` : ''}
            </div>
            <div class="p-6">
              <div class="flex justify-between items-start mb-2">
                <h3 class="font-serif text-xl font-bold text-stone-900 dark:text-white">${item.name}</h3>
                <span class="text-forest-600 dark:text-forest-400 font-bold text-lg">$${item.price}</span>
              </div>
              <p class="text-stone-600 dark:text-stone-400 text-sm leading-relaxed mb-4">${item.desc}</p>
            </div>
          </div>
          <div class="px-6 pb-6 pt-0">
            <button onclick="addToCart('${item.id}')" class="w-full py-2.5 rounded-xl border-2 border-forest-600 text-forest-600 dark:text-forest-400 hover:bg-forest-600 hover:text-white font-semibold text-sm transition-all flex items-center justify-center gap-2">
              <i class="fa-solid fa-plus"></i> Add to Selection
            </button>
          </div>
        `;
        container.appendChild(card);
      });
    }

    // Cart System
    window.addToCart = function(id) {
      const item = menuData.find(i => i.id === id);
      const existing = cart.find(i => i.id === id);
      if (existing) {
        existing.qty += 1;
      } else {
        cart.push({ ...item, qty: 1 });
      }
      updateCartUI();
      document.getElementById('cartModal').classList.remove('hidden');
    };

    function updateCartUI() {
      const totalCount = cart.reduce((sum, item) => sum + item.qty, 0);
      const totalPrice = cart.reduce((sum, item) => sum + (item.price * item.qty), 0);

      document.getElementById('cartBadge').innerText = totalCount;
      document.getElementById('mobileCartBadge').innerText = totalCount;
      document.getElementById('cartBadge').classList.toggle('hidden', totalCount === 0);
      document.getElementById('mobileCartBadge').classList.toggle('hidden', totalCount === 0);

      document.getElementById('cartTotal').innerText = `$${totalPrice.toFixed(2)}`;

      const cartList = document.getElementById('cartItemsList');
      if (cart.length === 0) {
        cartList.innerHTML = `<p class="text-stone-500 text-center py-8">Your selection is empty.</p>`;
      } else {
        cartList.innerHTML = cart.map(item => `
          <div class="flex items-center justify-between p-3 bg-stone-100 dark:bg-warmdark-800 rounded-xl">
            <div>
              <h4 class="font-bold text-stone-900 dark:text-white text-sm">${item.name}</h4>
              <span class="text-xs text-forest-600 font-semibold">$${item.price} x ${item.qty}</span>
            </div>
            <div class="flex items-center gap-2">
              <button onclick="changeQty('${item.id}', -1)" class="w-6 h-6 rounded bg-stone-200 dark:bg-warmdark-700 text-xs font-bold">-</button>
              <span class="text-sm font-semibold">${item.qty}</span>
              <button onclick="changeQty('${item.id}', 1)" class="w-6 h-6 rounded bg-stone-200 dark:bg-warmdark-700 text-xs font-bold">+</button>
            </div>
          </div>
        `).join('');
      }
    }

    window.changeQty = function(id, delta) {
      const index = cart.findIndex(i => i.id === id);
      if (index > -1) {
        cart[index].qty += delta;
        if (cart[index].qty <= 0) cart.splice(index, 1);
      }
      updateCartUI();
    };

    // Review Modal Events
    const reviewModal = document.getElementById('reviewModal');
    document.getElementById('openReviewModalBtn').addEventListener('click', () => reviewModal.classList.remove('hidden'));
    document.getElementById('closeReviewModalBtn').addEventListener('click', () => reviewModal.classList.add('hidden'));

    document.getElementById('addReviewForm').addEventListener('submit', (e) => {
      e.preventDefault();
      const name = document.getElementById('reviewerName').value;
      const rating = parseInt(document.getElementById('reviewerRating').value);
      const text = document.getElementById('reviewerText').value;

      reviewsData.unshift({ name, text, rating });
      renderReviews();
      reviewModal.classList.add('hidden');
      e.target.reset();
    });

    // Theme & Mobile Menu Toggles
    document.getElementById('themeToggle').addEventListener('click', () => document.documentElement.classList.toggle('dark'));
    document.getElementById('themeToggleMobile').addEventListener('click', () => document.documentElement.classList.toggle('dark'));
    document.getElementById('mobileMenuBtn').addEventListener('click', () => document.getElementById('mobileMenu').classList.toggle('hidden'));
    
    document.getElementById('openCartBtn').addEventListener('click', () => document.getElementById('cartModal').classList.remove('hidden'));
    document.getElementById('mobileCartBtn').addEventListener('click', () => document.getElementById('cartModal').classList.remove('hidden'));
    document.getElementById('closeCartBtn').addEventListener('click', () => document.getElementById('cartModal').classList.add('hidden'));

    // WhatsApp Checkout Redirect
    document.getElementById('checkoutBtn').addEventListener('click', () => {
      if(cart.length === 0) {
        alert('Please add items to your selection!');
        return;
      }
      const orderText = cart.map(i => `- ${i.name} (${i.qty}x)`).join('%0A');
      window.open(`https://wa.me/8801890187776?text=Hello%20Green%20Forester!%20I'd%20like%20to%20order:%0A${orderText}`, '_blank');
    });

    // Particle Canvas Animation
    const canvas = document.getElementById('heroParticleCanvas');
    const ctx = canvas.getContext('2d');
    let particles = [];

    function resizeCanvas() {
      canvas.width = canvas.parentElement.clientWidth;
      canvas.height = canvas.parentElement.clientHeight;
    }
    window.addEventListener('resize', resizeCanvas);
    resizeCanvas();

    for(let i=0; i<35; i++) {
      particles.push({
        x: Math.random() * canvas.width,
        y: Math.random() * canvas.height,
        r: Math.random() * 3 + 1,
        sy: Math.random() * 0.8 + 0.2,
        sx: Math.sin(Math.random()) * 0.5
      });
    }

    function drawParticles() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      ctx.fillStyle = 'rgba(74, 222, 128, 0.4)';
      particles.forEach(p => {
        ctx.beginPath();
        ctx.arc(p.x, p.y, p.r, 0, Math.PI*2);
        ctx.fill();
        p.y -= p.sy;
        p.x += p.sx;
        if(p.y < 0) p.y = canvas.height;
      });
      requestAnimationFrame(drawParticles);
    }
    drawParticles();

    // Init
    renderMenu();
    renderReviews();
  </script>
</body>
</html>