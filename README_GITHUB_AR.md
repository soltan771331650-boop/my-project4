# الطابعة المثالية - نسخة GitHub Actions

هذه النسخة مجهزة للبناء من GitHub بدون كمبيوتر، ويمكن رفع مجلد المشروع كما هو إلى مستودع GitHub.

## طريقة البناء من الهاتف

1. أنشئ Repository جديد في GitHub.
2. ارفع **محتويات هذا المجلد** إلى المستودع، وليس ملف ZIP نفسه.
3. تأكد أن الملف `.github/workflows/build-apk.yml` موجود.
4. بعد الرفع افتح تبويب **Actions** في المستودع.
5. اختر **Build Android APK**.
6. اضغط **Run workflow**.
7. بعد نجاح البناء افتح نتيجة التشغيل وابحث عن **Artifacts**.
8. نزّل `NativeWifiPrinter-debug` وستجد داخله ملف `app-debug.apk`.

## البناء التلقائي

الـWorkflow يعمل أيضًا عند الدفع إلى فرع `main` أو `master`.

## ملاحظات

- المشروع Native Android / Kotlin.
- لا يحتاج Android Studio على جهازك إذا استخدمت GitHub Actions.
- يستخدم JDK 17 وGradle 9.6 وAndroid Gradle Plugin 9.4.
- هذه نسخة Debug للتجربة. توقيع Release للنشر في Google Play خطوة لاحقة.
