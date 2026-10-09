# حزمة الأكواد البرمجية الكاملة لمنصة «نادي مَتن» وطريقة تحميلها كملف ZIP بضغطة زر

نظراً لأن بيئات التصفح السحابية لا تتيح تنزيل ملف `.zip` ثنائي مباشر إلى جهازك عبر الشات، قمنا بتجهيز **أسهل وسيلتين فوريتين** للحصول على ملف ZIP كامل للمنصة أو تحميل ملفاته بضغطة واحدة:

---

## ⚡ الطريقة الأولى (الأسرع على الإطلاق عبر GitHub - بضغطة زر واحدة):
إذا رفعت الملفات إلى مستودع GitHub الخاص بك (مثل `matn-club`):
1. افتح صفحة مستودعك على GitHub.
2. اضغط على الزر الأخضر **`Code`**.
3. اختر **`Download ZIP`**.
4. سيبدأ تحميل مجلد المنصة كاملاً كملف مضغوط فوراً على جهازك!

---

## 📦 الطريقة الثانية: إنشاء ملف الـ ZIP محلياً على جهازك في 30 ثانية
أنشئ مجلداً باسم `matn-club` وأنشئ بداخله الملفات التالية بنسخ الأكواد المصدرية النظيفة أدناه:

```text
matn-club/
├── index.html          (البوابة الرئيسية لنادي متن)
├── admin.html          (لوحة تحكم المشرف العام)
├── wallet.html         (محفظة الولاء ونقاط متن)
├── booking.html        (حجز مقاعد الصالون والأمسيات)
├── partners.html       (دليل وفروع شركاء الاستبدال)
├── recordings.html     (مشغل التسجيلات المرئية والنقاشات)
└── README.md           (دليل التثبيت والنشر)
```
بعد وضع الملفات في المجلد: انقر بزر الفأرة الأيمن على المجلد واختر **Compress to ZIP** (أو "إرسال إلى مجلد مضغوط").

---

# 📄 الأكواد الكاملة لجميع صفحات المنصة:

### 1. كود `index.html` (البوابة الرئيسية)
```html
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
```

---

### 2. كود `admin.html` (لوحة تحكم المشرف العام)
```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>لوحة تحكم المشرف العام | نادي مَتن</title>
    <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cairo:wght@400;600;700;800&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-[#fcf9f3] text-[#1c2421] font-['Cairo'] min-h-screen flex flex-col">
    <header class="bg-white border-b border-[#e8dec8] p-4 sticky top-0 z-40">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <div class="flex items-center gap-3">
                <a href="index.html" class="font-['Amiri'] font-bold text-2xl text-[#234e3d]">نادي مَتن</a>
                <span class="text-xs bg-[#c5a059]/20 text-[#173629] font-bold px-2 py-0.5 rounded">لوحة المشرف العام</span>
            </div>
            <a href="index.html" class="text-xs font-bold text-[#234e3d] hover:underline">العودة للبوابة الرئيسية ←</a>
        </div>
    </header>

    <main class="max-w-7xl mx-auto px-4 py-8 flex-1 w-full space-y-6">
        <div class="flex justify-between items-center">
            <h1 class="text-2xl font-bold font-['Amiri'] text-[#234e3d]">لوحة القيادة وإدارة صالونات القراءة</h1>
            <div class="flex gap-2">
                <button onclick="alert('تم تفعيل نموذج إضافة شريك جديد')" class="bg-[#234e3d] text-white px-4 py-2 rounded-xl text-xs font-bold shadow">+ إضافة شريك</button>
                <button onclick="alert('تم إنشاء قسيمة: MATN-2025-50')" class="bg-white border border-[#e8dec8] px-4 py-2 rounded-xl text-xs font-bold">توليد قسيمة شحن</button>
            </div>
        </div>

        <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
            <div class="bg-white p-5 rounded-2xl border border-[#e8dec8] shadow-sm">
                <div class="text-xs text-gray-500">إجمالي القراء</div>
                <div class="text-3xl font-bold font-['Amiri'] text-[#234e3d] mt-2">4,850</div>
                <div class="text-[11px] text-emerald-700 mt-1 font-semibold">↑ +14.2% هذا الشهر</div>
            </div>
            <div class="bg-white p-5 rounded-2xl border border-[#e8dec8] shadow-sm">
                <div class="text-xs text-gray-500">المشرفون والميسرون</div>
                <div class="text-3xl font-bold font-['Amiri'] text-[#234e3d] mt-2">24</div>
                <div class="text-[11px] text-gray-500 mt-1">عبر 7 فروع ومدن</div>
            </div>
            <div class="bg-white p-5 rounded-2xl border border-[#e8dec8] shadow-sm">
                <div class="text-xs text-gray-500">الصالونات المعتمدة</div>
                <div class="text-3xl font-bold font-['Amiri'] text-[#234e3d] mt-2">38</div>
                <div class="text-[11px] text-[#c5a059] font-semibold mt-1">نسبة الحضور 94%</div>
            </div>
            <div class="bg-white p-5 rounded-2xl border border-[#e8dec8] shadow-sm">
                <div class="text-xs text-gray-500">نقاط الولاء المصروفة</div>
                <div class="text-3xl font-bold font-['Amiri'] text-[#234e3d] mt-2">5,420</div>
                <div class="text-[11px] text-gray-500 mt-1">رصيد إدارة متاح للتحفيز</div>
            </div>
        </div>
    </main>
</body>
</html>
```

