# Thiết kế giao diện landing page — Tiệm bánh handmade Ngọt

> Mã việc: TEC-37 · Epic: TEC-36 (Sprint 1 — Landing page tiệm bánh handmade Ngọt)
> Nguồn: yêu cầu web MSR-6 (TEC-35) · Repo: Muse-Soft/m-software-banh-ngot
> Đối tượng dựng: Dev TEC-38 — dựng đúng file này, không tự đổi bảng màu, kiểu chữ hay thứ tự các mục
> mà không hỏi lại Designer/PO.

## 1. Tổng quan

- Tiệm bánh handmade "Ngọt", quận 3, TP.HCM. Tông pastel ấm, dễ thương, cảm giác "bánh mới ra lò".
- **Mobile-first (thiết kế cho điện thoại trước, rồi mới mở rộng ra màn hình lớn):**
  trang phải đẹp và dùng được ngay trên điện thoại, không cần phóng to/thu nhỏ.
- Một trang duy nhất, cuộn dọc từ trên xuống dưới, đúng thứ tự các mục ở phần 3.
- Ngôn ngữ: tiếng Việt, giọng thân mật, ngắn gọn.

## 2. Bảng màu pastel ấm (dùng đúng mã màu, không tự pha thêm)

| Vai trò | Màu | Mã HEX | Ghi chú |
|---|---|---|---|
| Nền chính | Kem sữa | `#FFF8F0` | Nền toàn trang |
| Nền phụ (xen kẽ các mục) | Hồng phấn nhạt | `#FDECEA` | Dùng cho mục 3.2 và 3.5 |
| Màu chủ đạo / nút chính | Hồng dâu | `#F4A7B3` | Nút "Đặt bánh", tiêu đề mục |
| Màu nhấn phụ | Cam đào | `#FBC99B` | Giá, huy hiệu, viền thẻ nổi bật |
| Màu chữ chính | Nâu socola | `#5C3D2E` | Tiêu đề, nội dung chính |
| Màu chữ phụ | Nâu nhạt | `#9A7B6B` | Mô tả nhỏ, ghi chú |
| Viền / đường chia | Hồng rất nhạt | `#F3D9D2` | Viền thẻ, đường kẻ giữa các mục |
| Nút phụ (Zalo) | Xanh Zalo | `#0068FF` | Chỉ dùng cho nút chat Zalo, không dùng chỗ khác |

Quy tắc màu:

- Nền luôn sáng (kem/hồng phấn nhạt); chữ luôn nâu socola — không dùng nền tối, không dùng chữ đen tuyền.
- Mỗi mục chỉ có tối đa 1 nút màu hồng dâu (nút chính); các nút còn lại dùng viền hồng nhạt, nền trắng.
- Giá luôn màu cam đào, in đậm, cỡ chữ lớn hơn mô tả sản phẩm.

## 3. Kiểu chữ (dễ thương, nhất quán toàn trang)

- Tiêu đề lớn (tên tiệm, tiêu đề mục): font chữ tròn, mềm, có chân bo tròn — gợi ý:
  **"Be Vietnam Pro" Bold** (ưu tiên, vì hỗ trợ tốt tiếng Việt) hoặc **"Quicksand" Bold**.
  Nếu trình duyệt không tải được font trên, dùng font dự phòng: `system-ui, sans-serif`.
- Nội dung thường, mô tả, form: **"Be Vietnam Pro" Regular** (hoặc `system-ui, sans-serif`).
- Cỡ chữ trên điện thoại (mobile-first):
  - Tên tiệm (hero): 32px, in đậm.
  - Tiêu đề mục: 22px, in đậm.
  - Tên sản phẩm: 17px, in đậm.
  - Nội dung thường: 15px; mô tả nhỏ/ghi chú: 13px, màu nâu nhạt.
- Tiêu đề luôn căn giữa; nội dung thường căn trái. Không dùng chữ in hoa toàn bộ
  (trừ tên tiệm "NGỌT" ở hero).

