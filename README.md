تم بناء هذا MinGW-w64 من الكود المصدري من الصفر، لإضافة مكتبة CS50 ليتم تضمينها بشكل افتراضي في البرنامج عند استدعائها ، لتسهيل الأمر على المبتدئين، كل ما عليك فعله هو تضمين ملف cs50.h في  ملف الكود المصدري الخاص بك .c/.cpp ,ويمكنك ايضًا استخدام المكتبة في مشروع C او ++C بكل سهولة, والهدف من هذا هو تسهيل عملية تثبيت MinGW-w64 على الويندوز من خلال هذا البرنامج.
هذا المترجم يدعم الإصدارات التالية من الويندوز.
* Windows 7       x64-bit
* Windows 8.1    x64-bit
* Windows 10     x64-bit
* Windows 11     x64-bit

ملاحظة: هذا المثبت يحتوي على التالي:
* MinGW-w64 (Minimalist GNU For Windows) v10.0.0
* (GNU Compiler Collection) v12.2.0
* GDB (GNU Debugger) v12.1
* Make tool v4.4
* Binutils v2.40

وايضًا يحتوي على المكتبات التالية:
* GMP(GNU GNU Multiple Precision) v6.2.1
* MPFR(GNU Multiple Precision Floating-Point Reliable) v4.1.0
* MPC(GNU Multiple Precision Complex) Library v1.2.1
* ISL(Integer Set Library) v0.24
* ZLib v1.2.13
* ZStd(internationalization conversion) v1.5.4
* ICONV(internationalization conversion) v1.17
* CS50 Library v10.1.1

ملحوظة يجب أن يكون خيار "إضافة MinGW-64 الى متغير مسار النظام" محدد هذا لإضافة MinGW إلى متغير مسار النظام, إذا كنت ستستخدم MinGW من خلال CMD(Command Line) او Visual Studio Code
ايضًا خيار "(GDB (GNU Debugg" يجب أن يكون محدد لتثبيته من أجل VS Code.

=============================================================================================================================================================
هنا مثال بسيط على استخدام المكتبة بلغة C, قم بنسخ الكود التالي وقم بحفظه في ملف بامتداد .c
``` c++
#include <stdio.h>
#include <cs50.h>
int main() {
    int age = get_int("Please enter your age: ");
    printf("Your age in days is: %d\n", age * 365);
    return 0;
}
```
لبناء الكود من خلال الـ Command Line (cmd) اكتب التالي: gcc filename.c -o myapp.exe
ولتشغيله اكتب: filename.exe

ملاحظة يجب أن يكون مسار الـ cmd في نفس المسار الذي يحتوي على ملف الــ c. على سبيل المثال اذا كان الملف الذي يحتوي على الكود اسمه main.c في المسار C:\Test
 يجب الانتقال الى المجلد Test عن طريق كتابة الامر: cd /d C :\Test
 الطريقة الثانية سنقوم ببناءه من خلال الاداة make tool فقط اكتب: make filename بدون امتداد الملف للتشغيل اكتب: filename.exe
=============================================================================================================================================================

هنا نفس المثال بالاعلى لكن بلغة الــ C++, قم بنسخ الكود التالي وقم بحفظه في ملف بامتداد .cpp
``` c
#include <iostream>
#include <cs50.h>
int main() {
    int age = get_int("Please enter your age: ");
    std::cout << "Your age in days is: " << (age * 365);
    return 0;
}
