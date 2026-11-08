بوت واتساب Rust — إصدار Linux x86_64 ثابت (musl)

بُني هذا الملف التنفيذي من آخر نسخة للمشروع أرسلها المستخدم. النسخة x86_64 ثابتة ولا تعتمد على glibc الخاصة بالحاوية، ومناسبة لحاويات Linux x86_64 مثل Wispbyte.

الإعداد والتشغيل:
1. انسخ .env.example إلى .env:
   cp .env.example .env
2. عدّل WHATSAPP_PHONE_NUMBER إلى رقم WhatsApp الدولي دون علامة +.
3. اترك YOUTUBE_COOKIES فارغًا إلا إذا تطلب المحتوى جلسة YouTube. إذا استخدمته، ضع Cookie header بصيغة name=value; name=value. هذه البيانات حساسة ككلمة مرور، فلا ترفعها إلى المستودع أو تشاركها.
4. شغّل:
   chmod +x ./whatsapp-rust-bot
   exec ./whatsapp-rust-bot
5. اتبع pairing code الظاهر في الطرفية لإقران الجهاز.

الأوامر: /hi، /ping، /echo، /yt، /ytaudio، /sendfile، /help.
عند رفض YouTube لصيغة محددة، يجرب البوت صيغة قريبة من النوع نفسه ويبلغك بـ itag البديل. كما يفحص إتاحة الصيغ قبل عرضها.

تُحفظ جلسة WhatsApp في whatsapp_bot.db داخل مجلد التشغيل. لا تشاركها. لا يحتوي المستودع على ملف .env فعلي أو cookies أو بيانات جلسة خاصة.
