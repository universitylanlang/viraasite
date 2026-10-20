# viraasite
welcome to viracun
<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VIRACUN CPNS - Bimbel & Tryout CAT CPNS Terpercaya</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Inter & FontAwesome Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        navy: {
                            800: '#0B192C',
                            900: '#1E3E62',
                        },
                        gold: {
                            400: '#FFD700',
                            500: '#FFB800',
                            600: '#E6A100',
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        .gradient-bg {
            background: linear-gradient(135deg, #0B192C 0%, #1E3E62 100%);
        }
        .gold-gradient {
            background: linear-gradient(135deg, #FFD700 0%, #FFB800 100%);
        }
        .custom-shadow {
            box-shadow: 0 10px 30px -10px rgba(11, 25, 44, 0.15);
        }
    </style>
</head>
<body class="font-sans bg-slate-50 text-slate-800 antialiased selection:bg-gold-500 selection:text-navy-800">

    <!-- TOP ANNOUNCEMENT BAR WITH COUNTDOWN -->
    <div class="bg-navy-800 text-white text-xs md:text-sm py-2.5 px-4 text-center border-b border-slate-700/50 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto flex flex-wrap justify-center items-center gap-2 md:gap-4">
            <span class="inline-flex items-center gap-1.5 font-medium text-gold-400">
                <i class="fa-solid fa-fire-flame-curved animate-bounce"></i> PROMO GELOMBANG PERTAMA CPNS 2026:
            </span>
            <span>Diskon hingga 60% berakhir dalam:</span>
            <div id="countdown" class="font-bold font-mono text-gold-400 bg-navy-900 px-2 py-0.5 rounded border border-gold-500/30">
                <span id="hours">00</span>h : <span id="minutes">00</span>m : <span id="seconds">00</span>s
            </div>
            <a href="#paket" class="underline text-gold-400 hover:text-white font-semibold ml-2 transition">Klaim Promo Sekarang &rarr;</a>
        </div>
    </div>

    <!-- HEADER / NAVIGATION -->
    <header class="bg-white/90 backdrop-blur-md sticky top-[37px] z-40 border-b border-slate-100 shadow-sm transition-all duration-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <!-- Logo -->
                <a href="#" class="flex items-center gap-3 group">
                    <div class="w-10 h-10 rounded-xl bg-navy-800 flex items-center justify-center text-gold-400 font-extrabold text-xl shadow-md group-hover:scale-105 transition">
                        A
                    </div>
                    <div>
                        <span class="text-xl font-extrabold text-navy-800 tracking-tight block leading-none">VIRACUN</span>
                        <span class="text-[10px] font-bold text-gold-600 tracking-widest uppercase">Bimbel CPNS No.1</span>
                    </div>
                </a>

                <!-- Desktop Navigation Menu -->
                <nav class="hidden md:flex items-center gap-8 text-sm font-semibold text-slate-600">
                    <a href="#beranda" class="hover:text-navy-800 transition">Beranda</a>
                    <a href="#paket" class="hover:text-navy-800 transition">Paket Belajar</a>
                    <a href="#fitur" class="hover:text-navy-800 transition">Fitur Utama</a>
                    <a href="#cara-bayar" class="hover:text-navy-800 transition">Cara Bayar</a>
                    <a href="#testimoni" class="hover:text-navy-800 transition">Testimoni</a>
                    <a href="#faq" class="hover:text-navy-800 transition">FAQ</a>
                </nav>

                <!-- Header CTA Button -->
                <div class="hidden md:flex items-center gap-4">
                    <button onclick="openPaymentModal()" class="gold-gradient hover:opacity-95 text-navy-800 px-5 py-2.5 rounded-xl font-bold shadow-md hover:shadow-lg transition transform active:scale-95">
                        <i class="fa-solid fa-receipt mr-1.5"></i> Konfirmasi Bayar
                    </button>
                </div>

                <!-- Mobile Hamburger Button -->
                <button id="mobileMenuBtn" class="md:hidden p-2 rounded-lg text-slate-600 hover:text-navy-800 focus:outline-none">
                    <i class="fa-solid fa-bars text-2xl"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Navigation Menu Dropdown -->
        <div id="mobileMenu" class="hidden md:hidden bg-white border-b border-slate-200 px-4 pt-2 pb-6 space-y-3 shadow-xl">
            <a href="#beranda" class="mobile-link block py-2 text-slate-700 font-medium hover:text-navy-800">Beranda</a>
            <a href="#paket" class="mobile-link block py-2 text-slate-700 font-medium hover:text-navy-800">Paket Belajar</a>
            <a href="#fitur" class="mobile-link block py-2 text-slate-700 font-medium hover:text-navy-800">Fitur Utama</a>
            <a href="#cara-bayar" class="mobile-link block py-2 text-slate-700 font-medium hover:text-navy-800">Cara Bayar</a>
            <a href="#testimoni" class="mobile-link block py-2 text-slate-700 font-medium hover:text-navy-800">Testimoni</a>
            <a href="#faq" class="mobile-link block py-2 text-slate-700 font-medium hover:text-navy-800">FAQ</a>
            <div class="pt-2 flex flex-col gap-2">
                <button onclick="openPaymentModal()" class="w-full gold-gradient text-navy-800 py-3 rounded-xl font-bold text-center shadow">
                    Konfirmasi Pembayaran
                </button>
            </div>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section id="beranda" class="gradient-bg text-white pt-12 pb-20 md:py-24 relative overflow-hidden">
        <!-- Background Pattern Decor -->
        <div class="absolute inset-0 opacity-10 bg-[radial-gradient(#fff_1px,transparent_1px)] [background-size:16px_16px] pointer-events-none"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                
                <!-- Hero Text Content -->
                <div class="lg:col-span-7 space-y-6 text-center lg:text-left">
                    <div class="inline-flex items-center gap-2 bg-slate-800/80 border border-slate-700 px-3.5 py-1.5 rounded-full text-xs font-semibold text-gold-400 backdrop-blur-md">
                        <span class="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span> Persiapan Seleksi CPNS 2026 Terbaru
                    </div>
                    
                    <h1 class="text-3xl sm:text-5xl lg:text-6xl font-extrabold leading-tight tracking-tight">
                        Lolos CPNS 2026 Bersama <span class="text-transparent bg-clip-text bg-gradient-to-r from-gold-400 to-amber-300">Bimbel CPNS Terpercaya</span>
                    </h1>
                    
                    <p class="text-slate-300 text-base sm:text-lg max-w-2xl mx-auto lg:mx-0 leading-relaxed">
                        Tingkatkan peluang kelulusanmu hingga 94% dengan Sistem Belajar Terpadu: Tryout CAT Standar BKN, Bimbingan Mentoring Eksklusif, dan Pembahasan Soal Terlengkap!
                    </p>

                    <!-- Hero CTA Buttons -->
                    <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start pt-2">
                        <a href="#paket" class="gold-gradient text-navy-800 font-bold px-8 py-4 rounded-xl shadow-lg hover:shadow-amber-500/20 hover:scale-105 transition duration-200 text-center text-lg">
                            Daftar Sekarang <i class="fa-solid fa-arrow-right ml-2"></i>
                        </a>
                        <a href="#cara-bayar" class="bg-navy-900/80 hover:bg-navy-900 text-white font-semibold px-8 py-4 rounded-xl border border-slate-700 hover:border-slate-500 transition text-center text-lg flex items-center justify-center gap-2">
                            <i class="fa-solid fa-credit-card text-gold-400"></i> Info Pembayaran
                        </a>
                    </div>

                    <!-- Key Stats -->
                    <div class="pt-8 border-t border-slate-800 grid grid-cols-3 gap-4 text-center lg:text-left">
                        <div>
                            <p class="text-2xl sm:text-3xl font-extrabold text-gold-400">14.800+</p>
                            <p class="text-xs sm:text-sm text-slate-400">Alumni Lolos NIP</p>
                        </div>
                        <div>
                            <p class="text-2xl sm:text-3xl font-extrabold text-gold-400">98.4%</p>
                            <p class="text-xs sm:text-sm text-slate-400">Kepuasan Peserta</p>
                        </div>
                        <div>
                            <p class="text-2xl sm:text-3xl font-extrabold text-gold-400">50.000+</p>
                            <p class="text-xs sm:text-sm text-slate-400">Bank Soal CAT</p>
                        </div>
                    </div>
                </div>

                <!-- Hero Image & Interactive Card -->
                <div class="lg:col-span-5 relative">
                    <div class="relative mx-auto max-w-md lg:max-w-none">
                        <!-- Decorative Glow -->
                        <div class="absolute -inset-1 rounded-3xl bg-gradient-to-r from-gold-500 to-amber-500 blur-xl opacity-30 animate-pulse"></div>
                        
                        <div class="relative bg-navy-900 border border-slate-700 rounded-3xl p-6 shadow-2xl text-white">
                            <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=800&q=80" alt="Siswa Bimbel CPNS" class="w-full h-52 object-cover rounded-2xl mb-6 shadow-md">
                            
                            <div class="space-y-4">
                                <div class="flex items-center justify-between bg-navy-800/90 p-3 rounded-xl border border-slate-700/60">
                                    <div class="flex items-center gap-3">
                                        <div class="w-10 h-10 rounded-full bg-emerald-500/20 text-emerald-400 flex items-center justify-center font-bold">
                                            <i class="fa-solid fa-check text-lg"></i>
                                        </div>
                                        <div>
                                            <p class="text-xs text-slate-400">Update Terakhir</p>
                                            <p class="text-sm font-semibold text-slate-200">Kisi-Kisi Soal PermenPANRB Terbaru</p>
                                        </div>
                                    </div>
                                </div>

                                <div class="bg-navy-800/90 p-4 rounded-xl border border-slate-700/60 space-y-2">
                                    <div class="flex justify-between text-xs text-slate-300">
                                        <span>Sisa Kuota Pendaftaran Diskon</span>
                                        <span class="font-bold text-gold-400">Tersisa 12 Kursi Lagi!</span>
                                    </div>
                                    <div class="w-full bg-slate-700 rounded-full h-2 overflow-hidden">
                                        <div class="bg-gold-500 h-2 rounded-full w-[82%]"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- FITUR UNGGULAN -->
    <section id="fitur" class="py-20 bg-slate-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16 space-y-3">
                <h2 class="text-gold-600 font-bold uppercase tracking-wider text-sm">Keunggulan Program</h2>
                <p class="text-3xl sm:text-4xl font-extrabold text-navy-800">Mengapa Pilih elerasi CPNS?</p>
                <p class="text-slate-600">Fasilitas komprehensif yang dirancang khusus untuk memastikan Anda siap menghadapi ujian Sistem CAT BKN.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Feature 1 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-100 custom-shadow hover:-translate-y-1 transition duration-300">
                    <div class="w-14 h-14 bg-navy-800/5 text-navy-800 rounded-2xl flex items-center justify-center text-2xl mb-6">
                        <i class="fa-solid fa-laptop-code text-gold-600"></i>
                    </div>
                    <h3 class="text-xl font-bold text-navy-800 mb-3">Simulasi Tryout CAT BKN</h3>
                    <p class="text-slate-600 leading-relaxed text-sm">Sistem ujian persis CAT BKN lengkap dengan timer real-time, skor otomatis langsung keluar, dan grafik perkembangan nilai.</p>
                </div>

                <!-- Feature 2 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-100 custom-shadow hover:-translate-y-1 transition duration-300">
                    <div class="w-14 h-14 bg-navy-800/5 text-navy-800 rounded-2xl flex items-center justify-center text-2xl mb-6">
                        <i class="fa-solid fa-video text-gold-600"></i>
                    </div>
                    <h3 class="text-xl font-bold text-navy-800 mb-3">Kelas Interactive Zoom</h3>
                    <p class="text-slate-600 leading-relaxed text-sm">Belajar tatap muka secara online bersama Tutor PNS Senior/Master Trainer yang siap menjawab setiap pertanyaan secara langsung.</p>
                </div>

                <!-- Feature 3 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-100 custom-shadow hover:-translate-y-1 transition duration-300">
                    <div class="w-14 h-14 bg-navy-800/5 text-navy-800 rounded-2xl flex items-center justify-center text-2xl mb-6">
                        <i class="fa-solid fa-book-open text-gold-600"></i>
                    </div>
                    <h3 class="text-xl font-bold text-navy-800 mb-3">Ribuan Bank Soal & PDF</h3>
                    <p class="text-slate-600 leading-relaxed text-sm">es modul PDF ringkas, kunci jawaban rasional, serta trik cepat (Fast Method) menjawab soal TWK, TIU, dan TKP.</p>
                </div>

                <!-- Feature 4 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-100 custom-shadow hover:-translate-y-1 transition duration-300">
                    <div class="w-14 h-14 bg-navy-800/5 text-navy-800 rounded-2xl flex items-center justify-center text-2xl mb-6">
                        <i class="fa-solid fa-users text-gold-600"></i>
                    </div>
                    <h3 class="text-xl font-bold text-navy-800 mb-3">Grup Diskusi Telegram/WA</h3>
                    <p class="text-slate-600 leading-relaxed text-sm">Komunitas belajar aktif 24/7 bersama ribuan pejuang NIP dari seluruh Indonesia untuk saling berbagi informasi dan motivasi.</p>
                </div>

                <!-- Feature 5 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-100 custom-shadow hover:-translate-y-1 transition duration-300">
                    <div class="w-14 h-14 bg-navy-800/5 text-navy-800 rounded-2xl flex items-center justify-center text-2xl mb-6">
                        <i class="fa-solid fa-[#0B192C] fa-chart-line text-gold-600"></i>
                    </div>
                    <h3 class="text-xl font-bold text-navy-800 mb-3">Analisis Kelemahan Sub-materi</h3>
                    <p class="text-slate-600 leading-relaxed text-sm">Rapor statistik akurat yang mengidentifikasi materi mana yang perlu ditingkatkan secara spesifik (TWK, TIU, TKP).</p>
                </div>

                <!-- Feature 6 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-100 custom-shadow hover:-translate-y-1 transition duration-300">
                    <div class="w-14 h-14 bg-navy-800/5 text-navy-800 rounded-2xl flex items-center justify-center text-2xl mb-6">
                        <i class="fa-solid fa-clock-rotate-left text-gold-600"></i>
                    </div>
                    <h3 class="text-xl font-bold text-navy-800 mb-3">Akses Rekaman Seumur Hidup</h3>
                    <p class="text-slate-600 leading-relaxed text-sm">Ketinggalan kelas live? Tenang, seluruh rekaman webinar dan materi dapat diakses kapan saja hingga ujian CPNS usai.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- PAKET BELAJAR (PRICING PLANS) -->
    <section id="paket" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16 space-y-3">
                <h2 class="text-gold-600 font-bold uppercase tracking-wider text-sm">Pilihan Paket Investasi Masa Depan</h2>
                <p class="text-3xl sm:text-4xl font-extrabold text-navy-800">Paket Bimbingan Belajar CPNS</p>
                <p class="text-slate-600">Pilih paket yang paling sesuai dengan kebutuhan belajarmu. Sekali bayar tanpa biaya tersembunyi.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-stretch">
                
                <!-- Package 1: Basic -->
                <div class="bg-white rounded-3xl border border-slate-200 p-8 custom-shadow flex flex-col justify-between relative hover:border-navy-800 transition">
                    <div>
                        <span class="bg-slate-100 text-slate-700 text-xs font-bold uppercase tracking-wider px-3 py-1 rounded-full">BCA</span>
                        <h3 class="text-2xl font-bold text-navy-800 mt-4 mb-2">Paket SKD Basic</h3>
                        <p class="text-slate-500 text-sm mb-6">Cocok untuk kamu yang ingin fokus latihan soal & tryout mandiri.</p>
                        
                        <div class="mb-6">
                            <span class="text-slate-400 line-through text-sm">Rp 359.000</span>
                            <div class="flex items-baseline gap-1">
                                <span class="text-4xl font-extrabold text-navy-800">Rp 189.000</span>
                                <span class="text-slate-500 text-xs">/akses</span>
                            </div>
                        </div>

                        <hr class="border-slate-100 mb-6">

                        <ul class="space-y-3.5 text-sm text-slate-600 mb-8">
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-emerald-500 text-base"></i> 10x Paket Tryout CAT SKD Premium
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-emerald-500 text-base"></i> Pembahasan Soal Teks & Video
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-emerald-500 text-base"></i> Ranking Nasional & Grafik Nilai
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-emerald-500 text-base"></i> Modul Ringkasan SKD (PDF)
                            </li>
                            <li class="flex items-center gap-3 text-slate-400 line-through">
                                <i class="fa-solid fa-circle-xmark text-slate-300 text-base"></i> Kelas Live Zoom Interaktif
                            </li>
                            <li class="flex items-center gap-3 text-slate-400 line-through">
                                <i class="fa-solid fa-circle-xmark text-slate-300 text-base"></i> Group Mentoring Eksklusif
                            </li>
                        </ul>
                    </div>

                    <button onclick="selectPackage('Paket SKD Basic', '149000')" class="w-full bg-slate-100 hover:bg-navy-800 hover:text-white text-navy-800 font-bold py-3.5 rounded-xl transition duration-200">
                        Pilih Paket Basic
                    </button>
                </div>

                <!-- Package 2: Recommended / Premium -->
                <div class="bg-navy-800 text-white rounded-3xl border-2 border-gold-500 p-8 shadow-2xl flex flex-col justify-between relative transform lg:-translate-y-4">
                    <div class="absolute -top-4 left-1/2 -translate-x-1/2 gold-gradient text-navy-800 text-xs font-extrabold uppercase tracking-wider px-4 py-1.5 rounded-full shadow-md">
                        <i class="fa-solid fa-star mr-1"></i> Paling Populer & Terfavorit
                    </div>

                    <div>
                        <span class="bg-navy-900 text-gold-400 border border-gold-500/30 text-xs font-bold uppercase tracking-wider px-3 py-1 rounded-full">Lengkap</span>
                        <h3 class="text-2xl font-bold text-white mt-4 mb-2">Paket SKD+SKB Premium</h3>
                        <p class="text-slate-300 text-sm mb-6">Persiapan intensif dari nol hingga tahap SKB bersama mentor.</p>
                        
                        <div class="mb-6">
                            <span class="text-slate-400 line-through text-sm">Rp 699.000</span>
                            <div class="flex items-baseline gap-1">
                                <span class="text-4xl font-extrabold text-gold-400">Rp 359.000</span>
                                <span class="text-slate-300 text-xs">/akses</span>
                            </div>
                        </div>

                        <hr class="border-slate-700 mb-6">

                        <ul class="space-y-3.5 text-sm text-slate-200 mb-8">
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-gold-400 text-base"></i> 30x Paket Tryout CAT SKD + SKB
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-gold-400 text-base"></i> 16x Session Live Zoom Interaktif
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-gold-400 text-base"></i> Rekaman Kelas Bimbingan Unlimited
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-gold-400 text-base"></i> Grup Mentoring Telegram VIP
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-gold-400 text-base"></i> Trik Cepat Menjawab (Fast Method)
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-gold-400 text-base"></i> Garansi Update Materi Terbaru
                            </li>
                        </ul>
                    </div>

                    <button onclick="selectPackage('Paket SKD+SKB Premium', '000')" class="w-full gold-gradient hover:opacity-90 text-navy-800 font-bold py-3.5 rounded-xl shadow-lg transition duration-200">
                        Pilih Paket Premium
                    </button>
                </div>

                <!-- Package 3: Platinum -->
                <div class="bg-white rounded-3xl border border-slate-200 p-8 custom-shadow flex flex-col justify-between relative hover:border-navy-800 transition">
                    <div>
                        <span class="bg-slate-100 text-slate-700 text-xs font-bold uppercase tracking-wider px-3 py-1 rounded-full">Privat</span>
                        <h3 class="text-2xl font-bold text-navy-800 mt-4 mb-2">Paket Platinum Intensif</h3>
                        <p class="text-slate-500 text-sm mb-6">Bimbingan eksklusif dengan pendampingan personal hingga lulus.</p>
                        
                        <div class="mb-6">
                            <span class="text-slate-400 line-through text-sm">Rp 1.200.000</span>
                            <div class="flex items-baseline gap-1">
                                <span class="text-4xl font-extrabold text-navy-800">Rp 599.000</span>
                                <span class="text-slate-500 text-xs">/akses</span>
                            </div>
                        </div>

                        <hr class="border-slate-100 mb-6">

                        <ul class="space-y-3.5 text-sm text-slate-600 mb-8">
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-emerald-500 text-base"></i> Semua Fitur Paket Premium
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-emerald-500 text-base"></i> Konsultasi Personal 1-on-1 Mentoring
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-emerald-500 text-base"></i> Bimbingan Resume & DRH CASN
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-emerald-500 text-base"></i> Tryout Custom Bebas Akses
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-check text-emerald-500 text-base"></i> Garansi Bebas Konsultasi Kapan Saja
                            </li>
                        </ul>
                    </div>

                    <button onclick="selectPackage('Paket Platinum Intensif', '599000')" class="w-full bg-slate-100 hover:bg-navy-800 hover:text-white text-navy-800 font-bold py-3.5 rounded-xl transition duration-200">
                        Pilih Paket Platinum
                    </button>
                </div>

            </div>
        </div>
    </section>

    <!-- METODE & INFORMASI PEMBAYARAN TRANSFER REKENING -->
    <section id="cara-bayar" class="py-20 bg-slate-100 border-t border-b border-slate-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16 space-y-3">
                <h2 class="text-gold-600 font-bold uppercase tracking-wider text-sm">Kemudahan Transaksi</h2>
                <p class="text-3xl sm:text-4xl font-extrabold text-navy-800">Rekening Resmi Pembayaran</p>
                <p class="text-slate-600">Lakukan pembayaran melalui transfer ke salah satu rekening bank resmi kami di bawah ini. Bebas biaya admin tambahan.</p>
            </div>

            

                <!-- Bank BCA -->
                <div class="bg-white rounded-2xl p-6 border border-slate-200 custom-shadow space-y-4">
                    <div class="flex items-center justify-between">
                        <span class="text-xl font-black text-amber-600 tracking-wider">BCA</span>
                        <span class="text-xs bg-amber-50 text-amber-700 px-2.5 py-1 rounded-full font-bold">Bank Transfer</span>
                    </div>
                    <div>
                        <p class="text-xs text-slate-400">Nomor Rekening</p>
                        <p class="text-xl font-mono font-bold text-slate-800 tracking-wider" id="rek-BCA">8106272030</p>
                    </div>
                    <div>
                        <p class="text-xs text-slate-400">Atas Nama</p>
                        <p class="text-sm font-semibold text-slate-700">MUHAMAD RAIHAN GIVARI</p>
                    </div>
                    <button onclick="copyToClipboard('rek-mandiri')" class="w-full bg-slate-50 hover:bg-navy-800 hover:text-white border border-slate-200 text-slate-700 font-semibold py-2 rounded-xl text-sm transition flex items-center justify-center gap-2">
                        <i class="fa-regular fa-copy"></i> Salin No. Rekening
                    </button>
                </div>

                

            <!-- Steps for Payment -->
            <div class="bg-white rounded-2xl p-8 border border-slate-200 custom-shadow">
                <h3 class="text-lg font-bold text-navy-800 mb-6 flex items-center gap-2">
                    <i class="fa-solid fa-list-check text-gold-600"></i> Alur Pendaftaran & Pembayaran:
                </h3>
                <div class="grid grid-cols-1 md:grid-cols-4 gap-6 relative">
                    <div class="space-y-2">
                        <div class="w-8 h-8 rounded-full bg-navy-800 text-gold-400 font-bold flex items-center justify-center text-sm">1</div>
                        <h4 class="font-bold text-slate-800">Pilih Paket</h4>
                        <p class="text-xs text-slate-500">Pilih paket bimbingan yang sesuai dengan kebutuhan persiapan CPNS-mu.</p>
                    </div>
                    <div class="space-y-2">
                        <div class="w-8 h-8 rounded-full bg-navy-800 text-gold-400 font-bold flex items-center justify-center text-sm">2</div>
                        <h4 class="font-bold text-slate-800">Transfer Biaya</h4>
                        <p class="text-xs text-slate-500">Transfer nominal biaya ke salah satu rekening bank resmi yang tertera di atas.</p>
                    </div>
                    <div class="space-y-2">
                        <div class="w-8 h-8 rounded-full bg-navy-800 text-gold-400 font-bold flex items-center justify-center text-sm">3</div>
                        <h4 class="font-bold text-slate-800">Upload Bukti</h4>
                        <p class="text-xs text-slate-500">Isi formulir konfirmasi pembayaran dan sertakan foto/screenshot bukti transfer.</p>
                    </div>
                    <div class="space-y-2">
                        <div class="w-8 h-8 rounded-full bg-navy-800 text-gold-400 font-bold flex items-center justify-center text-sm">4</div>
                        <h4 class="font-bold text-slate-800">Aktivasi Akun</h4>
                        <p class="text-xs text-slate-500">Tim admin akan mengkonfirmasi pembayaran dan mengaktifkan akunmu maksimal 15 menit.</p>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- TESTIMONI -->
    <section id="testimoni" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16 space-y-3">
                <h2 class="text-gold-600 font-bold uppercase tracking-wider text-sm">Kisah Sukses</h2>
                <p class="text-3xl sm:text-4xl font-extrabold text-navy-800">Kata Alumni Lolos CPNS</p>
                <p class="text-slate-600">Dengar langsung pengalaman belajar mereka hingga berhasil meraih NIP CPNS.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Testi 1 -->
                <div class="bg-slate-50 p-6 rounded-2xl border border-slate-100 flex flex-col justify-between">
                    <div class="space-y-4">
                        <div class="flex text-amber-400 gap-1 text-sm">
                            <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-slate-600 text-sm italic">"Metode pembelajaran di VIRACUN CPNS sangat to the point. Trik cepat matematika TIU terbukti menghemat waktu saat tes sesungguhnya!"</p>
                    </div>
                    <div class="flex items-center gap-3 mt-6 pt-4 border-t border-slate-200/60">
                        <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=100&q=80" alt="Avatar Alumni" class="w-11 h-11 rounded-full object-cover">
                        <div>
                            <p class="font-bold text-navy-800 text-sm">Rina Wulandari, S.Pd</p>
                            <p class="text-xs text-slate-500">Lolos CPNS Kemendikbud 2024</p>
                        </div>
                    </div>
                </div>

                <!-- Testi 2 -->
                <div class="bg-slate-50 p-6 rounded-2xl border border-slate-100 flex flex-col justify-between">
                    <div class="space-y-4">
                        <div class="flex text-amber-400 gap-1 text-sm">
                            <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-slate-600 text-sm italic">"Tryout CAT-nya persis banget sama tampilan komputer pas tes BKN asli. Jadi gak grogi lagi waktu pengerjaan SKD."</p>
                    </div>
                    <div class="flex items-center gap-3 mt-6 pt-4 border-t border-slate-200/60">
                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&w=100&q=80" alt="Avatar Alumni" class="w-11 h-11 rounded-full object-cover">
                        <div>
                            <p class="font-bold text-navy-800 text-sm">Budi Pratama, S.T</p>
                            <p class="text-xs text-slate-500">Lolos CPNS Kemenkeu 2024</p>
                        </div>
                    </div>
                </div>

                <!-- Testi 3 -->
                <div class="bg-slate-50 p-6 rounded-2xl border border-slate-100 flex flex-col justify-between">
                    <div class="space-y-4">
                        <div class="flex text-amber-400 gap-1 text-sm">
                            <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-slate-600 text-sm italic">"Sangat worth it ambil Paket Premium! Rekaman kelas Zoom-nya bisa diputar berulang kali kalau ada materi TKP yang kurang dipahami."</p>
                    </div>
                    <div class="flex items-center gap-3 mt-6 pt-4 border-t border-slate-200/60">
                        <img src="https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=100&q=80" alt="Avatar Alumni" class="w-11 h-11 rounded-full object-cover">
                        <div>
                            <p class="font-bold text-navy-800 text-sm">Siti Rahmawati, S.Kep</p>
                            <p class="text-xs text-slate-500">Lolos CPNS Kemenkes 2024</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ (ACCORDION) -->
    <section id="faq" class="py-20 bg-slate-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 space-y-3">
                <h2 class="text-gold-600 font-bold uppercase tracking-wider text-sm">Punya Pertanyaan?</h2>
                <p class="text-3xl sm:text-4xl font-extrabold text-navy-800">Sering Ditanyakan (FAQ)</p>
            </div>

            <div class="space-y-4">
                <!-- Item 1 -->
                <div class="border border-slate-200 bg-white rounded-2xl overflow-hidden custom-shadow">
                    <button onclick="toggleFaq(this)" class="w-full p-5 text-left font-bold text-navy-800 flex justify-between items-center gap-4 hover:bg-slate-50 transition">
                        <span>Bagaimana cara mengkonfirmasi pembayaran transfer bank?</span>
                        <i class="fa-solid fa-chevron-down text-slate-400 transition-transform duration-200"></i>
                    </button>
                    <div class="px-5 pb-5 hidden text-sm text-slate-600 leading-relaxed border-t border-slate-100 pt-3">
                        Setelah melakukan transfer ke salah satu rekening bank resmi kami , silakan klik tombol <strong>'Konfirmasi Bayar'</strong> di bagian menu atas website ini atau tombol konfirmasi setelah memilih paket. Isikan data pendaftaran serta lampirkan foto bukti transfer. Tim kami akan memverifikasinya.
                    </div>
                </div>

                <!-- Item 2 -->
                <div class="border border-slate-200 bg-white rounded-2xl overflow-hidden custom-shadow">
                    <button onclick="toggleFaq(this)" class="w-full p-5 text-left font-bold text-navy-800 flex justify-between items-center gap-4 hover:bg-slate-50 transition">
                        <span>Berapa lama akun saya diaktifkan setelah konfirmasi pembayaran?</span>
                        <i class="fa-solid fa-chevron-down text-slate-400 transition-transform duration-200"></i>
                    </button>
                    <div class="px-5 pb-5 hidden text-sm text-slate-600 leading-relaxed border-t border-slate-100 pt-3">
                        Proses aktivasi akun dilakukan secara otomatis/semi-otomatis oleh tim admin. Maksimal dalam kurun waktu <strong>5 - 15 menit</strong> setelah bukti transfer diverifikasi, link login dan grup VIP akan dikirimkan via WhatsApp & Email Anda.
                    </div>
                </div>

                <!-- Item 3 -->
                <div class="border border-slate-200 bg-white rounded-2xl overflow-hidden custom-shadow">
                    <button onclick="toggleFaq(this)" class="w-full p-5 text-left font-bold text-navy-800 flex justify-between items-center gap-4 hover:bg-slate-50 transition">
                        <span>Apakah materi dan tryout disesuaikan dengan kisi-kisi CPNS 2026 terbaru?</span>
                        <i class="fa-solid fa-chevron-down text-slate-400 transition-transform duration-200"></i>
                    </button>
                    <div class="px-5 pb-5 hidden text-sm text-slate-600 leading-relaxed border-t border-slate-100 pt-3">
                        Ya, 100% materi, tipe soal TWK, TIU, TKP, dan standar bobot penilaian disesuaikan dengan Peraturan MenPAN-RB terbaru & FR (Field Report) ujian CPNS tahun terakhir.
                    </div>
                </div>

                <!-- Item 4 -->
                <div class="border border-slate-200 bg-white rounded-2xl overflow-hidden custom-shadow">
                    <button onclick="toggleFaq(this)" class="w-full p-5 text-left font-bold text-navy-800 flex justify-between items-center gap-4 hover:bg-slate-50 transition">
                        <span>Bagaimana jika saya tidak bisa mengikuti kelas Live Zoom?</span>
                        <i class="fa-solid fa-chevron-down text-slate-400 transition-transform duration-200"></i>
                    </button>
                    <div class="px-5 pb-5 hidden text-sm text-slate-600 leading-relaxed border-t border-slate-100 pt-3">
                        Seluruh sesi pertemuan Live Zoom akan direkam HD dan diunggah ke dashboard akun peserta paling lambat 24 jam setelah sesi selesai. Anda bisa menonton ulang tanpa batas waktu.
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA BANNER -->
    <section class="py-16 gradient-bg text-white relative overflow-hidden">
        <div class="max-w-5xl mx-auto px-4 text-center space-y-6 relative z-10">
            <h2 class="text-3xl sm:text-5xl font-extrabold tracking-tight">Siap Wujudkan Impian Menjadi ASN Tahun Ini?</h2>
            <p class="text-slate-300 max-w-2xl mx-auto text-base sm:text-lg">Jangan menunda persiapanmu. Kuota bimbingan belajar dengan diskon terbatas untuk setiap gelombangnya.</p>
            <div class="pt-4">
                <a href="#paket" class="gold-gradient text-navy-800 font-extrabold px-10 py-4 rounded-xl shadow-xl hover:scale-105 transition inline-block text-lg">
                    Ambil Promo Sekarang
                </a>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-navy-800 text-slate-400 py-12 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-4 gap-8">
            <div class="space-y-4 md:col-span-1">
                <div class="flex items-center gap-2 text-white font-bold text-xl">
                    <div class="w-8 h-8 rounded-lg bg-gold-500 text-navy-800 flex items-center justify-center font-extrabold text-lg">A</div>
                    AKSELERASI CPNS
                </div>
                <p class="text-xs leading-relaxed">Platform bimbingan belajar persiapan tes CPNS & PPPK No. 1 di Indonesia dengan simulasi CAT BKN terakurat.</p>
            </div>

            <div>
                <h4 class="text-white font-semibold text-sm mb-4">Navigasi</h4>
                <ul class="space-y-2 text-xs">
                    <li><a href="#beranda" class="hover:text-gold-400 transition">Beranda</a></li>
                    <li><a href="#paket" class="hover:text-gold-400 transition">Paket Belajar</a></li>
                    <li><a href="#fitur" class="hover:text-gold-400 transition">Fitur Utama</a></li>
                    <li><a href="#cara-bayar" class="hover:text-gold-400 transition">Rekening Resmi</a></li>
                </ul>
            </div>

            <div>
                <h4 class="text-white font-semibold text-sm mb-4">Kontak Admin</h4>
                <ul class="space-y-2 text-xs">
                    <li class="flex items-center gap-2"><i class="fa-brands fa-whatsapp text-emerald-400"></i> +62 858-4669-6670</li>
                    <li class="flex items-center gap-2"><i class="fa-regular fa-envelope text-gold-400"></i> bantuan@VIRACUN.id</li>
                    <li class="flex items-center gap-2"><i class="fa-solid fa-location-dot text-rose-400"></i> Jakarta Selatan, Indonesia</li>
                </ul>
            </div>

            <div>
                <h4 class="text-white font-semibold text-sm mb-4">Keamanan Transaksi</h4>
                <p class="text-xs leading-relaxed mb-3">Seluruh transaksi hanya dialihkan ke nomor rekening resmi atas nama <strong>PT AKSELERATION EDUKASI INDONESIA</strong>.</p>
                <div class="flex gap-2 text-xl text-slate-300">
                    <i class="fa-solid fa-shield-halved text-gold-400"></i> Terverifikasi Legal
                </div>
            </div>
        </div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-12 pt-6 border-t border-slate-800 text-center text-xs">
            <p>&copy; 2026 Akselerasi CPNS. All rights reserved.</p>
        </div>
    </footer>

    <!-- MODAL FORM KONFIRMASI PEMBAYARAN TRANSFER -->
    <div id="paymentModal" class="fixed inset-0 bg-navy-800/80 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-white rounded-3xl max-w-xl w-full p-6 sm:p-8 custom-shadow my-8 relative animate-fadeIn">
            <!-- Close Modal Button -->
            <button onclick="closePaymentModal()" class="absolute top-6 right-6 text-slate-400 hover:text-slate-600 transition">
                <i class="fa-solid fa-xmark text-xl"></i>
            </button>

            <div class="mb-6">
                <h3 class="text-2xl font-bold text-navy-800">Konfirmasi Pembayaran</h3>
                <p class="text-xs text-slate-500">Lengkapi formulir di bawah ini setelah melakukan transfer rekening bank.</p>
            </div>

            <form id="paymentForm" onsubmit="handleFormSubmit(event)" class="space-y-4">
                <!-- Pilih Paket -->
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Paket Belajar Yang Dipilih</label>
                    <select id="modalPaket" class="w-full px-4 py-3 rounded-xl border border-slate-300 text-sm focus:ring-2 focus:ring-navy-800 focus:outline-none" required>
                        <option value="">-- Pilih Paket Belajar --</option>
                        <option value="Paket SKD Basic">Paket SKD Basic - Rp 189.000</option>
                        <option value="Paket SKD+SKB Premium">Paket SKD+SKB Premium - Rp 359.000</option>
                        <option value="Paket Platinum Intensif">Paket Platinum Intensif - Rp 599.000</option>
                    </select>
                </div>

                <!-- Nama Lengkap -->
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Nama Lengkap Peserta</label>
                    <input type="text" id="modalNama" placeholder="Contoh: Ahmad Rizki, S.T" class="w-full px-4 py-3 rounded-xl border border-slate-300 text-sm focus:ring-2 focus:ring-navy-800 focus:outline-none" required>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <!-- Email -->
                    <div>
                        <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Email Aktif</label>
                        <input type="email" id="modalEmail" placeholder="nama@email.com" class="w-full px-4 py-3 rounded-xl border border-slate-300 text-sm focus:ring-2 focus:ring-navy-800 focus:outline-none" required>
                    </div>
                    <!-- No WhatsApp -->
                    <div>
                        <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Nomor WhatsApp</label>
                        <input type="tel" id="modalWA" placeholder="08123456789" class="w-full px-4 py-3 rounded-xl border border-slate-300 text-sm focus:ring-2 focus:ring-navy-800 focus:outline-none" required>
                    </div>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <!-- Bank Tujuan -->
                    <div>
                        <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Bank Tujuan Transfer</label>
                        <select id="modalBank" class="w-full px-4 py-3 rounded-xl border border-slate-300 text-sm focus:ring-2 focus:ring-navy-800 focus:outline-none" required>
                            <option value="">-- Pilih Bank --</option>
                            <option value="BCA (8830192831)">BCA - 8106272030</option>
                        
                        </select>
                    </div>
                    <!-- Tanggal Transfer -->
                    <div>
                        <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Tanggal Transfer</label>
                        <input type="date" id="modalTanggal" class="w-full px-4 py-3 rounded-xl border border-slate-300 text-sm focus:ring-2 focus:ring-navy-800 focus:outline-none" required>
                    </div>
                </div>

                <!-- Upload Bukti Transfer -->
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Upload Struk / Bukti Transfer</label>
                    <input type="file" id="modalBukti" accept="image/*" onchange="previewImage(event)" class="w-full text-xs text-slate-500 file:mr-4 file:py-2.5 file:px-4 file:rounded-xl file:border-0 file:text-xs file:font-semibold file:bg-navy-800 file:text-white hover:file:bg-navy-900 cursor-pointer" required>
                    <!-- Preview Image -->
                    <div id="imagePreviewContainer" class="mt-2 hidden">
                        <img id="imagePreview" src="#" alt="Preview Bukti" class="max-h-36 rounded-xl border border-slate-200 object-contain">
                    </div>
                </div>

                <button type="submit" class="w-full gold-gradient text-navy-800 font-extrabold py-3.5 rounded-xl shadow-lg hover:opacity-95 transition mt-4 flex items-center justify-center gap-2">
                    <i class="fa-solid fa-paper-plane"></i> Kirim Konfirmasi Pembayaran
                </button>
            </form>
        </div>
    </div>

    <!-- MODAL NOTIFIKASI BERHASIL -->
    <div id="successModal" class="fixed inset-0 bg-navy-800/80 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl max-w-md w-full p-6 text-center custom-shadow space-y-4">
            <div class="w-16 h-16 bg-emerald-100 text-emerald-500 rounded-full flex items-center justify-center text-3xl mx-auto">
                <i class="fa-solid fa-circle-check"></i>
            </div>
            <h3 class="text-2xl font-bold text-navy-800">Konfirmasi Terkirim!</h3>
            <p class="text-sm text-slate-600 leading-relaxed">
                Terima kasih, data konfirmasi pembayaran Anda telah kami terima. Silakan selesaikan verifikasi cepat dengan mengirim pesan ke Whatsapp Admin.
            </p>
            <div id="waRedirectContainer" class="pt-2">
                <!-- Dynamic WA Button generated by JS -->
            </div>
            <button onclick="closeSuccessModal()" class="text-xs text-slate-400 underline hover:text-slate-600 block mx-auto">Tutup jendela ini</button>
        </div>
    </div>

    <!-- NOTIFICATION TOAST -->
    <div id="toast" class="fixed bottom-5 right-5 bg-navy-800 text-white px-5 py-3 rounded-xl shadow-2xl z-50 hidden flex items-center gap-3 border border-gold-500/30">
        <i class="fa-solid fa-check-circle text-gold-400 text-lg"></i>
        <span id="toastMessage" class="text-xs font-semibold">Berhasil disalin!</span>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // Set default date input into today
        document.getElementById('modalTanggal').valueAsDate = new Date();

        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mobileMenu = document.getElementById('mobileMenu');
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        document.querySelectorAll('.mobile-link').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Countdown Timer Logic
        function startCountdown() {
            let hours = 11, minutes = 59, seconds = 59;
            setInterval(() => {
                seconds--;
                if (seconds < 0) {
                    seconds = 59;
                    minutes--;
                    if (minutes < 0) {
                        minutes = 59;
                        hours--;
                        if (hours < 0) hours = 23;
                    }
                }
                document.getElementById('hours').innerText = hours.toString().padStart(2, '0');
                document.getElementById('minutes').innerText = minutes.toString().padStart(2, '0');
                document.getElementById('seconds').innerText = seconds.toString().padStart(2, '0');
            }, 1000);
        }
        startCountdown();

        // FAQ Accordion Toggle
        function toggleFaq(button) {
            const content = button.nextElementSibling;
            const icon = button.querySelector('i');
            
            content.classList.toggle('hidden');
            icon.classList.toggle('rotate-180');
        }

        // Copy Bank Account Number Function
        function copyToClipboard(elementId) {
            const textToCopy = document.getElementById(elementId).innerText;
            
            // Clipboard Fallback Strategy for browser iframe environment
            const tempInput = document.createElement('input');
            tempInput.value = textToCopy;
            document.body.appendChild(tempInput);
            tempInput.select();
            document.execCommand('copy');
            document.body.removeChild(tempInput);

            showToast('Nomor rekening ' + textToCopy + ' berhasil disalin!');
        }

        // Toast Helper
        function showToast(message) {
            const toast = document.getElementById('toast');
            const toastMessage = document.getElementById('toastMessage');
            toastMessage.innerText = message;
            toast.classList.remove('hidden');
            setTimeout(() => {
                toast.classList.add('hidden');
            }, 3000);
        }

        // Modal Functionalities
        function openPaymentModal() {
            document.getElementById('paymentModal').classList.remove('hidden');
        }

        function closePaymentModal() {
            document.getElementById('paymentModal').classList.add('hidden');
        }

        function closeSuccessModal() {
            document.getElementById('successModal').classList.add('hidden');
        }

        // Select package automatically from pricing cards
        function selectPackage(packageName, price) {
            const modalPaket = document.getElementById('modalPaket');
            modalPaket.value = packageName;
            openPaymentModal();
        }

        // Preview Bukti Transfer Image
        function previewImage(event) {
            const reader = new FileReader();
            reader.onload = function() {
                const output = document.getElementById('imagePreview');
                const container = document.getElementById('imagePreviewContainer');
                output.src = reader.result;
                container.classList.remove('hidden');
            };
            if(event.target.files[0]){
                reader.readAsDataURL(event.target.files[0]);
            }
        }

        // Handle Payment Confirmation Form Submit
        function handleFormSubmit(e) {
            e.preventDefault();

            const paket = document.getElementById('modalPaket').value;
            const nama = document.getElementById('modalNama').value;
            const email = document.getElementById('modalEmail').value;
            const wa = document.getElementById('modalWA').value;
            const bank = document.getElementById('modalBank').value;
            const tanggal = document.getElementById('modalTanggal').value;

            // Generate WhatsApp Redirect Link
            const adminNumber = "6281234567890"; // Ganti dengan nomor WhatsApp Admin
            const message = `Halo Admin Akselerasi CPNS,%0A%0ASaya sudah melakukan konfirmasi pembayaran via website dengan rincian:%0A- *Nama*: ${nama}%0A- *Email*: ${email}%0A- *Paket*: ${paket}%0A- *Bank Tujuan*: ${bank}%0A- *Tanggal Transfer*: ${tanggal}%0A%0AMohon bantuan untuk aktivasi akun saya. Terima kasih!`;
            
            const waUrl = `https://wa.me/${adminNumber}?text=${message}`;

            // Inject WA Button in Success Modal
            const waContainer = document.getElementById('waRedirectContainer');
            waContainer.innerHTML = `
                <a href="${waUrl}" target="_blank" class="w-full bg-emerald-500 hover:bg-emerald-600 text-white font-bold py-3.5 px-4 rounded-xl shadow-md transition flex items-center justify-center gap-2 text-sm">
                    <i class="fa-brands fa-whatsapp text-lg"></i> Konfirmasi Langsung ke WhatsApp Admin
                </a>
            `;

            closePaymentModal();
            document.getElementById('successModal').classList.remove('hidden');
            
            // Reset Form
            document.getElementById('paymentForm').reset();
            document.getElementById('imagePreviewContainer').classList.add('hidden');
        }
    </script>
</body>
</html>
