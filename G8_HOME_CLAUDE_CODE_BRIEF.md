# G8 Home — Brief cho Claude Code

## 1. Mục tiêu

Tạo app báo cáo tuần cho **G8 MOSQUITO SWATTER FLASHLIGHT MANUFACTURING COMPANY LIMITED**, thương hiệu G8 Home, tương tự app Mbike hiện có.

App chỉ dùng **tiếng Việt**, không cần song ngữ. Người dùng phải nhìn nhanh được:

1. Tình trạng vận hành và các vấn đề ảnh hưởng đến sao, traffic, chuyển đổi.
2. Visitor đến từ đâu, level nào, tìm sản phẩm gì.
3. Buyer nào gần chốt đơn, đang vướng giá/ship/spec/MOQ và cần follow gì.
4. Tuần tới cần làm 3–7 việc nào.

## 2. Nguồn dữ liệu

- Vận hành: `1KwPZ4-Xx1UR8KS6glUiE8r2Djjn0-geUXfD1-f8LcyU`, tab `15-2-2026 đến 21-2-2026`, tên `G8 MOSQUITO SWATTER FLASHLIGHT MANUFACTURING COMPANY LIMITED BÁO CÁO TUẦN`.
- Visitor: `1qnpYOb_AJwOoO-apHY2ZcGSonkp01JR8Bq-rt7LyI4A`, tên `G8 Home - Visitor Analyzer - Theo dõi hàng tuần`.
  - Tuần này: `16-22.08`.
  - Tuần trước: `09-15.08`.
- OneTalk: `14UCEVfn8ECHJdpV0PGy21JGJLvPoGjLMy9dbEwWvJlE`, tên `g8_home_onetalk_leads_2026-07-23_29`.
  - Tab: `Tong quan`, `Khach uu tien`, `Can theo doi`, `It phan hoi`.

## 3. Dữ liệu đã chuẩn hóa

Claude Code phải đọc file [G8_HOME_FULL_DATA.json](G8_HOME_FULL_DATA.json), không cần mở lại Google Sheets.

- `ops.history`: **20 tuần** và đầy đủ 13 chỉ số vận hành.
- `visitors.countries`: **46 quốc gia** trong tuần hiện tại.
- `visitors.keywords`: **393 keyword duy nhất**, đã gộp số lần xuất hiện, PV, level và quốc gia.
- `leads.priority`, `leads.followup`, `leads.lowResponse`: dữ liệu OneTalk.

## 4. KPI vận hành

### Tuần 09–15/08/2026

- Số sao: **3**.
- Tổng sản phẩm: **1.127**.
- Sản phẩm mới: **3**.
- Visitor: **422**.
- Inquiry: **31**, đã trả lời **31**.
- RFQ đã báo giá: **0**, RFQ còn lại **20**.
- Phản hồi trung bình: **1,7 giờ**.
- Phản hồi trong 24h: **98,25%**.
- Super Product: **3**.
- Top Product: **55**.

### Vấn đề chính

- Chưa có GMV Trade Assurance.
- Marketing có 709 khách, còn thiếu 291 khách để đạt mốc tiếp theo.
- Chưa sử dụng quyền lợi RFQ trong tuần hiện tại.
- Cần tiếp tục tăng traffic tại các thị trường phát triển và cải thiện chuyển đổi đơn hàng.
- Lịch sử có giai đoạn **1.111/1.113 sản phẩm rủi ro**, cần ưu tiên kiểm tra và sửa listing.
- Có cảnh báo GPSR/chứng chỉ khi bán tại châu Âu.
- Cần duy trì thanh toán qua Alibaba để tạo giao dịch, review và độ tin cậy.

### Hành động tuần tới

1. Đăng 5–10 sản phẩm hot mỗi ngày.
2. Xử lý sản phẩm rủi ro, ưu tiên sản phẩm Top/Potential.
3. Báo RFQ và tăng traffic từ Mỹ/châu Âu; không chỉ tập trung thị trường đang phát triển.
4. Nâng sản phẩm Potential/Top lên Super Product.
5. Tạo đơn Trade Assurance, đặc biệt đơn mẫu cho buyer lớn.
6. Hoàn tất/cập nhật GPSR và chứng chỉ liên quan.
7. Dùng ảnh/video thật, ảnh nhà máy và thông tin sản phẩm đạt PIS tốt.