## 4. Bố cục từng mục (theo đúng thứ tự từ trên xuống dưới)

### 4.1. Mục 1 — Mở đầu (Hero)

- Ảnh lớn: một chiếc bánh kem trang trí dâu tươi, chụp góc nghiêng, nền sáng, bo góc 20px,
  chiếm gần hết chiều rộng màn hình điện thoại (tỉ lệ ảnh khoảng 4:3).
- Trên/đưới ảnh: tên tiệm **"NGỌT"** (32px, hồng dâu, in đậm) + khẩu hiệu:
  > "Bánh nhà làm — ngọt vừa đủ, thương vừa đủ."
- Dưới khẩu hiệu: 1 nút chính màu hồng dâu: **"Đặt bánh sinh nhật"** (cuộn xuống form ở mục 4.3).
- Dưới nút: 1 dòng nhỏ màu nâu nhạt: "Quận 3, TP.HCM · Mở cửa 7:00–21:00 hằng ngày".

### 4.2. Mục 2 — Danh mục sản phẩm (kèm giá tham khảo)

- Tiêu đề mục: "Bánh nhà Ngọt làm".
- 3 nhóm, mỗi nhóm là 1 thẻ riêng (nền trắng, bo góc 16px, viền hồng rất nhạt):
  1. **Bánh kem sinh nhật** — từ 250.000đ (size 16cm, xem chi tiết giá ở form đặt bánh).
     Gợi ý hương vị: socola, dâu, trà xanh, vani.
  2. **Bánh mì** — từ 25.000đ/chiếc. Gợi ý: bánh mì bơ sữa, bánh mì phô mai chảy,
     bánh mì hoa cúc.
  3. **Bánh quy** — từ 60.000đ/hộp. Gợi ý: bánh quy bơ, bánh quy socola chip,
     bánh quy yến mạch.
- Mỗi thẻ gồm: ảnh sản phẩm (vuông, bo góc 12px) + tên nhóm + 2–3 món ví dụ + giá "từ ...".
- Ghi chú cuối mục (13px, nâu nhạt): "Giá tham khảo — giá chính xác theo size và hương vị
  khi đặt bánh. Bánh làm theo đơn trong ngày, không làm sẵn số lượng lớn."

### 4.3. Mục 3 — Form "Đặt bánh sinh nhật"

- Tiêu đề mục: "Đặt bánh sinh nhật".
- Form gồm đúng các trường sau (mỗi trường 1 hàng riêng trên điện thoại, nhãn nằm trên ô nhập):
  1. Họ tên người đặt (ô nhập chữ, bắt buộc).
  2. Số điện thoại (ô nhập số, bắt buộc).
  3. Kích thước bánh (chọn 1 trong: 16cm — 4–6 người; 20cm — 8–10 người;
     24cm — 12–15 người).
  4. Hương vị (chọn 1 trong: socola, dâu, trà xanh, vani).
  5. Ngày nhận bánh (chọn ngày; ghi chú dưới ô: "Vui lòng đặt trước ít nhất 1 ngày").
  6. Ghi chú thêm (ô nhập chữ, không bắt buộc — ví dụ: viết chữ lên bánh, dị ứng).
- Nút gửi form: màu hồng dâu, chữ "Gửi đơn đặt bánh".
- Sau khi gửi: hiện dòng xác nhận "Cảm ơn bạn! Ngọt sẽ gọi điện xác nhận đơn trong
  giờ mở cửa." (v1 chưa cần lưu đơn vào hệ thống — chỉ cần form hiển thị đúng và
  báo xác nhận; việc xử lý đơn thật do PO quyết định ở sprint sau).

### 4.4. Mục 4 — Thông tin giao hàng nội thành

