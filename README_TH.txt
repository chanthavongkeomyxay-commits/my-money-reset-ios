# My Money Reset — Web App Package

แพ็กเกจนี้ดึงหน้าเว็บที่ฝังอยู่ใน `app-debug.apk` ออกมาเป็นเว็บแอป และเพิ่ม manifest สำหรับการติดตั้งลงหน้าจอโฮม

## วิธีทดลอง
1. แตกไฟล์ ZIP นี้
2. อัปโหลดไฟล์ทั้งหมดไปยังโฮสต์เว็บแบบ static ที่ให้ HTTPS (เช่น GitHub Pages หรือ Netlify) โดยคงไฟล์ไว้ในโฟลเดอร์เดียวกัน
3. เปิด URL ที่โฮสต์ได้จาก Safari บน iPhone
4. หากต้องการเพิ่มไอคอน: Safari > Share > Add to Home Screen

## ข้อจำกัดที่ต้องรู้
- เว็บแอปโหลด Tailwind CSS และ Firebase จาก CDN จึงต้องมีอินเทอร์เน็ต
- การเข้าสู่ระบบ Google ผ่าน Firebase อาจยังไม่ทำงานจนกว่าจะเพิ่มโดเมนที่โฮสต์ใน Firebase Authentication > Settings > Authorized domains และตรวจสอบผู้ให้บริการเข้าสู่ระบบ
- ต้องตรวจสอบ Firestore Security Rules ก่อนใช้กับข้อมูลการเงินจริง ห้ามเปิดสิทธิ์ฐานข้อมูลให้ทุกคนอ่าน/เขียน
- แพ็กเกจนี้สร้างจากหน้า HTML ที่พบใน APK เท่านั้น ไม่ใช่ Source Code ต้นฉบับทั้งหมด และยังไม่ได้ทดสอบกับ Firebase project จริงหรืออุปกรณ์ iPhone
- นี่คือเว็บแอปที่ติดตั้งจาก Safari ได้ ไม่ใช่ไฟล์ IPA และยังไม่ได้เผยแพร่ใน App Store
