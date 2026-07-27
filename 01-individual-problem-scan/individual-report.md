# 01 — Individual Problem Scan

Case: **5 chủ đề đời sống/công việc dưới lăng kính hệ thống & AI**

Actor scan gồm nhiều actor khác nhau (nhân viên, người tìm việc, người nội trợ, người chơi xổ số, người dùng cộng đồng) vì bài scan gốc phân tích 5 bài toán độc lập, mỗi bài toán đã tự có sẵn 4 lăng kính riêng (lặp lại, tốn thời gian, điểm đau, giải pháp AI).

## Scan rộng

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Viết Daily Standup/báo cáo công việc mỗi cuối ngày hoặc đầu giờ sáng | Nhân viên, PM, người duy trì journaling | 15–30 phút/ngày để nhớ lại và viết |
| 2 | Tốn thời gian | Quyết định tối nay nấu món gì từ nguyên liệu sẵn có | Người tự nấu ăn sau giờ làm | 20–30 phút mỗi ngày vào 17h–19h, vẫn không quyết được |
| 3 | Lặp lại | Tùy chỉnh CV theo từng Job Description khi ứng tuyển | Người đang tìm việc | Hàng giờ đến hàng ngày cho mỗi lần ứng tuyển |
| 4 | Tốn thời gian | Soi cầu / phân tích xác suất kết quả xổ số Miền Bắc | Người chơi xổ số | Nhiều giờ tra cứu, ghi chép mỗi ngày lúc 18h30 |
| 5 | Pain từ cộng đồng | Spam bình luận để lấy XP trên các nền tảng gamification | Người dùng cá nhân và cộng đồng | Hàng chục–hàng trăm lượt bấm máy/ngày, nguy cơ bị khóa tài khoản |

Vì sao phần scan này mạnh:

- Có 5 problem đến từ 5 bối cảnh sống khác nhau, không dồn hết vào một actor.
- Mỗi problem đều có actor cụ thể và dấu hiệu thời gian/tần suất thật, không mơ hồ.
- Không bắt đầu bằng "làm app AI nấu ăn" hay "làm bot xổ số" — vẫn mô tả đúng bản chất bài toán trước khi nói tới giải pháp.
- Có cả problem mà AI giới hạn rõ ràng (xổ số) và problem có rủi ro đạo đức (spam XP), giúp phần Top 3 chọn lọc có cơ sở loại bớt.

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Viết Daily | Actor rõ, workflow lặp lại mỗi ngày, bottleneck cụ thể (nhớ lại + chọn lọc thông tin), dễ đo thời gian trước/sau | "Chất lượng report tốt" đo bằng gì ngoài thời gian |
| 2 | Viết CV theo JD | Actor rõ, pain có thật (không định lượng được thành tích, dễ bị ATS loại), workflow lặp lại theo từng job | Hiệu quả thật (tỷ lệ được gọi phỏng vấn) chịu ảnh hưởng nhiều yếu tố ngoài CV |
| 3 | Tối nay nấu gì | Pain rất phổ biến, có "decision fatigue" rõ, diễn ra đều đặn 365 ngày/năm | "Món ăn phù hợp" là tiêu chí cá nhân, khó có metric thống nhất giữa nhiều người dùng |

**Vì sao 2 problem còn lại không vào Top 3:**
- *Soi cầu xổ số*: bản chất là hệ thống ngẫu nhiên độc lập, chính tài liệu gốc cũng nêu rõ AI không thể dự đoán số trúng — impact của AI chỉ dừng ở thống kê, không giải quyết được bài toán gốc của người dùng.
- *Spam lấy XP*: pain có thật nhưng hành vi cốt lõi (spam để trục lợi điểm ảo) mang tính tiêu cực với cộng đồng; nếu build giải pháp cho "người tạo giá trị" thì lại gần với bài toán viết bình luận chất lượng hơn là bài toán spam ban đầu, nên cần định nghĩa lại actor trước khi chọn.

