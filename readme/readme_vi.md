# 🐦 Công Cụ Phân Tích Video Từ X.com

> Công cụ trích xuất nội dung video từ X (Twitter) nhẹ, nhanh và đa năng

[🌐 Dùng thử trực tuyến](https://twittervideodownloaderx.com/vi) • [📝 Hướng dẫn sử dụng](#-hướng-dẫn-sử-dụng) • [❓ Câu hỏi thường gặp](#-câu-hỏi-thường-gặp)

---

## 📋 Giới thiệu dự án

Dự án này là công cụ phân tích video dựa trên nền web, hỗ trợ trích xuất an toàn tài nguyên video từ các bài đăng công khai trên X.com (trước đây là Twitter), đồng thời cung cấp tùy chọn chuyển đổi và lưu trữ dưới nhiều định dạng khác nhau. Không cần cài đặt phần mềm máy khách, không yêu cầu đăng ký tài khoản, sử dụng ngay lập tức qua trình duyệt.

> ⚠️ **Thông báo quan trọng**: Công cụ này chỉ dành cho mục đích học tập cá nhân, nghiên cứu kỹ thuật và sử dụng trong phạm vi hợp lý. Vui lòng tuân thủ [Thỏa thuận nhà phát triển nền tảng X](https://developer.twitter.com/en/developer-terms/agreement) và luật bản quyền của từng quốc gia. Nghiêm cấm sử dụng với mục đích xâm phạm quyền lợi của người khác.

---

## ✨ Tính năng nổi bật

- 🔗 **Phân tích liên kết**: Hỗ trợ URL bài đăng chuẩn của X.com, tự động nhận diện video/ảnh động GIF
- 📥 **Xuất nhiều định dạng**:
  - Video MP4 chất lượng gốc
  - Trích xuất âm thanh → Định dạng MP3
  - Đoạn video ngắn → Chuyển đổi thành ảnh động GIF
- 🌍 **Giao diện đa ngôn ngữ**: Hỗ trợ tiếng Việt, tiếng Anh, tiếng Trung, tiếng Nhật, tiếng Hàn... tổng cộng 16 ngôn ngữ
- 📱 **Tương thích đa nền tảng**: Hoạt động tốt trên Chrome / Firefox / Safari / Edge, trải nghiệm mượt mà trên điện thoại và máy tính bảng
- 🔒 **Ưu tiên quyền riêng tư**: Không cần đăng ký tài khoản, không thu thập thông tin người dùng, quy trình phân tích hoàn toàn ẩn danh
- ⚡ **Xử lý tốc độ cao**: Hoàn thành phân tích trung bình trong vòng 5 giây, hỗ trợ yêu cầu song song

---

## 🚀 Bắt đầu nhanh

### Sử dụng trực tuyến (khuyến nghị)
1. Truy cập [https://twittervideodownloaderx.com/vi](https://twittervideodownloaderx.com/vi)
2. Sao chép liên kết bài đăng mục tiêu (ví dụ: `https://x.com/user/status/123456789`)
3. Dán liên kết vào ô nhập liệu → Nhấp nút 「Phân tích」
4. Chọn định dạng mong muốn → Lưu tệp theo hướng dẫn của trình duyệt

### Triển khai cục bộ (dành cho nhà phát triển)
```bash
# Clone repository
git clone https://github.com/your-repo/x-video-parser.git

# Cài đặt dependencies
cd x-video-parser && npm install

# Cấu hình biến môi trường (tùy chọn)
cp .env.example .env

# Khởi động server phát triển
npm run dev
```

> 💡 Lưu ý: Dự án sử dụng kiến trúc Node.js + Express. Vui lòng tham khảo tài liệu triển khai chi tiết tại `/docs/DEPLOY.md`

---

## 🛠 Công nghệ sử dụng

| Module | Công nghệ áp dụng |
|--------|------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Xử lý video | ffmpeg.wasm (chuyển đổi nhẹ trên frontend) |
| Proxy chuyển tiếp | Cloudflare Workers / Middleware tự xây dựng |
| Quốc tế hóa | vue-i18n + Gói ngôn ngữ JSON |

---

## 📚 Hướng dẫn sử dụng

### Quy trình thao tác cơ bản
```
1. Lấy liên kết bài đăng
   └─ Mở bài đăng mục tiêu trên X.com → Sao chép URL từ thanh địa chỉ trình duyệt

2. Gửi yêu cầu phân tích
   └─ Dán liên kết vào ô nhập của công cụ → Nhấp 「Tải video」

3. Chọn định dạng đầu ra
   ├─ 🎬 Tải dưới dạng MP4: Lưu với chất lượng gốc
   ├─ 🎵 Chuyển đổi sang MP3: Trích xuất track âm thanh
   └─ 🎞 Chuyển đổi sang GIF: Tạo ảnh động ngắn (khuyến nghị: ≤15 giây)

4. Lưu tệp
   └─ Tài nguyên mở trong tab mới → Nhấp chuột phải/menu → 「Lưu thành」
```

### Mẹo sử dụng trên điện thoại thông minh
- iOS Safari: Nút Chia sẻ → 「Lưu vào Tệp」
- Android Chrome: Nhấn giữ video → 「Tải video」
- Trường hợp video tự động phát: Nhấp `⋮` góc trên bên phải trình phát → Chọn 「Tải xuống」

---

## ❓ Câu hỏi thường gặp

**Hỏi: Tệp đã tải về được lưu ở đâu?**  
Đáp: Tệp sẽ được lưu vào thư mục tải xuống đã cài đặt trong trình duyệt. Bạn có thể kiểm tra hoặc thay đổi đường dẫn lưu trong phần cài đặt của trình duyệt.

**Hỏi: Có thể phân tích tài khoản riêng tư hoặc nội dung bị hạn chế không?**  
Đáp: Không. Công cụ này chỉ hỗ trợ các bài đăng được cài đặt ở chế độ công khai và tôn trọng cài đặt quyền truy cập của nội dung gốc.

**Hỏi: Chất lượng hình ảnh/âm thanh sau khi chuyển đổi có bị giảm không?**  
Đáp: Định dạng MP4 giữ nguyên chất lượng gốc. Định dạng MP3 sử dụng mã hóa tiêu chuẩn 128kbps. Định dạng GIF sẽ tối ưu hóa tốc độ khung hình theo thời lượng phát để cân bằng giữa kích thước tệp và độ mượt.

**Hỏi: Lịch sử tải xuống hoặc bộ nhớ đệm có được lưu trữ không?**  
Đáp: Không. Tất cả tài nguyên đều được truyền trực tiếp đến thiết bị người dùng qua proxy tạm thời, máy chủ không lưu trữ bất kỳ nội dung yêu cầu hoặc tệp media nào.

**Hỏi: Nếu phân tích thất bại thì phải làm sao?**  
Đáp: Vui lòng kiểm tra: ① Liên kết bài đăng công khai có hợp lệ không ② Môi trường mạng có ổn định không ③ Thử đổi trình duyệt khác và thử lại. Nếu vấn đề vẫn tiếp diễn, vui lòng báo cáo qua Issue bất cứ lúc nào.

---

## ⚖️ Tuân thủ quy định và Tuyên bố miễn trừ

- Công cụ này **không xâm nhập hoặc bypass bất kỳ biện pháp bảo vệ kỹ thuật nào** của nền tảng, chỉ thu thập siêu dữ liệu thông qua giao diện công khai
- Người dùng vui lòng tự xác nhận hành vi sử dụng của mình có phù hợp với quy định pháp luật địa phương và điều khoản sử dụng của nền tảng hay không
- Các trường hợp sử dụng được khuyến nghị: Lưu trữ cá nhân, minh họa giáo dục, tài liệu tham khảo sản xuất nội dung... trong phạm vi sử dụng hợp lý (Fair Use)
- Nếu phát hiện nội dung có nghi ngờ xâm phạm quyền lợi, vui lòng liên hệ kênh chính thức của [X qua biểu mẫu báo cáo bản quyền này](https://help.twitter.com/forms/dmca)

---

## 🤝 Hướng dẫn đóng góp

Chúng tôi hoan nghênh việc gửi Pull Request và báo cáo Issue! Trước khi đóng góp, vui lòng đọc kỹ các tài liệu sau:
- [Quy chuẩn mã nguồn](/CONTRIBUTING.md)
- [Hướng dẫn dịch đa ngôn ngữ](/locales/README.md)
- [Yêu cầu bảo mật và tuân thủ](/SECURITY.md)

---

## 📄 Giấy phép

Dự án này được phát hành dưới [Giấy phép MIT](/LICENSE), có thể sử dụng miễn phí cho mục đích học tập và nghiên cứu. Trường hợp sử dụng thương mại, vui lòng rà soát kỹ các yêu cầu tuân thủ pháp luật.

---

> 🌟 Nếu công cụ này hữu ích với bạn, vui lòng ✨nhấn Star để ủng hộ! Sự ủng hộ của mọi người chính là động lực lớn nhất để chúng tôi duy trì và phát triển dự án~

*Cập nhật lần cuối: Tháng 5 năm 2026 | Phiên bản: v2.1.0*