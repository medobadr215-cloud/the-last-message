# The Last Message — APK (آخر رسالة)

اللعبة جاهزة تتحول لـ APK أوتوماتيك على GitHub (بدون ما تنزّل Android Studio).

## الخطوات
1. اعمل حساب على github.com ثم **New repository** (خليه Public أو Private، مش فارق).
2. ارفع كل محتويات الفولدر ده للـ repository (Add file → Upload files).
   - **مهم:** لازم الفولدر المخفي `.github/workflows/build-apk.yml` يترفع. لو مرفعش مع السحب والإفلات:
     اختار **Add file → Create new file** واكتب في الاسم `.github/workflows/build-apk.yml` وانسخ محتوى الملف جواه.
3. افتح تبويب **Actions** — هتلاقي **Build Android APK** شغّال لوحده (أو اضغط **Run workflow**).
4. استنى حوالي 5–8 دقايق. لما يخلص (علامة ✔ خضرا) افتح التشغيل ونزّل **the-last-message-apk** من قسم Artifacts. جواه `the-last-message.apk`.
5. ابعت الـ APK للموبايل وثبّته (فعّل "التثبيت من مصادر غير معروفة").

## Release بلينك تحميل ثابت (اختياري)
اعمل Tag بالشكل `v1.0.0` (Releases → Draft a new release → Tag) وهيتنشر الـ APK في صفحة Releases.

## تعديل اللعبة
عدّل الملف `www/index.html` وارفعه — الـ APK بيتبني من جديد.

## ملاحظات
- الشاشة متقفلة **أفقي** (Landscape). لو عايزها تلف براحتها غيّر `ORIENTATION` في ملف الـ workflow إلى `unspecified`.
- الـ APK ده Debug موقّع تلقائياً وبيتثبّت عادي. للنشر على Google Play محتاج توقيع Release (Keystore) — اطلب مني أضيفه.
- الخطوط (Cairo / Amiri / Cinzel...) بتتحمّل من الإنترنت؛ من غير نت اللعبة شغالة بخطوط الجهاز.
- اسم الباكدج: `com.thelastmessage.game` (غيّره من `capacitor.config.json` قبل أول نشر لو عايز).
