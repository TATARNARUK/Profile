# 🚀 Backend Development Learning Journey

ยินดีต้อนรับสู่ Repository สำหรับบันทึกการเรียนรู้และโปรเจกต์ในรายวิชา Backend Development ครับ!

## 👨‍💻 About Me (เกี่ยวกับฉัน)
- **ชื่อ:** [ใส่ชื่อ-นามสกุลของคุณ] (Developer No. 673190105)
- **สถานศึกษา:** วิทยาลัยพณิชยการบางนา (Bangna Commercial College)
- **สาขาวิชา:** เทคโนโลยีสารสนเทศ (Information Technology)
- **จุดประสงค์:** เพื่อศึกษาและพัฒนาทักษะในรายวิชา Backend Development มุ่งเน้นการสร้าง API การจัดการฐานข้อมูล และระบบหลังบ้าน เพื่อนำไปต่อยอดในการพัฒนา Full-Stack Web Application และระบบจัดการต่างๆ ในอนาคต

---

## 📚 รายวิชา Backend Development

เนื้อหาใน Repository นี้จะประกอบไปด้วยการศึกษาและทดลองเขียนโค้ดในหัวข้อต่างๆ ดังนี้:

### 1. Fundamental of Node.js (พื้นฐาน Node.js)
- การทำงานของ V8 Engine และ Event Loop
- การจัดการ Module พื้นฐาน (CommonJS vs ES Modules)
- File System (fs) และ การจัดการ Path

### 2. Building RESTful APIs (การสร้าง API)
- การใช้งาน Express.js Framework
- การจัดการ Routing (GET, POST, PUT, DELETE)
- การสร้างและใช้งาน Middleware สำหรับจัดการ Request/Response

### 3. Database Integration (การเชื่อมต่อฐานข้อมูล)
- การออกแบบโครงสร้างฐานข้อมูล (Relational Database)
- การเชื่อมต่อและจัดการข้อมูลด้วย PostgreSQL / MySQL

---

## 💻 ตัวอย่างการเขียน Code ด้วย Node.js (Express.js)

นี่คือตัวอย่างพื้นฐานของการสร้าง Web Server และ API ง่ายๆ เพื่อส่งข้อมูล "Hello, IT Bangna!" กลับไปให้ผู้ใช้งาน

**ไฟล์: `server.js`**
```javascript
// อิมพอร์ตโมดูล express
const express = require('express');
const app = express();
const port = 3000;

// Middleware สำหรับแปลงข้อมูลให้อยู่ในรูปแบบ JSON
app.use(express.json());

// สร้าง Route พื้นฐาน (GET Request)
app.get('/', (req, res) => {
    res.json({ 
        message: 'Hello, IT Bangna!',
        developer_id: '673190105',
        status: 'Backend Server is running...'
    });
});

// กำหนดให้ Server รันบน Port ที่กำหนด
app.listen(port, () => {
    console.log(`🚀 Server เปิดทำงานแล้วที่ http://localhost:${port}`);
});