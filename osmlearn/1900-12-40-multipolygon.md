---
layout: page
permalink: /multi-polygon/
title: "ریلیشن پُر کاربرد multipolygon"
description: ریلیشن پُر کاربرد multipolygon 
category: 'learnosm'
tags:
- osm
- learnosm
image: "/assets/img/osmedit.png"
---

## ریلیشن پُر کاربرد multipolygon

خیلی وقت بود که میخواستم یه آموزش در مورد ریلیشن پُر کاربرد مولتی پلیگون بذارم اما متأسفانه فرصتش پیش نیومد تا امشب. 😊

اجازه بدین قبل از مولتی پلیگون خود پلیگون رو توضیح بدم تا بیشتر با مفهوم مولتی پلیگون آشنا بشیم.

 > ترجمه کلمه‌ی #پلیگون (#polygon) "چند ضلعی" هست و به معنی هر محیط بسته‌ای هست که با یکسری خط محدود شده است. (ما چند ضلعی باز نداریم)
 
و اما مولتی_پلیگون (#multipolygon) که البته تلفظ صحیحش مالتی پلیگون هست. اگه به معنی کلمه‌ی مشابه مولتی ویتامین دقت کنین معنی مولتی پلیگون رو کاملاً درک خواهید کرد. مولتی ویتامین، که همه‌ی ما باهاش آشنا هستیم، به معنی ترکیب ویتامین‌ها و کنار هم قرارگیری تعداد زیادی ویتامین هست، مولتی پلیگون هم دقیقاً به همین معنا یعنی به معنی ترکیب پلیگون‌ها و کنار هم قرارگیری متعدد پلیگون‌ها هست.
وقتی چند پلیگون کنار هم قرار میگیرن (به شکلی که دارای مرز مشترک باشن) و یا داخل هم قرار میگیرن (به شکلی که مرزها با هم تماسی ندارن) از این ریلیشن استفاده میشه. طبق یک قاعده‌ی کُلی هر عارضه‌ای که با پلیگون قابل رسم باشه با مولتی پلیگون هم قابل رسمه. ولی موارد بسیار زیادی داریم که با پلیگون قابل رسم نیستن و برای رسمشون حتماً باید از مولتی پلیگون استفاده کرد.
تا اینجای بحث ما مفهوم مولتی پلیگون رو فهمیدیم، حالا میریم سراغ بحث شیرین ریلیشن 😉 که ترجمه‌ی کلمه‌ش میشه "رابطه". #ریلیشن (#relation) در OSM در واقع یک قرارداد و تعریفه که نوع ارتباط بین چند عضو، و نقش هر عضو در این رابطه رو مشخص میکنه، و یک چیز فیزیکی نیست که قابل رویت باشه و مشکل اکثر ادیتورها با همین غیر قابل رویت و غیر ملموس بودنشه. اما نتیجه‌ی یک ریلیشن قابل رویته. یعنی مثلاً وقتی ما یک ساختمان که وسطش یک محوطه و فضای خالی وجود داره (مثلاً حیاط خونه‌های قدیمی که در وسطشون قرار داره) رو با ریلیشن مولتی پلیگون رسم میکنیم نتیجه‌ی کار قابل رویت هست. امیدوارم مفهوم ریلیشن رو متوجه شده باشین. 😊
حالا میریم سراغ #ریلیشن_مولتی_پلیگون که ما میتونیم اونو در #josm مستقيماً از سربرگ presets و بعد relations انتخاب و ایجاد کنیم. بعد از کلیک روی new relation و ایجاد ریلیشن یک صفحه باز میشه که دو قسمت کُلی داره،
قسمت بالا (Tags) مربوط به تگهای خود ریلیشن میشه که میتونیم ببینیم که تگ type=multipolygon بصورت پیش فرض از قبل به ریلیشن داده شده، سایر تگهای مربوط به عارضه‌ای که داریم با این ریلیشن رسمش میکنیم هم در همین قسمت باید وارد بشن. (مثلاً اگه یه ساختمونه باید تگ building=yes و سایر تگهای مربوطه در این قسمت وارد بشن) 
قسمت پایین (Members) مربوط به اعضا و نقش هر عضو در ریلیشن میشه، اگر شما قبل از ایجاد ریلیشن عضوها رو انتخاب کرده باشین در این قسمت نشون داده میشن و تنها کاری که باید بکنین مشخص کردن نقششون در ریلیشنه، اگر عضوها رو انتخاب نکردین چیزی در این قسمت نیست و خالیه، اما جای نگرانی نیست شما میتونین همین الآن عضوها رو انتخاب کنین. با انتخاب عضوها اونا در قسمت selection (پایین سمت راست) دیده میشن. با زدن اولین فلش در این قسمت عضوهای انتخابی وارد ستون سمت چپ میشن و سپس شما میتونین نقش عضوها رو براشون مشخص کنین...
کُل نقش‌های (role) موجود در این ریلیشن دو تا هستن، نقش outer و inner، یعنی هر عضو در این ریلیشن یا نقش outer داره یا inner، که البته نقش inner میتونه وجود نداشته باشه. مرزهای خارجی عارضه نقش outer میگیرن و مرزهای داخلی عارضه نقش inner. مثلاً در رسم یک خونه‌ی قدیمی که قبلاً به عنوان مثال ذکر شد مرز خارجی کُل خونه نقش outer میگیره و مرز داخلی که مربوط به حیاط هست نقش inner میگیره. به زبان دیگه میشه اینجوری گفت که عارضه‌ی ما داخل پلیگونی قرار میگیره که ضلع‌هاش نقش outer دارن و خارج پلیگونی قرار میگره که ضلع‌هاش نقش inner دارن.
در مورد رسم عوارضی که در مجاورت هم قرار دارن و مرز مشترک دارن و لزوماً از یک جنس نیستن هم از این ریلیشن استفاده میشه. برای مثال یک پارکینگ و محوطه یک تالار عروسی رو در نظر بگیرین که با یک دیوار از هم جدا شدن، دیوار مرز مشترک این دو عارضه هست، دیوار رو با یک خط رسم میکنیم و تگ barrier=wall رو بهش میدیم و بعد دو عارضه پارکینگ و تالار رو با دو ریلیشن مولتی پلیگون جداگانه ایجاد میکنیم و این دیوار در هر دو ریلیشن (بصورت جداگانه) نقش outer رو خواهد داشت. در مواردی یک عضو میتونه در یک ریلیشن نقش outer و در ریلیشن دیگه‌ای نقش inner رو داشته باشه، مثلاً در مثال قبل فرض کنید یک ساختمان نگهبانی در وسط پارکینگ وجود داشته باشه، مرز این ساختمان در ریلیشن مربوط به پارکینگ نقش inner و در ریلیشن مربوط به خود ساختمان نقش outer رو خواهد داشت.