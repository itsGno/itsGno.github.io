# Brute force attack 

ใช้หลักการ trial-and-error (ทดลองไปเรื่อย ๆ ) เพื่อที่จะเดาข้อมูล login หรือ account ของผู้ใช้งานเพื่อให้สามารถเข้าสู่ระบบ Brute force เป็นวิธีที่ง่ายและมีอัตราความสำเร็จที่สูง

## ประเภทของ Brute Force Attack

**Simple brute force attacks** - ใช้วิธีการสุ่มไปเรื่อย ๆ ทุกความเป็นไปได้โดยไม่มีการกรองชุดusername/password ที่จะทำการสุ่ม

**Hybrid brute force attacks** - ใช้วิธีการสุ่มโดยคิดหาความเป็นไปได้ของรูปแบบของ password และทำการสุ่มไปเรื่อย ๆ 

**Dictionary attacks** - เดา username หรือ password โดยใช้ dictionary (list) ที่มีอยู่ในการหาความเป็นไปได้

**Rainbow table attacks** - rainbow table เป็น list ของผลลัพธ์ของข้อมูลที่ถูก hash (hash value) นำมาใช้เพื่อเดา password ที่ถูก hash ว่ามีค่าตรงกับค่าก่อน hash หรือไม่

**Credential Stuffing** - นำเอา username และ password ที่มีการเผยแพร่ใน internet นำมาจับคู่และทำการ login บน web application

## Hydra

Hydra เป็น tools ที่เป็นที่นิยมในการ Brute force attack ในการเด่าสุ่ม username/password โดย hydra รองรับ protocol มากกว่า 50 protocol และหลาย operating systems.

![img](https://www.imperva.com/learn/wp-content/uploads/sites/13/2018/01/hydra-brute-force-attack.png)

## วิธีการป้องกัน

ในการป้องกันการโจมตี brute force attack (password guessing) ควรบังคับผู้ใช้งานให้มีการตั้งค่ารหัสผ่านที่มีความยากในการเดาโดยประกอบไปด้วยลักษณะดังต่อไปนี้

- มีจำนวนตัวอักษามากกว่า 12 ตัวอักษร
- ผสมตัวอักษร ตัวเลข และ อักขระพิเศษ
- ไม่ใช้ password ซ้ำกับ account อื่น ๆ 

สำหรับผู้พัฒนาซอฟแวร์ หรือ administrator ควรมีการพัฒนากระบวนการที่สามารถป้องกัน brute force attack

- Lockout policy - ทำการล็อก account ที่มีพยายามที่จะ login ผิดพลาดหลายครั้ง
- Progressive delays - ทำการเพิ่มระยะเวลาในการรอการ login ครั้งต่อ ๆ ไปนานขึ้นหลังจากการ login ผิดพลาดหลาย ๆ ครั้ง
- Captcha - ใช้ reCAPTCHA เพิ่มพิสูจน์ว่าเป็นผู้ใช้งานที่เป็น คนจริง ๆ ไม่ได้เป็น tools หรือ bots ที่พยายาม login เข้าระบบ



## อ้างอิง

https://www.imperva.com/learn/application-security/brute-force-attack

https://www.kaspersky.com/resource-center/definitions/brute-force-attack

