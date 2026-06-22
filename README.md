# TechTrend — GitHub Trending Today

Một trang web tĩnh hiển thị danh sách **trending repositories** từ GitHub theo khoảng thời gian và ngôn ngữ lập trình.

🔗 **Trang web trực tiếp:** https://huyzpka-commits.github.io/gihubtrend/

---

## Tính năng

- Xem repository trending theo **Hôm nay**, **7 ngày**, **30 ngày**
- Lọc theo ngôn ngữ: **Tất cả**, **Python**, **JavaScript**, **TypeScript**, **Go**, **Rust**
- Giao diện tối hiện đại, responsive
- Dữ liệu lấy trực tiếp từ **GitHub API**
- Tự động deploy lên **GitHub Pages** mỗi khi push nhánh `main`

---

## Cấu trúc dự án

```
.
├── index.html              # Giao diện chính và logic JavaScript
└── .github/workflows/
    └── pages.yml           # GitHub Actions workflow để deploy GitHub Pages
```

---

## Cách chạy local

Không cần cài đặt thêm, chỉ cần mở file `index.html` trong trình duyệt:

```bash
# macOS/Linux
open index.html

# Windows
start index.html
```

Hoặc dùng một server tĩnh đơn giản:

```bash
python -m http.server 8000
```

Sau đó mở http://localhost:8000

---

## Deploy

Mỗi lần push lên nhánh `main`, workflow `.github/workflows/pages.yml` sẽ tự động build và deploy lên GitHub Pages.

---

## Dữ liệu

Dữ liệu trending được lấy từ GitHub API:

```
https://api.github.com/search/repositories?q=sort:stars&sort=stars&order=desc
```

---

## License

MIT
