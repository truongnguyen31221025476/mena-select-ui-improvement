# Bài tập cá nhân Buổi 2 – Phát triển ứng dụng TMĐT

## 1. Giới thiệu

Bài tập tiếp tục phát triển trang chi tiết sản phẩm Mena Select từ Buổi 1, thực hành HTML5 và CSS3 trong khu vực “Sản phẩm liên quan”. Nội dung, tên, giá và tài nguyên sản phẩm được kế thừa từ bài trước.

## 2. Website tham khảo và phạm vi cải tiến

- Website tham khảo: [Mena Select](https://menaselect.com/).
- Phạm vi: `section#san-pham-lien-quan`, gồm bốn thẻ sản phẩm.
- Mục tiêu: tổ chức danh sách rõ hơn, điều chỉnh cách trình bày thẻ, thực hành Flexbox và Grid, làm rõ phản hồi hover và focus bằng bàn phím.

## 3. Kỹ thuật đã thực hành

| Kỹ thuật | Áp dụng thực tế |
|---|---|
| HTML5 | `section` và `h2` đặt tên khu vực, `ul/li` biểu diễn danh sách, mỗi `article` chứa một sản phẩm, `h3` là tên sản phẩm, `img` có `alt`, `a` có `href`. |
| CSS selector | Element selector như `img`, class selector `.product-card`, descendant selector `.product-card h3`. |
| Box Model | Thân thẻ dùng `padding: 16px 16px 18px`, liên kết chi tiết có `margin-top: 16px`, thẻ có viền và bo góc. Quy tắc toàn cục dùng `box-sizing: border-box`. |
| Flexbox | `.product-card__action` dùng `display: flex`, `justify-content: space-between`, `align-items: center`, `gap: 8px` để căn chữ và icon. |
| CSS Grid | `.product-grid` dùng Grid, `gap: 24px`, hiển thị một cột dưới 600px, hai cột từ 600px đến dưới 1040px và bốn cột từ 1040px. |
| Hình ảnh | Giữ `object-fit: contain` và khung ảnh hiện có để thấy trọn bao bì. `cover` được tìm hiểu nhưng không dùng cho ảnh thẻ ở bản cuối. |
| Hover và focus-visible | Chuyển màu nền và viền trong `160ms`, giữ vòng focus xanh toàn cục và dùng `outline-offset: -4px` cho liên kết ảnh. |

`div` chứa `article` trước đây vẫn hợp lệ. Việc dùng `ul/li` là cải thiện ngữ nghĩa, không được trình bày như sửa một lỗi cú pháp HTML.

## 4. Hướng dẫn chạy

1. Tải hoặc clone repository, giữ nguyên các thư mục tài nguyên.
2. Mở thư mục dự án và mở `index.html` bằng Chrome. Có thể dùng Live Server trong VS Code.
3. Trong `head`, trang dùng duy nhất `<link rel="stylesheet" href="css/style.css">`.
4. Khi sửa CSS, lưu tệp rồi tải lại bằng `Ctrl+Shift+R`.

| Đường dẫn | Nội dung |
|---|---|
| `index.html` | Trang HTML kế thừa từ Buổi 1 và cấu trúc danh sách đã chỉnh. |
| `css/style.css` | Tệp CSS đầy đủ đang sử dụng. Tệp `styles.css` cũ ở gốc đã được xóa. |
| `assets/` | Ảnh, logo và font đã có. Đường dẫn font từ CSS bắt đầu bằng `../assets/fonts/`. |
| `screenshots/` | Ảnh trước, sau và các minh chứng kiểm tra. |
| `AI_USAGE.md` | Nhật ký chứa đầy đủ prompt, phản hồi và phần kiểm tra, điều chỉnh. |
| `TESTING.md` | Kết quả kiểm thử và hạn chế còn lại. |
| `bao_cao/BaoCao_Buoi2_HTML5_CSS3.docx` | Báo cáo theo từng bước và các câu hỏi kiến thức. |

## 5. Những thay đổi đã thực hiện

| Hạng mục | Trước | Sau |
|---|---|---|
| Danh sách sản phẩm | `div.product-grid` chứa các `article`. | `ul.product-grid > li > article`, giữ chiều cao thẻ bằng `height: 100%`. |
| Tệp CSS | Có tệp `styles.css` ở gốc trong cấu trúc cũ. | Dùng một tệp đầy đủ `css/style.css`, liên kết đúng từ HTML, điều chỉnh đường dẫn font. |
| Thân thẻ | Padding `14px 16px 16px`. | Padding `16px 16px 18px`. |
| Tên và giá | Cỡ tên `14px`, giá `20px`. | Cỡ tên `15px`, giá `22px`. |
| Khoảng cách lưới | `16px`. | `24px`, giữ các breakpoint đã có. |
| Liên kết chi tiết | Đã có Flexbox và hover nền. | Thêm chuyển màu nền và viền `160ms`, áp dụng màu trạng thái cho cả hover và focus-visible. |
| Focus ảnh | Vòng focus chưa nhìn thấy rõ ở lượt kiểm tra trước sửa. | Thêm `outline-offset: -4px`, ảnh sau cho thấy vòng xanh quanh ảnh đầu tiên. |

Minh chứng chính:

- [Giao diện trước](screenshots/buoi2_buoc1_before_desktop.png).
- [Giao diện sau ở desktop](screenshots/buoi2_buoc8_desktop_1366.png).
- [Cấu trúc HTML](screenshots/buoi2_buoc2_html_structure.png).
- [Flexbox](screenshots/buoi2_buoc5_flexbox.png) và [thử Grid hai cột](screenshots/buoi2_buoc6_grid_2_cot.png).
- [Hover](screenshots/buoi2_buoc7_hover.png), [focus nút](screenshots/buoi2_buoc7_focus.png), [focus ảnh sau sửa](screenshots/buoi2_buoc8_photo_focus_after.png).
- [Tablet](screenshots/buoi2_buoc8_tablet_768.png) và [mobile](screenshots/buoi2_buoc8_mobile_390.png).

Hạn chế còn lại: nút “Xem chi tiết” của thẻ mực làm sạch cuối cùng chưa mở đúng trang theo kết quả kiểm tra. Liên kết được giữ nguyên trong đợt này. Mỗi thẻ vẫn có ba liên kết cùng đích. Tên class `product-card__category` vẫn được giữ theo mã cũ.

## 6. Sử dụng AI và kiểm tra kết quả

ChatGPT hỗ trợ rà soát phản hồi AI, chuẩn bị mã đầy đủ, tính tương phản và tổng hợp tài liệu. Các phản hồi Claude đã được cung cấp trong quá trình thực hành cũng được giữ trong nhật ký. Không ghi phiên bản mô hình khi chưa có thông tin xác nhận.

Kết quả được đối chiếu với mã nguồn, ảnh DevTools, thao tác chuột và bàn phím, cùng các ảnh Responsive. Nội dung prompt và phản hồi được giữ trực tiếp trong [AI_USAGE.md](AI_USAGE.md).

| CSS viewport đã chụp | Kết quả trong phạm vi ảnh |
|---|---|
| `1366 × 1328` | Bốn cột, thấy đầy đủ bốn thẻ. |
| `768 × 746` | Hai cột, thấy đầy đủ hai thẻ đầu và phần đầu hàng tiếp theo. |
| `390 × 544` | Một cột, thấy đầy đủ thẻ đầu và đầu thẻ tiếp theo. |

Các điều chỉnh sau đối chiếu gồm giữ `contain` thay cho gợi ý `cover`, giữ bố cục responsive thay cho hai cột cố định, sửa nhận định rằng `inline-flex` luôn làm nút co vừa nội dung, và giữ offset ảnh `-4px` sau khi quan sát ảnh kiểm tra. Hai cặp màu chữ và nền của liên kết chi tiết được tính lại, cho tỷ lệ xấp xỉ `9,25:1` ở trạng thái thường và `8,43:1` ở hover/focus-visible.

Chi tiết kết quả, gồm liên kết chưa đạt, có trong [TESTING.md](TESTING.md). Chưa thực hiện kiểm thử bằng trình đọc màn hình, Nu HTML Checker, axe hoặc Lighthouse trong đợt này.

## 7. Đường dẫn dự án

- Repository: https://github.com/truongnguyen31221025476/mena-select-ui-improvement
- Website đã triển khai: chưa xác minh đường dẫn truy cập của bản cập nhật này. Có thể chạy cục bộ bằng `index.html`.

### Câu hỏi kiến thức

1. `section`, `header`, `h2`, `ul/li`, `article`, `h3`, `img` và `a` tổ chức khu vực, danh sách, sản phẩm, ảnh và liên kết theo nội dung thực tế.
2. Margin ở ngoài đường viền, padding ở trong. Liên kết chi tiết có `margin-top: 16px`, thân thẻ có `padding: 16px 16px 18px`.
3. Flexbox căn chữ và icon trong liên kết chi tiết. `justify-content` căn theo trục chính, `align-items` căn theo trục phụ.
4. Flexbox chủ yếu tổ chức theo một trục. Grid điều khiển hàng và cột, phù hợp danh sách nhiều thẻ.
5. Bỏ `display: grid` mà không có bố cục khác thay thế sẽ làm các `li` trở về luồng danh sách thông thường, không chia cột như hiện tại.
6. `alt` cung cấp nội dung thay thế cho ảnh sản phẩm khi không xem được ảnh hoặc dùng công nghệ hỗ trợ.
7. Gợi ý `cover` đã được đối chiếu với yêu cầu nhìn trọn bao bì. Bản cuối giữ `contain` và khung ảnh hiện có.
