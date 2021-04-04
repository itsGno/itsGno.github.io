# Broken Access Control

`Broken Access Control` เป็นหนึ่งในประเภทของช่องโหว่ที่มีการเจอใน application ไม่ว่าจะเป็น Web application, Mobile application, Desktop application ดังนั้น การพัฒนา Software ให้มีความมั่นคงปลอดภัยจากช่องโหว่นั้นเราควรมารู้จักว่าช่องโหว่ `Broken Access Control`คืออะไร

`Broken Access Control` เป็นช่องโหว่ที่มักจะเกิดขึ้นเมื่อ application ขาดการตรวจสอบสิทธิ์ในการใช้งาน/เข้าถึง function, ข้อมูลต่าง ๆ ที่อยู่ในระบบเช่น ผู้ใช้งาน A เป็นพนักงานขององค์กรหนึ่ง ซึ่งทางองค์กรใช้ Software หนึ่งในการทำงานโดยทุกคนในองค์กรต้องใช้ Software ตัวนี้ แต่ปรากฏว่า นาย A สามารถเข้าถึงและใช้งาน Function บาง Function ที่อนุญาตให้เฉพาะ `Admin` เท่านั้นที่จะสามารถใช้งานได้

ซึ่งช่องโหว่ Broken Access Control ไม่สามารถตรวจหาช่องโหว่ชนิดนี้ได้ด้วย Tools Automate ดังนั้นจึงต้องอาศัยการทำ Manual test เพื่อตรวจสอบจะทำให้สามารถตรวจเจอช่องโหว่ชนิดนี้

## วิธิการป้องกัน

- ตั้งค่า Access Control ให้มีการรับค่า Key บางอย่างที่ถูกต้องการอนุญาตให้ใช้งาน Server-Sider Service (API)
- ปฏิเสธการเข้าถึงข้อมูลทั้งหมด ยกเว้นที่เป็น ข้อมูลสาธารณะ
- พัฒนากระบวนการกำหนด Access Control และใช้งานเพื่อควบคุมสิทธิ์การเข้าถึงภายใน Application ทั้งหมด
- สร้างและกำหนด User Matric เพื่อตรวจสอบสิทธิ์ในการใช้งานว่าผู้ใช้สิทธิ์ใดควรเข้าถึง Resource ได้มากแค่ไหน



## อ้างอิง

https://owasp.org/www-project-top-ten/2017/A5_2017-Broken_Access_Control

https://hdivsecurity.com/owasp-broken-access-control

