<div dir='rtl' align="justify">
<font face='XB Zar'>

<center>

سامانه درخواست خودرو - ۳
========================

</center>

<font size=4>

در این فاز قصد داریم تا ساختار کلاینت - سروری ایجاد کنیم و شما با کمک `Spring Boot` و معماری `REST` این مطلوب را پیاده‌سازی خواهید کرد. در این فاز شما یک کد سرور می‌نویسید و کلاینت‌های خود را با استفاده از [Postman](https://www.postman.com/) مدیریت می‌کنید. در نهایت، سرورهای شما نیز بایکدگیر تعامل خواهند داشت. در صورتی که راننده‌ای یافت نشد، هر سرور از دیگری کمک می‌گیرد.

</font>

درخواست‌ها و پاسخ‌ها
==================

##### ورود متقاضی

<div dir='ltr'>


##### Request

```json
GET /customer/login
** Query **
mobile_no:<mobile_no>
```

##### Response

```json
200 OK
{
    "passcode":<passcode>
}
```

</div>

##### ثبت‌نام راننده

<div dir='ltr'>


##### Request

```json
POST /driver/register
{
    "username":<username>,
    "password":<password>,
    "plateNo":<plate number>
}
```

##### Response

```json
200 OK
```

</div>

##### ورود راننده

<div dir='ltr'>


##### Request

```json
POST /driver/login
{
    "username":<username>,
    "password":<password>
}
```

##### Response

```json
200 OK
{
    "driverId":<driverId>
}
```

</div>

##### درخواست خودرو

<div dir='ltr'>


##### Request

```json
GET /customer/order
** Query **
customer_id:<customer_id>
```

##### Response

```json
200 OK
{
    "driverId": <driverId>,
    "orderId":  <orderId>
}
```

</div>

در صورت در دسترس نبودن راننده (در سرور گیرنده‌ٔ درخواست) ابتدا می‌بایست از سرورهای دیگر نیز سوال کند (از طریق درخواست‌های با معماری REST). پس نتیجتا چند دقیقه می‌بایست کلاینت معطل شود تا جواب مناسب بگیرد.

درصورت که راننده‌ای آزاد نبود، پاسخ زیر ارسال شود:

<div dir='ltr'>

##### Response

```json
404 NOT FOUND
```

</div>

##### اتمام سفر

<div dir='ltr'>


##### Request

```json
GET /driver/done
*** Query ***
driver_id:<driver_id>
```

##### Response

```json
200 OK
```

</div>

درصورتی که سفر فعالی برای راننده وجود نداشت پاسخ زیر ارسال شود:

<div dir='ltr'>

##### Response

```json
404 NOT FOUND
```

</div>

##### لغو سفر

<div dir='ltr'>


##### Request

```json
GET /customer/discard
**** Query ****
customer_id:<customer_id>
```

##### Request

```json
GET /driver/discard
driver_id:<driver_id>
```

##### Response

```json
200 OK
```

</div>

درصورتی که سفری وجود نداشت پاسخ زیر ارسال شود:

<div dir='ltr'>

##### Response

```json
404 NOT FOUND
```

</div>

درصورتی که سفر در حال انجام بود پاسخ زیر ارسال شود:

<div dir='ltr'>

##### Response

```json
403 Forbidden
```

</div>

ملاحضات
======

1. `passcode` تولید شما در ورود متقاضی، می‌بایست پس از زمان معقولی (بین ۱ تا ۳ دقیقه) منقضی شود.
2. وظیفه‌ی تصمیم‌گیری درمورد نحوه‌ی استفاده از MySQL و یا Redis بر عهده‌ی شماست.
3. توجه کنید که assign شدن راننده‌ای از سرویس دیگر، برای کلاینت شما نباید مشکلی ایجاد کند. کلاینت همچنان به شما متصل خواهد بود ولی شما به عنوان واسطه عمل می‌کنید.
4. درخواست‌ها و پاسخ‌های عنوان شده صرفا حداقل‌ها هستند. در صورت نیاز، می‌توانید درخواست‌های دیگری نیز ایجاد کنید.
5. در مواردی که نوع خطا ذکر نشده است، شما خود باید آن را تعیین کنید. حالات مختلف را مشخص کرده و `HttpStatus` مناسب برگردانید.

</font>

</div>