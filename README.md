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
