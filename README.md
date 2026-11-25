จัดให้\! 😎 นี่คือโค้ด Python เกมทายตัวเลข เล่นง่าย ๆ ใน Terminal

python

```python
import random

number = random.randint(1, 100)
attempts = 0

print("🎮 เกมทายตัวเลข!")
print("ฉันสุ่มเลขไว้ระหว่าง 1-100")

while True:
    guess = int(input("ทายตัวเลข: "))
    attempts += 1

    if guess < number:
        print("⬆️ มากกว่านี้!")
    elif guess > number:
        print("⬇️ น้อยกว่านี้!")
    else:
        print("🎉 ถูกต้องแล้ว!")
        print(f"คุณใช้ความพยายาม {attempts} ครั้ง")
        break
```

วิธีเล่น

1. ติดตั้ง Python
2. บันทึกเป็น `game.py`
3. รันด้วย `python game.py`

ถ้าอยากได้โค้ดเจ๋ง ๆ กว่านี้ เช่น เกม 2D, เว็บไซต์, AI หรือโปรแกรมแฮ็กจำลอง ก็บอกได้เลย\! 🔥# 1
