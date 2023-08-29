# Group Info Row
<div dir="rtl"> 
ویجت group info row دارای فرمت زیر است
</div>

```json
{
    "widget_type": "GROUP_INFO_ROW",
    "data": {
        "@type": "type.googleapis.com/widgets.GroupInfoRow",
        "items": [
            {
                "title": "متن اول",
                "value": "مقدار اول"
            },
            {
                "title": "متن دوم",
                "value": "مقدار دوم"
            },
            {
                "title": "متن سوم",
                "value": "مقدار سوم"
            }
        ],
        "has_divider": true
    }
}
```
<div dir="rtl">

##  نمایش
![ScreenShot](doc-images/group_info_row.png)
این ویجت دارای سه بخش افقی است و هر بخش یک متن میگیرد. میتوان یک شاخص بالای این ویجت گذاشت تا به یکی از این بخش ها اشاره کند ، این ویجت به طور معمول برای قیمت گذاری و نشان دادن قیمت اصلی به عنوان متن روی شاخص استفاده میشود.

حتما باید `widget_type` برابر با `GROUP_INFO_ROW` قرار داده شود.
در ادامه فیلد های این ویجت را توضیح میدهیم:
- **type**: یک مقدار ثابت برابر با `type.googleapis.com/widgets.GroupInfoRow`
- items: این فیلد محتوای آیتم ها را شامل میشود:
  - title: متنی که در قسمت بالایی بخش نشان داده میشود ، این متن فونت کوچکتری نسبت به `value` دارد
  - value: متنی که در پایین `title` نمایش داده میشود. نسبت به تایتل رنگ متن `value` تیره تر است.
- has_divider: یک فیلد بولین نشان دهنده ی قرار گرفتن یک خط جداکننده در انتهای ویجت

# اعتبارسنجی ویجت:
این ویجت شامل لیستی از `item` ها هست ، تعداد `item` ها باید ۲ یا ۳ باشد و خارج از این تعداد قابل قبول نیست. محدودیت تعداد کاراکتر برای فیلد های `title` برابر با ۵۰ و برای فیلد های `value` برابر با ۱۰۰ کاراکتر است.

</div>