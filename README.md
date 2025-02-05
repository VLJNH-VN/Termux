
# Hướng dẫn tạo bot termux

Bạn muốn có một con bot termux như này?

### Bước 1: Tải Termux trên F-droid
- Link tải: [Termux trên F-droid](https://f-droid.org/packages/com.termux/)
- Sau khi tải xong, chuyển qua bước 2.

### Bước 2: Cập nhật và cài đặt Debian
Mở termux và chạy lệnh sau:
```bash
pkg update -y && pkg upgrade -y && pkg install proot-distro -y && proot-distro install debian && proot-distro login debian
```
- (Lưu ý: Do mình đã tải trước đó nên bạn có thể thấy khác với các bạn mới tải.)

### Bước 3: Cài đặt Node.js
Sau khi vào debian, chạy lệnh:
```bash
apt install nodejs -y
```

### Bước 4: Cài đặt NVM (Node Version Manager)
NVM hỗ trợ bạn tải các phiên bản cũ của Node.js:
```bash
curl -o https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash
```

### Bước 5: Tải lại cấu hình bash
Chạy lệnh:
```bash
source ~/.bashrc
```

### Bước 6: Cài đặt phiên bản Node.js
Cài đặt và sử dụng phiên bản Node.js 20:
```bash
nvm install 20
nvm use 20
```

### Bước 7: Cài đặt FileBrowser
FileBrowser giúp bạn quản lý file trên web:
```bash
curl -fsSL https://raw.githubusercontent.com/filebrowser/get/master/get.sh | bash
```
(Lưu ý: Do mình đã cài đặt trước nên có thể bỏ qua bước này.)

### Bước 8: Khởi động FileBrowser
Khởi động FileBrowser với lệnh:
```bash
filebrowser -r ~
```
- (Thay thế `~` bằng đường dẫn thư mục của bạn nếu cần.)

Sau khi chạy, mở trình duyệt web và truy cập `localhost:8080` để xem FileBrowser có hoạt động ổn không.

- **Tài khoản đăng nhập:**
  - **User:** admin
  - **Password:** admin

### Bước 9: Thêm file của bạn vào FileBrowser
Bạn có thể thêm các file vào. Do không có file sẵn, mình sẽ lấy file `miraiv3` và tạo file `test` để chứa Mirai v3.

```bash
cd /tên file bot của bạn/
```

### Bước 10: Chỉnh sửa file `package.json`
Mở file `package.json` trong thư mục bot và tìm mục liên quan đến `canvas`. Sau đó xóa đi.

### Bước 11: Cài đặt phụ thuộc
Chạy lệnh:
```bash
npm i
```
Lưu ý: Quá trình này có thể mất một chút thời gian, hãy kiên nhẫn đợi.

### Bước 12: Cài đặt Cookie hoặc AppState
- Nếu bạn chạy bot với **cookie**, thêm cookie vào file `cookie.txt`.
- Nếu bạn chạy bot với **appstate**, thêm appstate vào `appstate.json`.

Sau khi hoàn thành, chạy lệnh sau để khởi động bot:
```bash
npm start
```

---

Chúc các bạn thành công!
----
Mình có bán file bot khá ngon mọi người có nhu cầu mua ủng hộ mình nhé
Zalo:
```bash
0336176273
