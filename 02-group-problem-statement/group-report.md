# 02 — Group Problem Statement

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
| 1 | Trương Minh Hoàng | 2A202601262 | Người trình bày, tổng hợp problem, vẽ workflow |
| 2 | Đào Trung Hiếu | 2A202601238 | Người góp ý, challenge candidate, research giải pháp và kiểm chứng |
| 3 | Phan Văn Hoàng Nam | 2A202601160 | Người viết Problem Statement, tổng hợp quyết định cuối (Final Decision) và hoàn thiện báo cáo |

## 01 — Individual problem scan của nhóm

Nhóm tổng hợp từ top 3 cards của các thành viên. Ba candidate nổi bật là:

| # | Candidate problem | Actor | Bottleneck |
| 1 | Kiểm tra bài lab trước khi nộp | Sinh viên làm lab | Đối chiếu thủ công giữa nhiều tài liệu và repo mất nhiều thời gian |
| 2 | Gặp lỗi khi cài đặt công cụ hoặc làm bài | Sinh viên, đặc biệt là người mới | Câu hỏi ban đầu thiếu context, phải trao đổi thêm nhiều lần |
| 3 | Tổng hợp nhận xét báo cáo nhóm | Thành viên phụ trách báo cáo | Comment nằm rải rác, cần đọc lại nhiều nguồn để tổng hợp đúng |

## 02 — Shortlist và chọn candidate

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
| Kiểm tra bài lab trước khi nộp | Cụ thể, lặp lại trước mỗi deadline, có workflow rõ, và có thể đo bằng thời gian và tỷ lệ phát hiện lỗi | Cần xác định rõ phạm vi: kiểm tra file/folder/heading hay cả chất lượng nội dung |
| Xử lý lỗi công cụ và môi trường | Pain thật, ảnh hưởng đến nhiều người, có thể so sánh Rule/Workflow/Agent | Scope có thể rộng vì phụ thuộc vào nhiều lỗi khác nhau và môi trường kỹ thuật |
| Tổng hợp comment báo cáo nhóm | Workflow rõ, có thể dùng AI để nhóm comment, phù hợp với việc hỗ trợ ngôn ngữ | Cần làm rõ nguồn dữ liệu và cách xác nhận comment nào đã được xử lý |

Chúng tôi chọn candidate:

**Kiểm tra bài lab trước khi nộp.**

Vì sao chọn:

- Candidate có actor rõ: sinh viên làm lab và nộp bài.
- Workflow hiện tại có thể vẽ được và lặp lại trước mỗi deadline.
- Bottleneck là một bước cụ thể: phải đối chiếu thủ công giữa README, worksheet, bài mẫu và repo.
- Impact có thể đo bằng thời gian kiểm tra và số lỗi bị bỏ sót.
- Không quá rộng cho mục tiêu lab: tập trung vào việc kiểm tra cấu trúc và nội dung cơ bản trước khi nộp.

Vì sao không chọn candidate khác:

- Xử lý lỗi công cụ có nhiều biến thể môi trường, nên scope dễ mở rộng quá mức và khó đo chuẩn.
- Tổng hợp comment báo cáo nhóm là vấn đề tốt nhưng phụ thuộc nhiều vào nhiều nguồn và quy trình nhóm, chưa đủ trực tiếp cho pilot nhỏ.

## 03 — Quick validation

Nhóm đã thử kiểm chứng nhanh với 3 người quen hoặc đồng nghiệp:

| Nguồn | Số người | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
| Hỏi nhanh 3 sinh viên làm lab | 3 | 2/3 người đã từng mất thời gian để kiểm tra lại README, worksheet và cấu trúc repo trước khi nộp | 1 người cho rằng phần này chỉ cần checklist đơn giản hơn | Thu hẹp scope: không phải “tự chấm toàn bộ bài”, mà là “kiểm tra các file/heading/yêu cầu bắt buộc trước khi nộp”. |
| Quan sát cá nhân | 1 | Tôi đã phải mở nhiều file và đối chiếu thủ công trước khi nộp | N/A | Xác nhận bottleneck nằm ở bước đối chiếu và phát hiện thiếu sót. |

## 04 — Research giải pháp đã có

| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
| GitHub Actions / pre-commit checks | https://github.com/features/actions | Tự động chạy kiểm tra cấu trúc và rule trong repo | Hữu ích cho việc check file, lint, format | Không tự hiểu đầy đủ yêu cầu ngữ nghĩa trong README/worksheet | Rule/script phù hợp cho phần cấu trúc, nhưng chưa thay thế việc đánh giá chất lượng nội dung |
| Markdownlint / repo linter | https://github.com/DavidAnson/markdownlint | Kiểm tra markdown, heading, cấu trúc file | Nhanh, có thể dùng ngay với repo | Chỉ giải quyết phần định dạng, chưa kiểm tra toàn bộ yêu cầu bài lab | Có thể dùng làm phần đầu tiên của workflow kiểm tra |
| Notion AI / Gemini in Docs | https://www.notion.so/product/ai | Tóm tắt và đối chiếu nội dung theo ngữ cảnh | Giúp tóm tắt yêu cầu và gợi ý phần còn thiếu | Có khả năng suy luận quá mức hoặc hiểu sai ngữ cảnh | AI phù hợp để hỗ trợ gợi ý, nhưng người thật vẫn phải review |

Research takeaway:

- Rule/script có giá trị lớn cho việc kiểm tra cấu trúc, tên file và cấu trúc folder.
- AI chỉ nên hỗ trợ ở bước tóm tắt yêu cầu và gợi ý các mục còn thiếu, không nên tự quyết toàn bộ kết quả.
- Workflow tốt nhất là kết hợp rule + AI + người dùng review trước khi nộp.

## 05 — Workflow before/after

CURRENT STATE — 6 bước, 15–20 phút

1. Mở README để xem cấu trúc bài nộp.
2. Mở worksheet để kiểm tra các nội dung bắt buộc.
3. Mở bài mẫu để đối chiếu cách trình bày.
4. Mở từng folder/file trong repo để kiểm tra.
5. Đối chiếu từng yêu cầu với bài làm.
6. Ghi lại phần còn thiếu hoặc sai và sửa lại.

Bottleneck chính:

- Bước 4 và 5: phải chuyển qua lại giữa nhiều tài liệu và repo để đối chiếu thủ công; dễ bỏ sót field hoặc sai cấu trúc.

FUTURE STATE — 5 bước, dưới 10 phút

1. Hệ thống quét repo theo checklist từ README và worksheet. -- Rule/script
2. Hệ thống kiểm tra tên file, cấu trúc folder và heading bắt buộc. -- Rule/script
3. AI tóm tắt các yêu cầu còn thiếu và gợi ý nội dung cần bổ sung. -- Workflow step
4. Sinh viên rà soát và sửa các mục còn thiếu. -- Human boundary
5. Sinh viên xác nhận trước khi nộp. -- Human boundary

Fallback:

- Nếu script không đọc được repo hoặc phát hiện sai, sinh viên quay lại kiểm tra thủ công bằng README và worksheet.
- Nếu AI gợi ý chưa rõ, sinh viên vẫn mở trực tiếp file gốc để kiểm tra.

Before/after impact:

| Metric                  |              Trước |                         Sau kỳ vọng | Ghi chú                                |
| ----------------------- | -----------------: | ----------------------------------: | -------------------------------------- |
| Tổng thời gian kiểm tra |         15–20 phút |                        Dưới 10 phút | Giảm thời gian đáng kể trước deadline  |
| Số bước thủ công        |                  6 |                                 3–4 | Giảm số lần chuyển đổi giữa nhiều file |
| Bottleneck chính        | Đối chiếu thủ công |     Review và sửa các mục còn thiếu |                                        |
| Risk mới                |     Bỏ sót yêu cầu | AI gợi ý sai hoặc chưa đủ chính xác | Cần người dùng review                  |

## 06 — Problem Statement v0

| Field              | Nội dung                                                                                                                                                     |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Actor**          | Sinh viên làm lab và cần nộp bài đúng cấu trúc, đầy đủ yêu cầu.                                                                                              |
| **Workflow**       | Trước khi nộp, sinh viên mở README, worksheet, bài mẫu và repo, sau đó đối chiếu từng yêu cầu để kiểm tra phần còn thiếu hoặc sai.                           |
| **Bottleneck**     | Đối chiếu thủ công giữa nhiều tài liệu và nhiều file mất nhiều thời gian và dễ bỏ sót.                                                                       |
| **Impact**         | Mỗi lần kiểm tra tốn khoảng 15–20 phút; lỗi về file/folder/heading có thể bị phát hiện quá muộn, làm chậm việc nộp bài.                                      |
| **Success Metric** | Giảm thời gian kiểm tra xuống dưới 10 phút; phát hiện được hầu hết lỗi về tên file, cấu trúc folder và heading bắt buộc; giảm số lần sửa lại trước deadline. |
| **Boundary**       | Không tự thay đổi nội dung bài làm; chỉ hỗ trợ kiểm tra, gợi ý và nhắc các mục còn thiếu.                                                                    |

