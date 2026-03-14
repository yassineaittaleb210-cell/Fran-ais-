# 📱 Apprendre le Français — APK Android
## طريقة بناء تطبيق APK من هذا الملف

---

## ✅ الطريقة 1: بدون برمجة — موقع WebIntoApp (أسهل وأسرع)

1. افتح الموقع: https://www.webintoapp.com
2. اضغط **"Create App"**
3. في خانة URL اكتب أي رابط مؤقت أو:
   - ارفع ملف `index.html` من مجلد `www` عبر GitHub Pages أو Netlify Drop
4. اكتب اسم التطبيق: **Français 10 Jours**
5. اختر أيقونة
6. اضغط **"Build APK"** وانتظر
7. حمّل الـ APK وثبّته على هاتفك

---

## ✅ الطريقة 2: Netlify Drop + WebIntoApp

### الخطوة 1 — رفع الملف على Netlify (مجاني)
1. افتح: https://app.netlify.com/drop
2. اسحب مجلد `www` وأفلته في الموقع
3. انسخ الرابط الذي يعطيك إياه (مثال: `https://abc123.netlify.app`)

### الخطوة 2 — تحويله إلى APK
1. افتح: https://www.webintoapp.com
2. الصق الرابط من Netlify
3. اضغط Build وحمّل APK

---

## ✅ الطريقة 3: Capacitor (للمطورين) — APK احترافي

### المتطلبات:
- Node.js: https://nodejs.org
- Android Studio: https://developer.android.com/studio
- Java JDK 17

### الخطوات:
```bash
# 1. افتح هذا المجلد في Terminal
cd francais_app

# 2. ثبّت المكتبات
npm install

# 3. أضف منصة Android
npx cap add android

# 4. انسخ الملفات
npx cap sync

# 5. افتح Android Studio
npx cap open android
```

### في Android Studio:
1. انتظر حتى ينتهي Gradle من التحميل
2. من القائمة: **Build > Build Bundle(s) / APK(s) > Build APK(s)**
3. ستجد الـ APK في: `android/app/build/outputs/apk/debug/app-debug.apk`

---

## 📁 هيكل الملفات

```
francais_app/
├── www/
│   └── index.html          ← التطبيق الرئيسي
├── capacitor.config.json   ← إعدادات Capacitor
├── package.json            ← مكتبات Node.js
└── README.md               ← هذا الملف
```

---

## 💡 نصائح

- **الطريقة 1** هي الأسهل إذا لم يكن لديك خبرة برمجية
- **الطريقة 3** تعطيك APK أكثر احترافية وأسرع أداءً
- عند تثبيت APK على الهاتف، فعّل **"مصادر غير معروفة"** في إعدادات الأمان

---

## 📞 دعم

إذا واجهت أي مشكلة، راسل المطور أو أعد رفع الملف على Claude للمساعدة.
