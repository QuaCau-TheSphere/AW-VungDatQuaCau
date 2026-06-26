---
share: true
created: 2026-02-03T13:43
updated: 2026-06-16T22:01
---
## Mục tiêu
- [Khi nhập hoặc di chuyển tệp thì URL đã chia sẻ vẫn truy cập được](../../Y%C3%AAu%20c%E1%BA%A7u%20ch%E1%BB%A9c%20n%C4%83ng/Chia%20s%E1%BA%BB%20d%E1%BB%AF%20li%E1%BB%87u/Khi%20nh%E1%BA%ADp%20ho%E1%BA%B7c%20di%20chuy%E1%BB%83n%20t%E1%BB%87p%20th%C3%AC%20URL%20%C4%91%C3%A3%20chia%20s%E1%BA%BB%20v%E1%BA%ABn%20truy%20c%E1%BA%ADp%20%C4%91%C6%B0%E1%BB%A3c.md)

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

