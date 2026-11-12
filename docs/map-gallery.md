# Map — demo từ hai video gameplay raw

Các video này chạy chính worker `Tracker` của Genshin Visual Localizer, sau đó đưa kết quả vào `SpatialState`, `OverlayController`, `MapCanvas` và HUD điều hướng sẵn có. Tọa độ được suy luận từ minimap; không gán đường đi hay tọa độ ground truth.

Đầu vào raw 1920×1080, 60 FPS. Bộ định vị lấy mẫu 4 lần/giây theo thời gian video; video kết quả 30 FPS giữ kết quả định vị gần nhất. Đây là replay offline, không phải phép đo FPS Live. Thao tác chọn ghim, bật chế độ và hoàn tác được thực hiện bằng kịch bản lúc replay; tiến độ lưu riêng cho demo.

| Demo | Phiên raw | Mẫu định vị được chấp nhận | Thời lượng bản xuất |
|---|---|---:|---:|
| Định vị và bám vị trí | `20261112-210751-21172158` | 155/157 | 39.2s |
| Điều hướng tới ghim | `20261112-211224-4678a89b` | 134/137 | 34.2s |
| Thu thập đặc sản và hoàn tác | `20261112-211224-4678a89b` | 134/137 | 34.2s |

Số mẫu được chấp nhận là trạng thái khớp hình học/theo dõi qua bộ lọc của tool, không phải độ chính xác trên tọa độ đối chứng. Khoảng cách hiển thị theo đơn vị map, chưa quy đổi sang mét.

## Định vị và bám vị trí

[Tải video MP4](https://raw.githubusercontent.com/nbngoc123/P.A.I.M.O.N/main/media/map/replay/tracking/demo.mp4) · [Nguồn và cấu hình](../media/map/replay/tracking/provenance.json)

**3.0s — Định vị và bám vị trí.**

![Định vị và bám vị trí](../media/map/replay/tracking/01-003.0s.jpg)

**7.5s — Định vị và bám vị trí.**

![Định vị và bám vị trí](../media/map/replay/tracking/02-007.5s.jpg)

**12.0s — Định vị và bám vị trí.**

![Định vị và bám vị trí](../media/map/replay/tracking/03-012.0s.jpg)

**16.5s — Định vị và bám vị trí.**

![Định vị và bám vị trí](../media/map/replay/tracking/04-016.5s.jpg)

**21.0s — Định vị và bám vị trí.**

![Định vị và bám vị trí](../media/map/replay/tracking/05-021.0s.jpg)

**25.5s — Định vị và bám vị trí.**

![Định vị và bám vị trí](../media/map/replay/tracking/06-025.5s.jpg)

**30.0s — Định vị và bám vị trí.**

![Định vị và bám vị trí](../media/map/replay/tracking/07-030.0s.jpg)

**34.5s — Định vị và bám vị trí.**

![Định vị và bám vị trí](../media/map/replay/tracking/08-034.5s.jpg)

## Điều hướng tới ghim

[Tải video MP4](https://raw.githubusercontent.com/nbngoc123/P.A.I.M.O.N/main/media/map/replay/navigation/demo.mp4) · [Nguồn và cấu hình](../media/map/replay/navigation/provenance.json)

Ghim chọn từ catalog thật: **Fairy Wormwood**. Khoảng cách và mũi tên dùng vị trí/hướng suy luận trong từng thời điểm.

**3.0s — Điều hướng tới ghim.**

![Điều hướng tới ghim](../media/map/replay/navigation/01-003.0s.jpg)

**7.5s — Điều hướng tới ghim.**

![Điều hướng tới ghim](../media/map/replay/navigation/02-007.5s.jpg)

**12.0s — Điều hướng tới ghim.**

![Điều hướng tới ghim](../media/map/replay/navigation/03-012.0s.jpg)

**16.5s — Điều hướng tới ghim.**

![Điều hướng tới ghim](../media/map/replay/navigation/04-016.5s.jpg)

**21.0s — Điều hướng tới ghim.**

![Điều hướng tới ghim](../media/map/replay/navigation/05-021.0s.jpg)

**25.5s — Điều hướng tới ghim.**

![Điều hướng tới ghim](../media/map/replay/navigation/06-025.5s.jpg)

**30.0s — Điều hướng tới ghim.**

![Điều hướng tới ghim](../media/map/replay/navigation/07-030.0s.jpg)

## Thu thập đặc sản và hoàn tác

[Tải video MP4](https://raw.githubusercontent.com/nbngoc123/P.A.I.M.O.N/main/media/map/replay/collection/demo.mp4) · [Nguồn và cấu hình](../media/map/replay/collection/provenance.json)

Bán kính 17 đơn vị map; đã ghi nhận 1 lượt đánh dấu với 3 ghim khác nhau, chuyển mục tiêu rồi thực hiện hoàn tác. Theo hành vi gốc của tool, hoàn tác dừng phiên thu thập. Đánh dấu theo khoảng cách chưa xác nhận đã nhặt vật phẩm.

**3.0s — Thu thập đặc sản và hoàn tác.**

![Thu thập đặc sản và hoàn tác](../media/map/replay/collection/01-003.0s.jpg)

**7.5s — Thu thập đặc sản và hoàn tác.**

![Thu thập đặc sản và hoàn tác](../media/map/replay/collection/02-007.5s.jpg)

**8.5s — Đánh dấu cụm ghim và chuyển mục tiêu.**

![Đánh dấu cụm ghim và chuyển mục tiêu](../media/map/replay/collection/event-mark.jpg)

**12.0s — Thu thập đặc sản và hoàn tác.**

![Thu thập đặc sản và hoàn tác](../media/map/replay/collection/03-012.0s.jpg)

**12.5s — Hoàn tác lượt đánh dấu; phiên thu thập dừng.**

![Hoàn tác lượt đánh dấu; phiên thu thập dừng](../media/map/replay/collection/event-undo.jpg)

**16.5s — Thu thập đặc sản và hoàn tác.**

![Thu thập đặc sản và hoàn tác](../media/map/replay/collection/04-016.5s.jpg)

**21.0s — Thu thập đặc sản và hoàn tác.**

![Thu thập đặc sản và hoàn tác](../media/map/replay/collection/05-021.0s.jpg)

**25.5s — Thu thập đặc sản và hoàn tác.**

![Thu thập đặc sản và hoàn tác](../media/map/replay/collection/06-025.5s.jpg)

**30.0s — Thu thập đặc sản và hoàn tác.**

![Thu thập đặc sản và hoàn tác](../media/map/replay/collection/07-030.0s.jpg)

