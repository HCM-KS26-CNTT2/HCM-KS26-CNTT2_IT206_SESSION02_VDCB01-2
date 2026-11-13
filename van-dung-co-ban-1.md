## [Vận dụng cơ bản 1] Sửa đổi prompt thiếu cấu trúc ràng buộc định dạng
### 1. KẾT QUẢ PHÂN TÍCH LỖI 
3 phần văn bản thừa thãi thường xuất hiện trong câu trả lời cũ của AI:
1. Lời chào xã giao ở đầu: Ví dụ như "Chào bạn! Dưới đây là phần giải thích...", "Rất vui được hỗ trợ bạn...".
2. Lời dẫn dắt, giải thích lòng vòng: Các đoạn văn mở đầu trước khi đi vào nội dung chính hoặc các câu nhận xét, tóm tắt dư thừa.
3. Lời kết/cảm ơn ở cuối: Ví dụ như "Hy vọng thông tin trên hữu ích cho bạn!", "Chúc bạn học tập tốt!".

### 2. PROMPTING TỐI ƯU
- Prompt tối ưu áp dụng ràng buộc định dạng và loại bỏ văn bản thừa:

Context: Bạn là trợ lý học tập chuyên nghiệp, cung cấp thông tin kỹ thuật chính xác và cô đọng.
Request: Giải thích ngắn gọn các nội dung sau:
1. Khung CREATE (Context, Request, Explanation, Action, Tone, Extras).
2. Zero-shot vs Few-shot Prompting.
3. Ép định dạng trả về (Markdown, Table, JSON thô, Bullet points).
Ràng buộc định dạng: 
- KHÔNG viết lời chào hỏi, lời mở đầu hoặc lời kết xã giao dưới mọi hình thức.
- Bắt đầu trả về ngay lập tức bằng nội dung chính.
- Sử dụng cấu trúc gạch đầu dòng hoặc bảng ngắn gọn, súc tích cho từng ý.

### 3. KẾT QUẢ PHẢN HỒI MẪU TỪ AI 
- Khung CREATE: 
  * Context (Bối cảnh): Đặt ngữ cảnh cho AI.
  * Request (Yêu cầu): Nhiệm vụ cụ thể.
  * Explanation (Giải thích): Làm rõ chi tiết.
  * Action (Hành động): Yêu cầu AI thực thi.
  * Tone (Giọng điệu): Định hình văn phong.
  * Extras (Phần mở rộng): Yêu cầu bổ sung.
- Zero-shot vs Few-shot:
  * Zero-shot: Prompt trực tiếp không kèm ví dụ mẫu.
  * Few-shot: Cung cấp từ 1 đến nhiều ví dụ mẫu giúp AI hiểu rõ mong đợi kết quả.
- Ép định dạng: Sử dụng câu lệnh chỉ định rõ cấu trúc đầu ra (Markdown, Table, JSON) để dễ dàng tích hợp vào hệ thống hoặc báo cáo.