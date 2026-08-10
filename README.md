# TurnBro Software

เว็บไซต์บริษัทพัฒนาซอฟต์แวร์จำลองสำหรับงานกลุ่มรายวิชา **960241** นำเสนอภาพรวมบริษัท บริการ กรณีศึกษา และสมาชิกทีมผ่านเว็บไซต์แบบ Static ที่รองรับภาษาไทย อังกฤษ และจีน

> โปรเจกต์นี้จัดทำเพื่อการศึกษา ชื่อบริษัท ข้อมูลติดต่อ ลูกค้า และผลลัพธ์ของกรณีศึกษาบางส่วนเป็นข้อมูลจำลอง

## จุดเด่น

- Responsive design รองรับ Desktop, Tablet และ Mobile
- สลับภาษาไทย อังกฤษ และจีน พร้อมจดจำภาษาที่เลือกในเบราว์เซอร์
- หน้าแนะนำบริการ Web Application, Business System และ UX/UI Design
- กรณีศึกษาจำลอง SmartPOS, ClassFlow และ CareConnect
- หน้าแนะนำสมาชิกทีมพร้อมลิงก์ Portfolio รายบุคคล
- Mobile navigation, scroll reveal และ interactive project cards
- กล่องยืนยันก่อนเปิดลิงก์ภายนอก
- รองรับ `prefers-reduced-motion` เพื่อช่วยลด Animation ตามการตั้งค่าของผู้ใช้

## เทคโนโลยี

- HTML5
- CSS3
- Vanilla JavaScript
- Google Fonts: Manrope และ Noto Sans Thai
- Google Maps Embed สำหรับแผนที่ในหน้าติดต่อ
- FormSubmit สำหรับส่งข้อความจากแบบฟอร์มไปยังอีเมลของทีม

โปรเจกต์นี้ไม่มี Build step, Package manager, Framework, Database หรือ Application server

## เริ่มต้นใช้งาน

สิ่งที่ต้องมี: เว็บเบราว์เซอร์สมัยใหม่ และ Python 3 หากต้องการรันผ่าน Local server

1. Clone Repository และเข้าไปยังโฟลเดอร์โปรเจกต์

   ```bash
   git clone https://github.com/thekorachan/960241-group-project.git
   cd 960241-group-project
   ```

2. เปิด `index.html` โดยตรง หรือรัน Local server (แนะนำ)

   ```bash
   python3 -m http.server 8000
   ```

3. เปิด [http://localhost:8000](http://localhost:8000) ในเบราว์เซอร์

> การเชื่อมต่ออินเทอร์เน็ตจำเป็นสำหรับการโหลด Google Fonts, แผนที่, Portfolio ภายนอก และการส่งแบบฟอร์ม ส่วนเนื้อหาหลักของเว็บไซต์ยังเปิดจากไฟล์ในเครื่องได้

## โครงสร้างโปรเจกต์

```text
.
├── index.html                 # หน้าแรก บริการ และกรณีศึกษา
├── team.html                  # สมาชิกทีมและ Portfolio
├── contact.html               # ข้อมูลติดต่อ แผนที่ และแบบฟอร์มตัวอย่าง
├── web-application.html       # รายละเอียดบริการ Web Application
├── business-system.html       # รายละเอียดบริการ Business System
├── ux-ui-design.html          # รายละเอียดบริการ UX/UI Design
├── css/
│   └── style.css              # Style, responsive layout และ animation
├── js/
│   └── script.js              # Navigation, i18n และ interaction
└── asset/
    └── image/                 # Logo, รูปสมาชิก และภาพกรณีศึกษา
```

## การแก้ไขเนื้อหา

- แก้โครงสร้างและข้อความเริ่มต้นในไฟล์ `.html` ที่เกี่ยวข้อง
- แก้คำแปลทั้งสามภาษาใน Object `translations` ภายใน `js/script.js`
- แก้รูปแบบ สี และ Responsive breakpoints ใน `css/style.css`
- เพิ่มหรือเปลี่ยนรูปภาพใน `asset/image/` แล้วอัปเดต Path ที่อ้างอิงใน HTML หรือ CSS

เมื่อเพิ่มข้อความที่ต้องแปล ให้กำหนด Translation key เดียวกันในภาษา `th`, `en` และ `zh` เพื่อไม่ให้เนื้อหาบางภาษาขาดหาย

## การเผยแพร่ด้วย GitHub Pages

1. Push โปรเจกต์ขึ้น GitHub
2. เปิด **Settings → Pages**
3. ในหัวข้อ **Build and deployment** เลือก **Deploy from a branch**
4. เลือก Branch `main` และโฟลเดอร์ `/ (root)` แล้วกด **Save**

เนื่องจากเว็บไซต์ใช้ Relative paths จึงไม่ต้องตั้งค่า Build เพิ่มเติมสำหรับ GitHub Pages

## ข้อจำกัด

- แบบฟอร์มใน `contact.html` ส่งข้อมูลผ่านบริการ FormSubmit ภายนอกไปยัง `kora@thekorachan.com` และต้องยืนยันอีเมลเปิดใช้งานครั้งแรกก่อนรับข้อความ
- อีเมล หมายเลขโทรศัพท์ และข้อมูลบริษัทบางส่วนเป็น Placeholder
- ผลงานและตัวเลขผลลัพธ์ในกรณีศึกษาเป็นข้อมูลจำลองเพื่อการศึกษา
- ไม่มี Automated test suite; ควรตรวจสอบทุกหน้า ทุกภาษา และหลายขนาดหน้าจอก่อนเผยแพร่

## ทีมผู้จัดทำ

- **Hydra07188** — Project Manager / Developer
- **thekorachan** — UX/UI Designer / Front-end Developer
- **Kitichet.me** — Full-stack Developer

ดู Portfolio ของสมาชิกแต่ละคนได้จากหน้า `team.html`

---

จัดทำเพื่อรายวิชา **960241 Group Project** · © 2026 TurnBro
