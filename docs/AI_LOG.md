# Nhật ký thay đổi

Ghi lại các thay đổi lớn ảnh hưởng đến chức năng, giao diện, cấu trúc, cách chạy hoặc tài liệu quan trọng của dự án. Không cần ghi các chỉnh sửa nhỏ như sửa lỗi chính tả hay định dạng.

## 2026-11-05 — Ghi nhận phiên bản đầu tiên

- Hoàn thành website CV/portfolio cá nhân dạng tĩnh, giới thiệu bản thân, kỹ năng, dự án và thông tin liên hệ.
- Hỗ trợ bố cục responsive trên điện thoại, máy tính bảng và máy tính.
- Có thể mở trực tiếp bằng trình duyệt hoặc chạy qua máy chủ web tĩnh; README cũng hướng dẫn chạy bằng Docker.
- Phiên bản phát hành tương ứng: v1.0. Chi tiết xem [RELEASENOTE.md](RELEASENOTE.md).

## 2026-11-05 — Bổ sung báo cáo kiểm thử trước bàn giao

- Tạo [test_report.md](test_report.md) ghi nhận rà soát tĩnh theo sáu nhóm tiêu chí chất lượng.
- Phân biệt các điểm xác nhận được từ mã nguồn với những kiểm thử runtime chưa thực hiện; liệt kê vấn đề tồn đọng và điều kiện đề xuất để nghiệm thu.

## 2026-11-05 — Bổ sung minh chứng kiểm thử responsive

- Chụp ảnh toàn trang ở viewport mobile (390 × 844), tablet (768 × 1024) và desktop (1440 × 1000), lưu trong [screenshots/](screenshots/).
- Xác nhận lưới dự án hiển thị lần lượt một, hai và ba cột; cả 5 ảnh tải thành công ở mỗi viewport.
- Cập nhật [test_report.md](test_report.md) với trạng thái kiểm thử và liên kết minh chứng; các kiểm thử đa trình duyệt, Docker và hiệu năng vẫn còn cần thực hiện.

## Quy ước cập nhật

Sau mỗi thay đổi lớn, thêm một mục mới ở đầu phần nhật ký, theo mẫu:

### YYYY-MM-DD — Mô tả ngắn

- **Thay đổi:** Nội dung đã thay đổi.
- **Lý do:** Mục tiêu hoặc vấn đề cần giải quyết.
- **Kiểm tra:** Cách xác nhận thay đổi hoạt động.