## 07 — Rule / Workflow / Agent

| Mức          | Phương án cho bài toán nhóm                                                                | Khi nào đủ                                                            | Rủi ro                                                              | Chọn?                  |
| ------------ | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------- | ------------------------------------------------------------------- | ---------------------- |
| **Rule**     | Checklist và script kiểm tra cấu trúc repo theo README/worksheet                           | Đủ nếu mục tiêu chỉ là phát hiện file, folder và heading bắt buộc     | Không đủ để hiểu toàn bộ ngữ nghĩa yêu cầu hoặc chất lượng nội dung | Không chọn làm toàn bộ |
| **Workflow** | Rule/script kiểm tra cấu trúc → AI tóm tắt/đề xuất mục còn thiếu → sinh viên review và sửa | Hợp vì quy trình rõ ràng, có bước tự động và bước người dùng kiểm tra | AI có thể gợi ý chưa chính xác hoặc hiểu sai ngữ cảnh               | Có                     |
| **Agent**    | Agent tự quét repo, tự suy luận yêu cầu và tự sửa bài làm                                  | Chỉ cần nếu workflow phức tạp và cần nhiều bước tự động hóa liên tục  | Quá rộng cho scope lab, dễ gây sai sót và mất kiểm soát             | Chưa                   |

Mức chọn:

Workflow.

Vì sao:

- Rule đơn thuần đủ cho việc kiểm tra cấu trúc nhưng chưa giải quyết được phần ngữ nghĩa và chất lượng nội dung.
- AI phù hợp để hỗ trợ tóm tắt và gợi ý phần còn thiếu, nhưng không nên tự quyết toàn bộ kết quả.
- Sinh viên vẫn giữ vai trò review và sửa đổi trước khi nộp.

## 08 — Problem Statement v1

| Field                            | Nội dung                                                                                                                           |
| -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Actor**                        | Sinh viên làm lab muốn nộp bài đúng cấu trúc và đầy đủ yêu cầu trước deadline.                                                     |
| **Workflow**                     | Kiểm tra README → worksheet → bài mẫu → repo → đối chiếu yêu cầu → sửa lại trước khi nộp.                                          |
| **Bottleneck**                   | Đối chiếu thủ công giữa nhiều tài liệu và nhiều file mất nhiều thời gian và dễ bỏ sót.                                             |
| **Impact**                       | Mỗi lần kiểm tra mất khoảng 15–20 phút; nếu lặp lại nhiều lần, thời gian chuẩn bị bài nộp bị kéo dài và nguy cơ sai cấu trúc tăng. |
| **Success Metric**               | Giảm thời gian kiểm tra xuống dưới 10 phút và giảm số lỗi về tên file, folder, heading hoặc field bắt buộc.                        |
| **Boundary**                     | Không tự sửa toàn bộ bài làm; chỉ hỗ trợ phát hiện, gợi ý và nhắc các mục cần kiểm tra.                                            |
| **AI intervention point**        | Sau khi hệ thống quét repo và kiểm tra rule, AI tóm tắt các mục còn thiếu và gợi ý phần cần bổ sung.                               |
| **Mức chọn**                     | Workflow                                                                                                                           |
| **Rủi ro & người thật kiểm tra** | Risk: AI hiểu sai yêu cầu hoặc gợi ý thiếu chính xác. Person check: sinh viên review lại các mục và quyết định sửa như thế nào.    |

## 09 — Final decision

Decision:

Go with scope nhỏ.

Lý do:

- Candidate cụ thể, workflow rõ, metric dễ đo.
- Có non-AI fallback bằng checklist và kiểm tra thủ công cơ bản.
- AI chỉ tham gia ở một bước hỗ trợ rõ: tóm tắt và gợi ý các mục còn thiếu.
- Người dùng vẫn kiểm tra lại và quyết định cuối cùng trước khi nộp.

Pilot nhỏ nhất:

- Chọn 1 repo lab mẫu và 1 bộ README/worksheet/bài mẫu để thử quy trình.
- Dùng rule/script kiểm tra cấu trúc thư mục, tên file và heading bắt buộc.
- Dùng AI để tóm tắt yêu cầu còn thiếu và gợi ý cách bổ sung.
- Đo thời gian kiểm tra và số lỗi phát hiện được trước khi nộp.

Exit / rollback:

- Nếu rule/script chỉ giải quyết được phần cấu trúc nhưng không giúp kiểm tra chất lượng nội dung, hạ xuống checklist + review thủ công.
- Nếu AI gợi ý quá nhiều sai hoặc không đáng tin cậy, chỉ dùng rule/script và người dùng tự kiểm tra.
