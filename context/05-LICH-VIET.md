# LỊCH VIẾT & BẢNG THEO DÕI

> Lưu trữ trong repo (`context/05-LICH-VIET.md` hoặc `_meta/lich-viet.md`) để theo dõi trạng thái bài viết và tiến độ dự án.
>
> *Phiên bản 2 — đã bỏ sprint từ vựng chủ đề, rút từ 15 tuần xuống 14 tuần, từ 79 file xuống 60 file.*

## 1. Khối lượng thực tế

| Hạng mục | Số lượng | Ước tính |
|---|---|---|
| Bài học | 53 | ~1.900 từ/bài → ~101.000 từ |
| Phụ lục | 7 | ~2.500 từ/mục → ~17.500 từ |
| **Tổng** | **60 file nội dung** | **~118.000 từ** |

Một buổi làm việc = **một bài hoàn chỉnh**, khoảng 45–60 phút (gồm thời gian đọc lại và kiểm tra).

## 2. Ba nhịp độ — chọn một

| Nhịp độ | Buổi/tuần | Thời gian hoàn thành | Phù hợp với |
|---|---|---|---|
| Gấp | 10 (2 bài/ngày × 5 ngày) | ~7 tuần | Đang rảnh, muốn xong sớm |
| **Chuẩn (khuyến nghị)** | **5** | **~14 tuần** | Vừa đi làm vừa viết |
| Thong thả | 3 | ~23 tuần | Viết cuối tuần |

Lịch dưới đây theo nhịp **Chuẩn**. Nếu chọn nhịp khác, giữ nguyên thứ tự sprint, chỉ đổi số tuần.

## 3. Lịch 14 tuần

Tổng 69 buổi. Ranh giới sprint không trùng ranh giới tuần — hết bài này thì làm bài kế tiếp trong hàng đợi, không cần chờ sang tuần mới.

| Sprint | Nội dung | Buổi | Tuần |
|---|---|---|---|
| 0 | Dựng khung | 3 | Tuần 0 |
| 1 | Chương 1 — 9 bài + 1 buổi rà chương | 10 | Tuần 1–2 |
| 2 | Chương 4 — 11 bài + 1 buổi rà chương | 12 | Tuần 3–5 |
| 3 | Chương 2 — 12 bài + 1 buổi rà chương | 13 | Tuần 5–7 |
| 4 | Chương 5 — 8 bài | 8 | Tuần 8–9 |
| 5 | Chương 3 — 5 bài | 5 | Tuần 9–10 |
| 6 | Chương 0 + Chương 6 — 8 bài | 8 | Tuần 10–12 |
| 7 | Phụ lục — 7 mục | 5 | Tuần 12–13 |
| 8 | QA & phát hành | 5 | Tuần 13–14 |

### Sprint 0 — Dựng khung (3 buổi)

| Buổi | Việc |
|---|---|
| 0.1 | Tạo repo GitHub, dựng cây thư mục, viết `.gitbook.yaml`, dán `SUMMARY.md` từ CONTEXT 1 |
| 0.2 | Viết `README.md` (sách này cho ai, dùng thế nào, lộ trình gợi ý), kết nối GitBook ↔ GitHub git-sync |
| 0.3 | Cấu hình Antigravity (`GEMINI.md`, skills), viết thử **bài 1.06** rồi so với bài mẫu để hiệu chỉnh rules |

> **Lưu ý**  
> Đừng bỏ buổi 0.3. Bài viết thử là lúc rẻ nhất để phát hiện instructions còn thiếu gì. Nếu bài viết ra lệch bài mẫu, sửa rules / style guide ngay chứ đừng sửa tay từng bài về sau.

### Sprint 1 — Chương 1: Từ loại (10 buổi)

`1.01 → 1.09`, rồi 1 buổi đọc lại cả chương liền mạch.

Viết `1.09` (tổng luyện 60 câu) sau cùng — nó rút câu hỏi từ 8 bài trước, viết sớm sẽ phải sửa lại.

Buổi rà chương kiểm: có ví dụ nào lặp giữa các bài không, phân bố đáp án A/B/C/D trong cả chương có lệch không.

### Sprint 2 — Chương 4: Liên kết câu (12 buổi)

`4.01 → 4.11`, rồi 1 buổi rà chương.

`4.01` (nguyên tắc vàng) phải viết trước và viết chắc — 10 bài sau đều trỏ về nó.

