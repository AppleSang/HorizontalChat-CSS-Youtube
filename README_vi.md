# HorizontalChat-CSS-Youtube

Trình chỉnh sửa CSS trên trình duyệt để tạo overlay chat ngang cho YouTube Live Chat. Tin nhắn chat hiển thị trên một dòng ngang với avatar, tên và nội dung nằm cùng hàng.



## Tính năng

- **Xem trước trực tiếp** — Thay đổi settings thấy ngay kết quả
- **Bố cục ngang** — Avatar + Tên + Tin nhắn trên cùng một dòng
- **Màu theo vai trò** — Màu tùy chỉnh cho Mặc định, Mod, Hội viên và Chủ kênh
- **Hỗ trợ Super Chat** — Màu đúng theo tier của YouTube
- **Gifted Membership** — Nền gradient xanh lá đến cyan
- **Bật/tắt Timestamp** — Hiện hoặc ẩn thời gian
- **Ẩn badge Top Chat** — Xóa badge xếp hạng
- **Tương thích OBS** — Copy CSS trực tiếp vào OBS Browser Source
- **Giao diện tối** — Phù hợp cho streamer
- **Tự động lưu** — Settings lưu vào localStorage
- **Đa ngôn ngữ** — Tiếng Việt và tiếng Anh (tự detect theo IP)

## Bắt đầu nhanh

1. Mở `editor.html` trên trình duyệt
2. Điều chỉnh settings ở panel bên trái (typography, màu sắc, bố cục)
3. Dùng các nút preview (Viewer, Mod, Member, Owner, Super Chat, Gift, Join) để test các loại tin nhắn
4. Nhấn **Copy CSS** để copy CSS đã tạo
5. Trong OBS, thêm **Browser Source** trỏ đến URL popout YouTube live chat
6. Paste CSS vào trường **Custom CSS**

## Các loại tin nhắn

| Nút | Mô tả |
|-----|-------|
| Viewer | Tin nhắn người xem thường |
| Mod | Tin nhắn moderator (badge shield tím) |
| Member | Tin nhắn hội viên (badge member xanh lá) |
| Owner | Tin nhắn chủ kênh (tên đỏ) |
| Super Chat | Super chat với đúng màu tier |
| Gift | Tặng hội viên (gradient xanh lá-cyan) |
| Join | Thông báo mới gia nhập hội viên |

## Các cấp màu Super Chat

Dựa trên scheme màu chính thức của YouTube:

| Tier | Số tiền | Màu chính | Màu phụ |
|------|---------|-----------|---------|
| 1 | $1-$2 | Xanh dương `rgb(30,136,229)` | Xanh đậm `rgb(21,101,192)` |
| 2 | $5 | Cyan `rgb(0,229,255)` | Cyan đậm `rgb(0,184,212)` |
| 3 | $10-$20 | Xanh lá `rgb(29,233,182)` | Xanh lá đậm `rgb(0,191,165)` |
| 4 | $50 | Vàng `rgb(255,202,40)` | Vàng đậm `rgb(255,179,0)` |
| 5 | $100 | Cam `rgb(245,124,0)` | Cam đậm `rgb(230,81,0)` |
| 6 | $200-$500 | Hồng `rgb(233,30,99)` | Hồng đậm `rgb(194,24,91)` |
| 7 | $1000+ | Đỏ `rgb(230,33,23)` | Đỏ đậm `rgb(208,0,0)` |

## Màu mặc định

- **Tên**: `#9a8484` (hồng xám)
- **Tên Mod**: `#5541da` (tím)
- **Tên Hội viên**: `#41da93` (xanh lá)
- **Tên Chủ kênh**: `#dd5050` (đỏ)
- **Tin nhắn**: `#ffffff` (trắng)

## Hướng dẫn OBS

1. Trong OBS, nhấn **+** dưới Sources → **Browser**
2. Đặt URL thành URL popout YouTube live chat:
   ```
   https://www.youtube.com/live_chat?is_popout=1&v=VIDEO_ID_CUA_BAN
   ```
3. Đặt Width: `5000`, Height: `200`
4. Tích **Shutdown source when not visible** (tùy chọn)
5. Nhấn **OK**
6. Chuột phải vào Browser Source → **Properties**
7. Cuộn đến **Custom CSS** và paste CSS đã copy
8. Nhấn **OK**

## Credit

- **[Zaladin5x](https://github.com/Zaladin5x)** — CSS bố cục HorizontalChat-CSS-Youtube cơ bản
- **[Touru Baskara](https://ko-fi.com/s/c1037bb627)** — Concept editor & thiết kế GUI
- **[Septapus](https://chatv2.septapus.com/)** — Chat V2 style generator (cảm hứng cho các tính năng tùy chỉnh)
- **[Reza (DekReza)](https://github.com/dekreza)** — Dữ liệu HTML chat & logic rendering

## License

Dự án này là open source. Feel free to use and modify.
