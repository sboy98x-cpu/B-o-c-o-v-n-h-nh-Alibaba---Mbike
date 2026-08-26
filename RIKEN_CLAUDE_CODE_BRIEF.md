# Riken — Brief cho Claude Code

## 1. Mục tiêu

Tạo app báo cáo tuần cho **RIKEN VIET NAM CO LTD**, tương tự app Mbike hiện có trong `index.html`.

App phải giúp người dùng nhanh chóng biết:

1. Gian hàng đang ở mức sao nào, vấn đề nào ảnh hưởng đến traffic và chuyển đổi?
2. Visitor đến từ đâu, thuộc level nào và đang tìm sản phẩm abrasive/sanding/tool nào?
3. Buyer nào đã có nhu cầu thật, thiếu thông số gì và cần làm gì tiếp theo để báo giá/chốt đơn?
4. Tuần tới cần ưu tiên 3–5 hành động nào?

Giao diện song ngữ có thể dùng tiếng Việt làm ngôn ngữ chính; dữ liệu nguồn có cả tiếng Trung. Thiết kế card ngắn, ưu tiên đọc nhanh và chụp màn hình báo cáo.

## 2. Nguồn dữ liệu

- Vận hành: `1UlxJruIUI9LH-g10mVVLqjUWOyS45gyPIsRjO12N0QI`, tab `Trang tính1`, tên `RIKEN VIET NAM CO LTD - Báo Cáo Tuần`.
- Visitor: `1Fs4Bces592xi67xKvfttG2O4Imk9p6wsE2w7vFjgOjI`, tên `RIKEN VIET NAM CO LTD - vn19068503409mzos`.
  - Tuần này: `16-22.08`.
  - Tuần trước: `10-16.08`.
  - Tab có song ngữ Việt/Trung: Tổng quan, Khách truy cập, Từ khóa, Quốc gia.
- OneTalk: `1lgfpYWEQconuxATb3E0Z717nCgsmQrnyGdSZyzunYRE`, tên `RIKEN OneTalk Leads Song ngu Viet Trung 2026-08-18`.
  - Tab: `Tong quan 总览`, `Khach uu tien 重点客户`, `Can theo doi 继续跟进`, `It phan hoi 低优先级`.

## 3. KPI vận hành

| Chỉ số | Tuần 09–15/08 | Tuần trước trong bảng | Ý nghĩa |
|---|---:|---:|---|
| Số sao | 1 | 1 | Gian hàng vẫn ở 1 sao |
| Tổng sản phẩm | 2.340 | 2.201 | Catalog tăng |
| Sản phẩm mới | 139 | 1.251 | Vẫn tăng nhưng giảm mạnh so với đợt trước |
| Visitor | 119 | 175 | Traffic giảm |
| Inquiry | 4 | 2 | Inquiry tăng |
| Inquiry đã trả lời | 4 | 2 | Tỷ lệ trả lời 100% |
| RFQ đã báo giá | 5 | 15 | Đã dùng RFQ nhưng giảm |
| RFQ còn lại | 29 | 16 | Còn nhiều cơ hội |
| Phản hồi trung bình | 0,72h | 0,04h | Tốc độ vẫn tốt |
| Phản hồi trong 24h | 100% | 100% | Điểm vận hành tốt |
| Super Product | 0 | 0 | Chưa có |
| Top Product | 3 | 1 | Có cải thiện |

Toàn bộ lịch sử các tuần và 13 chỉ số nằm trong `RIKEN_FULL_DATA.json` tại `ops.history`.

### Vấn đề chính

- Forecast chỉ **1 sao**; Marketing có **209 visitor**, còn thiếu **91** để lên mốc tiếp theo; Service có **14 buyer phản hồi**, còn thiếu **1**.
- Có **501 sản phẩm gây hiểu nhầm**, ảnh hưởng chất lượng và trọng số tìm kiếm.
- Chưa có GMV/đơn Trade Assurance.
- RFQ chưa được tận dụng hết dù còn 29 lượt có thể báo giá.
- Traffic và cơ hội kinh doanh còn thấp, trước đây tập trung nhiều tại Việt Nam.
- Cần sử dụng thanh toán trên Alibaba/Trade Assurance.

### Hành động tuần tới

1. Xử lý 501 sản phẩm gây hiểu nhầm và kiểm tra chất lượng listing.
2. Duy trì 5–10 sản phẩm hot mỗi ngày; ưu tiên abrasive/sandpaper có nhu cầu thật.
3. Dùng RFQ để tăng traffic mục tiêu; theo dõi 29 lượt RFQ còn lại.
4. Tăng buyer feedback lần hai để đạt mốc Service tiếp theo.
5. Đẩy 3 Top Product lên chất lượng cao hơn và tạo Super Product khi đủ điều kiện.
6. Dùng ảnh/video thật tại nhà máy hoặc người cầm sản phẩm; tránh ảnh ghép/chỉnh quá mức.
7. Theo dõi buyer lớn hằng tuần và tạo báo giá trong Alibaba.

