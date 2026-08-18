# CONTEXT 2 — Style guide & chuẩn ra đề
 
> Upload vào **Project knowledge**. File này quy định *cách viết*; file 02 quy định *viết cái gì*.
>
> *Phiên bản 3 — chuẩn hoá định dạng để chạy được ở cả GitBook và Hugo: bỏ `{% hint %}`, chỗ trống dùng `______`, mỗi phương án một dòng. Khi mâu thuẫn với bản cũ, bản này thắng.*
 
---
 
# PHẦN A — TRÌNH BÀY
 
## A0. Tương thích trình render — đọc trước tiên
 
Repo vừa publish bằng GitBook, vừa build static site bằng Hugo. Chỉ dùng cú pháp chạy được ở cả hai.
 
| Được dùng | Cấm |
|---|---|
| Bảng Markdown, danh sách, in đậm, in nghiêng, inline code | Mọi cú pháp `{% ... %}` — `{% hint %}`, `{% endhint %}`, `{% tabs %}` |
| Blockquote `>` để làm hộp chú ý | `<br>` và mọi thẻ HTML khác ngoài hai thẻ ở ô bên trái |
| `<details>` và `<summary>` — repo đã bật `unsafe = true` nên hai thẻ này an toàn | Xuống dòng bằng cách gõ Enter một lần rồi viết tiếp |
| Xuống dòng cứng bằng **hai dấu cách** ở cuối dòng | |
 
Nguyên nhân gốc của mọi lỗi trình bày trong sách này: **một dấu xuống dòng đơn không tạo dòng mới trong Markdown.** Hai dòng viết liền nhau sẽ bị dán thành một dòng khi render. Muốn xuống dòng thật mà không mở đoạn mới, kết thúc dòng bằng hai dấu cách.
 
```markdown
Dòng một␣␣
Dòng hai
```
 
Đừng dùng `<br>` để làm việc này. Nó là HTML, một số trình render nuốt hoặc in ra nguyên chữ.
 
> **Cảnh báo**  
> Trong toàn bộ file style guide này, `␣␣` chỉ là ký hiệu minh hoạ cho hai dấu cách thật. Không bao giờ gõ ký tự `␣` vào bài viết — gõ hai dấu cách bình thường.
 
## A1. Template một bài (copy khi bắt đầu bài mới)
 
```markdown
# <Mã bài> <Tên bài>
 
<Một câu mô tả bài này giải quyết vấn đề gì.>
 
> **Định vị trong đề**␣␣
> Xuất hiện ở: Part 5, Part 6␣␣
> Ước lượng: ~N câu/đề␣␣
> Ưu tiên: Cao␣␣
> Học trước bài này: <mã bài>
 
## 1. Ngữ pháp cốt lõi
## 2. Bảng tổng hợp
## 3. Nhận diện trong đề
## 4. Bẫy thường gặp
## 5. Luyện tập
## 6. Đáp án & giải thích
## 7. Ghi nhớ nhanh
## Bài liên quan
```
 
`␣␣` = hai dấu cách thật. Dòng cuối của blockquote không cần.
 
Hộp cảnh báo giữa bài dùng cùng cú pháp, mở đầu bằng nhãn in đậm:
 
```markdown
> **Lưu ý**␣␣
> Sau động từ nối, chỗ trống cần tính từ chứ không phải trạng từ.␣␣
> ✓ *The prototype seems **reliable**.* ✗ *The prototype seems reliably.*
```
 
Nhãn dùng thống nhất: `**Lưu ý**` cho ngoại lệ cần nhớ, `**Cảnh báo**` cho lỗi dễ mất điểm, `**Định vị trong đề**` cho hộp đầu bài.
 
## A2. Quy ước ký hiệu
 
