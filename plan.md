# PLAN — AI Product Teardown Lab

## 1. Mục tiêu bài lab

Phân tích teardown một sản phẩm AI thật để hiểu **chuỗi quyết định sản phẩm** bên trong thay vì chỉ liệt kê tính năng.

Sau bài lab, nhóm cần có khả năng:

- Dựng timeline **6–8 cột mốc lớn** từ nguồn công khai.
- Revert mỗi cột mốc về một **nguyên lý sản phẩm** đã học.
- Xác định **early adopters**, tệp user hiện tại và **JTBD**.
- Phân tích **switching cost theo 4 forces**.
- Đưa ra **3 dự đoán hướng đi trong 6–12 tháng** dựa trên dữ liệu đã phân tích.
- Khai báo **AI Log** trung thực: AI làm gì, nhóm làm gì và kiểm chứng ra sao.

---

## 2. Output cuối cùng

Nhóm cần nộp:

```text
memo.md
slides.pdf
```

### `memo.md`

Gồm 4 phần:

1. Timeline các cập nhật lớn.
2. Tệp user & JTBD.
3. Ba dự đoán hướng đi.
4. AI Log.

### `slides.pdf`

Trình bày ngắn gọn:

```text
Sản phẩm
  ↓
Timeline
  ↓
Nguyên lý rút ra
  ↓
User & JTBD
  ↓
Switching Cost
  ↓
3 dự đoán
```

---

# 3. Tổng quan quy trình

```text
CP0
Chọn sản phẩm + tìm nguồn
        ↓
CP1
Timeline 6–8 mốc + Revert nguyên lý
        ↓
CP2
User + JTBD + 4 Forces
        ↓
CP3
3 dự đoán 6–12 tháng
        ↓
CP4
AI Log + hoàn thiện memo
        ↓
Hoàn tất
Slides + kiểm tra + nộp bài
```

**Tổng thời lượng:** khoảng 2 giờ.

**Nhóm:** 3–4 người.

---

# 4. Thuật ngữ cần hiểu

## 4.1. Teardown

Teardown là **tháo rời sản phẩm để hiểu các quyết định bên trong**, không chỉ xem sản phẩm có những tính năng gì.

Câu hỏi chính:

> Tại sao sản phẩm lại đi theo hướng này ở thời điểm đó?

---

## 4.2. Milestone — Cột mốc

Một milestone là **quyết định sản phẩm lớn**, ví dụ:

- Ra mắt tính năng AI lớn.
- Pivot sản phẩm.
- Thay đổi pricing.
- Mở rộng sang segment mới.
- Thay đổi mô hình sản phẩm.

Không chọn các cập nhật nhỏ như:

- Bug fix.
- Sửa UI nhỏ.
- Cải thiện performance nhỏ.
- Thay đổi text.

Mục tiêu là chọn **6–8 quyết định quan trọng**, không phải copy toàn bộ changelog.

---

## 4.3. Revert về nguyên lý

Sau khi xác định một milestone, phải hỏi:

> “Nước đi này đang thể hiện nguyên lý sản phẩm nào?”

Các framework cần ưu tiên:

- **x10**
- **Wrapper vs Moat**
- **Vertical AI**
- **Learning Loop**
- **Definition of Good**

Không dùng các nhãn chung chung như:

- “để tăng trưởng”
- “để giữ chân user”
- “để tăng doanh thu”

---

## 4.4. JTBD — Jobs To Be Done

JTBD mô tả **việc user thuê sản phẩm để hoàn thành**, không mô tả tính năng.

Sai:

> User cần AI chatbot.

Đúng:

> User muốn hoàn thành việc trả lời email khách hàng nhanh hơn.

Công thức đơn giản:

> Khi [bối cảnh], tôi muốn [hoàn thành việc gì], để [kết quả mong muốn].

---

## 4.5. Switching Cost — 4 Forces

Phân tích lý do user chuyển hoặc ở lại sản phẩm.

```text
                 PUSH
        Vấn đề với sản phẩm hiện tại
                  ↓
                  +
              PULL
       Sức hút của sản phẩm mới
                  ↓
        ─────────────────────
                  ↑
              INERTIA
          Thói quen cũ
                  +
              ANXIETY
        Lo ngại khi chuyển đổi
```