> **Mốc 1 (hết Sprint 2, khoảng tuần 5)**  
> Đã có 20 bài phủ ~40% số câu Part 5. Bật GitBook public, cho vài người học thử.

### Sprint 3 — Chương 2: Động từ (13 buổi)

`2.01 → 2.12`, rồi 1 buổi rà chương. Ưu tiên chất lượng cho `2.06`, `2.09`, `2.11` — ba bài ra đề nhiều nhất trong chương.

### Sprint 4 — Chương 5: Mệnh đề (8 buổi)

`5.01 → 5.08`.

### Sprint 5 — Chương 3: Đại từ & từ hạn định (5 buổi)

`3.01 → 3.05`. Chương nhẹ nhất — dùng để lấy lại đà nếu đang chậm lịch.

### Sprint 6 — Khung sách (8 buổi)

`0.01 → 0.04` và `6.01 → 6.04`. Viết sau cùng là có chủ ý: các bài này phải trỏ ngược vào nội dung đã tồn tại thật, không phải nội dung dự kiến.

Lưu ý khi viết `6.01` và `6.02`: hai bài này đã hấp thụ nội dung của các bài từ vựng bị cắt — `6.01` phải có mục xử lý câu hỏi chọn giữa 4 từ gần nghĩa, `6.02` phải có mục mẫu câu email/memo/thông báo.

### Sprint 7 — Phụ lục (5 buổi)

| Buổi | Việc |
|---|---|
| 7.1 | A.01 bảng hậu tố + A.03 bảng giới từ (tổng hợp từ chương 1 và 4) |
| 7.2 | A.02 bảng to V / V-ing + A.04 bảng từ nối |
| 7.3 | A.05 đề luyện 1–2 |
| 7.4 | A.05 đề luyện 3–5 |
| 7.5 | A.06 đáp án đề luyện + A.07 lộ trình học |

### Sprint 8 — QA & phát hành (5 buổi)

| Buổi | Việc | Prompt gợi ý |
|---|---|---|
| 8.1 | Rà đáp án toàn sách: câu nào có 2 đáp án đúng, phân bố A/B/C/D | `Rà soát chương 1 theo checklist B7, chỉ báo mục chưa đạt, không viết lại bài.` |
| 8.2 | Thống nhất thuật ngữ theo bảng A4 style guide | `Liệt kê mọi chỗ dùng thuật ngữ lệch bảng A4 trong chương 2 và 4.` |
| 8.3 | Kiểm tra link nội bộ chết + ví dụ trùng lặp | |
| 8.4 | Đọc thử trên GitBook, đặc biệt mobile: bảng có tràn không | |
| 8.5 | Viết README cuối, gắn version 1.0, publish | |

> **Mốc 2 (hết tuần 14)**  
> GitBook v1.0 hoàn chỉnh, 60 file nội dung.

## 4. Prompt mẫu theo loại công việc

| Việc | Prompt Antigravity |
|---|---|
| Viết bài mới | `viết bài 4.03` |
| Viết lại một phần | `bài 4.03 phần 5: viết lại 15 câu Part 5, tăng tỉ lệ câu về in/on/at lên 6 câu` |
| Thêm bài tập | `bài 2.09: viết thêm 10 câu Part 5 band 800+, đánh số tiếp từ 16` |
| Bài tổng luyện | `viết bài 1.09: 60 câu Part 5 chia 4 cụm 15 câu, rút kiến thức từ 1.01 đến 1.08, không viết phần lý thuyết` |
| Đề luyện | `viết đề luyện số 1 cho A.05: 30 câu Part 5 + 2 đoạn Part 6, phạm vi kiến thức chương 1 và chương 4` |
| QA một bài | `rà soát bài 2.09 theo checklist B7. Chỉ báo cáo mục chưa đạt kèm câu số, không viết lại bài.` |
| Cập nhật SUMMARY | `cập nhật SUMMARY.md theo các file đã có trong repo` |

## 5. Định nghĩa "Xong"

Một bài được tính là **Xong** khi:

1. Đủ 7 khối, qua toàn bộ checklist B7 trong style guide.
2. Đã tự làm thử phần bài tập và không thấy câu nào mơ hồ.
3. File đã được tạo và đặt đúng thư mục trong repo.
4. Đã đánh dấu trong bảng theo dõi tiến độ.

Trạng thái: `☐` chưa viết · `◐` đang nháp · `☑` xong · `★` đã QA