| Ký hiệu | Dùng khi | Ví dụ |
|---|---|---|
| ✓ | Câu đúng | ✓ *He works **efficiently**.* |
| ✗ | Câu sai | ✗ *He works **efficient**.* |
| `______` | Chỗ trống trong câu hỏi — sáu gạch dưới | *The manager ______ the report.* |
| **in đậm** | Từ khoá / từ được xét | |
| *in nghiêng* | Câu tiếng Anh trong dòng văn | |
| `[nâng cao]` | Câu band 800+ | |
| → | Dẫn tới kết luận | |
 
Chỗ trống dùng gạch dưới, **không** dùng gạch nối `-------`. Gạch dưới giống đề thật hơn và không bị Markdown hiểu nhầm thành dòng kẻ ngang.
 
## A3. Cách trình bày ví dụ
 
Luôn theo cấu trúc: câu tiếng Anh → xuống dòng → dịch tiếng Việt trong ngoặc đơn.
 
```markdown
✓ *The proposal was submitted **prior to** the deadline.*
(Bản đề xuất đã được nộp trước hạn chót.)
```
 
Với cặp sai/đúng, đặt sát nhau và thêm một dòng lý do bắt đầu bằng `→`:
 
```markdown
✗ *Despite the price increased, sales remained strong.*
✓ *Despite **the price increase**, sales remained strong.*
→ `despite` là giới từ, sau nó phải là danh từ/cụm danh từ, không phải mệnh đề.
```
 
## A4. Thuật ngữ Việt–Anh chuẩn (dùng thống nhất toàn sách)
 
| Tiếng Việt | Tiếng Anh | Viết tắt trong bảng |
|---|---|---|
| Danh từ | noun | N |
| Động từ | verb | V |
| Tính từ | adjective | Adj |
| Trạng từ | adverb | Adv |
| Giới từ | preposition | Prep |
| Liên từ | conjunction | Conj |
| Trạng từ liên kết | transition / conjunctive adverb | — |
| Mệnh đề | clause | — |
| Mệnh đề quan hệ | relative clause | — |
| Mệnh đề danh ngữ | noun clause | — |
| Chủ ngữ / tân ngữ | subject / object | S / O |
| Dạng từ | word form | — |
| Kết hợp từ | collocation | — |
| Phương án nhiễu | distractor | — |
| Danh động từ | gerund | V-ing |
| Động từ nguyên mẫu có to | to-infinitive | to V |
| Động từ nguyên thể | bare infinitive | V |
| Phân từ hiện tại / quá khứ | present / past participle | V-ing / V-ed |
| Động từ nối | linking verb | — |
| Thức giả định | subjunctive | — |
| Đảo ngữ | inversion | — |
 
Không dùng lẫn lộn: **"trạng từ liên kết"** (however, therefore) phải phân biệt rõ với **"liên từ"** (although, because) trong toàn bộ chương 4.
 
## A5. Giọng văn — làm và không làm
 
**Làm:**
- Câu ngắn, chủ động. "Nhìn 4 phương án trước, đọc câu sau."
- Chỉ thẳng lỗi người Việt hay mắc: "Người Việt hay dịch *mặc dù* thành *despite* rồi ghép luôn mệnh đề vào sau. Đó là câu sai kinh điển."
- Cho quy tắc dùng được ngay, kể cả khi hơi đơn giản hoá — rồi ghi chú ngoại lệ trong blockquote riêng.
**Không làm:**
- Liệt kê đủ mọi trường hợp lý thuyết chỉ vì "cho đầy đủ".
- Viết "như chúng ta đã biết", "rất đơn giản thôi", "chỉ cần nhớ là xong".
- Dùng ví dụ đời thường không liên quan công sở (*My mother cooks dinner*). Ngữ liệu phải là business.
- Dùng emoji ở bất kỳ đâu trong nội dung sách.
---
 
# PHẦN B — CHUẨN RA ĐỀ
 
## B1. Định lượng mỗi bài
 
