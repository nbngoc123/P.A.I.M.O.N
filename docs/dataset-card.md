# Dataset card — Thằn Lằn Ánh Trăng Bức Xạ

## Nguồn được giới thiệu

- Phiên gameplay tự thu: `20261111-235058-e2e170d8`.
- Bản dataset chọn làm nguồn mẫu: `boss-dataset-b5f271b2d622-full-event2`.
- Số liệu từ manifest của bản này: **1.202 frame**, **1.081 frame đã label box**, **121 frame chưa label box**; trong số đã label có **1.061 frame dương** và **20 frame âm**.
- Nhịp trích ảnh: **10 FPS**. Có **36 bản ghi nhãn thời gian** trong manifest và hai loại crop: `ken_buc_xa`, `khieng_la_chan`.
- Hai lớp box: Boss và Đá Neo Mặt Trăng.

Đây là thống kê của **một bản xuất**, không phải tổng số dữ liệu dự án và không phải thống kê test độc lập. Mức duyệt nhãn box và mức duyệt nhãn thời gian là hai thông tin khác nhau.

## Mẫu công khai

Xem [sample.json](../samples/lizard/sample.json) để biết số frame thật được đóng gói, các cửa sổ đã chọn và nguồn hash. Mẫu gồm các cửa sổ ngắn giữ nguyên timestamp; không nối các đoạn xa nhau thành một chuỗi liên tục giả.

- `images/`: ảnh gameplay gốc từ bản xuất, không vẽ nhãn dự đoán vào ảnh training.
- `labels/`: nhãn YOLO tương ứng.
- `crops/`: ảnh crop đi kèm đúng frame và mã vùng.
- `annotations.jsonl`: box, trạng thái duyệt, timestamp và liên kết ảnh/crop.
- `temporal-events.jsonl`: các nhãn thời gian giao với cửa sổ mẫu; giữ biên sự kiện gốc và ghi thêm phần giao của mẫu.
- `object-boxes.jsonl`, `class-map.json`, `regions.json`, `mechanics.jsonl`: vật thể, lớp, vùng và định nghĩa cơ chế.
- `checksums.json`: SHA-256 để kiểm tra file.

Mẫu để đọc cấu trúc và đối chiếu ảnh/nhãn. Không đủ để train model hoặc công bố chất lượng tổng quát. Không có split validation/test độc lập trong mẫu này.

[Tải toàn bộ mẫu nhỏ dạng ZIP](https://github.com/nbngoc123/P.A.I.M.O.N/releases/download/lizard-showcase-v0.1/paimon-lizard-dataset-sample-v0.1.zip).

## Chất lượng và giới hạn

Nhãn có thao tác người dùng duyệt, một số bắt đầu từ AI gợi ý rồi được duyệt/sửa. Điều đó không loại trừ lỗi người gán nhãn. Hiệu ứng, che khuất và vật thể nhỏ là các tình huống cần rà thêm.

Timestamp/PTS cho biết vị trí trong media; không tự chứng nhận đồng bộ chính xác với đầu vào bàn phím hoặc sự kiện nội bộ game. Dữ liệu raw toàn phiên không được commit vào Git.

Ảnh gameplay có thể còn UID hiển thị trong hình. Mẫu chia sẻ là nội dung người dùng chủ động chọn từ phiên của mình. Chưa gán giấy phép tái sử dụng mở cho dataset; nội dung game thuộc chủ sở hữu tương ứng.
