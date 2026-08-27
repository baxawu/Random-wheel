# Challenge Wheel Requirements

## MVP

- Web realtime bằng React/Vite + Express + Socket.IO.
- Không đăng nhập.
- Host tạo phòng với danh sách thử thách hoặc random từ bank mặc định.
- Player join bằng mã phòng hoặc link `?code=XXXXX`.
- Mỗi phòng dùng 10-20 thử thách khác nhau.
- Mỗi lượt chọn một player active và một challenge.
- Wheel phải quay, giảm tốc, dừng ở số thứ tự thử thách rồi mới reveal nội dung.
- Vote `Đạt` / `Chưa đạt`, mỗi player vote một lần.
- Đa số active player chốt kết quả tự động.
- Nếu hòa hoặc chưa có đa số, host quyết định bằng `Chốt Đạt` hoặc `Chốt Chưa đạt`.
- Lưu lịch sử lượt quay in-memory.
- UI tiếng Việt, pastel, mobile-first, màu tương tự Bingo.

## An toàn nội dung

Challenge mặc định không dùng hình phạt thể chất nguy hiểm, không yêu cầu tiết lộ thông tin riêng tư, ưu tiên kể chuyện, diễn tả, đố vui và tương tác nhẹ trong lớp.

## Architecture Requirements

- Domain rule thuần nằm trong `shared/` và có unit test.
- Socket event flow nằm trong `server/socketHandlers.js`.
- Server serialization nằm trong `server/lib/serializers.js` để phân biệt host/player view.
- UI component tái dùng nằm trong `client/src/components/`.
- Content bank nằm trong `client/src/data/`.
- Kiến trúc và event contract phải được document trong `docs/`.
