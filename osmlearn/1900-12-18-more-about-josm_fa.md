---
layout: page
permalink: /more-josm/
title: "فرآیند ویرایش در JOSM"
description: آموزش گام به گام OpenStreetMap .
category: 'learnosm'
tags:
- osm
- learnosm
---


<h1>فرآیند ویرایش در JOSM</h1>
<blockquote>
<p>این راهنما را می‌توان به صورت <a href="/hotosm/learnosm/blob/gh-pages/files/josm_more-about-josm_fa.odt">josm_more-about-josm_fa.odt</a> و یا <a href="/hotosm/learnosm/blob/gh-pages/files/josm_more-about-josm_fa.pdf">josm_more-about-josm_fa.pdf</a> دانلود کرد.<br>
تاریخ بازبینی ۱۳۹۴/۰۴/۳۱</p>
</blockquote>
<p>در بخش قبل شما
JOSM را نصب کردید و شروع به کشیدن اولین نقطه‌ها، خطوط و شکلها کردید.
تعاریف پیش‌فرض را به این اشیاء اضافه کردید تا اطلاعاتی درباره ماهیت آنها به
آنها اضافه کنید. دست آخر توانستید نقشه خودتان را در JOSM بکشید.</p>
<p>تا به حال تمرین خوبی داشتیم و اکنون آماده‌ایم تا OpenStreetMap را ویرایش کنیم.</p>
<p>در این بخش ما نگاه کاملتری به رابط کاربری JOSM خواهیم انداخت و می‌بینیم
که چگونه از آن برای ویرایش نقشه OpenStreetMap استفاده می‌کنیم.</p>
<h2><a id="user-content-چرخه-ویرایش" class="anchor" aria-hidden="true" href="#چرخه-ویرایش"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>چرخه ویرایش</h2>
<p>ویرایش OpenStreetMap در JOSM شبیه ویرایش آن با ویرایشگر iD که
قبلاً دیده‌ایم می‌باشد. اما از آنجا که JOSM یک برنامه تحت دستکتاپ است
کمی متفاوت‌تر کار می‌کند. روند ویرایش و افزودن به OpenStreetMap با
JOSM به طور کلی به صورت زیر است:</p>
<ol>
<li><strong>دانلود</strong> نقشه جاری از OSM</li>
<li><strong>ویرایش</strong> آن با استفاده از تصاویر ماهواره‌ای، GPS، برگه‌های میدانی و یادداشتها به عنوان راهنما</li>
<li><strong>ذخیره</strong> تغییرات در OpenStreetMap</li>
</ol>
<h2><a id="user-content-دانلود-دادههای-osm" class="anchor" aria-hidden="true" href="#دانلود-دادههای-osm"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>دانلود داده‌های OSM</h2>
<p>اولین گام در ویرایش نقشه دانلود داده‌های آن ناحیه از جهان است که
تصمیم به بهبود آن دارید. به یاد داشته باشید که اینکار را هربار که می‌خواهید
در نقشه تغییری ایجاد کنید بایستی انجام دهید زیرا نقشه دائما توسط کاربران دیگر در حال به‌روزرسانی می‌باشد.</p>
<p>روی “File” درگوشه بالا و چپ JOSM کلیک کرده و سپس "Download from OSM"
رابزنید. اینکارپنجره دانلود را باز می‌کند همچنین جهت سهولت کار
می‌توانید روی دکمه‌ای که در این شکل نشان داده شده
کلیک کنید:</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/josm/josm_download-button.png"><img src="/hotosm/learnosm/raw/gh-pages/images/josm/josm_download-button.png" alt="JOSM Download Button" style="max-width:100%;"></a></p>
<p>پس از باز شدن پنجره دانلود، نقشه را با کادر صورتی رنگی
در آن می‌بینید اگرنقشه را نمی‌بینید، روی زبانه‌ای که "Slippy map" نوشته<br>
کلیک کنید.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/josm/josm_download-dialog.png"><img src="/hotosm/learnosm/raw/gh-pages/images/josm/josm_download-dialog.png" alt="JOSM Download Dialog" style="max-width:100%;"></a></p>
<p>کادر صورتی رنگ منطقه‌ای است که می‌خواهید
جهت ویرایش دانلود کنید. از ماوس جهت بزرگنمایی و حرکت نقشه استفاده کنید و به منطقه‌ای
که کاملاً آشنا هستید مانند محله یا شهر خود بروید.
کنترل‌ها دقیقاً مانند کنترل‌های پنجره نقشه JOSM هستند. کلید راست ماوس
باعث جابجایی نقشه و کلید چرخان وسط آن موجب تغییر بزرگنمایی
می‌شود.</p>
<blockquote>
<p>گاهی اوقات کار کردن با یک لپتاپ و انجام عمل
تغییر بزرگنمایی نقشه مشکل است. کار کردن با JOSM در صورت داشتن ماوس بسیار راحت تر است،
اما در بسیاری از لپ‌تاپهای جدید امکان استفاده از تاچ‌پد وجود دارد.</p>
</blockquote>
<p>اطراف ناحیه‌ای که می‌خواهید دانلود کنید کادر صورتی رنگ را بکشید. برای کشیدن کادر جدید، روی نقشه
کلیک کنید، کلید چپ ماوس را پائین نگه دارید و ماوس را بکشید تا
کادر را رسم کنید. برای اتمام کشیدن کادر کلید ماوس  را رها کنید.
زمانی که از موقعیت و اندازه کادر خود راضی شدید، کلید
"Download" را در پائین پنجره بزنید. JOSM داده‌ها را
برای این ناحیه از OpenStreetMap دانلود میکند و پنجره نقشه را برای
ویرایش باز می‌کند.</p>
<p>###افزودن تصاویر ماهواره‌ای
چنانچه با ما هنگام اضافه کردن اولین نقطه‌ها با ویرایشگر iD همراه بودید،
حتماً به خاطر دارید که زیر داده‌های نقشه تصاویر ماهواره‌ای وجود داشت که به ما کمک می‌کرد
تا اشیاء روی زمین را تشخیص دهیم. این تصاویر از Microsoft Bing بود که
بسیار سخاوتمندانه تصاویر ماهواره‌اش را در اختیار کاربران OpenStreetMap قرار داده تا به عنوان مرجع
در هنگام مشارکت در نقشه از آنها استفاده کنند.</p>
<p>برای اضافه کردن تصاویر ماهواره‌ای بینگ به JOSM، از منوی بالایی روی "Imagery"
کلیک کرده و "Bing Sat" را انتخاب کنید.</p>
<blockquote>
<p>اگر Bing Sat را در منوی Imagery نمی‌بینید بایستی آنرا
از روی تنظیمات JOSM فعال کنید. به Edit -&gt; Preferences بروید و روی آیکنی که
“WMS TMS” نوشته کلیک کنید. شاید لازم باشد روی فلش پائین کلیک کنید تا آنرا پیدا کنید.
<a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/josm/josm_preferences-up-down.png"><img src="/hotosm/learnosm/raw/gh-pages/images/josm/josm_preferences-up-down.png" alt="JOSM Preferences up down" style="max-width:100%;"></a>
<a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/josm/josm_preferences-wms-tms.png"><img src="/hotosm/learnosm/raw/gh-pages/images/josm/josm_preferences-wms-tms.png" alt="JOSM Preferences WMS TMS" style="max-width:100%;"></a>
روی “Bing Sat” کلیک کنید و سپس “Activate” را بزنید.</p>
</blockquote>
<p>###گردش در JOSM
حالا که ما داده‌های OpenStreetMap را دانلود کرده و تصاویر ماهواره‌ای را اضافه کردیم،
بیایید نگاه مجددی به رابط کاربری JOSM بیاندازیم.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/josm/josm_layout.png"><img src="/hotosm/learnosm/raw/gh-pages/images/josm/josm_layout.png" alt="JOSM layout" style="max-width:100%;"></a></p>
<p>پنجره اصلی که از قبل با آن آشنا هستید - پنجره نقشه است و<br>
جایی است که بیشتر کارها در آن اتفاق می‌افتد. اینجا می‌توانید
داده‌های OpenStreetMap را ببینید و ویرایش کنید.</p>
<p>در طرف راست پنجره نقشه، یک سری پانل وجود دارد که هرکدام
کاربرد خودش را دارد. معمولاً در اولین نصب JOSM بعضی
از آنها به طور پیشفرض نشان داده می‌شوند مانند پانل لایه‌ها، خصوصیات،
و انتخاب. وقتی که نقطه، خط یا شی را در نقشه انتخاب می‌کنید،
آن مورد در پانل Selection (انتخاب) نمایش داده می‌شود. اطلاعات در خصوص<br>
آن مورد در پانل Properties (خصوصیات) و نام کاربری که
آن مورد را ایجاد کرده است در پانل Authors نمایش داده می‌شود.</p>
<p>این پانلها را می‌توان با کلیک روی دکمه‌های متنوعی که
در قسمت چپ و پائین JOSM وجود دارند باز یا بسته کرد. در بالای این کلیدها در سمت چپ و بالا ابزارهایی هستند که می‌توانند
کاری را که با ماوس انجام می‌دهید تغییر دهند. قبلاً با چند تا از اینها آشنا شده‌اید:
ابزار انتخاب و ابزار ترسیم. زیر آنها ابزارهایی وجود دارند که کار
بزرگنمایی، حذف یک شی، ترسیم شکل و یا ایجاد خط موازی
با خط دیگر را تسهیل می‌کنند.</p>
<h2><a id="user-content-ویرایش" class="anchor" aria-hidden="true" href="#ویرایش"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>ویرایش</h2>
<p>خب حالا ما اولین گام در فرآیند ویرایش یعنی دانلود کردن را انجام دادیم. همچنین
JOSM را آماده کردیم تا تصاویر ماهواره‌ای را به عنوان مرجع قرار بدهد. گام بعدی ویرایش
نقشه و افزودن چیزهای جدید به آن است.</p>
<p>بسته به ناحیه‌ای که برای دانلود انتخاب کرده‌اید، ممکن است
داده‌های نقشه کم یا زیادی وجود داشته باشد. اما توجه داشته باشید که همانند همان نوع
داده‌هایی هستند که قبلاًدیده بودیم - نقطه، خط و شکل.</p>
<p>از روشهایی که قبلاً یاد گرفته‌اید چند مورد از
مواردی که میشناسید به نقشه اضافه کنید. اگر اشکالی می‌بینید سعی کنید تا آنرا رفع کنید.
نیاز نیست خیلی شلوغ  کاری کنید. اگر از چیزی مطمئن نیستید
بهتر است که آنرا به حال خود رها کنید و به آن دست نزنید.
اگر می‌خواهید نقطه‌، خط یا شکلی را جابجا کنید،
از <strong>ابزار انتخاب</strong>  استفاده کنید. روی مورد کلیک کنید و آنرا با ماوس
به جایی که باید باشد حرکت دهید. این کار برای اصلاح موقعیت اشیایی که
درمکان ناصحیح قرار دارند به کار میرود.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/josm/josm_select-tool.png"><img src="/hotosm/learnosm/raw/gh-pages/images/josm/josm_select-tool.png" alt="JOSM select tool" style="max-width:100%;"></a></p>
<p>از <strong>ابزار ترسیم</strong> استفاده کنید تا نقطه، خط یا شکل جدیدی بکشید.
هرکدام از این اشیا را با استفاده از منوی Presets همانگونه که
در بخش قبلی دیدید توصیف کنید.</p>
<blockquote>
<p>هیچگاه خارج از محدوده‌ای که دانلود کرده‌اید را ویرایشنکنید.<br>
منطقه‌ای که دانلود شده به صورت مستطیل به رنگ سیاه یکنواخت مشخص می‌باشد،<br>
در حالیکه مناطق دانلود نشده خطوط هاشور خورده کج دارند.</p>
</blockquote>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/josm/josm_area-downloaded.png"><img src="/hotosm/learnosm/raw/gh-pages/images/josm/josm_area-downloaded.png" alt="JOSM area downloaded" style="max-width:100%;"></a></p>
<h2><a id="user-content-تغییرات-را-ذخیره-کنید" class="anchor" aria-hidden="true" href="#تغییرات-را-ذخیره-کنید"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>تغییرات را ذخیره کنید</h2>
<p>سومین و آخرین گام برای تکمیل ویرایش‌های ما، آپلود تغییرات داده شده
به پایگاه داده OpenStreetMap می‌باشد. برای ذخیره تغییرات بایستی
به اینترنت متصل بود.</p>
<p>از منوی بالا روی “File” و سپس روی “Upload Data” کلیک کنید. اینکار
پنجره آپلود را باز می‌کند.  برای دسترسی
راحتتر به این پنجره می‌توانید روی دکمه آپلود که به شکل زیر است، کلیک کنید:</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/josm/josm_upload-button.png"><img src="/hotosm/learnosm/raw/gh-pages/images/josm/josm_upload-button.png" alt="JOSM Upload Button" style="max-width:100%;"></a></p>
<p>درپنجره‌ای که باز  میشود لیست کلیه اشیایی که
اضافه کرده‌اید یا تغییر داده‌اید و یا حذف کرده‌اید نمایش داده می‌شوند. در کادر
پائین صفحه از شما خواسته می‌شود تا توضیحی درباره تغییراتی که
انجام داده‌اید بنویسید. درباره تغییراتتان شرحی بنویسید.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/josm/josm_upload-dialog.png"><img src="/hotosm/learnosm/raw/gh-pages/images/josm/josm_upload-dialog.png" alt="JOSM Upload Dialog" style="max-width:100%;"></a></p>
<p>روی “Upload Changes” کلیک کنید.</p>
<p>اگراولین باری است که تغییرات را در OpenStreetMap ذخیره می‌کنید، از شما خواسته می‌شود که
نام کاربری و رمز OpenStreetMapتان را وارد کنید.
آنها را در پنجره‌ای که ظاهر می‌شود وارد کنید. اگر مربع
این پنجره را تیک بزنید، نام کاربری و رمز شما ذخیره می‌شود و
نیازی به وارد کردن مجدد آنها در دفعات بعدی نمی‌باشد. روی “Authenticate” کلیک کنید.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/josm/josm_authenticate.png"><img src="/hotosm/learnosm/raw/gh-pages/images/josm/josm_authenticate.png" alt="JOSM Authenticate" style="max-width:100%;"></a></p>
<p>لازم است که چند ثانیه‌ای برای آپلود شدن تغییرات صبر کنید،
و سپس کار تمام است! شما نقشه  OpenStreetMap را ویرایش کردید.</p>
<blockquote>
<p>در زمان ویرایش، همیشه اظمینان حاصل کنید که تغییرات خود را قبل از بستن JOSM آپلود کرده‌اید.<br>
حتی اگر ویرایش‌های بیشتری می‌خواهید انجام دهید تغییرات خود را آپلود کنید،<br>
و سپس به این فرآیند بعداً هرزمان که وقت داشتید ادامه دهید.<br>
دوست ندارید که کارهایی که کردید از بین بروند!</p>
</blockquote>
<h2><a id="user-content-تغییرات-خود-را-در-نقشه-ببینید" class="anchor" aria-hidden="true" href="#تغییرات-خود-را-در-نقشه-ببینید"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>تغییرات خود را در نقشه ببینید.</h2>
<p>مرورگر اینترنت را باز کنید و به سایت <a href="http://openstreetmap.org/" rel="nofollow">http://openstreetmap.org/</a> بروید.
نقشه را به منطقه‌ای که ویرایش کردید جابجا کنید.
می‌بینید که تغییرات شما در نقشه ظاهر می‌شوند! اگر چیزی ندیدید،
دکمه‌های CTRL+R را با هم بزنید تا صفحه وب را بارگزاری مجدد کنید. گاهی اوقات
نقشه به درستی به‌روز نمی‌شود و بایستی آنرا بارگزاری مجدد کرد.
اگرتغییرات خود را ندیدید چه می‌شود؟ نگران نباشید - چند
دقیقه‌ای زمان می‌برد تاتغییرات دیده شوند. همچنین بررسی کنید که
اضافات خود را به درستی در JOSM به درستی وارد کرده‌اید. قاعده
کلی این است که اگر نقطه شما در JOSM دارای آیکن میباشد،
روی وبسایت OpenStreetMap هم بایستی دارای همان نماد باشد.</p>
<h2><a id="user-content-خلاصه" class="anchor" aria-hidden="true" href="#خلاصه"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>خلاصه</h2>
<p>حالا که فهمیدید چطور می‌توان به OpenStreetMap اضافه کرد، بعدش میشه چیکار کرد؟ خب، ویرایش
خیلی عالیه، اما تنها جنبه نقشه سازی نیست. مسلماً نیاز دارید که
به محیط بیرون رفته و درباره مواردی که روی زمین هست اطلاعات
جمع‌آوری کنید.</p>