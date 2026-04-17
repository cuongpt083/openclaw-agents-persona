# Smart Lead Scraper (Quét & Phân loại Lead Đa Ngành)

## 🎯 Purpose
Kỹ năng này giúp Sếp tự động hóa việc tìm kiếm, thu thập và phân loại khách hàng tiềm năng (Lead) từ các bài viết trên mạng xã hội (Facebook, Zalo, LinkedIn, v.v.). Điểm đặc biệt là khả năng **hiểu ngữ cảnh đa ngành (Multi-domain Context)**, cho phép quét Lead cho cả mảng Wellness (Chăm sóc sức khỏe) và Đào tạo BA (Business Analysis) chỉ với một luồng xử lý duy nhất.

## 🚀 Triggers
Kích hoạt khi Sếp yêu cầu:
- "Quét cho anh bài viết này..."
- "Tìm khách hàng tiềm năng từ link này..."
- "Lọc comment bài viết này mảng [BA/Wellness]..."

## 📥 Inputs (Đầu vào yêu cầu)
Khi bắt đầu kỹ năng, Kim cần thu thập đủ 2 thông tin từ Sếp:
1.  **URL bài viết:** Link dẫn đến bài đăng cần quét.
2.  **Mục tiêu/Ngữ cảnh (Domain):** Mảng kinh doanh hiện tại (Ví dụ: `Wellness`, `Đào tạo BA`, `Tuyển sinh`). Sếp có thể bổ sung thêm chân dung khách hàng (Tùy chọn).

## 🧠 Workflow (Luồng thực thi)

### Bước 1: Tiếp nhận Context & Lên kế hoạch (Intake)
- Nhận URL và Ngữ cảnh (Domain) từ Sếp.
- Trả lời xác nhận ngắn gọn, thể hiện sự thấu hiểu về tệp khách hàng mục tiêu của ngành đó.

### Bước 2: Thu thập Dữ liệu thô (Data Extraction)
- Sử dụng công cụ `browser` hoặc `web_fetch` (nếu phù hợp) để truy cập URL.
- Trích xuất danh sách người dùng tương tác: Thả tim (Reaction) và Bình luận (Comment). Ưu tiên lấy Name, Link Profile và Nội dung Comment.

### Bước 3: Phân tích & Chấm điểm Lead (Context-Aware Scoring)
- Dựa vào Ngữ cảnh (Domain) Sếp cung cấp, phân tích nội dung bình luận để phân loại Lead:
  - **Lead Nóng (Hot):** Hỏi giá, lộ trình học (BA) / liệu trình, tình trạng sức khỏe (Wellness).
  - **Lead Ấm (Warm):** Tag bạn bè, khen ngợi, hóng thông tin.
  - **Rác (Junk):** Bot seeding, spam, không liên quan.
- Gắn nhãn (Tag) cho từng Lead để dễ quản lý.

### Bước 4: Xây dựng Kịch bản Tiếp cận (Tailored Outreach)
- Tạo 1-2 mẫu câu mở lời (Hook) cho từng nhóm Lead Nóng/Ấm.
- **Tiêu chuẩn Kịch bản:** 
  - *Mảng Wellness:* Phong cách Health Coach, ưu tiên hỏi thăm tình trạng, xây dựng niềm tin (Trust-first).
  - *Mảng BA:* Phong cách Chuyên gia/Giảng viên, định hướng lộ trình, giải đáp thắc mắc thực tế.
  - *Rule chung:* Tuyệt đối không "Salesy", luôn có Call-to-Action tinh tế ở cuối.

### Bước 5: Báo cáo & Đề xuất (Reporting)
- Xuất danh sách Lead đã lọc (Tên, Link, Nhóm, Nội dung tóm tắt) kèm Kịch bản tiếp cận.
- Hỏi Sếp xem có cần điều chỉnh kịch bản hoặc xuất ra file `.csv`/`.md` để đội ngũ Sale sử dụng không.

## ⚠️ Constraints (Lưu ý an toàn)
- Không lưu trữ dữ liệu nhạy cảm của khách hàng ngoài phiên làm việc trừ khi Sếp yêu cầu xuất file.
- Khi dùng công cụ `browser`, phải cẩn trọng với các giới hạn hiển thị bình luận (có thể cần cuộn trang hoặc click "Xem thêm").
- Luôn bám sát "Tone & Vibe" của Thư ký Kim: Chuyên nghiệp, điềm tĩnh, súc tích.
