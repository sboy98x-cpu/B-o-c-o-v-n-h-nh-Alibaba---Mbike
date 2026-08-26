# CM Decor — Brief cho Claude Code

## 1. Mục tiêu

Xây dựng app báo cáo tuần cho gian hàng **CM Decor** trên Alibaba.com, tương tự app Mbike hiện có trong `index.html`, nhưng tập trung vào 4 câu hỏi:

1. Tuần này gian hàng đang khỏe hay yếu ở điểm nào?
2. Khách truy cập đến từ quốc gia nào, xem sản phẩm/nhóm từ khóa nào và ở level nào?
3. Buyer nào cần follow ngay, vấn đề của họ là gì và bước tiếp theo để chốt đơn?
4. Tuần tới cần làm ít việc nào nhưng tác động lớn nhất?

App phải đọc nhanh trên một màn hình, phù hợp để chụp màn hình gửi báo cáo. Không biến thành bảng dữ liệu dài.

## 2. Nguồn dữ liệu đã chuẩn hóa

### Vận hành

- Spreadsheet: `1d94o5XOL1fU1gHnJQQ6ki1uBu1mE2JbUShXm92RZsYo`
- Tên: `CMDECOR BÁO CÁO TUẦN`
- Tab chính: `Trang tính1`
- Kỳ mới nhất trong bảng: `09-08-2026 đến 15-08-2026`
- Kỳ so sánh: `02-08-2026 đến 08-08-2026`

### Visitor Analyzer

- Spreadsheet: `1Ct6zBQ0Ryuw5VnpagOnACZGu9OBwPG8msAtrU5jbLVM`
- Tên: `CM Decor - Visitor Analyzer - Theo dõi hàng tuần`
- Tab hiện tại:
  - `Tuần này · Tổng quan · 16-22.08`
  - `Tuần này · Khách truy cập · 16-22.08`
  - `Tuần này · Từ khóa · 16-22.08`
  - `Tuần này · Quốc gia · 16-22.08`
- Tab so sánh: `Tuần trước · ... · 09-15.08`

### OneTalk Leads

- Spreadsheet: `1mnEzH8wn-6ZboYRkYP3QmU3yX0LUqWs4s4L9WTcGYKI`
- Tên: `CM Decor OneTalk Leads 2026-08-18`
- Tab sử dụng:
  - `Tong quan`
  - `Khach uu tien`
  - `Can theo doi`
  - `It phan hoi`

## 3. KPI vận hành cần hiển thị

Kỳ mới nhất / kỳ trước:

| Chỉ số | Tuần này | Tuần trước | Ý nghĩa hiển thị |
|---|---:|---:|---|
| Số sao | 0 | 1 | Cảnh báo đỏ; forecast hiện tại 1 sao |
| Tổng sản phẩm | 1.061 | 1.061 | Không tăng sản phẩm |
| Sản phẩm mới | 0 | 0 | Cần khởi động lại lịch đăng |
| Tổng người ghé thăm | 196 | 74 | Tăng mạnh, nhưng cần kiểm tra chất lượng |
| Inquiry | 1 | 2 | Giảm nhẹ |
| Inquiry đã trả lời | 1 | 2 | Tỷ lệ trả lời 100% |
| RFQ đã báo giá | 0 | 0 | Chưa sử dụng RFQ |
| RFQ còn lại | 20 | 20 | Còn nguồn cơ hội để khai thác |
| Thời gian phản hồi trung bình | 0h | 0h | Dữ liệu hiển thị là 0h, không suy diễn thêm |
| Trả lời trong 24h | 100% | 100% | Điểm vận hành tốt |
| Super Product | 0 | 0 | Chưa có |
| Top Product | 0 | 1 | Đang giảm |

### Cảnh báo vận hành đã có trong dữ liệu

- Gian hàng hiện **0 sao**, forecast **1 sao**.
- Marketing mới có **115 khách**.
- Service mới có **2 người mua phản hồi**.
- Chưa có GMV Trade Assurance.
- Có **1 sản phẩm gặp vấn đề**, **63 sản phẩm điểm thấp**.
- Chưa có Top Product/Super Product ở kỳ mới nhất.
- Chưa sử dụng RFQ.
- Không đăng sản phẩm mới trong tuần.
- Tránh đăng hình/sản phẩm có logo tranh bóng đá hoặc dấu hiệu vi phạm bản quyền thương hiệu.

