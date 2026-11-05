# Metric Lab — bản thử

Website tiếng Việt, gồm 12 câu tính toán và lựa chọn tình huống performance marketing đa ngành, có gợi ý, bài giải có thể mở ngay dưới mỗi câu, lưu tiến độ trên trình duyệt, chấm điểm và giải thích sau khi nộp.

## Chạy

Mở `index.html` bằng trình duyệt, hoặc chạy `python3 -m http.server 8000` từ thư mục này và truy cập qua HTTP nội bộ. Không cần cài dependency hay có backend. Trình duyệt có thể giới hạn lưu localStorage khi mở file trực tiếp; website vẫn cho làm bài trong phiên.

## Triển khai Vercel

Đây là static site. Nếu import repository trên Vercel, chọn Framework Preset **Other**, Root Directory là thư mục chứa `index.html`, không cần lệnh build/install, Output Directory là `.`.

Hoặc từ thư mục này, với Vercel CLI đã xác thực trên máy của bạn:

```sh
vercel deploy --prod
```

Chọn/tạo project riêng cho Metric Lab; không ghi đè project khác. Tài khoản Vercel cần được xác thực để triển khai. Không lưu token vào mã nguồn.

## Giới hạn bản thử

- Dữ liệu bài tập mô phỏng và giả định được ghi trong từng câu, tham khảo tài liệu DPM029 và dạng đề IKAME do người dùng cung cấp.
- Chưa có tự luận, visual brief, AI chấm bài, đăng nhập hay đồng bộ đa thiết bị.
- Đáp án có trong JavaScript phía trình duyệt; phù hợp tự luyện, không dùng làm hệ thống thi bảo mật.
- Lưu tiến độ trong localStorage riêng cho trình duyệt/địa chỉ website; mở từ địa chỉ khác không tự chuyển tiến độ.

## Xác minh

Đã kiểm tra bằng Chromium/Playwright: làm đủ 12 câu đúng, kết quả 12/12, giải thích từng câu, tải kết quả TXT, khôi phục sau reload, màn hình mobile, làm lại, báo số không hợp lệ, gợi ý, điều hướng và nộp bài bỏ trống 0/12.
