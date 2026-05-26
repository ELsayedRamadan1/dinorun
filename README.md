# 🦖 DINO RUN — PWA

## رفع على GitHub Pages (خطوة بخطوة)

### الخطوة 1 — عمل repo على GitHub
1. افتح **github.com** وسجّل دخول
2. اضغط **New repository**
3. اسمه: `dino-run`
4. اختار **Public**
5. اضغط **Create repository**

### الخطوة 2 — رفع الملفات
**طريقة سهلة (بدون كمبيوتر):**
1. في صفحة الـ repo اضغط **uploading an existing file**
2. اسحب كل الملفات دي:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - فولدر `icons/` (كل الصور جوّاه)
3. اضغط **Commit changes**

**طريقة Git:**
```bash
git init
git add .
git commit -m "Add Dino Run PWA"
git branch -M main
git remote add origin https://github.com/USERNAME/dino-run.git
git push -u origin main
```

### الخطوة 3 — تفعيل GitHub Pages
1. في الـ repo اضغط **Settings**
2. من القائمة الجانبية اضغط **Pages**
3. تحت **Source** اختار **GitHub Actions**
4. انتظر دقيقة، هيظهر لك الـ link:
   `https://USERNAME.github.io/dino-run`

---

## تحويل لـ APK بـ PWABuilder

1. افتح **pwabuilder.com**
2. حط الـ link: `https://USERNAME.github.io/dino-run`
3. اضغط **Start**
4. هيحلل الـ PWA ويعطيك score
5. اضغط **Package for stores**
6. اختار **Android** → **Download package**
7. هتاخد ملف APK تقدر ترفعه على Play Store

---

## هيكل الملفات
```
dino-run/
├── index.html          ← اللعبة الكاملة
├── manifest.json       ← معلومات الـ PWA
├── sw.js               ← Service Worker (offline support)
├── icons/
│   ├── icon-72.png
│   ├── icon-96.png
│   ├── icon-128.png
│   ├── icon-144.png
│   ├── icon-152.png
│   ├── icon-192.png
│   ├── icon-384.png
│   ├── icon-512.png
│   └── screenshot.png
└── .github/
    └── workflows/
        └── deploy.yml  ← Auto-deploy
```

---

## نشر على Google Play Store
بعد ما تاخد الـ APK من PWABuilder:
1. افتح **play.google.com/console**
2. ادفع $25 (مرة واحدة بس)
3. Create new app
4. ارفع الـ APK
5. امليء المعلومات والصور
6. Submit for review (بياخد 3-7 أيام)
