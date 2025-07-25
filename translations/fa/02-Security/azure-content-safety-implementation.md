<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "1b6c746d9e190deba4d8765267ffb94e",
  "translation_date": "2025-07-16T23:15:15+00:00",
  "source_file": "02-Security/azure-content-safety-implementation.md",
  "language_code": "fa"
}
-->
# پیاده‌سازی Azure Content Safety با MCP

برای تقویت امنیت MCP در برابر تزریق پرامپت، مسمومیت ابزار و سایر آسیب‌پذیری‌های خاص هوش مصنوعی، توصیه می‌شود Azure Content Safety را یکپارچه کنید.

## یکپارچه‌سازی با سرور MCP

برای ادغام Azure Content Safety با سرور MCP خود، فیلتر ایمنی محتوا را به‌عنوان میان‌افزار در خط لوله پردازش درخواست‌ها اضافه کنید:

1. فیلتر را هنگام راه‌اندازی سرور مقداردهی اولیه کنید  
2. تمام درخواست‌های ورودی ابزار را قبل از پردازش اعتبارسنجی کنید  
3. تمام پاسخ‌های خروجی را قبل از بازگرداندن به کلاینت‌ها بررسی کنید  
4. نقض‌های ایمنی را ثبت و هشدار دهید  
5. مدیریت خطای مناسب برای بررسی‌های ناموفق ایمنی محتوا پیاده‌سازی کنید  

این کار دفاع محکمی در برابر موارد زیر فراهم می‌کند:  
- حملات تزریق پرامپت  
- تلاش‌های مسمومیت ابزار  
- استخراج داده‌ها از طریق ورودی‌های مخرب  
- تولید محتوای مضر  

## بهترین روش‌ها برای یکپارچه‌سازی Azure Content Safety

1. **فهرست‌های مسدودسازی سفارشی**: فهرست‌های مسدودسازی مخصوص الگوهای تزریق MCP ایجاد کنید  
2. **تنظیم شدت**: آستانه‌های شدت را بر اساس مورد استفاده و میزان تحمل ریسک خود تنظیم کنید  
3. **پوشش جامع**: بررسی‌های ایمنی محتوا را روی تمام ورودی‌ها و خروجی‌ها اعمال کنید  
4. **بهینه‌سازی عملکرد**: برای بررسی‌های مکرر ایمنی محتوا، کشینگ را در نظر بگیرید  
5. **مکانیزم‌های جایگزین**: رفتارهای جایگزین واضحی برای مواقعی که سرویس‌های ایمنی محتوا در دسترس نیستند تعریف کنید  
6. **بازخورد به کاربر**: هنگام مسدود شدن محتوا به دلیل نگرانی‌های ایمنی، بازخورد واضحی به کاربران ارائه دهید  
7. **بهبود مستمر**: فهرست‌ها و الگوها را بر اساس تهدیدات نوظهور به‌طور منظم به‌روزرسانی کنید

**سلب مسئولیت**:  
این سند با استفاده از سرویس ترجمه هوش مصنوعی [Co-op Translator](https://github.com/Azure/co-op-translator) ترجمه شده است. در حالی که ما در تلاش برای دقت هستیم، لطفاً توجه داشته باشید که ترجمه‌های خودکار ممکن است حاوی خطاها یا نواقصی باشند. سند اصلی به زبان بومی خود باید به عنوان منبع معتبر در نظر گرفته شود. برای اطلاعات حیاتی، ترجمه حرفه‌ای انسانی توصیه می‌شود. ما مسئول هیچ گونه سوءتفاهم یا تفسیر نادرستی که از استفاده این ترجمه ناشی شود، نیستیم.