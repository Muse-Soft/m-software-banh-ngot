# Ngọt — Landing page tiệm bánh handmade

Landing page một trang cho tiệm bánh handmade **Ngọt**, quận 3, TP.HCM.
Tông pastel ấm, mobile-first, tiếng Việt, giọng thân mật.

## Sản phẩm

- Bánh kem sinh nhật, bánh mì, bánh quy — làm theo đơn trong ngày.
- Mở cửa 7:00–21:00 hằng ngày.
- Trang gồm: giới thiệu tiệm, thực đơn bánh, lý do chọn Ngọt, đặt bánh (Zalo),
  địa chỉ và giờ mở cửa.
- Thiết kế theo `DESIGN.md` (TEC-37), dựng bằng `index.html` tĩnh (TEC-38).

## Link demo

- Demo công khai: https://m-software-banh-ngot.genalpha.dev
- Bản Pages mặc định: https://m-software-banh-ngot.pages.dev

## Cách chạy local

Không cần build, không cần cài đặt gì thêm:

```bash
# Cách 1: mở trực tiếp file
# Mở index.html bằng trình duyệt.

# Cách 2: chạy server tĩnh (khuyên dùng, để font và đường dẫn hoạt động đúng)
python3 -m http.server 8000
# rồi mở http://localhost:8000
```

## Nguồn yêu cầu

- Yêu cầu web MSR-6: https://github.com/Muse-Soft/m-software-requests/issues/6
- Linear: TEC-35 (yêu cầu) → TEC-36 (Epic Sprint 1) → TEC-40 (deploy + README này).
- Repo: https://github.com/Muse-Soft/m-software-banh-ngot
