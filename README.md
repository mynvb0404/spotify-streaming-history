# Spotify Streaming History
Exploratory data analysis of Spotify streaming history to uuncover listening patterns, user behavior and music consumption trends using Python

# 1. Data Overview
| Cột                 | Mô tả                                                                | Kiểu dữ liệu                       |
| ------------------- | -------------------------------------------------------------------- | ---------------------------------- |
| `spotify_track_uri` | Mã định danh của bài hát                                             | `string`                           |
| `ts`                | Thời điểm bài hát dừng phát, theo múi giờ UTC                        | `datetime` (`YYYY-MM-DD HH:MM:SS`) |
| `platform`          | Nền tảng được sử dụng để phát nhạc                                   | `string`                           |
| `ms_played`         | Số mili giây bài hát đã được phát                                    | `int64`                            |
| `track_name`        | Tên bài hát                                                          | `string`                           |
| `artist_name`       | Tên nghệ sĩ                                                          | `string`                           |
| `album_name`        | Tên album                                                            | `string`                           |
| `reason_start`      | Lý do bài hát bắt đầu phát                                           | `string`                           |
| `reason_end`        | Lý do bài hát kết thúc                                               | `string`                           |
| `shuffle`           | Cho biết chế độ phát ngẫu nhiên có được bật hay không                | `boolean`                          |
| `skipped`           | Cho biết bài hát có bị bỏ qua để chuyển sang bài tiếp theo hay không | `boolean`                          |
