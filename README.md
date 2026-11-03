# Bài tập cá nhân Buổi 2 HTML5 và CSS3

Website tham khảo: https://menaselect.com/

Phạm vi thực hành: khu vực “Sản phẩm liên quan”, có
id="san-pham-lien-quan", tiếp tục từ mã nguồn Buổi 1.

## 1. Rà soát và lựa chọn phạm vi

Khu vực gồm bốn sản phẩm với ảnh, thương hiệu và quy cách,
tên, giá và liên kết xem chi tiết.

| Vấn đề hoặc điểm cần cải thiện | Hướng xử lý |
|---|---|
| Nhóm sản phẩm chưa biểu diễn bằng danh sách HTML | Dùng ul/li, giữ article cho từng sản phẩm |
| Khoảng cách và cỡ chữ cần được tinh chỉnh | Điều chỉnh padding, margin, font-size và border-radius |
| Viền focus của liên kết ảnh từng hiển thị chưa đầy đủ | Đặt outline vào phía trong liên kết ảnh |

Div chứa article vẫn hợp lệ. Việc đổi sang ul/li là cải thiện
ngữ nghĩa, không phải sửa lỗi cú pháp.

## 2. Cấu trúc HTML5

Section gom nội dung cùng chủ đề. H2 đặt tên khu vực.
Ul biểu diễn danh sách sản phẩm, mỗi li chứa một article.
Article gom nội dung của một sản phẩm. H3 biểu thị tên sản phẩm.
Img có alt mô tả ảnh. A có href để điều hướng tới trang chi tiết.

Cấu trúc danh sách đã được đối chiếu bằng ảnh Elements.

### Câu hỏi tự kiểm tra

- Nav nhận diện một khối điều hướng, không cần dùng cho mọi liên kết.
- Article biểu thị nội dung tương đối độc lập. Div là phần tử chứa chung.
- Alt cung cấp văn bản thay thế cho ảnh.
- Ul/li phù hợp với danh sách không có thứ tự bắt buộc. Ol dùng khi thứ tự có ý nghĩa.

## 3. Tạo và liên kết CSS

Tệp sử dụng: css/style.css.

HTML liên kết bằng:
<link rel="stylesheet" href="css/style.css">

Styles.css ở thư mục gốc được giữ lại làm bản tham chiếu.
Đường dẫn font trong CSS mới bắt đầu bằng ../assets/fonts/.

Font sử dụng là SVN-Omny, có Arial và sans-serif dự phòng.
Màu sắc kế thừa bảng màu Mena Select đã có.
Body sử dụng margin: 0. Ảnh có quy tắc giới hạn chiều rộng.
Ảnh DevTools đã cho thấy quy tắc được lấy từ style.css.

## 4. CSS selector và Box Model

- Element selector chọn theo tên thẻ, ví dụ img và a.
- Class selector chọn theo class, ví dụ .product-card.
- Descendant selector chọn phần tử bên trong một phần tử khác,
  ví dụ .product-card h3.
- Margin tạo khoảng cách ngoài đường viền.
- Padding tạo khoảng đệm trong đường viền.
- Border tạo đường viền. Border-radius bo góc.
- Box-sizing: border-box làm kích thước khai báo bao gồm padding
  và border, không bao gồm margin.

Trong bản CSS bổ sung, thân thẻ có padding 16px 16px 18px.
Liên kết chi tiết có margin-top: 16px và padding 10px 14px.
Tên sản phẩm có font-size: 15px, giá có font-size: 22px.

## 5. Flexbox

Thân thẻ sử dụng display: flex và flex-direction: column.
Justify-content: flex-start bố trí nội dung từ đầu trục chính.
Align-items: stretch giúp các phần tử giãn theo chiều ngang.
Gap: 6px tạo khoảng cách giữa các phần tử con.

Liên kết chi tiết dùng Flexbox để căn nhãn và biểu tượng:
justify-content: space-between, align-items: center, gap: 10px.

### Câu hỏi tự kiểm tra

- Display: flex đặt trên phần tử cha.
- Space-between đưa các mục đầu và cuối về hai đầu trục chính,
  phân phối khoảng trống còn lại giữa các mục.
- Gap tạo khoảng cách giữa các mục. Margin thuộc từng phần tử
  và có thể tạo khoảng cách ở mép ngoài.

