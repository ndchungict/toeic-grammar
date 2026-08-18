# CONTEXT 1 — Cấu trúc sách & bản đồ bài học
 
> Upload file này vào **Project knowledge**. Đây là nguồn chân lý duy nhất về tên bài, mã bài, đường dẫn file. Khi có mâu thuẫn, file này thắng.
>
> *Phiên bản 2 — đã loại bỏ chương từ vựng, đánh lại số chương 7 → 6.*
 
## 1. Thông tin sách
 
| Trường | Giá trị |
|---|---|
| Tên sách | Ngữ pháp TOEIC — Từ nhận diện đến phản xạ |
| Ngôn ngữ giảng giải | Tiếng Việt |
| Ngôn ngữ ngữ liệu | Tiếng Anh (business/workplace) |
| Phạm vi | TOEIC Listening & Reading, trọng tâm Part 5–6, hỗ trợ Part 7 và Listening |
| Tổng số bài | 53 bài + 7 phụ lục |
| Nền tảng xuất bản | GitBook (git-sync với GitHub) |
 
## 2. Phạm vi — cái gì KHÔNG nằm trong sách này
 
Đây là sách **ngữ pháp**. Ranh giới phân định:
 
**Thuộc phạm vi** — từ vựng mang bản chất ngữ pháp:
- Từ chức năng: giới từ, liên từ, trạng từ liên kết, từ hạn định.
- Kết trị của động từ: động từ nào đi với giới từ nào, động từ nào theo sau bởi *to V* hay *V-ing*.
- Cặp từ nhầm về **dạng**: *affect/effect, rise/raise, economic/economical* — vì đây là câu hỏi dạng từ.
- Cụm động từ (phrasal verbs) — động từ + tiểu từ, thuộc chương giới từ.
**Ngoài phạm vi** — từ vựng thuần nghĩa:
- Danh sách từ theo chủ đề (khách sạn, y tế, vận chuyển...). Biết *itinerary* = lịch trình không suy ra được từ quy tắc nào, chỉ có thuộc lòng.
- Truyện chêm, bảng tra từ IPA, bài luyện nhớ từ.
Phần ngoài phạm vi thuộc về **một cuốn thứ hai riêng biệt** ("Từ vựng TOEIC theo chủ đề"), có project riêng, lịch riêng, chỉ cross-link sang cuốn này.
 
Trong cuốn ngữ pháp, từ vựng business đóng vai trò **ngữ liệu** — kho từ để dựng câu ví dụ và câu bài tập — chứ không phải nội dung được dạy. Ràng buộc này đã nằm ở mục B2 và B6 của style guide.
 
{% hint style="warning" %}
Nếu một bài đang viết bắt đầu dạy nghĩa của từ thay vì dạy quy tắc, bài đó đã trượt khỏi phạm vi. Cắt.
{% endhint %}
 
## 3. Cấu trúc thư mục repo
 
```
.
├── README.md                  # Trang bìa: sách này dành cho ai, dùng thế nào
├── SUMMARY.md                 # Mục lục điều hướng của GitBook
├── .gitbook.yaml
├── 00-mo-dau/
├── 01-tu-loai/
├── 02-dong-tu/
├── 03-dai-tu-han-dinh/
├── 04-lien-ket-cau/
├── 05-menh-de/
├── 06-theo-part/
├── phu-luc/
├── _meta/                     # lịch viết, danh sách cần sửa, ý tưởng v2
└── .gitbook/assets/
```
 
`.gitbook.yaml`:
 
```yaml
root: ./
structure:
  readme: README.md
  summary: SUMMARY.md
```
 
## 4. Quy ước đặt tên
 
- Mã bài: `C.NN` — C là số chương (0–6), NN là số thứ tự trong chương.
- Tên file: `CC-NN-slug-khong-dau.md`, ví dụ `04-03-gioi-tu-noi-chon.md`.
- Phụ lục: `A.NN` → `phu-luc/A-NN-slug.md`.
- Slug không dấu, không khoảng trắng, dùng gạch nối.
## 5. Phân bổ bối cảnh theo chương
 
