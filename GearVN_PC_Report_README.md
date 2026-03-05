# GearVN · PC Category — Weekly Report Framework

> Tài liệu mô tả những gì đã xây dựng cho báo cáo tháng 2/2026 và định nghĩa framework báo cáo tuần chuẩn cho PC Category.

---

## 📦 I. Những Gì Đã Làm — Tháng 2/2026

### Dashboard HTML (`FEB2026_Revenue_Dashboard.html`)

Dashboard tích hợp 3 nguồn dữ liệu thực tế, gồm 3 tab phân tích:

| Tab | Nội dung | Biểu đồ |
|-----|----------|---------|
| **Doanh Thu** | Rev theo ngày (Offline / Online / Sàn), tỷ trọng kênh | Line chart · Pie · Stacked bar |
| **Đơn Hàng & AOV** | Số đơn Online vs Offline, AOV từng ngày vs TB tháng | Stacked bar · Combo chart |
| **ROAS & Chi Phí Ads** | Rev vs Ad Spend, ROAS/ngày, cơ cấu GG/FB, bảng ROAS | 4 hero cards · 4 charts · Table |

### Nguồn dữ liệu đã xử lý

| File | Nội dung |
|------|----------|
| `FEB_2026_Sheet8.csv` | Doanh thu theo ngày · 4 nhóm kênh: Offline / Sàn TMĐT / Online / Khác |
| `FEB_2026_Donhang_Kenh.csv` | Số đơn Online & Offline · AOV = (Rev Onl + Rev Off) / (Đơn Onl + Đơn Off) |
| `FEB_2026_GG_Ad.csv` | Chi phí GG Ads & FB Ads từng ngày · ROAS theo ngày và tổng tháng |

### KPI Highlights — Tháng 2/2026

| Chỉ số | Giá trị | Ghi chú |
|--------|---------|---------|
| Tổng Doanh Thu | **7.88 tỷ ₫** | 22 ngày hoạt động |
| Tổng Đơn Hàng | **548 đơn** | Online + Offline |
| AOV | **13,261,938 ₫** | (Rev Onl+Off) / Tổng đơn |
| Tổng Ad Spend | **102.6 triệu** | GG: 25.2tr · FB: 77.4tr |
| ROAS Tổng Tháng | **76.9x** | |
| Ngày DT cao nhất | **726tr — 25/02** | |
| ROAS cao nhất | **226.8x — 21/02** | Ngày đầu sau Tết |

### Lưu ý dữ liệu tháng 2

- Nghỉ Tết Nguyên Đán **15–20/02**: không có doanh thu nhưng vẫn chi ~13.2tr/ngày FB Ads
- Ngày **11/02**: cột Khác có lỗi `#REF!` trong nguồn — đã bỏ qua khi tính toán
- **AOV cao nhất 03/02** (~26.9tr): ngày doanh thu lớn với ít đơn hàng
- **Kênh Offline** chiếm >50% tổng doanh thu — kênh trọng tâm cần bảo vệ

---

## 📋 II. Framework Báo Cáo Tuần

---

### 🔵 A | Số Revenue / Order / AOV

#### A1. Doanh Thu Theo Kênh Bán

Phân tích theo 4 nhóm kênh, so sánh tuần/tháng/target:

| Kênh | Định nghĩa | Tỷ trọng mục tiêu | Nguồn dữ liệu |
|------|-----------|-------------------|---------------|
| **Offline** | Cửa hàng: HHT, KVC, NCV, Thái Hà, THĐ | **>50% tổng DT** | POS / ERP |
| **Online** | Website, Chat, Tổng đài | ~35% tổng DT | GA4 / CRM |
| **Sàn TMĐT** | Shopee, TikTok Shop | ~10% tổng DT | Seller Center |
| **Khác** | Nguồn phát sinh ngoài phân loại | <5% tổng DT | Manual |

**Checklist:**
- [ ] Kênh Offline có đạt >50% tổng DT không?
- [ ] So sánh WoW (tuần này vs tuần trước) từng kênh
- [ ] So sánh với target tháng — tiến độ đang ở mức nào?
- [ ] Kênh nào tăng/giảm bất thường → escalate ngay

**Bảng theo dõi doanh thu tuần:**

| Kênh | Tuần này | Tuần trước | WoW % | Target tháng | Tiến độ % |
|------|----------|------------|-------|-------------|-----------|
| Offline | | | | | |
| Online | | | | | |
| Sàn TMĐT | | | | | |
| Khác | | | | | |
| **TỔNG** | | | | | |

---

#### A2. Số Order & AOV

```
AOV = (Doanh thu Online + Doanh thu Offline) / (Đơn Online + Đơn Offline)
      ⚠️  Không bao gồm doanh thu Sàn TMĐT
```

**Bảng theo dõi tuần:**

| Chỉ số | Tuần này | Tuần trước | WoW % | Target |
|--------|----------|------------|-------|--------|
| Đơn Online | | | | |
| Đơn Offline | | | | |
| Tổng Đơn | | | | |
| AOV | | | | |

> Nếu AOV giảm: kiểm tra cơ cấu đơn — nhiều đơn giá thấp hay ít đơn cao?

---

#### A3. SKUs Focus

- Liệt kê top 5–10 SKU doanh thu cao nhất trong tuần
- Đánh dấu SKU nằm trong danh sách Focus tháng
- So sánh số lượng bán SKU focus vs tuần trước
- Nếu SKU focus không đạt: kiểm tra tồn kho / giá / hiển thị sản phẩm

| SKU | Tên sản phẩm | Số lượng bán | Doanh thu | vs Tuần trước | Focus? |
|-----|-------------|-------------|----------|--------------|--------|
| | | | | | ⭐ |
| | | | | | |
| | | | | | |

