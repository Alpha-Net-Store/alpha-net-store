# 🔒 سياسة الأمان

## الثغرات المعالجة

### ✅ 1. XSS (Cross-Site Scripting) Protection
- استخدام `innerHTML` آمن عبر `textContent`
- دالة `esc()` تحول النصوص لـ HTML entities
- كل المدخلات يتم تنقيتها قبل العرض

### ✅ 2. URL Validation
- دالة `validateUrl()` تتحقق من صحة الروابط
- السماح فقط بـ http:// و https://
- رفض أي روابط مريبة

### ✅ 3. Rate Limiting
- تحديد محاولات الدخول (5 محاولات فقط)
- تأخير 1 ثانية بين المحاولات
- حظر الدخول بعد 5 محاولات فاشلة

### ✅ 4. Input Validation
- التحقق من طول النصوص
- التحقق من وجود البيانات المطلوبة
- التحقق من صيغة البيانات

### ✅ 5. Firebase Security
- استخدام Firestore Rules
- تقييد البيانات المكشوفة
- تشفير البيانات في الـ Transit

---

## ⚠️ الإجراءات المطلوبة

### يجب عليك فعل هذا:

1. **غيّر كلمة السر الضعيفة**
   - احالياً: `alpha2024`
   - استخدم: كلمة قوية (20+ حرف مع أرقام ورموز)

2. **أضف Firebase Security Rules**
   ```javascript
   rules_version = '2';
   service cloud.firestore {
     match /databases/{database}/documents {
       match /apps/{document=**} {
         allow read: if true;
         allow write: if request.auth != null;
       }
       match /transactions/{document=**} {
         allow read, write: if request.auth != null;
       }
     }
   }
   ```

3. **استخدم HTTPS فقط**
   - عند النشر على github.io يكون تلقائي

4. **حماية رقم الواتساب**
   - لا يمكن إخفاء الرقم تماماً (يحتاجه العملاء)
   - استخدم service worker لفحص IP

---

## 🛡️ أفضل الممارسات

- ✅ استخدم كلمات سر قوية
- ✅ فعّل اثنتين-عامل authentication على GitHub
- ✅ اختبر الموقع على XSS
- ✅ استخدم HTTPS دائماً
- ✅ عدّل الإعدادات الحساسة محلياً فقط

---

## 📞 الإبلاغ عن الثغرات

إذا وجدت ثغرة أمنية:
1. لا تنشرها علناً
2. أرسل بريد خاص على البريد المسجل

---

**آخر تحديث:** 5 مايو 2026