Mỗi phiên viết bài là một cuộc trò chuyện độc lập — Claude không nhìn thấy các bài đã viết trước đó. Nếu mọi bài đều rút từ chung một nhúm tên công ty, thì qua 53 bài × khoảng 19 câu, gần một nghìn câu hỏi sẽ xoay quanh vài cái tên. Đọc rời từng bài thì không nhận ra; đọc liền mạch thì nhàm rõ rệt.
 
Cách chặn mà không cần Claude đọc lại repo: **mỗi chương có một lĩnh vực kinh doanh riêng và bộ tên riêng riêng.** Lĩnh vực khác nhau kéo theo từ vựng nền khác nhau, nên va chạm giảm hẳn.
 
| Chương | Lĩnh vực | Công ty | Tên người |
|---|---|---|---|
| 1 — Từ loại | Sản xuất, kiểm định chất lượng | Nordvale Manufacturing, Keswick Industrial | Ms. Tanaka, Mr. Reyes, Ms. Bergström |
| 2 — Động từ | Hậu cần, vận chuyển, kho bãi | Halverson Logistics, Tam Freight | Mr. Okonkwo, Ms. Delacroix, Mr. Halvorsen |
| 3 — Đại từ & từ hạn định | Nhân sự, tuyển dụng, đào tạo | Meridian Consulting, Alder & Voss | Ms. Duval, Mr. Nakamura, Ms. Achebe |
| 4 — Liên kết câu | Hợp đồng, pháp lý, truyền thông | Castellan Group, Brightpath Media | Ms. Lindqvist, Mr. Sandoval, Ms. Rahman |
| 5 — Mệnh đề | Tài chính, ngân hàng, đầu tư | Fairmont Capital, Ashworth & Pine | Mr. Whitfield, Ms. Petrova, Mr. Adeyemi |
| 0 và 6 | Tổng hợp | dùng lại tự do từ các chương trên | |
| Phụ lục | Tổng hợp | dùng lại tự do | |
 
Quy tắc áp dụng:
 
- Trong một bài dùng tối đa 2–3 tên công ty; không lặp cùng một công ty quá 4 câu liên tiếp.
- Đoạn Part 6 và Part 7 của bài cũng đặt trong lĩnh vực của chương, không lệch sang lĩnh vực khác.
- Được phép nghĩ thêm tên hư cấu mới **cùng lĩnh vực** nếu thấy bí — miễn không dùng tên có thật.
- Bài 1.09 (tổng luyện) và phụ lục A.05 (đề luyện) rút câu từ nhiều chương nên được trộn tên tự do; đây chính là chỗ đề thi thật cũng trộn.
## 6. Bản đồ bài học
 
### Chương 0 — Mở đầu (`00-mo-dau/`)
 
| Mã | Tên bài | File | Ghi chú nội dung |
|---|---|---|---|
| 0.01 | Cấu trúc đề TOEIC & thang điểm 10–990 | `00-01-cau-truc-de-toeic.md` | 7 part, thời lượng, quy đổi điểm, phân bổ thời gian Reading |
| 0.02 | Bản đồ ngữ pháp TOEIC: chủ điểm nào ra bao nhiêu câu | `00-02-ban-do-ngu-phap.md` | Bảng phân bố dạng câu hỏi Part 5–6, lộ trình theo mục tiêu điểm |
| 0.03 | Thuật ngữ & ký hiệu dùng trong sách | `00-03-thuat-ngu.md` | Bảng thuật ngữ Việt–Anh, ký hiệu ✓ ✗ `[nâng cao]` |
| 0.04 | Quy trình xử lý một câu Part 5 trong 20 giây | `00-04-quy-trinh-20-giay.md` | Nhìn 4 phương án trước → phân loại dạng câu → xét vị trí trống |
 
### Chương 1 — Từ loại & vị trí từ (`01-tu-loai/`) — **Ưu tiên Cao, ~10–12 câu/đề**
 