| Chương | Part 5 | Part 6 | Part 7 |
|---|---|---|---|
| 0 — Mở đầu | 0 | 0 | 0 |
| 1, 2, 3, 5 | 15 câu | 1 đoạn (4 chỗ trống) | — |
| 4 — Liên kết câu | 15 câu | 2 đoạn | — |
| 6 — Chiến lược theo Part | theo nội dung bài | theo nội dung bài | 1 đoạn (3 câu hỏi) |
 
Ngoại lệ: bài **1.09** (tổng luyện) gồm 60 câu Part 5, không có Part 6. Các mục phụ lục **A.05 / A.06** theo định dạng đề luyện riêng.
 
Trong 15 câu Part 5: 12 câu band 600–800, 3 câu cuối `[nâng cao]` band 800+.
 
Đánh số chạy liên tục qua các Part trong cùng một bài: Part 5 là 1–15, bốn chỗ trống Part 6 là 16–19.
 
## B2. Quy tắc viết câu Part 5
 
1. **Độ dài** 10–22 từ. Ngắn hơn thì không đủ ngữ cảnh, dài hơn thì không giống đề thật.
2. **Bối cảnh** luôn là công sở/kinh doanh: hợp đồng, tuyển dụng, vận chuyển, họp, báo cáo, khách hàng, bảo hành, ngân sách.
3. **Chủ đề cấm** (theo chuẩn đề thật): chính trị, tôn giáo, chiến tranh, bệnh tật nghiêm trọng, tai nạn chết người, tình cảm cá nhân, đánh giá tiêu cực về một quốc gia.
4. **Tên riêng hư cấu**, đa dạng quốc tịch. Lấy theo **bảng phân bổ bối cảnh theo chương** ở mục 5 của CONTEXT 1.
5. **4 phương án đồng hạng.** Ba kiểu hợp lệ:
   - *Word form*: `inform / information / informative / informatively`
   - *Grammar*: `has completed / completing / to complete / completes`
   - *Vocabulary*: 4 từ cùng loại từ, gần nghĩa: `approve / accept / admit / allow`
   - **Không trộn** word form với vocabulary trong cùng một câu.
6. **Chỗ trống** đặt ở giữa câu, không đặt ở từ đầu tiên hoặc từ cuối cùng. Ngoại lệ: bài dạy đảo ngữ, và bài dạy trạng từ hoặc trạng từ liên kết đứng đầu câu — khi đó được đặt một câu có chỗ trống ở đầu, vì đó chính là điểm ngữ pháp đang kiểm tra.
7. **Chỉ một đáp án đúng.** Kiểm tra lại: có phương án nào cũng dùng được trong ngữ cảnh khác không? Nếu có, sửa câu cho ngữ cảnh loại trừ nó.
8. **Phân bố đáp án** gần đều A/B/C/D trong mỗi cụm 15 câu (khoảng 3–5 câu mỗi ký tự), không quá 2 câu liên tiếp trùng đáp án. Muốn cân phân bố thì đổi vị trí phương án trong câu, không cần viết lại câu.
9. **Trình bày.** Mở đầu mục Part 5 bằng một dòng hướng dẫn, rồi mỗi câu theo đúng khuôn dưới đây: số câu in đậm, một dòng trống, bốn phương án mỗi phương án một dòng, ký tự in đậm, ba dòng đầu kết thúc bằng hai dấu cách.
```markdown
### Part 5 — Incomplete Sentences
 
Chọn phương án đúng (A/B/C/D) điền vào chỗ trống.
 
**1.** The technicians inspect each component ______ before it leaves the assembly line.
 
**(A)** thorough␣␣
**(B)** thoroughness␣␣
**(C)** thoroughly␣␣
**(D)** more thorough
 
**2.** `[nâng cao]` Repair costs were ______ double the amount set aside in the budget.
 
**(A)** near␣␣
**(B)** nearly␣␣
**(C)** nearest␣␣
**(D)** nearness
```
 
Nhãn `[nâng cao]` đặt ngay sau số câu, trước câu tiếng Anh.
 
## B3. Quy tắc viết đoạn Part 6
 
