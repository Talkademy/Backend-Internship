<div dir="rtl" align="justify">

# فاز چهار : الگوهای طراحی و لومبوک

## الگوهای طراحی

 در این فاز می‌خواهیم به صورت اجمالی با الگوهای طراحی آشنا شویم تا بتوانیم ساختارمندی کد خود را بالا ببریم. همچنین با کتابخانه lombok آشنا می‌شویم و از مزیت‌های آن برای آنکه کد کمتری بزنیم بهره می‌بریم.

1.  مقدمه‌ای بر الگوهای طراحی 
   
   تاریخچه‌ی الگوهای طراحی به سال‌ها قبل برمی‌گردد زمانی که آقایی به نام Christopher Alexander که یک مهندسی عمران بود، متوجه می‌شود در ساخت و ساز‌های خود برخی اصول و الگوها مرتبا تکرار می‌شوند. بنابراین تصمیم گرفت که یک راهنمایی بنویسد تا افراد مختلف بتوانند از این دانسته‌ها استفاده کنند و زمان کمتری صرف بهبود بخش‌هایی کنند که پیش‌تر مسیرشان طی شده است.
 
 ۱۵ سال پیش، متخصصین حوزه‌ی نرم‌افزار تصمیم گرفتند تا چنین روالی را برای برنامه‌نویسی نیز پیاده‌سازی کنند که نهایتا منتهی به انتشار کتاب [Design Patterns: Elements of Reusable Object-Oriented Software in 1995 by Erich Gamma](https://school.hbh7.com/pdfs/RPI/Erich%20Gamma%2C%20Richard%20Helm%2C%20Ralph%20Johnson%2C%20John%20M.%20Vlissides%20-%20Design%20Patterns_%20Elements%20of%20Reusable%20Object-Oriented%20Software%20%20-Addison-Wesley%20Professional%20%281994%29.pdf) شد که حاوی ۲۳ قاعده بود و قرار است در این دوره‌ی کارآموزی با برخی از این قواعد آشنا شوید.
 
   ممکن است برای شما سوال پیش بیاید که الگوهای طراحی چه دردی را دوا می‌کنند؟
 
 مزیت اول که به صورت ضمنی هم به آن اشاره داشتیم، استفاده از راهکار‌های آزموده شده برای مسائل مشخص است. در فازهای بعدی که برنامه‌های پیچیده‌تر و با جزئیات بیشتر خواهید نوشت این دغدغه را بیشتر درک خواهید کرد.
 
 مزیت دوم این است که الگوهای طراحی، مانند یک زبان مشترک، درک متقابل توسعه‌دهندگان را از کدهای یکدیگر افزایش می‌دهد. توجه داشته باشید که در پروژه‌های مقیاس صنعتی، برنامه‌نویسی گروهی بسیار متداول است و نتیجتا افراد باید حتی‌الامکان از نوشته‌های دیگران درک کافی داشته باشند. 
   اکنون که این نیازمندی را لمس کرده‌اید، به بررسی برخی الگوها می‌پردازیم.
 
2. الگوهای ایجادی
   
   الگوهای نوع اول، مربوط به مسائلی درباره‌ی نحوه ایجاد اشیاء هستند. برای مثال آیا استفاده از `Constructor` همواره مناسب است یا راه‌های جایگزینی نیز وجود دارند؟ در این مقطع، یادگیری الگو‌های زیر پیشنهاد می‌شود
   - [Singleton](https://refactoring.guru/design-patterns/singleton)
   - [Builder](https://refactoring.guru/design-patterns/builder)

برای آشنایی بیشتر و بهره بردن از این الگوهای طراحی می‌توانید این   الگو‌های پر کاربرد را نیز مطالعه کنید
   - [Prototype](https://refactoring.guru/design-patterns/prototype)
   - [Factory Method](https://refactoring.guru/design-patterns/factory-method)

   
3. الگوهای ساختاری
   
   این الگوها قصدشان ارائه‌ی یک راه‌حل برای ترکیب اشیاء مختلف برای ساختن یک ساختار یا واحد بزرگتر است.

   مطالعه این دو الگو می‌تواند برای شما مفید باشد
- [Bridge](https://www.javatpoint.com/bridge-pattern)
- [Proxy](https://www.javatpoint.com/proxy-pattern)

برای مطالعه بیشتر می‌توانید این الگوها را مشاهده نمایید
- [Adapter](https://refactoring.guru/design-patterns/adapter)
- [Composite](https://refactoring.guru/design-patterns/composite)

4. الگوهای رفتاری
   
   این دسته الگوها جهت سازمان‌دهی رفتار برنامه استفاده می‌شود. به عبارتی هدف این قسمت کاهش Hardcoding و وابستگی بیش از حد اشیاء به هم است. 

   برای آشنایی بیشتر با این دسته مطالعه الگو زیر پیشنهاد می‌شود.
- [Observer](https://refactoring.guru/design-patterns/observer)

   برای مطالعه بیشتر می‌توانید این الگوها را نیز مطالعه کنید. 
- [Command](https://www.javatpoint.com/command-pattern)
- [Chain of Responsibility](https://www.javatpoint.com/chain-of-responsibility-pattern)
- [Iterator](https://www.javatpoint.com/iterator-pattern)
- [Interpreter](https://www.javatpoint.com/interpreter-pattern)
- [State](https://www.javatpoint.com/state-pattern)
- [Template](https://www.javatpoint.com/template-pattern)

## لومبوک
لومبوک یک کتابخانه جاوا است که به طور خودکار به ویرایشگر شما متصل می شود و ابزارهایی را ایجاد می کند که شما را از کدهای تکراری و خسته کننده نجات می‌دهد.
 
 شما با استفاده از این کتابخانه سرعت کدنویسی خود را چندبرابر می‌کنید بدون آنکه کیفیت کد شما پایین بیاید . در ضمن لومبوک به شما کمک می‌کند که با حذف  [Boilerplate Code](https://en.wikipedia.org/wiki/Boilerplate_code) خوانایی کد خود را بالاتر ببرید.

برای آشنایی بیشتر با لمبوک می‌توانید به لینک زیر مراجعه نمایید

[آشنایی با Lombok](https://javacup.ir/introduction-to-lombok/)

## پروژه فاز چهار
در این فاز شما با مراجعه به کدی که در فاز یک  توسعه‌دادید. می‌توانید کدهای خود را اصلاح‌کنید و از الگوی طراحی Builder و کتابخانه Lombok استفاده نمایید.

</div>