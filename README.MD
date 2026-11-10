<div align="center">

# شرح إستخراج مفاتيح واجهة برمجة التطبيقات API

---

<div align="center">

<img src="img/p1.jpg"
width="90%"
style="border-radius: 20px;
border: 2px solid var(--color-border-default);
box-shadow: 0 8px 16px rgba(0,0,0,0.2);
background: var(--color-canvas-default);
padding: 5px;">

</div>

---

[![by](https://img.shields.io/badge/mmuhacker-%EF%BA%97%EF%BB%84%EF%BB%AE%EF%BB%B3%EF%BA%AE-blue?style=for-the-badge&logo=github)](https://github.com/mmuhacker)<br>
![Version](https://img.shields.io/badge/1.0-%EF%BA%8D%EF%BB%B9%EF%BA%BB%EF%BA%AA%EF%BA%8D%EF%BA%AE-blue?style=for-the-badge&logo=semver)<br>
![Platform](https://img.shields.io/badge/%EF%BB%9B%EF%BA%8E%EF%BB%9F%EF%BB%B2%20%EF%BB%9F%EF%BB%B4%EF%BB%A8%EF%BB%9C%EF%BA%B2-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=kalilinux&logoColor=%23FFC107)<br>
![Platform](https://img.shields.io/badge/%EF%BA%84%EF%BB%A7%EF%BA%AA%EF%BA%AE%EF%BB%AE%EF%BB%B3%EF%BA%AA-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=android)<br>
![Platform](https://img.shields.io/badge/%EF%BB%A7%EF%BB%88%EF%BA%8E%D9%85%20%EF%BB%A3%EF%BA%8E%D9%83-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=MAC)<br>
![Python](https://img.shields.io/badge/3.x-%EF%BA%91%EF%BA%8E%EF%BB%B3%EF%BA%9C%EF%BB%AE%EF%BB%A6-blue?style=for-the-badge&logo=python)<br>
![License](https://img.shields.io/badge/%EF%BA%97%EF%BA%AE%EF%BA%A7%EF%BB%B4%EF%BA%BA%20%EF%BA%A7%EF%BA%8E%D8%B5-%EF%BA%8D%EF%BB%9F%EF%BA%98%EF%BA%AE%EF%BA%A7%EF%BB%B4%EF%BA%BA-8A2BE2?style=for-the-badge&logo=law)<br>
![Status](https://img.shields.io/badge/%EF%BB%A7%EF%BA%B8%EF%BB%82-%EF%BA%8D%EF%BB%9F%EF%BA%A4%EF%BA%8E%EF%BB%9F%EF%BA%94-blue?style=for-the-badge&logo=statuspal)<br>

---

**📚 المحتويات**
</div>

- [نظرة عامة](#نظرة)
- [المميزات](#المميزات)
- [حالات الإستخدام](#حالات)
- [مخرجات التحليل](#مخرجات)
- [متطلبات التشغيل](#متطلبات)
- [التثبيت والتشغيل](#تثبيت)
  - [📲 تيرمكس](#تيرمكس)
  - [🐧 لينكس](#لينكس)



---

<div align="center" id="نظرة">
     
## 📋 نظرة عامة

</div>

أأداة تحليل ثابتة للملفات المشبوهة المكتوبة بلغة بايثون، تقوم بفحص الملفات المضغوطة والمشفرة (zlib + marshal) دون تنفيذ أي كود، مع استخراج جميع المؤشرات الخطرة وتحليل السلوكيات الخبيثة.

> ⚠️ **تنبيه قانوني:** هذه الأداة مخصصة للأغراض التعليمية والبحث الأمني الأخلاقي فقط. استخدمها بمسؤولية ووفقاً لقوانين بلدك.

---

<div align="center" id="المميزات">
  
## ✨ المميزات

</div>

- ✅ تحليل ثابت 100% — بدون تنفيذ أي كود مشبوه
- ✅ فك ضغط zlib + marshal واستخراج البيانات
- ✅ كشف أكثر من 150 كلمة خطرةeval, exec, os.system, requests, وغيرها
- ✅ استخراج المعرفات الحساسة:
  - 🤖 توكنات بوتات تيليجرام
  - 🔑 مفاتيح API
  - 📧 الإيميلات
  - 🌐 عناوين IP والروابط
  - 🗄️ روابط قواعد البيانات
- ✅ تحليل سلوكي ذكي — تصنيف التهديدات إلى 8 فئات
- ✅ نظام تقييم الخطر — درجة من 0 إلى 100 مع شريط تقدم
- ✅ تفكيك bytecode مع تفسير التعليمات (hex → instructions)
- ✅ إعادة بناء الكود المصدر عبر pychd (rules-only)
- ✅ تقارير مفصلة بصيغة نصية
- ✅ واجهة عربية مع دعم كامل للغة

---

<div align="center" id="حالات">
  
# 🎯 حالات الاستخدام

  </div>

- فحص الملفات المشبوهة قبل تشغيلها
- تحليل عينات البرمجيات الخبيثة (Malware Analysis)
- التدقيق الأمني للمشاريع مفتوحة المصدر
- اكتشاف محاولات التهرب والكود المشفر
- استخراج مؤشرات الاختراق (IOCs)
---

<div align="center" id="مخرجات">

# 📊 مخرجات التحليل

</div>

- **تقرير نصي** — يحتوي على جميع الاستدعاءات الخطرة والروابط
- **تفكيك bytecode** — مع تفسير التعليمات (hex → instructions)
- **كود مصدر مفكوك** — إعادة بناء الكود الأصلي (عبر pychd)
- **تحليل سلوكي** — تصنيف التهديدات حسب النوع
- **نظام نقاط** — درجة الخطر مع توصيات

---

<div align="center" id="متطلبات">

## 🏗 متطلبات التشغيل

```
python 3.10 +    # لغة بايثون أساسية لتشغيل الأداة
arabic-reshaper  # لطباعة النص العربي متصلاً
python-bidi      # لتنسيق النص العربي
arabic font      # لطباعة الحروف العربية
pychd            # إختياري لإعادة بناء الكود

```

</div>

---

<div algn="center" id="تثبيت">
  
## 🚀 التثبيت والتشغيل

</div>


<div align="center" id="تيرمكس">


***Android 📲 Termux***


</div>


- ***الخطوة الأولى***: تحديث النظام والمكتبات

```bash
pkg update && pkg upgrade -y
```

- ***الخطوة الثانية***: تثبيت بايثون إذا لم تكن مثبتة

```bash
pkg install python
```

- ***الخطوة الثالثة***: تثبيت المكتبات الأساسية المسؤولة عن طباعة النص العربي بالشكل الصحيح إذا لم تكن مثبتة لديك

``bash
pip install arabic-reshaper python-bidi
```

- ***الخطوة الرابعة***: تثبيت الخط العربي إذا لم يكن مثبتاً

```bash
curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf
termux-reload-settings
```

⚠️ **بعد تثبيت الخط يجب إغلاق تيرمكس نهائيا وإغلاقه من التطبيقات المصغَّرة في الخلفية وإعادة تشغيله ليتم إستخدام الخط في النظام بالشكل الصحيح**

- ***الخطوة الخامسة***: تثبيت pychd إختياري لبناء الكود المصدري

```bash
pip install pychd
```
- ***الخطوة السادسة***: تثبيت الأداة وإعطاء صلاحية التشغيل
- ***الخطوة السابعة***: إنشاء رابط إختصار للتشغيل
- ***تشغيل الأداة***:
   - *بالأمر الكامل*:
  ```bash
  python mud_fsc.py
  ```
   - *بالإختصار*:
  ```bash
  fsc
  ```
  **أو قم بعمل كل شيء بأمر واحد مُجمَّع**

  ```bash

  ```
  
---

<div align="center" id="لينكس">

# 🐧 توزيعات لينكس

</div>

- ***الخطوة الأولى***:
- ***الخطوة الثانية***:
- ***الخطوة الثالثة***:
- ***الخطوة الرابعة***:
- ***الخطوة الخامسة***:
- ***الخطوة السادسة***:
- ***الخطوة السابعة***:
   - *الأمر الكامل*
   - *الإختصار*

---

<div align="center" id="mac">

# نظام ماك 🍎 MAC os

</div>

- ***الخطوة الأولى***:
- ***الخطوة الثانية***:
- ***الخطوة الثالثة***:
- ***الخطوة الرابعة***:
- ***الخطوة الخامسة***:
- ***الخطوة السادسة***:
- ***الخطوة السابعة***:
   - *الأمر الكامل*
   - *الإختصار*

---

<div align="center" id="أخطاء">

# 🏣 أخطاء قد تواجهك

</div>

- **الخطأ**:<br>
**الحل**:<br>
- **الخطأ**: ظهور النص العربي متقطع ومعكوس<br>
**الحل**: تثبيت arabic-reshaper و python-bidi<br>
```bash
pip install arabic-reshaper python-bidi
```

---

<div align="center" id="إستخدام">

# 🎛 طريقة الإستخدام
</div>

