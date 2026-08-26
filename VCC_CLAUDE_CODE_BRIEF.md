# VCC Weekly Alibaba Report App — Brief cho Claude Code

## 1. Mục tiêu

Tạo một app HTML offline, trực quan và tương tự app Mbike hiện tại trong `index.html`.

App dành cho **VIET COLDCHAIN JOINT STOCK COMPANY**, theo dõi báo cáo tuần trên Alibaba.com.
Mục tiêu chính: người quản lý mở app là biết ngay:

1. Tuần này gian hàng đang tốt/xấu ở đâu.
2. Việc nào cần ưu tiên xử lý trong 48 giờ và 7 ngày.
3. Buyer nào cần follow để chốt đơn.
4. Traffic đến từ quốc gia nào và buyer level ra sao.

Không cần đọc lại Google Sheets khi chạy app. Nên nhúng dữ liệu đã chuẩn hóa vào một object JSON `VCC_DATA` trong HTML hoặc file `data.js`.

## 2. Ba nguồn dữ liệu gốc

### A. Sheet Vận hành

- Spreadsheet ID: `16wvQPpN8glsQbjyQ_gT_iYRQe19dlwGDSNsH23OcjHQ`
- URL: https://docs.google.com/spreadsheets/d/16wvQPpN8glsQbjyQ_gT_iYRQe19dlwGDSNsH23OcjHQ/edit
- Tab: `Trang tính1`
- Dữ liệu chính: các cột tuần từ `09-08-2026 đến 15-08-2026` lùi về trước.

### B. Sheet Visitor Analyzer

- Spreadsheet ID: `1yO-IJ7xmLCaiXQRut50XHzK5iIa6KQ9uMJQDVy3k2KE`
- URL: https://docs.google.com/spreadsheets/d/1yO-IJ7xmLCaiXQRut50XHzK5iIa6KQ9uMJQDVy3k2KE/edit
- Tab tuần hiện tại: `Tuần này · Tổng quan · 16-22.08`
- Tab visitor: `Tuần này · Khách truy cập · 16-22.08`
- Tab keyword: `Tuần này · Từ khóa · 16-22.08`
- Tab country: `Tuần này · Quốc gia · 16-22.08`
- Tab so sánh: `Tuần trước · Tổng quan · 09-15.08`

### C. Sheet OneTalk Leads

- Spreadsheet ID: `1hfqwG1AR1QPZXPgozWbjn4CCbl0dPzKpU0V8RhHvj4Q`
- URL: https://docs.google.com/spreadsheets/d/1hfqwG1AR1QPZXPgozWbjn4CCbl0dPzKpU0V8RhHvj4Q/edit
- Tab tổng quan: `Tong quan`
- Tab ưu tiên: `Khach uu tien`
- Tab theo dõi: `Can theo doi`
- Tab ít phản hồi: `It phan hoi`

## 3. Kỳ dữ liệu chuẩn để hiển thị

- Báo cáo vận hành gần nhất đầy đủ: `09-08-2026 đến 15-08-2026`.
- Visitor gần nhất: `16-08-2026 đến 22-08-2026`.
- OneTalk review: `12-08-2026 đến 18-08-2026`, cập nhật tổng quan `25/08/2026`.
- Vì 3 nguồn không cùng kỳ hoàn toàn, app phải ghi rõ kỳ dữ liệu dưới từng module và không tính một tỷ lệ funnel tổng hợp nếu khác kỳ.

## 4. Chỉ số Vận hành cần nhúng

### Tuần gần nhất: 09-08-2026 đến 15-08-2026

```json
{
  "period": "09-08-2026 đến 15-08-2026",
  "stars": 2,
  "total_products": 1025,
  "new_products": 1,
  "visitors": 103,
  "inquiries": 5,
  "inquiries_replied": 5,
  "rfq_quoted": 1,
  "rfq_remaining": 21,
  "avg_reply_hours": 4.84,
  "reply_24h_rate": 93.33,
  "super_products": 1,
  "top_products": 11
}
```

### Tuần trước: 02-08-2026 đến 08-08-2026

