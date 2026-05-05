# 🚀 خطوات النشر على GitHub (مجاني)

## الخطوة 1: إنشاء حساب GitHub
1. اذهب إلى [github.com](https://github.com)
2. اضغط Sign Up
3. أملأ البيانات الخاصة بك

## الخطوة 2: تثبيت Git

### على Windows:
1. اذهب إلى [git-scm.com](https://git-scm.com/download/win)
2. اضغط على أحدث نسخة وحمّلها
3. اتبع خطوات التثبيت (اضغط Next)
4. افتح Command Prompt واكتب:
```bash
git --version
```
إذا ظهر إصدار = التثبيت نجح ✅

### على Mac:
```bash
brew install git
```

### على Linux:
```bash
sudo apt install git
```

## الخطوة 3: إنشاء Repository على GitHub

1. اذهب لـ [github.com/new](https://github.com/new)
2. اكتب اسم: `alpha-net-store`
3. اختر: Public
4. اضغط Create Repository

## الخطوة 4: رفع الملفات

افتح Command Prompt/Terminal في مجلد الموقع وشغّل:

```bash
# إعداد Git
git init
git add .
git commit -m "Initial commit - Alpha Net Store"

# ربط مع GitHub (استبدل YOUR_USERNAME و YOUR_REPO)
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/alpha-net-store.git
git push -u origin main
```

## الخطوة 5: فتح الموقع

بعد الرفع، الموقع سيكون متاح على:
```
https://username.github.io/alpha-net-store/
```

---

## 🔐 نصائح الأمان

❌ لا تضع في الملفات:
- كلمات سر حقيقية
- مفاتيح API خاصة
- بيانات شخصية

✅ بدلاً من ذلك:
- استخدم متغيرات environment
- استخدم Firebase Security Rules
- استخدم ملفات .gitignore

---

## ✨ نشر سريع بدون Git

إذا أردت نشر بدون تثبيت Git:

1. اذهب إلى [github.com/new](https://github.com/new)
2. أنشئ repository
3. اختر "uploading an existing file"
4. اسحب وأفلت الملفات
5. اضغط Commit

---

**هذا كل شيء! الموقع الآن على الإنترنت! 🎉**
