# Prompt triển khai cho Claude Code — Riken Trung–Việt

Bạn đang làm việc trong workspace:

`/Users/phantam/Documents/ChatGPT/Alibaba inservice`

Hãy sửa hoặc tạo app Riken theo yêu cầu dưới đây.

## 1. Xác định file app

1. Tìm file hiện tại theo thứ tự:
   - `/Users/phantam/Documents/ChatGPT/Alibaba inservice/riken/index.html`
   - các thư mục app hiện có trong workspace nếu Riken đang dùng template khác.
2. Nếu chưa có app Riken, tạo:

`/Users/phantam/Documents/ChatGPT/Alibaba inservice/riken/index.html`

3. Không sửa các app CM Decor, Hoàng Đức Thịnh, Viet Drip, Vivika hoặc Mbike.

## 2. Dữ liệu nguồn đã chuẩn hóa

Đọc file:

`/Users/phantam/Documents/ChatGPT/Alibaba inservice/RIKEN_FULL_DATA.json`

Đọc brief để hiểu ngữ cảnh kinh doanh:

`/Users/phantam/Documents/ChatGPT/Alibaba inservice/RIKEN_CLAUDE_CODE_BRIEF.md`

Không cần mở lại Google Sheets. Không tự tổng hợp lại dữ liệu.

File JSON đã có:

- `ops.history`: toàn bộ lịch sử vận hành và 13 chỉ số mỗi tuần.
- `visitors.currentSummary`, `visitors.previousSummary`.
- `visitors.countries`: toàn bộ quốc gia trong tuần hiện tại.
- `visitors.keywords`: toàn bộ keyword chính xác, số lần xuất hiện, PV, level và quốc gia.
- `leads.priority`, `leads.followup`, `leads.lowResponse`: dữ liệu OneTalk.

Nếu app mở bằng `file://` và trình duyệt không cho phép `fetch()` JSON, hãy nhúng dữ liệu JSON vào app hoặc tạo cơ chế fallback rõ ràng. App phải mở được bằng cách double-click `index.html`.

## 3. Chức năng song ngữ Trung–Việt

Thêm language switcher ở góc phải header:

- `VI Tiếng Việt`
- `中文 中文`

Yêu cầu:

- Mặc định: tiếng Việt.
- Khi chọn 中文, dịch toàn bộ label giao diện, tiêu đề section, tab, KPI, trạng thái, nút, chú giải và action plan sang tiếng Trung giản thể.
- Không dịch sai tên buyer, tên sản phẩm, keyword gốc, số liệu hoặc tên thương hiệu Riken.
- Keyword phải giữ nguyên văn bản gốc; có thể thêm nhãn nhóm song ngữ.
- Nội dung OneTalk Việt–Trung có thể hiển thị song song hoặc dùng bản tiếng Việt khi chọn VI và bản tiếng Trung khi chọn 中文.
- Lưu ngôn ngữ đã chọn vào `localStorage` với key `riken_lang`.
- Tất cả text giao diện phải đi qua object dịch, ví dụ `t('dashboard.title')`, không hard-code rải rác.

## 4. Cấu trúc giao diện

Tạo dashboard desktop-first, responsive, phù hợp chụp màn hình báo cáo.

### Header

- Tên: `Riken Việt Nam — Báo cáo tuần`
- Tiếng Trung: `Riken 越南 — 周报`
- Kỳ vận hành: `09–15/08/2026`
- Kỳ visitor: `16–22/08/2026`
- Badge: `Abrasive Materials / 研磨材料`
- Badge nguồn: `Vận hành · Visitor · OneTalk / 运营 · 访客 · OneTalk`

### Tab 1 — Tổng quan / 总览

Hiển thị các KPI:

- Số sao: `1`
- Tổng sản phẩm: `2.340`
- Visitor vận hành: `119`
- Inquiry: `4`
- RFQ đã báo giá: `5`
- RFQ còn lại: `29`
- Phản hồi trong 24h: `100%`
- Top Product: `3`
- Super Product: `0`

Hiển thị cảnh báo nổi bật:

- `501 sản phẩm gây hiểu nhầm / 501个误导性产品`
- `Thiếu 91 Marketing visitor / 距离营销下一档还差91位访客`
- `Thiếu 1 Service feedback / 距离服务下一档还差1位买家回复`
- `Chưa có GMV Trade Assurance / 尚无信保交易GMV`

Thêm biểu đồ xu hướng dùng toàn bộ `ops.history`, không chỉ tuần này:

