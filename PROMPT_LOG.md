# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)
- **Họ và tên:** Nguyễn Anh Thắng
- **MSSV:** 125001071
- **Tên đề tài Website:** Website Thương Mại Điện Tử - Cửa Hàng Giày Sneaker Hub (10 Sản phẩm)
- **Công cụ AI đã sử dụng:** Google Gemini

## 1. Yêu cầu ban đầu (System/Initial Prompt)
> *Hãy xây dựng trọn bộ mã nguồn hoàn chỉnh cho một website thương mại điện tử bán giày thể thao chính hãng tên là "Sneaker Hub" phục vụ bài kiểm tra giữa kỳ môn Thiết kế Web tại Đại học Lạc Hồng. Cấu trúc mã nguồn phải tuân thủ chuẩn Semantic HTML5 (gồm các thẻ header, nav, main, section, article, footer). Về phần giao diện, khai báo bảng màu thương hiệu hiện đại bằng CSS Variables trong khối :root; thiết kế Layout linh hoạt responsive sử dụng CSS Flexbox cho thanh điều hướng/khung nhà sáng lập và CSS Grid cho bộ sưu tập 10 sản phẩm. Trang web cần tích hợp hiệu ứng chuyển động mượt mà từ thư viện Animate.css, hiệu ứng cuộn trang AOS (Animate On Scroll), khung ảnh chân dung avatar.jpg của nhà sáng lập, cùng phần Footer chứa đầy đủ thông tin địa chỉ Đại học Lạc Hồng, liên hệ và bản quyền sinh viên Nguyễn Anh Thắng - MSSV 125001071.*

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iterations)

### Lần 1: Dựng khung Semantic HTML & CSS Variables
- **Prompt đã dùng:** Hãy dựng khung xương HTML5 chuẩn Semantic cho trang web Sneaker Hub và định nghĩa bảng màu phong cách Sneaker hiện đại bằng CSS Variables trong khối `:root`.
- **Kết quả AI tạo ra:** AI tạo ra đoạn mã HTML cơ bản cùng các biến màu CSS như `--primary-color`, `--accent-color`, `--bg-color`, `--text-color`.
- **Nhận xét & Tinh chỉnh của SV:** AI sử dụng lạm dụng thẻ `<div>` ở phần danh sách sản phẩm và phần thông tin chân trang. Tôi đã nhắc AI tái cấu trúc lại: chuyển khối nội dung chính sang thẻ `<main>`, các khu vực giao diện lớn dùng thẻ `<section>`, từng thẻ sản phẩm dùng thẻ `<article>`, thanh menu dùng thẻ `<nav>`, và chân trang dùng thẻ `<footer>` để đảm bảo tối ưu chuẩn SEO và điểm Semantic HTML.

### Lần 2: Thiết kế Bố cục Responsive (CSS Grid & Flexbox cho 10 sản phẩm)
- **Prompt đã dùng:** Hãy viết CSS dàn trang Flexbox cho Header, Hero Section, Founder Section và ứng dụng CSS Grid để tạo lưới hiển thị 10 card sản phẩm giày thể thao responsive mượt mà trên mọi thiết bị.
- **Kết quả AI tạo ra:** AI sử dụng `display: grid` với thuộc tính `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr))` tạo ra lưới 10 sản phẩm tự động co giãn.
- **Nhận xét & Tinh chỉnh của SV:** Ảnh sản phẩm bị méo tỉ lệ khung hình khi co dãn màn hình mobile. Tôi đã yêu cầu AI thêm thuộc tính `object-fit: cover` cho thẻ `<img>` và đặt chiều cao cố định cho khung ảnh `.product-card img`, đồng thời bổ sung hiệu ứng `:hover` phóng to nhẹ (`transform: translateY(-8px)`) và đổ bóng (`box-shadow`) cho từng card sản phẩm.

### Lần 3: Tích hợp thư viện Hiệu ứng Animate.css & AOS (Animate On Scroll)
- **Prompt đã dùng:** Thêm thư viện Animate.css vào tiêu đề Hero section và tích hợp thư viện AOS (Animate On Scroll) để các thẻ sản phẩm và footer xuất hiện mượt mà khi người dùng cuộn trang.
- **Thách thức gặp phải:** Hiệu ứng AOS không hoạt động khi cuộn trang, các phần tử bị ẩn hoàn toàn hoặc hiển thị không đồng bộ do thiếu đoạn script khởi tạo JavaScript.
- **Cách sửa prompt (Debug prompt):** Hãy kiểm tra và bổ sung các liên kết CDN của AOS (`aos.css` và `aos.js`), sau đó thêm đoạn mã JavaScript khởi tạo `AOS.init({ duration: 800, once: true });` ngay trước thẻ đóng `</body>`, đồng thời gắn đúng các thuộc tính `data-aos="fade-up"` và `data-aos-delay` vào các thẻ HTML tương ứng.

