# Group Report — Day 02


## 1. Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
|---|---|---|---|
| 1 | Lê Văn Tuệ | 2A202601048 | Documentation, đề xuất candidate, tổng hợp workflow |
| 2 | Nguyễn Cảnh Hoàng | 2A202601588 | Research lead, phân tích evidence, validation |
| 3 | Hồ Trọng Hảo | 2A202601358 | Data analyst, thiết kế pilot, đánh giá metric |
| 4 | Trần Mạnh Hùng | 2A202601058 | Domain research, khảo sát người dùng, screening |
| 5 | Trương Đan Vi | 2A202601178 | Team lead, report, trình bày kết quả |
## 2. Nhật ký hội tụ

### Candidates và cluster

| Cluster | Candidates included | Pattern chung |
|---|---|---|
| Nghiên cứu/học tập | Literature review; đánh giá mức học bổng FPT | Đọc nhiều nguồn và đưa ra đánh giá có bằng chứng |
| Tuyển dụng | Custom CV theo JD; tinh chỉnh CV theo ngành | Mapping yêu cầu với bằng chứng trong hồ sơ |
| Báo cáo công việc | Daily standup; meeting action items | Gom activity rồi viết theo format lặp lại |
| Phân loại/vận hành | Tag review Shopee; theo dõi công nhân và tính lương | Chuyển dữ liệu thô thành tag/trạng thái/quyết định |

### Shortlist

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
|---|---|---|
| Literature Review | Impact cao, workflow rõ, có nhiều bước AI có thể hỗ trợ | Hallucination, bỏ sót bài, paywall, metric quality khó |
| Custom CV theo JD | Actor rõ, dễ pilot, lặp theo từng job | Không được bịa; callback chịu nhiều yếu tố ngoài CV |
| Daily Standup | Scope nhỏ, dễ đo và triển khai | Pain có thể nhỏ; template/rule có thể đã đủ |

### Score tạm thời


| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Literature Review | 4 | 5 | 3 | 4 | 4 | 5 | 4 | 29 |
| Custom CV theo JD | 5 | 5 | 3 | 4 | 5 | 5 | 4 | 31 |
| Daily Standup | 5 | 5 | 3 | 5 | 5 | 4 | 4 | 31 |

**Candidate chọn để deep-dive:** Literature Review cho nghiên cứu viên mới.

**Vì sao chọn:** Tuy điểm evidence hiện tại chưa cao nhất, đây là bài có impact chất lượng lớn nhất, có workflow search–screen–extract–synthesize rõ, và tạo được lập luận tốt về giới hạn của AI. Nhóm chọn để kiểm chứng sâu chứ chưa khẳng định đây là Problem Statement cuối.

**Vì sao chưa chọn hai bài còn lại:**

- Custom CV dễ pilot hơn nhưng tác động đến callback khó quy hoàn toàn cho CV.
- Daily Standup dễ làm nhưng template/form có thể giải phần lớn pain; cần chứng minh AI tạo thêm giá trị.

**Disagreement:** không có

## 3. Quick validation

### Kế hoạch và trạng thái

| Nguồn | Số người / mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Interview nghiên cứu viên/học viên cao học | Mục tiêu 3, hiện 0 | Chưa có dữ liệu | Chưa có dữ liệu | Chưa được phép khẳng định baseline |
| Pilot bộ paper | Mục tiêu 20 bài | Chưa chạy | Chưa chạy | Giữ metric là target, không gọi là kết quả |
| Research nguồn công khai | 4 nguồn chính thức | Existing tools hỗ trợ search, screening, extraction, citation management | Công cụ không loại bỏ nhu cầu kiểm nguồn và ra quyết định của researcher | Thu hẹp về AI-assisted workflow có human review |

### Câu hỏi interview

