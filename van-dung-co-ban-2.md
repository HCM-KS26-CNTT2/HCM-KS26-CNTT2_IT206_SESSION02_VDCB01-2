## [Vận dụng cơ bản 2] Khắc phục lỗi khai báo biến số trong prompt mẫu
### 1. KẾT QUẢ PHÂN TÍCH LỖI 
- Nguyên nhân & Tác hại:
  1. Thiếu tính đồng nhất: Trộn lẫn cú pháp giữa ngoặc vuông và ngoặc nhọn gây khó khăn cho việc viết code tự động quét biến (regex/script).
  2. Dễ bị AI đọc nhầm thành từ khóa ngữ nghĩa thay vì biến số thực tế cần thay thế nội dung động.
  3. Giảm khả năng tái sử dụng của prompt trong các hệ thống quy mô lớn.

### 2. ĐỒNG BỘ BIẾN SỐ & PROMPTING TỐI ƯU 
- Giải pháp: Đưa toàn bộ biến số về dạng viết hoa hoàn toàn, nằm trong dấu ngoặc vuông để tạo quy chuẩn chung, ví dụ: [NGÔN_NGỮ], [ĐỐI_TƯỢNG].
```
Context: Bạn là chuyên gia truyền thông công nghệ và sáng tạo nội dung giáo dục.
Request: Hãy viết một bài chia sẻ chi tiết, mạch lạc về chủ đề "Cấu trúc Prompt Tiêu chuẩn & Định dạng".
Constraint (Ràng buộc):
- Viết toàn bộ bài viết bằng ngôn ngữ: [NGÔN_NGỮ].
- Điều chỉnh giọng văn, thuật ngữ và ví dụ cho phù hợp với đối tượng độc giả mục tiêu là: [ĐỐI_TƯỢNG].
- Đảm bảo độ dài từ 300 - 500 từ, trình bày rõ ràng bằng các tiêu đề phụ (Markdown headings) và gạch đầu dòng.
```
### 3. KẾT QUẢ CHẠY THỬ
* Dữ liệu truyền vào: 
  - [NGÔN_NGỮ] = Tiếng Việt
  - [ĐỐI_TƯỢNG] = Sinh viên năm nhất chuyên ngành CNTT
* Kết quả phản hồi từ AI:
```
  # Cấu trúc Prompt Tiêu chuẩn & Định dạng dành cho Sinh viên CNTT
  
  Chào các bạn sinh viên năm nhất! Khi làm việc với Trí tuệ Nhân tạo (AI), việc viết prompt không chỉ là "gõ đại câu hỏi" mà là một kỹ năng kỹ thuật thực thụ. Dưới đây là bí quyết giúp bạn tối ưu hóa câu lệnh:
  
  * **1. Khung CREATE Chuẩn Mực:**
    * **Context (Bối cảnh):** Định nghĩa vai trò và môi trường cho AI.
    * **Request (Yêu cầu):** Nêu rõ nhiệm vụ chính cần hoàn thành.
    * **Explanation (Giải thích):** Cung cấp thêm tài liệu hoặc lý do chi tiết.
    * **Action (Hành động):** Hành động cụ thể mà bạn muốn AI thực thi.
    * **Tone (Giọng điệu):** Định hình phong cách trình bày (ví dụ: thân thiện, học thuật).
    * **Extras (Phần mở rộng):** Các ràng buộc phụ (độ dài, định dạng).
    
  * **2. Tầm quan trọng của Ép Định Dạng:**
    * Thay vì để AI trả về văn bản tự do khó đọc, hãy yêu cầu định dạng rõ ràng như **Markdown**, **Bảng (Table)** hoặc **JSON** để dễ dàng tích hợp vào code hoặc tài liệu học tập của bạn.