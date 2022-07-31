<div dir="rtl" align="justify">

فاز هفت: Redis
=====

در فاز هفتم با  [Redis](https://redis.io/documentation)  که یک پایگاه داده‌ی غیر رابطه‌ای محسوب می‌شود آشنا می‌شویم.
1. مقدمه
   
   همانطور که احتمالا در پرسش اول فاز قبل بررسی کرده‌اید، انواع مختلفی از پایگاه داده‌های غیررابطه‌ای وجود دارد که یکی از آن‌ها فرم کلید-مقدار (key-value) است. Redis یک نمونه از همین خانواده است. همچنین این پایگاه داده درون-حافظه‌ای (in-memory) است و از همین جهت سرعت دسترسی به داده‌های آن به مراتب سریع‌تر از دسترسی به فضای ذخیره‌سازی ثانویه (Secondary storage: HDD/SSD) است. اکنون در گام‌های زیر با اجزای Redis آشنا می‌شویم.

2. نصب و راه‌اندازی

   Redis نیز مشابه MySQL نیاز به سرور و کلاینت دارد. برای نصب آن می‌توانید [این راهنما](https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-redis-on-ubuntu-20-04) را مطالعه کنید و گام به گام پیش‌روید. مجددا توصیح می‌شود که با کلاینت CLI آن دوست شوید و به آن عادت کنید اما درصورتی که در این مقطع جهت شهود بهتر با GUI راحت‌تر هستید می‌توانید [RDM](https://snapcraft.io/redis-desktop-manager) را بر روی سیستم خود نصب کنید.

3. انواع داده‌ها
   
   Redis طیف وسیعی از کلید‌ها را پشتیبانی می‌کند که مهم‌ترین آن‌ها رشته‌ها، لیست‌ها، مجموعه‌ها و هش‌ها هستند. پیشنهاد می‌شود [این مستند](https://redis.io/topics/data-types-intro) که نوشته‌ی تیم فنی Redis است مطالعه کنید و مثال‌های آن (به‌ویژه چهار مورد اول) را جهت تمرین خود انجام دهید.

4. دستورها
   
   فهرست تمامی دستور‌های Redis از [این مستند](https://redis.io/commands) در دسترس است اما نیازی به تسلط به تمامی آن‌ها وجود ندارد. آنچه که شما بهتر است در این فاز یاد بگیرید در پایین لیست شده‌است.
5. کار با Jedis

   با توجه به اینکه برنامه‌نویسی  دوره‌ی بک‌اند عموما مبتنی بر جاوا است، برای ارتباط با پایگاه داده‌ی Redis نیاز به یک واسط داریم که یکی از آن‌ها `Jedis‍` است. برای درک عملکرد این واسط می‌توانید از [این مثال](https://www.javacodegeeks.com/2013/10/getting-started-with-jedis.html) بهره ببرید.
   
نوع داده‌ها در Redis و دستورهای کاربردی
==============

به صورت کلی می‌توان اشیاء Redis را به صورت زیر دسته‌بندی کرد:

- String
- Key
  
  - `SET KEY VALUE`
  - `DEL KEY`
  - `EXISTS KEY`
  - `EXPIRE KEY`
  - `RENAME KEY N_KEY`
- Hash
  
  - `HMSET KEY [VALUES...]`
  - `HGETALL KEY`
  - `HDEL KEY [FIELDS]`
  - `HEXIST KEY FIELD`
  - `HGET KEY FIELD`
- List
  
  - `LPUSH KEY [VALUES...]`
  - `LRANGE KEY START_INDEX END_INDEX`
  - `LPOP KEY`
  - `LREM KEY COUNT VALUE`
  - `LSET KEY INDEX VALUE`
- Set
  
  - `SADD KEY [VALUES...]`
  - `SCARD KEY`
  - `SDIFF KEY_1 [KEY_i...]`
  - `SINTER KEY_1 [KEY_i...]`
  - `SPOP KEY`
  - `SMOVE SRC_KEY DST_KEY MEMBER`
- Sorted Set
  
  - `ZADD KEY [SCORE MEMBER...]`
  - `ZCARD KEY`
  - `ZCOUNT KEY MIN_SCORE MAX_SCORE`
  - `ZRANK KEY MEMBER`


وظایف شما
=========
1. پرسش‌های نظری
   
   با توجه به صورت مسئله‌ی [پروژه‌ی اول](../PHASE-09-Project-1/Readme.md) خود، به سوالات زیر پاسخ دهید.
   1. آیا اساسا نیازی به استفاده از هر دو نوع پایگاه داده وجود دارد؟ چرا؟ توجه کنید در صورتی که از هر دو استفاده می‌کنید می‌بایست حجم داده‌ی بسیار کمتری در Redis نگه دارید (در قیاس با MySQL) و نمی‌توانید همه‌ی داده‌های خود را در حافظه ذخیره کنید.
   2. چه مواردی برای ذخیره‌سازی در MySQL مناسب‌تر اند؟
   3. چه مواردی برای ذخیره‌سازی در Redis مناسب‌تر اند؟
2. تبدیل MySQL به Redis
   
   برای تسلط بیشتر روی دستورهای مطرح شده (و موارد بیشتر که می‌توانید از [این لینک](https://www.javatpoint.com/redis-commands) ببینید) پرسمان‌های MySQL زیر را به Redis تبدیل کنید و در [لیست وظایف](TaskList.md) ثبت کنید.

<div dir="ltr">

- Query 1
```SQL
insert into Products (id, name, description, price)
values (10200, “ZXYW”,“Description for ZXYW”, 300);
   ```

- Query 2
```SQL
select * from Products where id = 10200
   ```

- Query 3
```SQL
select * from Product where price < 300
   ```

</div>

3. [تمرین عملی](Project.md)

</div>
