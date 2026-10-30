# AI LOG – BUỔI 7, TIẾT 3

> Điền vào `[ ... ]`, tích `[x]` vào lựa chọn phù hợp. Ghi đúng việc đã làm; chưa kiểm tra thì ghi “Chưa kiểm tra”. Không cần chép toàn bộ cuộc trò chuyện AI.

## Thông tin sinh viên

- Họ và tên: [ Lỗ Văn Tuấn ]
- Mã sinh viên – Lớp: [ 1771020716 - CNTT17-08 ]
- Ngày thực hiện: [30/10/2026 ]
- Link repository: [ https://github.com/tuan1143/K20_Portfolio_CNTT20_02.git ]
- URL website: [ https://tuan1143.github.io/K20_Portfolio_CNTT20_02/ ]
- Tình huống: [ ] Website của tôi  [ ] Repo luyện của giảng viên

## 1. Nhận định của tôi trước khi hỏi AI

- Trang/thao tác gặp lỗi: [trang thông tin giới thiệu lỗi thiếu css ]
- Mong muốn và hiện tượng thực tế: [Mong muốn trang hiển thị giao diện đã thiết kế, Thực tế trang chỉ hiển thị nội dung chữ thuần túy (HTML thô), vỡ bố cục, ]
- Dữ kiện đã kiểm tra (cấu trúc tệp, Request URL, Status…): [ css/style.css ]
- Tôi nghi nguyên nhân là: [ Đường dẫn import/link đến tệp CSS bị sai ]
- Vì sao tôi nhận định như vậy: [Khi nội dung chữ vẫn tải bình thường nhưng hoàn toàn không có màu sắc hay định dạng, chứng tỏ mã nguồn HTML vẫn chạy nhưng trình duyệt không thể tải hoặc tìm thấy tệp css đi kèm.]

## 2. Tôi hỏi AI và nhận được gợi ý

- Nguồn: [ ] Công cụ AI: [ git copilot ]  [ ] Phản hồi mẫu của giảng viên
- Câu hỏi/prompt tôi đã gửi (hoặc tình huống của phản hồi mẫu):

  [ PROMPT MẪU
Tôi có URL [https://tuan1143.github.io/K20_Portfolio_CNTT20_02/], cấu trúc [K20_Portfolio_CNTT20_02/
├── index.html
├── about.html
├── assets/
│   └── css/
│       └── style.css
└── js/].
Network: Request URL [https://github.com/tuan1143/K20_Portfolio_CNTT20_02.git], Status [404].
Tôi dự đoán [Đường dẫn import/link đến tệp CSS bị sai].
Hãy nêu giả thuyết, dữ kiện cần kiểm tra và bản sửa tối thiểu.
Chỉ tư vấn, không sửa tệp. Không kết luận đã sửa thành công. ]

- Gợi ý chính của AI:

  [ thay đường dẫn tham chiếu D:\CNTT20-04\portfolio\css\style.css bằng css\style.css ]

## 3. Quyết định của tôi

- [x] Chấp nhận gợi ý
- [ ] Chỉnh sửa gợi ý rồi áp dụng
- [ ] Bác bỏ gợi ý

- Tôi quyết định làm gì: [ Thay thế đường dẫn tệp CSS hiện tại trong file indexl.html thành đường dẫn tương đối đúng chuẩn (css/style.css) để tương thích với cơ chế định tuyến của GitHub Pages. ]
- Lý do, dựa trên dữ kiện nào: [ Dựa trên dữ kiện Network trả về lỗi 404 và cấu trúc dự án thực tế trên GitHub, nguyên nhân do thẻ link stylesheet đang trỏ sai vị trí thư mục gốc, khiến trình duyệt không tìm thấy file style.css ]

## 4. Thực hiện và kiểm chứng

- Tệp/vị trí đã sửa (không sửa thì ghi rõ): [ indexl.html ]
- Nội dung thay đổi hoặc cách xử lý khác: [ Sửa lại thẻ <link> gọi tệp CSS sang đường dẫn tương đối đúng chuẩn: <link rel="stylesheet" href="css/style.css"> ]
- Commit của bản sửa, nếu có: [ sửa lần 1 ]
- Bản sửa đã deploy: [X] Có  [ ] Chưa  [ ] Không phát sinh bản sửa

| Nội dung kiểm tra | Trước xử lý | Sau xử lý/thử lại |
| --- | --- | --- |
| Request URL và Status của tài nguyên liên quan | [ Status: 404 Not Found ] | [ Status: 200 OK ] |
| Giao diện/chức năng trên URL website | [ Trang giới thiệu mất toàn bộ CSS, hiển thị dạng văn bản thuần túy, vỡ bố cục. ] | [ Giao diện hiển thị đầy đủ màu sắc, định dạng, bố cục chuẩn chỉnh theo thiết kế. ] |

- Cách thử lại và kết quả thực tế: [ Commit và push code lên GitHub, chờ GitHub Pages cập nhật, sau đó mở lại trang [https://tuan1143.github.io/K20_Portfolio_CNTT20_02/about.html](https://tuan1143.github.io/K20_Portfolio_CNTT20_02/about.html), nhấn F12 kiểm tra tab Network thấy file style.css tải thành công (Status 200) và giao diện đã load style đầy đủ. ]
- Căn cứ để đối chiếu (URL tệp, commit, đường dẫn ảnh chụp hoặc dữ kiện quan sát): [ Lịch sử commit trên GitHub repository tuan1143/K20_Portfolio_CNTT20_02 và trạng thái build thành công trên GitHub Pages. ]

## 5. Kết luận

- [X] Đã xử lý được  [ ] Xử lý được một phần  [ ] Chưa xử lý được
- Điều tôi rút ra hoặc việc cần làm tiếp: [ Khi triển khai các trang web tĩnh (static website) lên GitHub Pages dạng Project Site, cần đặc biệt chú ý sử dụng đường dẫn tương đối hoặc bao gồm tên repository trong đường dẫn tuyệt đối để tránh lỗi 404 đối với các tài nguyên tĩnh như CSS, JS và hình ảnh. ]

---

*Tệp là minh chứng MC2 để nhận định mức đạt của tiết học; không tính điểm MC2 riêng. Nếu có tình huống khác, sao chép mục 1–5 để ghi thêm.*
