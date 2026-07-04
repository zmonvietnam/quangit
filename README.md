<p align="center">
  <img src="./landingpage.png" alt="Z-MON Việt Nam — Nền tảng quản lý hiệu suất doanh nghiệp" width="100%" />
</p>

<h1 align="center">Z-MON Việt Nam</h1>
<p align="center">
  <strong>Nền tảng quản lý hiệu suất lực lượng lao động trên máy tính — dành cho doanh nghiệp hiện đại</strong>
</p>

<p align="center">
  <a href="https://zmon.vn">Website</a> ·
  <a href="https://my.zmon.vn">Dashboard</a> ·
  <a href="https://docs.zmon.vn">Tài liệu</a> ·
  <a href="mailto:support@zmon.vn">Hỗ trợ</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/AI-Powered-009883?style=for-the-badge" alt="AI Powered" />
  <img src="https://img.shields.io/badge/Realtime-WebSocket-1570EF?style=for-the-badge" alt="Realtime" />
  <img src="https://img.shields.io/badge/Multi--tenant-SaaS-6941C6?style=for-the-badge" alt="Multi-tenant" />
  <img src="https://img.shields.io/badge/VI%20%7C%20EN-Bilingual-027A48?style=for-the-badge" alt="Bilingual" />
</p>

---

## Tầm nhìn

**Z-MON** là hệ sinh thái quản trị vận hành end-to-end: thu thập dữ liệu làm việc theo phút từ máy tính nhân viên, chuyển hóa thành KPI thời gian thực, phân tích thất thoát chi phí, kiểm soát gian lận, quản lý công việc và báo cáo tập trung — trên một nền tảng thống nhất.

Không chỉ là công cụ giám sát. Z-MON là **trung tâm điều hành** giúp lãnh đạo nhìn thấy năng suất thực tế, IT vận hành ổn định, HR đối soát chính xác và đội ngũ quản lý ra quyết định dựa trên dữ liệu — không phỏng đoán.

> *Triển khai gọn nhẹ · Vận hành ổn định · ROI có thể đo lường ngay từ những tuần đầu*

---

## Kiến trúc hệ thống

| Thành phần | Công nghệ | Vai trò |
|---|---|---|
| **Landing & Marketing** | React | Giới thiệu sản phẩm, đăng ký, chính sách pháp lý |
| **Dashboard Admin** | React 18 · Tailwind CSS | Trung tâm điều hành doanh nghiệp |
| **Backend API** | Rust · Actix-web 4 | Xử lý nghiệp vụ, bảo mật, realtime |
| **Cơ sở dữ liệu** | PostgreSQL 15 | Multi-tenant, audit, lưu trữ dài hạn |
| **ZMON Agent** | Go · Windows Service | Thu thập dữ liệu nền trên máy nhân viên |
| **Agent UI** | React · Tauri | Giao diện nhân viên: chat, task, hỗ trợ, thông báo |
| **Realtime** | WebSocket | Dashboard, máy trạm, nhắn tin, cảnh báo |
| **AI** | LLM Streaming | Trợ lý phân tích · AI Công việc |
| **Thông báo** | Web Push · Telegram · Desktop Notify | Cảnh báo đa kênh |

---

## Trải nghiệm sản phẩm

### Dashboard Tổng quan — Trung tâm điều hành

14+ KPI cards, biểu đồ xu hướng, trạng thái thiết bị và quick-access tới AI, Công việc, Máy trạm, Báo cáo. Dữ liệu làm mới theo chu kỳ, lọc theo ngày/tuần/tháng (múi giờ Việt Nam UTC+7).

<p align="center">
  <img src="./tong-quan.png" alt="Dashboard Tổng quan Z-MON" width="92%" />
</p>

**Năng lực chính:**
- Nhân viên đang làm (trong ca + có hoạt động máy)
- Máy có dữ liệu: làm việc / idle / không data
- Cảnh báo, license, tài khoản hệ thống
- KPI công việc: đang làm, quá hạn, dự án, năng suất, tích hợp
- Biểu đồ hoạt động theo giờ · Top máy theo hiệu suất
- Deep link tới module chi tiết khi phát hiện bất thường

---

### Module Công việc — Quản trị dự án & task doanh nghiệp

<p align="center">
  <img src="./tongquancongviec.png" alt="Tổng quan Công việc Z-MON" width="92%" />