---

### 3. كود `wallet.html` (محفظة الولاء واستبدال النقاط)
```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>محفظة الولاء ونقاط مَتن | نادي مَتن</title>
    <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cairo:wght@400;600;700;800&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-[#fcf9f3] text-[#1c2421] font-['Cairo'] min-h-screen flex flex-col">
    <header class="bg-white border-b border-[#e8dec8] p-4">
        <div class="max-w-4xl mx-auto flex justify-between items-center">
            <a href="index.html" class="font-['Amiri'] font-bold text-2xl text-[#234e3d]">نادي مَتن</a>
            <div class="flex gap-4 text-xs font-bold">
                <a href="index.html">الرئيسية</a>
                <a href="booking.html">الصالونات</a>
                <a href="partners.html">الشركاء</a>
            </div>
        </div>
    </header>

    <main class="max-w-4xl mx-auto px-4 py-8 flex-1 w-full space-y-6">
        <div class="bg-gradient-to-r from-[#173629] to-[#234e3d] text-white p-8 rounded-3xl shadow-xl flex flex-col sm:flex-row justify-between items-start sm:items-center gap-6">
            <div>
                <span class="text-xs text-[#e8dec8] font-bold">رصيد الولاء الثقافي المتاح</span>
                <div class="text-5xl font-bold font-['Amiri'] text-[#dfbe7e] mt-1">340 نقطة</div>
                <p class="text-xs text-gray-200 mt-2">الرتبة: القارئ المتميز • المتن الراسخ (خصم 40% لدور النشر)</p>
            </div>
            <div class="flex flex-col gap-2 w-full sm:w-auto">
                <a href="partners.html" class="bg-[#c5a059] hover:bg-[#dfbe7e] text-[#173629] text-center font-bold px-6 py-2.5 rounded-xl text-xs transition">استبدال النقاط بمزايا ←</a>
                <button onclick="let code = prompt('أدخل رمز قسيمة الولاء:'); if(code) alert('تم شحن القسيمة بنجاح!');" class="bg-white/10 hover:bg-white/20 text-white font-bold px-6 py-2 rounded-xl text-xs border border-white/20">شحن قسيمة هدية</button>
            </div>
        </div>

        <div class="bg-white p-6 rounded-2xl border border-[#e8dec8] shadow-sm space-y-4">
            <h3 class="font-bold text-[#234e3d] font-['Amiri'] text-lg">كيف تجمع المزيد من نقاط مَتن؟</h3>
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-3 text-xs">
                <div class="p-4 bg-[#fcf9f3] rounded-xl border border-[#e8dec8]">
                    <div class="font-bold text-[#234e3d] text-sm">+20 نقطة</div>
                    <div class="text-gray-600 mt-1">حضور صالون نقاش كتاب والتفاعل الصوتي</div>
                </div>
                <div class="p-4 bg-[#fcf9f3] rounded-xl border border-[#e8dec8]">
                    <div class="font-bold text-[#234e3d] text-sm">+2 نقطتان يومياً</div>
                    <div class="text-gray-600 mt-1">تجاوز 10 دقائق قراءة للمقالات داخل المنصة</div>
                </div>
                <div class="p-4 bg-[#fcf9f3] rounded-xl border border-[#e8dec8]">
                    <div class="font-bold text-[#234e3d] text-sm">+10 نقاط</div>
                    <div class="text-gray-600 mt-1">كتابة مراجعة أو خاطرة فكرية ملهمة</div>
                </div>
            </div>
        </div>
    </main>
</body>
</html>
```

