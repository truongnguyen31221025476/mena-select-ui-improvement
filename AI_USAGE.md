# AI Usage Log

## 1. Công cụ AI
Gemini và ChatGPT; chưa ghi nhận phiên bản cụ thể.

## 2. Mục đích sử dụng
Phân tích giao diện, đề xuất bố cục, giải thích HTML/CSS và hỗ trợ sửa mã theo phản hồi của sinh viên.

## 3. Prompt đã sử dụng

### Phân tích website
```text
Bạn là chuyên gia phân tích nghiệp vụ và thiết kế trải nghiệm người dùng cho website thương mại điện tử.
Tôi đang khảo sát website Mena Select: https://menaselect.com/.
Hãy giúp tôi lập bảng phân tích các khu vực:
1. Trang chủ.
2. Danh mục sản phẩm.
3. Chi tiết sản phẩm.
4. Tìm kiếm.
5. Giỏ hàng.
Với mỗi khu vực, hãy nêu:
- Mục đích của chức năng.
- Thành phần giao diện cần có.
- Điểm thuận tiện đối với khách hàng.
- Một vấn đề có thể phát sinh.
- Một đề xuất cải tiến.
Không khẳng định những tính năng chưa được kiểm chứng.
Phân biệt rõ nhận xét dựa trên quan sát và đề xuất của AI.
```

### Đề xuất giao diện
```text
Tôi đang thực hiện bài tập phát triển giao diện website thương mại điện tử bằng HTML5 và CSS3.

Tôi muốn cải tiến khu vực: trang chi tiết sản phẩm của website Mena Select (https://menaselect.com/), tập trung tối ưu khung ảnh và tính thẩm mỹ, xử lý bố cục mất cân đối khi mô tả chi tiết kéo dài ở một cột; sắp xếp rõ mô tả ngắn, thông tin mua hàng, khuyến mãi/quà tặng, chính sách và sản phẩm liên quan.

Đối tượng sử dụng: khách hàng mua sắm trực tuyến tại Việt Nam.

Hãy đề xuất:
1. Bố cục giao diện.
2. Các thành phần HTML cần sử dụng.
3. Cách tổ chức CSS.
4. Cách hiển thị trên máy tính và điện thoại.
5. Những điểm cần kiểm tra về khả năng sử dụng.

Trước tiên, hãy giải thích phương án thiết kế.
Chưa tạo toàn bộ mã nguồn cho đến khi tôi yêu cầu.
```

### Tạo mã nguồn
```text
Tôi chọn phương án A: phía trên là hai cột ảnh và thông tin mua hàng; phía dưới là mô tả chi tiết hiển thị sẵn trên toàn chiều rộng, chia thành các mục dễ đọc.

Dùng “Cá phèn Hải Nam fillet còn da size 20–40 gói 500g” làm sản phẩm chính, kèm bốn sản phẩm liên quan. Giữ khu vực mô tả ngắn, khuyến mãi/quà tặng và liên kết chính sách; banner quảng bá được bố trí riêng.

Dựa trên phương án đã thống nhất, hãy tạo một trang giao diện thương mại điện tử bằng HTML5 và CSS3.

Yêu cầu:
- Giao diện có tiêu đề và khu vực sản phẩm.
- Có tối thiểu 4 sản phẩm mẫu.
- Mỗi sản phẩm có hình ảnh, tên, giá và nút thao tác.
- Bố cục phù hợp với màn hình máy tính và điện thoại.
- Mã HTML có cấu trúc rõ ràng.
- CSS được tách thành file riêng.
- Không sử dụng backend hoặc cơ sở dữ liệu.
- Không đưa thư viện hoặc thành phần không cần thiết vào dự án.

Giải thích cách chạy trang web và những phần tôi cần kiểm tra.

```

### Các yêu cầu điều chỉnh
Sinh viên yêu cầu giữ header/footer/danh mục, làm rõ VAT và phí vận chuyển, thêm ảnh, sửa hành vi xem ảnh, bỏ nhãn phụ và bổ sung Chia sẻ.


## 4. Kết quả AI đề xuất
Bản lưu bước 3: Gallery có ba ảnh và thumbnail; thao tác xem ảnh ở bản này còn mở tệp ảnh nguồn.

## 5. Kiểm tra và điều chỉnh
Bổ sung ảnh cá phèn xiên rau củ và cá phèn nướng, dải thumbnail và chú thích từng ảnh; chuẩn hóa nhãn danh mục.
Đây là bản đã lưu trong quá trình chỉnh sửa. Kết quả kiểm tra của bản hoàn thiện được bổ sung ở lượt cuối; không dùng kết quả đó để khẳng định mọi bản cũ đã đạt.

## 6. Phần tôi hiểu và có thể giải thích
Cấu trúc HTML, liên kết CSS, Grid và Flexbox, media query, margin/padding/gap, radio/label/:checked và popover. Chi tiết áp dụng phụ thuộc chức năng đã có trong từng bản lưu.
