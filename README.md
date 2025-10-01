# 🏷️ Prizo - دستیار قیمت‌یابی دیجی‌کالا

<div dir="rtl">

**Prizo** یک افزونه مرورگر قدرتمند برای دیجی‌کالا است که به شما کمک می‌کند با نمایش تاریخچه قیمت‌ها، مقایسه فروشندگان و بهینه‌سازی سبد خرید، بهترین تصمیم خرید را بگیرید.

</div>

---

## ✨ Features | امکانات

<div dir="rtl">

### 📊 پیگیری تاریخچه قیمت
- نمایش کمترین قیمت ماهانه محصولات
- نمودار تغییرات قیمت در طول زمان
- مشاهده روند افزایش یا کاهش قیمت

### 💰 مقایسه قیمت فروشندگان
- مقایسه قیمت‌های مختلف فروشندگان
- نمایش هزینه ارسال برای هر فروشنده
- محاسبه قیمت نهایی (قیمت + ارسال)
- مرتب‌سازی بر اساس بهترین قیمت

### 🛒 بهینه‌سازی سبد خرید هوشمند
- پیشنهاد بهترین ترکیب فروشندگان برای کل سبد خرید
- کاهش هزینه کل ارسال
- محاسبه خودکار صرفه‌جویی

### 📝 لیست پیگیری (Watchlist)
- افزودن محصولات به لیست پیگیری
- مشاهده تغییرات قیمت محصولات در یک نگاه
- مدیریت آسان محصولات مورد علاقه

### 🔔 اعلان‌های قیمت
- دریافت اعلان هنگام کاهش قیمت
- تنظیم حد قیمت دلخواه
- پیگیری خودکار محصولات

### 🥬 پشتیبانی از دیجی‌کالا فرش
- نمایش اطلاعات قیمت برای محصولات فرش
- پیگیری قیمت مواد غذایی تازه

### 🎨 رابط کاربری زیبا و کاربرپسند
- طراحی مدرن و ساده
- سازگار با طراحی دیجی‌کالا
- عملکرد سریع و بدون اختلال

</div>

---

## 📸 Screenshots | تصاویر

<div dir="rtl">

_تصاویر نمایشی به زودی اضافه می‌شوند_

<!-- Add screenshots here:
- Product page with price history
- Seller comparison view
- Smart cart optimization
- Watchlist interface
- Popup menu
-->

</div>

---

## 🚀 Installation | نصب

<div dir="rtl">

### برای Chrome، Edge، Brave

1. آخرین نسخه را از صفحه [Releases](https://github.com/zanasaed/prizo-extension/releases) دانلود کنید
2. فایل zip را در یک مکان دائمی استخراج کنید
3. مرورگر خود را باز کرده و به آدرس زیر بروید:
   - Chrome: `chrome://extensions/`
   - Edge: `edge://extensions/`
   - Brave: `brave://extensions/`
4. گزینه "Developer mode" را در گوشه بالا سمت راست فعال کنید
5. روی "Load unpacked" کلیک کنید
6. پوشه استخراج شده حاوی فایل‌های افزونه را انتخاب کنید
7. افزونه Prizo باید در لیست افزونه‌های شما نمایش داده شود

### برای Firefox

1. آخرین نسخه `.xpi` یا `.zip` را از صفحه [Releases](https://github.com/zanasaed/prizo-extension/releases) دانلود کنید
2. Firefox را باز کرده و به `about:addons` بروید
3. روی آیکون چرخ‌دنده کلیک کرده و "Install Add-on From File..." را انتخاب کنید
4. فایل دانلود شده را انتخاب کنید
5. هنگام درخواست نصب، روی "Add" کلیک کنید

**نکته:** برای نصب موقت در Firefox جهت تست:
1. به `about:debugging#/runtime/this-firefox` بروید
2. روی "Load Temporary Add-on" کلیک کنید
3. فایل `manifest.json` را از پوشه استخراج شده انتخاب کنید

</div>

---

## 📖 Usage | نحوه استفاده

<div dir="rtl">

1. **بازدید از دیجی‌کالا**: پس از نصب، به [Digikala.com](https://www.digikala.com/) بروید
2. **مشاهده قیمت‌ها**: در صفحه محصول، اطلاعات تاریخچه قیمت به صورت خودکار نمایش داده می‌شود
3. **مقایسه فروشندگان**: در لیست فروشندگان، قیمت‌ها به صورت خودکار مقایسه و مرتب می‌شوند
4. **استفاده از Popup**: روی آیکون افزونه در نوار ابزار کلیک کنید تا منوی تنظیمات و watchlist را ببینید
5. **بهینه‌سازی سبد خرید**: در صفحه سبد خرید، دکمه "بهینه‌سازی سبد خرید" را کلیک کنید

</div>

---

## 🛠️ Technical Details | جزئیات فنی

<div dir="rtl">

- **Manifest Version**: 3 (MV3)
- **Supported Browsers**:
  - Chrome 102+
  - Firefox 109+
  - Edge 102+
  - Brave (latest)
- **Permissions**:
  - `activeTab`: برای تعامل با صفحات دیجی‌کالا
  - `storage`: برای ذخیره تنظیمات و داده‌های کاربر
  - `notifications`: برای اعلان‌های قیمت
  - `alarms`: برای بررسی دوره‌ای قیمت‌ها
- **Host Permissions**: دسترسی به دیجی‌کالا برای دریافت اطلاعات قیمت

</div>

---

## 📝 Changelog | تاریخچه تغییرات

<div dir="rtl">

برای مشاهده تاریخچه کامل نسخه‌ها و تغییرات، به فایل [CHANGELOG.md](CHANGELOG.md) مراجعه کنید.

</div>

---

## 🤝 Support & Contribution | پشتیبانی و مشارکت

<div dir="rtl">

### گزارش مشکلات
اگر مشکلی پیدا کردید یا پیشنهادی دارید، لطفاً از طریق [GitHub Issues](https://github.com/zanasaed/prizo-extension/issues) با ما در میان بگذارید.

### حمایت مالی
اگر از این افزونه استفاده می‌کنید و می‌خواهید از توسعه آن حمایت کنید:

☕ [Buy Me a Coffee](https://www.coffeebede.com/zanasaed)

💙 یا از طریق کریپتو:
- **Bitcoin (BTC)**: `bc1qlf5rq26hfw95acrrxkjh4atezksxcvsx73qnsd`
- **Ethereum (ETH)**: `0x0F15d9fCD78C303868B8D36862504feD1A935aCC`
- **Polygon (POL)**: `0x0F15d9fCD78C303868B8D36862504feD1A935aCC`
- **SOLANA (SOL)**: `Cr7cxHZqnSz1t5YWxdNTzJ3ZcEZ1DyZ9dfez7E1qTWjh`

</div>

---

## 👨‍💻 Author | سازنده

<div dir="rtl">

**Zana Saedpanah**

- GitHub: [@zanasaed](https://github.com/zanasaed)
- Email: zanadeveloper@gmail.com

</div>

---

## 📄 License | مجوز

<div dir="rtl">

این پروژه تحت مجوز MIT منتشر شده است. برای جزئیات بیشتر به فایل [LICENSE](LICENSE) مراجعه کنید.

</div>



[⬆ بازگشت به بالا](#-prizo---دستیار-قیمتیابی-دیجیکالا)

</div>
