# TS – plugin SketchUp

Bộ plugin TS cho **SketchUp 2027** (Windows). Repo này chỉ chứa file cài đặt (`.rbz`) trong mục **Releases**, không chứa source.

| Bộ | File | Gồm |
|---|---|---|
| TS Section | `00.TS_Section_v*.rbz` | Mặt cắt + hatch, View Frame, MView, ViewBox, thư viện hatch, ẩn nét, nhận diện tag |
| TS Sheets | `00.TS_Sheets_v*.rbz` | Tờ bản vẽ, ghi chú / dim / dummy, quy trình model → bản vẽ, Layout |
| TS Edit | `00.TS_Edit_v*.rbz` | Công cụ chỉnh sửa, dán từ AutoCAD, View cube |
| TS System | `00.TS_System_v*.rbz` | Health Check, Fix Plugin, **TS Updater** (tự cập nhật) |
| TS Export | `00.TS_Export_v*.rbz` | Xuất DWG 2D + PNG |
| TS Tray | `00.TS_Tray_v*.rbz` | Khung Tray và công cụ dựng model |
| TS.Animation | `00.TS_Animation_v*.rbz` | Tháo dỡ / lắp đặt theo bước |

## Cài đặt lần đầu

1. Vào [Releases](../../releases/latest), tải file `.rbz` của bộ cần dùng. Nên cài **TS System** để có tự cập nhật.
2. SketchUp → **Extensions › Extension Manager › Install Extension** → chọn file `.rbz`.
3. Khởi động lại SketchUp.

## Cập nhật

- **Extensions › TS Updater › Kiểm tra cập nhật...**: kiểm mọi bộ TS đang cài, hỏi trước khi tải, kiểm mã SHA-256 rồi cài. Cài xong cần khởi động lại SketchUp.
- Tự kiểm khi mở SketchUp: tắt mặc định, bật trong cùng menu (1 lần / ngày).
- Cài tay: tải `.rbz` mới ở Releases rồi cài như lần đầu (cài đè bản cũ).

Mỗi file `.rbz` đi kèm file `.rbz.sha256` để kiểm tra file tải về không bị lỗi hay bị thay.

## Lưu ý

- Code trong file `.rbz` là Ruby mà SketchUp phải đọc được để chạy, nên **không được bảo vệ khỏi việc sao chép**. Repo này không chứa source gốc, nhưng không khẳng định code không thể bị đọc lại.
- Plugin chỉ kết nối mạng khi kiểm tra cập nhật (tới `api.github.com` và máy chủ tải file của GitHub), qua HTTPS.
- Dùng plugin với mức rủi ro của bạn; nên lưu file model trước khi cài bản mới.
