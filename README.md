# Gugukula-```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gurukula Hub - Your All-in-One Student & Living Ecosystem</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/js/all.min.js"></script>
    <style>
        body { font-family: 'Inter', sans-serif; }
        .hero-gradient { background: linear-gradient(135deg, #4f46e5 0%, #312e81 100%); }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 antialiased flex flex-col min-h-screen">

    <header class="sticky top-0 z-50 bg-white/90 backdrop-blur-md border-b border-slate-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16 items-center">
                <div class="flex items-center space-x-3 cursor-pointer" onclick="switchTab('home')">
                    <div class="w-10 h-10 rounded-xl bg-indigo-600 flex items-center justify-center text-white font-bold text-xl shadow-md">
                        <i class="fa-solid fa-graduation-cap"></i>
                    </div>
                    <span class="text-xl font-bold bg-gradient-to-r from-indigo-600 to-violet-800 bg-clip-text text-transparent">Gurukula Hub</span>
                </div>
                <nav class="hidden md:flex space-x-1 lg:space-x-4 text-sm font-medium">
                    <button onclick="switchTab('home')" class="nav-btn px-3 py-2 rounded-lg text-indigo-600 font-semibold hover:bg-indigo-50 transition">Home</button>
                    <button onclick="switchTab('coaching')" class="nav-btn px-3 py-2 rounded-lg text-slate-600 hover:bg-slate-100 transition">Coaching</button>
                    <button onclick="switchTab('accommodation')" class="nav-btn px-3 py-2 rounded-lg text-slate-600 hover:bg-slate-100 transition">PG & Hostels</button>
                    <button onclick="switchTab('rooms')" class="nav-btn px-3 py-2 rounded-lg text-slate-600 hover:bg-slate-100 transition">Rent Rooms</button>
                    <button onclick="switchTab('ride')" class="nav-btn px-3 py-2 rounded-lg text-slate-600 hover:bg-slate-100 transition">Ride Berry</button>
                    <button onclick="switchTab('mess')" class="nav-btn px-3 py-2 rounded-lg text-slate-600 hover:bg-slate-100 transition">Mess</button>
                    <button onclick="switchTab('stationery')" class="nav-btn px-3 py-2 rounded-lg text-slate-600 hover:bg-slate-100 transition">Stationery</button>
                </nav>
                <div class="flex items-center space-x-3">
                    <button onclick="openModal('contactModal')" class="bg-indigo-600 hover:bg-indigo-700 text-white px-4 py-2 rounded-xl text-sm font-medium shadow-sm transition">List Service</button>
                    <button id="mobileMenuBtn" class="md:hidden p-2 text-slate-600 hover:text-indigo-600 focus:outline-none"><i class="fa-solid fa-bars text-xl"></i></button>
                </div>
            </div>
        </div>
        <!-- Mobile Dropdown Menu -->
        <div id="mobileMenu" class="hidden md:hidden bg-white border-b border-slate-200 px-4 pt-2 pb-4 space-y-1">
            <button onclick="switchTab('home'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded-md font-medium text-indigo-600">Home</button>
            <button onclick="switchTab('coaching'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded-md font-medium text-slate-600">Coaching Hub</button>
            <button onclick="switchTab('accommodation'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded-md font-medium text-slate-600">PG & Hostel</button>
            <button onclick="switchTab('rooms'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded-md font-medium text-slate-600">Rent Room</button>
            <button onclick="switchTab('ride'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded-md font-medium text-slate-600">Ride Berry</button>
            <button onclick="switchTab('mess'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded-md font-medium text-slate-600">Mess Services</button>
            <button onclick="switchTab('stationery'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded-md font-medium text-slate-600">Stationery Hub</button>
        </div>
    </header>

    <main class="flex-grow">

        <!-- TAB: HOME -->
        <section id="tab-home" class="tab-content">
            <div class="hero-gradient text-white py-20 px-4 sm:px-6 lg:px-8 text-center relative overflow-hidden">
                <div class="absolute inset-0 opacity-10 bg-[radial-gradient(#fff_1px,transparent_1px)] [background-size:16px_16px]"></div>
                <div class="max-w-3xl mx-auto relative z-10">
                    <span class="inline-block bg-indigo-500/30 border border-indigo-400/30 text-indigo-100 text-xs font-semibold px-3 py-1 rounded-full mb-6 uppercase tracking-wider">Welcome to Gurukula Hub</span>
                    <h1 class="text-4xl sm:text-5xl font-extrabold tracking-tight mb-6">Everything a Student Needs, Under One Roof</h1>
                    <p class="text-lg text-indigo-100 mb-8">Discover top-rated coaching institutes, comfortable PGs and hostels, rental rooms, mess services, ride-sharing, and stationery hubs effortlessly.</p>
                    <div class="flex flex-wrap justify-center gap-4">
                        <button onclick="switchTab('coaching')" class="bg-white text-indigo-600 hover:bg-indigo-50 font-semibold px-6 py-3 rounded-xl shadow-lg transition">Explore Coaching</button>
                        <button onclick="switchTab('accommodation')" class="bg-indigo-700 hover:bg-indigo-800 text-white font-semibold px-6 py-3 rounded-xl border border-indigo-500 shadow-lg transition">Find Accommodation</button>
                    </div>
                </div>
            </div>

            <!-- Quick Service Grid -->
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
                <div class="text-center mb-12">
                    <h2 class="text-2xl sm:text-3xl font-bold text-slate-900">Explore Our Core Services</h2>
                    <p class="text-slate-600 mt-2">Click on any category to browse verified listings and student deals.</p>
                </div>
                <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
                    <div onclick="switchTab('coaching')" class="bg-white p-6 rounded-2xl border border-slate-200 hover:border-indigo-500 hover:shadow-xl transition cursor-pointer text-center group">
                        <div class="w-14 h-14 bg-indigo-50 group-hover:bg-indigo-600 text-indigo-600 group-hover:text-white rounded-2xl flex items-center justify-center mx-auto mb-4 text-2xl transition shadow-sm">
                            <i class="fa-solid fa-chalkboard-user"></i>
                        </div>
                        <h3 class="font-bold text-slate-800">Coaching Hub</h3>
                        <p class="text-xs text-slate-500 mt-1">Top rated institutes & test series</p>
                    </div>
                    <div onclick="switchTab('accommodation')" class="bg-white p-6 rounded-2xl border border-slate-200 hover:border-indigo-500 hover:shadow-xl transition cursor-pointer text-center group">
                        <div class="w-14 h-14 bg-emerald-50 group-hover:bg-emerald-600 text-emerald-600 group-hover:text-white rounded-2xl flex items-center justify-center mx-auto mb-4 text-2xl transition shadow-sm">
                            <i class="fa-solid fa-building"></i>
                        </div>
                        <h3 class="font-bold text-slate-800">PG & Hostel</h3>
                        <p class="text-xs text-slate-500 mt-1">Safe & affordable stay</p>
                    </div>
                    <div onclick="switchTab('rooms')" class="bg-white p-6 rounded-2xl border border-slate-200 hover:border-indigo-500 hover:shadow-xl transition cursor-pointer text-center group">
                        <div class="w-14 h-14 bg-amber-50 group-hover:bg-amber-600 text-amber-600 group-hover:text-white rounded-2xl flex items-center justify-center mx-auto mb-4 text-2xl transition shadow-sm">
                            <i class="fa-solid fa-house-chimney"></i>
                        </div>
                        <h3 class="font-bold text-slate-800">Rent Room</h3>
                        <p class="text-xs text-slate-500 mt-1">Independent student flats</p>
                    </div>
                    <div onclick="switchTab('ride')" class="bg-white p-6 rounded-2xl border border-slate-200 hover:border-indigo-500 hover:shadow-xl transition cursor-pointer text-center group">
                        <div class="w-14 h-14 bg-blue-50 group-hover:bg-blue-600 text-blue-600 group-hover:text-white rounded-2xl flex items-center justify-center mx-auto mb-4 text-2xl transition shadow-sm">
                            <i class="fa-solid fa-bicycle"></i>
                        </div>
                        <h3 class="font-bold text-slate-800">Ride Berry</h3>
                        <p class="text-xs text-slate-500 mt-1">Eco-friendly student carpool</p>
                    </div>
                    <div onclick="switchTab('mess')" class="bg-white p-6 rounded-2xl border border-slate-200 hover:border-indigo-500 hover:shadow-xl transition cursor-pointer text-center group">
                        <div class="w-14 h-14 bg-rose-50 group-hover:bg-rose-600 text-rose-600 group-hover:text-white rounded-2xl flex items-center justify-center mx-auto mb-4 text-2xl transition shadow-sm">
                            <i class="fa-solid fa-utensils"></i>
                        </div>
                        <h3 class="font-bold text-slate-800">Mess Services</h3>
                        <p class="text-xs text-slate-500 mt-1">Hygienic & healthy meals</p>
                    </div>
                    <div onclick="switchTab('stationery')" class="bg-white p-6 rounded-2xl border border-slate-200 hover:border-indigo-500 hover:shadow-xl transition cursor-pointer text-center group">
                        <div class="w-14 h-14 bg-purple-50 group-hover:bg-purple-600 text-purple-600 group-hover:text-white rounded-2xl flex items-center justify-center mx-auto mb-4 text-2xl transition shadow-sm">
                            <i class="fa-solid fa-book"></i>
                        </div>
                        <h3 class="font-bold text-slate-800">Stationery Hub</h3>
                        <p class="text-xs text-slate-500 mt-1">Books, notes & printing</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- TAB: COACHING HUB -->
        <section id="tab-coaching" class="tab-content hidden max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-8 gap-4">
                <div>
                    <h2 class="text-3xl font-bold text-slate-900">Coaching Hub</h2>
                    <p class="text-slate-600 mt-1">Discover top-rated institutes for competitive exams and academic excellence.</p>
                </div>
                <div class="flex gap-2">
                    <select id="coachingFilter" onchange="filterCoaching()" class="bg-white border border-slate-300 rounded-xl px-4 py-2 text-sm focus:outline-none focus:ring-2 focus:ring-indigo-500">
                        <option value="all">All Categories</option>
                        <option value="JEE/NEET">JEE / NEET</option>
                        <option value="UPSC">UPSC / Civil Services</option>
                        <option value="Foundation">Foundation & School</option>
                    </select>
                </div>
            </div>
            <div id="coachingGrid" class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Dynamically populated or static cards -->
                <div class="bg-white border border-slate-200 rounded-2xl p-6 shadow-sm hover:shadow-md transition" data-category="JEE/NEET">
                    <div class="flex justify-between items-start mb-4">
                        <span class="bg-indigo-100 text-indigo-700 text-xs font-semibold px-2.5 py-1 rounded-full">JEE/NEET</span>
                        <div class="flex items-center text-amber-500 text-sm font-bold"><i class="fa-solid fa-star mr-1"></i> 4.8</div>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-2">Apex Science Academy</h3>
                    <p class="text-slate-600 text-sm mb-4">Specialized coaching for IIT-JEE and NEET with expert faculty and weekly test series.</p>
                    <div class="flex items-center text-xs text-slate-500 mb-4"><i class="fa-solid fa-location-dot mr-2 text-indigo-600"></i> Main Road, Study District</div>
                    <button onclick="openInquiry('Apex Science Academy')" class="w-full bg-indigo-50 text-indigo-600 hover:bg-indigo-600 hover:text-white font-medium py-2 rounded-xl transition text-sm">Enroll / Inquire</button>
                </div>
                <div class="bg-white border border-slate-200 rounded-2xl p-6 shadow-sm hover:shadow-md transition" data-category="UPSC">
                    <div class="flex justify-between items-start mb-4">
                        <span class="bg-violet-100 text-violet-700 text-xs font-semibold px-2.5 py-1 rounded-full">UPSC</span>
                        <div class="flex items-center text-amber-500 text-sm font-bold"><i class="fa-solid fa-star mr-1"></i> 4.9</div>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-2">Civil servants IAS Hub</h3>
                    <p class="text-slate-600 text-sm mb-4">Comprehensive guidance, answer writing practice, and mentorship for civil service aspirants.</p>
                    <div class="flex items-center text-xs text-slate-500 mb-4"><i class="fa-solid fa-location-dot mr-2 text-indigo-600"></i> Library Square, Knowledge Park</div>
                    <button onclick="openInquiry('Civil servants IAS Hub')" class="w-full bg-indigo-50 text-indigo-600 hover:bg-indigo-600 hover:text-white font-medium py-2 rounded-xl transition text-sm">Enroll / Inquire</button>
                </div>
                <div class="bg-white border border-slate-200 rounded-2xl p-6 shadow-sm hover:shadow-md transition" data-category="Foundation">
                    <div class="flex justify-between items-start mb-4">
                        <span class="bg-emerald-100 text-emerald-700 text-xs font-semibold px-2.5 py-1 rounded-full">Foundation</span>
                        <div class="flex items-center text-amber-500 text-sm font-bold"><i class="fa-solid fa-star mr-1"></i> 4.7</div>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-2">Scholar's Point Tuition</h3>
                    <p class="text-slate-600 text-sm mb-4">Dedicated board exam prep and conceptual clarity for grades 9th to 12th students.</p>
                    <div class="flex items-center text-xs text-slate-500 mb-4"><i class="fa-solid fa-location-dot mr-2 text-indigo-600"></i> College Lane, Campus Zone</div>
                    <button onclick="openInquiry('Scholar\'s Point Tuition')" class="w-full bg-indigo-50 text-indigo-600 hover:bg-indigo-600 hover:text-white font-medium py-2 rounded-xl transition text-sm">Enroll / Inquire</button>
                </div>
            </div>
        </section>

        <!-- TAB: ACCOMMODATION (PG & HOSTEL) -->
        <section id="tab-accommodation" class="tab-content hidden max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="mb-8">
                <h2 class="text-3xl font-bold text-slate-900">PG & Hostels</h2>
                <p class="text-slate-600 mt-1">Safe, comfortable, and fully furnished accommodation options with Wi-Fi and mess facilities.</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="bg-white border border-slate-200 rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition">
                    <img src="https://placehold.co/600x300/4f46e5/ffffff?text=Modern+PG" alt="PG" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <div class="flex justify-between items-center mb-2">
                            <h3 class="text-xl font-bold text-slate-900">Greenwood Boys PG</h3>
                            <span class="text-indigo-600 font-bold">₹6,500<span class="text-xs text-slate-500">/mo</span></span>
                        </div>
                        <p class="text-slate-600 text-sm mb-4">Single & Double sharing rooms with 3-time meals, Wi-Fi, and 24/7 power backup.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-slate-100 text-slate-600 text-xs px-2.5 py-1 rounded-md">Wi-Fi</span>
                            <span class="bg-slate-100 text-slate-600 text-xs px-2.5 py-1 rounded-md">Food Included</span>
                            <span class="bg-slate-100 text-slate-600 text-xs px-2.5 py-1 rounded-md">AC / Non-AC</span>
                        </div>
                        <button onclick="openInquiry('Greenwood Boys PG')" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-medium py-2 rounded-xl transition text-sm">Book Visit</button>
                    </div>
                </div>
                <div class="bg-white border border-slate-200 rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition">
                    <img src="https://placehold.co/600x300/10b981/ffffff?text=Girls+Hostel" alt="Hostel" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <div class="flex justify-between items-center mb-2">
                            <h3 class="text-xl font-bold text-slate-900">Starlight Girls Hostel</h3>
                            <span class="text-indigo-600 font-bold">₹7,000<span class="text-xs text-slate-500">/mo</span></span>
                        </div>
                        <p class="text-slate-600 text-sm mb-4">Secure campus with strict security, CCTV surveillance, nutritious mess, and study rooms.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-slate-100 text-slate-600 text-xs px-2.5 py-1 rounded-md">Security</span>
                            <span class="bg-slate-100 text-slate-600 text-xs px-2.5 py-1 rounded-md">Mess</span>
                            <span class="bg-slate-100 text-slate-600 text-xs px-2.5 py-1 rounded-md">Laundry</span>
                        </div>
                        <button onclick="openInquiry('Starlight Girls Hostel')" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-medium py-2 rounded-xl transition text-sm">Book Visit</button>
                    </div>
                </div>
                <div class="bg-white border border-slate-200 rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition">
                    <img src="https://placehold.co/600x300/f59e0b/ffffff?text=Executive+PG" alt="PG" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <div class="flex justify-between items-center mb-2">
                            <h3 class="text-xl font-bold text-slate-900">Elite Executive Living</h3>
                            <span class="text-indigo-600 font-bold">₹8,500<span class="text-xs text-slate-500">/mo</span></span>
                        </div>
                        <p class="text-slate-600 text-sm mb-4">Premium single rooms 