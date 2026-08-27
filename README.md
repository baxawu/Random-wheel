# Challenge Wheel

Game vòng quay thử thách realtime cho lớp học. Host tạo phòng, người chơi tham gia bằng mã phòng hoặc link, mỗi lượt quay chọn ngẫu nhiên một người chơi active và một thử thách an toàn. Cả phòng vote `Đạt` hoặc `Chưa đạt`; kết quả tự chốt khi đạt đa số, còn hòa thì host quyết định.

## Chạy local

```bash
npm install
npm run dev
```

Server mặc định chạy ở `http://localhost:6683`, client Vite ở cổng Vite tự chọn.

## Scripts

```bash
npm test          # unit tests
npm run typecheck # TypeScript check cho client
npm run build     # production build
npm start         # serve production dist bằng Express
```

## Tính năng

- Tạo/join phòng realtime bằng Socket.IO.
- Random active player + challenge.
- Wheel quay chậm dần, mũi tên dừng ở số thử thách rồi mới hiện nội dung.
- Bank mặc định khoảng vài nghìn thử thách tiếng Việt an toàn cho trẻ em.
- Mỗi phòng dùng 10-20 thử thách.
- Tùy chọn cho phép lặp thử thách và cho người chơi bấm quay.
- Vote một lần mỗi người, đa số active player tự chốt kết quả.
- Khi vote hòa/chưa đủ đa số, host chọn `Chốt Đạt` hoặc `Chốt Chưa đạt`.
- Host có thể tạm nghỉ/active người chơi và kết thúc phòng.
- Reconnect bằng `localStorage`.

## Documentation

- [Architecture](docs/ARCHITECTURE.md)
- [Socket events](docs/EVENTS.md)
- [Requirements](requirements.md)
