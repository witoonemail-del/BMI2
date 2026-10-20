# BMI Pro - Android Project

## วิธี Build เป็น APK จริง

### วิธีที่ 1: Android Studio (แนะนำ - ง่ายสุด)
1. เปิด Android Studio
2. File > Open > เลือกโฟลเดอร์ BMIPro-Android-Project นี้
3. รอให้ Gradle Sync เสร็จ
4. ไปที่เมนู Build > Build APK(s) หรือ Build > Generate Signed Bundle / APK
5. APK จะอยู่ที่ app/build/outputs/apk/debug/app-debug.apk
6. ส่งไฟล์นี้เข้าโทรศัพท์แล้วกดติดตั้งได้เลย

### วิธีที่ 2: PWABuilder (เร็วสุด 1 นาที ไม่ต้องติดตั้งอะไร)
1. อัปโหลดไฟล์แอป PWA ที่ได้ไปโฮสต์ (หรือใช้ลิงก์ Preview)
2. ไปที่ https://www.pwabuilder.com
3. ใส่ URL ของแอป > Package > Android > Download APK

### วิธีที่ 3: Bubblewrap (CLI)
npx @bubblewrap/cli init --manifest https://your-host/manifest.json
npx @bubblewrap/cli build

## โครงสร้าง
- MainActivity.kt = WebView โหลดไฟล์ assets/index.html
- assets/index.html = แอป BMI ทั้งหมด ทำงานออฟไลน์

แอปนี้ไม่ต้องขอ Internet ก็ทำงานได้ เพราะใช้ไฟล์ local ทั้งหมด
