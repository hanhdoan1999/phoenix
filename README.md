# Hanh Doan, portfolio

Trang tĩnh (HTML, CSS, JS), không cần build.

## Cấu trúc
- `index.html`: toàn bộ trang (CSS và JS nằm trong file, ảnh chân dung nhúng sẵn)
- `vendor/`: Three.js r128 và GSAP 3.12.5 (đã tải về, không phụ thuộc CDN)
- `og.jpg`: ảnh xem trước khi chia sẻ link (LinkedIn, Facebook, Zalo)
- `favicon-*.png`, `apple-touch-icon.png`: biểu tượng tab và màn hình chính
- `robots.txt`, `sitemap.xml`, `vercel.json`: SEO và cấu hình Vercel

## Chạy thử trên máy
```bash
npx serve .
```
Mở địa chỉ hiện ra (thường là http://localhost:3000).

## Triển khai lên Vercel
1. Tạo repo mới trên GitHub, đẩy toàn bộ thư mục này lên nhánh `main`:
   ```bash
   git init && git add . && git commit -m "Portfolio"
   git branch -M main
   git remote add origin https://github.com/<ten-ban>/hanhdoan-portfolio.git
   git push -u origin main
   ```
2. Vào https://vercel.com, đăng nhập bằng GitHub, chọn **Add New → Project**, chọn repo vừa tạo.
3. **Project Name**: `hanhdoan` (địa chỉ sẽ là `hanhdoan.vercel.app`).
   Framework Preset: **Other**. Để trống Build Command và Output Directory.
4. Bấm **Deploy**.

Nếu tên `hanhdoan` đã có người dùng, Vercel báo trùng. Khi đó đổi tên (ví dụ `hanh-doan`) và sửa 4 chỗ có `hanhdoan.vercel.app` trong `index.html`, cùng `robots.txt`, `sitemap.xml`.

## Sau khi lên mạng
- Dán link vào LinkedIn Post Inspector và Facebook Sharing Debugger để làm mới ảnh xem trước.
- Mỗi lần đẩy mã lên `main`, Vercel tự đăng lại.
