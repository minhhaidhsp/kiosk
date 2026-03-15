# KIOS kiosk-code — Dev server nhanh

Hai file HTML có trong thư mục:

- `admin-cms.html`
- `kiosk.html`

Mục tiêu: chạy một dev server với live-reload để phát triển và xem 2 trang trên trình duyệt.

Yêu cầu
- Node.js (>=14) và npm (kèm theo Node) hoặc npx.

Script sẵn có (chạy trong PowerShell, ở thư mục project):

```powershell
# Chạy và mở admin-cms.html
npm run start

# Chạy và mở kiosk.html
npm run kiosk

# Chạy server (không tự mở file)
npm run dev
```

Nếu không muốn dùng npx, có thể cài `live-server` toàn cục:

```powershell
npm install -g live-server
live-server --port=3000 --open=admin-cms.html
```

Truy cập thủ công (nếu trình duyệt không tự mở):

- http://127.0.0.1:3000/admin-cms.html
- http://127.0.0.1:3000/kiosk.html

Nếu bạn chưa cài Node.js: tải tại https://nodejs.org (chọn LTS), cài xong mở PowerShell và kiểm tra `node -v`.

Ghi chú
- Port mặc định là 3000; nếu bị chiếm, đổi port trong `package.json` hoặc chạy `npx live-server --port=<PORT>`.