### Hành động tuần tới

1. Đăng 5–10 sản phẩm decor/lighting có nhu cầu mỗi ngày.
2. Bổ sung ảnh thật, video thật, kích thước, vật liệu, MOQ và thông tin đóng gói.
3. Xử lý 63 sản phẩm điểm thấp và sản phẩm lỗi trước khi mở rộng danh mục.
4. Khai thác RFQ còn lại; ưu tiên nhu cầu phù hợp lighting/decor.
5. Đẩy sản phẩm đủ điều kiện lên Top/Super Product.
6. Tạo đơn Trade Assurance để bắt đầu có GMV và tín hiệu giao dịch.

## 4. KPI Visitor Analyzer

### Tuần này: 16–22/08/2026

- Bản ghi khách truy cập: **21**
- Quốc gia/vùng: **18**
- PV trên gian hàng: **33**
- Bản ghi keyword chính xác: **53**
- Visitor có keyword: **18**
- Buyer L1+: **10**
- Level: **L0 = 11, L1 = 10, L2 = 0, L3 = 0, L4 = 0**
- Số trang nguồn đã lấy: **3**

### Tuần trước: 09–15/08/2026

- Bản ghi khách truy cập: **24**
- Quốc gia/vùng: **16**
- PV trên gian hàng: **196**
- Bản ghi keyword chính xác: **66**
- Visitor có keyword: **22**
- Buyer L1+: **10**
- Level: **L0 = 14, L1 = 10, L2 = 0, L3 = 0, L4 = 0**

### Insight cần đưa lên dashboard

- Số buyer L1+ giữ nguyên ở mức 10 dù PV giảm mạnh; đây là nhóm cần ưu tiên.
- Traffic tuần này phân tán: 18 quốc gia, phần lớn mỗi nước chỉ có 1 visitor.
- Trung Quốc có 4 visitor nhưng đều L0; không nên xem đây là nhóm ưu tiên bán hàng.
- Các tín hiệu L1 đáng chú ý đến từ Togo, Ấn Độ, Campuchia, Colombia, Papua New Guinea, Thái Lan, Pháp, Hàn Quốc, Jamaica và một số nước khác.
- Keyword có tín hiệu decor/lighting: `hand tufted wool rug`, `wall art`, `abstract art print`, `gate light`, `quartz wall clock`, `outdoor spotlight`, `dcor maison`, `tapis salon modern`, `paintings and wall arts`.
- Một số keyword không phù hợp danh mục hoặc có ý định nghiên cứu rộng; cần hiển thị nhãn “cần xác minh”, không coi là lead nóng.

### Country data tối thiểu cần nhúng

```js
const countries = [
  {country:'China', visitors:4, pv:5, keywordVisitors:4, keywordRecords:12, l1Plus:0, level:'L0'},
  {country:'India', visitors:1, pv:2, keywordVisitors:1, l1Plus:1, level:'L1'},
  {country:'Cambodia', visitors:1, pv:1, keywordVisitors:1, l1Plus:1, level:'L1'},
  {country:'Colombia', visitors:1, pv:1, keywordVisitors:1, l1Plus:1, level:'L1'},
  {country:'Papua New Guinea', visitors:1, pv:3, l1Plus:1, level:'L1'},
  {country:'Togo', visitors:1, pv:3, l1Plus:1, level:'L1'},
  {country:'Thailand', visitors:1, pv:1, l1Plus:1, level:'L1'},
  {country:'France', visitors:1, pv:1, l1Plus:1, level:'L1'},
  {country:'South Korea', visitors:1, pv:1, l1Plus:1, level:'L1'},
  {country:'Jamaica', visitors:1, pv:1, l1Plus:1, level:'L1'}
];
```

## 5. OneTalk — danh sách cần xử lý

Tổng quan: **2 khách ưu tiên, 2 cần theo dõi, 6 ít phản hồi/rủi ro**. Có **3 buyer có tín hiệu mua thật**: Hannahchiwendu Christopher, Friedrich Donges, Kyei Kyei.

