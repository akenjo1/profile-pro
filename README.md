# Trang hồ sơ cá nhân

Trang link-in-bio một file, không cần máy chủ: gom link các app, mỗi app có mã QR quét được, kèm hiệu ứng rơi đổi theo mỗi lần chạm.

## Trong repo này có gì

| File | Vai trò |
|---|---|
| `index.html` | Trang công khai. Đây là file duy nhất được đưa lên GitHub. |
| `.gitignore` | Chặn `admin.html` lọt lên repo. |

## File KHÔNG có trong repo

`admin.html` — công cụ chỉnh sửa, **giữ trong máy, không bao giờ commit**.

Repo công khai thì ai cũng tải file về được. Tệ hơn: file đã lỡ commit vẫn nằm trong lịch sử git kể cả sau khi xoá. Nếu lỡ đẩy lên, cách chắc chắn nhất là tạo repo mới.

## Cách cập nhật trang

**Cách nhanh — đăng thẳng từ trình duyệt:**

1. Mở `admin.html`, nhập PIN
2. Sửa nội dung, bật/tắt app
3. Bấm **🚀 Đăng lên GitHub** — xong, trang thật cập nhật sau khoảng 1 phút

Lần đầu cần điền tài khoản, tên repo và token GitHub trong mục *Đăng thẳng lên GitHub*. Token lấy tại **Settings → Developer settings → Personal access tokens → Fine-grained tokens**, phần *Repository access* chọn **Only select repositories** (chọn đúng repo này), phần *Permissions* bật **Contents: Read and write**. Token chỉ lưu trong trình duyệt, không nằm trong file nào.

Đổi sang máy khác: điền lại thông tin rồi bấm **⬇️ Lấy cấu hình từ GitHub** để kéo về đúng nội dung đang chạy.

**Cách thủ công (không cần token):** bấm **⬇️ Tạo file index.html** rồi tải file đó lên repo, thay cho file cũ.

## Bật GitHub Pages

Vào **Settings → Pages** (mục *Code and automation*) → phần *Build and deployment* → *Source*: chọn **Deploy from a branch** → *Branch*: **main**, thư mục **/ (root)** → **Save**.

Địa chỉ trang sẽ là:

- `https://<tên-tài-khoản>.github.io` nếu repo đặt tên là `<tên-tài-khoản>.github.io`
- `https://<tên-tài-khoản>.github.io/<tên-repo>` với repo tên bất kỳ

Lần đầu có thể mất vài phút mới lên.

## Sao lưu

Trong `admin.html` bấm **🗂 Sao lưu cấu hình** để tải file `.json` chứa toàn bộ thiết lập. Đổi máy hoặc lỡ mất dữ liệu thì dùng **📂 Nạp cấu hình** để khôi phục.

Đừng commit file `.json` này lên repo — `.gitignore` đã chặn sẵn.