## 6. CSS Grid

Danh sách sản phẩm sử dụng display: grid và gap: 20px.

| Chiều rộng CSS viewport | Số cột khai báo |
|---|---:|
| Dưới 600px | 1 |
| Từ 600px đến dưới 1040px | 2 |
| Từ 1040px | 4 |

Grid-template-columns khai báo các cột.
Repeat giúp lặp lại cấu trúc cột.
Minmax(0, 1fr) chia đều không gian và cho phép cột co lại.

Object-fit: cover lấp đầy khung nhưng có thể cắt ảnh.
Bài giữ object-fit: contain để ảnh bao bì hiển thị nguyên vẹn.

## 7. Hover và focus

Liên kết chi tiết có hover đổi màu nền và viền.
Transition làm chuyển đổi màu diễn ra nhẹ trong 0.2 giây.
Focus-visible tạo viền nhận diện khi điều hướng bằng bàn phím.
Liên kết ảnh dùng outline-offset: -4px để đặt viền vào phía trong.

Hover gắn với con trỏ chuột. Focus là trạng thái phần tử
đang nhận điều hướng hoặc tương tác bàn phím.

## 8. Kiểm tra và tự điều chỉnh

Trong quá trình thực hành, trang từng mất định dạng sau khi
thay CSS. Tệp styles.css đã được khôi phục bằng Ctrl+Z,
lưu lại và tải lại trang. Ảnh sau đó cho thấy CSS hiển thị trở lại.
Nguyên nhân chính xác của lần mất định dạng chưa được xác định.

| Nội dung kiểm tra | Trạng thái có bằng chứng |
|---|---|
| Trang HTML mở được | Đạt trên ảnh đã cung cấp |
| CSS được áp dụng | Đạt, DevTools hiển thị nguồn style.css |
| Bốn ảnh sản phẩm hiển thị | Đạt trên ảnh đã cung cấp |
| Liên kết mở đúng trang đích | Chưa xác nhận thao tác nhấp |
| Bố cục khu vực ở viewport 1366px | Hiển thị bốn cột trên ảnh đã cung cấp |
| Hover/focus sau phần CSS bổ sung | Cần kiểm tra sau khi lưu |
| Có tự điều chỉnh khi gặp vấn đề | Đã khôi phục stylesheet bằng Ctrl+Z |

## 9. Sử dụng AI và cập nhật GitHub

Claude hỗ trợ các lượt phân tích đã được cung cấp.
ChatGPT rà soát phản hồi, điều chỉnh mã và hướng dẫn kiểm tra.

Các đề xuất được đối chiếu với mã nguồn và ảnh thực tế.
Không thêm dữ liệu sản phẩm, giá, khuyến mãi hoặc chức năng
mua hàng chưa có trong bài.

Nhật ký chi tiết được lưu trong AI_USAGE.md và cập nhật bổ sung.

Repository:

Website đã triển khai:

## Bảy câu hỏi kiến thức

1. HTML5 được sử dụng gồm section, header, article, h2/h3,
   ul/li, img và a. Chúng thể hiện khu vực, danh sách và
   từng sản phẩm, đồng thời tổ chức ảnh và liên kết.

2. Margin nằm ngoài đường viền, padding nằm trong đường viền.
   Ví dụ liên kết chi tiết có margin-top: 16px, thân thẻ có
   padding: 16px 16px 18px.

3. Flexbox được sử dụng trong thân thẻ và liên kết chi tiết.
   Justify-content căn theo trục chính, align-items căn theo
   trục còn lại.

4. Flexbox chủ yếu tổ chức theo một trục. Grid tổ chức theo
   hàng và cột, phù hợp với danh sách sản phẩm.

5. Nếu bỏ display: grid, danh sách có thể trở về luồng khối,
   các sản phẩm xếp dọc và cấu hình cột Grid không còn tác dụng.

6. Alt truyền đạt nội dung ảnh khi người dùng không xem được ảnh,
   bao gồm trường hợp sử dụng trình đọc màn hình.

7. Nhận xét của AI về div chứa article đã được điều chỉnh:
   cấu trúc đó hợp lệ. Ul/li được chọn để cải thiện ngữ nghĩa,
   thay vì trình bày đây là một lỗi cú pháp.