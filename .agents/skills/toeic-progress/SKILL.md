---
name: toeic-progress
description: >-
  Theo dõi tiến độ, thống kê các bài học đã hoàn thành / còn thiếu, và đồng bộ SUMMARY.md.
  Kích hoạt khi người dùng yêu cầu: kiểm tra tiến độ, xem bài nào chưa viết,
  cập nhật mục lục SUMMARY.md, hoặc tổng kết trạng thái sách.
---

# TOEIC Progress Tracker — Quản lý tiến độ & Mục lục

Kỹ năng này quét toàn bộ cây thư mục của dự án, đối chiếu với danh mục 60 bài học trong `context/02-CONTEXT-cau-truc-sach.md` và `context/05-LICH-VIET.md`, sau đó báo cáo tiến độ chi tiết và tự động cập nhật `SUMMARY.md`.

---

## 1. Quy trình kiểm tra tiến độ

1. Quét các thư mục nội dung:
   - `00-mo-dau/` (4 bài)
   - `01-tu-loai/` (9 bài: 1.01 -> 1.09)
   - `02-dong-tu/` (12 bài: 2.01 -> 2.12)
   - `03-dai-tu-han-dinh/` (5 bài: 3.01 -> 3.05)
   - `04-lien-ket-cau/` (11 bài: 4.01 -> 4.11)
   - `05-menh-de/` (8 bài: 5.01 -> 5.08)
   - `06-theo-part/` (4 bài: 6.01 -> 6.04)
   - `phu-luc/` (7 mục: A.01 -> A.07)

2. Đếm số lượng file thực tế đã hoàn thành so với tổng số 60 file.

3. Liệt kê danh sách các bài còn thiếu hoặc đang ở dạng nháp.

4. Đồng bộ file `SUMMARY.md` và cập nhật các ô tick trong `context/05-LICH-VIET.md`.

---

## 2. Định dạng báo cáo tiến độ

```markdown
### 📊 Báo cáo tiến độ dự án: Ngữ pháp TOEIC

- **Tổng số file:** XX / 60 file (XX%)
- **Chương 0 (Mở đầu):** 4/4 (100%)
- **Chương 1 (Từ loại):** X/9 (XX%)
- **Chương 2 (Động từ):** 12/12 (100%)
- **Chương 3 (Đại từ & Từ hạn định):** 5/5 (100%)
- **Chương 4 (Liên kết câu):** 11/11 (100%)
- **Chương 5 (Mệnh đề):** 8/8 (100%)
- **Chương 6 (Vận dụng theo Part):** 4/4 (100%)
- **Phụ lục:** 7/7 (100%)

#### 🎯 Các bài cần viết tiếp theo:
1. `1.01` — Trật tự từ và 8 từ loại (`01-tu-loai/01-01-trat-tu-tu.md`)
2. `1.09` — Tổng luyện dạng từ 60 câu (`01-tu-loai/01-09-tong-luyen-dang-tu.md`)
```
