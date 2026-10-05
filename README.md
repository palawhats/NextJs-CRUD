Markdown


# Student Management System (Next.js CRUD)

ระบบจัดการข้อมูลนักเรียน (CRUD - Create, Read, Update, Delete) พัฒนาด้วย Next.js (App Router), Prisma ORM และ Tailwind CSS

---

## 🛠️ Tech Stack

* **Framework:** [Next.js](https://nextjs.org/) (App Router)
* **Language:** TypeScript[cite: 1]
* **Database ORM:** [Prisma](https://www.prisma.io/)[cite: 1]
* **Database:** SQLite[cite: 1]
* **Styling:** Tailwind CSS[cite: 1]

---

## ✨ Features

* 📜 **Read:** แสดงรายการนักเรียนทั้งหมด[cite: 1]
* ➕ **Create:** เพิ่มข้อมูลนักเรียนใหม่ พร้อมระบบ Validation[cite: 1]
* ✏️ **Update:** แก้ไขข้อมูลนักเรียนที่มีอยู่[cite: 1]
* 🗑️ **Delete:** ลบข้อมูลนักเรียน[cite: 1]

---

## 📋 Prerequisites

* **Node.js** (เวอร์ชัน 18.0.0 หรือใหม่กว่า)
* **npm** / **pnpm** / **yarn**

---

## 🚀 Getting Started (ขั้นตอนการติดตั้ง)

### 1. Clone Repository

```bash
git clone [https://github.com/](https://github.com/)<YOUR-USERNAME>/<YOUR-REPOSITORY-NAME>.git
cd NextJs-CRUD-main
2. Install Dependencies
ติดตั้งแพ็กเกจที่จำเป็นสำหรับโปรเจกต์:

Bash


npm install
3. Environment Variables Setup
สร้างไฟล์ .env ที่ root folder ของโปรเจกต์ แล้วกำหนดค่า DATABASE_URL[cite: 1]:

Code snippet


DATABASE_URL="file:./dev.db"
4. Database Setup (Prisma)
รันคำสั่งเพื่อ Migrate ฐานข้อมูล SQLite และ Generate Prisma Client[cite: 1]:

Bash


npx prisma migrate dev
(ตัวเลือกเสริม) เปิดดูและจัดการข้อมูลผ่าน Prisma Studio:

Bash


npx prisma studio
5. Run Development Server
Bash


npm run dev
เปิดเบราว์เซอร์แล้วเข้าไปที่ http://localhost:3000

📁 Project Structure
Plaintext


NextJs-CRUD-main/
├── app/
│   ├── lib/
│   │   └── prisma.ts       # Prisma Client instance[cite: 1]
│   ├── students/
│   │   ├── create/         # ฟอร์มเพิ่มข้อมูลนักเรียน[cite: 1]
│   │   ├── edit/[id]/      # ฟอร์มแก้ไขข้อมูลนักเรียน[cite: 1]
│   │   ├── actions.ts      # Server Actions จัดการข้อมูล[cite: 1]
│   │   ├── delete-button.tsx[cite: 1]
│   │   ├── page.tsx        # หน้าแสดงรายการนักเรียน[cite: 1]
│   │   └── validation.ts   # ตรวจสอบความถูกต้องของข้อมูล[cite: 1]
│   ├── globals.css         # Tailwind CSS styling[cite: 1]
│   ├── layout.tsx          # Root Layout[cite: 1]
│   └── page.tsx            # Home Page[cite: 1]
├── prisma/
│   ├── migrations/         # Database Migration History[cite: 1]
│   └── schema.prisma       # Prisma Schema Model[cite: 1]
├── .env                    # Environment variables[cite: 1]
├── next.config.ts          # Next.js configuration[cite: 1]
├── package.json[cite: 1]
└── README.md