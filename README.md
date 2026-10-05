# KinetiQ — Dashboard Brief Canvas, KPI Table & Wireframe
กลุ่มอุตสาหกรรมเครื่องจักรและระบบอัตโนมัติ
**Use case ที่เลือก:** มอนิเตอร์การเชื่อมต่อและประสิทธิภาพเครื่องจักรแบบเรียลไทม์ สำหรับผู้จัดการฝ่ายผลิตที่ดูแลเครื่องจักรหลายยี่ห้อ

## โครงสร้าง repository

```
kinetiq-bi/
├── README.md
├── data/
│   ├── machine_status_snapshot.csv   ← สถานะเครื่องจักร 36 เครื่อง 3 ไซต์ (วันนี้)
│   └── kpi_daily_trend.csv           ← แนวโน้ม KPI ย้อนหลัง 14 วัน
├── dashboard/
│   └── index.html                    ← Brief Canvas + KPI Table + Wireframe + Chart rationale + Filter/Alert (ไฟล์เดียว เปิดในเบราว์เซอร์ได้ทันที)
└── docs/
    ├── group_members.md
    └── kpi_definition_table.csv
```

## เนื้อหาตาม Deliverable ของแบบฝึกหัด
ไฟล์ `dashboard/index.html` รวมทุกส่วนไว้ในหน้าเดียว :

1. **Brief Canvas** — User / Decision / Metric / Grain / Dimension / Action ตาม use case ของ KinetiQ
2. **KPI Definition Table** — นิยาม สูตร grain เป้าหมาย และเจ้าของ KPI ทั้ง 5 ตัว (มีไฟล์ CSV คู่กันที่ `docs/kpi_definition_table.csv`)
3. **Dashboard Wireframe (1 หน้า)** — mock แดชบอร์ดจริงพร้อม KPI card, กราฟแนวโน้ม, status grid, bar chart เปรียบเทียบ
4. **เหตุผลการเลือก Chart** — ตารางจับคู่ metric กับประเภท chart และเหตุผล
5. **Filter และ Alert** — รายการ filter 6 ตัว และ alert 4 ระดับความสำคัญ

## ข้อมูลที่ใช้ (/data)
ข้อมูลทั้งหมดเป็น ข้อมูลจำลอง (synthetic) สร้างให้สอดคล้องกับลักษณะปัญหาจริงที่ระบุใน Business Model Canvas ของทีม (เครื่องจักรหลายยี่ห้อ ปัญหาข้อมูลไซโล) — หากนำไปใช้งานจริงควรเชื่อมต่อกับข้อมูล sensor จริงผ่าน KinetiQ API

| ไฟล์ | เนื้อหา | Grain |
|---|---|---|
| `machine_status_snapshot.csv` | สถานะ, connectivity, latency, OEE, downtime, error ของเครื่องจักร 36 เครื่อง ใน 3 ไซต์ 7 สายการผลิต | รายเครื่อง ณ วันปัจจุบัน |
| `kpi_daily_trend.csv` | ค่าเฉลี่ย KPI รายวัน ย้อนหลัง 14 วัน พร้อมเหตุการณ์ incident จำลองวันที่ 1–2 ต.ค. | รายวัน |

## กลุ่ม
ดู `docs/group_members.md`