Cần xem xét:

- Data đã nằm trong sản phẩm chưa?
- User đã hình thành thói quen chưa?
- Workflow/team đã phụ thuộc chưa?
- Community/network có tạo lock-in không?
- Chuyển sang sản phẩm khác có tốn công không?

---

## 4.6. Wrapper vs Moat

**Wrapper mỏng:** giá trị chủ yếu là lớp giao diện/workflow trên một model mà model thế hệ sau có thể tự hấp thụ.

**Moat:** lợi thế khó bị model hoặc đối thủ sao chép, ví dụ:

- Proprietary data.
- Workflow sâu.
- Distribution.
- Community.
- Domain expertise.
- Network effects.
- Integration ecosystem.

Câu hỏi:

> Nếu model nền tảng ngày mai mạnh hơn rất nhiều, phần giá trị này còn tồn tại không?

---

## 4.7. Vertical AI

Vertical AI thường kết hợp:

```text
AI Expert
    +
Domain Expert
    ↓
Domain-specific AI product
```

Moat không nhất thiết nằm ở model mà có thể nằm ở **domain expertise + workflow + data + integration**.

---

## 4.8. AI Log

AI Log không chấm việc nhóm dùng AI nhiều hay ít.

Nó kiểm tra:

- AI đã làm phần nào?
- Nhóm tự quyết định phần nào?
- Nhóm kiểm chứng output AI như thế nào?

---

# 5. CP0 — Chọn sản phẩm & khai phá nguồn

**Thời lượng:** 10 phút.

## Mục tiêu

Chọn 1 sản phẩm có đủ dữ liệu để teardown.

## Điều kiện chọn

Sản phẩm phải:

1. Có AI đóng vai trò quan trọng.
2. Có đủ dữ liệu công khai để tìm ít nhất 6 milestone.
3. Có use case/JTBD tương đối rõ.

## Sản phẩm gợi ý

### Nhóm AI được tích hợp vào sản phẩm truyền thống

- Google Search
- Notion
- Canva
- Adobe Photoshop
- Grammarly
- Zoom
- Khan Academy
- Spotify
- Salesforce
- Figma

### Nhóm AI-native

- ChatGPT
- Claude
- Perplexity
- Cursor
- Lovable
- v0
- Replit
- NotebookLM
- Granola
- Midjourney
- ElevenLabs
- Suno
- Harvey
- Abridge
- Character.ai

## Nguồn nên tìm

Ưu tiên:

1. Official changelog.
2. Official product/company blog.
3. Product Hunt.
4. Founder/CEO posts.
5. Podcast/interview.
6. Hacker News.
7. Reddit/community.
8. G2/Capterra/App Store reviews.
9. Job postings.
10. Roadmap công khai.

## Nguyên tắc nguồn

Mọi milestone đưa vào memo phải có:

```text
Nguồn gốc
+
Link
+
Nhóm tự mở và kiểm chứng
```

Không chỉ dựa vào câu trả lời của AI.

## Output CP0

```text
Sản phẩm đã chọn:
...

Nguồn chính:
1. ...
2. ...
3. ...

Các milestone ứng viên:
1. ...
2. ...
3. ...
...
```

---

# 6. CP1 — Timeline & Revert nguyên lý

**Thời lượng:** 30 phút.

## Mục tiêu

Biến changelog thành **chuỗi quyết định sản phẩm**.

## Quy trình

### Bước 1 — Thu thập milestone

Từ các nguồn đã tìm, lập danh sách ứng viên.

### Bước 2 — Lọc

Chỉ giữ lại các quyết định có tác động lớn.

Mục tiêu:

> **6–8 milestone**

### Bước 3 — Phân tích context

Với mỗi milestone hỏi:

- Công ty đang ở giai đoạn nào?
- User đang có vấn đề gì?
- Đối thủ vừa làm gì?
- Model AI lúc đó mạnh đến đâu?
- Thị trường đang thay đổi như thế nào?

### Bước 4 — Revert nguyên lý

Hỏi:

> “Tại sao sản phẩm lại đưa ra quyết định này?”