1. Lần gần nhất bạn làm literature review là khi nào, trong lĩnh vực nào?
2. Bao nhiêu bài được tìm thấy, screen và đọc full text?
3. Bước nào mất nhiều thời gian nhất? Bạn có log hoặc ước lượng bao lâu?
4. Bạn đang dùng database, Zotero/spreadsheet hoặc công cụ AI nào?
5. Lỗi nào có hậu quả lớn nhất: bỏ sót bài, trích sai, citation sai hay synthesis thiên lệch?
6. Bạn có chấp nhận AI hỗ trợ bước nào và bắt buộc tự kiểm bước nào?

## 4. Research giải pháp đã có

| Nguồn / tool / pattern | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học |
|---|---|---|---|---|---|
| Elicit Literature Review | https://support.elicit.com/en/articles/14757967-why-elicit-is-different-from-other-research-tools | Semantic + keyword search, abstract summary, filter, custom extraction columns, export | Hỗ trợ nhiều bước trong evidence table | Kết quả AI vẫn phải kiểm với paper; coverage phụ thuộc corpus/full text | Không cần build toàn bộ từ đầu; pilot workflow và đo trên domain thật |
| Elicit Reports | https://orion.elicit.com/solutions/reports | Search, screening, eligibility, synthesis có audit trail | Cho phép xem lựa chọn paper và evidence | Không thay protocol và phán đoán học thuật | Provenance/audit trail phải là yêu cầu cốt lõi |
| Zotero | https://www.zotero.org/ | Thu thập, tổ chức, annotate, cite và chia sẻ nguồn | Citation management, tag/collection, bibliography | Không tự đánh giá relevance hoặc viết synthesis | Dùng rule/tool truyền thống cho metadata/citation; AI không cần ôm hết |
| PRISMA 2020 | https://www.prisma-statement.org/prisma-2020 | Checklist và flow diagram cho báo cáo systematic review | Tăng minh bạch và khả năng tái lập | Là guideline báo cáo, không tự thực hiện review | Workflow phải lưu query, tiêu chí, quyết định include/exclude và số lượng từng bước |

**Research takeaway:**
Phương án hợp lý là workflow tuyến tính có audit trail: rule/tool quản lý metadata và loại trùng; AI hỗ trợ query, ưu tiên screening, extraction và draft; researcher quyết định inclusion/exclusion, kiểm evidence và duyệt synthesis. Chưa có lý do để cho một Agent tự lập kế hoạch và tự xuất bản.

## 5. Current workflow

```text
CURRENT STATE — baseline cần đo

[1 Researcher đặt câu hỏi + keyword]
→ [2 Search từng database]
→ [3 Export citation, gộp và loại trùng]
→ [4 Screen title/abstract]                 <-- bottleneck 1
→ [5 Tìm/đọc full text]
→ [6 Trích dữ liệu vào spreadsheet]         <-- bottleneck 2
→ [7 Nhóm theme + so sánh]
→ [8 Viết synthesis + kiểm citation]
```

| Bước | Actor | Input | Output | Thời gian/tần suất | Ghi chú |
|---|---|---|---|---|---|
| 1 | Researcher | Research question | Query + criteria v0 | Cần đo | Chất lượng query ảnh hưởng toàn flow |
| 2 | Researcher | Query | Danh sách kết quả | Theo từng database | Cần lưu search log |
| 3 | Researcher/tool | Citation export | Bộ record đã loại trùng | Cần đo | Rule/tool thường đủ |
| 4 | Researcher | Title/abstract + criteria | Include/exclude/maybe | Cần đo | Bottleneck; quyết định có tính học thuật |
| 5 | Researcher | Danh sách include/maybe | Full text đủ điều kiện | Cần đo | Có paywall/thiếu PDF |
| 6 | Researcher | PDF + extraction schema | Evidence table | Cần đo | Bottleneck; dễ chép sai |
| 7 | Researcher | Evidence table | Theme/gap/contradiction | Cần đo | Cần judgment |
| 8 | Researcher | Outline + evidence | Review có citation | Cần đo | Chịu trách nhiệm cuối |

