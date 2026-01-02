# 🚀 Hướng dẫn Deploy SQL Mystery Vietnam

## Các nền tảng miễn phí để host

### 1. 🌟 GitHub Pages (Đề xuất - Dễ nhất)

#### Bước 1: Tạo GitHub Repository
1. Đăng nhập [GitHub](https://github.com)
2. Click **"New repository"**
3. Đặt tên: `sql-mystery-vietnam`
4. Chọn **Public**
5. Click **"Create repository"**

#### Bước 2: Upload files
1. Click **"uploading an existing file"**
2. Kéo thả 2 file:
   - `index.html`
   - `sql_mystery_vietnam.db`
3. Click **"Commit changes"**

#### Bước 3: Bật GitHub Pages
1. Vào **Settings** → **Pages**
2. Source: chọn **"Deploy from a branch"**
3. Branch: chọn **"main"** và **"/ (root)"**
4. Click **Save**

#### Bước 4: Truy cập
- URL của bạn: `https://<username>.github.io/sql-mystery-vietnam/`
- Đợi 1-2 phút để deploy hoàn tất

---

### 2. ⚡ Vercel

#### Bước 1: Chuẩn bị
1. Đăng ký tài khoản tại [vercel.com](https://vercel.com)
2. Liên kết với GitHub

#### Bước 2: Deploy
1. Click **"New Project"**
2. Import từ GitHub repo (sau khi đã push lên GitHub)
3. Click **"Deploy"**

#### Hoặc dùng CLI:
```bash
npm i -g vercel
cd sql_mystery_web
vercel
```

URL: `https://sql-mystery-vietnam.vercel.app`

---

### 3. 🔷 Netlify

#### Cách 1: Drag & Drop (Nhanh nhất)
1. Vào [app.netlify.com/drop](https://app.netlify.com/drop)
2. Kéo thả folder `sql_mystery_web` vào
3. Done! Nhận URL ngay

#### Cách 2: Từ GitHub
1. Đăng nhập [netlify.com](https://netlify.com)
2. Click **"Add new site"** → **"Import an existing project"**
3. Chọn GitHub và repo của bạn
4. Click **"Deploy"**

URL: `https://sql-mystery-vietnam.netlify.app`

---

### 4. 🔥 Cloudflare Pages

1. Đăng nhập [Cloudflare Dashboard](https://dash.cloudflare.com)
2. Vào **Pages** → **Create a project**
3. Kết nối GitHub
4. Chọn repo và deploy

URL: `https://sql-mystery-vietnam.pages.dev`

---

### 5. 🌐 Surge.sh (Dùng CLI)

```bash
npm install -g surge
cd sql_mystery_web
surge
```

Nhập email và chọn domain, ví dụ: `sql-mystery-vietnam.surge.sh`

---

## 📁 Cấu trúc thư mục cần upload

```
sql_mystery_web/
├── index.html              # Trang web chính
└── sql_mystery_vietnam.db  # Database SQLite
```

**Chỉ cần 2 file này là đủ!**

---

## ⚠️ Lưu ý quan trọng

### Về CORS và Database
- Database được load bằng `fetch()`, cần server hỗ trợ static files
- Các nền tảng trên đều hỗ trợ tốt

### Về kích thước file
- Database: ~500KB - OK với tất cả các nền tảng
- GitHub Pages limit: 1GB/repo
- Netlify limit: 100MB/site (miễn phí)
- Vercel limit: 100MB

### Custom Domain (Tùy chọn)
Tất cả các nền tảng đều hỗ trợ custom domain miễn phí:
1. Mua domain (Namecheap, GoDaddy, Tenten.vn...)
2. Cấu hình DNS theo hướng dẫn của từng nền tảng

---

## 🎯 Đề xuất: Dùng GitHub Pages

**Lý do:**
1. ✅ Hoàn toàn miễn phí
2. ✅ Dễ setup nhất
3. ✅ URL đẹp: `username.github.io/sql-mystery-vietnam`
4. ✅ Có thể dùng custom domain
5. ✅ Cộng đồng có thể contribute

---

## 🔧 Troubleshooting

### Database không load được
- Kiểm tra file `sql_mystery_vietnam.db` đã upload chưa
- Kiểm tra tên file chính xác (case-sensitive)
- Mở DevTools (F12) → Console để xem lỗi

### Trang trắng
- Đợi 1-2 phút sau khi deploy
- Clear cache trình duyệt (Ctrl+Shift+R)

### Lỗi CORS
- Đảm bảo dùng các nền tảng static hosting
- Không mở file HTML trực tiếp bằng `file://`

---

## 📞 Liên hệ hỗ trợ

Nếu gặp vấn đề, tạo Issue trên GitHub repo của bạn!

**Chúc bạn deploy thành công! 🎉**
