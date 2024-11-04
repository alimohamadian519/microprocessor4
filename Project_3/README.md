# آزمایش شماره3

## گزارش کار

در این آزمایش، هدف این است که با هر بار فشار دادن کلید، یک LED به طور تصادفی روشن شود. برای این کار از تولید اعداد تصادفی استفاده می‌کنیم.
---

### کد برنامه

```cpp
#define key1 digitalRead(A0)
int btn = A0;

void setup() {
  Serial.begin(9600);
  pinMode(A0, INPUT);   // مشخص کردن پین های خروجی برای 6 عدد LED
  for (int i = 8; i < 14; i++) {
    pinMode(i, OUTPUT);
  }
  randomSeed(analogRead(btn));  // افزایش ضریب اطمینان پذیری اعداد رندوم
}

void loop() {
  if (key1 == 0) {
    for (int i = 8; i < 14; i++) {
      digitalWrite(i, LOW);     
    }
    int randomNum = random(8, 14);  
    digitalWrite(randomNum, HIGH);
    Serial.println(randomNum-7);
    delay(500);
  }
}
```

---

### تصویر مدار 

<br>

<div align="center">
<img src="/pic/microprocessor_9.jpg">
</div>

---

### شماتیک مدار 

<br>

<div align="center">
<img src="/pic/schematic_8.jpg" width="600px" height="300px">
</div>