**Bottleneck chính:** screening và trích xuất evidence. Chưa đủ dữ liệu để chọn một trong hai là bottleneck lớn nhất.

## 6. Future workflow

```text
FUTURE STATE — pilot có kiểm soát

[1 Researcher chốt question + protocol]
→ [2 AI gợi ý query; researcher duyệt]
→ [3 Rule chạy search log + de-duplicate]
→ [4 AI xếp hạng/suggest screening]
→ [5 Researcher quyết định include/exclude]       <-- human boundary
→ [6 AI trích field + quote/page/confidence]
→ [7 Researcher đối chiếu PDF, duyệt evidence]    <-- human boundary
→ [8 AI draft synthesis từ evidence đã duyệt]
→ [9 Researcher sửa, kiểm citation và phát hành]  <-- owner

Fallback:
- Không có full text/confidence thấp → manual-review queue.
- Không truy được claim về PDF → không cho vào synthesis.
- Kết quả pilot kém hơn threshold → quay về Zotero + spreadsheet + protocol.
```

### Before/after impact

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Tổng thời gian cho pilot 20 bài | Đo ở lượt manual | Giảm ≥50% | So cùng bộ bài và extraction schema |
| Bước | 8 | 9 | Thêm checkpoint; không tối ưu bằng cách bỏ kiểm soát |
| Bước thủ công hoàn toàn | 8/8 | 4/9 | Researcher vẫn quyết định và duyệt |
| Traceable claims | Đo baseline | 100% | DOI/URL + quote/page |
| Screening recall | Đo trên gold set | ≥90% | Threshold pilot, cần domain expert chốt |
| Risk mới | Sai sót thủ công | Hallucination, automation bias, privacy/copyright | Có audit log và rollback |

## 7. Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Học viên cao học/nghiên cứu viên mới viết literature review. |
| **Workflow** | Đặt query → search → loại trùng → screen → đọc full text → extract → synthesize → cite. |
| **Bottleneck** | Screening và extraction thủ công từ nhiều bài, phải quay lại PDF để xác minh. |
| **Impact** | Tốn nhiều buổi làm việc và có nguy cơ bỏ sót nguồn/trích sai; baseline chưa được đo. |
| **Success Metric** | Giảm ≥50% thời gian trên pilot 20 bài; recall ≥90%; 100% claim truy ngược được; không có citation bịa. |
| **Boundary** | AI không tự đặt tiêu chí cuối, không tự loại bài ở case không chắc, không viết claim ngoài evidence đã duyệt, không tự phát hành. |

### Lỗ hổng của v0

- Actor còn rộng; cần chọn lĩnh vực và loại review.
- Baseline chưa có interview/log.
- Recall threshold cần chuyên gia domain xác nhận.
- Chưa xác nhận quyền sử dụng/upload full-text PDF.

## 8. Rule / Workflow / Agent

**Ma trận:** độ phức tạp cao (nhiều nguồn, nhiều bước), độ mơ hồ cao (relevance và synthesis cần judgment). Tuy vậy, đường đi chính vẫn xác định được nên chưa cần Agent tự quyết định động.

| Mức | Phương án | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| Rule | Query template + Zotero + de-duplicate + extraction sheet | Review nhỏ, tiêu chí rõ, nhân lực đủ | Không giảm nhiều công đọc/tổng hợp | Dùng làm nền |
| Workflow | Rule quản lý record → AI suggest/extract/draft → researcher duyệt | Các bước tuyến tính, có protocol và checkpoint | Hallucination, automation bias | **Chọn cho pilot** |
| Agent | Tự đổi query, gọi database, quyết định bài, viết review | Chỉ khi quyền, evaluation và nhánh xử lý đã rất rõ | Scope/permission lớn, khó audit, sai sót lan truyền | Chưa chọn |

