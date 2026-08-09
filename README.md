# TurnBro Software

เว็บไซต์บริษัทพัฒนาซอฟต์แวร์จำลองสำหรับงานกลุ่มรายวิชา 960241 จัดทำโดยทีมสมาชิก 3 คน เพื่อแนะนำบริการ ผลงานจำลอง บทบาทของสมาชิก และ Portfolio รายบุคคล

## หน้าเว็บไซต์

- `index.html` - หน้าแนะนำบริษัท บริการ และกรณีศึกษาผลงาน SmartPOS, ClassFlow และ CareConnect
- `team.html` - หน้ารวมสมาชิก ตำแหน่ง และลิงก์ไปยัง Portfolio ของแต่ละคน
- `contact.html` - หน้าช่องทางติดต่อ แผนที่ และแบบฟอร์มตัวอย่าง
- `css/style.css` - รูปแบบ Responsive, Animation และ Visual effects ส่วนกลาง
- `js/script.js` - เมนูมือถือ, Reveal animation, Project card interaction และระบบภาษา TH/EN/ZH

## ความสามารถหลัก

- Responsive layout สำหรับ Desktop, Tablet และ Mobile
- รองรับภาษาไทย อังกฤษ และจีน
- Navigation เชื่อมต่อหน้า Home, ผลงาน, ทีม และ Contact
- Project case studies อธิบายโจทย์ โซลูชัน และผลลัพธ์
- Portfolio รายบุคคลเปิดผ่านลิงก์ออนไลน์จากหน้า Team
- รองรับผู้ใช้ที่ตั้งค่า `prefers-reduced-motion`

## วิธีเปิดในเครื่อง

เปิด `index.html` โดยตรง หรือรัน Static server จากโฟลเดอร์โปรเจกต์:

```bash
python3 -m http.server 8000
```

จากนั้นเปิด `http://localhost:8000`

## แนวทางการทำงานร่วมกัน

สมาชิกแต่ละคนพัฒนางานบน Branch ของตนเอง แล้วส่ง Pull Request เข้า `main`:

```bash
git switch main
git pull origin main
git switch -c <branch-name>

# หลังแก้ไขและทดสอบเรียบร้อย
git add <files>
git commit -m "Describe the change"
git push -u origin <branch-name>
```

Portfolio สามารถแยกเป็นโฟลเดอร์ภายในโปรเจกต์หรือเผยแพร่เป็นเว็บไซต์ภายนอกได้ แต่ต้องเชื่อมจาก `team.html` และเปิดใช้งานได้จริง

## การเผยแพร่

โปรเจกต์เป็น Static website และสามารถเผยแพร่ด้วย GitHub Pages โดยเลือก Deploy from a branch แล้วใช้ branch `main` กับโฟลเดอร์ `/ (root)`

## หมายเหตุ

- ผลงาน บริษัท และข้อมูลการติดต่อบางส่วนเป็นกรณีศึกษาจำลองเพื่อการศึกษา
- แบบฟอร์ม Contact ยังไม่เชื่อมต่อระบบส่งอีเมลจริง
- โปรเจกต์ไม่ใช้ Database หรือ Application server