| Mã | Tên bài | File |
|---|---|---|
| 1.01 | Trật tự từ trong câu tiếng Anh & 8 từ loại | `01-01-trat-tu-tu.md` |
| 1.02 | Danh từ: vị trí và hậu tố nhận biết | `01-02-danh-tu-vi-tri-hau-to.md` |
| 1.03 | Danh từ chỉ người vs chỉ vật; danh từ ghép | `01-03-danh-tu-nguoi-vat-danh-tu-ghep.md` |
| 1.04 | Danh từ đếm được và không đếm được | `01-04-danh-tu-dem-duoc.md` |
| 1.05 | Tính từ: vị trí, hậu tố, các cặp dễ bẫy | `01-05-tinh-tu.md` |
| 1.06 | Trạng từ: vị trí bổ nghĩa và nhóm không đuôi -ly | `01-06-trang-tu.md` |
| 1.07 | Động từ: hậu tố -ize, -ify, -en, -ate | `01-07-dong-tu-hau-to.md` |
| 1.08 | Những từ dễ nhầm về dạng | `01-08-tu-de-nham.md` |
| 1.09 | Tổng luyện dạng từ — 60 câu | `01-09-tong-luyen-dang-tu.md` |
 
> **1.08** chỉ xử lý các cặp nhầm về **dạng và cấu tạo**: *affect/effect, rise/raise, lay/lie, economic/economical, considerable/considerate, assure/ensure/insure, principal/principle*. Không mở rộng thành bài từ vựng.
>
> **1.09** là bài đặc biệt: không có phần lý thuyết, chỉ gồm 60 câu Part 5 chia 4 cụm 15 câu + đáp án giải thích. Viết sau khi xong 1.01–1.08.
 
### Chương 2 — Động từ: thì, thể, dạng (`02-dong-tu/`) — **Ưu tiên Cao, ~8–10 câu/đề**
 
| Mã | Tên bài | File |
|---|---|---|
| 2.01 | 12 thì và 6 thì chiếm 90% đề TOEIC | `02-01-he-thong-thi.md` |
| 2.02 | Manh mối thời gian trong câu hỏi thì | `02-02-manh-moi-thoi-gian.md` |
| 2.03 | Hiện tại hoàn thành vs quá khứ đơn trong văn phong công sở | `02-03-hoan-thanh-vs-qua-khu.md` |
| 2.04 | Diễn đạt tương lai: will, be going to, be due to, be scheduled to | `02-04-dien-dat-tuong-lai.md` |
| 2.05 | Sự phối hợp thì trong câu phức | `02-05-phoi-hop-thi.md` |
| 2.06 | Hoà hợp chủ ngữ – động từ | `02-06-hoa-hop-chu-ngu-dong-tu.md` |
| 2.07 | Động từ khuyết thiếu và bán khuyết thiếu | `02-07-dong-tu-khuyet-thieu.md` |
| 2.08 | Câu bị động và các cụm bị động cố định | `02-08-cau-bi-dong.md` |
| 2.09 | To V hay V-ing: bảng phân loại theo tần suất | `02-09-to-v-va-ving.md` |
| 2.10 | Cấu trúc V + O + to V | `02-10-v-o-to-v.md` |
| 2.11 | Phân từ và mệnh đề rút gọn | `02-11-phan-tu-rut-gon.md` |
| 2.12 | Bảng động từ bất quy tắc theo nhóm quy luật | `02-12-dong-tu-bat-quy-tac.md` |
 
### Chương 3 — Đại từ & từ hạn định (`03-dai-tu-han-dinh/`) — **Ưu tiên TB, ~4–5 câu/đề**
 
| Mã | Tên bài | File |
|---|---|---|
| 3.01 | Đại từ nhân xưng, sở hữu, phản thân | `03-01-dai-tu.md` |
| 3.02 | another / other / others / the other / each / every / either / neither / both | `03-02-tu-chi-dinh-doi-lap.md` |
| 3.03 | Mạo từ a, an, the và trường hợp không mạo từ | `03-03-mao-tu.md` |
| 3.04 | Từ chỉ số lượng | `03-04-tu-chi-so-luong.md` |
| 3.05 | Chủ ngữ giả It và There | `03-05-chu-ngu-gia.md` |
 
### Chương 4 — Liên kết câu (`04-lien-ket-cau/`) — **Ưu tiên Cao nhất, ~12–15 câu/đề**
 