## 5. Visitor Analyzer

### Tuần này: 16–22/08/2026

- Visitor records: **218**.
- Quốc gia/vùng: **46**.
- PV gian hàng: **629**.
- Keyword chính xác: **448**.
- Visitor có keyword: **175**.
- Buyer L1+: **108**.
- Level: **L0 = 110, L1 = 35, L2 = 62, L3 = 9, L4 = 2**.
- Trang nguồn: **22**.

### Tuần trước: 09–15/08/2026

- Visitor records: **155**.
- Quốc gia/vùng: **39**.
- PV gian hàng: **422**.
- Keyword chính xác: **296**.
- Visitor có keyword: **110**.
- Buyer L1+: **76**.
- Level: **L0 = 79, L1 = 18, L2 = 50, L3 = 7, L4 = 1**.

### Insight

- Visitor tăng 155 → 218; PV tăng 422 → 629; keyword tăng 296 → 448.
- L1+ tăng 76 → 108, trong đó có cả L2/L3/L4; đây là tín hiệu chất lượng tốt hơn nhiều so với các nhà chỉ có L0/L1.
- Thị trường lớn: Bangladesh **40 visitor / 32 L1+**, Pakistan **36 / 12**, Ấn Độ **26 / 7**, Hoa Kỳ **20 / 11**.
- Bangladesh có 159 PV và 87 keyword records; Ấn Độ có 42 PV và 52 keyword records; Hoa Kỳ có 49 PV và 44 keyword records.
- Cần ưu tiên Hoa Kỳ và các buyer L2–L4; không chỉ nhìn số visitor lớn ở Bangladesh/Pakistan.

### Nhóm keyword

**Đúng ngành đèn LED:** `led bulb`, `led bulb raw material`, `18w led bulb`, `SKD LED bulb`, `LED DOB bulb`, `B22`, `E27`, `6500K`, `3200K`, `LED PCB`, `DOB driver`, `LED bulb wholesale`.

**Cơ hội liên quan:** `lighting`, `electric bulb`, `LED accessories`, `chargers`, `connectors`, `soldered and assembled`.

**Lệch ngành/cần xác minh:** `mens jeans`, `watch`, `toys`, `car parts`, `food processor`, `tea`, `airsoft`, `clothing`.

Bảng quốc gia và keyword toàn bộ phải lấy trực tiếp từ `G8_HOME_FULL_DATA.json`, không dùng danh sách mẫu.

## 6. OneTalk — buyer ưu tiên

### Nhóm cần xử lý ngay

1. **Abdul Halim** — 5.000 bóng LED SKD 12W/18W/7W/5W, B22/E27, 6500K/3200K; order card USD 0,13/pc, tổng USD 4.402,43, đang chờ thanh toán Alibaba. Gọi lại bước thanh toán, xác nhận cấu hình và Trade Assurance.
2. **Meelay Cho** — 4.000 pcs 6500K + 1.000 pcs 3200K, E27, Myanmar; cần shipping/landed cost. Tính ship Naypyidaw và xác nhận đóng gói.
3. **Qazi Zia** — 10.000 pcs LED SKD 12W, đã báo USD 0,23/pc EXW, cần video close-up top cover PP. Gửi video, hỏi địa chỉ và logo custom.
4. **Taraq Khan** — 5.000 pcs, đang tư vấn 15W SKD B22/E27 6500K, giá tham chiếu USD 0,13/pc. Chốt wattage/base và tạo order card.
5. **MD SHAMEM HOSSAN** — cần catalog/specs LED SKD 3W–50W, B22/E27. Gửi datasheet ngắn, hỏi wattage, CCT, qty và cảng nhận.
6. **Mohamed ElDawly** — 5.000 pcs SKD 12W, thấy giá USD 0,21/pcs cao; hỏi target price, nhấn mạnh bảo hành 2 năm/20.000 giờ và báo bậc 5k/10k/20k.
7. **Md Mannan** — hỏi PCB nhiều wattage, từng nói 3.000 pcs nhưng MOQ 5.000/size. Gửi bảng PCB/DOB và giải thích MOQ/mix mẫu.
8. **Huseyin Temel** — 9W warm white/white, lịch sử 100.000 units. Xác nhận assembled hay SKD, số lượng, gửi giá theo bậc.

