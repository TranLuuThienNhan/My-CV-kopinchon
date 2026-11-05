# BÁO CÁO KIỂM THỬ TRƯỚC KHI BÀN GIAO

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | My-CV-kopinchon — website CV/portfolio cá nhân |
| Phiên bản đối chiếu | v1.0 (theo `docs/RELEASENOTE.md`) |
| Ngày kiểm thử/rà soát | 05/11/2026 |
| Người thực hiện | Rà soát QA/QC mã nguồn và tài liệu trong repository; tên cá nhân chưa được cung cấp |
| Người đánh giá/phê duyệt | Chưa cung cấp — bổ sung trước khi ký bàn giao |
| Phạm vi | `index.html`, `assets/css/styles.css`, `README.md`, `docs/RELEASENOTE.md`, cấu trúc tài liệu và minh chứng hiện có |
| Phương pháp | Rà soát mã nguồn/tài liệu và kiểm thử hiển thị trực tiếp trên trình duyệt tích hợp qua máy chủ HTTP cục bộ |
| Môi trường kiểm thử | Trình duyệt tích hợp; viewport 390 × 844 (mobile), 768 × 1024 (tablet), 1440 × 1000 (desktop); 5/5 ảnh tải thành công ở mỗi viewport |

> **Giới hạn của báo cáo:** Đã kiểm tra hiển thị responsive trên trình duyệt ở ba viewport và lưu ảnh minh chứng bên dưới. Chưa thực hiện kiểm thử trên nhiều trình duyệt/thiết bị vật lý, kiểm thử triển khai Docker, đo hiệu năng hoặc kiểm thử bảo mật chuyên sâu. Các mục này cần được kiểm tra bổ sung trước khi nghiệm thu.

### Quy ước trạng thái

- **Đạt:** Có thể xác nhận từ mã nguồn hoặc tài liệu đã kiểm tra.
- **Chưa đạt:** Có lỗi hoặc yêu cầu chưa được đáp ứng rõ ràng.
- **Cần cải thiện:** Chưa có đủ bằng chứng để kết luận, hoặc còn vấn đề cần xử lý/xác nhận.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---:|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Có các phần giới thiệu, kỹ năng, dự án và liên hệ; một số liên kết dự án và hồ sơ cá nhân vẫn dùng `href="#"`. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Cần cải thiện | Đã xác nhận responsive ở ba viewport và lưu ảnh minh chứng; cần rà soát alt ảnh, nội dung và khả năng tương thích đa trình duyệt/thiết bị. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | README hướng dẫn chạy bằng Python và Docker; chưa có kết quả chạy thử, kiểm tra tài nguyên lỗi hoặc đo hiệu năng. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Website là nội dung tĩnh, không thấy mã JavaScript/backend; vẫn cần rà soát dữ liệu cá nhân, cấu hình image Docker và kiểm tra phát hành. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Cần cải thiện | HTML/CSS tách riêng và có tài liệu cơ bản; còn điểm chưa nhất quán về nội dung, liên kết và danh mục cấu trúc trong README. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Đã có ảnh responsive và kết quả kiểm thử hiển thị; chưa kiểm thử Docker, chưa có bộ test tự động và biên bản triển khai production. |

## 3. Chi tiết kiểm tra theo nhóm tiêu chí

### 3.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| F-01 | Có nội dung giới thiệu, kỹ năng, dự án và liên hệ | Đạt | `index.html` có các section `#about`, `#skills`, `#projects`, `#contact`. |
| F-02 | Menu điều hướng trỏ đến đúng section | Đạt | Các liên kết điều hướng trong `index.html` dùng các fragment tương ứng với ID section. Cần xác nhận thao tác thực tế trên trình duyệt. |
| F-03 | Nút kêu gọi hành động trong phần giới thiệu | Đạt | “Xem dự án” trỏ đến `#projects`, “Liên hệ tôi” trỏ đến `#contact`. Chưa kiểm thử thao tác runtime. |
| F-04 | Liên kết xem chi tiết của các thẻ dự án | Chưa đạt | Cả bốn liên kết “Xem chi tiết” đang dùng `href="#"`, chưa dẫn đến trang/nội dung chi tiết. Cần bổ sung URL hợp lệ hoặc trình bày rõ đây là thẻ chưa có trang đích. |
| F-05 | Liên kết GitHub và LinkedIn | Chưa đạt | Hai liên kết trong phần liên hệ đang dùng `href="#"`; README cũng ghi nhận URL hồ sơ chưa được cấu hình. |
| F-06 | Tính nhất quán của thông tin cá nhân | Cần cải thiện | Phần thương hiệu đầu trang hiển thị “Trần Lưu Thiện Nhân14”, trong khi tiêu đề và phần giới thiệu không có “14”. Cần xác nhận và sửa nội dung dự kiến. |
| F-07 | Liên kết email | Cần cải thiện | Có `mailto:zenotnhan@gmail.com`; chưa kiểm tra ứng dụng email hoặc xác nhận địa chỉ thuộc chủ sản phẩm. |

