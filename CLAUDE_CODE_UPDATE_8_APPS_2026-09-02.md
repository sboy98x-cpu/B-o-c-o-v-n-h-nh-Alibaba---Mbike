# BRIEF CHO CLAUDE CODE — CẬP NHẬT TUẦN MỚI CHO 8 APP ALIBABA

## Mục tiêu

Cập nhật dữ liệu tuần mới cho đúng 8 app hiện có trong thư mục `/Users/phantam/Documents/ChatGPT/Alibaba inservice`. Giữ nguyên thiết kế, cấu trúc điều hướng và các tương tác đang hoạt động; chỉ thay dữ liệu, tính lại so sánh và viết lại insight/hành động theo dữ liệu mới.

Kỳ Visitor Analyzer mới: **27.08–02.09.2026**. Kỳ so sánh: **16–22.08.2026**.

Không cần mở hoặc tổng hợp lại Google Sheets. Dữ liệu đầy đủ đã được đóng gói trong 8 file JSON dưới đây.

## Ánh xạ app và file dữ liệu

| Nhà | File app cần cập nhật | File dữ liệu tuần mới | Số tuần vận hành | Quốc gia | Từ khóa chính xác | Buyer ưu tiên | Buyer theo dõi |
|---|---|---|---:|---:|---:|---:|---:|
| Mbike | `index.html` | `MBIKE_WEEKLY_UPDATE_2026-09-02.json` | 21 | 155 | 2.924 | 51 | 46 |
| VCC | `viet-coldchain/index.html` | `VCC_WEEKLY_UPDATE_2026-09-02.json` | 15 | 24 | 68 | 13 | 16 |
| CM Decor | `cm-decor/index.html` | `CM_DECOR_WEEKLY_UPDATE_2026-09-02.json` | 15 | 15 | 28 | 12 | 10 |
| Hoàng Đức Thịnh | `hoang-duc-thinh/index.html` | `HOANG_DUC_THINH_WEEKLY_UPDATE_2026-09-02.json` | 13 | 60 | 275 | 18 | 19 |
| Viet Drip | `viet-drip/index.html` | `VIET_DRIP_WEEKLY_UPDATE_2026-09-02.json` | 10 | 29 | 93 | 11 | 17 |
| Vivika | `vivika/index.html` | `VIVIKA_WEEKLY_UPDATE_2026-09-02.json` | 7 | 91 | 669 | 20 | 20 |
| Riken | `riken/index.html` | `RIKEN_WEEKLY_UPDATE_2026-09-02.json` | 5 | 25 | 81 | 18 | 16 |
| G8 Home | `g8-home/index.html` | `G8_HOME_WEEKLY_UPDATE_2026-09-02.json` | 21 | 55 | 335 | 33 | 24 |

Tất cả đường dẫn trên đều tương đối với thư mục gốc dự án.

## Kiểm tra nhanh KPI Visitor tuần mới

| Nhà | Visitor mới / trước | PV mới / trước | L1+ mới / trước |
|---|---:|---:|---:|
| Mbike | 1.546 / 1.649 | 3.416 / 3.691 | 635 / 661 |
| VCC | 38 / 36 | 67 / 74 | 16 / 6 |
| CM Decor | 26 / 21 | 54 / 33 | 10 / 10 |
| Hoàng Đức Thịnh | 156 / 177 | 252 / 315 | 54 / 55 |
| Viet Drip | 47 / 45 | 257 / 108 | 28 / 22 |
| Vivika | 375 / 299 | 1.344 / 772 | 143 / 132 |
| Riken | 50 / 38 | 95 / 70 | 35 / 16 |
| G8 Home | 218 / 218 | 585 / 629 | 104 / 108 |

Các số này chỉ dùng để kiểm tra sau khi cập nhật. Mọi bảng chi tiết phải lấy trực tiếp từ JSON tương ứng.

## Công việc bắt buộc cho từng app

