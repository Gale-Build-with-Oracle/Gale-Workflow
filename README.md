# Gale Workflow — คู่มือภาษาไทยฉบับสมบูรณ์

หนังสือเทคนิคภาษาไทยที่อธิบายระบบ **Oracle 3 ชั้นแบบ ephemeral** สำหรับวางระบบให้คนกับ AI coding agent หลายตัวทำงานร่วมกันได้จริง — ลึกกว่า oracle101 ครอบคลุมตั้งแต่หลักการ การติดตั้ง ไปจนถึงการ orchestrate, การ deploy และการ troubleshoot.

🌐 **เผยแพร่ที่:** <https://oracle102.vercel.app>
📦 **Framework ที่ใช้คู่กัน:** [Gale-Framework](https://github.com/Gale-Build-with-Oracle/Gale-Framework)

> oracle101 = เล่มเก่า (แนะนำ Oracle เบื้องต้น) · **oracle102 = เล่มนี้** (Gale Workflow ฉบับเต็ม)

## โครงสร้าง

```
website/
├── index.html          # หน้าแรก + สารบัญ
├── ch00.html–ch15.html # 16 บท แบ่งเป็น 4 ภาค
├── css/style.css       # design system (IBM Plex Sans Thai + indigo)
└── vercel.json         # config สำหรับ deploy บน Vercel
```

## สารบัญ (16 บท, 4 ภาค)

| ภาค | บท |
|---|---|
| **Foundation** | `ch00` บทนำ · `ch01` 5 Principles + Rule 6 · `ch02` สถาปัตยกรรม 3 ชั้น · `ch03` ψ Vault |
| **Installation & Runtime** | `ch04` ติดตั้งจาก 0 · `ch05` Oracle Brain · `ch06` Skills System · `ch07` maw-js Commands |
| **Orchestration** | `ch08` Delegation Tiers · `ch09` SOLO vs TEAM · `ch10` SOPs & Merge Gate · `ch11` CMMI & Docs |
| **Cross-Language & Production** | `ch12` Cross-Language · `ch13` Hooks เจาะลึก · `ch14` Fleet & Multi-Oracle · `ch15` Troubleshooting |

## รูปแบบ

Pure static HTML + CSS + [Mermaid.js](https://mermaid.js.org/) (โหลดผ่าน CDN) — ไม่มี build step. เปิดอ่าน local ได้ทันที:

```bash
cd website
python3 -m http.server 8000   # เปิด http://localhost:8000
```

## Deploy

Deploy เป็น static site บน Vercel (root directory = `website/`). `vercel.json` ตั้ง `public: true` และ alias `oracle102.vercel.app`.

---

หนังสือเล่มนี้เป็นเนื้อหาสาธารณะ (ไม่มีข้อมูลส่วนตัวหรือ credential ใด ๆ) — ตัวอย่างทั้งหมดใช้ชื่อ generic เช่น `my-oracle`, `dev-worker`, `YourProject`.