### 3.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| UI-01 | Bố cục responsive theo kích thước màn hình | Đạt | Đã xác nhận trên trình duyệt: 390px hiển thị lưới dự án một cột, 768px hai cột, 1440px ba cột. Ảnh minh chứng: [mobile](screenshots/responsive-mobile.png), [tablet](screenshots/responsive-tablet.png), [desktop](screenshots/responsive-desktop.png). |
| UI-02 | Hình ảnh và khả năng co giãn trong layout | Đạt | Có quy tắc `img { max-width: 100%; height: auto; }`; các ảnh nội dung có thuộc tính `alt`, `width`, `height`. |
| UI-03 | Mô tả thay thế ảnh phù hợp | Cần cải thiện | Một số `alt` mô tả chung như “Ảnh minh họa dự án Landing Page” hoặc “Todo App”, không khớp rõ với nội dung thẻ dự án. Cần cập nhật mô tả chính xác. |
| UI-04 | Điều hướng bàn phím và trạng thái focus | Đạt | CSS có `:focus-visible` cho liên kết menu và outline focus toàn cục. Cần kiểm tra thao tác bằng bàn phím trên trình duyệt và độ tương phản thực tế. |
| UI-05 | Tôn trọng tùy chọn giảm chuyển động | Đạt | CSS có `prefers-reduced-motion: reduce` để tắt transition/animation và cuộn mượt. Chưa kiểm thử với cài đặt hệ điều hành/trình duyệt. |
| UI-06 | Kiểm tra tương thích đa trình duyệt và thiết bị vật lý | Cần cải thiện | Đã chụp giao diện ở ba kích thước viewport trên trình duyệt tích hợp, nhưng chưa kiểm tra độc lập trên Chrome/Edge/Firefox/Safari hoặc điện thoại/tablet vật lý. |
| UI-07 | Rà soát nội dung hiển thị và tính chuyên nghiệp | Cần cải thiện | Cần chủ sản phẩm xác nhận nội dung giới thiệu, vai trò, văn phong, thông tin trường học và nội dung thẻ dự án trước khi công khai. |

### 3.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| OP-01 | Có thể phục vụ website như trang tĩnh theo cấu trúc tài liệu | Đạt | README hướng dẫn mở `index.html`, chạy Python HTTP server hoặc phục vụ bằng Apache trong Docker. Các cách chạy chưa được thực thi trong lần rà soát này. |
| OP-02 | Tải CSS và ảnh theo đường dẫn trong HTML | Cần cải thiện | Đường dẫn CSS và ảnh có trong `index.html`; chưa chạy kiểm tra HTTP/network để xác nhận không có tài nguyên trả lỗi hoặc lỗi tên tệp trên môi trường triển khai. |
| OP-03 | Xử lý trang/tài nguyên không tồn tại | Cần cải thiện | Chưa xác định hoặc kiểm thử trang 404 và hành vi khi thiếu ảnh/CSS. README hiện không mô tả trang lỗi tùy chỉnh. |
| OP-04 | Hiệu năng tải cơ bản | Cần cải thiện | Chưa đo thời gian tải, kích thước trang, hiệu năng trên mạng chậm hoặc chỉ số bằng Lighthouse/WebPageTest. Các ảnh dự án cần được đánh giá dung lượng và phương án tối ưu trước khi phát hành công khai. |
| OP-05 | Hành vi lỗi của máy chủ cục bộ/container | Cần cải thiện | Chưa kiểm tra cổng đã được sử dụng, Docker chưa khởi động, tải image thất bại hoặc dừng dịch vụ. Hướng dẫn README có nêu lệnh dừng bằng `Ctrl+C`. |