</p>

| Tính năng | Mô tả |
|---|---|
| **Tổng quan công việc** | Health score, velocity, completion rate, AI tóm tắt tự động |
| **Danh sách công việc** | List · Kanban · Lịch · Timeline · Gantt |
| **Dự án công việc** | Quản lý dự án, milestone, tiến độ tổng thể |
| **AI Công việc** | Tạo task bằng ngôn ngữ tự nhiên, phân tích bottleneck, đề xuất ưu tiên |
| **Tiến độ** | Burndown, velocity chart, theo dõi deadline |
| **Kết nối nền tảng** | 149+ tích hợp: Jira, Slack, Google, GitHub, Trello… |
| **Nhật ký công việc** | Audit sync, automation log, lịch sử thay đổi |
| **Mẫu công việc** | Template onboarding, sprint, checklist tái sử dụng |
| **Nhân viên** | Hồ sơ HR, gán máy, ca làm việc, lương/giờ |
| **Kiến thức cho nhân viên** | Knowledge base nội bộ |
| **Lịch sử chấm công** | Đối soát ca làm, trạng thái attendance theo ngày |

---

### Máy trạm & Agent — Giám sát sâu từng thiết bị

<p align="center">
  <img src="./hieu-suat-tong-may.png" alt="Hiệu suất tổng máy Z-MON" width="92%" />
</p>

**ZMON Agent** chạy nền trên Windows, thu thập snapshot theo phút và đồng bộ realtime qua WebSocket.

#### Sơ đồ Agent
Trực quan hóa kết nối, trạng thái và luồng dữ liệu giữa Agent ↔ Cloud.

#### Máy quản lý — 13 tab forensic chi tiết

| Tab | Năng lực |
|---|---|
| **Tổng quan** | Snapshot realtime: CPU, RAM, disk, uptime, user |
| **Tiến trình** | Process tree, CPU/RAM từng app |
| **Mạng** | Kết nối, bandwidth, DNS |
| **Ảnh màn hình** | Screenshot theo lịch / theo sự kiện |
| **Nhật ký gõ phím** | Keylog theo app, cửa sổ, URL web |
| **Phím tắt** | Shortcut history theo ứng dụng |
| **Clipboard** | Sao chép/dán — audit nội dung |
| **Trình duyệt** | Lịch sử web, tab đang mở |
| **USB** | Thiết bị cắm/rút |
| **Tải xuống** | File download tracking |
| **Tệp tin** | Thay đổi file hệ thống |
| **Ứng dụng** | App usage, icon, thời gian focus |
| **Hiệu suất** | Productivity score, focus time, AFK |

**Điều khiển từ xa:** khóa màn hình · restart · shutdown · bật/tắt thu thập dữ liệu  
**Bảo mật dữ liệu:** OTP mở khóa xem forensic (30 phút/máy) · audit đầy đủ

#### Hiệu suất tổng máy
So sánh hôm nay vs hôm qua, tháng này vs tháng trước, tuần vs tuần trước — productivity, focus, WPM, app switching, activity density.

---

## AI — Trí tuệ nhân tạo tích hợp

### AI Trợ lý (toàn hệ thống)
- Chat streaming realtime, 30 phiên hội thoại
- Phân tích nhân viên, máy offline, cảnh báo khẩn, báo cáo hiệu suất
- Gợi ý câu hỏi thông minh · Hỗ trợ tiếng Việt & English
- Truy vấn dữ liệu doanh nghiệp A-Z qua ngôn ngữ tự nhiên

### AI Công việc (chuyên module Work)
- Tạo task từ mô tả tự nhiên · Preview trước khi lưu
- Báo cáo tiến độ, task quá hạn, đề xuất xử lý
- Phân tích workload, bottleneck, rủi ro deadline

---

## Phân tích & Báo cáo

### Hiệu suất
- Tab **Máy tính**: productivity theo nhân viên, máy, phòng ban
- Tab **Công việc**: task completion, velocity, overdue trend
- Lọc thời gian linh hoạt · So sánh kỳ

### Phân tích thất thoát
- Thất thoát **thời gian** và **chi phí lao động (VND)**
- Cấu hình lương/giờ theo nhân viên hoặc mặc định
- Chỉ tính phút trong ca làm việc đã cấu hình

