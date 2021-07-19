<div dir="rtl" align="justify">

# JOIN

دستور JOIN در MySQL برای بازیابی اطلاعات از چند جدول استفاده‌ می‌شود.
چندین نوع JOIN وجود دارد :
- INNER JOIN
- LEFT OUTER JOIN (LEFT JOIN)
- RIGHT OUTER JOIN (RIGHT JOIN)
- CROSS JOIN

## INNER JOIN 
پر استفاده‌ترین نوع JOIN می‌باشد و در این نوع تمام دیتاهای که شرط اتصال را برقرار کنند برگردانده می‌شوند.

فرمت دستور INNER JOIN به صورت زیر می باشد 

<div dir="ltr">
         
      ```sql	
        SELECT columns
        FROM table1 
        INNER JOIN table2
        ON table1.column = table2.column;
      ```     
</div>

## LEFT JOIN 
این نوع از JOIN تمام ردیف‌های از جدول مشخص شده در سمت چپ در واژه ON و تمام ردیف های سمت راست که شرایط اتصال برقرار باشد را برمی‌گرداند.

فرمت دستور LEFT JOIN به صورت زیر می باشد 

<div dir="ltr">
         
      ```sql	
        SELECT columns
        FROM table1
        LEFT [OUTER] JOIN table2
        ON table1.column = table2.column;
      ```     
</div>

## RIGHT JOIN 

این نوع از JOIN تمام ردیف‌های از جدول مشخص شده در سمت راست در واژه ON و تمام ردیف های جدول سمت چپ که شرایط اتصال برقرار باشد را برمی‌گرداند.

فرمت دستور RIGHT JOIN به صورت زیر می باشد 

<div dir="ltr">
         
      ```sql	
        SELECT columns
        FROM table1
        RIGHT [OUTER] JOIN table2
        ON table1.column = table2.column;
      ```     
</div>

## CROSS JOIN
 بر خلاف اتصال INNER, LEFTو RIGHT در اتصال CROSS هیج قسمت شرطی وجود ندارد. اتصال CROSS به صورت ضرب کارتیزانی است به این صورت که اگر در یک جدول ۵ ردیف و در جدول دیگر ۴ ردیف وجود داشته باشد نتیجه اتصال CROSS برابر ۲۰ ردیف می‌باشد. 

 فرمت دستور CROSS JOIN به صورت زیر می باشد 

<div dir="ltr">
         
      ```sql	
        SELECT select_list
        FROM table_1
        CROSS JOIN table_2;
      ```     
</div>

# UNION

عملگر UNION برای تجمیع کردن نتایج در دو یا چند کوئری مجزا استفاده می‌شود.

در استفاده از این عملگر براید به موارد زیر دقت شود

-  هر دو کوئری SELECT باید ستون‌ها برابر باشد.
- همچنین باید نوع داده هر ستون یکسان باشد
- همچنین ترتیب ستونها باید یکسان باشد

 فرمت دستور UNIO به صورت زیر می باشد 

<div dir="ltr">
         
      ```sql	
        SELECT column_name(s) FROM table1
        UNION
        SELECT column_name(s) FROM table2;
      ```     
</div>

برای تسلط بیشتر متن زیر را مطالعه نمایید 

[SQL UNION Operator](https://www.w3schools.com/sql/sql_union.asp)

# GROUP BY , HAVING , EXISTS



</div>