## 4. Visitor Analyzer

### Tuần này: 16–22/08/2026

- Visitor records: **38**
- Quốc gia/vùng: **24**
- PV gian hàng: **70**
- Keyword chính xác: **75**
- Visitor có keyword: **27**
- Buyer L1+: **16**
- Level: **L0 = 22, L1 = 16, L2–L4 = 0**

### Tuần trước: 10–16/08/2026

- Visitor records: **49**
- Quốc gia/vùng: **31**
- PV gian hàng: **89**
- Keyword chính xác: **85**
- Visitor có keyword: **33**
- Buyer L1+: **20**
- Level: **L0 = 29, L1 = 20, L2–L4 = 0**

Traffic tuần này giảm so với tuần trước; L1+ giảm 20 → 16. Cần ưu tiên chất lượng lead thay vì chỉ tăng số visitor.

### Tín hiệu keyword

Nhóm phù hợp: sanding sponge/block, sandpaper, sanding cloth, sanding paper, spray gun, abrasive belt, polishing pad, Silicon Carbide waterproof sandpaper, jewelry saw blade, wood glue/furniture tools.

Nhóm cần xác minh hoặc lệch ngành: airsoft gun, car parts, watches, toys, clothing, kitchen products, electronics. Không coi mọi visitor là buyer abrasive.

Toàn bộ 24 quốc gia nằm trong `RIKEN_FULL_DATA.json` tại `visitors.countries`; toàn bộ 72 keyword duy nhất đã gộp theo số lần xuất hiện và PV nằm tại `visitors.keywords`.

### Quốc gia đáng chú ý

- Mexico: 3 visitor, 2 L1+, 11 PV.
- Philippines: 2 visitor, 2 L1+, 8 keyword records.
- Sri Lanka: 2 visitor, 2 L1+, 4 PV.
- Tanzania: 2 visitor, 2 L1+, 7 keyword records.
- Canada: 1 visitor, L1+, có 4 RFQ.
- Bulgaria: 1 visitor, L1+, có 25 RFQ.
- Dominican Republic: 1 visitor, L1+, 5 PV và 12 RFQ.
- Việt Nam: 5 visitor, 4 L1+ nhưng không có keyword; cần xác minh nhu cầu thực.

## 5. OneTalk — buyer ưu tiên

Tổng hợp mới: **7 lead được lọc**, trong đó **4 ưu tiên**, **3 cần theo dõi**. OneTalk ghi nhận 14 buyer có phản hồi trong 30 ngày; thời gian phản hồi trung bình 0,63 giờ.

### Ưu tiên cao

| Buyer | Nhu cầu | Blocker | Next action |
|---|---|---|---|
| Antonio Majano | Hỏi Riken là nhà sản xuất hay thương mại | Chưa biết năng lực factory | Xác nhận Riken là nhà máy/chuyên abrasive, nêu năng lực; hỏi product và qty |
| Ali Lali | 20 rolls sandpaper, grit 120/180 | Thiếu backing, coating, size, destination | Hỏi backing/coating, width/length, destination; báo giá 120/180 grit |
| Zephy Lubwela | 25 rolls P100 + 25 rolls P120, mỗi roll 50m | Thiếu company, application, destination, trial/regular | Lấy đủ company/application/address; gửi quote và freight |
| yael Ramirez — Dominican Republic | Abrasive sponge xanh 100×120×12mm, grit 60–400, medium, dùng car/wood | Thiếu destination, schedule, target price | Hỏi city/port, target price, company; gửi quote trong ngày |
| Victor Pedrozo — Mexico | Nhiều grit 320–3000, khoảng 500 pcs, MOQ 100/grit | Grit 80 không có; cần chia qty theo grit | Xác nhận mix grit, hỏi 500 pcs chia thế nào; báo giá chính thức |
| balaji Selvam — India | Aluminum Oxide Sandpaper thay Rhynowet, grit 80–800, RFQ ≥20.000 pcs, USD 0,20/pc | Thiếu xác nhận substitute, grit/size cụ thể và địa chỉ | Hỏi có chấp nhận Riken thay Rhynowet không, chốt grit/size/address, tính ship |

### Lead cần theo dõi

