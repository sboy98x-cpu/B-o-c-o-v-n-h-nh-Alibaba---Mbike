# Prompt cho Claude Code — Bổ sung “Insight cần chú ý” cho VCC và Mbike

Hãy sửa trực tiếp hai app hiện có trong workspace:

- VCC: `/Users/phantam/Documents/ChatGPT/Alibaba inservice/viet-coldchain/index.html`
- Mbike: `/Users/phantam/Documents/ChatGPT/Alibaba inservice/index.html`

Không sửa các app CM Decor, Hoàng Đức Thịnh, Viet Drip, Vivika, Riken hoặc G8 Home.

## 1. Yêu cầu chung

Thêm một block nổi bật tên:

`Insight cần chú ý`

Tiếng Anh nếu app có chế độ English:

`Key insights`

Block phải nằm ngay sau phần KPI/summary đầu tiên, trước bảng chi tiết hoặc trước phần action plan. Mục đích là giúp người dùng hiểu ngay yếu tố nào quan trọng, không phải tự đọc toàn bộ bảng.

Thiết kế:

- Card nền vàng nhạt hoặc xanh nhạt, có icon `💡` hoặc biểu tượng insight.
- Mỗi insight là một dòng ngắn, có nhãn mức độ: `Cần chú ý`, `Cơ hội`, `Đang tốt`.
- Tối đa 5 insight trên màn hình chính.
- Có thể bấm `Xem chi tiết` để mở bảng/section liên quan.
- Không lặp lại nguyên văn toàn bộ action plan.
- Không tạo số liệu mới; chỉ dùng dữ liệu đang có trong object dữ liệu của app.
- Nếu kỳ Visitor và kỳ Vận hành khác nhau, ghi rõ kỳ trong insight.

## 2. Nội dung cho app VCC

Đọc object dữ liệu hiện có của VCC và hiển thị các insight sau nếu số liệu tương ứng tồn tại:

### Insight 1 — Traffic chất lượng giảm

`Cần chú ý — Visitor tăng nhẹ nhưng PV giảm và buyer L1+ giảm mạnh so với tuần trước. Cần ưu tiên chất lượng traffic thay vì chỉ tăng số visitor.`

Dữ liệu tham chiếu:

- Visitor: 36 so với 32.
- PV: 74 so với 103.
- Buyer L1+: 6 so với 13.

### Insight 2 — Traffic đang lệch thị trường

`Cần chú ý — Traffic đang tập trung nhiều ở Việt Nam và Trung Quốc, trong khi nhóm Mỹ/EU còn thấp. Cần mở rộng traffic đúng thị trường cold-chain.`

Dữ liệu tham chiếu:

- Việt Nam: 11 visitor, 24 PV, 2 L1+.
- Trung Quốc: 8 visitor, 20 PV, 0 L1+.
- Hoa Kỳ: 6 visitor, 12 PV, 2 L1+.

### Insight 3 — Cơ hội buyer thật

`Cơ hội — Mary Jane Zamora, Keneth Adesulu, Alviaa Alviaa và Kirti Jain Kothari là nhóm cần follow trước vì đã có nhu cầu về sample, MOQ container, IQF/frozen fruits hoặc giá thị trường.`

### Insight 4 — Blocker chốt đơn

`Cần chú ý — Các blocker chính là phí ship sample, MOQ container, giá cạnh tranh tại India và yêu cầu trao đổi ngoài Alibaba.`

### Insight 5 — Điểm vận hành

`Đang tốt — Inquiry đã được trả lời đầy đủ và tỷ lệ phản hồi trong 24h đang trên 93%, nhưng cần cải thiện Marketing/traffic và tạo đơn Trade Assurance.`

## 3. Nội dung cho app Mbike

Đọc đúng số liệu hiện có trong object dữ liệu Mbike. Không lấy số liệu VCC để dùng cho Mbike.

Hiển thị các insight theo logic sau:

### Insight 1 — Gian hàng đang có nền tảng tốt

Nếu `stars >= 5` hoặc rating hiện tại ở mức cao:

`Đang tốt — Gian hàng đang duy trì rating cao và có nền tảng sản phẩm lớn. Trọng tâm tiếp theo là chuyển traffic thành inquiry và đơn Trade Assurance.`

### Insight 2 — Traffic và inquiry

Nếu visitor tuần này tăng nhưng inquiry không tăng tương ứng:

`Cần chú ý — Traffic đang có nhưng tỷ lệ chuyển thành inquiry chưa tương xứng. Cần tối ưu ảnh chính, title, keyword, giá, MOQ và CTA trên các sản phẩm có PV cao.`

Nếu inquiry giảm so với tuần trước:

`Cần chú ý — Inquiry đang giảm so với tuần trước. Ưu tiên kiểm tra các sản phẩm có lượt xem cao nhưng chưa tạo hỏi hàng.`

### Insight 3 — Quốc gia và buyer quality

Tự lấy từ bảng country:

`Cơ hội — Ưu tiên các quốc gia có L1+ cao và keyword đúng ngành motorcycle accessories; không chỉ ưu tiên quốc gia có nhiều visitor L0.`

Hiển thị thêm 2–3 quốc gia dẫn đầu theo `L1+` hoặc `PV`.

### Insight 4 — Keyword

Tự lọc các keyword phù hợp nhóm motorcycle accessories, ví dụ:

- motorcycle accessories
- crash bar
- luggage rack
- motorcycle top box
- motorcycle light/headlight
- motorcycle phone holder
- model cụ thể như CB, Yamaha, Honda, KTM, BMW, Ducati

Nhãn hiển thị:

`Cơ hội — Keyword đang cho thấy buyer tìm đúng nhóm phụ kiện xe máy và một số model cụ thể. Nên tạo/đẩy sản phẩm theo model có nhu cầu rõ.`

### Insight 5 — Buyer cần chốt

Tự lấy buyer priority từ object dữ liệu:

`Cần làm ngay — Ưu tiên buyer đã có product, quantity, model, địa chỉ hoặc câu hỏi về shipping. Next action phải cụ thể: gửi spec, báo giá, phí ship và link Trade Assurance.`

## 4. Quy tắc hiển thị động

Tạo hàm dùng chung, ví dụ:

```js
function renderInsights(insights) {
  return insights.slice(0, 5).map(item => `
    <div class="insight-card ${item.type}">
      <span class="insight-badge">${item.label}</span>
      <span class="insight-text">${item.text}</span>
    </div>
  `).join('');
}
```

Không hard-code số liệu trong UI nếu số liệu đã có trong `D`, `VCC_DATA` hoặc object tương ứng. Có thể dùng nội dung insight cố định nhưng số phải lấy động.

## 5. Kiểm tra hoàn thành

Sau khi sửa:

1. Mở được cả hai file bằng `file://`.
2. VCC có block “Insight cần chú ý” ngay dưới KPI đầu trang.
3. Mbike có block “Insight cần chú ý” ngay dưới KPI đầu trang.
4. Nội dung VCC và Mbike không bị dùng nhầm dữ liệu của nhau.
5. Không có lỗi console.
6. Responsive trên màn hình desktop và mobile.
7. Các tab/bảng/chart hiện tại vẫn hoạt động bình thường.