### Lần 4: Cập nhật Footer định danh Sinh viên & Địa chỉ Trường Đại học Lạc Hồng
- **Prompt đã dùng:** Hãy bổ sung phần Footer đầy đủ thông tin bao gồm: Tên thương hiệu Sneaker Hub, thông tin Trường Đại học Lạc Hồng (LHU), địa chỉ cơ sở tại Số 10 Huỳnh Văn Nghệ, P. Bửu Long, TP. Biên Hòa, Đồng Nai, Hotline, Email cá nhân (a.thang1311@gmail.com), giờ mở cửa, các kênh mạng xã hội, và dòng ghi nhận bản quyền: "© 2026 Nguyễn Anh Thắng - MSSV: 125001071 - Sinh viên Đại học Lạc Hồng. All rights reserved."
- **Kết quả AI tạo ra:** Footer hiển thị trực quan với các biểu tượng emoji phù hợp (`🎓`, `📍`, `📞`, `✉️`, `⏰`, `🌐`), bố cục cân đối và đường viền chia cách đẹp mắt.

### Lần 5: Triển khai dự án lên GitHub & Xuất bản qua GitHub Pages
- **Prompt đã dùng:** Hướng dẫn chi tiết quy trình đẩy các file dự án (`index.html`, `style.css`, `avatar.jpg`, `PROMPT_LOG.md`) lên GitHub Repository `Thang_NguyenAnh_125001071` và cấu hình xuất bản trang web live qua GitHub Pages.
- **Thách thức gặp phải:** Ban đầu do kéo thả nguyên cả thư mục bao ngoài nên file `index.html` bị nằm trong thư mục con, dẫn đến GitHub Pages báo lỗi 404 Not Found do không tìm thấy file ở thư mục gốc (`root`).
- **Cách sửa prompt (Debug prompt):** Hướng dẫn cách đưa tất cả các file lẻ xuất hiện trực tiếp ở thư mục gốc (`/root`), chọn nhánh `main` trong phần Settings -> Pages và xuất bản thành công địa chỉ trang web trực tuyến: `https://thangili.github.io/Thang_NguyenAnh_125001071/`.

## 3. Đánh giá cá nhân về quá trình Vibe Coding
- **AI đã giúp bạn tiết kiệm thời gian ở phần nào nhất?**
  AI giúp tiết kiệm hơn 80% thời gian viết mã thủ công. Cụ thể là việc tự động phát sinh cú pháp HTML5 chuẩn Semantic, tạo bộ dữ liệu 10 sản phẩm đồng bộ kèm hình ảnh chất lượng cao, tính toán các quy tắc CSS Grid/Flexbox phức tạp, và đặc biệt là hỗ trợ chẩn đoán - khắc phục lỗi cấu trúc thư mục khi triển khai lên môi trường GitHub Pages.
- **Bài học rút ra khi đặt câu hỏi (Prompt) for AI trong thiết kế web?**
  1. *Độ chi tiết của Prompt quyết định chất lượng đầu ra:* Cần cung cấp đầy đủ ngữ cảnh (vai trò sinh viên, tên trường LHU, mã số sinh viên, tên sản phẩm, công nghệ yêu cầu) ngay từ Initial Prompt.
  2. *Phương pháp Prompt phân tầng (Iterative Prompting):* Không nên bắt AI làm tất cả trong 1 câu lệnh duy nhất mà nên chia nhỏ quy trình thành từng giai đoạn (Dựng khung HTML -> Trang trí CSS/Grid -> Thêm hiệu ứng AOS/Animation -> Chuẩn hóa Footer -> Debug deployment).
  3. *Kiểm soát mã nguồn:* AI là trợ lý đắc lực nhưng sinh viên phải nắm vững kiến thức nền tảng để kiểm tra cấu trúc thẻ, tinh chỉnh thẩm mỹ và nghiệm thu sản phẩm cuối cùng.