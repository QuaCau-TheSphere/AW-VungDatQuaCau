---
share: true
created: 2026-08-18T15:48
updated: 2026-08-23T16:24
---

```js
title = case frontmatter.title {
    "$filename", "", nil -> filename
    "$h1" -> h1
    _ -> frontmatter.title 
}

description = case frontmatter.description {
    "$h2", "", nil -> h2Elements.join(". ")
    "$p" -> body.pElements[0]
    "$alias" -> frontmatter.aliases[0]
    _ -> frontmatter.description 
}
description = case frontmatter.ogTitle {
    "$title", "", nil -> title
    _ -> frontmatter.ogTitle 
}
```
[Các thẻ meta có thể lấy dữ liệu được gán nhãn từ dataview inline](./Frontmatter/C%C3%A1c%20th%E1%BA%BB%20meta%20c%C3%B3%20th%E1%BB%83%20l%E1%BA%A5y%20d%E1%BB%AF%20li%E1%BB%87u%20%C4%91%C6%B0%E1%BB%A3c%20g%C3%A1n%20nh%C3%A3n%20t%E1%BB%AB%20dataview%20inline.md)

| Vai trò                                                                                                            | Vị trí xuất hiện                                                    | Cách điều chỉnh | Nếu không điều chỉnh thì mặc định sẽ lấy giá trị từ | Sử dụng khi                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- | --------------- | --------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| Quản lý tập tin từ hệ điều hành. Tạo slug                                                                          | filename: lúc xuất file, terminal, Windows Explorer, dữ liệu Dataview                | filename        | Luôn có                                             | Luôn sử dụng                                                                                                         |
| Cho phép filename không phải slugify quá nhiều ký tự đặc biệt                                                      | Enveloppe tạo git                                                   | `filename`      | filename                                            | Có thể dùng khi gặp tên dài, và thấy việc tránh alias dài quan trọng hơn việc URL trên web và trên vault giống nhau* |
| Nhận diện bài viết, tóm tắt nội dung, quản lý theo cấu trúc của tác giả hoặc người đang tìm kiếm theo một cấu trúc | Tiêu đề: trên cao, file explorer, breadcrumb, menu, navigation pane | `title`         | filename                                            | Tiêu đề chứa ký tự đặc biệt hoặc quá dài*. Tiêu đề đọc từ cây thư mục giống với tiêu đề nội dung về mặt ngữ nghĩa    |
| Tạo dự đoán cho người đọc về nội dung bên trong, làm cho họ thấy vì sao họ cần đọc bài đó, đáp ứng câu hỏi của họ  | Headline (`<title>`, `<h1>`)                                        | Markdown `#`    | `title`, filename                                   | Mental model của người đã hiểu nó rồi khác với mental model của người chưa hiểu nó                                   |
| Nối tiếp dòng suy nghĩ                                                                                             | Liên kết (`[[]]`, `<a>`)                                            | `alias`         | `title`, filename                                   |                                                                                                                      |
|                                                                                                                    | Search autocomplete, kết quả Google                                 | Không cần chỉnh | `alias`, `title`, filename                          |                                                                                                                      |
| Tiêu đề lúc chia sẻ trên Facebook                                                                                  | Tiêu đề trong Open Graph (`meta property="og:title"`)               | `ogTitle`       | `title`, filename                                   |                                                                                                                      |