```json
{
  "period": "02-08-2026 đến 08-08-2026",
  "stars": 0,
  "total_products": 1024,
  "new_products": 0,
  "visitors": 77,
  "inquiries": 7,
  "inquiries_replied": 7,
  "rfq_quoted": 1,
  "rfq_remaining": 21,
  "avg_reply_hours": 5.74,
  "reply_24h_rate": 93.75,
  "super_products": 2,
  "top_products": 16
}
```

### Vấn đề và hướng xử lý đã có trong sheet Vận hành

- Marketing chỉ có `0 sao` trong các ghi chú vận hành; cần tăng traffic/quảng cáo để nâng sao.
- Traffic thấp; có xu hướng tập trung tại Việt Nam, chưa đủ thị trường Mỹ/EU.
- Có ghi chú `11 sản phẩm lỗi trên trang chủ` cần xử lý.
- Chưa liên kết EU Responsible Person.
- Tỷ lệ click từ hiển thị thấp; cần tối ưu ảnh chính, title, giá và MOQ.
- Cần tăng đơn thanh toán qua Alibaba / Trade Assurance.
- Kế hoạch tuần: đăng thêm sản phẩm high-demand, báo RFQ, nâng Basic lên Top/Super, làm nhiệm vụ traffic.

## 5. Chỉ số Visitor hiện tại và tuần trước

### Tuần này: 16-22.08.2026

```json
{
  "period": "16-22.08.2026",
  "visitor_records": 36,
  "countries": 14,
  "store_pv": 74,
  "exact_keyword_records": 57,
  "visitors_with_keyword": 23,
  "buyer_l1_plus": 6,
  "levels": {"L0": 30, "L1": 6, "L2": 0, "L3": 0, "L4": 0}
}
```

### Tuần trước: 09-15.08.2026

```json
{
  "period": "09-15.08.2026",
  "visitor_records": 32,
  "countries": 13,
  "store_pv": 103,
  "exact_keyword_records": 55,
  "visitors_with_keyword": 20,
  "buyer_l1_plus": 13,
  "levels": {"L0": 19, "L1": 13, "L2": 0, "L3": 0, "L4": 0}
}
```

### Quốc gia nổi bật tuần này

```json
[
  {"country":"Việt Nam","visitors":11,"pv":24,"l1_plus":2},
  {"country":"Trung Quốc","visitors":8,"pv":20,"l1_plus":0},
  {"country":"Hoa Kỳ","visitors":6,"pv":12,"l1_plus":2},
  {"country":"Hàn Quốc","visitors":1,"pv":1,"l1_plus":1},
  {"country":"Indonesia","visitors":1,"pv":2,"l1_plus":0},
  {"country":"Brazil","visitors":1,"pv":3,"l1_plus":0},
  {"country":"Đức","visitors":1,"pv":1,"l1_plus":0}
]
```

App vẫn cần giữ full country table từ sheet, nhưng màn hình chính chỉ hiển thị Top 5–7.

### Keyword nổi bật để hiển thị dạng bảng/search

Visitor đang tìm nhiều nhóm không hoàn toàn khớp ngành cold chain, ví dụ: `dried fruit`, `frozen fruit`, `frozen calamansi lime halves philippines`, `iqf frozen kiwifruit`, `passion fruit 1 kg price`, `frozen food`, `frozen whole passion fruit`.

Không cần hard-code toàn bộ keyword trên màn hình chính. Nhúng full keyword array để người dùng tìm kiếm/lọc khi mở tab chi tiết.

## 6. OneTalk: tổng quan và buyer cần ưu tiên

### Tổng quan

```json
{
  "updated": "25/08/2026",
  "review_period": "12/08-18/08/2026",
  "priority_count": 2,
  "follow_count": 6,
  "low_response_or_risk_count": 3,
  "real_response_leads": 4,
  "main_blockers": [
    "phí ship sample",
    "MOQ container",
    "giá cạnh tranh tại India",
    "buyer yêu cầu email ngoài Alibaba"
  ]
}
```

### Buyer cần đưa lên đầu app

