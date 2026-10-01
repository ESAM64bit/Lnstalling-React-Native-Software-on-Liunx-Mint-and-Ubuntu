# React Native Setup Guide on Linux Mint

[English](#english) | [العربية](#العربية)

---

## English

A step-by-step guide to setting up **React Native** on **Linux Mint**, from a clean system to running your first project. Available in English and Arabic, with a ready-to-use shell script.

### What's inside

| File | Description |
|------|-------------|
| `English.pdf` | Full guide in English |
| `Arabic.pdf` | Full guide in Arabic (الدليل بالعربية) |
| `code` | All commands from the guide in one file |

### Overview

React Native works fully on Linux Mint for **Android** development. iOS apps require macOS, but you can work around this with **Expo Go** on an iPhone or a cloud build service like **EAS Build**.

1. **Install core requirements**: nvm, Node.js (LTS) and JDK 17, with environment variables added to `~/.bashrc`
2. **Install Android Studio & Android SDK**: download the `.tar.gz` from the official site, then set `ANDROID_HOME`
3. **Create your first project**: with Expo (recommended for beginners) or the React Native CLI
4. **Run the app**: scan the QR code with Expo Go, or use an Android emulator

### Quick start

```bash
# Step 1: Node.js + JDK 17
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash && \
source ~/.bashrc && \
nvm install --lts && \
sudo apt update && sudo apt install -y openjdk-17-jdk && \
echo 'export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64' >> ~/.bashrc && \
echo 'export PATH=$JAVA_HOME/bin:$PATH' >> ~/.bashrc && \
source ~/.bashrc && \
node -v && java -version

# Step 2: after installing Android Studio manually
echo 'export ANDROID_HOME=$HOME/Android/Sdk' >> ~/.bashrc
echo 'export PATH=$PATH:$ANDROID_HOME/emulator:$ANDROID_HOME/platform-tools' >> ~/.bashrc
source ~/.bashrc

# Step 3: create a project (Expo, recommended)
npx create-expo-app MyApp && cd MyApp

# Step 4: run
npx expo start
```

> Prefer the React Native CLI? Use `npx @react-native-community/cli init MyApp` in Step 3.

### Tips

- Use a **real phone** instead of an emulator for much better performance on weaker machines.
- iOS builds need **macOS & Xcode**, which are not supported on Linux.
- **Expo** is easier for beginners and doesn't require the full Android Studio setup just to try things out.
- **EAS Build** lets you build iOS/Android apps in the cloud without a Mac.

### Contributing

Found a mistake or want to improve the guide? Open an issue or submit a pull request.

### Author

Created by [ESAM64bit](https://github.com/ESAM64bit) and [Claude](https://claude.ai) (Anthropic).

---

## العربية

دليل مرتب خطوة بخطوة لتثبيت **React Native** على **Linux Mint**، من نظام نظيف حتى تشغيل أول مشروع. متوفر بالعربية والإنجليزية مع ملف يحتوي على الأوامر جاهزة للنسخ.

### محتويات المستودع

| الملف | الوصف |
|------|-------|
| `Arabic.pdf` | الدليل الكامل بالعربية |
| `English.pdf` | الدليل الكامل بالإنجليزية |
| `code` | جميع أوامر الدليل في ملف واحد |

### نظرة عامة

يعمل React Native بشكل كامل على Linux Mint لتطوير تطبيقات **Android**. أما تطبيقات iOS فتتطلب macOS، ويمكن تجاوز ذلك باستخدام **Expo Go** على الآيفون مباشرة أو خدمة البناء السحابية **EAS Build**.

1. **تثبيت المتطلبات الأساسية**: nvm وNode.js (LTS) وJDK 17 مع إضافة متغيرات البيئة إلى `~/.bashrc`
2. **تثبيت Android Studio وAndroid SDK**: حمّل ملف `.tar.gz` من الموقع الرسمي ثم اضبط `ANDROID_HOME`
3. **إنشاء أول مشروع**: باستخدام Expo (الأنسب للمبتدئين) أو React Native CLI
4. **تشغيل التطبيق**: امسح رمز QR بتطبيق Expo Go أو استخدم محاكي Android

### البدء السريع

الأوامر نفسها المذكورة في قسم **Quick start** أعلاه (الأوامر تبقى بالإنجليزية). يمكنك أيضًا نسخها من ملف `code`.

### نصائح

- استخدم **هاتفًا حقيقيًا** بدل المحاكي لأداء أسرع بكثير على الأجهزة الضعيفة.
- بناء تطبيقات iOS يتطلب **macOS وXcode**، وهما غير مدعومين على Linux.
- استخدم **Expo** للمبتدئين، فهو أسهل في الإعداد ولا يحتاج Android Studio كاملًا للتجربة.
- يتيح **EAS Build** بناء تطبيقات Android/iOS سحابيًا دون الحاجة لجهاز Mac.

### المساهمة

وجدت خطأ أو تريد تحسين الدليل؟ افتح Issue أو أرسل Pull Request.

### المؤلف

من إعداد [ESAM64bit](https://github.com/ESAM64bit) و[Claude](https://claude.ai) (Anthropic).
