# BÀI LÀM: SỬA ĐỔI PROMPT THIẾU CẤU TRÚC RÀNG BUỘC ĐỊNH DẠNG

---

## Bước 1: Phân tích lỗi

Giả sử với prompt cũ (`Hãy giải thích ngắn gọn các nội dung của Custom Instructions, Prompt Library, Prompt Injection.`), AI trả về một đoạn văn dài có mở đầu, giải thích lan man và kết thúc gợi ý thêm. Khi dán thẳng vào tài liệu học tập hoặc báo cáo, 3 phần văn bản thừa thãi sau đây làm loãng nội dung chính:

1. **Lời chào và câu dẫn mở đầu:** Ví dụ các câu như *"Chào bạn, rất vui được hỗ trợ bạn! Dưới đây là phần giải thích chi tiết nhưng dễ hiểu cho các khái niệm mà bạn vừa quan tâm nhé:"* — không mang thông tin học thuật, chỉ tốn dòng và làm chậm việc trích xuất ý chính.
2. **Phần diễn giải lan man / lặp ý ví dụ:** AI thường mở rộng thêm các tình huống phụ hoặc lặp lại cùng một ý bằng nhiều cách diễn đạt khác nhau thay vì chốt thẳng bản chất, khiến nội dung khó quét nhanh khi làm tài liệu.
3. **Lời kết và câu mời hỏi tiếp ở cuối:** Ví dụ *"Hy vọng phần giải thích trên sẽ hữu ích cho việc học của bạn! Nếu bạn cần mình làm rõ thêm khái niệm nào hoặc cho ví dụ thực tế hơn thì cứ bảo mình nhé."* — dư thừa khi mục tiêu là lấy nội dung ngắn gọn để dán thẳng vào báo cáo.

---

## Bước 2: Prompt tối ưu

```text
Giải thích ngắn gọn các khái niệm sau: Custom Instructions, Prompt Library, Prompt Injection.

Ràng buộc bắt buộc:
- Bắt buộc trình bày hoàn toàn dưới dạng gạch đầu dòng (- ), mỗi khái niệm tối đa 1-2 câu ngắn, nêu đúng bản chất.
- Cấm tuyệt đối viết lời chào, câu dẫn mở đầu, giải thích lan man hoặc lời kết/câu hỏi gợi ý ở cuối.
- Bắt đầu ngay vào gạch đầu dòng đầu tiên.

```

---

## Kết quả phản hồi từ prompt đã sửa

* **Custom Instructions:** Là bộ quy tắc và ngữ cảnh cố định được thiết lập sẵn để định hướng vai trò, giọng văn, phạm vi xử lý và giới hạn của AI trong suốt quá trình làm việc.
* **Prompt Library:** Là kho lưu trữ tập trung các mẫu prompt đã được chuẩn hóa và kiểm thử cho từng tác vụ lặp lại nhằm tái sử dụng nhanh, đồng bộ chất lượng và tiết kiệm thời gian soạn lại.
* **Prompt Injection:** Là kỹ thuật chèn chỉ thị độc hại hoặc lệnh đánh lừa vào dữ liệu đầu vào nhằm ép AI bỏ qua quy tắc gốc, làm sai lệch hành vi hoặc rò rỉ thông tin hệ thống.