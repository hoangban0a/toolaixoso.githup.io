# toolaixoso.githup.io

Trang này là bản local của giao diện "Tool xổ số siêu tốc" (dựng bởi LadiPage). Mở [index.html](index.html) để xem và chạy giao diện.

## Tổng quan
Tool mô phỏng giao diện phân tích số dành cho "678 VIP" với các thành phần chính:
- Canvas nền mạng lưới: element `#net-bg` ([#net-bg](index.html)).
- Chat / composer tương tác (nhập mã kỳ 8 số) và hàm xử lý: [`generate`](index.html), [`addResult`](index.html), [`typeText`](index.html).
- Lock screen với mật khẩu cứng: danh sách `validPasses` và hàm kiểm tra [`checkPass`](index.html).
- Audio SFX cho mô phỏng quay: [`startDiceSFX`](index.html), [`stopDiceSFX`](index.html).
- RNG dựa trên seed: [`mulberry32`](index.html), [`pickUnique`](index.html).
- Luồng lịch sử thắng giả lập: API nội bộ `SessionFeed.push` ([`SessionFeed.push`](index.html)).

## Cài đặt & chạy
1. Clone hoặc copy workspace vào máy.
2. Mở trình duyệt và mở tệp [index.html](index.html).
3. Cho phép phát âm thanh nếu muốn nghe hiệu ứng (trình duyệt yêu cầu tương tác người dùng).

## Sử dụng nhanh
- Nhập mã kỳ (8 chữ số) vào ô trên giao diện và nhấn "Gửi" / "Phân tích".
- Nếu bật lock-screen, nhập một trong các mật khẩu hợp lệ để mở: danh sách lưu trong `validPasses` ([`validPasses`](index.html)) và kiểm tra bởi [`checkPass`](index.html).
- Lịch sử thắng được tạo tự động bởi `SessionFeed.push`.

## Ghi chú kỹ thuật
- Mã toàn bộ nằm trong [index.html](index.html) (CSS, JS nội tuyến).
- Các hàm chính để tham khảo: [`generate`](index.html), [`addResult`](index.html), [`typeText`](index.html), [`mulberry32`](index.html), [`pickUnique`](index.html), [`startDiceSFX`](index.html), [`checkPass`](index.html).
- Tệp README hiện tại: [README.md](README.md).

## Bản quyền / nguồn
Giao diện & script gốc do LadiPage/author tạo; tài nguyên ảnh được tải từ CDN trong [index.html](index.html)