1. Cập nhật tiêu đề kỳ báo cáo và toàn bộ KPI tổng quan bằng kỳ 27.08–02.09, so sánh với 16–22.08.
2. Phần **Vận hành** phải dùng toàn bộ lịch sử trong JSON, không chỉ hai tuần gần nhất. Hiển thị đủ các chỉ số có trong từng tuần: sao, tổng sản phẩm, sản phẩm mới, visitor, inquiry, inquiry đã trả lời, RFQ đã báo, RFQ còn lại, thời gian phản hồi, phản hồi trong 24h, Super Product, Top Product và các ghi chú/hành động liên quan.
3. Vẽ lại biểu đồ xu hướng nhiều tuần từ toàn bộ `history`. Không cắt bớt tuần và không tự nội suy ô trống.
4. Phần **Người xem – Quốc gia** phải hiển thị toàn bộ quốc gia trong JSON, đủ visitor, PV, visitor có keyword, số bản ghi keyword, L0–L4 và L1+. Có tìm kiếm/sắp xếp; mặc định ưu tiên L1+ rồi đến PV.
5. Phần **Người xem – Từ khóa** phải hiển thị toàn bộ từ khóa chính xác, giữ nguyên chuỗi gốc, kèm số lần xuất hiện, tổng PV, level và quốc gia. Không dịch, không sửa chính tả và không chỉ hiển thị vài ví dụ.
6. Phần **Tin nhắn/OneTalk** phải cập nhật đủ tổng quan, buyer ưu tiên, buyer cần theo dõi và buyer ít phản hồi/spam. Mỗi buyer cần thể hiện tối thiểu: quốc gia, level, sản phẩm/nội dung hỏi, số lượng, tình trạng trao đổi, mức ưu tiên và đề xuất hành động tiếp theo nếu dữ liệu có cung cấp.
7. Tính lại khối **Insight cần chú ý** cho cả Mbike và VCC, đồng thời duy trì khối này ở sáu app còn lại. Insight phải ngắn, có số liệu và trả lời: điều gì thay đổi, vấn đề ở đâu, cơ hội nào đáng tập trung, hành động nào cần làm trước.
8. Viết lại phần **Tuần qua đã làm gì**, **Vấn đề gian hàng**, **Hành động tuần tới** và **Kết quả cần theo dõi** từ dữ liệu mới. Không giữ lại nhận định cũ nếu không còn đúng.

## Quy tắc tính insight

- So sánh visitor, PV, L1+ và tỷ lệ L1+/visitor giữa hai kỳ.
- Xếp quốc gia theo chất lượng buyer L1+ trước, không chỉ theo lượng visitor.
- Phân biệt từ khóa đúng ngành, cơ hội cần xác minh và từ khóa lệch ngành/nhiễu; mọi kết luận phải truy ngược được về danh sách từ khóa trong JSON.
- Ưu tiên buyer theo khả năng chốt đơn, độ rõ của nhu cầu, số lượng, trạng thái báo giá/thanh toán và blocker đang tồn tại.
- Hành động phải cụ thể: buyer nào cần follow, vấn đề gì cần xử lý, nội dung cần gửi, thời hạn hoặc thứ tự ưu tiên.
- Với dữ liệu thiếu/null, hiển thị **Chưa có dữ liệu**; tuyệt đối không tự bịa số.

## Ngôn ngữ và phạm vi

- Riken: giữ giao diện song ngữ **Việt / 中文**, bao gồm tiêu đề mới và insight mới.
- G8 Home: chỉ dùng tiếng Việt.
- Sáu app còn lại: giữ đúng ngôn ngữ hiện có của từng app.
- Không trộn dữ liệu giữa các nhà. Cập nhật tuần tự từng app theo đúng file JSON ánh xạ.
- Không thay đổi nhận diện thương hiệu, màu sắc hoặc bố cục tổng thể nếu không cần thiết.
- App phải tiếp tục mở trực tiếp bằng `file://`; không thêm phụ thuộc server hoặc API bắt buộc.

## Lưu ý về cấu trúc JSON

- Sáu file CM Decor, Hoàng Đức Thịnh, Viet Drip, Vivika, Riken và G8 Home dùng các nhóm chính: `operations`, `visitor`, `onetalk`.
- Hai file Mbike và VCC dùng tên nhóm tương đương: `ops`, `visitors`, `leads`.
- Ánh xạ: `ops.history` = `operations.history`; `visitors.countries` = `visitor.current_countries`; `visitors.keywords` = `visitor.current_exact_keywords`; `leads.priority` = `onetalk.priority_buyers`; `leads.followup` = `onetalk.followup_buyers`; `leads.lowResponse` = `onetalk.low_response_or_spam`.

## Kiểm thử bắt buộc

Sau mỗi app:

1. Mở file HTML bằng `file://` và kiểm tra không có lỗi console.
2. Kiểm tra đúng kỳ 27.08–02.09 và kỳ so sánh 16–22.08.
3. Đối chiếu 3 KPI kiểm tra nhanh ở bảng trên.
4. Kiểm tra số dòng quốc gia và số từ khóa khớp bảng ánh xạ.
5. Kiểm tra tìm kiếm, bộ lọc, tab, nút chuyển trang và biểu đồ.
6. Kiểm tra desktop và mobile; bảng dài không được phá layout.
7. Kiểm tra Riken vẫn song ngữ và G8 Home không xuất hiện tiếng Trung.

## Kết quả Claude Code cần trả về

Trả về bảng trạng thái 8 app gồm: app đã sửa, file đã sửa, kỳ dữ liệu, số tuần/quốc gia/từ khóa đã nạp, insight chính, kết quả kiểm thử và lỗi còn lại nếu có. Không chỉ nói “đã cập nhật”; phải nêu số liệu đối chiếu cho từng app.
