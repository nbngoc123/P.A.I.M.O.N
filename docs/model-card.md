# Checkpoint card — Boss Thằn Lằn

## Gói phát hành

[Tải checkpoint detector + temporal](https://github.com/nbngoc123/P.A.I.M.O.N/releases/download/lizard-showcase-v0.1/paimon-lizard-checkpoints-v0.1.zip).

Gói lấy từ **checkpoint đã gán trong profile tại lúc tạo demo**, không tự chọn lại một lượt train khác. Run và SHA-256 được ghi ở [checkpoint-manifest.json](checkpoint-manifest.json), hash file ZIP ở [checkpoint-download.json](checkpoint-download.json).

```text
models/detector.pt
models/temporal.pt
profile.json
checkpoint-manifest.json
```

Các trọng số đã học được giữ nguyên; metadata đường dẫn máy cá nhân được chuyển thành tên tương đối trước khi phát hành. Vì được lưu lại sau khi làm sạch metadata, hash file công khai có thể khác file gốc; manifest ghi cả hai.

## Đầu vào và đầu ra

- **Detector:** ảnh → các lớp box và điểm detection.
- **Temporal:** chuỗi ảnh + feature schema đối tượng + crop/tín hiệu tương ứng checkpoint → các điểm state/mechanic.
- **Alert policy:** không phải trọng số được YOLO học; chuyển điểm temporal thành cảnh báo bằng ngưỡng, xác nhận, reset và cooldown trong profile.

Detector và temporal là hai nhiệm vụ khác nhau. Đổi lớp detector, thứ tự feature hoặc cấu trúc crop có thể làm đầu vào temporal sai. Checkpoint temporal không thể chạy riêng như một file YOLO.

## Phạm vi minh chứng

Demo Thằn Lằn dùng raw gameplay và suy luận từ checkpoint trên. Dữ liệu minh họa có thể thuộc nguồn từng dùng để huấn luyện. Chưa công bố kết quả trên test độc lập cho bộ phát hành này và không đưa mAP pilot cũ của Boss khác vào đây.

Cảnh báo được phát bởi model và policy, có thể sai hoặc muộn. Thông điệp là nội dung người dùng cấu hình, không phải hướng dẫn chiến thuật đã được hệ thống xác minh.

## Phân phối

Checkpoint được chia sẻ để xem xét hiện vật nghiên cứu của dự án; mã nguồn ứng dụng vẫn riêng tư. Công bố checkpoint không đảm bảo che giấu kiến trúc hay mọi chi tiết mô hình. Chưa gán giấy phép mở cho gói; cần phân biệt quyền của tác giả dự án với quyền của các thư viện/mô hình nền và nội dung game.