### Buyer kỹ thuật cần theo dõi

- archil inaishvili: A70-12W/G01, 12–50W, A/T bulb; hỏi wattage/base/qty.
- Twara David: LED 9W–12W, base screw, B22/E27 220V; xác nhận base và số lượng thật.
- Sohail Aftab: DOB, hỏi carton packing, trọng lượng/kích thước; gửi packing specs.
- Sagar Hegde: connectors cần soldered/assembled; hỏi loại đầu nối, bản vẽ, qty và tiêu chuẩn test.
- Adilet Sagynbaev: LED 15W, 6500K, AC220V, CRI>84, 1370lm, E27/B22, MOQ 5.000.
- Mary Henewaa: cần 1.000 pcs mỗi loại nhưng MOQ factory 5.000; đề xuất mix wattage hoặc RTS.

### Rủi ro

- Không đưa các tin chỉ có `thank you`, `sir`, `for the inquiry`, auto reception hoặc hỏi MOQ nhỏ vào lead nóng.
- Aaron nambafu có yêu cầu WhatsApp; giữ trao đổi và báo giá trên Alibaba.
- Các buyer hỏi nhỏ hơn MOQ cần giải thích MOQ 5.000 pcs/wattage và đề xuất mix model nếu có.

## 7. Cấu trúc app — chỉ tiếng Việt

### Tab 1 — Tổng quan / Vận hành

- Header: `G8 Home — Báo cáo tuần | 09–15/08/2026`.
- KPI: 3 sao, 1.127 sản phẩm, 422 visitor, 31 inquiry, 0 RFQ tuần này, 3 Super Product, 55 Top Product, 98,25% phản hồi 24h.
- Cảnh báo: chưa có GMV TA, thiếu 291 Marketing visitor, listing rủi ro/GPSR, cần tăng traffic Mỹ/châu Âu.
- Biểu đồ xu hướng dùng toàn bộ 20 tuần trong `ops.history`.

### Tab 2 — Người xem

- KPI: 218 visitor, 46 quốc gia, 629 PV, 175 có keyword, 108 L1+.
- Bảng toàn bộ quốc gia: visitor, PV, keyword visitor, keyword records, L0–L4, L1+.
- Bảng toàn bộ keyword: keyword nguyên bản, số lần xuất hiện, PV, level, quốc gia.
- Bộ lọc theo quốc gia, level, keyword, PV và RFQ.

### Tab 3 — Buyer & tin nhắn

- Nhóm `Gần thanh toán`, `Lead số lượng lớn`, `Lead kỹ thuật`, `Cần theo dõi`, `Rủi ro/không ưu tiên`.
- Mỗi card: buyer, sản phẩm, qty, blocker, next action.
- Badge: `Thanh toán`, `Shipping`, `MOQ`, `Wattage`, `B22/E27`, `CCT`, `Spec`, `RFQ`.
- Nút copy hành động tiếp theo, không gửi tự động.

### Tab 4 — Kết luận & hành động

- Kết luận: traffic và buyer L1+ tăng, có nhiều buyer L2–L4, nhưng gian hàng cần chuyển traffic thành đơn TA và xử lý listing rủi ro/GPSR.
- Checklist 7 ngày: chốt Abdul/Meelay/Qazi/Taraq, xử lý listing rủi ro, khai thác RFQ, tăng traffic Mỹ/châu Âu, cập nhật chứng chỉ, tạo đơn mẫu TA.

## 8. Data contract

```js
const G8_HOME_DATA = {
  meta: {account:'G8 Home', opsPeriod:'09–15/08/2026', visitorPeriod:'16–22/08/2026'},
  ops: {history: []},
  visitors: {currentSummary:{}, previousSummary:{}, countries:[], keywords:[]},
  leads: {overview:[], priority:[], followup:[], lowResponse:[]}
};
```

Quy tắc:

- App chỉ dùng tiếng Việt.
- Dùng dữ liệu trong `G8_HOME_FULL_DATA.json`, không mở lại Google Sheets.
- Không bịa GMV, doanh thu, đơn hàng hoặc conversion rate.
- Không coi mọi visitor là buyer phù hợp; ưu tiên level + keyword + PV + hành vi.
- Giữ báo giá và thanh toán trên Alibaba.
- Mở được offline, responsive, desktop-first và không sửa các app khác.