---

### 4. كود `booking.html` (حجز مقاعد الصالون)
```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حجز مقعد بالصالون | نادي مَتن</title>
    <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cairo:wght@400;600;700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-[#fcf9f3] text-[#1c2421] font-['Cairo'] min-h-screen flex flex-col">
    <header class="bg-white border-b border-[#e8dec8] p-4 flex justify-between items-center max-w-4xl mx-auto w-full">
        <a href="index.html" class="font-bold text-lg text-[#234e3d] font-['Amiri']">← نادي مَتن للقراءة</a>
        <span class="text-xs text-gray-500">حجز مقعد الجلسة</span>
    </header>

    <main class="max-w-2xl mx-auto px-4 py-8 flex-1 w-full space-y-6">
        <div class="bg-white p-6 rounded-3xl border border-[#e8dec8] shadow-lg space-y-5">
            <span class="text-xs bg-[#234e3d]/10 text-[#234e3d] font-bold px-3 py-1 rounded-full">صالون الرياض • حضوري وافتراضي</span>
            <h1 class="text-2xl font-bold font-['Amiri'] text-[#234e3d]">أمسية نقاش: ثلاثية غرناطة (رضوى عاشور)</h1>
            <p class="text-xs text-gray-600 leading-relaxed">جلسة حوارية نقدية تستجلي معالم الوجع الإنساني، وتفكيك الهوية والأفول في سردية رضوى عاشور.</p>
            <div class="p-4 bg-[#fcf9f3] rounded-xl text-xs space-y-2 border border-[#e8dec8]">
                <div class="flex justify-between"><span>الموعد:</span><strong>السبت القادم • 7:30 مساءً</strong></div>
                <div class="flex justify-between"><span>المكان:</span><strong>صالون مَتن - فرع السليمانية / Zoom VIP</strong></div>
                <div class="flex justify-between"><span>المقاعد المتبقية:</span><strong class="text-amber-800">6 مقاعد فقط</strong></div>
            </div>
            <button onclick="alert('تم تأكيد حجز مقعدك بنجاح! تم إرسال التذكرة المشفرة إلى بريدك الإلكتروني.'); window.location.href='index.html';" class="w-full bg-[#234e3d] hover:bg-[#173629] text-white py-3.5 rounded-xl font-bold text-sm shadow transition">
                تأكيد حجز مقعدي بالصالون مجاناً (مشترك)
            </button>
        </div>
    </main>
</body>
</html>
```

---

