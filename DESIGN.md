# DESIGN.md — Landing page Gió Đồng

- Sản phẩm: landing page 1 trang cho hãng xe đạp thủ công Gió Đồng.
- Nguồn: yêu cầu MSR-33 (TEC-252), Epic TEC-253, task thiết kế TEC-254.
- Repo: https://github.com/Muse-Soft/m-software-gio-dong
- Nguyên tắc: mọi quyết định thẩm mỹ dưới đây đều kèm thông số cụ thể (mã màu, tên font, cỡ chữ, tỉ lệ khung). Không dùng mô tả chung chung kiểu "đẹp, hiện đại" mà không có thông số.

## 1. Bảng màu (mã hex + vai trò từng màu)

| Mã hex | Tên gọi | Vai trò |
|---|---|---|
| `#F3EFE7` | Giấy kem | Nền chính toàn trang — nền giấy ấm, sáng, gợi giấy báo cũ và xưởng thủ công. |
| `#E9E2D4` | Kem đậm | Nền khối phụ (khối Xưởng, khối Đặt đóng riêng) và nền thẻ, tạo nhịp xen kẽ với nền chính. |
| `#FFFFFF` | Trắng giấy | Nền thẻ sản phẩm và form liên hệ, nổi trên nền kem. |
| `#1E2A24` | Xanh than | Chữ chính: tiêu đề, nội dung, giá. Độ tương phản cao trên nền kem, đọc rõ cả ngoài nắng. |
| `#5C6B62` | Xanh rêu xám | Chữ phụ: mô tả ngắn, chú thích ảnh, nhãn nhỏ. Không dùng cho chữ chính. |
| `#C75B21` | Cam đất nung | Màu nhấn duy nhất cho hành động: nút CTA ("Đặt lịch tư vấn", "Xem dòng xe"), giá nổi bật, gạch chân tiêu đề khối. |
| `#9C4418` | Đất nung đậm | Trạng thái hover/active của nút cam đất nung. Không dùng làm màu nền lớn. |
| `#D8A24A` | Vàng mật | Điểm nhấn phụ, dùng tiết chế: đường kẻ trang trí, tag "Thủ công", viền ảnh chọn. Không dùng cho nút chính. |

Quy tắc dùng màu:
- Một màn hình chỉ có tối đa 1 nút cam `#C75B21`; các nút phụ dùng viền xanh than, nền trong suốt.
- Không dùng màu ngoài bảng này cho văn bản, nút và nền. Ảnh là ngoại lệ duy nhất (xem mục 4).
- Tỉ lệ diện tích màu trên một khối: nền kem/trắng ~80%, chữ xanh than ~15%, cam đất nung + vàng mật ~5%.

## 2. Font chữ

- Font tiêu đề: **Playfair Display** (serif, chân chữ cổ điển) — tiêu đề hero, tiêu đề từng khối, tên dòng xe.
- Font nội dung: **Be Vietnam Pro** (sans-serif, hỗ trợ tốt tiếng Việt) — mô tả, giá, nhãn, nút, form.
- Không dùng font thứ ba.

Cỡ chữ (desktop / mobile):
- Hero H1: 56px / 40px, Playfair Display, đậm vừa (600), dòng cách 1,15.
- Tiêu đề khối H2: 40px / 30px, Playfair Display, 600, dòng cách 1,2.
- Tiêu đề thẻ H3 (tên dòng xe, bước đặt xe): 26px / 22px, Playfair Display, 600.
- Nội dung chính: 17px / 16px, Be Vietnam Pro, 400, dòng cách 1,7.
- Chữ phụ / chú thích ảnh: 14px, Be Vietnam Pro, 400, màu `#5C6B62`.
- Nút CTA: 16px, Be Vietnam Pro, 700, chữ hoa toàn bộ, bo tròn 999px, đệm 14px dọc × 28px ngang.
- Nhãn nhỏ trên tiêu đề khối (eyebrow): 13px, Be Vietnam Pro, 700, chữ hoa, giãn cách chữ 2px, màu `#C75B21`.

## 3. Phong cách tham chiếu (MỘT phong cách duy nhất)

**Editorial xe đạp cổ điển châu Âu** — phong cách của tạp chí xe đạp in giấy: ảnh lớn chiếm trọn bề ngang như ảnh bìa tạp chí, tiêu đề serif cỡ lớn đặt chồng hoặc sát ảnh, khoảng trắng rộng như lề trang in, chi tiết kim loại (khung thép, nan hoa) được chụp cận rõ. Áp dụng nhất quán: không dùng hiệu ứng bóng đổ nặng, không dùng gradient rực, không dùng icon hoạt hình.

## 4. Quy tắc hình ảnh

