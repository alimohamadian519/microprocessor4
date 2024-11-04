## آزمایش شماره2 

### گزارش کار

هدف تنظیم شدت روشنایی LED به صورت داینامیک و در لحظه است. از پتانسیومتر که نوعی مقاومت متغیر است، استفاده کردیم. با چرخاندن ولوم پتانسیومتر، ولتاژ بین ۰ تا ۵ ولت تغییر می‌کند. این ولتاژ متغیر به ورودی آنالوگ آردوینو داده می‌شود و بر اساس آن خروجی LED تنظیم می‌شود.

---

### کد برنامه

```cpp
int led = 10;
int val = 0;    

void setup() {
  pinMode(led, OUTPUT);
  Serial.begin(9600);
}

void loop() {
 val = analogRead(A0);   
 int hashVal = map(val, 0, 1023, 0, 255);  
 analogWrite(led, hashVal);
 int voltVal = map(val, 0, 1023, 0, 5); 
   Serial.println(voltVal);
   delay(2000);
}
```

---

### تصویر مدار 

<br>

<div align="center">
<img src="/pic/microprocessor_8.jpg">
</div>

---

### شماتیک مدار 

<br>

<div align="center">
<img src="/pic/schematic_7.jpg" width="600px" height="300px">
</div>
