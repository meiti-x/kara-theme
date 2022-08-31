# تیتر یک



این یک محتوای آزمایشی برای نمایش قابلیتهای ***markdown*** هست.

## تیتر دو

### تیتر سه

#### تیتر چهار

##### تیتر پنج

###### تیتر شش



# بلاک کد

```php
// BAD
class AreaCalculator
{
    protected $shapes;

    public function __construct($shapes = [])
    {
        $this->shapes = $shapes;
    }

    public function sum()
    {
        foreach ($this->shapes as $shape) {
            if (is_a($shape, 'Square')) {
                $area[] = pow($shape->length, 2);
            } elseif (is_a($shape, 'Circle')) {
                $area[] = pi() * pow($shape->radius, 2);
            }
        }
        return array_sum($area);
    }
}

// GOOD
class AreaCalculator
{
    public function sum()
    {
        foreach ($this->shapes as $shape) {
            // get area function from child(DIP)
            $area[] = $shape->area();
        }
        return array_sum($area);
    }
}
```

# نقل قول

> بازآی که تا به خود نیازم بینی
>
> بیداریِ شبهایِ درازم بینی
>
> نی نی غلطم که خود فراقِ تو مرا
>
> کِی زنده رها کند که بازم بینی
>
> -- <cite>**مولوی**</cite>



# سبک های متن

این یک متن آزمایشی برای سبک های *تاکیدی*، **بولد**، ==هایلایت==، متن ^بالانوشت^، متن ~پایین‌نوشت~ ، `تکه کد`، ~~خط خورده~~، [لینک]() و ریاضی :
$$
![\Large x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}]
$$
و تصویر : 

![](/home/mahdi/Dropbox/Documents/Software engineering/assets/HOC.jpg)


# لیست ها

## ترتیبی

1. عنوان یک
2. عنوان دوم

## غیر ترتیبی

- عنوان یک
- عنوان دو

## چک لیست

- [ ] یه کار خفن
- [x] خوندن کتاب
- [x] جلسه امشب
- [ ] یه کار باحال

## تو در تو

1.  یک کار مهم
   1. زیر کار
      1. زیر زیر کار
         - عنوان زیر زیر زیر کار
         - [ ] یه کار خفن
         - [x] خوندن کتاب
      2. زیر زیر کار ۲
   2. زیر کار ۲
2.  یک کار مهم ۲

# جدول

| نام فیلم(راستچین) | سال انتشار(وسط چین) | امتیاز از ده(چپ چین) |
| ----------------: | :-----------------: | :------------------- |
|     فیلم شماره یک |      **۱۴۰۰**       | **۱۰**               |
|      فیلم شمار دو |      **۱۴۰۱**       | **۹.۸**              |

# جدول محتوا

[TOC]