**Vì sao không chỉ chọn Rule:** Rule giải tốt metadata, format và de-duplicate nhưng không xử lý tốt semantic relevance, extraction từ văn bản và synthesis.

**Vì sao không chọn Agent:** Pilot chưa có baseline, gold set, quyền truy cập và evaluation đủ mạnh; workflow không cần AI tự quyết định inclusion hoặc tự phát hành.

## 9. Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | Nghiên cứu viên mới thực hiện một literature review nhỏ trong lĩnh vực nhóm sẽ chọn sau interview. |
| **Workflow** | Protocol → search/log → de-duplicate → screen → full text → evidence table → synthesis → citation check. |
| **Bottleneck** | Screen và trích xuất evidence từ nhiều paper; mỗi quyết định/claim cần truy về nguồn gốc. |
| **Impact** | Baseline chưa xác nhận; giả thuyết là nhiều giờ thao tác và nguy cơ bỏ sót/trích sai. |
| **Success Metric** | Pilot 20 bài: giảm ≥50% thời gian so với manual; recall ≥90% trên gold set; 100% claim có provenance; 0 citation bịa. |
| **Boundary** | Chỉ dùng nguồn được phép; AI không quyết định inclusion cuối, không suy đoán khi thiếu PDF, không tạo claim ngoài evidence, không tự phát hành. |
| **AI intervention point** | Sau khi protocol được duyệt: gợi ý query, xếp hạng screening, extraction có quote/page, draft từ evidence đã duyệt. |
| **Mức chọn** | Workflow. |
| **Rủi ro & người thật kiểm tra** | Hallucination, bỏ sót paper, automation bias, privacy/copyright. Researcher kiểm screening, PDF, claim và citation. |

## 10. Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
|---|---|---|
| Actor và workflow đã rõ? | Not Yet | Cần thu hẹp lĩnh vực/loại review |
| Baseline và success metric đã đo? | Not Yet | Có target nhưng chưa có baseline/gold set |
| Có data/input đủ dùng? | Not Yet | Cần 20 paper hợp lệ và quyền sử dụng |
| Nếu AI sai, hậu quả chấp nhận được? | Yes, trong pilot | Không xuất bản; researcher kiểm mọi output |
| Có người review/owner? | Yes | Researcher là owner |
| Có cách non-AI đơn giản hơn? | Yes | Zotero + protocol + spreadsheet là baseline/fallback |
    
**Decision: NOT YET — được phép chạy pilot nội bộ, chưa Go cho workflow thật.**

**Lý do:** Workflow và boundary đã rõ nhưng chưa có evidence người dùng, baseline, gold set và xác nhận quyền đối với full text. Chọn “Go” lúc này sẽ dựa trên giả định thay vì kiểm chứng.

### Cần validate trước khi Go

1. Phỏng vấn 3 researcher và chọn một domain cụ thể.
2. Tạo bộ 20 paper có nhãn relevance và evidence table chuẩn do researcher duyệt.
3. Chạy manual baseline và AI-assisted workflow trên cùng bộ dữ liệu.
4. Đo thời gian, recall, extraction accuracy, provenance coverage và số lỗi.
5. Xác nhận chính sách dữ liệu/copyright trước khi upload PDF.

### Pilot nhỏ nhất

- Scope: 1 research question, 20 paper, 3–5 extraction fields.
- Không tích hợp database/API; researcher cung cấp record/PDF được phép dùng.
- AI chỉ suggest; không auto-exclude và không publish.
- Hai lượt: manual trước, assisted sau; lưu log mọi quyết định.

### Exit / rollback

- Recall dưới 90% hoặc bỏ sót một paper quan trọng → dừng auto-prioritization.
- Có citation bịa/claim không truy nguồn → dừng draft synthesis.
- Researcher phải sửa trên 50% extraction field → quay về spreadsheet manual, chỉ giữ query/de-duplicate rule.
- Không xác nhận được quyền dùng PDF → chỉ dùng title/abstract/metadata hợp lệ.

