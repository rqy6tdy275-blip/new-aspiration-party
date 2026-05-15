# 🌻 พรรคความหวังใหม่ | New Aspiration Party

> ระบบ Full Stack สำหรับพรรคการเมืองสมัยใหม่ — เว็บไซต์ + Admin Dashboard + Mobile PWA

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen)](https://github.com)

---

## 🗂️ โครงสร้างโปรเจกต์

```
new-aspiration-party/
├── index.html          # 🌐 เว็บไซต์หลัก (Public Website)
├── admin.html          # 🛠️ Admin Dashboard (หลังบ้าน)
├── app.html            # 📱 Mobile PWA App
├── entities/           # 🗄️ Database Entity Schemas (JSON)
│   ├── Banner.json
│   ├── ContactMessage.json
│   ├── Donation.json
│   ├── Event.json
│   ├── EventRegistration.json
│   ├── MediaFile.json
│   ├── Member.json
│   ├── MembershipPlan.json
│   ├── News.json
│   ├── PartySettings.json
│   ├── Policy.json
│   └── Volunteer.json
└── README.md
```

---

## 🎨 Design System

| Token | Value |
|-------|-------|
| Primary Color | `#0B7A33` |
| Secondary Color | `#FFF04F` |
| Accent Color | `#F5C400` |
| Dark Color | `#1A1A1A` |
| Background | `#F8FAF7` |
| Font (TH) | Kanit / Sarabun |
| Font (EN) | Poppins |

---

## 📄 หน้าเว็บไซต์

### 🌐 `index.html` — Public Website
- **Hero Section** — สโลแกนพรรค + ปุ่ม CTA + รูปดอกทานตะวัน AI
- **Features Strip** — นโยบายหลัก 6 ด้าน
- **นโยบาย** — 4 นโยบายหลักพร้อม card
- **สถิติสมาชิก** — แสดงตัวเลขสำคัญ
- **ข่าวสาร** — ข่าวล่าสุด 3 ข่าว
- **กิจกรรม** — กิจกรรมที่กำลังจะมา
- **ระบบสมาชิก** — รายปี / ตลอดชีพ
- **บริจาค** — PromptPay + โอนธนาคาร
- **อาสาสมัคร** — ลงทะเบียน form
- **ติดต่อ** — ฟอร์มติดต่อ + Social Links
- **Footer** — ลิงก์ครบ + Social icons

**Mobile Features:**
- Hamburger Menu พร้อม Drawer animation
- Bottom Navigation 5 ปุ่ม (active state ตาม scroll)
- Responsive ทุก breakpoint (375px / 768px / 1024px)

---

### 🛠️ `admin.html` — Admin Dashboard

**Login Demo:**
```
Email:    admin@newaspirationparty.or.th
Password: Admin@2026
```

**ฟีเจอร์:**
- **Dashboard** — Stats cards, Bar chart, Donut chart, Quick actions
- **สมาชิก** — ตาราง, อนุมัติ/ปฏิเสธ, Export
- **บริจาค** — ตรวจสอบสลิป, อนุมัติ, ออกใบเสร็จ
- **ข่าวสาร** — CRUD + เผยแพร่/แบบร่าง
- **ตั้งค่าพรรค** — แก้ไขข้อมูลพรรค, Social, ธนาคาร
- **Media Manager** — จัดการไฟล์
- **Activity Log** — ประวัติการทำงาน
- **ข้อความติดต่อ** — ตอบกลับ inbox

**Sidebar navigation** responsive — collapse เป็น overlay บน mobile

---

### 📱 `app.html` — Mobile PWA App

**Features:**
- Splash Screen + Loading animation
- Bottom Navigation 5 ปุ่ม (Home / ข่าว / บริจาค / กิจกรรม / โปรไฟล์)
- **หน้าแรก** — Hero card, Stats strip, Quick actions 8 ปุ่ม, ข่าว, นโยบาย, กิจกรรม
- **ข่าวสาร** — Filter tabs, List view พร้อม thumbnail
- **กิจกรรม** — Event cards พร้อมลงทะเบียน
- **บริจาค** — เลือกจำนวน, PromptPay QR, โอนธนาคาร
- **โปรไฟล์** — Digital Member Card + QR Code, Dark Mode toggle

---

## 🗄️ Database Entities (ตาราง)

| Entity | คำอธิบาย |
|--------|---------|
| `PartySettings` | ข้อมูลพรรค, สี, Social, ธนาคาร |
| `Member` | ข้อมูลสมาชิก, สถานะ, ประเภท |
| `MembershipPlan` | แผนสมาชิก รายปี/ตลอดชีพ |
| `Donation` | การบริจาค, สลิป, สถานะ |
| `News` | ข่าวสาร, บทความ, SEO |
| `Policy` | นโยบายพรรค 10 หมวด |
| `Event` | กิจกรรม, ลงทะเบียน, QR |
| `EventRegistration` | การลงทะเบียนกิจกรรม, Check-in |
| `Volunteer` | อาสาสมัคร, ทักษะ, พื้นที่ |
| `Banner` | แบนเนอร์, Hero, Popup |
| `ContactMessage` | ข้อความติดต่อ, inbox |
| `MediaFile` | ไฟล์รูป, วิดีโอ, PDF |

---

## ⚙️ Tech Stack

### Frontend
- **HTML5 + CSS3 + Vanilla JS** (Zero dependencies)
- **Google Fonts** — Kanit, Sarabun, Poppins
- **CSS Variables** — Design System
- **CSS Grid + Flexbox** — Responsive layout
- **Intersection Observer API** — Fade-up animations

### Backend / Platform
- **Base44** — Backend as a Service
- **PostgreSQL** — Database (via Base44 Entities)
- **Base44 Storage** — File/Image hosting
- **Base44 Automations** — CRON + Entity triggers

### Design Pattern
- Mobile-first responsive
- Political Modern Campaign aesthetic
- Glassmorphism hero sections
- Smooth animations + micro-interactions

---

## 🚀 การ Deploy

### ใช้งานผ่าน Base44 (แนะนำ)
ระบบ deploy บน Base44 Platform พร้อมใช้งานทันที

### Deploy บน VPS/Static Hosting
```bash
# Clone โปรเจกต์
git clone https://github.com/rqy6tdy275-blip/new-aspiration-party.git

# เปิดด้วย live server หรือ static file server
npx serve .

# หรือใช้ nginx
# copy ไฟล์ไปยัง /var/www/html/
```

---

## 🔐 Admin Credentials (Demo)

```
URL:      /admin.html
Email:    admin@newaspirationparty.or.th
Password: Admin@2026
Role:     Super Admin
```

---

## 📱 Screenshots

| หน้า | คำอธิบาย |
|------|---------|
| 🌐 Website | เว็บไซต์หลัก responsive ทุกขนาด |
| 🛠️ Admin | Dashboard + จัดการสมาชิก + บริจาค |
| 📱 Mobile | PWA App พร้อม Digital Member Card |

---

## 📄 License

MIT License — สามารถนำไปใช้และปรับแต่งได้อย่างอิสระ

---

<div align="center">

🌻 **พรรคความหวังใหม่ | New Aspiration Party** 🌻

*ร่วมสร้างความหวังใหม่ เพื่ออนาคตที่ดีกว่า*

Built with ❤️ on [Base44](https://base44.com)

</div>