### 3.4. Bảo mật, quản lý cấu hình và dữ liệu

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| SEC-01 | Bề mặt xử lý dữ liệu phía ứng dụng | Đạt | README mô tả website không dùng JavaScript, backend, cơ sở dữ liệu hoặc biểu mẫu; trong `index.html` được rà soát không thấy form/script. Đây là quan sát mã nguồn, không thay thế kiểm tra triển khai. |
| SEC-02 | Bí mật, token và cấu hình nhạy cảm | Cần cải thiện | Không thấy cấu hình ứng dụng riêng trong phạm vi rà soát; chưa chạy công cụ quét secret trên toàn bộ repository hoặc kiểm tra lịch sử Git. |
| SEC-03 | Dữ liệu cá nhân trước khi công khai | Cần cải thiện | Website hiển thị tên, email, ảnh và thông tin cá nhân. Chủ sản phẩm cần xác nhận quyền sử dụng và đồng ý công khai các dữ liệu/ảnh này. |
| SEC-04 | Cấu hình image khi chạy Docker | Cần cải thiện | README dùng `httpd:2.4`; tag không cố định tới digest nên phiên bản image có thể thay đổi theo thời gian. Cần đánh giá chính sách cập nhật và cố định phiên bản nếu quy trình phát hành yêu cầu tái lập. |
| SEC-05 | HTTPS và cấu hình môi trường triển khai | Cần cải thiện | README chỉ hướng dẫn chạy local/Docker; chưa có cấu hình hoặc bằng chứng triển khai HTTPS, header bảo mật hay cấu hình máy chủ production. |

### 3.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| Q-01 | Tách biệt cấu trúc nội dung và giao diện | Đạt | HTML nằm trong `index.html`, CSS tách tại `assets/css/styles.css`; không thấy JavaScript hoặc framework cần build theo tài liệu README. |
| Q-02 | Cấu trúc HTML và ngữ nghĩa cơ bản | Đạt | Có `lang="vi"`, metadata viewport, `header`, `nav`, `main`, `section`, `article`, `footer` và tiêu đề trang. Chưa chạy validator HTML. |
| Q-03 | Đường dẫn tài nguyên và nội dung thẻ dự án | Cần cải thiện | Cần rà soát lại sự tương ứng giữa ảnh/alt/mô tả dự án; các liên kết chi tiết còn là `#`. |
| Q-04 | Tính nhất quán của README với repository | Cần cải thiện | Cấu trúc repository trong README chưa liệt kê thư mục `docs/` và các tài liệu bàn giao như `RELEASENOTE.md`, `test_report.md`. |
| Q-05 | Hướng dẫn cài đặt và chạy | Đạt | README có hướng dẫn mở trực tiếp, dùng Python trên Windows/macOS/Linux và dùng Docker. Các lệnh cần được chạy thử trên môi trường bàn giao. |
| Q-06 | Tài liệu phát hành và kiểm thử | Cần cải thiện | Có ghi chú phát hành v1.0 và báo cáo này; chưa có kết quả kiểm thử runtime để làm căn cứ nghiệm thu. |

### 3.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| DEL-01 | Hướng dẫn chạy cục bộ | Đạt | README chỉ rõ lệnh Python HTTP server và địa chỉ truy cập local; chưa thực hiện chạy thử. |
| DEL-02 | Hướng dẫn triển khai qua Docker | Cần cải thiện | Có lệnh chạy Apache và ánh xạ thư mục dự án, nhưng chưa xác nhận container khởi động, phục vụ đúng trang và truy cập được trên trình duyệt. |
| DEL-03 | Kịch bản kiểm thử lặp lại được | Cần cải thiện | Chưa có bộ test tự động hoặc checklist kết quả runtime kèm người chạy, môi trường và thời điểm. |
| DEL-04 | Ảnh chụp/minh chứng trực quan | Đạt | Đã lưu ảnh chụp toàn trang ở [mobile 390 × 844](screenshots/responsive-mobile.png), [tablet 768 × 1024](screenshots/responsive-tablet.png), và [desktop 1440 × 1000](screenshots/responsive-desktop.png). |
| DEL-05 | Truy vết lỗi và kết quả kiểm thử | Cần cải thiện | Báo cáo ghi lại các phát hiện tĩnh, nhưng chưa có mã lỗi/ticket, mức độ ưu tiên được chủ sản phẩm xác nhận, kết quả retest hoặc phê duyệt bàn giao. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Website có nền tảng phù hợp cho một portfolio tĩnh: các khu vực nội dung chính hiện diện, CSS được tách riêng, có breakpoint responsive, và README cung cấp nhiều cách chạy thử. Tuy nhiên, kết quả hiện tại mới là **rà soát tĩnh**; chưa có bằng chứng xác nhận website chạy đúng trên trình duyệt hoặc môi trường bàn giao.

