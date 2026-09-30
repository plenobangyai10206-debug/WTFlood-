# น้ำนนท์ Watch (ชื่อชั่วคราว)

เว็บติดตามสถานการณ์น้ำท่วมลุ่มน้ำเจ้าพระยา เน้นนนทบุรี — Next.js (App Router) + TypeScript + Tailwind

## รันในเครื่อง
```bash
npm install
npm run dev      # เปิด http://localhost:3000
npm run build    # ทดสอบ build ก่อน deploy
```

## แก้เนื้อหาโดยไม่ต้องแตะโค้ด (โฟลเดอร์ /data)
- `data/prepare.json`  เช็กลิสต์หน้า "เตรียมตัว" (ตรวจแล้วเปลี่ยน `reviewStatus` เป็น `"reviewed"`)
- `data/contacts.json` เบอร์โทร (เติมเบอร์ท้องถิ่นที่ `number: null` ทีละรายการ)
- `data/sources.json`  รายชื่อแหล่งข้อมูล (ตรวจลิงก์แล้วเปลี่ยน `verified` เป็น `true`)

## แก้สี/ฟอนต์/ระยะ
ไฟล์เดียว: `src/app/globals.css` (Design tokens)

## โครงสร้าง
- `src/app/*` หน้าเว็บ · `src/components/ui/*` คอมโพเนนต์กลาง · `src/lib/*` ฟังก์ชันและชนิดข้อมูล
- เฟสถัดไป: `src/lib/sources/*.ts` (adapter) และ `src/app/api/*` (Route Handler)