---

### 🟣 B | Chỉ Số Marketing

#### B1. Paid Ads — Facebook Campaign Overview

So sánh với tuần trước và benchmark đề ra (riêng cho từng hạng mục):

| Chỉ số | Tuần này | Tuần trước | WoW % | Benchmark | Đạt? |
|--------|----------|------------|-------|-----------|------|
| Reach | | | | WoW ≥ 0% | |
| Impressions | | | | WoW ≥ 0% | |
| CTR | | | | ≥ 1.5% | |
| CPC | | | | ≤ 5,000 ₫ | |
| CPM | | | | Theo ngành | |
| ROAS (FB) | | | | ≥ 5x | |
| Ad Spend | | | | Theo plan | |

**Bài Ad tốt nhất trong tuần:**
- Link / screenshot ad có CTR cao nhất hoặc ROAS tốt nhất
- Phân tích: tại sao ad này hoạt động tốt? (hook / visual / offer / audience)

**Bài Ad lụm nhặt từ đối thủ:**
- 1–2 ad hay thấy từ đối thủ (PC gaming / tech) trên feed
- Nhận xét: điểm gì có thể học / adapt cho GearVN?

**Key Action tuần này:**
- [ ] Kiểm soát budget: Tăng/giảm ngân sách theo hiệu suất campaign
- [ ] Đổi mới Creative: Thay ad set yếu, test format/hook mới
- [ ] Audience: Mở rộng hoặc thu hẹp tệp nếu cần

---

#### B2. ROAS — Google Ads + Facebook Ads

```
ROAS = Tổng Doanh Thu / (GG Ad Spend + FB Ad Spend)
```

**Cách lấy GG Ads budget:**
1. Vào **Google Ads** → Reports → Predefined reports → Time → **Daily**
2. Lọc theo date range tuần báo cáo, lấy cột `Cost`
3. Hoặc: Billing → Transaction history để xem chi phí thực tế

**Bảng ROAS tuần:**

| Nguồn | Ad Spend tuần này | Ad Spend tuần trước | WoW % | ROAS | Benchmark |
|-------|------------------|---------------------|-------|------|-----------|
| Google Ads | | | | | ≥ 10x |
| Facebook Ads | | | | | ≥ 5x |
| **TỔNG** | | | | | **≥ 7x** |

> 📌 Benchmark tháng 2/2026: ROAS tổng tháng = **76.9x** (tháng Tết đặc thù — chi phí thấp tuần Tết)

---

#### B3. Traffic — Trendline 3 Tháng

Nguồn: **Google Analytics 4** → Reports → Acquisition → Traffic acquisition

| Nguồn Traffic | Sessions tuần này | vs Tuần trước | vs KPI | Đánh giá | Action nếu giảm |
|--------------|------------------|--------------|--------|----------|----------------|
| Organic Search | | | | | Kiểm tra SEO, content, indexing |
| Paid Search (GG) | | | | | Review keyword, bid, landing page |
| Social (FB/TikTok) | | | | | Tăng frequency, đổi creative |
| Direct | | | | | Brand awareness check |
| Referral | | | | | Partner / affiliate review |
| **TỔNG** | | | | | |

**Key Learning:**
- Trendline 3 tháng đang có xu hướng tăng / giảm / ổn định?
- Nguồn nào đang contribute nhiều nhất / ít nhất?
- Lượng traffic tuần qua diễn biến như thế nào?

**Key Action:**
- Nếu traffic giảm >10% WoW: phân tích nguyên nhân từng nguồn → đề xuất action cụ thể
- [ ] ...
- [ ] ...

---

#### B4. Social Media — Metrics & Content

| Platform | Reach | Engagement Rate | Follower Growth | vs Tuần trước | vs KPI |
|----------|-------|-----------------|-----------------|--------------|--------|
| Facebook Page | | | | | |
| TikTok | | | | | |
| YouTube | | | | | |
| Instagram | | | | | |

**Content review:**
- Bài đăng nào đạt reach / engagement cao nhất trong tuần?
- Format nào hoạt động tốt (video / ảnh / carousel / Reels)?

**Key Action:**
- [ ] ...
- [ ] ...

---

### 🟢 C | Tasklist for Cate

#### C1. Những Việc Đã Làm Trong Tuần

> Format: `[Tên việc] — [Kết quả / Hiệu quả đo được]`

| STT | Việc đã làm | Ngày | Kết quả / Hiệu quả | Ghi chú |
|-----|------------|------|-------------------|---------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

#### C2. Planning Tuần Tới

> Format: `[Tên việc] — [Mục tiêu cụ thể] — [Deadline]`

| STT | Việc cần làm | Mục tiêu | Deadline | Độ ưu tiên |
|-----|-------------|---------|----------|------------|
| 1 | | | | 🔴 High |
| 2 | | | | 🔴 High |
| 3 | | | | 🟡 Medium |
| 4 | | | | 🟡 Medium |
| 5 | | | | 🟢 Low |

---

## 🗂️ III. Cấu Trúc File & Quy Ước Đặt Tên

```
GearVN_PC_Reports/
├── data/
│   ├── FEB_2026_Sheet8.csv            # Doanh thu theo kênh
│   ├── FEB_2026_Donhang_Kenh.csv      # Đơn hàng & AOV
│   └── FEB_2026_GG_Ad.csv             # Ad spend GG + FB
├── dashboard/
│   └── FEB2026_Revenue_Dashboard.html
└── README.md
```

**Quy ước đặt tên file data:**
```
{MONTH}_{YEAR}_{DESCRIPTION}.csv
Ví dụ: MAR_2026_Rev_Kenh_Day.csv
```

---

*GearVN · PC Category · Cập nhật lần cuối: 02/2026*
