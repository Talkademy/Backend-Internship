<div dir="rtl" align="justify">

فاز پنج : MySQL
======

در این فاز، قصد داریم شما را با یکی از پایگاه‌داده‌های رابطه‌ای [Relational Database](https://en.wikipedia.org/wiki/Relational_database) به نام [MySQL]() آشنا کنیم.
1. مقدمه
   
   همانطور که در بالا گفته شد، شما در این نوبت با MySQL آشنا خواهید شد.
   از آنجایی که اکثر RDBMS ها از زبان پرسمان سازمان‌یافته یا SQL(Structured Query Language) استفاده می‌کنند، با آشنایی با یکی از این RDBMS ها می‌توانید با صرف زمان کم نحوه استفاده از یک RDBMS جدید را فرابگیرید. همچنین SQL جزو استاندارد ANSI و ISO می‌باشد.

   RDBMS های فراوانی وجود دارند که بسته به نیاز از آن‌ها استفاده می‌شود. MySQL, SQL Server, PostgreSQL, SQLite, ... نمونه‌های از RDBMS های معروف هستند.

1. مفاهیم
   
   در ابتدا بد نیست با مفهوم تراکنش آشنا شوید. احتمالا چنین لفظی پیشتر در امور بانکی به گوشتان خورده است. تراکنش در حقیقت عملیاتی است که یا می‌بایست تمام و کمال اجرا شود و یا به هیچ‌وجه صورت نگیرد. برای مثال، در یک تراکنش بانکی ده میلیون تومانی ممکن نیست دو میلیون آن واریز شود ولی هشت میلیون آن خیر. چنین مفهومی در پایگاه‌داده نیز موجود است و به خصوصیاتی که عملیات‌های تراکنشی را ممکن می‌سازند [ACID properties](https://www.geeksforgeeks.org/acid-properties-in-dbms/?ref=leftbar-rightbar) گفته می‌شود.
   جهت تطبیق MySQL با مفاهیمی که تا به‌اینجای مستند خوانده‌اید می‌توانید از [این لینک](https://www.w3schools.com/MySQL/mysql_rdbms.asp) کمک بگیرید.

1. نصب و راه‌اندازی
   
   برای شروع به کار خود با MySQL می‌بایست هم سرور و هم کلاینت آن را بر روی سیستم خود نصب کنید. کلاینت پیش‌فرض MySQL به صرت خط-فرمان است و پیشنهاد می‌شود برای تسلط بیشتر بر روی پرسمان‌ها (Query) به این محیط خود را عادت دهید. همچنین در توسعه‌ی حقیقی نیز اغلب دسترسی‌ها از طریق Terminal بوده و امکان استفاده از برنامه‌های مجهز به GUI وجود ندارد. هرچند درصورت تمایل به مشاهده‌ی جدول‌ها و انجام پرسمان‌ها به صورت گرافیکی می‌توانید از خود IntelliJ نیز بهره ببرید.
   [این لینک](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04) می‌تواند در نصب موارد خواسته شده راهگشا باشد.
   
1. دستورات ‌SQL 

   دستورات SQL به دو دسته کلی دسته بندی می‌شوند 
   - DDL (Data Definition Language.)
   - DML (Data Manipulation Languag)
   ### DDL
   این دستورات به شما کمک می‌کنند تا ساختار یا اسکیما دیتابیس خود را تعریف کنید. زمانی که شما این دستورات را اجرا می‌کنید به دلیل اینکه auto commit هستند تغییرات بلافاصله برروی دیتابیس شما اعمال می‌شوند.

   این دستورات شامل : 
   - CREATE

      این دستورات به منظور ساخت دیتابیس و یا موجودیت‌های مثل جدول، دید، function , stored procedure, triggers و غیره  

   - DROP

      برای حذف دیتابیس و یا موجودیت‌های وابسته به دیتابیس.
      
   - ALTER

      به منظور اعمال تغییرات بروری دیتابیس و  تغییرات برروی اسکیما به منظور حذف و یا اضافه کردن ویژگی  در دیتابیس است. 

   - TRUNCATE 

      به منظور حذف تمام دیتاها از جداول  شامل ساختارها و فضای اختصاص داده‌ ‌شده به آنها می‌باشد.

   - RENAME

      به منظور تغییر نام در محتوای دیتابیس است. 
      
   برای تسلط بر این دستورات لطفا لینک‌های زیر را مطالعه کنید

   - [CREATE DATABASE](https://www.w3schools.com/MySQL/mysql_create_db.asp)
   - [CREATE TABLE](https://www.w3schools.com/MySQL/mysql_create_table.asp)
   - [DROP DATABASE](https://www.w3schools.com/MySQL/mysql_drop_db.asp)
   - [DROP TABLE](https://www.w3schools.com/MySQL/mysql_drop_table.asp)
   - [ALTER TABLE](https://www.w3schools.com/MySQL/mysql_alter.asp)
   - [PRIMARY KEY](https://www.w3schools.com/MySQL/mysql_primarykey.asp)
   - [FOREIGN KEY](https://www.w3schools.com/MySQL/mysql_foreignkey.asp)
   - [AUTO INCREMENT](https://www.w3schools.com/MySQL/mysql_autoincrement.asp)

   ### DML
   این دستوردات به منظور تغییرات بر روی دیتاهای ذخیره شده در داخل دیتابیس است و مسئول تغییر بر روی این دیتاهای است. 

   این دستورات شامل موارد زیر است 
   - SELECT
   - INSERT
   - UPDATE
   - DELETE 
   
   برای تسلط بر این دستورات لطفا لینک‌های زیر را مطالعه کنید
   - [How to Use SQL](https://www.w3schools.com/MySQL/mysql_sql.asp)
   - [SELECT](https://www.w3schools.com/MySQL/mysql_select.asp)
   - [INSERT INTO](https://www.w3schools.com/MySQL/mysql_insert.asp)
   - [UPDATE](https://www.w3schools.com/MySQL/mysql_update.asp)
   - [DELETE](https://www.w3schools.com/MySQL/mysql_delete.asp)

1. نکات بیشتر در مورد SQL
   - فیلتر کردن نتایج 

   به منظور فیلتر کردن نتایج باید از  WHERE در کوئری ها استفاده کرد به منظور تسلت بر این موضوع می‌توانید لینک زیر را مطالعه نمایید 
   
   [WHERE Clause](https://www.w3schools.com/MySQL/mysql_where.asp)

   - مرتب‌سازی نتایج 
   
   به منظور مرتب‌سازی نتایج باید می‌توانید از دستور ORDER BY استفاده نمایید . به منظور مطالعه بیشتر به لینک زیر مراجعه شود 

   [ORDER BY](https://www.w3schools.com/MySQL/mysql_orderby.asp)

   - توابع از پیش تعریف شده   

   شما در کوئری‌های خود می‌توانید از یکسری از توابع از پیش‌ تعرف شده که در زیر لیست شده‌اند استفاده نمایید:

   [MIN , MAX](https://www.w3schools.com/MySQL/mysql_min_max.asp)

   [COUNT, AVG , SUM](https://www.w3schools.com/MySQL/mysql_count_avg_sum.asp)

1. ایندکس گذاری در دیتابیس 

   دیتاها در دیتابیس‌های رابطه‌ای به اشکال مختلفی ذخیره ‌می‌شوند و جست‌وجو‌های مختلفی برروی آنها انجام ‌می‌شود. بعضی‌ها از کوئریها پر تکرار هستند و  نیاز است که عمل جست‌وجو را سریع انجام دهد و برای این کار باید  دیتاها را به صورت خاصی ذخیره کنیم که دسترسی در آینده برای ما سریع‌تر باشد. 
   یکی از موارد که به ما برای بالابردن سرعت کمک می‌کند عمل ایندکس گذاری است . عمل ایندکس کذاری بروری ستون‌های یک جدول انجام می‌شود .

   برای آشنایی لطفا به لینک زیر مراجعه شود.

   [CREATE INDEX](https://www.w3schools.com/MySQL/mysql_create_index.asp)



</div>
