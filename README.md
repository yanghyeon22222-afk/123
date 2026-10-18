# ToMaTe — Website trải nghiệm sách ảo

Bản frontend React/Vite theo tài liệu ToMaTe và sơ đồ quy trình được cung cấp. Giao diện responsive, dữ liệu mẫu chạy trong bộ nhớ của phiên trình duyệt.

## Chạy trên máy

Yêu cầu Node.js 18+.

```bash
npm install
npm run dev
```

Mở địa chỉ local mà Vite hiển thị (thường là `http://localhost:5173`). Để tạo bản production:

```bash
npm run build
npm run preview
```

## Ba cổng truy cập độc lập

- **Phụ huynh & bé:** đăng ký/đăng nhập riêng; duyệt sách, preview, mở khóa nội dung/gói dịch vụ mô phỏng, hồ sơ trẻ (tối đa 3), giới hạn thời gian, lịch sử và tiến trình.
- **Nhà cung cấp:** đăng ký đối tác riêng (trạng thái chờ Admin xác minh); gửi nội dung/kịch bản, theo dõi trạng thái, nghiệm thu bản dựng, xem lượt tương tác và doanh thu.
- **Admin:** đăng nhập cổng quản trị riêng; cấu hình danh mục/gói, xác minh/từ chối hồ sơ, kiểm duyệt/trả sửa/xuất bản sách, quản lý người dùng và đối soát giao dịch.

## Luồng nghiệp vụ được mô phỏng

1. Admin khởi tạo danh mục, nhóm tuổi và gói dịch vụ.
2. Nhà cung cấp nộp hồ sơ; Admin xác minh và cấp quyền (demo trạng thái).
3. Nhà cung cấp gửi bản thảo, tài liệu và kịch bản.
4. Admin/Studio tiếp nhận, dựng 3D 360° và kiểm duyệt; nhà cung cấp xem trước/nghiệm thu hoặc yêu cầu sửa.
5. Admin duyệt và xuất bản; phụ huynh tìm sách, chọn gói/mua lẻ hoặc đi theo nhánh miễn phí.
6. Phụ huynh cài đặt giới hạn thời gian; trẻ trải nghiệm không gian sách, hotspot, câu đố và AI Tutor demo.
7. Hệ thống ghi nhận lịch sử demo; phụ huynh xem tiến trình, nhà cung cấp xem tương tác/doanh thu, Admin xem giao dịch/đối soát.

## Lưu ý quan trọng

Đây là **prototype frontend**, chưa phải hệ thống production. Các thao tác xác thực, thanh toán, tải file, AI Tutor, dữ liệu lịch sử và phân quyền hiện được mô phỏng phía trình duyệt. Không nhập dữ liệu cá nhân thật. Trước khi triển khai thật cần backend/API, cơ sở dữ liệu, mã hóa mật khẩu, phân quyền server-side, lưu trữ tệp an toàn, cổng thanh toán sandbox/production, chính sách bảo vệ trẻ em và kiểm thử bảo mật. Dữ liệu sẽ trở về mẫu khi tải lại trang.