| Mã | Tên bài | File |
|---|---|---|
| 4.01 | Nguyên tắc vàng: giới từ + danh từ / liên từ + mệnh đề / trạng từ liên kết + câu | `04-01-nguyen-tac-vang.md` |
| 4.02 | Giới từ chỉ thời gian | `04-02-gioi-tu-thoi-gian.md` |
| 4.03 | Giới từ chỉ nơi chốn và phương hướng | `04-03-gioi-tu-noi-chon.md` |
| 4.04 | Giới từ chỉ nguyên nhân, nhượng bộ, mục đích | `04-04-gioi-tu-nguyen-nhan.md` |
| 4.05 | Cụm giới từ cố định trong văn phòng | `04-05-cum-gioi-tu-co-dinh.md` |
| 4.06 | Kết hợp cố định: N + giới từ / Adj + giới từ / V + giới từ | `04-06-collocation-gioi-tu.md` |
| 4.07 | Liên từ kết hợp và liên từ tương quan | `04-07-lien-tu-ket-hop.md` |
| 4.08 | Liên từ phụ thuộc | `04-08-lien-tu-phu-thuoc.md` |
| 4.09 | Từ nối đoạn — trọng tâm Part 6 | `04-09-tu-noi-doan.md` |
| 4.10 | Ba bộ bẫy kinh điển: because/because of/therefore — although/despite/however — during/while | `04-10-ba-bo-bay.md` |
| 4.11 | Cụm động từ (phrasal verbs) tần suất cao | `04-11-phrasal-verbs.md` |
 
> **4.11** dạy theo **tiểu từ** (*up, out, off, over, through*) chứ không theo danh sách từ vựng — mục tiêu là người đọc suy được nghĩa từ tiểu từ, không phải học thuộc 80 cụm.
 
### Chương 5 — Mệnh đề (`05-menh-de/`) — **Ưu tiên Cao, ~6–8 câu/đề**
 
| Mã | Tên bài | File |
|---|---|---|
| 5.01 | Mệnh đề quan hệ: who, whom, whose, which, that, where, when | `05-01-menh-de-quan-he.md` |
| 5.02 | Mệnh đề quan hệ xác định và không xác định; giới từ + which/whom | `05-02-menh-de-quan-he-nang-cao.md` |
| 5.03 | Rút gọn mệnh đề quan hệ | `05-03-rut-gon-menh-de-quan-he.md` |
| 5.04 | Mệnh đề danh ngữ | `05-04-menh-de-danh-ngu.md` |
| 5.05 | Câu điều kiện trong thư tín thương mại | `05-05-cau-dieu-kien.md` |
| 5.06 | Đảo ngữ điều kiện và đảo ngữ nhấn mạnh | `05-06-dao-ngu.md` |
| 5.07 | Thức giả định | `05-07-thuc-gia-dinh.md` |
| 5.08 | So sánh và các bẫy so sánh kiểu TOEIC | `05-08-so-sanh.md` |
 
### Chương 6 — Vận dụng theo từng Part (`06-theo-part/`)
 
| Mã | Tên bài | File | Ghi chú |
|---|---|---|---|
| 6.01 | Part 5: 6 dạng câu hỏi và thứ tự ưu tiên xử lý | `06-01-chien-luoc-part-5.md` | Bao gồm cách xử lý câu hỏi từ vựng (chọn giữa 4 từ gần nghĩa) bằng ngữ cảnh và collocation |
| 6.02 | Part 6: thì theo mạch văn, từ nối, câu điền vào đoạn | `06-02-chien-luoc-part-6.md` | Bao gồm mẫu câu email, memo, thông báo, quảng cáo |
| 6.03 | Part 7: đọc lướt, câu suy luận, bài đọc kép và ba | `06-03-chien-luoc-part-7.md` | |
| 6.04 | Ngữ pháp cho Listening: dạng rút gọn, nối âm, paraphrase | `06-04-ngu-phap-cho-listening.md` | |
 
### Phụ lục (`phu-luc/`)
 
| Mã | Tên | File |
|---|---|---|
| A.01 | Bảng hậu tố nhận diện từ loại | `A-01-bang-hau-to.md` |
| A.02 | Bảng động từ theo sau bởi to V / V-ing / cả hai | `A-02-bang-to-v-ving.md` |
| A.03 | Bảng giới từ đi kèm N / Adj / V | `A-03-bang-gioi-tu.md` |
| A.04 | Bảng từ nối phân theo chức năng | `A-04-bang-tu-noi.md` |
| A.05 | 5 đề luyện Part 5 + Part 6 | `A-05-de-luyen.md` |
| A.06 | Đáp án và giải thích đề luyện | `A-06-dap-an-de-luyen.md` |
| A.07 | Lộ trình 4 / 8 / 12 tuần theo mục tiêu điểm | `A-07-lo-trinh.md` |
 