## 6. Bảng theo dõi tiến độ

### Chương 0 — Mở đầu
- ☑ 0.01 Cấu trúc đề TOEIC & thang điểm
- ☑ 0.02 Bản đồ ngữ pháp TOEIC
- ☑ 0.03 Thuật ngữ & ký hiệu
- ☑ 0.04 Quy trình 20 giây

### Chương 1 — Từ loại
- ☐ 1.01 Trật tự từ và 8 từ loại
- ☑ 1.02 Danh từ: vị trí và hậu tố
- ☑ 1.03 Danh từ chỉ người vs chỉ vật
- ☑ 1.04 Danh từ đếm được / không đếm được
- ☑ 1.05 Tính từ
- ☑ 1.06 Trạng từ
- ☑ 1.07 Động từ: hậu tố
- ☑ 1.08 Những từ dễ nhầm về dạng
- ☐ 1.09 Tổng luyện dạng từ (60 câu)
- ☐ Rà chương 1

### Chương 2 — Động từ
- ☑ 2.01 Hệ thống thì
- ☑ 2.02 Manh mối thời gian
- ☑ 2.03 Hoàn thành vs quá khứ
- ☑ 2.04 Diễn đạt tương lai
- ☑ 2.05 Phối hợp thì
- ☑ 2.06 Hoà hợp chủ ngữ – động từ
- ☑ 2.07 Động từ khuyết thiếu
- ☑ 2.08 Câu bị động
- ☑ 2.09 To V và V-ing
- ☑ 2.10 V + O + to V
- ☑ 2.11 Phân từ và rút gọn
- ☑ 2.12 Động từ bất quy tắc
- ☐ Rà chương 2

### Chương 3 — Đại từ & từ hạn định
- ☑ 3.01 Đại từ
- ☑ 3.02 another / other / each / every / either / neither / both
- ☑ 3.03 Mạo từ
- ☑ 3.04 Từ chỉ số lượng
- ☑ 3.05 Chủ ngữ giả It và There

### Chương 4 — Liên kết câu
- ☑ 4.01 Nguyên tắc vàng
- ☑ 4.02 Giới từ thời gian
- ☑ 4.03 Giới từ nơi chốn
- ☑ 4.04 Giới từ nguyên nhân – nhượng bộ – mục đích
- ☑ 4.05 Cụm giới từ cố định
- ☑ 4.06 Kết hợp cố định với giới từ
- ☑ 4.07 Liên từ kết hợp và tương quan
- ☑ 4.08 Liên từ phụ thuộc
- ☑ 4.09 Từ nối đoạn
- ☑ 4.10 Ba bộ bẫy kinh điển
- ☑ 4.11 Cụm động từ (phrasal verbs)
- ☐ Rà chương 4

### Chương 5 — Mệnh đề
- ☑ 5.01 Mệnh đề quan hệ
- ☑ 5.02 Mệnh đề quan hệ nâng cao
- ☑ 5.03 Rút gọn mệnh đề quan hệ
- ☑ 5.04 Mệnh đề danh ngữ
- ☑ 5.05 Câu điều kiện
- ☑ 5.06 Đảo ngữ
- ☑ 5.07 Thức giả định
- ☑ 5.08 So sánh

### Chương 6 — Chiến lược theo Part
- ☑ 6.01 Part 5
- ☑ 6.02 Part 6
- ☑ 6.03 Part 7
- ☑ 6.04 Ngữ pháp cho Listening

### Phụ lục
- ☑ A.01 Bảng hậu tố
- ☑ A.02 Bảng to V / V-ing
- ☑ A.03 Bảng giới từ
- ☑ A.04 Bảng từ nối
- ☑ A.05 5 đề luyện
- ☑ A.06 Đáp án đề luyện
- ☑ A.07 Lộ trình học

## 7. Quy tắc duy trì chất lượng

1. **Không sửa lại bài cũ giữa sprint.** Ghi vào danh sách cần sửa rồi xử lý gọn trong Sprint 8.
2. **Không thêm chương mới.** Cuốn từ vựng theo chủ đề đã bị tách ra thành dự án riêng — đừng kéo ngược vào.
3. **Chỉ dạy quy tắc ngữ pháp.** Từ vựng business là ngữ liệu để dựng câu ví dụ và bài tập.
4. **Ghi lại mọi hiệu chỉnh style guide.** Cập nhật ngay khi phát hiện trường hợp mới cần chuẩn hóa.