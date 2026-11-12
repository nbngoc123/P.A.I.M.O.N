# Mẫu dataset Thằn Lằn

Mẫu chọn từ bản xuất `boss-dataset-b5f271b2d622-full-event2` của phiên `20261111-235058-e2e170d8`.

Mở [sample.json](sample.json) để biết số ảnh và các khoảng thời gian, [annotations.jsonl](annotations.jsonl) để nối ảnh → box → crop, [temporal-events.jsonl](temporal-events.jsonl) để xem các nhãn thời gian giao với mẫu.

Ảnh và crop giữ nguyên pixel bản xuất; nhãn YOLO giữ nguyên. Không coi các cửa sổ tách rời là một chuỗi liên tục. Sự kiện vẫn có biên gốc; trường `sample_overlap_ms` chỉ rõ phần nào có trong mẫu. Mẫu này để đọc và xem, không phải gói đủ dữ liệu để huấn luyện hoặc đánh giá độc lập.

[Dataset card đầy đủ](../../docs/dataset-card.md).
