# 960241 Group Project

เว็บไซต์บริษัทพัฒนาซอฟต์แวร์จำลองสำหรับงานกลุ่มรายวิชา 960241

## โครงสร้างโปรเจกต์

- `index.html` - หน้าแนะนำบริษัทและผลงาน
- `team.html` - หน้ารวมสมาชิกและตำแหน่ง
- `portfolio/<github-username>/` - Portfolio แยกของสมาชิกแต่ละคน
- `css/style.css` - สไตล์ส่วนกลางของเว็บไซต์
- `js/script.js` - JavaScript ส่วนกลาง

## วิธีเริ่มทำงาน

สมาชิกแต่ละคนควรสร้าง Branch และโฟลเดอร์ของตนเอง:

```bash
git switch main
git pull origin main
git switch -c portfolio-ชื่อของคุณ
mkdir -p portfolio/ชื่อของคุณ
```

หลังทำเสร็จให้ Commit, Push และเปิด Pull Request:

```bash
git add .
git commit -m "เพิ่ม portfolio ของชื่อคุณ"
git push -u origin portfolio-ชื่อของคุณ
```

## สิ่งที่ต้องแก้ก่อนส่ง

- เปลี่ยนชื่อบริษัทและเนื้อหาให้ตรงกับข้อตกลงของกลุ่ม
- เพิ่มรายชื่อ ตำแหน่ง และลิงก์ Portfolio ของสมาชิกทุกคนใน `team.html`
- ใส่ผลงานจำลองของบริษัทให้ครบ
- ทดสอบลิงก์และการแสดงผลบนโทรศัพท์

