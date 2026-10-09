<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>نادي مَتن للقراءة والحوار | البوابة الرئيسية</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Amiri:ital,wght@0,400;0,700;1,400&family=Cairo:wght@300;400;500;600;700;800&family=Aref+Ruqaa:wght@400;700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        matn: {
                            emerald: '#234e3d',
                            emeraldDark: '#173629',
                            emeraldLight: '#2f6751',
                            gold: '#c5a059',
                            goldLight: '#dfbe7e',
                            cream: '#fcf9f3',
                            creamDark: '#f2ece0',
                            sand: '#e8dec8',
                            charcoal: '#1c2421',
                            muted: '#5a6b63'
                        }
                    },
                    fontFamily: { amiri: ['Amiri', 'serif'], cairo: ['Cairo', 'sans-serif'], ruqaa: ['"Aref Ruqaa"', 'serif'] }
                }
            }
        }
    </script>
</head>
<body class="min-h-screen flex flex-col bg-[#fcf9f3] text-[#1c2421] font-['Cairo']">
    <div class="bg-matn-emeraldDark text-matn-goldLight px-4 py-2 text-xs md:text-sm text-center flex items-center justify-center gap-2 border-b border-matn-emerald/40">
        <span class="inline-block w-2 h-2 rounded-full bg-matn-gold animate-pulse"></span>
        <span>الصالون الثقافي العربي المعاصر • دورة ربيع 2025: نلتقي حول كتاب، ونغادر بفكرة.</span>
        <a href="booking.html" class="underline font-bold hover:text-white mr-2 transition">احجز مقعدك الآن ←</a>
    </div>

    <header class="sticky top-0 z-50 bg-[#fcf9f3]/95 backdrop-blur-md border-b border-matn-sand/60">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <a href="index.html" class="flex items-center gap-3">
                <div class="w-12 h-12 rounded-full border-2 border-matn-gold flex items-center justify-center bg-white shadow-sm overflow-hidden p-1">
                    <div class="text-center font-['Amiri'] font-bold text-matn-emerald text-xl leading-none">مَتن</div>
                </div>
                <div>
                    <span class="font-['Amiri'] text-2xl font-bold text-matn-emerald tracking-wide block">نادي مَتن</span>
                    <span class="text-[10px] text-matn-muted tracking-wider block">للقراءة والحوار الثقافي</span>
                </div>
            </a>
            <nav class="hidden md:flex items-center gap-7 text-sm font-semibold text-matn-charcoal">
                <a href="index.html" class="text-matn-emerald border-b-2 border-matn-emerald pb-1">الرئيسية</a>
                <a href="booking.html" class="hover:text-matn-emerald transition">صالونات القراءة</a>
                <a href="wallet.html" class="hover:text-matn-emerald transition flex items-center gap-1.5">
                    <span>محفظة الولاء</span>
                    <span class="bg-matn-gold/20 text-matn-emeraldDark text-[11px] px-2 py-0.5 rounded-full font-bold">نقاط مَتن</span>
                </a>
                <a href="partners.html" class="hover:text-matn-emerald transition">دليل الشركاء</a>
                <a href="recordings.html" class="hover:text-matn-emerald transition">التسجيلات المرئية</a>
                <a href="admin.html" class="hover:text-matn-emerald transition text-matn-muted">بوابة الإشراف</a>
            </nav>
            <div class="flex items-center gap-3">
                <a href="wallet.html" class="hidden sm:flex items-center gap-2 bg-matn-creamDark border border-matn-sand px-3.5 py-1.5 rounded-full text-xs font-bold text-matn-emerald shadow-sm hover:border-matn-gold transition">
                    <span class="w-2.5 h-2.5 rounded-full bg-matn-gold"></span>
                    <span>340 نقطة</span>
                </a>
                <a href="booking.html" class="bg-matn-emerald hover:bg-matn-emeraldLight text-white px-5 py-2.5 rounded-xl text-sm font-bold shadow-md hover:shadow-lg transition">انضم لصالون</a>
            </div>
        </div>
    </header>

    <main class="flex-1">
        <section class="py-12 md:py-20 border-b border-matn-sand/40 bg-gradient-to-b from-[#fcf9f3] to-matn-creamDark/40">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                    <div class="lg:col-span-7 space-y-6 text-center lg:text-right">
                        <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-matn-emerald/10 border border-matn-emerald/20 text-matn-emerald text-xs font-bold">
                            <span>📖</span>
                            <span>مساحة فكرية هادئة لعشاق الكتب والنقاش العميق</span>
                        </div>
                        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold font-['Amiri'] text-matn-emerald leading-tight">
                            نَلتقِي حَولَ كِتَاب،<br>
                            <span class="text-matn-gold">وَنُغَادِرُ بِفِكْرَة.</span>
                        </h1>
                        <p class="text-base sm:text-lg text-matn-muted leading-relaxed max-w-2xl mx-auto lg:mx-0">
                            ملاذ فكري لأولئك الذين يؤمنون بأن الكلمة جسر للوعي. يجمع صالون <strong class="text-matn-charcoal">مَتن</strong> نخبة القراء في جلسات دورية تليق بجواهر الفكر والأدب العربي.
                        </p>
                        <div class="pt-2 flex flex-wrap items-center justify-center lg:justify-start gap-4">
                            <a href="booking.html" class="bg-matn-emerald hover:bg-matn-emeraldLight text-white px-7 py-3.5 rounded-xl font-bold text-base shadow-lg transition">احجز مقعدك بالصالون القادم ←</a>
                            <a href="wallet.html" class="bg-white hover:bg-matn-cream border border-matn-sand text-matn-charcoal px-6 py-3.5 rounded-xl font-bold text-base shadow-sm transition">محفظة الولاء والمكافآت</a>
                        </div>
                    </div>

                    <div class="lg:col-span-5 bg-white rounded-3xl p-6 sm:p-8 border border-matn-sand shadow-xl space-y-4">
                        <div class="flex items-center justify-between pb-4 border-b border-matn-sand/50">
                            <span class="text-xs font-bold text-matn-muted">جلسة هذا الأسبوع الحية</span>
                            <span class="px-3 py-1 rounded-full text-xs font-bold bg-amber-50 text-amber-800 border border-amber-200">متبقي 3 مقاعد فقط</span>
                        </div>
                        <h3 class="text-xl font-bold font-['Amiri'] text-matn-emerald">جلسة نقاش «مُدن الملح»</h3>
                        <p class="text-xs text-matn-muted">قراءة معمقة في تحولات الصحراء والذاكرة مع الكاتب عبد الرحمن منيف.</p>
                        <div class="bg-matn-cream p-4 rounded-2xl border border-matn-sand/60 text-xs space-y-1">
                            <div><strong>الموعد:</strong> الثلاثاء القادم • 8:00 مساءً</div>
                            <div><strong>الميسر:</strong> د. ياسر السليمان</div>
                            <div><strong>المكان:</strong> مكتبة الملك فهد الوطنية / Zoom VIP</div>
                        </div>
                        <a href="booking.html" class="block text-center bg-matn-emerald hover:bg-matn-emeraldLight text-white py-3 rounded-xl font-bold text-sm shadow transition">تأكيد حجز مقعدك ←</a>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer class="mt-auto bg-matn-emeraldDark text-white border-t border-matn-emerald py-8 text-center text-xs">
        <div>© 2025 نادي مَتن للقراءة والحوار. نَلْتَقِي حَولَ كِتَاب.. وَنُغَادِرُ بِفِكْرَة.</div>
    </footer>
</body>
</html>