**Đánh giá sẵn sàng bàn giao: Chưa nên xác nhận nghiệm thu cuối cùng** cho đến khi xử lý các liên kết chưa có đích, xác nhận nội dung cá nhân và hoàn tất kiểm thử runtime kèm minh chứng. Có thể bàn giao bản xem trước nội bộ nếu người nhận được thông báo rõ các hạn chế này.

### Vấn đề cần xử lý trước khi nghiệm thu

1. Thay các liên kết `href="#"` của bốn thẻ dự án và hồ sơ GitHub/LinkedIn bằng đích đến hợp lệ, hoặc bỏ/đổi nhãn các liên kết chưa có chức năng.
2. Xác nhận nội dung thương hiệu “Trần Lưu Thiện Nhân14”, nội dung giới thiệu và toàn bộ thông tin cá nhân; sửa nếu không đúng chủ đích.
3. Rà soát `alt` ảnh để mô tả đúng ảnh và nội dung dự án.
4. Chạy website bằng ít nhất một phương thức trong README; xác nhận CSS, tất cả ảnh, menu, CTA, email và các liên kết hoạt động, đồng thời ghi nhận lỗi nếu có.
5. Kiểm tra giao diện ở màn hình điện thoại, tablet và desktop; kiểm tra điều hướng bàn phím và trạng thái giảm chuyển động.
6. Bổ sung ảnh minh chứng vào `docs/screenshots/`, ghi môi trường/trình duyệt/kích thước màn hình và kết quả pass/fail.
7. Cập nhật README để liệt kê thư mục tài liệu bàn giao; xác nhận quyền công khai ảnh/thông tin liên hệ và rà soát cấu hình triển khai Docker/HTTPS theo môi trường thực tế.

### Điều kiện đề xuất để đóng kiểm thử

- Tất cả liên kết có đích đến đúng hoặc được ghi rõ là chưa hỗ trợ.
- Các luồng chức năng chính không có lỗi chặn; các lỗi còn lại có người phụ trách và kế hoạch xử lý được chấp thuận.
- Kiểm thử trình duyệt/viewport mục tiêu hoàn tất và có minh chứng lưu trong repository.
- Chủ sản phẩm xác nhận nội dung, dữ liệu cá nhân và phê duyệt kết quả bàn giao.

### Minh chứng giao diện responsive

| Thiết bị mô phỏng | Viewport | Kết quả kiểm tra | Ảnh chụp |
|---|---:|---|---|
| Mobile | 390 × 844 | Lưới dự án 1 cột; 5/5 ảnh tải thành công | [responsive-mobile.png](screenshots/responsive-mobile.png) |
| Tablet | 768 × 1024 | Lưới dự án 2 cột; 5/5 ảnh tải thành công | [responsive-tablet.png](screenshots/responsive-tablet.png) |
| Desktop | 1440 × 1000 | Lưới dự án 3 cột; 5/5 ảnh tải thành công | [responsive-desktop.png](screenshots/responsive-desktop.png) |

Ảnh được chụp toàn trang từ website chạy trên máy chủ HTTP cục bộ bằng trình duyệt tích hợp; không phải ảnh dựng hoặc mockup.

| Xác nhận | Người xác nhận | Ngày | Ý kiến |
|---|---|---|---|
| QA/QC | ____________________ | ____/____/________ | ____________________ |
| Chủ sản phẩm/Đại diện bàn giao | ____________________ | ____/____/________ | ____________________ |