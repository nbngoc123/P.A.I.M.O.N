# Genshin Data — từ gameplay đến dataset

## Mục tiêu

Giữ được nguồn video, thời gian, ảnh và quyết định gán nhãn trong một luồng có thể mở lại để sửa, thay vì tạo nhiều thư mục ảnh/nhãn không biết thuộc phiên nào.

## Luồng sử dụng

1. Chọn loại dữ liệu: thông tin cơ bản, Boss Vision hoặc cả hai.
2. Thu phiên chơi bằng OBS; lưu video raw, ảnh mốc và metadata.
3. Xử lý video theo timestamp/PTS; chọn vùng xanh, vùng đỏ và cấu hình crop.
4. Mở màn hình label: vẽ/sửa box, dùng AI gợi ý nếu muốn, duyệt từng frame.
5. Gán đoạn state/action/mechanic ngay cùng màn hình label; sửa bộ nhãn theo từng Boss.
6. Xuất hoặc cập nhật dataset; có thể chọn một đoạn để xuất subdataset.
7. Boss Vision đọc dataset đã xuất để huấn luyện và đánh giá; luồng label vẫn thuộc Genshin Data.

## Những loại nhãn khác nhau

| Loại | Câu hỏi được trả lời |
|---|---|
| Box Boss | Boss ở vị trí nào trong ảnh? |
| Box vật thể/tín hiệu | Cột, vật thể hoặc dấu hiệu cơ chế ở đâu? |
| Nhãn đoạn thời gian | Hành động/cơ chế nào xảy ra trong khoảng nào? |
| ROI crop | Cần quan sát vùng giao diện nào để nhận tín hiệu? |
| Duyệt/loại | Dữ liệu nào được phép dùng làm nhãn thật? |

Không đồng nhất “không có box Boss” với “không xảy ra state”. Khung hình chưa label box cũng không tự trở thành ảnh âm của detector. Cách hiểu khoảng trống của nhãn thời gian được cấu hình theo mức độ người dùng đã rà dataset.

[Xem mẫu dataset Thằn Lằn](dataset-card.md).