### Kiểm soát gian lận
- Quét tự động nền khi Agent gửi dữ liệu
- Phát hiện autoclicker, macro, pattern bất thường
- Preset rule theo chính sách công ty · Evidence review

### Báo cáo
- 4 tab: Tổng quan · Máy tính · Công việc · Thất thoát
- Xuất **CSV / Excel 5 sheet**
- Lọc theo thời gian, phòng ban, nhân viên

---

## Cảnh báo & Thông báo

### Cảnh báo (Alerts)
- Ngưỡng CPU, RAM, disk, idle, hiệu suất thấp
- Cảnh báo gian lận, máy mất kết nối, license
- Phân loại: Critical · High · Medium · Low
- Workflow: mở → xử lý → resolved

### Thông báo đa kênh
- **Dashboard hub**: chuông + toast + desktop notification
- **Web Push**: nhận khi đóng tab (Service Worker)
- **Telegram Bot**: 30+ sự kiện cấu hình được
- **Agent EXE**: thông báo tin nhắn, hỗ trợ, công việc, hộp thư

---

## Giao tiếp & Hỗ trợ

| Kênh | Đối tượng | Mô tả |
|---|---|---|
| **Nhắn tin** | Admin ↔ Nhân viên | Chat realtime qua WebSocket, đính kèm file |
| **Yêu cầu hỗ trợ** | Nhân viên → Admin | Ticket từ Agent, trạng thái open/inprogress/resolved |
| **Hỗ trợ Z-MON online** | Khách hàng → Z-MON | Chat trực tiếp với đội ngũ Z-MON |
| **Thông báo hệ thống** | Platform → Tenant | Announcement, cập nhật, khuyến mãi |

---

## Quản trị & Bảo mật

### Phân quyền Operator
- Ma trận **Edit / View / Deny** theo từng menu feature
- Role template: Admin · Quản lý · Nhân viên IT · Giám sát
- Audit log mọi thao tác đăng nhập, cấu hình, CRUD

### Đa tenant SaaS
- Mỗi doanh nghiệp = 1 tenant độc lập
- Subscription: trial 7 ngày · gói theo license slot
- Gia hạn · thanh toán · hóa đơn · hợp đồng dịch vụ số

### Bảo mật phiên đăng nhập
- JWT access + refresh token · HttpOnly cookie
- Phiên 24 giờ · Tối đa **2 thiết bị** đồng thời / admin
- 2FA TOTP · Rate limiting · Token revocation
- OTP mở khóa dữ liệu máy · Single-device operator

### Tuân thủ pháp lý
17+ chính sách: Điều khoản · Bảo mật · GDPR · CCPA · Luật ANM VN · Chính sách giám sát nhân viên · DPA…

---

## Tích hợp nền tảng (149+)

Đăng nhập liên kết OAuth / API key cho:
**Jira · Slack · Google Workspace · GitHub · Microsoft · Trello · Confluence · Asana · Notion · HubSpot · Salesforce** và hàng trăm nền tảng khác.

- Đồng bộ tăng dần / toàn bộ
- Webhook receiver · Automation rules
- Sync log · Error reconnect · Field mapping

---

## ZMON Agent (Desktop)

Agent Windows chạy nền, giao diện nhân viên gồm:

- **Panel nổi** + **System tray**
- Nhắn tin nội bộ · Hỗ trợ · Công việc · Hộp thư
- Thông báo realtime + chuông
- Đa ngôn ngữ VI/EN
- Auto-update qua `download.zmon.vn`
- License activation · Heartbeat 2s · AFK detection

---

## Công cụ tiện ích Dashboard

| Công cụ | Mô tả |
|---|---|
| **Ctrl+K** | Tìm kiếm nhanh mọi trang, chức năng |
| **Hướng dẫn sử dụng** | Tài liệu A-Z tích hợp trong dashboard |
| **Gói của tôi** | Thông tin subscription, license đã dùng |
| **Mời doanh nghiệp** | Chương trình giới thiệu affiliate |
| **Giỏ hàng & Gia hạn** | Mua gói, thanh toán, nâng cấp |
| **Nhật ký hoạt động** | Audit trail toàn hệ thống |
| **Kích hoạt** | Tạo license, tải Agent, theo dõi slot |
| **Cài đặt chung** | Hạ tầng · Telegram · API/Webhook · Giới thiệu |
| **Hồ sơ** | Đổi mật khẩu, 2FA, avatar, thông tin cá nhân |