## 7. SUMMARY.md (bản hoàn chỉnh — copy thẳng vào repo)
 
```markdown
# Table of contents
 
* [Giới thiệu](README.md)
 
## Mở đầu
 
* [0.01 Cấu trúc đề TOEIC & thang điểm](00-mo-dau/00-01-cau-truc-de-toeic.md)
* [0.02 Bản đồ ngữ pháp TOEIC](00-mo-dau/00-02-ban-do-ngu-phap.md)
* [0.03 Thuật ngữ & ký hiệu](00-mo-dau/00-03-thuat-ngu.md)
* [0.04 Quy trình xử lý một câu Part 5 trong 20 giây](00-mo-dau/00-04-quy-trinh-20-giay.md)
 
## Chương 1 — Từ loại & vị trí từ
 
* [1.01 Trật tự từ và 8 từ loại](01-tu-loai/01-01-trat-tu-tu.md)
* [1.02 Danh từ: vị trí và hậu tố](01-tu-loai/01-02-danh-tu-vi-tri-hau-to.md)
* [1.03 Danh từ chỉ người vs chỉ vật](01-tu-loai/01-03-danh-tu-nguoi-vat-danh-tu-ghep.md)
* [1.04 Danh từ đếm được và không đếm được](01-tu-loai/01-04-danh-tu-dem-duoc.md)
* [1.05 Tính từ](01-tu-loai/01-05-tinh-tu.md)
* [1.06 Trạng từ](01-tu-loai/01-06-trang-tu.md)
* [1.07 Động từ: hậu tố](01-tu-loai/01-07-dong-tu-hau-to.md)
* [1.08 Những từ dễ nhầm về dạng](01-tu-loai/01-08-tu-de-nham.md)
* [1.09 Tổng luyện dạng từ — 60 câu](01-tu-loai/01-09-tong-luyen-dang-tu.md)
 
## Chương 2 — Động từ
 
* [2.01 Hệ thống thì](02-dong-tu/02-01-he-thong-thi.md)
* [2.02 Manh mối thời gian](02-dong-tu/02-02-manh-moi-thoi-gian.md)
* [2.03 Hiện tại hoàn thành vs quá khứ đơn](02-dong-tu/02-03-hoan-thanh-vs-qua-khu.md)
* [2.04 Diễn đạt tương lai](02-dong-tu/02-04-dien-dat-tuong-lai.md)
* [2.05 Phối hợp thì](02-dong-tu/02-05-phoi-hop-thi.md)
* [2.06 Hoà hợp chủ ngữ – động từ](02-dong-tu/02-06-hoa-hop-chu-ngu-dong-tu.md)
* [2.07 Động từ khuyết thiếu](02-dong-tu/02-07-dong-tu-khuyet-thieu.md)
* [2.08 Câu bị động](02-dong-tu/02-08-cau-bi-dong.md)
* [2.09 To V và V-ing](02-dong-tu/02-09-to-v-va-ving.md)
* [2.10 V + O + to V](02-dong-tu/02-10-v-o-to-v.md)
* [2.11 Phân từ và mệnh đề rút gọn](02-dong-tu/02-11-phan-tu-rut-gon.md)
* [2.12 Động từ bất quy tắc](02-dong-tu/02-12-dong-tu-bat-quy-tac.md)
 
## Chương 3 — Đại từ & từ hạn định
 
* [3.01 Đại từ](03-dai-tu-han-dinh/03-01-dai-tu.md)
* [3.02 another / other / each / every / either / neither / both](03-dai-tu-han-dinh/03-02-tu-chi-dinh-doi-lap.md)
* [3.03 Mạo từ](03-dai-tu-han-dinh/03-03-mao-tu.md)
* [3.04 Từ chỉ số lượng](03-dai-tu-han-dinh/03-04-tu-chi-so-luong.md)
* [3.05 Chủ ngữ giả It và There](03-dai-tu-han-dinh/03-05-chu-ngu-gia.md)
 
## Chương 4 — Liên kết câu
 
* [4.01 Nguyên tắc vàng](04-lien-ket-cau/04-01-nguyen-tac-vang.md)
* [4.02 Giới từ thời gian](04-lien-ket-cau/04-02-gioi-tu-thoi-gian.md)
* [4.03 Giới từ nơi chốn](04-lien-ket-cau/04-03-gioi-tu-noi-chon.md)
* [4.04 Giới từ nguyên nhân – nhượng bộ – mục đích](04-lien-ket-cau/04-04-gioi-tu-nguyen-nhan.md)
* [4.05 Cụm giới từ cố định](04-lien-ket-cau/04-05-cum-gioi-tu-co-dinh.md)
* [4.06 Kết hợp cố định với giới từ](04-lien-ket-cau/04-06-collocation-gioi-tu.md)
* [4.07 Liên từ kết hợp và tương quan](04-lien-ket-cau/04-07-lien-tu-ket-hop.md)
* [4.08 Liên từ phụ thuộc](04-lien-ket-cau/04-08-lien-tu-phu-thuoc.md)
* [4.09 Từ nối đoạn](04-lien-ket-cau/04-09-tu-noi-doan.md)
* [4.10 Ba bộ bẫy kinh điển](04-lien-ket-cau/04-10-ba-bo-bay.md)
* [4.11 Cụm động từ (phrasal verbs)](04-lien-ket-cau/04-11-phrasal-verbs.md)
 
## Chương 5 — Mệnh đề
 
* [5.01 Mệnh đề quan hệ](05-menh-de/05-01-menh-de-quan-he.md)
* [5.02 Mệnh đề quan hệ nâng cao](05-menh-de/05-02-menh-de-quan-he-nang-cao.md)
* [5.03 Rút gọn mệnh đề quan hệ](05-menh-de/05-03-rut-gon-menh-de-quan-he.md)
* [5.04 Mệnh đề danh ngữ](05-menh-de/05-04-menh-de-danh-ngu.md)
* [5.05 Câu điều kiện](05-menh-de/05-05-cau-dieu-kien.md)
* [5.06 Đảo ngữ](05-menh-de/05-06-dao-ngu.md)
* [5.07 Thức giả định](05-menh-de/05-07-thuc-gia-dinh.md)
* [5.08 So sánh](05-menh-de/05-08-so-sanh.md)
 
## Chương 6 — Chiến lược theo Part
 
* [6.01 Part 5](06-theo-part/06-01-chien-luoc-part-5.md)
* [6.02 Part 6](06-theo-part/06-02-chien-luoc-part-6.md)
* [6.03 Part 7](06-theo-part/06-03-chien-luoc-part-7.md)
* [6.04 Ngữ pháp cho Listening](06-theo-part/06-04-ngu-phap-cho-listening.md)
 
## Phụ lục
 
* [A.01 Bảng hậu tố](phu-luc/A-01-bang-hau-to.md)
* [A.02 Bảng to V / V-ing](phu-luc/A-02-bang-to-v-ving.md)
* [A.03 Bảng giới từ](phu-luc/A-03-bang-gioi-tu.md)
* [A.04 Bảng từ nối](phu-luc/A-04-bang-tu-noi.md)
* [A.05 Đề luyện](phu-luc/A-05-de-luyen.md)
* [A.06 Đáp án đề luyện](phu-luc/A-06-dap-an-de-luyen.md)
* [A.07 Lộ trình học](phu-luc/A-07-lo-trinh.md)
```
 
## 8. Thứ tự viết khuyến nghị
 
Không viết theo thứ tự 0.01 → 6.04. Viết theo thứ tự sau để có bản dùng được sớm nhất:
 
1. **Lõi:** 1.01 → 1.07, rồi 4.01 → 4.11, rồi 2.06 và 2.09. (~20 bài, phủ khoảng 40% số câu Part 5.)
2. **Bổ sung:** chương 2 còn lại, chương 5.
3. **Mở rộng:** chương 3, bài 1.08.
4. **Tổng luyện:** 1.09 — sau khi xong toàn bộ chương 1.
5. **Khung:** chương 0, chương 6 — viết sau cùng vì cần trỏ ngược vào các bài đã có.
6. **Phụ lục:** viết cuối, tổng hợp lại từ các bài đã viết để tránh mâu thuẫn.
 