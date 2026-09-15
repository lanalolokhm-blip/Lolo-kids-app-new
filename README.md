# Lulu Kids — لولو 🐰✨

مشروع Android بسيط لتطبيق أطفال تعليمي وترفيهي باللغة العربية.

## البناء من GitHub بدون كمبيوتر

المشروع يحتوي على GitHub Actions جاهز لبناء ملف APK.

1. ارفع/استبدل ملفات المشروع في مستودع GitHub.
2. افتح تبويب **Actions**.
3. اختر **Build Lulu APK**.
4. اضغط **Run workflow**.
5. انتظر حتى تنتهي المهمة بدون علامة حمراء.
6. افتح نتيجة التشغيل، ثم قسم **Artifacts**.
7. نزّل **lulu-debug-apk** وستجد داخله `app-debug.apk`.

## إعدادات البناء

- JDK 17
- Gradle 8.10.2
- Android Gradle Plugin 8.7.3
- Kotlin 2.0.21
- Android SDK 35
- Java/Kotlin JVM target: 17
- Jetpack Compose

## سبب الإصلاح

تم توحيد هدف JVM إلى Java/Kotlin 17، وإضافة Compose Compiler Plugin المتوافق مع Kotlin 2.0.21، وإزالة خطوة إنشاء ملفات Gradle مؤقتة من GitHub Actions. الـ Workflow يبني ملفات المشروع الموجودة في المستودع مباشرة.