- Thể loại: email, memo, thông báo nội bộ, quảng cáo, thư khách hàng, bản tin công ty.
- Độ dài 100–150 từ.
- Đúng **4 chỗ trống**, và phải phủ đủ 4 dạng:
  1. một chỗ về **ngữ pháp** (thì / dạng từ / dạng động từ),
  2. một chỗ về **từ vựng**,
  3. một chỗ về **từ nối** (however, therefore, in addition...),
  4. một chỗ **điền câu** (sentence insertion) — 4 phương án là 4 câu hoàn chỉnh.
- Chỗ điền câu bắt buộc phải quyết định được bằng logic mạch văn (đại từ chỉ lại, thứ tự thời gian, quan hệ nguyên nhân), không đoán mò.
**Trình bày:** một dòng dẫn `**Questions N–M** refer to the following memo.`, rồi toàn bộ đoạn văn đặt trong blockquote. Dòng tiêu đề và dòng To/From nằm trong blockquote, kết thúc bằng hai dấu cách. Chỗ trống viết `**(16)______**`.
 
Câu hỏi có phương án ngắn thì dồn một dòng cho gọn; câu điền câu (phương án là câu hoàn chỉnh) thì tách dòng như Part 5.
 
```markdown
### Part 6 — Text Completion
 
**Questions 16–19** refer to the following memo.
 
> **MEMO — Updated Defect Logging Procedure**␣␣
> **To:** All Assembly Line Staff␣␣
> **From:** Daniel Reyes, Operations Manager
>
> Beginning Monday, June 3, all defects must be entered in the digital log. When findings are recorded **(16)______**, the quality team can identify recurring faults earlier.
>
> Paper forms will remain available until the end of the month. **(19)______**
 
**16.**   **(A)** accurate   **(B)** accuracy   **(C)** accurately   **(D)** accuracies␣␣
**17.**   **(A)** installed   **(B)** invented   **(C)** inspected   **(D)** insured␣␣
**18.**   **(A)** Therefore   **(B)** However   **(C)** For example   **(D)** Otherwise
 
**19.**
 
**(A)** Please return all damaged tablets to the maintenance desk.␣␣
**(B)** Last year's inspection targets were revised in September.␣␣
**(C)** After that date, only digital entries will be accepted.␣␣
**(D)** The plant will observe reduced hours during the summer.
```
 
Giữa các phương án dồn dòng dùng **ba dấu cách** cho dễ đọc. Dòng cuối của cụm dồn dòng không cần hai dấu cách.
 
## B4. Quy tắc viết đoạn Part 7
 
- Độ dài 150–250 từ. Thể loại: thông báo, email, bài báo ngắn, lịch trình, hoá đơn, đánh giá sản phẩm.
- 3 câu hỏi, gồm: 1 câu tìm chi tiết, 1 câu suy luận hoặc mục đích văn bản, 1 câu từ vựng trong ngữ cảnh (*The word "X" in paragraph 1, line 3, is closest in meaning to*).
- Thông tin trả lời phải nằm trong bài, không cần kiến thức ngoài.
- Trình bày y hệt Part 6: dòng dẫn `**Questions N–M** refer to the following notice.`, đoạn văn trong blockquote, câu hỏi và phương án tách dòng như Part 5 (phương án Part 7 thường dài).
## B5. Quy tắc viết lời giải
 
Toàn bộ mục 6 nằm trong `<details>`. Trong đó chia nhóm bằng dòng in đậm `**Part 5**`, `**Part 6**` — không dùng tiêu đề `###` để khỏi lọt vào mục lục.
 
Mỗi câu giải theo đúng ba dòng, nối bằng hai dấu cách cuối dòng. Dòng đầu ghi **cả ký tự và từ đáp án** để người học tự chấm nhanh.
 
