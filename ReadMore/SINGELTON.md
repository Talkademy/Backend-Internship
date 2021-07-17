<div dir='rtl' align="justify">

# singleton‬‬ ‫طراحی‬ ‫الگوی‬  
سینگلتون یک الگوی طراحی است که این اطمینان را میدهد که کلاس شما فقط یک نمونه دارد و یک نقطه‌ی دسترسی گلوبال فراهم میکند.
  
  دو مشکلی که این الگو برطرف میکند:
  
  ۱- اطمینان از داشتن تنها یک نمونه از یک کلاس: دلیل نیاز به همچین چیزی عموما کنترل دسترسی به بعضی منابع اشتراکی است مانند یک دیتابیس یا فایل

  ۲- نقطه ی دسترسی گلوبال به آن نمونه: همانند متغیر های گلوبال، سینگلتون به شما این امکان را میدهد که از هر جای برنامه به آن شی دسترسی داشته باشید. همچنین از بازنویسی(overwrite) آن توسط کد‌های دیگر جلوگیری میکند
  
  ## شیوه‌ی ساخت
کانستراکتور اصلی را private کنید تا از ساخت نمونه‌های جدید با new جلو گیری کنید
یک تابع استاتیک بسازید که مشابه یک کانستراکتور عمل میکند این تابع کانستراکتور اصلی را صدا میزند و یک شی از آن کلاس میسازد  و آن را در یک فیلد استاتیک ذخیره میکند. دفعات بعدی که این تابع صدا زده می‌شود همان شی که قبلاً ساخته شده را برمی‌گرداند. در اینجا از lazy initialization (ساخت در اولین استفاده) استفاده شده است
  
  به این نمونه کد توجه کنید:
    <div dir='ltr' align="justify">
```java
public final class ClassSingleton {

    private static ClassSingleton INSTANCE;
    private String info = "Initial info class";
    
    private ClassSingleton() {        
    }
    
    public static ClassSingleton getInstance() {
        if(INSTANCE == null) {
            INSTANCE = new ClassSingleton();
        }
        
        return INSTANCE;
    }

}
```
</div>
  
  • این الگو SRP (single resposibility principle) را نقص میکند زیرا ۲ مشکل را همزمان حل میکند.

  • میتواند طراحی بد را مخفی کند!
  
  • در محیط چندنخی نیاز به رفتار خاصی دارد که در آن چند ترد شی سینگلتون را چندبار نسازند
    
  • ممکن است تست نویسی را مشکل کند (تست خود کلاس سینگلتون)
  
  • این الگو میتواند در بعضی الگوهای دیگر نیز استفاده شود مثل factory, builder و prototype 
  
  چند مثال دیگر از این الگو (به همراه مالتی ترد) 
  
https://refactoring.guru/design-patterns/singleton/java/example

چند لینک کمکی
  
https://refactoring.guru/design-patterns/singleton
  
https://sourcemaking.com/design_patterns/singleton
  
https://www.baeldung.com/java-singleton
  
</div>
