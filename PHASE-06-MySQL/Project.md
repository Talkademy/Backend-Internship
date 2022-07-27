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


ممکن است نیاز شود چند جدول واسط نیز اضافه کنید. (در صورت استفاده منطق پیاده‌سازی و طراحی پایگاه‌داده را به اختصار توضیح دهید.)


برای شروع کار، نیاز است تا تعدادی داده به جدول اضافه کنید. مقادیر داده‌های وارد شده دلخواه خودتان است.



### پرسمان‌ها

- add student \<parameters\> (insert)
- add course \<parameters\> (insert)
- add professor \<parameters\> (insert)
- register student_id course_id (foreign key)
- w student_id course_id (delete)
- accept professor_id course_id (foreign key)
- change student_id fave (update)
- score professor_id student_id \<score\> (update)
- view students gpa \<score\> (select) - مشاهده‌ی دانشجویانی با وضعیت کل حداقل score

</div>
