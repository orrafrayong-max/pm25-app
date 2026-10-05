# PM2.5 app (อ่านอย่างเดียว)

## นำขึ้น GitHub Pages (PowerShell)

1. สร้าง repository ว่างบน github.com (เช่นชื่อ `pm25-app`) โดยไม่ต้องติ๊กเพิ่ม README
2. เปิด PowerShell ในโฟลเดอร์นี้ แล้วรัน (แก้ `USERNAME` และชื่อ repo):

```powershell
git init -b main
git add .
git commit -m "PM2.5 app"
git remote add origin https://github.com/USERNAME/pm25-app.git
git push -u origin main
```

3. บน GitHub: Settings > Pages > Source: "Deploy from a branch" > Branch: `main` / `(root)` > Save
4. รอสักครู่ แล้วเปิด `https://USERNAME.github.io/pm25-app/` บนมือถือ

## ติดตั้งบนมือถือ
- Android (Chrome): กดปุ่ม "ติดตั้ง" ในหน้าแอป หรือเมนู > ติดตั้งแอป
- iPhone (Safari เท่านั้น): แชร์ > เพิ่มลงหน้าจอโฮม

## ปรับค่าในไฟล์ index.html
- `STALE_H` = จำนวนชั่วโมงที่ถือว่าข้อมูลเก่า (ตอนนี้ 3)
- `BANDS` = ช่วง AQI และสี (ช่วงสูงกว่า 100 ยังไม่ได้ยืนยันกับแหล่งทางการ)
- คีย์ใน `KEY` เป็นคีย์สาธารณะแบบอ่านอย่างเดียว ไม่ใช่ความลับ
