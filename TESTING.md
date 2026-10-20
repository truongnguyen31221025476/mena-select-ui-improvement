# Kiểm tra giao diện

Ngày kiểm tra: 20/10/2026. Trình duyệt Chrome trong phiên hỗ trợ AI.
Khung điện thoại và tablet được dựng bằng iframe có kích thước CSS cố định; không phải thử nghiệm thiết bị thật.

| Khung hiển thị | Rộng nội dung | Rộng có thể cuộn | Kết quả |
|---|---:|---:|---|
| Máy tính 1363 × 936 | 1348 px | 1348 px | Không tràn ngang |
| Tablet 768 × 900 | 753 px | 753 px | Không tràn ngang |
| Điện thoại 390 × 844 | 375 px | 375 px | Không tràn ngang |
| Điện thoại 320 × 568 | 305 px | 305 px | Không tràn ngang |

Thanh cuộn dọc chiếm một phần chiều rộng khung trong trình duyệt kiểm tra.

| Thao tác | Kết quả quan sát |
|---|---|
| Chọn thumbnail 1, 2, 3 | Hiển thị đúng ảnh và chú thích tương ứng |
| Bấm thumbnail 3 bằng con trỏ | Vị trí cuộn giữ nguyên 279 px |
| Bấm ảnh lớn và đóng bằng Esc | Khung phóng to mở/đóng; vị trí cuộn giữ nguyên 279 px |
| Mở Chia sẻ | Hiện liên kết sản phẩm và lựa chọn Facebook/Email; không gửi nội dung |
| Nhập số lượng 2 | Giá trị ô nhập là 2; không kiểm tra tồn kho |
| Bấm Thêm vào giỏ | Hiện thông báo sản phẩm chưa được thêm; không tạo đơn |
| Quay lại mua hàng | Khối giá xuất hiện gần đầu vùng nhìn thấy |
| Bốn sản phẩm liên quan | Đủ ảnh đã tải, tên, giá và liên kết thao tác |

Lỗi phát hiện khi kiểm tra: khung 390 px có chiều rộng nội dung cuộn 878 px.
Nguyên nhân được đối chiếu trong DOM: nhãn liên kết ẩn trong thanh điều hướng thoát khỏi vùng cuộn.
Sửa `.navigation-links` bằng `position: relative`; kiểm tra lại còn 375/375 px.

Chưa thử thiết bị thật, gửi chia sẻ ra ngoài, đăng nhập, thanh toán hoặc nghiệp vụ giỏ hàng thật.
