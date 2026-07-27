Nhân vật ví dụ: Hoàng, sinh viên mới ra trường đang học tại khóa học AI thực chiến và là trưởng nhóm 4 người. Mỗi ngày Hoàng phải tổng hợp lại ý kiến của các thành viên trong nhóm, rà soát tất cả các kênh thông báo để không bỏ sót bất kì thông tin nào. Gặp các thông tin cần tra lại thì rất khó để tìm lại vì thông tin ở rất nhiều kênh, từ slide bài giảng, sổ tay sinh viên, các mẹo mà anh chị chia sẻ trên discord hay những thông tin đơn giản như mssv đều phải mở outlock tra lại.

# 01 — Individual Problem Scan

## Scan rộng

Hoàng scan 5 problems.

| #   | Lăng kính         | Problem quan sát được                                                                                        | Ai chịu ảnh hưởng?    | Dấu hiệu thật                                     |
| --- | ----------------- | ------------------------------------------------------------------------------------------------------------ | --------------------- | ------------------------------------------------- |
| 1   | Lặp lại           | Mỗi ngày phải kiểm tra Discord, Outlook, VLearn và các kênh khác để không bỏ sót thông báo hoặc deadline     | Hoàng, cả nhóm        | Mất khoảng 20–30 phút/ngày                        |
| 2   | Lặp lại           | Là trưởng nhóm nên phải tổng hợp ý kiến của 4 thành viên rồi gửi lại cho cả nhóm hoặc giảng viên             | Hoàng, các thành viên | Mỗi lần thảo luận đều phải đọc lại nhiều tin nhắn |
| 3   | Tốn thời gian     | Khi cần tìm lại thông tin cũ (slide, sổ tay sinh viên, email, Discord...) rất khó vì dữ liệu nằm ở nhiều nơi | Hoàng                 | Mỗi lần tra cứu mất khoảng 10–20 phút             |
| 4   | Tốn thời gian     | Mỗi ngày phải đọc lại slide bài giảng để ôn tập kiến thức trước khi học tiếp                                 | Hoàng                 | Khoảng 30 phút/ngày                               |
| 5   | AI có thể tốt hơn | Không có công cụ nào tổng hợp toàn bộ thông tin học tập và trả lời theo ngữ cảnh của khóa học                | Hoàng, các thành viên | Phải tự nhớ hoặc tự tìm ở nhiều nguồn khác nhau   |

## Top 3

| Rank | Problem                                       | Vì sao chọn                                                                  | Điều còn chưa chắc                          |
| ---- | --------------------------------------------- | ---------------------------------------------------------------------------- | ------------------------------------------- |
| 1    | Theo dõi thông báo và deadline từ nhiều kênh  | Xảy ra hằng ngày, dễ bỏ sót, ảnh hưởng trực tiếp đến tiến độ học và làm nhóm | Khả năng tích hợp dữ liệu từ nhiều nền tảng |
| 2    | Tìm lại thông tin cũ từ nhiều nguồn           | Xuất hiện rất thường xuyên khi làm bài tập hoặc dự án, mất nhiều thời gian   | Cần xây dựng cơ chế tìm kiếm hiệu quả       |
| 3    | Tổng hợp ý kiến của các thành viên trong nhóm | Là công việc lặp lại của trưởng nhóm, có thể tự động hóa một phần            | Chất lượng bản tóm tắt cần được kiểm chứng  |

# Problem Card #1 — Theo dõi thông báo và deadline từ nhiều kênh

**Problem 1 câu:**  
Mỗi ngày Hoàng phải kiểm tra nhiều kênh như Discord, Outlook, VLearn và các nền tảng khác để không bỏ sót thông báo hoặc deadline quan trọng của khóa học.

**Actor:**  
Hoàng, sinh viên mới ra trường đang học khóa AI thực chiến và là trưởng nhóm 4 người.

**Thời điểm / bối cảnh:**  
Đầu ngày, trước mỗi buổi học hoặc trước khi làm bài tập nhóm.

**Current workflow:**

```text
1. Mở Outlook đọc email
2. Kiểm tra các Discord của khóa học
3. Đọc thông báo trên VLearn
4. Kiểm tra tài liệu hoặc nhóm chat
5. Ghi nhớ hoặc tự ghi lại deadline
6. Thông báo cho các thành viên trong nhóm nếu cần
```

**Bottleneck:**  
Thông tin nằm rải rác ở nhiều nền tảng nên phải kiểm tra thủ công từng nơi và rất dễ bỏ sót deadline.

**Impact:**  
Mất khoảng 20–30 phút mỗi ngày chỉ để kiểm tra thông báo. Nếu bỏ sót một thông báo, cả nhóm có thể nộp bài muộn hoặc thiếu yêu cầu.

**Success metric:**  
Giảm thời gian kiểm tra xuống dưới 5 phút/ngày và không bỏ sót bất kỳ deadline quan trọng nào.

**Non-AI alternative:**  
Tự ghi tất cả deadline vào Google Calendar hoặc Notion sau khi đọc từng thông báo.

