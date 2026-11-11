# Hidden Text Injection Demo

Dự án này minh họa cách chèn thông điệp ẩn vào văn bản bằng Unicode Tag characters và các kỹ thuật tương tự như zero-width text, nhằm phục vụ mục đích nghiên cứu, giáo dục và kiểm thử an toàn dữ liệu.

## Tổng quan

Project bao gồm:

- `index.html`: giao diện demo chạy trực tiếp trên trình duyệt, cho phép tạo, giải mã, quét và làm sạch văn bản với payload ẩn.

Mục tiêu của dự án là giúp người dùng hiểu cách các payload ẩn có thể được nhúng trong text, cũng như cách phát hiện và xử lý chúng trước khi dữ liệu đi vào hệ thống AI hoặc các ứng dụng khác.

## Tính năng

- Mã hóa ASCII sang Unicode Tag characters
- Mã hóa UTF-8 sang Unicode Tag characters (hỗ trợ tiếng Việt)
- Ẩn payload ở cuối văn bản (`hide`)
- Giải mã payload ẩn (`decode`)
- Quét và phát hiện ký tự ẩn (`scan`)
- Làm sạch văn bản (`clean`)
- Demo giao diện web tương tác để thử nghiệm ngay trên browser

## Cấu trúc project

```text
.
├── invisible.html
└── README.md
```

## Chạy demo trên trình duyệt

1. Mở file `index.html` trong trình duyệt.
2. Chọn tab `Encode/Edit` hoặc `Decode/Clear`.
3. Nhập văn bản, chọn mode mã hóa/giải mã và nhấn nút tương ứng.

Demo này xử lý dữ liệu ngay trên client-side, không cần backend hoặc dịch vụ ngoài.

## Lưu ý về an toàn và hợp pháp

- Đây là công cụ phục vụ mục đích giáo dục, nghiên cứu và kiểm thử môi trường an toàn.
- Không nên dùng kỹ thuật ẩn văn bản để vượt qua chính sách, kiểm soát nội dung hoặc quyền hạn của hệ thống AI.
- Trước khi đưa dữ liệu vào LLM hoặc pipeline xử lý tự động, nên quét và làm sạch input nếu có khả năng chứa ký tự ẩn.
- Nếu dùng cho môi trường production, hãy triển khai kiểm tra/strip dữ liệu đầu vào theo tiêu chuẩn của bạn.

## Dữ liệu nào được xử lý?

- Unicode Tag characters
- Zero-width characters
- Payload dạng văn bản và UTF-8
- Chuỗi ẩn có thể được phát hiện bằng quét và giải mã

## Tài liệu tham khảo

Dự án dựa trên các kỹ thuật ẩn văn bản thông qua Unicode tag và zero-width characters, được sử dụng trong nghiên cứu về prompt injection, hidden text và kiểm soát đầu vào dữ liệu.

## License

Dự án này được cung cấp "as-is" cho mục đích học tập và nghiên cứu. Không có giấy phép thương mại cụ thể được gắn kèm.