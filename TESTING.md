# Kiểm thử khu vực Sản phẩm liên quan Buổi 2

Phạm vi: `#san-pham-lien-quan`. Kiểm tra bằng Chrome trên máy tính, dùng Device Toolbar để thay CSS viewport. Các ảnh Responsive là mô phỏng viewport, không phải thử nghiệm thiết bị thật.

## 1. Bảng kiểm thử

| Nội dung kiểm tra | Kết quả | Ghi chú |
|---|---|---|
| Trang HTML mở được | Đạt | Có ảnh thực tế của khu vực được chọn. |
| CSS được áp dụng | Đạt | DevTools hiển thị nguồn style.css, giao diện được định dạng sau khi thay tệp. |
| Hình ảnh hiển thị đúng | Đạt trong phạm vi quan sát | Ảnh bao bì giữ tỷ lệ trong các ảnh đã chụp. |
| Liên kết hoạt động | Chưa đạt | Liên kết chi tiết của thẻ mực làm sạch cuối cùng chưa mở đúng trang. Giữ nguyên trong đợt này. |
| Bố cục không bị tràn nghiêm trọng | Đạt trong phạm vi đã chụp | Bố cục tại các chiều rộng 1366, 768 và 390 CSS px lần lượt bốn, hai và một cột. |
| Hover/focus hoạt động | Đạt với trạng thái đã kiểm tra | Có ảnh hover và focus của nút chi tiết, cùng focus ảnh sau điều chỉnh. |
| Đã sửa một vấn đề nhỏ và kiểm tra lại | Đạt | Áp dụng outline-offset -4px theo gợi ý AI, kiểm tra lại và xác nhận giữ giá trị. |

## 2. Vấn đề và cách xử lý

| Vấn đề | Cơ sở xác định hoặc kiểm tra | Cách xử lý | Kết quả |
|---|---|---|---|
| Vòng focus ảnh chưa nhìn thấy rõ | CSS tạo outline phía ngoài, thẻ có overflow: hidden. Ảnh trước chưa xác nhận riêng phần tử active, nên nguyên nhân cắt vòng ban đầu là giả thuyết cần kiểm tra. | Thêm .product-card__photo:focus-visible với outline-offset: -4px. | Ảnh sau có vòng xanh đủ bốn cạnh. Không khẳng định đã thực hiện mọi bước Console hoặc tắt overflow nếu chưa có xác nhận. |
| Trang từng mất định dạng khi thay CSS | Đã có ảnh mất định dạng và xác nhận khôi phục. Nguyên nhân chính xác của lần đó chưa được xác định. | Khôi phục, sau đó dùng tệp CSS đầy đủ tại css/style.css và một liên kết stylesheet trong HTML. | Người dùng xác nhận giao diện bình thường và đã xóa styles.css ở gốc. |
| Liên kết mực làm sạch chưa mở đúng trang | Người dùng đã bấm nút và báo kết quả không đúng. | Giữ href hiện tại theo phạm vi chốt. | Chưa đạt. Chưa xác định lỗi HTTP hay chuyển hướng. |

## 3. Responsive

| CSS viewport | Cột nhìn thấy | Minh chứng |
|---|---:|---|
| 1366 × 1328 | 4 | screenshots/buoi2_buoc8_desktop_1366.png |
| 768 × 746 | 2 | screenshots/buoi2_buoc8_tablet_768.png |
| 390 × 544 | 1 | screenshots/buoi2_buoc8_mobile_390.png |

Thông số được đọc từ thanh thiết bị trong ảnh. Không suy ra viewport từ kích thước tệp PNG. Bản tablet/mobile chỉ chứng minh phần nội dung được chụp.

## 4. Kiểm tra từ mã và màu

- Bốn thẻ có tổng cộng 12 liên kết, mỗi thẻ có ba href cùng đích, đều có target=_blank và rel=noopener noreferrer. Đây là kiểm tra tĩnh, không thay thế thao tác nhấp.
- Đã đối chiếu được nội dung trang đích của cá hồi, mực nhồi thịt và nghêu bằng công cụ web. Liên kết cuối chưa đạt theo kiểm tra trên máy người dùng.
- Tương phản chữ #2b452d với nền #edf2e5: 9,254260864662935:1. Với nền #e0eacb: 8,434805246430496:1. Kết luận vượt 4,5:1 dùng giá trị chưa làm tròn. Đây là kiểm tra hai cặp màu, không phải chứng nhận toàn trang đáp ứng WCAG.
- Chưa chạy Nu HTML Checker, axe, Lighthouse hoặc trình đọc màn hình. Chưa đo thời gian transition từ ảnh tĩnh.

## 5. Nguồn đối chiếu

- https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html
- https://www.w3.org/WAI/WCAG22/Understanding/focus-visible.html
- https://www.w3.org/TR/css-ui-4/#outline-offset
- https://www.w3.org/TR/css-grid-1/
- https://www.w3.org/TR/css-images-3/#the-object-fit

## 6. Nội dung kiểm tra đã có từ Buổi 1

Phần dưới giữ nguyên bản TESTING.md đang có trong repository để bảo toàn lịch sử. Các kết quả cũ không được dùng thay cho kiểm tra Buổi 2 ở trên.

<details>
<summary>Xem bản kiểm tra Buổi 1 đã lưu</summary>

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


</details>