- Số sao.
- Tổng sản phẩm.
- Sản phẩm mới.
- Visitor.
- Inquiry.
- RFQ đã báo giá.
- Phản hồi trong 24h.
- Top Product/Super Product.

### Tab 2 — Người xem / 访客

KPI tuần hiện tại:

- `38` visitor records.
- `24` quốc gia/vùng.
- `70` PV.
- `75` keyword records.
- `27` visitor có keyword.
- `16` buyer L1+.

Hiển thị:

1. Bảng toàn bộ `visitors.countries`, gồm:
   - Quốc gia.
   - Visitor.
   - PV.
   - Visitor có keyword.
   - Keyword records.
   - L0, L1, L2, L3, L4, L1+.
2. Bảng toàn bộ `visitors.keywords`, gồm:
   - Keyword chính xác giữ nguyên.
   - Số lần xuất hiện.
   - PV.
   - Level.
   - Quốc gia.
3. Bộ lọc theo country, level, keyword và PV.
4. Nhóm keyword:
   - Abrasive/Sanding / 研磨与砂纸.
   - Spray Gun/Tool / 喷枪与工具.
   - Furniture/DIY / 家具与DIY.
   - Nhiễu / 非相关.

Không coi mọi visitor là buyer abrasive. Ưu tiên L1+, keyword phù hợp và PV cao.

### Tab 3 — Buyer & tin nhắn / 买家与消息

Hiển thị các nhóm:

- Ưu tiên cao / 高优先级.
- Cần theo dõi / 继续跟进.
- Ít phản hồi hoặc rủi ro / 低优先级或风险.

Mỗi buyer card chỉ cần:

- Tên buyer.
- Quốc gia.
- Sản phẩm.
- Quantity.
- Blocker.
- Next action.
- Badge: `Spec`, `Grit`, `MOQ`, `Freight`, `Sample`, `RFQ`, `Off-platform risk`.

Buyer cần đặt ở đầu danh sách:

1. Antonio Majano — hỏi Riken là nhà sản xuất hay thương mại.
2. Ali Lali — 20 rolls sandpaper, grit 120/180.
3. Zephy Lubwela — P100/P120, 50 rolls, mỗi roll 50m.
4. yael Ramirez — abrasive sponge 1000 pcs, 100×120×12mm, grit 60–400.
5. Victor Pedrozo — khoảng 500 pcs, nhiều grit, MOQ 100/grit.
6. balaji Selvam — RFQ ≥20.000 pcs, Riken thay Rhynowet.

Nút `Copy next action / 复制下一步` chỉ copy nội dung, không gửi tin tự động.

### Tab 4 — Kết luận & hành động / 结论与行动

Hiển thị kết luận:

> Riken có tốc độ phản hồi tốt và catalog lớn, nhưng rating/traffic chất lượng còn yếu. 501 listing gây hiểu nhầm là rủi ro lớn nhất. Các buyer hỏi rõ grit, size, quantity và freight cần được chốt trước.

Checklist 7 ngày:

1. Xử lý 501 listing gây hiểu nhầm.
2. Báo giá Ali Lali, Zephy, yael, Victor và balaji.
3. Khai thác 29 RFQ còn lại.
4. Xin thêm 1 Service feedback.
5. Đẩy 3 Top Product và chuẩn bị Super Product.
6. Tạo đơn Trade Assurance.
7. Bổ sung ảnh/video thực tế tại nhà máy.

## 5. Quy tắc kỹ thuật

- Giữ app offline-openable.
- Không dùng backend.
- Không làm mất dữ liệu gốc.
- Không bịa GMV, doanh thu, đơn hàng hoặc conversion rate.
- Không sửa dữ liệu nguồn Google Sheets.
- Không gửi email, WhatsApp hoặc tin nhắn tự động.
- Giữ báo giá và thanh toán trên Alibaba.
- Dùng màu: đỏ = xử lý ngay, cam = theo dõi, xanh = tín hiệu tốt, xám = thiếu dữ liệu.
- Kiểm tra console không có lỗi.
- Kiểm tra nút đổi VI/中文 trên tất cả 4 tab.
- Kiểm tra bảng quốc gia và keyword có đủ toàn bộ dữ liệu, không chỉ dữ liệu mẫu.

## 6. Kết quả cần trả về

Sau khi sửa xong, báo cáo:

1. Đã sửa/tạo file nào.
2. Đã thêm nút chuyển ngôn ngữ ở đâu.
3. Đã nạp `RIKEN_FULL_DATA.json` như thế nào.
4. Đã kiểm tra đủ 4 tab và bảng dữ liệu chưa.
