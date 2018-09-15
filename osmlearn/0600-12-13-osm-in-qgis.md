---
layout: page
permalink: /osm-qgis/
title: "استفاده از داده‌های OSM در QGIS"
description: آموزش گام به گام OpenStreetMap .
category: 'learnosm'
tags:
- osm
- learnosm
---

<h1>استفاده از داده‌های OSM در QGIS</h1>
<blockquote>
<p>این راهنما را می‌توان به صورت  <a href="/hotosm/learnosm/blob/gh-pages/files/Using_OSM_data_in_QGIS_fa.odt">Using_OSM_data_in_QGIS_fa.odt</a> و یا <a href="/hotosm/learnosm/blob/gh-pages/files/Using_OSM_data_in_QGIS_fa.pdf">Using_OSM_data_in_QGIS_fa.pdf</a> دانلود کرد.<br>
تاریخ بازبینی ۱۳۹۴/۰۴/۲۸</p>
</blockquote>
<p>QGIS (که قبلاْ کوانتوم GIS نامیده میشد) یک سیستم اطلاعات جفرافیایی کامل  و متن‌باز و بین پلتفرمی با ویژگی‌های بسیار است. با QGIS هرزمان که بخواهید می‌توانید به داده‌های OSM دسترسی داشته باشید، مشخص کنید که کدام تگ‌ها را درنظر بگیرد و به راحتی از آنها به صورت یک پایگاه داده SQLite جمع و جور یا Shapefile خروجی بگیرید.</p>
<p>در این بخش ما کارهایی که لازم است تا اینها صورت پذیرد را نشان میدهیم. فرض می‌کنیم که شما قبلاً QGIS 2.x را دانلود و نصب کرده‌اید. اگر اینطور نیست می‌توانید آنرا از <a href="http://www.qgis.org/en/site/forusers/download.html" rel="nofollow">http://www.qgis.org/en/site/forusers/download.html</a> دانلود کنید.</p>
<p>برای داشتن لایه‌های کاملاً به روز و مورد نظر ما در QGIS ابتدا آخرین داده‌های OSM را به صورت خام و قالب <strong>.osm</strong> دریافت می‌کنیم. سپس، آنها را به شکل پایگاه داده SQLite نبدیل می‌کنیم که یک سیستم پایگاه داده سبک است که در یک فایل روی سیستم شما نگهداری می‌شود. در آخر، لایه‌(یا چند لایه)ای را ایجاد می‌کنیم که شامل تنها نوع خصوصیت و تگی است که ما می‌خواهیم به آن دسترسی داشته باشیم. این لایه‌ها را می‌توان در QGIS به همان صورت و یا به صورت قالب دیگری مانند shapefile ذخیره کرد.</p>
<h2><a id="user-content-دستیابی-به-دادههای-osm" class="anchor" aria-hidden="true" href="#دستیابی-به-دادههای-osm"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>دستیابی به داده‌های OSM</h2>
<p>اولین چیزی که بایست انجام بدیم این است که داده‌های به‌روز OSM را بگیریم. این کار را به چندین روش می‌توان انجام داد.
مسلم است که تقاضای داده از سرور OSM مانند آنچه که در JOSM انجام می‌دهیم، محدود میباشد و ما نمی‌توانیم
مقدار زیادی از داده را یکجا دریافت کنیم - بهرحال همانطور که در فصلهای پیشین
در <a href="/osm-data/getting-data">دریافت داده‌های OSM</a> و <a href="/osm-data/geofabrik-and-hot-export">استفاده از Geofabrik و خروجی HOT</a> توضیح داده شده روشهای زیادی برای دریافت مجموعه داده‌های بزرگ وجود دارد.</p>
<p>در این راهنما از تابع درونزاد دانلود خود QGIS استفاده می‌کنیم.</p>
<p>QGIS را باز کنید به Vector -&gt; OpenStreetMap -&gt; Download Data... بروید
در اینجا از چندین انتخاب پیش رو می‌توانید یکی را انتخاب کنید - اگر پنجره شما قبلاً محدوده‌ای
که شما می‌خواهید را نشان می‌دهد چک باکس کنار "From map canvas" را علامت بزنید. چنانچه لایه صحیحی در QGIS بارگزاری شده است
"From layer" را علامت بزنید و لایه‌ای که می‌خواهید استفاده کنید را انتخاب کنید. ما در اینجا "Manual" را انتخاب می‌کنیم
و طول و عرض جغرافیایی که کادر محدوده اطراف منطقه‌ای
را که می‌خواهیم دسترسی داشته باشیم وارد می‌کنیم. می‌توانید طول و عرض جغرافیایی محل مورد علاقه خود را وارد کنید اما به یاد داشته باشید که محدوده
نمی‌تواند خیلی بزرگ باشد و نمی‌توانید همه داده‌ها را دانلود کنید.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/osm-data/bounding_box.png"><img src="/hotosm/learnosm/raw/gh-pages/images/osm-data/bounding_box.png" alt="کادر محدوده" style="max-width:100%;"></a></p>
<p>یک نام و محل برای فایل خروجی انتخاب کنید و OK را بزنید، پسوند فایل <strong>.osm</strong> خواهد بود.
اگر دانلود کامل شود به شما اعلام می‌شود. "Close" را بزنید تا از کادر محاوره‌ای دانلود
خارج شوید.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/osm-data/download_complete.png"><img src="/hotosm/learnosm/raw/gh-pages/images/osm-data/download_complete.png" alt="دانلود کامل شد" style="max-width:100%;"></a></p>
<p>حالا داده‌های OSM در محلی که انتخاب کرده‌اید ذخیره شده است.</p>
<p>این روش دستیابی به داده‌های OSM شبیه آن چیزی است که در JOSM و یا خود
سایت <a href="http://www.openstreetmap.org" rel="nofollow">openstreetmap.org</a> از آن استفاده می‌شود. برای داده‌های بزرگتر و به روزتر،
می‌توانید از <a href="http://export.hotosm.org" rel="nofollow">سایت خروجی HOT</a> و یا</p>
<blockquote>
<p><a href="http://extract.bbbike.org/" rel="nofollow">bbbike.org</a> استفاده کنید. به یاد داشته باشید که چنانچه فایل فشرده OSM را دانلود کنید
ابتدا باید آنرا از حالت فشرده خارج و به قالب <strong>.osm</strong> تبدیل کنید تا بتوانید سایر مراحل را انجام دهید.</p>
</blockquote>
<h2><a id="user-content-وارد-کردن-دادهها-به-sqlite" class="anchor" aria-hidden="true" href="#وارد-کردن-دادهها-به-sqlite"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>وارد کردن داده‌ها به SQLite</h2>
<p>حالا ما باید فایل خام <strong>.osm</strong>مان را به پایگاه داده SQLite وارد کنیم.</p>
<p>به Vector -&gt; OpenStreetMap -&gt; Import Topology from XML بروید
در اولین مرحله، فایل <strong>.osm</strong>تان را انتخاب کنید.
اگر می‌خواهید می‌توانید نام پایگاه خروجی را تغییر دهید.
علامت مربع کنار "Create Connection..." را دست نزنید</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/osm-data/import_dialog.png"><img src="/hotosm/learnosm/raw/gh-pages/images/osm-data/import_dialog.png" alt="وارد کردن داده‌ها" style="max-width:100%;"></a></p>
<p>OK را کلیک کنید.
پس از اتمام کار "Close" را بزنید.</p>
<h2><a id="user-content-ایجاد-لایهها" class="anchor" aria-hidden="true" href="#ایجاد-لایهها"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>ایجاد لایه‌ها</h2>
<p>دست آخر لایه‌هایی را که در QGIS استفاده خواهد شد بر اساس نیازهایمان تعریف می‌کنیم.</p>
<p>به Vector -&gt; OpenStreetMap -&gt; Export Topology to SpatiaLite بروید
در اولین مرحله، پایگاه داده‌ای که در مرحله قبل ایجاد کرده بودید را انتخاب کنید.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/osm-data/input_db_file.png"><img src="/hotosm/learnosm/raw/gh-pages/images/osm-data/input_db_file.png" alt="واردکردن فایل db" style="max-width:100%;"></a></p>
<p>در قسمت "Export type" نوع خصوصیات نقشه‌ای که می‌خواهید برای آنها لایه ایجاد کنید را انتخاب کنید. در اینجا
ما لایه حاوی چندضلعی‌ها را درست می‌کنیم.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/osm-data/export_type.png"><img src="/hotosm/learnosm/raw/gh-pages/images/osm-data/export_type.png" alt="نوع خروجی" style="max-width:100%;"></a></p>
<p>اگر مایلید نام لایه را تغییر دهید.</p>
<p>قسمت "Exported tags" جایی‌ست که معجزه اصلی رخ می‌دهد. در اینجا تگ‌هایی که می‌خواهیم در لایه
خروجی ما وجود داشته باشند را انتخاب می‌کنیم. این موضوع قابلیت انتخاب نوع داده‌ای که ما می‌خواهیم به آنها
دسترسی داشته باشیم را به ما می‌دهد.</p>
<p>روی "Load from DB" کلیک کنید تا فهرستی از همه تگ‌های موجود در پایگاه داده را ببینید. اندازه پنجره را با نگه داشتن و کشیدن ماوس بر روی گوشه‌های آن بزرگتر کنید. می‌توانید
همه تگ‌ها و نیز تعداد هر تگ گنجانده شده در این داده را ببینید.
چک باکس‌های کنار هر تگ را که می‌خواهید انتخاب کنید. در اینجا ما چند مورد
که مناسب برای چند ضلعی‌هایی که ساختمان می‌باشند را انتخاب می‌کنیم.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/osm-data/export_full.png"><img src="/hotosm/learnosm/raw/gh-pages/images/osm-data/export_full.png" alt="export full" style="max-width:100%;"></a></p>
<p>پس از اتمام کار OK را کلیک کنید.
کادر را ببندید. لایه شما به طور خودکار اضافه خواهد شد.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/osm-data/cairo_polygons.png"><img src="/hotosm/learnosm/raw/gh-pages/images/osm-data/cairo_polygons.png" alt="چندضلعی‌های قاهره" style="max-width:100%;"></a></p>
<p>بر روی لایه راست کلیک کنید و "Open Attribute Table" را بزنید.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/osm-data/open_attribute_table.png"><img src="/hotosm/learnosm/raw/gh-pages/images/osm-data/open_attribute_table.png" alt="جدول بازکردن خصوصیات" style="max-width:100%;"></a></p>
<p>در اینجا می‌بینید که جدولی داریم که شامل ویژگی‌هایی‌ست که انتخاب کرده‌ایم.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/hotosm/learnosm/blob/gh-pages/images/osm-data/attribute_table.png"><img src="/hotosm/learnosm/raw/gh-pages/images/osm-data/attribute_table.png" alt="جدول ویژگی‌ها" style="max-width:100%;"></a></p>
<p>توجه کنید که لایه‌ای <strong>تنها</strong> شامل ساختمان‌ها نساختیم. درعوض، لایه‌ای ساخته‌ایم که
شامل همه چندضلعی‌های داده‌های اصلی ماست ولی فقط تگ‌های
انتخاب شده را شامل می‌شود. برای ساختن فیلتری برای این لایه تا فقط ساختمان‌ها نشان داده شوند بایستی یک کوئری اجرا شود که
فقط چندضلعی‌هایی را که تگ building=yes را فیلتر کند.</p>
<h2><a id="user-content-خلاصه" class="anchor" aria-hidden="true" href="#خلاصه"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>خلاصه</h2>
<p>این پروسه دریافت داده‌های به روز از OSM و قراردادن آنرا به QGIS را آسان می‌کند. به محض اینکه
لایه اینچنینی در QGIS داشته باشید می‌توانید آنها را به صورت shapefiles ذخیره کنید، فیلتر و کوئری را اجرا کنید،
و غیره. برای اطلاع از جزئیات این کارها منوی Help برنامه QGIS را ببینید.</p>