```json
[
  {
    "name":"Mary Jane Zamora",
    "country":"Philippines",
    "priority":"Rất cao",
    "need":"Sample nhiều sản phẩm frozen fruits, pack 200g hoặc 500g",
    "signal":"Đã gửi địa chỉ nhận và hỏi phí ship sample",
    "next":"Gửi danh sách sample có thể gửi ngay, trọng lượng/dry ice, phí ship và ngày gửi mẫu"
  },
  {
    "name":"Keneth Adesulu",
    "country":"Chưa xác định",
    "priority":"Rất cao",
    "need":"Frozen whole passion fruit, pack 1kg",
    "signal":"Buyer hỏi giá nhưng seller chỉ nhận MOQ container 20ft",
    "next":"Nói rõ không/ có bán retail 1kg; nếu chỉ container thì báo MOQ, packing, giá/kg và lead time"
  },
  {
    "name":"Alviaa Alviaa",
    "country":"Chưa xác định",
    "priority":"Cao nhưng có rủi ro off-platform",
    "need":"HALAL IQF frozen taro, MOQ 1000",
    "signal":"Buyer để email ngoài Alibaba và muốn đặt hàng qua email",
    "next":"Giữ thông số, báo giá và order trên Alibaba; hỏi cut size, packing, quantity, destination port"
  },
  {
    "name":"Kirti Jain Kothari",
    "country":"India",
    "priority":"Trung bình-cao",
    "need":"IQF / freeze-dried fruits",
    "signal":"Quan tâm giá nhưng nói sản phẩm tại India đang rất rẻ",
    "next":"Chỉ chọn 3 SKU có lợi thế Việt Nam; báo FOB/container, chứng chỉ và điểm khác biệt"
  },
  {
    "name":"Mary Jane Zamora",
    "country":"Philippines",
    "priority":"Lead tốt - ưu tiên cao",
    "need":"01 x 40RF, retail packaging, sourcing nguyên liệu",
    "signal":"Trao đổi sâu về lead time và packaging",
    "next":"Chốt SKU, packing method, retail packaging và gửi timeline bulk vs retail"
  },
  {
    "name":"Carolina Santos",
    "country":"Chưa xác định",
    "priority":"Lead tốt - ưu tiên cao",
    "need":"Smart Food Kitchen Scales và Freeze-Dried Yogurt Melts, catalog/mẫu/custom logo",
    "signal":"Hỏi rõ catalog, giá, lead time, mẫu và packaging customization",
    "next":"Gửi catalog yoghurt melts; nói rõ nếu không có kitchen scales; hỏi flavor, pack size, target market, sample address"
  }
]
```

### Buyer theo dõi nhẹ

Các trường hợp chính cần giữ trong tab riêng, không đưa lên màn hình đầu:

- Maryorit: đã có order/mẫu 1kg, cần hỏi phản hồi và đề xuất đơn tiếp theo.
- Thong Pham: cần làm rõ lượng hàng, cảng đi/đến, nhiệt độ, LCL/FCL.
- ming ze ma: cần chụp ảnh mẫu và gửi thông số kỹ thuật như đã hứa.
- Kirti Jain Kothari: rào cản giá tại India; chỉ follow nếu có lợi thế khác biệt.
- Alviaa: lead sớm, cần hỏi lại SKU/spec.
- DOCK RACE WEAR: phản hồi “Okay”, chưa đủ nhu cầu.

### Ít phản hồi / rủi ro

Không ưu tiên trên dashboard chính:

- Yêu cầu gửi catalog qua email ngoài nhưng không rõ công ty/sản phẩm/số lượng.
- Supplier chào ngược hoặc không liên quan.
- Translation Tip / auto follow-up không có nhu cầu mua rõ.
- Buyer yêu cầu giữ trao đổi ngoài Alibaba: đánh dấu rủi ro và đưa về Alibaba.

## 7. Thiết kế app cần yêu cầu Claude Code

### Header

- Tên khách: `VIET COLDCHAIN JOINT STOCK COMPANY`.
- Ngành: `Cold Chain / Frozen Fruits / IQF / Freeze-dried`.
- Hiển thị kỳ dữ liệu của từng nguồn, vì không cùng ngày.
- Có dropdown khách hàng 01–08 nhưng VCC là khách đầu tiên.

