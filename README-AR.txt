بوت واتساب Rust — إصدار Linux x86_64 ثابت (musl)

بُني هذا الملف التنفيذي من أحدث نسخة للمشروع المرفقة. النسخة x86_64 ثابتة ولا تعتمد على glibc الخاصة بالحاوية، ومناسبة لحاويات Linux x86_64 مثل Wispbyte.

الإعداد والتشغيل:
1. انسخ .env.example إلى .env:
   cp .env.example .env
2. عدّل WHATSAPP_PHONE_NUMBER إلى رقم WhatsApp الدولي دون علامة +.
3. اترك YOUTUBE_COOKIES فارغًا إلا إذا تطلب محتوى YouTube جلسة حساب. إن أضفته، استخدم Cookie header بصيغة name=value; name=value. بيانات cookies حساسة ككلمة مرور؛ لا ترفعها أو تشاركها.
4. شغّل:
   chmod +x ./whatsapp-rust-bot
   exec ./whatsapp-rust-bot
5. اتبع pairing code الظاهر في الطرفية لإقران الجهاز.

الأوامر: /hi، /ping، /echo، /yt، /ytaudio، /sendfile، /help.
يفحص البوت أول نطاق 1 MB من روابط الصيغ قبل عرضها. عند رفض YouTube لصيغة مختارة، يجرب صيغة قريبة من النوع نفسه ويذكر itag البديل.

تُحفظ جلسة WhatsApp في whatsapp_bot.db داخل مجلد التشغيل؛ لا تشاركها. لا يحتوي المستودع على .env فعلي أو cookies أو بيانات جلسة خاصة.