Sau đó map vào framework đã học.

## Bảng chuẩn

| Thời điểm | Cập nhật | Context lúc đó | Nguyên lý | Nguồn |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |
| | | | | |
| | | | | |
| | | | | |

## Cách làm nhóm

Mỗi người phụ trách khoảng 2 milestone:

```text
Member A → Mốc 1–2
Member B → Mốc 3–4
Member C → Mốc 5–6
Member D → Mốc 7–8
```

Sau đó **cả nhóm review chéo toàn bộ**.

## CP1 cần đạt

- 6–8 milestone.
- Mỗi milestone có nguồn.
- Mỗi milestone có context.
- Mỗi milestone có nguyên lý cụ thể.
- Có giải thích vì sao loại các milestone khác.

---

# 7. CP2 — User & JTBD

**Thời lượng:** 15 phút.

## Mục tiêu

Xác định:

> Ai dùng sản phẩm và họ thuê sản phẩm để làm việc gì?

## 7.1. Early adopters

Không viết:

> Developer.

Nên viết cụ thể:

> Frontend developer tại startup nhỏ, đang dùng VS Code, thường xuyên thử công cụ AI coding và theo dõi cộng đồng AI.

Cần tìm:

- Họ là ai?
- Họ ở đâu?
- Họ gặp vấn đề gì?
- Tại sao họ thử sản phẩm sớm?

## 7.2. Tệp user hiện tại

Xác định:

- User hiện tại khác early adopter thế nào?
- Segment có mở rộng không?
- Milestone nào tạo ra sự dịch chuyển?

## 7.3. JTBD

Bảng phân tích:

| Tệp | Đặc điểm | JTBD | Cách cũ |
|---|---|---|---|
| Early adopters | | | |
| User hiện tại | | | |

JTBD phải mô tả **outcome/job**, không mô tả tính năng.

## 7.4. Segment shift

Dùng logic:

```text
Milestone
   ↓
Thay đổi sản phẩm
   ↓
Giải quyết JTBD mới
   ↓
Thu hút segment mới
```

## 7.5. Switching Cost

Phân tích 4 forces:

| Force | Câu hỏi |
|---|---|
| Push | Điều gì khiến user muốn rời sản phẩm hiện tại? |
| Pull | Điều gì hấp dẫn user sang sản phẩm mới? |
| Inertia | Thói quen nào khiến user không muốn đổi? |
| Anxiety | User lo ngại điều gì khi chuyển? |

## CP2 cần đạt

- Early adopter cụ thể.
- User hiện tại cụ thể.
- JTBD rõ.
- Cách cũ họ giải quyết job.
- Segment shift nối được với milestone.
- Phân tích đủ 4 forces.

---

# 8. CP3 — Ba dự đoán hướng đi

**Thời lượng:** 20 phút.

## Mục tiêu

Dự đoán hướng đi trong **6–12 tháng tới** dựa trên dữ liệu đã phân tích.

Không dự đoán kiểu:

> “Sản phẩm sẽ có thêm nhiều tính năng AI.”

Phải cụ thể.

## Các loại dự đoán

Có thể chọn:

1. Mở rộng tính năng.
2. Mở rộng segment.
3. Thay đổi mô hình kiếm tiền.
4. Phản ứng trước Big Tech.

## Công thức

```text
Dữ liệu quá khứ
     ↓
Pattern
     ↓
User/JTBD
     ↓
Giả định
     ↓
Dự đoán
```

## Template

### Dự đoán 1

**Loại:** ...

**Dự đoán:** Sản phẩm sẽ ...

**Lập luận:** Milestone ... cho thấy ...; tệp user ... có JTBD ...; do đó ...

### Dự đoán 2

**Loại:** ...

**Dự đoán:** ...

**Lập luận:** ...

### Dự đoán 3

**Loại:** ...

**Dự đoán:** ...

**Lập luận:** ...

## Câu hỏi phản biện

Với mỗi dự đoán hỏi:

> “Dựa vào milestone nào?”

> “Dựa vào segment/JTBD nào?”

> “Giả định nào nếu sai thì dự đoán này không còn đúng?”

## CP3 cần đạt

3 dự đoán:

- Cụ thể.
- Có thời hạn 6–12 tháng.
- Có lập luận.
- Dẫn ngược về CP1 và CP2.

---

# 9. CP4 — AI Log & Memo

**Thời lượng:** 15 phút.

## Mục tiêu

Hoàn thiện memo và khai báo trung thực việc sử dụng AI.

## AI Log

| Việc | AI làm hay nhóm làm? | Nhóm kiểm chứng/phán đoán lại thế nào? |
|---|---|---|
| Tìm/tổng hợp milestone | | |
| Tóm tắt context | | |
| Revert nguyên lý | | |
| Phân tích user | | |
| Viết JTBD | | |
| Đề xuất dự đoán | | |
| Hoàn thiện memo | | |

### Nguyên tắc

AI có thể:

- Tìm kiếm.
- Tóm tắt.
- Gợi ý pattern.
- So sánh.
- Hỗ trợ viết.

Nhưng nhóm phải chịu trách nhiệm:

- Chọn milestone.
- Kiểm chứng nguồn.
- Xác định nguyên lý.
- Xác định user/JTBD.
- Chọn dự đoán cuối cùng.

---

# 10. Template `memo.md`

```markdown
# Memo Teardown — [TÊN SẢN PHẨM]

**Nhóm:** ...
**Thành viên:** ...

## Vì sao chọn sản phẩm này

...

## §1. Timeline các cập nhật lớn

| Thời điểm | Cập nhật | Context lúc đó | Nguyên lý |
|---|---|---|---|
| | | | |
| | | | |

### Vì sao chọn những mốc này?

...

## §2. Tệp user & JTBD

| | Early adopters | Tệp hiện tại |
|---|---|---|
| Đặc điểm | | |
| JTBD chính | | |
| Trước đó họ làm bằng cách nào | | |

### Dịch chuyển tệp

...

### Switching cost — 4 forces

- Push:
- Pull:
- Inertia:
- Anxiety:

## §3. Ba dự đoán hướng đi — 6–12 tháng

### Dự đoán 1

**Loại:** ...

- **Dự đoán:** ...
- **Lập luận:** ...

### Dự đoán 2

**Loại:** ...

- **Dự đoán:** ...
- **Lập luận:** ...

### Dự đoán 3

**Loại:** ...

- **Dự đoán:** ...
- **Lập luận:** ...

## §4. AI Log

| Việc | AI làm hay nhóm làm? | Nhóm kiểm chứng/phán đoán lại thế nào? |
|---|---|---|
| | | |
| | | |
| | | |
```

---

# 11. Kế hoạch phân công nhóm 4 người

## Member 1 — Timeline researcher

Phụ trách:

- Official blog/changelog.
- Milestone 1–2.
- Source verification.

## Member 2 — Timeline + context

Phụ trách:

- Milestone 3–4.
- Context thị trường.
- Founder/company statements.

## Member 3 — User research

Phụ trách:

- Early adopters.
- Current users.
- Reviews/community.
- JTBD.
- Switching cost.

## Member 4 — Product/AI analysis

Phụ trách:

- Milestone 5–8.
- Revert nguyên lý.
- Framework comparison.

## Cả nhóm cùng làm

Bắt buộc làm chung:

- Chốt 6–8 milestone cuối.
- Chốt nguyên lý.
- Chốt segment/JTBD.
- Viết 3 dự đoán.
- Review memo.
- Chuẩn bị thuyết trình.

---

# 12. Timeline 2 giờ đề xuất

| Thời gian | Việc |
|---|---|
| 0:00–0:10 | CP0 — Chọn sản phẩm + nguồn |
| 0:10–0:40 | CP1 — Timeline + nguyên lý |
| 0:40–0:55 | CP2 — User + JTBD |
| 0:55–1:15 | CP3 — 3 dự đoán |
| 1:15–1:30 | CP4 — AI Log + memo |
| 1:30–2:00 | Slides + kiểm tra + chuẩn bị thuyết trình |

---

# 13. Checklist trước khi nộp

## Timeline