### KPI đầu trang

Chỉ hiển thị 6 KPI dễ đọc:

1. Stars / trạng thái gian hàng: `2 sao` theo sheet Vận hành.
2. Visitor tuần này: `36` theo Visitor Analyzer.
3. Inquiry tuần vận hành: `5`.
4. Reply trong 24h: `93.33%`.
5. Buyer L1+: `6`.
6. Buyer cần ưu tiên: `6 dòng chi tiết / 4 lead có phản hồi thật`.

KPI phải có ghi chú nguồn và kỳ dữ liệu. Không gộp số liệu khác kỳ thành một funnel giả.

### 4 tab chính

1. **Vận hành**
   - 3 việc cần làm trong tuần.
   - Trend 14–15 tuần: products, visitors, inquiries, response rate.
   - RFQ quoted/remaining.
   - Star, Super Product, Top Product.
   - Bảng tuần chi tiết.

2. **Người xem**
   - Visitor records, countries, PV, keyword records, L1+.
   - Funnel L0 → L1 → L2 → L3 → L4.
   - Top country chart + full sortable country table.
   - Keyword search table.

3. **Buyer & tin nhắn**
   - Đưa 4–6 buyer ưu tiên lên đầu.
   - Có badge priority, quantity, signal, next action.
   - Sub-tabs: `Ưu tiên`, `Theo dõi nhẹ`, `Ít phản hồi/rủi ro`.
   - Có search buyer.

4. **Kết luận & action**
   - Kết luận P0/P1.
   - Action plan 48h / 7 ngày / tuần kế tiếp.
   - Owner: Sales, Ops, Manager.
   - Data gaps rõ ràng.

## 8. Logic chẩn đoán mặc định

- P0 nếu: giao hàng thấp, buyer đã gửi địa chỉ/sample/order, hoặc buyer cần chốt thông tin giá/MOQ.
- P1 nếu: RFQ còn nhiều, sản phẩm lỗi/thiếu thông tin, traffic lệch thị trường, cần tối ưu title/ảnh/MOQ.
- DATA nếu thiếu: Click, Inquiry visitors, Orders/TA orders, Data Overview cùng kỳ.
- Không gọi buyer là “hot” nếu chưa có tín hiệu thật trong message.
- Buyer yêu cầu chuyển email ngoài Alibaba phải gắn cờ rủi ro, không mặc định là lead tốt.
- Không tự suy luận doanh thu, conversion rate hoặc ROAS nếu sheet không có số cùng kỳ.

## 9. Cấu trúc dữ liệu nên dùng trong app

```js
const VCC_DATA = {
  profile: { name, industry, brand, report_period },
  ops: { latest, previous, weeks: [], recommendations: [], issues: [] },
  visitor: { latest, previous, levels: {}, countries: [], keywords: [], visitors: [] },
  messages: { summary, priority: [], follow_up: [], low_response: [] },
  sources: { ops_url, visitor_url, message_url }
};
```

Render dữ liệu bằng các hàm độc lập:

- `renderHeader()`
- `renderKpis()`
- `renderOpsPane()`
- `renderVisitorPane()`
- `renderBuyerPane()`
- `renderDiagnosisPane()`
- `renderSortableTable()`

## 10. Tiêu chí hoàn thành

- App mở offline bằng cách mở file HTML.
- Không cần gọi Google Sheets runtime để xem báo cáo đã nhúng.
- Có thể thay toàn bộ dữ liệu khách bằng cách sửa một object `VCC_DATA`.
- Không cần Claude Code tự đọc lại 3 Google Sheets để dựng giao diện.
- Có ghi rõ kỳ dữ liệu và nguồn của từng metric.
- Có tab chi tiết nhưng màn hình đầu chỉ tập trung vào các việc cần làm.
- Giao diện tiếng Việt, phong cách sạch giống app Mbike hiện tại: header navy, KPI cards, tab navigation, charts, tables, diagnosis.