### Ưu tiên cao

| Buyer | Nhu cầu | Vấn đề | Bước tiếp theo |
|---|---|---|---|
| Hannahchiwendu Christopher | Đèn pendant/lantern M03.01, hỏi 1–2 pcs | Thiếu địa chỉ, số lượng cuối và phí ship | Xác nhận USD 32/pc, hỏi địa chỉ đầy đủ + postal code, báo ship/thời gian, đề xuất Trade Assurance |
| Janez Korelc — UK | Giải pháp đèn indoor cho thị trường UK | Chưa có số lượng; cần chứng từ an toàn | Gửi CE/UKCA/RoHS nếu có, hỏi dòng sản phẩm và qty |
| Friedrich Donges — Greece | Đã gửi product card, có unread | Chưa rõ sản phẩm/qty/địa chỉ | Trả lời trong Alibaba, hỏi product + qty + country, gửi catalog phù hợp, báo giá trong ngày |
| Kyei Kyei — Ghana | Đồng hồ treo tường tròn quartz | Chưa rõ kim hay digital, qty chưa rõ | Gửi 3 mẫu, MOQ/sample price/size/material, hỏi chọn kim hay digital và trial qty |

### Cần theo dõi

- DK Gupta: hỏi mục đích sử dụng đèn; cần indoor/outdoor, project, qty, target price.
- Nguyen Hung — Việt Nam: hỏi đèn sân vườn; cần loại, công suất, qty, địa điểm, ngân sách.
- Svetlana Kononiuk — US: hỏi chiều cao/trọng lượng đèn solar; gửi thông số, quy cách đóng gói, ảnh thật và hỏi qty.
- Arnold Amet — Papua New Guinea: quan tâm kiểu artistic/metal; gửi 2–3 mẫu, hỏi size/color/qty.
- Nhóm hỏi indoor lighting cho UK: chỉ cung cấp CE/RoHS/UKCA nếu có, xác minh công ty/sản phẩm/qty.

### Ít phản hồi / rủi ro

- Các yêu cầu xin catalog/báo giá qua email ngoài Alibaba: `luyalcomunication@zohomail.com`, `SALESEXPORT@INTERNET.RU`, `maxelectro05@gmail.com`, `spencesales25@gmail.com`.
- Không gửi thông tin nhạy cảm hoặc chuyển giao dịch ra ngoài Alibaba khi chưa xác minh.
- Williams mark: nội dung thiên về promotion, chưa phải buyer decor rõ ràng.
- sabreee jak: có dấu hiệu muốn dẫn sang website ngoài; hỏi lại product/qty và giữ trao đổi trên Alibaba.

## 6. Cấu trúc app đề xuất

Giữ lại mô hình hiện tại của Mbike: một file HTML offline, dữ liệu mock/đã chuẩn hóa nằm trong object `D`, biểu đồ ECharts và 4 tab.

### Tab 1 — Tổng quan / Vận hành

- Header: `CM Decor — Báo cáo tuần | 16–22/08/2026`
- Bộ lọc kỳ báo cáo: tuần này, tuần trước, 30 ngày.
- 6 KPI lớn: sao, visitor, inquiry, L1+, Top/Super Product, cảnh báo cần xử lý.
- Card “3 việc phải làm tuần này”.
- Card “Vấn đề lớn nhất”: 0 sao, 63 sản phẩm điểm thấp, chưa dùng RFQ, chưa có GMV TA.
- Sparkline so sánh visitor/inquiry/Top Product theo tuần.

### Tab 2 — Người xem / Visitor

- KPI: 21 visitors, 18 quốc gia, 33 PV, 10 L1+.
- Bar chart quốc gia; nhóm L1+ nổi bật đặt trước L0.
- Keyword chips có phân nhóm: decor, lighting, clock, furniture, không liên quan/cần xác minh.
- Funnel đơn giản: visitor → có keyword → L1+; không tự tạo inquiry/purchase nếu nguồn không có dữ liệu.
- Bảng lọc theo quốc gia, level, keyword, PV, RFQ.