```markdown
## 6. Đáp án & giải thích
 
<details>
 
<summary>Xem đáp án &#x26; giải thích</summary>
 
**Part 5**
 
**1. (C) thoroughly** — Bỏ chỗ trống đi, câu vẫn đủ S–V–O → cần **trạng từ** đứng sau tân ngữ.␣␣
Sai: (A) tính từ, (B) danh từ, (D) tính từ so sánh hơn — không dạng nào bổ nghĩa được cho động từ.␣␣
Từ khoá: *thoroughly* = một cách kỹ lưỡng. Collocation: *inspect / review / examine thoroughly*.
 
</details>
```
 
Bắt buộc:
- Dòng 1: **lý do đúng**, nêu bằng dấu hiệu quan sát được trong câu (vị trí, từ đứng trước/sau, dấu hiệu thời gian), không nói chung chung "vì đây là trạng từ".
- Dòng 2: **lý do sai của cả 3 phương án còn lại**.
- Dòng 3: **nghĩa của đáp án đúng** + collocation liên quan nếu có.
- Với câu `[nâng cao]`, thêm dòng 4 bắt đầu bằng `Mẹo:` — dấu hiệu nhanh để làm trong 15 giây.
- Với câu điền câu Part 6, dòng đầu chỉ ghi ký tự (không có từ đáp án).
## B6. Kiểm soát độ khó từ vựng
 
- Từ vựng trong **câu hỏi** và **đáp án đúng**: nằm trong vốn từ TOEIC thông dụng (business 3000 từ). Nếu buộc dùng từ hiếm, chú thích nghĩa ngay dưới câu.
- Phương án nhiễu có thể dùng từ hơi lạ hơn, nhưng không được là từ bịa. Bốn phương án phải cùng một họ từ, không chèn một từ khác gốc vào bộ word form.
- Không dùng từ lóng, viết tắt kiểu chat, tiếng Anh-Anh và Anh-Mỹ lẫn lộn trong cùng một bài (mặc định dùng **Anh-Mỹ**: *organize, center, program, traveled*).
## B7. Checklist tự kiểm trước khi kết thúc bài
 
Chạy checklist này trước khi xuất file. Nếu có mục nào chưa đạt, sửa rồi mới xuất.
 
**Nội dung**
- [ ] Đủ 7 khối theo template, đúng thứ tự.
- [ ] Có ít nhất một bảng tổng hợp.
- [ ] Phần "Bẫy thường gặp" có 3–5 bẫy, mỗi bẫy có cặp ✗/✓ và một dòng `→`.
- [ ] Đủ số câu theo bảng B1, đánh số chạy liên tục 1–19.
- [ ] Mọi câu Part 5 dài 10–22 từ, bối cảnh business.
- [ ] Không câu nào có 2 đáp án đúng.
- [ ] Phân bố đáp án A/B/C/D gần đều, không quá 2 câu liên tiếp trùng.
- [ ] Mọi lời giải có đủ 3 dòng; câu `[nâng cao]` có thêm dòng `Mẹo:`.
- [ ] Ghi nhớ nhanh đúng 5 gạch đầu dòng.
- [ ] Link "Bài liên quan" trỏ đúng đường dẫn trong file 02.
- [ ] Độ dài ≥ 1.200 từ.
**Định dạng** — chạy tìm kiếm trên file, các chuỗi sau phải cho **0 kết quả**:
- [ ] `{%` — không còn cú pháp GitBook.
- [ ] `<br` — không còn thẻ xuống dòng HTML.
- [ ] `-------` — chỗ trống phải là `______`.
- [ ] Ba dòng trống liên tiếp.
**Định dạng** — các mục sau phải có:
- [ ] Hộp định vị đầu bài là blockquote, các dòng nối bằng hai dấu cách.
- [ ] Mỗi phương án Part 5 nằm trên một dòng riêng, ký tự in đậm `**(A)**`.
- [ ] Đoạn Part 6 / Part 7 nằm trong blockquote, có dòng dẫn `**Questions N–M** refer to...`.
- [ ] Đáp án nằm trong `<details>`, dòng đầu mỗi lời giải ghi cả ký tự lẫn từ.