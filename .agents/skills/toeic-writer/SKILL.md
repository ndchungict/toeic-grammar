---
name: toeic-writer
description: >-
  Chuyên gia soạn thảo bản thảo bài học cho cuốn sách "Ngữ pháp TOEIC — Từ nhận diện đến phản xạ".
  Kích hoạt khi người dùng yêu cầu: viết bài mới (vd: "viết bài 4.03"), viết lại một phần,
  thêm bài tập, soạn đề tổng luyện, hoặc bổ sung nội dung bài học.
---

# TOEIC Lesson Writer — Quy trình soạn thảo bài học

Kỹ năng này chịu trách nhiệm sản xuất bài học chuẩn mực cho dự án **"Ngữ pháp TOEIC — Từ nhận diện đến phản xạ"**.

---

## 1. Các bước thực hiện khi nhận lệnh viết bài

### Bước 1: Tra cứu thông tin bài trong `context/02-CONTEXT-cau-truc-sach.md`
- **Mã bài & Tên bài:** Xác định chính xác mã (vd `4.03`), tên hiển thị, tên file (vd `04-03-gioi-tu-noi-chon.md`), thư mục đích (`04-lien-ket-cau/`).
- **Lĩnh vực & Bộ tên riêng:** Tra cứu lĩnh vực kinh doanh của chương và các công ty/nhân vật hư cấu được phân bổ.
- **Bài liên quan:** Lấy danh sách mã bài học trước và bài liên kết.

### Bước 2: Chuẩn bị nội dung theo cấu trúc 7 phần chuẩn
Đảm bảo bài học có đầy đủ 7 khối (độ dài 1.500 – 2.500 từ):

1. **Khối mở đầu:**
   ```markdown
   # <Mã bài> <Tên bài>

   <Một câu mô tả bài này giải quyết vấn đề gì trong đề thi.>

   > **Định vị trong đề**  
   > Xuất hiện ở: Part 5, Part 6  
   > Ước lượng: ~N câu/đề  
   > Ưu tiên: Cao / Trung bình / Thấp  
   > Học trước bài này: <mã bài>
   ```

2. **`## 1. Ngữ pháp cốt lõi`**:
   - Giải thích bản chất, trực diện, không hàn lâm.
   - Mỗi quy tắc đi kèm ví dụ tiếng Anh + dịch tiếng Việt ngay dòng dưới `(Dịch nghĩa...)`.
   - Thuật ngữ ngữ pháp song ngữ ở lần đầu xuất hiện: `danh động từ (gerund)`.

3. **`## 2. Bảng tổng hợp`**:
   - Tối thiểu 1 bảng tra cứu nhanh tóm tắt các quy tắc cốt lõi (tối đa 5 cột).

4. **`## 3. Nhận diện trong đề`**:
   - Dấu hiệu nhận biết đặc trưng trong câu hỏi TOEIC.
   - Quy trình từng bước xử lý câu hỏi (vd: 3 bước chọn đáp án trong 15 giây).

5. **`## 4. Bẫy thường gặp`**:
   - 3–5 bẫy điển hình người Việt hay mắc phải.
   - Mỗi bẫy gồm cặp ✗ / ✓ và một dòng giải thích nguyên nhân bắt đầu bằng `→`.

6. **`## 5. Luyện tập`**:
   - **Số lượng câu:** 15 câu Part 5 + 1 đoạn Part 6 (4 chỗ trống). Đánh số liên tục **1–19**.
     *(Chương 4: 2 đoạn Part 6 -> câu 1–23; Chương 6: thêm đoạn Part 7 -> 3 câu; Bài 1.09: 60 câu Part 5).*
   - **Phân bổ độ khó:** Câu 1–12 (band 600–800), Câu 13–15 đánh dấu `[nâng cao]` (band 800+).
   - **Quy tắc câu Part 5:** Độ dài 10–22 từ; 4 phương án **đồng hạng** (cùng word form / cùng grammar / cùng vocab); chỗ trống `______` ở giữa câu.
   - **Cân bằng đáp án:** A/B/C/D phân bố gần đều (3–5 câu mỗi ký tự), không quá 2 câu liên tiếp trùng đáp án.
   - **Đoạn Part 6:** Độ dài 100–150 từ trong blockquote `>`, phủ 4 dạng: (1) ngữ pháp, (2) từ vựng, (3) từ nối, (4) điền câu logic.

7. **`## 6. Đáp án & giải thích`**:
   - Nằm trọn vẹn trong `<details><summary>Xem đáp án &#x26; giải thích</summary> ... </details>`.
   - Phân nhóm bằng `**Part 5**`, `**Part 6**`.
   - Mỗi câu giải đủ **3 dòng** chuẩn (nối bằng 2 dấu cách cuối dòng):
     - **Dòng 1:** Lý do đúng (nêu căn cứ quan sát trực tiếp trong câu).
     - **Dòng 2:** Lý do sai của cả 3 phương án còn lại.
     - **Dòng 3:** Nghĩa của đáp án đúng + Collocation thường gặp.
     - *(Câu nâng cao có thêm Dòng 4: `Mẹo:`)*.

8. **`## 7. Ghi nhớ nhanh`**:
   - Đúng **5 gạch đầu dòng** tinh gọn nhất.

9. **`## Bài liên quan`**:
   - Danh sách link nội bộ Markdown đến các bài liên quan.

---

## 2. Kiểm tra định dạng trước khi lưu file (Checklist B7)
- [ ] Không có thẻ HTML cấm (chỉ cho phép `<details>` và `<summary>`).
- [ ] Không có cú pháp GitBook cũ `{% ... %}`.
- [ ] Xuống dòng cứng bằng 2 dấu cách (`  `) ở cuối dòng tại các vị trí cần ngắt dòng.
- [ ] Chỗ trống dùng đúng `______` (6 gạch dưới).

---

## 3. Tạo file và trả về kết quả
Sử dụng công cụ `write_to_file` để lưu trực tiếp vào đường dẫn tương ứng trong repo. Kết thúc phản hồi bằng khối chuẩn:

```text
File: <tên file>
Đặt tại: <thư mục>/
Dòng thêm vào SUMMARY.md, mục "<tên mục>":
  * [<mã bài> <tên hiển thị>](<đường dẫn đầy đủ>)
Kế tiếp: <mã bài sau>
Cần bổ sung style guide: <không / liệt kê>
```