---

## Bản đồ tính năng đầy đủ

```
Z-MON
├── 🏠 Tổng quan                    KPI realtime · Biểu đồ · Quick access
├── 🤖 AI Trợ lý                    Streaming chat · 30 phiên · Phân tích A-Z
├── 💬 Nhắn tin                       Admin ↔ NV · Realtime · Đính kèm
├── 📋 Công việc
│   ├── Tổng quan công việc          Health · Velocity · AI Summary
│   ├── Nhân viên                    HR · Ca làm · Gán máy · Lương/giờ
│   ├── Danh sách công việc          List · Kanban · Lịch · Gantt
│   ├── Dự án công việc              Milestone · Progress
│   ├── AI Công việc                 NL task creation · Risk analysis
│   ├── Tiến độ                      Burndown · Velocity
│   ├── Kết nối nền tảng             149+ integrations
│   ├── Nhật ký công việc             Sync log · Automation
│   └── Mẫu công việc                Templates
├── 🖥️ Máy trạm
│   ├── Sơ đồ Agent                  Topology · Status map
│   ├── Máy quản lý                  13 forensic tabs · Remote control
│   └── Hiệu suất tổng máy           Fleet analytics · Comparison
├── 📊 Hiệu suất                     Machine + Work tabs
├── 📉 Phân tích thất thoát          Time + Cost (VND)
├── 🛡️ Kiểm soát gian lận           Autoclicker · Macro · Rules
├── 📑 Báo cáo                       CSV/Excel 5 sheets
├── 🔔 Cảnh báo                      Threshold · Severity · Workflow
├── 📣 Thông báo                     Hub · Push · Telegram
├── 🎫 Yêu cầu hỗ trợ               Ticket từ Agent
├── 📚 Kiến thức NV                  Knowledge base
├── ⏱️ Lịch sử chấm công            Attendance audit
├── 👤 Quản lý Operator              Roles · Permissions matrix
├── 🔑 Kích hoạt                     License · Agent download
├── ⚙️ Cài đặt chung                Infra · Notify · API
└── 🌐 Landing + Admin Platform     zmon.vn · SaaS billing · Legal
```

---

## Liên kết chính thức

| | |
|---|---|
| 🌐 **Website** | [zmon.vn](https://zmon.vn) |
| 📊 **Dashboard** | [my.zmon.vn](https://my.zmon.vn) |
| 📖 **Tài liệu** | [docs.zmon.vn](https://docs.zmon.vn) |
| ☁️ **API** | [cloud.zmon.vn](https://cloud.zmon.vn) |
| 📥 **Agent Update** | [download.zmon.vn](https://download.zmon.vn) |
| ✉️ **Hỗ trợ** | [support@zmon.vn](mailto:support@zmon.vn) |

---

## Tác giả

<p align="center">
  <img src="https://img.shields.io/badge/Phát_triển_bởi-QUANG_IT-009883?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjIiPjxwYXRoIGQ9Ik0xMiAyTDIgMTJoM2w3IDcgNy03aDNMMTIgMnoiLz48L3N2Zz4=" alt="QUANG IT" />
</p>

<p align="center">
  <strong>QUANG IT</strong><br/>
  <em>Kiến trúc sư & Nhà phát triển chính — Z-MON Việt Nam</em>
</p>

<p align="center">
  Z-MON được thiết kế, phát triển và vận hành bởi <strong>QUANG IT</strong> — kết hợp tư duy sản phẩm SaaS hiện đại,<br/>
  kỹ nghệ backend hiệu năng cao (Rust) và trải nghiệm dashboard doanh nghiệp chuẩn quốc tế.<br/>
  Sứ mệnh: mang lại minh bạch năng suất và giảm thất thoát chi phí lao động cho doanh nghiệp Việt Nam và khu vực.
</p>

<p align="center">
  <a href="https://github.com/zmonvietnam">GitHub</a> ·
  <a href="mailto:support@zmon.vn">Liên hệ hợp tác</a>
</p>

---

<p align="center">
  <sub>© 2026 Z-MON Việt Nam · Bản quyền thuộc về Z-MON · Phát triển bởi QUANG IT</sub><br/>
  <sub>Phần mềm thương mại · Dùng thử miễn phí 7 ngày</sub>
</p>
