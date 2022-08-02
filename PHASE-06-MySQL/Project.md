<div dir="rtl" align="justify">

<center>

کار با JDBC
=========================

</center>

هدف این تمرین آشنایی شما با شیوه‌ی کار با JDBC در جاوا است. 

### خواسته

برنامه‌ای بنویسید و در آن جداولی برای دانشجوها، درس‌ها و اساتید در نظر بگیرید. سپس پرسمان‌های زیر را انجام دهید. (پرسمان Create)

##### دانشجو

- شماره دانشجویی
- نام و نام خانوادگی
- درس مورد علاقه
- وضعیت مشروطی
- نمره‌ی کل

##### استاد
- شناسه‌ی استاد
- نام و نام خانوادگی

##### درس
- شماره درس
- نام درس
- ظرفیت

دقت کنید هر دانشجو برای هر درسی که باید یک استاد ارائه می‌شود یک نمره دارد. 

ممکن است نیاز شود چند جدول واسط نیز اضافه کنید. (در صورت استفاده منطق پیاده‌سازی و طراحی پایگاه‌داده را به اختصار توضیح دهید.)


برای شروع کار، نیاز است تا تعدادی داده به جدول اضافه کنید. مقادیر داده‌های وارد شده دلخواه خودتان است.



### پرسمان‌ها

- add student \<parameters\> (insert)
- add course \<parameters\> (insert)
- add professor \<parameters\> (insert)
- accept professor_id course_id (foreign key)
- register student_id course_id (foreign key)
- deleteCourse student_id course_id (delete)
- change student_id fave (update)
- score professor_id student_id \<score\> (update)
- view average \<score\> for course_id(select,avg)
- view students gpa \<score\> (select) - مشاهده‌ی دانشجویانی بانمره کل حداقلscore  
- view student count for ech favourite course(select,group by) - برای هر درسی ، تعداد دانشجویانی که این درس موردعلاقه آن‌ها بوده نمایش داده شود.


اضافه کردن پرسمان‌های اضافه‌ی دیگر مانعی ندارد.

</div>