**AI hypothesis:**  
AI tự tổng hợp thông báo từ nhiều nguồn, lọc các nội dung quan trọng, nhắc deadline và tạo checklist công việc mỗi ngày.

**Quick gut:**  
**Agent**

### Draft current workflow

```text
CURRENT STATE — ~30 phút

[Outlook]
      ↓
[Discord]
      ↓
[VLearn]
      ↓
[Tài liệu]
      ↓
[Tự tổng hợp]
      ↓
[Ghi nhớ deadline]
```

### Draft future workflow

```text
FUTURE STATE — ~5 phút

[AI đọc tất cả nguồn]
          ↓
[AI lọc deadline]
          ↓
[Tạo checklist hôm nay]
          ↓
[Hoàng xác nhận]
```

---

# Problem Card #2 — Tra cứu lại thông tin học tập từ nhiều nguồn

**Problem 1 câu:**  
Khi cần tìm lại một thông tin đã học hoặc đã được thông báo, Hoàng phải tìm qua nhiều nguồn khác nhau nên mất nhiều thời gian.

**Actor:**  
Hoàng, sinh viên AI thực chiến và trưởng nhóm.

**Thời điểm / bối cảnh:**  
Trong lúc làm bài tập, dự án hoặc khi các thành viên hỏi lại thông tin.

**Current workflow:**

```text
1. Cố nhớ thông tin nằm ở đâu
2. Mở slide bài giảng
3. Nếu không có thì mở sổ tay sinh viên
4. Tiếp tục tìm trên Discord
5. Nếu vẫn chưa thấy thì mở Outlook
6. Gửi lại thông tin cho nhóm
```

**Bottleneck:**  
Thông tin được lưu ở nhiều nơi khác nhau nên việc tra cứu phụ thuộc vào trí nhớ và mất nhiều thời gian.

**Impact:**  
Mỗi lần tìm mất khoảng 10–20 phút, làm gián đoạn quá trình học và xử lý công việc của nhóm.

**Success metric:**  
Tìm được thông tin cần thiết trong dưới 1 phút.

**Non-AI alternative:**  
Tự tổng hợp tất cả tài liệu vào một thư mục hoặc Notion.

**AI hypothesis:**  
AI lập chỉ mục toàn bộ slide, email, Discord và tài liệu của khóa học, cho phép tìm kiếm bằng ngôn ngữ tự nhiên.

**Quick gut:**  
**Agent**

### Draft current workflow

```text
CURRENT STATE — ~15 phút

[Cố nhớ]
      ↓
[Slide]
      ↓
[Sổ tay]
      ↓
[Discord]
      ↓
[Outlook]
      ↓
[Tìm thấy]
```

### Draft future workflow

```text
FUTURE STATE — <1 phút

[Đặt câu hỏi]
        ↓
[AI tìm kiếm]
        ↓
[Trả về đúng tài liệu]
```

---

# Problem Card #3 — Tổng hợp ý kiến của các thành viên trong nhóm

**Problem 1 câu:**  
Sau mỗi buổi thảo luận, Hoàng phải đọc lại toàn bộ tin nhắn để tổng hợp ý kiến và phân công công việc cho nhóm.

**Actor:**  
Hoàng, trưởng nhóm 4 người trong khóa AI thực chiến.

**Thời điểm / bối cảnh:**  
Sau mỗi buổi họp hoặc khi nhóm trao đổi trên Discord.

**Current workflow:**

```text
1. Đọc lại toàn bộ cuộc trò chuyện
2. Ghi lại từng ý kiến của thành viên
3. Tổng hợp thành nội dung chung
4. Phân chia công việc
5. Gửi lại kết quả cho cả nhóm
```

**Bottleneck:**  
Cuộc trò chuyện dài, nhiều ý kiến lặp lại hoặc thay đổi khiến việc tổng hợp mất thời gian và dễ bỏ sót.

**Impact:**  
Mỗi lần tổng hợp mất khoảng 15–20 phút và đôi khi các thành viên vẫn phải hỏi lại nhiệm vụ của mình.

**Success metric:**  
Giảm thời gian tổng hợp xuống dưới 5 phút và mọi thành viên đều nhận đúng nhiệm vụ.

**Non-AI alternative:**  
Một thành viên ghi biên bản cuộc họp hoặc ghi chú thủ công.

**AI hypothesis:**  
AI tự động tóm tắt cuộc trò chuyện, trích xuất quyết định cuối cùng và tạo danh sách công việc cho từng thành viên.

**Quick gut:**  
**Workflow**

### Draft current workflow

```text
CURRENT STATE — ~20 phút

[Đọc toàn bộ chat]
         ↓
[Tổng hợp ý kiến]
         ↓
[Phân chia công việc]
         ↓
[Gửi cho nhóm]
```

### Draft future workflow

```text
FUTURE STATE — ~5 phút

[AI đọc cuộc trò chuyện]
            ↓
[AI tóm tắt quyết định]
            ↓
[AI tạo danh sách nhiệm vụ]
            ↓
[Hoàng kiểm tra và gửi]
```