- Ảnh là nội dung chính, không phải trang trí nền mờ: mỗi khối có ít nhất 1 ảnh lớn, đặt ở vị trí trung tâm bố cục.
- Tông ảnh: ấm, sáng tự nhiên (ánh sáng buổi sớm, ngoài trời hoặc xưởng có cửa sổ lớn). Không dùng ảnh tối, lạnh, hoặc lọc màu lạnh.
- Tỉ lệ khung:
  - Hero: toàn màn hình, 16:9 trên desktop; 4:5 trên mobile (cắt dọc, giữ xe đạp nguyên trong khung).
  - Ảnh khối Xưởng và Nhật ký xưởng: 4:3 (ngang) hoặc 1:1 (vuông) khi xếp lưới 2–3 ảnh.
  - Ảnh thẻ dòng xe: 4:3, xe chụp nghiêng toàn thân, nền sáng đồng tông.
- Khoảng trắng: chiều rộng nội dung tối đa 1200px, căn giữa; đệm dọc mỗi khối 96px desktop / 56px mobile; khoảng cách giữa các thẻ 24px.
- Ảnh mẫu ở bản đầu tiên: dùng ảnh mẫu chất lượng cao, đồng tông ấm sáng, đúng tỉ lệ khung trên; ghi rõ trong code/bản dựng rằng đó là ảnh mẫu, chờ ảnh thật của xưởng. Thông tin thật chưa có phải ghi `[CẦN BỔ SUNG]`, tuyệt đối không bịa địa chỉ, số điện thoại hay giá thật.

## 5. Bố cục 6 khối

1. **Hero — ảnh lớn toàn màn hình:** xe đạp khung thép trên đường làng buổi sớm, ánh sáng vàng nhạt. Tiêu đề H1 "Gió Đồng — Xe đạp đóng tay, đi cả đời." (Playfair Display 56px). Nút CTA cam `#C75B21` "Đặt lịch tư vấn" + nút phụ viền xanh than "Xem ba dòng xe".
2. **Xưởng và người thợ:** ảnh lớn 4:3 người thợ đang hàn/hàn khung hoặc lắp nan hoa trong xưởng sáng. Văn bản ngắn kể quy trình đóng xe: chọn ống thép → hàn khung → sơn → lắp ráp → kiểm tra chạy thử. Mỗi bước 1 dòng, không dài quá 2 câu.
3. **Ba dòng xe kèm giá mẫu:** 3 thẻ ngang hàng, mỗi thẻ ảnh 4:3 + tên + mô tả 1–2 dòng + giá mẫu:
   - Xe phố — giá mẫu: 12.900.000 VNĐ.
   - Xe touring — giá mẫu: 18.500.000 VNĐ.
   - Xe đua cổ điển — giá mẫu: 24.900.000 VNĐ.
   - Tất cả giá trên đều là GIÁ MẪU để dựng bố cục, chưa phải giá bán thật — giá thật ghi `[CẦN BỔ SUNG]` khi khách cung cấp.
4. **Đặt đóng riêng — 3 bước:** đo người → chọn khung → lắp ráp. Mỗi bước 1 thẻ có số thứ tự lớn (Playfair Display 40px, màu `#C75B21`), tên bước và mô tả ngắn. Nền khối kem đậm `#E9E2D4`.
5. **Nhật ký xưởng bằng ảnh:** lưới ảnh 2–3 cột, tỉ lệ 1:1 hoặc 4:3, mỗi ảnh 1 chú thích ngắn (14px, màu `#5C6B62`): ví dụ "Khung thép vừa sơn xong", "Lắp nan hoa bằng tay". Ảnh mẫu đồng tông ấm sáng.
6. **Form liên hệ / đặt lịch tư vấn — CHỈ giao diện:** 4 trường (Họ tên, Số điện thoại, Dòng xe quan tâm, Lời nhắn), nút gửi cam `#C75B21`. Form ở bản này chỉ là giao diện, chưa gửi dữ liệu đi đâu; ghi chú dưới form: "Form mẫu — [CẦN BỔ SUNG] địa chỉ xưởng, số điện thoại và email thật của Gió Đồng."

## 6. Ghi chú cho Dev và QA

- Dev dựng trang theo đúng bảng màu, font và cỡ chữ mục 1–2; ảnh mẫu đồng tông ấm sáng, đúng tỉ lệ khung mục 4, bố cục ảnh lớn + khoảng trắng mục 5.
- QA đối chiếu bản dựng với DESIGN.md này ở mức thị giác (ảnh chụp màn hình desktop + mobile): sai màu/font chủ đạo, vỡ bố cục hoặc ảnh lệch tông là lỗi cần sửa.
- Mọi thông tin thật chưa có (địa chỉ, điện thoại, email, giá bán thật) đều để `[CẦN BỔ SUNG]`, không tự bịa.