- Tiêu đề mục: "Giao hàng nội thành".
- Nội dung (dạng 3 gạch đầu dòng, có biểu tượng xe/bánh):
  - Giao trong nội thành TP.HCM, ưu tiên quận 3 và các quận lân cận.
  - Phí giao hàng tính theo khoảng cách — báo phí khi xác nhận đơn qua điện thoại.
  - Bánh kem giao bằng hộp giữ lạnh, giữ nguyên dáng bánh; khách nên nhận bánh
    trong khung giờ đã hẹn.
- Ghi chú (13px, nâu nhạt): "Khách cũng có thể đến lấy trực tiếp tại tiệm trong giờ mở cửa."

### 4.5. Mục 5 — Liên hệ (chân trang)

- Tiêu đề mục: "Ghé Ngọt chơi nhé".
- Thông tin hiển thị, theo đúng thứ tự:
  1. Địa chỉ: Quận 3, TP.HCM.
     > ⚠️ Địa chỉ số nhà + tên đường cụ thể: **chưa có trong yêu cầu MSR-6** — Dev giữ
     > chỗ trống dạng "[Địa chỉ cụ thể — PO bổ sung]" và KHÔNG tự bịa địa chỉ.
  2. Giờ mở cửa: **7:00–21:00 hằng ngày**.
  3. Nút gọi điện: nút viền hồng nhạt, chữ "📞 Gọi cho Ngọt"
     (số điện thoại: **[PO bổ sung]** — Dev gắn số thật khi PO cung cấp, không tự bịa số).
  4. Nút chat Zalo: nút xanh Zalo, chữ "💬 Chat Zalo"
     (link Zalo: **[PO bổ sung]** — tương tự, không tự bịa link).
- Dòng cuối trang (13px, nâu nhạt, căn giữa): "Ngọt — Bánh nhà làm, quận 3, TP.HCM."

## 5. Quy tắc mobile-first (bắt buộc khi dựng)

- **Điện thoại (dưới 768px — mặc định):** mọi mục xếp dọc 1 cột; ảnh rộng gần hết màn hình;
  nút bấm cao tối thiểu 44px, dễ bấm bằng ngón tay; form mỗi trường 1 hàng; lề hai bên 16px.
- **Máy tính bảng / máy tính (từ 768px trở lên):** nội dung chính giới hạn chiều rộng tối đa
  720px, căn giữa; danh mục sản phẩm xếp 3 thẻ thành 1 hàng; hero xếp ảnh bên trái,
  tên tiệm + khẩu hiệu + nút bên phải.
- Không có thành phần nào tràn ngang màn hình điện thoại; không bắt người dùng cuộn ngang.
- Ảnh dùng định dạng webp/jpg nén nhẹ để tải nhanh trên mạng điện thoại.
- Tương phản chữ/nền: chữ nâu socola trên nền kem/hồng phấn nhạt — phải đọc rõ dưới nắng.

## 6. Đối chiếu Acceptance Criteria (TEC-37)

| Tiêu chí | Đáp ứng ở |
|---|---|
| Mở đầu: hình bánh + khẩu hiệu | Mục 4.1 |
| Danh mục: bánh kem sinh nhật, bánh mì, bánh quy + giá tham khảo | Mục 4.2 |
| Form "Đặt bánh sinh nhật": kích thước, hương vị, ngày nhận | Mục 4.3 |
| Thông tin giao hàng nội thành | Mục 4.4 |
| Liên hệ: địa chỉ, giờ 7:00–21:00, nút gọi điện và chat Zalo | Mục 4.5 |
| Bảng màu pastel ấm + kiểu chữ dễ thương, nhất quán | Mục 2, 3 |
| Mobile-first, hiển thị tốt trên điện thoại | Mục 5 |

Lưu ý cho Dev: số điện thoại, link Zalo và địa chỉ cụ thể chưa có trong yêu cầu gốc
(MSR-6 chỉ ghi "quận 3, TP.HCM") — giữ placeholder "[PO bổ sung]", không tự bịa.
