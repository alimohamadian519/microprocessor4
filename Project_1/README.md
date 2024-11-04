# آزمایش شماره1 

## گزارش کار 
سیگنال‌های دیجیتال معمولاً به حالت‌های صفر و یک (High و Low) محدود هستند، ولی گاهی نیاز به سیگنال آنالوگ داریم که بین این دو حالت تغییر کند. برای این کار، از سیگنال PWM استفاده می‌کنیم که خروجی بین ۰ تا ۲۵۵ دارد. در این آزمایش، با تولید موج‌های PWM، شدت روشنایی LED را بین حداکثر (۲۵۵) و حداقل (۰) تغییر می‌دهیم.

---

### کد برنامه 

```cpp
int led = 10;
int increase = 0;   

void setup() {
  pinMode(led, OUTPUT);
}

void loop() {
 for (int i = 0; i < 51; i++) {
  increase += 5;
  analogWrite(led, increase);
  delay(50);    
  }

  for (int i = 0; i < 51; i++) {
  increase -= 5;
  analogWrite(led, increase);
  delay(50);    
  }
}
```

---

### تصویر مدار

<br>

<div align="center">
<img src="/pic/microprocessor_7.jpg">
</div>

---

### شماتیک مدار

<br>

<div align="center">
<img src="/pic/schematic_6.jpg" width="600px" height="300px">
</div>