## Problem Card #1 — Viết Daily

**Problem 1 câu:**
Mỗi cuối ngày (hoặc đầu giờ sáng hôm sau), người viết mất 15–30 phút để nhớ lại, chọn lọc và viết lại các hoạt động trong ngày thành báo cáo/daily journal có cấu trúc.

**Actor:**
Nhân viên/PM cần gửi Daily Standup report cho cấp trên, hoặc cá nhân duy trì thói quen journaling hằng ngày.

**Thời điểm / bối cảnh:**
Cuối giờ làm việc hoặc đầu giờ sáng hôm sau, trước khi bắt đầu công việc mới.

**Current workflow:**

```text
1. Mở lại lịch làm việc, Trello/Jira/Notion để xem đã làm gì
2. Nhớ lại các việc vặt không nằm trong hệ thống
3. Chọn lọc thông tin quan trọng, bỏ bớt chi tiết thừa
4. Viết thành văn bản theo format quen thuộc
5. Gửi/đăng báo cáo
```

**Bottleneck:**
Bước 2–3 — nhớ lại và chọn lọc thông tin. Viết chi tiết thì tốn thời gian, viết sơ sài thì cấp trên không nắm được tiến độ; dễ quên việc vặt vì không ghi log theo thời gian thực.

**Impact:**
15–30 phút/ngày, khoảng 75–150 phút/tuần cho một cá nhân. Với một team nhiều người, tổng chi phí thời gian nhân lên đáng kể; ngoài ra có rủi ro bỏ dở thói quen giữa chừng vì thiếu kiên trì.

**Success metric:**
Giảm thời gian viết report xuống dưới 5 phút, vẫn giữ đủ 3 phần (Việc đã hoàn thành – Việc đang tắc nghẽn – Kế hoạch ngày mai) mà cấp trên không phải hỏi lại.

**Non-AI alternative:**
Template cố định 3 mục (Done – Blocked – Next) giúp giảm phần định dạng, nhưng không giải quyết được việc tự nhớ lại và chọn lọc thông tin thô.

**AI hypothesis:**
AI đọc note thô (chat nhanh, task log, voice note) trong ngày và tự động nhóm thành 3 khung chuẩn; người dùng chỉ cần review/chỉnh sửa trước khi gửi.

**Quick gut:**
Workflow.

### Draft current workflow

```text
CURRENT STATE — 15-30 phút

[1 Mở lịch/tool xem việc đã làm: 5']
→ [2 Nhớ lại việc vặt: 5-10']        <-- bottleneck
→ [3 Chọn lọc thông tin: 5-10']      <-- bottleneck
→ [4 Viết thành văn bản: 5']
→ [5 Gửi/đăng báo cáo: 2']
```

### Draft future workflow

```text
FUTURE STATE — dưới 5 phút

[1 Note thô trong ngày: song song với công việc, không tốn thêm thời gian riêng]
→ [2 AI nhóm thành 3 khung Done-Blocked-Next: 1']
→ [3 Người dùng review + chỉnh sửa: 3']   <-- human boundary
→ [4 Gửi/đăng: 1']

Fallback: AI nhóm sai/thiếu ý → người dùng tự bổ sung thủ công trước khi gửi.
```

## Problem Cards #2 và #3 — tóm tắt

| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| Viết CV theo JD | Người đang tìm việc | Định lượng thành tích + khớp từ khóa với JD | Hàng giờ/CV → vài chục phút/CV | Workflow | Actor rõ nhưng hiệu quả thật (tỷ lệ được gọi phỏng vấn) khó quy hoàn toàn cho CV |
| Tối nay nấu gì | Người tự nấu ăn sau giờ làm | Ra quyết định giữa nhiều biến số (nguyên liệu, thời gian, decision fatigue) | 20-30 phút → dưới 5 phút | Workflow | Pain có thật nhưng "món ăn phù hợp" là tiêu chí cá nhân, khó có metric thống nhất |

---