بوت واتساب Rust — إصدار Linux x86_64 ثابت (musl)

الملف التنفيذي مبني من النسخة المحدّثة المرفقة، لمعمارية x86_64، وثابت لتفادي الاعتماد على glibc في حاويات مثل Wispbyte.

الإعداد والتشغيل:
1. انسخ .env.example إلى .env:
   cp .env.example .env
2. عدّل WHATSAPP_PHONE_NUMBER وأدخل رقم WhatsApp الدولي دون علامة +.
3. اترك YOUTUBE_COOKIES فارغًا ما لم يتطلب محتوى يوتيوب جلسة حساب. ملفات cookies حساسة وتعامل معها ككلمة مرور، ولا ترفعها للمستودع.
4. شغّل:
   chmod +x ./whatsapp-rust-bot
   exec ./whatsapp-rust-bot
5. اتبع pairing code الظاهر في الطرفية لإقران الجهاز.

الأوامر: /hi، /ping، /echo، /yt، /ytaudio، /sendfile، /help.
تُنشأ جلسة WhatsApp في whatsapp_bot.db في مجلد التشغيل؛ لا تشاركها.
لا يتضمن المستودع ملف .env فعليًا أو cookies أو بيانات جلسة خاصة.
