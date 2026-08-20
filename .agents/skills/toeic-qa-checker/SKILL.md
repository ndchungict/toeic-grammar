---
name: toeic-qa-checker
description: >-
  Chuyên gia kiểm định chất lượng (QA) và rà soát bài học theo Checklist B7.
  Kích hoạt khi người dùng yêu cầu: soát lỗi (vd: "rà soát bài 2.09", "kiểm tra chương 1"),
  tìm lỗi định dạng, kiểm tra phân bố đáp án, hoặc phát hiện trùng lặp ví dụ.
---

# TOEIC QA Checker — Rà soát chất lượng theo Checklist B7

Kỹ năng này thực hiện quy trình kiểm tra toàn diện một hoặc nhiều bài học để phát hiện các lỗi định dạng, ngữ pháp, độ khó và phân bố đáp án.

---

## 1. Quy trình kiểm tra chi tiết

Khi nhận lệnh rà soát một bài học (ví dụ: `rà soát bài 2.09 theo checklist B7`):

### Bước 1: Kiểm tra cấu trúc & Nội dung
1. **7 khối bắt buộc:** Đủ 7 phần theo đúng tên tiêu đề chuẩn?
2. **Độ dài bài:** Đạt tối thiểu 1.200 từ (mục tiêu 1.500–2.500 từ)?
3. **Bảng tổng hợp:** Có ít nhất 1 bảng tra cứu nhanh không quá 5 cột?
4. **Bẫy thường gặp:** Có 3–5 bẫy, mỗi bẫy có cặp ✗ / ✓ và dòng giải thích bắt đầu bằng `→`?
5. **Ghi nhớ nhanh:** Đạt đúng 5 gạch đầu dòng?
6. **Bài liên quan:** Các đường dẫn link nội bộ có trỏ đúng file trong repo không?

### Bước 2: Kiểm tra phần Luyện tập & Ra đề
1. **Số lượng câu:** Đủ 15 câu Part 5 + 1 đoạn Part 6 (hoặc 2 đoạn với Ch4)?
2. **Đánh số thứ tự:** Chạy liên tục từ 1 đến hết (vd: 1–19)?
3. **Phân loại độ khó:** Có đúng 3 câu cuối Part 5 được gắn nhãn `[nâng cao]`?
4. **Đồng hạng 4 phương án:** 4 lựa chọn có cùng loại (word form / grammar / vocab) không bị trộn lẫn?
5. **Chỗ trống:** Dùng đúng `______` (6 gạch dưới) và đặt ở giữa câu?
6. **Tính duy nhất của đáp án:** Chỉ có duy nhất 1 phương án đúng trong ngữ cảnh?
7. **Phân bố đáp án:**
   - Tỉ lệ A/B/C/D có cân bằng (3–5 câu cho mỗi chữ cái)?
   - Không có quá 2 câu liên tiếp trùng đáp án?
8. **Đoạn Part 6:**
   - Đủ 4 dạng chỗ trống: Ngữ pháp, Từ vựng, Từ nối, Điền câu?
   - Câu điền câu có thể suy luận được từ mạch logic của đoạn?

### Bước 3: Kiểm tra phần Đáp án & Lời giải
1. **Vị trí `<details>`:** Nằm toàn bộ trong thẻ `<details>` với summary `<summary>Xem đáp án &#x26; giải thích</summary>`?
2. **Cấu trúc 3 dòng:**
   - Dòng 1: Ký tự + Từ đáp án + Lý do đúng (dấu hiệu trong câu)?
   - Dòng 2: Phân tích vì sao cả 3 phương án còn lại bị loại trừ?
   - Dòng 3: Dịch nghĩa đáp án đúng + Collocation liên quan?
   - Dòng 4 (cho câu `[nâng cao]`): Có dòng `Mẹo:` làm nhanh?

### Bước 4: Quét lỗi Định dạng & Markdown
Kiểm tra các lỗi kỹ thuật:
- [ ] Không có chuỗi `{%` (cú pháp GitBook cũ).
- [ ] Không có thẻ `<br>` hoặc thẻ HTML nào khác ngoài `<details>` và `<summary>`.
- [ ] Không có chuỗi `-------` trong câu hỏi.
- [ ] Các dòng trong blockquote `>`, các dòng dịch tiếng Việt, các dòng phương án và các dòng giải thích có đủ **2 dấu cách (`  `) ở cuối dòng** để ngắt dòng cứng không?

---

## 2. Định dạng báo cáo kết quả

Khi xuất báo cáo QA, chỉ tập trung vào các điểm phát hiện được kèm số câu cụ thể:

```markdown
### Kết quả QA bài <Mã bài> (<Tên file>)

- **Trạng thái chung:** [Đạt / Cần chỉnh sửa]
- **Số từ:** ~XXXX từ

#### 1. Các điểm đạt:
- Đầy đủ 7 khối cấu trúc chuẩn.
- Phân bố đáp án Part 5: A(X), B(Y), C(Z), D(W) — Cân bằng.

#### 2. Các điểm cần chỉnh sửa (nếu có):
- **Câu X:** [Mô tả vấn đề: ví dụ thiếu 2 dấu cách cuối dòng / 4 phương án chưa đồng hạng / phân bố đáp án trùng 3 câu liên tiếp...]
- **Mục Y:** [Mô tả vấn đề...]

#### 3. Đề xuất khắc phục:
[Đưa ra giải pháp khắc phục cụ thể hoặc thực hiện chỉnh sửa trực tiếp nếu người dùng yêu cầu.]
```
