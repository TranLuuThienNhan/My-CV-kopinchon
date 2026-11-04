# My-CV-kopinchon

Trang CV/portfolio cá nhân của **Trần Lưu Thiện Nhân**, giới thiệu bản thân, kỹ năng, một số dự án và thông tin liên hệ. Dự án là website tĩnh, được xây dựng để hiển thị trên cả máy tính và thiết bị di động.

## Chức năng

- Giới thiệu cá nhân và vai trò.
- Trình bày các kỹ năng.
- Hiển thị các dự án tiêu biểu dưới dạng thẻ.
- Cung cấp thông tin liên hệ.
- Điều hướng đến từng phần trong trang và nút quay lại đầu trang.
- Bố cục responsive, hỗ trợ màn hình điện thoại, máy tính bảng và máy tính.

## Công nghệ sử dụng

- **HTML5**: cấu trúc và nội dung trang.
- **CSS3**: giao diện, Flexbox, CSS Grid và thiết kế responsive.
- **Python 3 (tùy chọn)**: chạy máy chủ web tĩnh khi thử nghiệm trên máy cá nhân.
- **Docker và Apache HTTP Server (tùy chọn)**: phục vụ website trong container.

Website hiện không sử dụng JavaScript, framework, backend hay cơ sở dữ liệu. Không cần cài đặt thư viện hoặc chạy lệnh build.

## Yêu cầu môi trường

Để xem trang, cần có một trình duyệt web hiện đại như Chrome, Firefox, Edge hoặc Safari.

Để chạy máy chủ web cục bộ, cài đặt **Python 3**. Để chạy bằng Docker, cần cài đặt **Docker Desktop** (Windows/macOS) hoặc Docker Engine (Linux) và khởi động Docker.

## Cấu trúc dự án

```text
My-CV-kopinchon/
├── index.html
├── README.md
└── assets/
    ├── css/
    │   └── styles.css
    └── img/
        ├── ảnh the.jpg
        ├── câu nói hay.jpg
        ├── học sinh giỏi.jpg
        ├── tháo pc.jpg
        └── vô địch.jpg
```

## Cài đặt và chạy thử

### Cách nhanh: mở trực tiếp bằng trình duyệt

1. Tải hoặc giải nén thư mục dự án.
2. Mở `index.html` bằng trình duyệt.

### Windows

Mở PowerShell hoặc Windows Terminal, chuyển đến thư mục dự án rồi chạy:

```powershell
cd đường-dẫn\đến\My-CV-kopinchon
py -m http.server 8000
```

Nếu lệnh `py` không có trên máy, thử:

```powershell
python -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trên trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
cd /đường/dẫn/đến/My-CV-kopinchon
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trên trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### Linux

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
cd /đường/dẫn/đến/My-CV-kopinchon
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trên trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

> Nếu máy chưa có Python 3, hãy cài Python 3 theo hướng dẫn của hệ điều hành hoặc dùng phương án Docker bên dưới.

## Chạy bằng Docker

Đảm bảo Docker đã được cài đặt và đang chạy. Mở terminal tại thư mục gốc của dự án, sau đó chạy lệnh phù hợp với hệ điều hành.

**Windows PowerShell:**

```powershell
docker run --rm -p 8080:80 -v "${PWD}:/usr/local/apache2/htdocs:ro" httpd:2.4
```

**macOS hoặc Linux:**

```bash
docker run --rm -p 8080:80 -v "$PWD:/usr/local/apache2/htdocs:ro" httpd:2.4
```

Lần đầu chạy, Docker sẽ tải image `httpd:2.4` nếu image chưa có trên máy. Khi container khởi động, mở [http://localhost:8080](http://localhost:8080). Dừng container bằng `Ctrl+C`; tùy chọn `--rm` sẽ tự xóa container sau khi dừng.

## Cấu hình và tùy chỉnh

Dự án hiện không có tệp cấu hình riêng hoặc bước cài đặt phụ thuộc.

- Chỉnh nội dung, tiêu đề và thông tin trong `index.html`.
- Chỉnh màu sắc, bố cục và kiểu hiển thị trong `assets/css/styles.css`.
- Thay ảnh trong `assets/img/`; nếu đổi tên hoặc vị trí ảnh, cập nhật đường dẫn tương ứng trong `index.html`.
- Trước khi phát hành, cập nhật thông tin liên hệ và các đường dẫn hồ sơ. Liên kết GitHub và LinkedIn trong trang hiện đang dùng `href="#"`, cần thay bằng URL thực tế.

## Thông tin liên hệ

- **Tên:** Trần Lưu Thiện Nhân
- **Email:** [zenotnhan@gmail.com](mailto:zenotnhan@gmail.com)
- **GitHub:** [github.com/Kopinchon](https://github.com/Kopinchon) (đường dẫn trên trang hiện chưa được liên kết)
- **LinkedIn:** linkedin.com/in/Trần Lưu Thiện Nhân (đường dẫn trên trang hiện chưa được liên kết)