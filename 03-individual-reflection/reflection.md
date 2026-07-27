# 03 — Individual Reflection Example

## Đóng góp của tôi trong nhóm

| Hoạt động | Tôi đã làm gì? | Kết quả |
|---|---|---|
| Scan cá nhân | Đưa ra các ý tưởng candidate ban đầu | Nhóm có thêm candidate ở các mảng nghiên cứu, tuyển dụng, vận hành |
| Pitch | Pitch bài toán Literature Review cho nghiên cứu viên | Bài được nhóm chọn vào shortlist để deep-dive |
| Challenge | Hỏi nhóm về baseline thực tế và rủi ro hallucination | Nhóm nhận diện rõ lỗ hổng và hạ từ "Go" xuống "Not Yet" để validate thêm |
| Workflow | Tham gia vẽ current/future workflow cho Literature Review | Nhóm chốt được các nút thắt (bottleneck) ở bước screening và extraction |
| Research | Tìm hiểu Elicit, Zotero và tiêu chuẩn PRISMA 2020 | Nhóm thấy rõ bức tranh giải pháp, không cần build agent từ đầu |
| Rule / Workflow / Agent | Lập luận chọn Workflow, không chọn Agent | Nhóm thống nhất decision: cần có human boundary (người thật duyệt) |

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì |
|---|---|---|---|---|
| Scan | Gợi ý thêm problems theo góc nhìn của researcher | Giúp hệ thống hóa các bước như search, screen, extract | Gợi ý vài quy trình quá vĩ mô, thiếu tính khả thi | Bỏ các ý không có workflow thực tế để thu hẹp scope |
| Workflow | Nhờ AI chuyển mô tả thành Mermaid | Nhanh hơn khi phác thảo sơ đồ flow | AI gộp nhầm bước AI trích xuất với bước researcher duyệt | Tách lại rõ ràng vì bắt buộc phải có checkpoint của con người |
| Research | Tìm tool tương tự trên thị trường | Gợi ý nhanh các tool học thuật như Elicit, Zotero | Có claim về % tiết kiệm thời gian không rõ nguồn | Chỉ giữ link chính thức và các tính năng cốt lõi (audit trail) |
| Problem Statement | Nhờ AI phản biện field mơ hồ | Chỉ ra metric recall và baseline hiện tại chưa có data | AI đề xuất làm Agent tự động hóa toàn bộ | Kéo nhóm về mức Workflow để kiểm soát rủi ro sai citation |

## Bài học của tôi

- Problem tốt không phải problem nghe "AI" nhất, mà là problem có workflow tuyến tính và metric đo lường rõ.
- Vẽ workflow chi tiết giúp thấy rõ điểm nào AI làm tốt (draft/extract), điểm nào bắt buộc con người phải giữ quyền quyết định (human boundary).
- Agent không phải đích đến mặc định. Trong case này, Workflow hợp lý hơn vì cần tính minh bạch (audit trail) và researcher phải chịu trách nhiệm cuối cùng.
- Research không phải để copy tool, mà để thấy pattern: các sản phẩm nghiên cứu tốt đều để AI hỗ trợ xử lý khối lượng lớn, còn người thật chốt tính học thuật.

Nếu làm lại:

```text
Tôi sẽ thúc đẩy nhóm đi phỏng vấn các nghiên cứu viên thực tế sớm hơn để có baseline và gold set cụ thể, thay vì chỉ dựa vào các target giả định cho đợt pilot.