### Tab 3 — Buyer & tin nhắn

- KPI: 3 buyer có tín hiệu thật, 4 ưu tiên xử lý, 6 rủi ro/ít phản hồi.
- Bảng card theo mức ưu tiên: `Làm ngay`, `Theo dõi`, `Không ưu tiên`.
- Mỗi card chỉ hiển thị 4 dòng: buyer, nhu cầu, blocker, next best action.
- Nút `Copy next action` để nhân viên lấy câu nhắc xử lý.
- Không hiển thị email ở màn hình chính; chỉ hiện badge “off-platform risk”.

### Tab 4 — Kết luận & action plan

- Kết luận ngắn: traffic tăng nhưng chất lượng/chuyển đổi chưa đủ; nhóm L1+ có thể khai thác; gian hàng đang bị giới hạn bởi chất lượng sản phẩm, rating và thiếu hoạt động RFQ/TA.
- Checklist 7 ngày, mỗi việc có owner/status/due date.
- Block “điều kiện thành công”: có sản phẩm mới, xử lý sản phẩm điểm thấp, ít nhất một RFQ được báo giá, tạo tín hiệu TA, thu thêm buyer response.

## 7. Data contract cho Claude Code

Claude Code không cần đọc Google Sheets khi chạy app. Hãy tạo một object duy nhất, ví dụ:

```js
const CM_DECOR_DATA = {
  meta: {account:'CM Decor', currentPeriod:'16–22/08/2026', opsPeriod:'09–15/08/2026'},
  ops: {current:{}, previous:{}, alerts:[], actions:[]},
  visitors: {current:{}, previous:{}, countries:[], keywords:[], records:[]},
  leads: {summary:{}, priority:[], followup:[], lowResponse:[]}
};
```

Quy tắc:

- Dùng đúng các số liệu ở brief này làm dữ liệu ban đầu.
- Các trường thiếu dữ liệu phải để `null` hoặc `Chưa có dữ liệu`, không tự bịa.
- Phân biệt kỳ Visitor `16–22/08` với kỳ vận hành `09–15/08`; hiển thị rõ ngày trên từng tab.
- Không tạo conversion rate, GMV, đơn hàng hoặc doanh thu nếu nguồn không có số liệu.
- Không gửi email/tin nhắn tự động; app chỉ hỗ trợ xem và copy next action.
- Giữ giao dịch trên Alibaba; các email ngoài nền tảng chỉ là cảnh báo rủi ro.
- Dùng màu: đỏ = xử lý ngay, cam = cần theo dõi, xanh = tín hiệu tốt, xám = chưa có dữ liệu.
- Thiết kế desktop-first 1440px nhưng responsive; ưu tiên khoảng trắng, card ngắn, không dùng bảng quá nhiều cột.

## 8. Tiêu chí hoàn thành

- Mở `index.html` là xem được ngay, không cần backend.
- Người dùng hiểu trong 10 giây: tình trạng gian hàng, 3 vấn đề lớn nhất, 3 buyer cần xử lý.
- Có thể chụp màn hình từng tab làm báo cáo tuần.
- Không cần đọc lại 3 Google Sheets để hiểu dữ liệu ban đầu.
- Có cấu trúc dữ liệu tách khỏi UI để tuần sau chỉ thay `CM_DECOR_DATA`.
- Dữ liệu đầy đủ để dựng biểu đồ và bảng chi tiết nằm tại [CM_DECOR_FULL_DATA.json](CM_DECOR_FULL_DATA.json). Claude Code phải đọc file này để lấy toàn bộ lịch sử tuần, danh sách quốc gia và keyword; không dùng các ví dụ rút gọn trong brief làm toàn bộ dữ liệu.
- Cấu trúc file: `CM_DECOR_FULL_DATA.ops.history` = toàn bộ tuần và 13 chỉ số vận hành; `CM_DECOR_FULL_DATA.visitors.countries` = toàn bộ quốc gia trong tuần hiện tại; `CM_DECOR_FULL_DATA.visitors.keywords` = toàn bộ keyword chính xác đã gộp theo keyword, gồm `occurrences`, `pv`, level và quốc gia.
