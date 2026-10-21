# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)
- **Họ và tên:** Nguyễn Quốc Bảo
- **MSSV:** 125000946
- **Tên đề tài Website:** Trang Portfolio Cá nhân (Personal Portfolio)
- **Công cụ AI đã sử dụng:** Gemini

## 1. Yêu cầu ban đầu (System/Initial Prompt)
> *Đóng vai một chuyên gia Front-end Web Developer, hãy viết cho tôi một file index.html cho trang Portfolio cá nhân. Yêu cầu bắt buộc: Sử dụng chuẩn Semantic HTML5 (header, nav, main, section, footer), tích hợp CDN của Animate.css và thư viện AOS (Animate On Scroll).*

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration Iterations)
### Lần 1: Dựng khung Semantic HTML & CSS Variable
- **Prompt đã dùng:** Viết file style.css sử dụng CSS Variables để quản lý màu sắc, font chữ. Sử dụng Flexbox/Grid để chia bố cục cho header và các section. Thêm hiệu ứng hover cho các nút bấm.
- **Kết quả AI tạo ra:** AI tạo ra mã CSS cơ bản đáp ứng responsive, các biến `:root` được khai báo rõ ràng.
- **Nhận xét & Tinh chỉnh của SV:** Layout ổn định nhưng phần header chưa dính chặt trên cùng khi cuộn trang. Đã yêu cầu AI thêm thuộc tính `position: sticky` cho header.

### Lần 2: Tích hợp thư viện Animate.css & AOS
- **Prompt đã dùng:** Hướng dẫn tôi cách thêm data-aos="fade-up" vào các thẻ HTML để tạo hiệu ứng cuộn trang và khởi tạo AOS trong JavaScript.
- **Thách thức gặp phải:** Hiệu ứng AOS không hoạt động khi mới load trang, phải cuộn xuống mới thấy.
- **Cách sửa prompt (Debug prompt):** Làm sao để fix lỗi AOS không chạy ngay khi trang vừa load xong ở section đầu tiên? (Đã fix bằng cách thêm đoạn script khởi tạo `AOS.init();` ở cuối thẻ body).

## 3. Đánh giá cá nhân về quá trình Vibe Coding
- AI đã giúp bạn tiết kiệm thời gian ở phần nào nhất? 
  -> AI giúp tiết kiệm 80% thời gian dựng khung boilerplate HTML, viết các class CSS Grid/Flexbox phức tạp và nhúng nhanh các thư viện hiệu ứng mà không cần phải tự tìm link CDN.
- Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web?
  -> Cần đưa ra yêu cầu (constraint) rõ ràng ngay từ đầu (ví dụ: bắt buộc dùng Semantic tag, bắt buộc dùng CSS Variable). Thay vì bảo AI "làm cho tôi trang web", hãy chia nhỏ ra yêu cầu AI làm HTML trước, CSS sau, và cuối cùng mới tích hợp thư viện.

### Lần 3: Nâng cấp UI/UX hiện đại (Dark Theme & Glassmorphism)
- **Prompt đã dùng:** Giao diện cũ còn đơn giản quá, hãy nâng cấp toàn bộ website sang phong cách Dark Theme hiện đại, sử dụng hiệu ứng Glassmorphism (kính mờ) cho header và các thẻ dự án. Thêm section Kỹ năng (Tech Stack) và Form Liên hệ. Thêm hiệu ứng glowing (phát sáng) khi hover vào các nút bấm và project card.
- **Kết quả AI tạo ra:** Mã nguồn HTML được bổ sung thêm section `#skills` và `#contact`. CSS được đắp thêm các thuộc tính `backdrop-filter: blur()`, background gradient chuyển động, và cập nhật lại toàn bộ hệ thống biến CSS (CSS Variables) sang tông màu tối (Dark Mode).
- **Nhận xét & Tinh chỉnh của SV:** Giao diện lột xác hoàn toàn, trông giống một portfolio của dân IT chuyên nghiệp thực thụ. Các thư viện Animate.css và AOS phối hợp rất mượt với giao diện mới.