- [ ] Có 6–8 milestone.
- [ ] Mỗi milestone là quyết định sản phẩm lớn.
- [ ] Có thời điểm.
- [ ] Có context.
- [ ] Có nguyên lý.
- [ ] Có link nguồn gốc.
- [ ] Đã loại các milestone nhỏ.

## User & JTBD

- [ ] Early adopter cụ thể.
- [ ] User hiện tại cụ thể.
- [ ] JTBD viết theo job/outcome.
- [ ] Có cách cũ user dùng.
- [ ] Segment shift nối với milestone.
- [ ] Đã phân tích Push.
- [ ] Đã phân tích Pull.
- [ ] Đã phân tích Inertia.
- [ ] Đã phân tích Anxiety.

## Dự đoán

- [ ] Có đúng 3 dự đoán.
- [ ] Mỗi dự đoán cụ thể.
- [ ] Có phạm vi 6–12 tháng.
- [ ] Có lập luận.
- [ ] Lập luận dẫn về timeline.
- [ ] Lập luận dẫn về user/JTBD.
- [ ] Đã xác định giả định có thể làm dự đoán sai.

## AI Log

- [ ] Có ít nhất 3 hàng.
- [ ] Phân biệt AI và nhóm.
- [ ] Có cách kiểm chứng.
- [ ] Không nhận phần AI làm là phán đoán của nhóm.
- [ ] Không bỏ qua nguồn gốc.

## File

- [ ] `memo.md`
- [ ] `slides.pdf`

---

# 14. Tiêu chí chấm điểm

| Phần | Điểm |
|---|---:|
| Timeline + revert nguyên lý | 30 |
| User + JTBD + switching cost | 20 |
| 3 dự đoán | 30 |
| AI Log | 10 |
| Thuyết trình + thảo luận | 10 |
| **Tổng** | **100** |

## Trọng tâm để đạt điểm tốt

### Timeline — 30 điểm

Không cần nhiều milestone.

Quan trọng là:

> **Chọn đúng mốc + hiểu context + revert được nguyên lý.**

### User — 20 điểm

Không nói:

> “sinh viên”, “developer”, “dân văn phòng”.

Hãy mô tả thành **một người dùng cụ thể có bối cảnh và job rõ ràng**.

### Dự đoán — 30 điểm

Không cần dự đoán “đúng tương lai”.

Quan trọng là:

> **Dự đoán có logic và chứng minh được nó mọc ra từ dữ liệu của nhóm.**

### AI Log — 10 điểm

Không chấm việc dùng AI nhiều hay ít.

Chấm:

> **Minh bạch + kiểm chứng + ranh giới giữa AI và phán đoán của nhóm.**

---

# 15. Câu hỏi phản biện quan trọng

Trong quá trình làm, nhóm nên liên tục hỏi 7 câu này:

1. **Đây có thật sự là milestone hay chỉ là changelog?**
2. **Nguồn gốc của thông tin này ở đâu?**
3. **Context tại thời điểm đó là gì?**
4. **Quyết định này phản ánh nguyên lý nào?**
5. **User cụ thể nào đang được phục vụ?**
6. **User thuê sản phẩm để hoàn thành job gì?**
7. **Dự đoán này có thực sự mọc ra từ timeline + user không?**

---

# 16. Công thức ghi nhớ toàn bài

```text
TEARDOWN
   ↓
WHAT CHANGED?
   ↓
WHY DID IT CHANGE?
   ↓
WHICH PRINCIPLE?
   ↓
WHO USES IT?
   ↓
WHAT JOB ARE THEY HIRING IT FOR?
   ↓
WHY DO THEY STAY / SWITCH?
   ↓
WHAT COULD HAPPEN NEXT?
   ↓
WHY DO WE BELIEVE THAT?
```

Tóm lại, bài lab không yêu cầu nhóm **đoán tương lai một cách ngẫu nhiên**.

Logic đúng là:

```text
Nguồn công khai
      ↓
6–8 quyết định lớn
      ↓
Revert về nguyên lý
      ↓
Hiểu user + JTBD
      ↓
Hiểu switching cost
      ↓
Nhận ra pattern
      ↓
3 dự đoán có căn cứ
```

Đây chính là chuỗi lập luận mà giảng viên cần nhìn thấy trong `memo.md`.
