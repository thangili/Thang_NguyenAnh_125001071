# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

**Họ và tên:** Nguyễn Anh Thắng
**MSSV:** 125001071
**Tên đề tài Website:** Website Thương Mại Điện Tử - Cửa Hàng Giày Sneaker Hub
**Công cụ AI đã sử dụng:** Google Gemini

## 1. Yêu cầu ban đầu (System/Initial Prompt)
> "Hãy thiết kế toàn bộ mã nguồn cho một website bán giày thể thao (Sneaker Hub) sử dụng Semantic HTML5 chuẩn xác gồm header, nav, main, section, article, footer. Sử dụng CSS Variables (:root) với tông màu cam hiện đại, áp dụng CSS Grid cho danh sách sản phẩm và Flexbox cho layout điều hướng."

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iterations)

### Lần 1: Xây dựng cấu trúc Semantic HTML & CSS Grid/Flexbox
- **Prompt đã dùng:** "Kiểm tra cấu trúc HTML của trang web bán giày, đảm bảo sử dụng đúng các thẻ `<article>` cho từng thẻ sản phẩm và `<section>` cho từng khu vực nội dung chính."
- **Kết quả AI tạo ra:** Mã nguồn HTML chuẩn Semantic, tổ chức bố cục linh hoạt bằng CSS Grid cho lưới sản phẩm.
- **Nhận xét & Tinh chỉnh của SV:** Thêm các hiệu ứng `:hover` mượt mà cho card sản phẩm và tinh chỉnh biến `:root` để giao diện đồng bộ màu sắc.

### Lần 2: Tích hợp thư viện Animate.css & AOS (Animate On Scroll)
- **Prompt đã dùng:** "Hãy tích hợp thêm thư viện Animate.css vào phần tiêu đề Hero và AOS (Animate On Scroll) cho các sản phẩm để tạo hiệu ứng chuyển động khi cuộn trang."
- **Thách thức gặp phải:** Các hiệu ứng cuộn trang cần khởi tạo đúng cú pháp thư viện JavaScript của AOS.
- **Cách sửa prompt (Debug prompt):** "Bổ sung đoạn script khởi tạo `AOS.init()` vào cuối file HTML và gắn các thuộc tính `data-aos` vào các khối thẻ tương ứng."

## 3. Đánh giá cá nhân về quá trình Vibe Coding
- **AI đã giúp bạn tiết kiệm thời gian ở phần nào nhất:** Giúp sinh mã nguồn HTML/CSS cho một website bán hàng hoàn chỉnh rất nhanh chóng, cấu trúc rõ ràng và tối ưu chuẩn giao diện thương mại điện tử.
- **Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web:** Cần xác định rõ chủ đề sản phẩm từ đầu để AI định hình màu sắc và bố cục (Grid/Flexbox) chuẩn xác theo yêu cầu đề bài.