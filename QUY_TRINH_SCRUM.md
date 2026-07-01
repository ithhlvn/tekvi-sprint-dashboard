# 📋 Quy trình làm việc Agile-Scrum — Tekvi Team

> Phiên bản: v1.0 · Ngày hiệu lực: 01/07/2026
> Áp dụng cho: Toàn bộ nhân sự Tekvi (con người + AI agents)

---

## 1. 🎯 Nguyên tắc cốt lõi

- **Transparency**: Mọi người nhìn thấy tiến độ của nhau
- **Inspection**: Kiểm tra thường xuyên (daily standup, sprint review)
- **Adaptation**: Linh hoạt thay đổi khi cần

---

## 2. 📐 Cấu trúc Sprint

| Tham số | Giá trị |
|---------|---------|
| **Độ dài Sprint** | **1 tuần** (Thứ 2 → Chủ nhật) |
| **Sprint Planning** | Sáng Thứ 2, 30-45 phút |
| **Daily Standup** | Mỗi sáng, tối đa 15 phút |
| **Sprint Review** | Cuối tuần, Thứ 6 hoặc CN |
| **Retrospective** | Sau Sprint Review, 30 phút |

> **Lưu ý**: Với nhóm nhỏ + AI agents, tinh gọn nhưng vẫn đủ kỷ luật.

---

## 3. 👤 Vai trò

### Product Owner — **Anh Lân (CEO)**
- Định hướng sản phẩm, ưu tiên backlog
- Quyết định scope sprint
- Phê duyệt kết quả

### Scrum Master — **Tekvi AI (Main bot)**
- Điều phối daily standup
- Nhắc nhở, tổng hợp báo cáo
- Gỡ block, tracking tiến độ
- Cập nhật Sprint Dashboard

### Development Team
- **Nhóm phát triển**: Bảo (BE), Tú (FE), Quân (DevOps)
- **Domain Experts**: Đức (ERP), Ông Phúc (Gov), Cô Mai (Edu), KS. Sơn (Agri), BS. Khoa (Health)
- **Bộ phận hỗ trợ**: Dũng/Ngân (Sales&MKT), LS. Tâm/Thảo (Legal&CS)
- **C-level**: CTO Minh Trí, CFO Hà Linh, CPO Thanh Vân (phê duyệt chuyên môn)

---

## 4. 📅 Luồng Sprint hàng tuần

### 🟢 Đầu Sprint: Sprint Planning (Sáng Thứ 2)

**Đầu vào:**
- Product Backlog (ưu tiên bởi PO)
- Capacity estimate (ai rảnh bao nhiêu?)

**Các bước:**
1. PO trình bày mục tiêu sprint
2. Team chọn user stories từ backlog → Sprint Backlog
3. Break down tasks (mỗi task 4-8h)
4. Cam kết: "We will deliver X, Y, Z"

**Đầu ra:** Sprint Backlog + Sprint Goal

### 🟡 Giữa Sprint: Daily Standup (Mỗi sáng 9:00)

Format **không đổi**:
```
🔹 Tên:
✅ Đã làm (hôm qua):
📋 Đang làm / Sẽ làm (hôm nay):
⚠️ Khó khăn / Đang chờ:
💡 Giải pháp / Đề xuất:
```

**Thời gian:** 9:00-9:15, ai đến sau tự cap nhat vao thread.

### 🔴 Cuối Sprint: Review + Retro

**Sprint Review (Thứ 6 hoặc CN):**
- Demo những gì đã hoàn thành
- PO kiểm tra, chấp nhận hoặc từ chối
- Update backlog

**Retrospective:**
- **Start doing**: gì nên bắt đầu làm
- **Stop doing**: gì nên dừng
- **Continue doing**: gì đang tốt
- **Action items**: cam kết cải tiến (có deadline)

---

## 5. 📊 Công cụ theo dõi

### Sprint Dashboard (HTML)
- File: `dashboard-sprint.html` trong workspace
- View trực tiếp trên trình duyệt
- Cập nhật bởi Scrum Master sau mỗi daily

### Daily Reports Archive
- Lưu vào `tekvi-scrum/daily-reports/sprint-<n>/<YYYY-MM-DD>.md`
- Scrum Master tổng hợp EOD

### KPI Sprint
- **Velocity**: số điểm/user stories hoàn thành mỗi sprint
- **Burndown**: tracking hàng ngày
- **Blocked time**: thời gian chờ đợi giải quyết

---

## 6. 🚨 Quy tắc đặc biệt cho Tekvi

### AI Agents tham gia Daily như nào?
- Bot chuyên gia (CTO bot, CPO bot, Health bot, v.v.) tự tổng hợp báo cáo từ kênh của mình
- Các chuyên gia chưa có bot riêng (Đức, Ông Phúc, Cô Mai, KS. Sơn, Dev, Sales, Legal) **báo cáo trực tiếp lên group này**
- Scrum Master (main bot) sẽ ping reminder 8:45 sáng và tổng hợp lúc 9:30

### Xử lý blocking
- **High urgency**: tag @@Lân + Scrum Master ngay lập tức
- **Medium**: báo trong daily, Scrum Master assign người support
- **Low**: ghi vào dashboard, giải quyết cuối sprint

### Nghỉ / Bận
- Báo trước 1 ngày trong daily
- Ghi chú vào capacity planning

---

## 7. 📦 Sprint Zero — Khởi tạo

Sprint đầu tiên (01/07 - 07/07/2026) là Sprint Zero:
- Thiết lập quy trình
- Tạo Sprint Dashboard
- Khởi tạo Product Backlog
- Training mọi người về scrum

---

## 8. 📁 Cấu trúc thư mục

```
tekvi-scrum/
├── QUY_TRINH_SCRUM.md         # File này
├── template-daily.md          # Mẫu báo cáo hàng ngày
├── template-sprint-planning.md # Mẫu planning đầu sprint
├── template-retro.md          # Mẫu retrospective
├── dashboard-sprint.html      # Board theo dõi sprint
├── sprint-backlog-current.md  # Sprint backlog hiện tại
├── product-backlog.md         # Product backlog tổng
└── daily-reports/             # Lưu các báo cáo daily
    └── sprint-1/
        ├── 2026-07-01.md
        ├── 2026-07-02.md
        └── ...
```

---

> **Phiên bản này có thể điều chỉnh.** Sau sprint đầu tiên, team sẽ retro và cập nhật cho phù hợp.