### 5. كود `partners.html` (دليل شركاء الاستبدال)
```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دليل شركاء الاستبدال | نادي مَتن</title>
    <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cairo:wght@400;600;700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-[#fcf9f3] text-[#1c2421] font-['Cairo'] min-h-screen flex flex-col">
    <header class="bg-white border-b border-[#e8dec8] p-4 flex justify-between items-center max-w-5xl mx-auto w-full">
        <a href="index.html" class="font-bold text-lg text-[#234e3d] font-['Amiri']">← نادي مَتن</a>
        <a href="wallet.html" class="text-xs font-bold text-[#234e3d]">رصيدك: 340 نقطة</a>
    </header>

    <main class="max-w-5xl mx-auto px-4 py-8 flex-1 w-full space-y-6">
        <div>
            <h1 class="text-2xl font-bold font-['Amiri'] text-[#234e3d]">دليل وفروع شركاء استبدال نقاط مَتن</h1>
            <p class="text-xs text-gray-600 mt-1">استبدل نقاطك بقسائم فورية لدى دور النشر، المشاغل النسائية، النوادي الرياضية، والمقاهي الأدبية.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
            <div class="bg-white p-5 rounded-2xl border border-[#e8dec8] shadow-sm space-y-3">
                <span class="text-[11px] font-bold bg-[#c5a059]/20 text-[#234e3d] px-2 py-0.5 rounded">عناية ومشاغل نسائية</span>
                <h3 class="font-bold text-base text-[#1c2421]">مشغل لافندر للعناية النسائية</h3>
                <p class="text-xs text-gray-500">قسيمة خصم 100 ريال لكافة الخدمات التجميلية والمساج الأروماتك.</p>
                <div class="pt-2 flex justify-between items-center text-xs">
                    <span class="font-bold text-[#c5a059]">120 نقطة</span>
                    <button onclick="alert('تم إصدار قسيمة الاستبدال بنجاح! كود القسيمة: LAV-8891')" class="bg-[#234e3d] text-white px-3 py-1.5 rounded-lg font-bold">استبدال فوراً</button>
                </div>
            </div>

            <div class="bg-white p-5 rounded-2xl border border-[#e8dec8] shadow-sm space-y-3">
                <span class="text-[11px] font-bold bg-blue-50 text-blue-800 px-2 py-0.5 rounded">لياقة وبدنية نسائية</span>
                <h3 class="font-bold text-base text-[#1c2421]">نادي فيتا للياقة النسائية</h3>
                <p class="text-xs text-gray-500">اشتراك أسبوعي تجريبي كامل شامل الصالة وحصص البيلاتس واليوغا.</p>
                <div class="pt-2 flex justify-between items-center text-xs">
                    <span class="font-bold text-[#c5a059]">150 نقطة</span>
                    <button onclick="alert('تم إصدار قسيمة الاستبدال بنجاح! كود القسيمة: VITA-4421')" class="bg-[#234e3d] text-white px-3 py-1.5 rounded-lg font-bold">استبدال فوراً</button>
                </div>
            </div>

            <div class="bg-white p-5 rounded-2xl border border-[#e8dec8] shadow-sm space-y-3">
                <span class="text-[11px] font-bold bg-amber-50 text-amber-800 px-2 py-0.5 rounded">مقاهي أدبية وثقافة</span>
                <h3 class="font-bold text-base text-[#1c2421]">مقهى ومكتبة صوفيا</h3>
                <p class="text-xs text-gray-500">مشروب قهوة مختصة مجاني مع حجز ركن قراءة هادئ لمدة ساعتين.</p>
                <div class="pt-2 flex justify-between items-center text-xs">
                    <span class="font-bold text-[#c5a059]">50 نقطة</span>
                    <button onclick="alert('تم إصدار قسيمة الاستبدال بنجاح! كود القسيمة: SOF-1029')" class="bg-[#234e3d] text-white px-3 py-1.5 rounded-lg font-bold">استبدال فوراً</button>
                </div>
            </div>
        </div>
    </main>
</body>
</html>
```

---

### 6. كود `recordings.html` (مشغل التسجيلات المرئية والنقاشات)
*(تم تجهيزه أيضاً في وثيقة `recordings.html` المخصصة في مساحة العمل)*:
```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أرشيف التسجيلات المرئية | نادي مَتن</title>
    <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cairo:wght@400;600;700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-[#fcf9f3] text-[#1c2421] font-['Cairo'] min-h-screen flex flex-col">
    <header class="bg-white border-b border-[#e8dec8] p-4 flex justify-between items-center max-w-6xl mx-auto w-full">
        <a href="index.html" class="font-bold text-xl text-[#234e3d] font-['Amiri']">← نادي مَتن</a>
        <div class="flex gap-4 text-xs font-bold">
            <a href="index.html">الرئيسية</a>
            <a href="wallet.html">محفظة الولاء</a>
            <a href="admin.html">بوابة المشرف</a>
        </div>
    </header>

    <main class="max-w-6xl mx-auto px-4 py-8 flex-1 w-full space-y-6">
        <h1 class="text-2xl font-bold font-['Amiri'] text-[#234e3d]">أمسية الفلسفة والفكر: تهافت الفلاسفة وتهافت التهافت</h1>
        <div class="bg-black rounded-3xl aspect-video flex items-center justify-center text-white relative shadow-xl">
            <button onclick="alert('بدأ تشغيل التسجيل المرئي بدقة 4K')" class="w-16 h-16 rounded-full bg-[#c5a059] text-black font-bold flex items-center justify-center text-2xl shadow-lg">▶</button>
        </div>
        <div class="bg-white p-6 rounded-2xl border border-[#e8dec8] shadow-sm">
            <h3 class="font-bold text-[#234e3d] font-['Amiri'] text-lg">المداخلة المثبتة في الصدارة:</h3>
            <p class="text-xs text-gray-700 mt-2 leading-relaxed">«ابن رشد لم يكن يدافع عن الفلسفة ضد الدين، بل برهن أن إعمال العقل هو عين التكليف الشرعي.» - د. عبد الرحمن بن فهد</p>
        </div>
    </main>
</body>
</html>
```