- michael tigano — US: Silicon Carbide waterproof sandpaper Riken C35P, 230×280mm, P60–P2000, 1.000 pcs, target USD 0,09; hỏi grit test và địa chỉ sample.
- Ruby N — corundum sanding paper rolls, 80–800 grit, xử lý aluminum; gửi hai phương án single sheet/roll và giá.
- Raymond lockett — spray gun 600mL, test 1 unit; báo express/economy shipping tới US.
- Javier Garcia — Aluminum Oxide Flap Disc 100mm, grit 40/60, 1.000 pcs; tách proposal thành quote ngắn, hỏi logo/packing/address sample.
- MauroCesar Andrade — RFQ Silicon Carbide waterproof sandpaper P60–P3000, OEM; follow bằng bảng grit/size/packing.
- Tee Poungkaew — đang kẹt ở phí vận chuyển; hỏi qty và kích thước kiện để báo DHL/FedEx.

### Rủi ro

- Không coi auto reception stopped, chào hỏi, refund/cancel order hoặc seller follow-up đơn thuần là lead nóng.
- Victor nói công ty sẽ phản hồi qua email: nên kéo trao đổi và báo giá về Alibaba.
- I RIN LEE đã có trao đổi email: tóm tắt lại báo giá trong Alibaba.
- Trước khi xin email/điện thoại, phải chốt product, grit, size, qty, packing và destination.

## 6. Cấu trúc app

### Tab 1 — Tổng quan / Vận hành

- Header: `Riken — Báo cáo tuần | 09–15/08/2026`
- KPI: 1 sao, 119 visitor, 4 inquiry, 5 RFQ, 16 L1+ visitor, 0 Super Product.
- Cảnh báo: 501 sản phẩm gây hiểu nhầm, thiếu 91 Marketing visitor, thiếu 1 Service feedback, chưa có TA GMV.
- Card 3 việc ngay: xử lý listing lỗi, báo giá Ali Lali/Zephy/yael, follow RFQ balaji/Victor.
- Biểu đồ xu hướng dùng toàn bộ `ops.history`.

### Tab 2 — Người xem / Visitor

- KPI: 38 visitor, 24 quốc gia, 70 PV, 27 có keyword, 16 L1+.
- Bảng quốc gia dùng toàn bộ `visitors.countries`, có visitor, PV, keyword visitor, exact keywords, L0–L4, L1+.
- Bảng keyword dùng toàn bộ `visitors.keywords`, có keyword nguyên bản, occurrences, PV, level và quốc gia.
- Nhãn nhóm: Abrasive/Sanding, Spray Gun/Tool, Furniture/DIY, Nhiễu.
- Funnel chỉ dùng số thật: visitor → có keyword → L1+; không tự tạo purchase conversion.

### Tab 3 — Buyer & tin nhắn

- KPI: lead ưu tiên, lead theo dõi, buyer có phản hồi thật.
- Badge: `Spec`, `Grit`, `MOQ`, `Freight`, `Sample`, `RFQ`, `Off-platform risk`.
- Mỗi card: buyer, product/qty, blocker, next action.
- Nút `Copy next action`, không gửi tự động.

### Tab 4 — Kết luận & action plan

- Kết luận: phản hồi nhanh và catalog tăng, nhưng rating/traffic chất lượng còn yếu; 501 listing gây hiểu nhầm là rủi ro lớn nhất; các lead abrasive có thông số rõ nên được chốt trước.
- Checklist 7 ngày: xử lý listing lỗi, báo RFQ, chốt grit/size/qty/freight, xin Service feedback, dùng Trade Assurance.

## 7. Data contract

Claude Code phải đọc file [RIKEN_FULL_DATA.json](RIKEN_FULL_DATA.json), không cần tổng hợp lại Google Sheets.

```js
const RIKEN_DATA = {
  meta: {account:'Riken Viet Nam Co Ltd', opsPeriod:'09–15/08/2026', visitorPeriod:'16–22/08/2026'},
  ops: {history: []},
  visitors: {currentSummary:{}, previousSummary:{}, countries:[], keywords:[]},
  leads: {overview:[], priority:[], followup:[], lowResponse:[]}
};
```

Quy tắc:

- Kỳ vận hành và kỳ visitor khác nhau; hiển thị ngày rõ trên từng tab.
- Không tự bịa GMV, doanh thu, đơn hàng hoặc conversion rate.
- Không coi mọi visitor là buyer abrasive; lọc theo level + keyword + PV + hành vi.
- Giữ trao đổi, báo giá và thanh toán trên Alibaba.
- Màu: đỏ = xử lý ngay, cam = theo dõi, xanh = tín hiệu tốt, xám = chưa đủ dữ liệu.
- App mở được offline, responsive, desktop-first 1440px và dữ liệu tách khỏi UI.
