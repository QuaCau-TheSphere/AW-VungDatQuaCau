---
share: true
created: 2026-02-03T13:43
updated: 2026-06-14T11:57
---
Yêu cầu:
- Mỗi ghi chú có một id duy nhất
- Ngắn nhất có thể
- Từ id có thể xác định được là ghi chú gì
- Hai ghi chú có cùng thời gian tạo có id khác nhau
- Dù có chuyển ghi chú đi đâu hoặc thay đổi tiêu đề, nội dung thế nào thì id cũng không đổi
- Nếu phát hiện có hai ghi chú có chung một id (VD: lúc lập kho mới thì sao chép tệp "Tự ngẫm nghĩ, trải nghiệm") thì...

Khi nhập ghi chú lại thì lấy tất cả id?
## Giải pháp
### Khi tạo thì kiểm tra id được tạo gần nhất rồi gán id trong frontmatter luôn
Cần một nơi tập trung để lưu id gần nhất. Khi tạo mới thì cần cập nhật

### Dùng thời gian tạo dưới dạng unix rồi chuyển sang hệ 64
### Xếp theo thứ tự tạo ra rồi gán id từ trên xuống dưới
Có một bảng để chuyển đổi từ id sang thời gian tạo

