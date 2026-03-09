# Báo cáo dự án: HỆ THỐNG QUẢN LÍ NHÀ HÀNG
**Thành viên:**
11 - Nguyễn Hồng Anh Khôi
15 - Nguyễn Phúc Lộc
23 - Nguyễn Vạn Đăng Thành

# Mục lục
# Mục lục

- [I. Giới thiệu sản phẩm](#i-giới-thiệu-sản-phẩm)
  - [1. Tổng quan về dự án](#1-tổng-quan-về-dự-án)
  - [2. Tính năng sản phẩm](#2-tính-năng-sản-phẩm)

- [II. Hướng dẫn sử dụng](#ii-hướng-dẫn-sử-dụng)
  - [1. Cách cài đặt cục bộ](#1-cách-cài-đặt-cục-bộ)
  - [2. Hướng dẫn sử dụng các tính năng](#2-hướng-dẫn-sử-dụng-các-tính-năng)

- [III. Các công cụ đã dùng](#iii-các-công-cụ-đã-dùng)
  - [1. Các ngôn ngữ lập trình và thư viện](#1-các-ngôn-ngữ-lập-trình-và-thư-viện)
  - [2. Công cụ thứ ba](#2-công-cụ-thứ-ba)

- [IV. Mã nguồn](#iv-mã-nguồn)
  - [1. Mã nguồn](#1-mã-nguồn)
  - [2. Cấu trúc tệp](#2-cấu-trúc-tệp)
  - [3. Sơ đồ cơ sở dữ liệu](#3-sơ-đồ-cơ-sở-dữ-liệu)
  - [4. Danh sách endpoint API](#4-danh-sách-endpoint-api)

- [V. Tài liệu tham khảo](#v-tài-liệu-tham-khảo)
## I. Giới thiệu sản phẩm
### 1. Tổng quan về dự án
Hệ thống quản lí nhà hàng là một ứng dụng web được xây dựng nhằm hỗ trợ việc quản lí các hoạt động cơ bản trong nhà hàng một cách hiệu quả và thuận tiện hơn. Thay vì thực hiện việc ghi chép thủ công hoặc sử dụng nhiều công cụ rời rạc, hệ thống cho phép người quản lí theo dõi và xử lí thông tin tập trung trên một nền tảng duy nhất. Ứng dụng cung cấp các chức năng chính như quản lí danh sách món ăn, tạo và lưu trữ đơn hàng, cũng như thống kê doanh thu của nhà hàng theo thời gian.

Hệ thống được phát triển dựa trên công nghệ Node.js, Express cho phần xử lí phía máy chủ và giao diện web, kết hợp với cơ sở dữ liệu MySQL để lưu trữ và quản lí dữ liệu. Nhờ đó, các thông tin về món ăn, đơn hàng và doanh thu có thể được cập nhật nhanh chóng, chính xác và dễ dàng truy xuất khi cần thiết. Bên cạnh đó, việc xây dựng hệ thống dưới dạng ứng dụng web cũng giúp người dùng có thể truy cập và sử dụng trên nhiều thiết bị khác nhau thông qua trình duyệt.

Thông qua dự án này, mục tiêu chính là xây dựng một hệ thống quản lí nhà hàng đơn giản nhưng hiệu quả, giúp tự động hóa một số quy trình quản lí cơ bản, đồng thời tạo nền tảng để phát triển thêm các chức năng nâng cao trong tương lai.
### 2. Tính năng sản phẩm
- **Quản lí danh sách món ăn**
  - Sắp xếp theo các tiêu chí 
  - Thêm món ăn mới vào hệ thống
  - Chỉnh sửa thông tin món ăn (tên món, giá, loại món)
  - Xóa món ăn khỏi danh sách
  - Hiển thị danh sách toàn bộ món ăn
- **Quản lí đơn hàng**
  - Các trạng thái quản lí
  - Tạo đơn hàng mới cho khách
  - Thêm các món ăn vào đơn hàng
  - Cập nhật số lượng món trong đơn
  - Tự động tính tổng tiền của đơn hàng
  - Lưu trữ thông tin đơn hàng vào cơ sở dữ liệu
- **Thống kê và báo cáo doanh thu**
  - Tính tổng doanh thu của nhà hàng
  - Thống kê doanh thu theo ngày
  - Thống kê doanh thu theo khoảng thời gian
  - Thống kê món ăn bán chạy, phân tích theo danh mục
- **Quản lí dữ liệu**
  - Lưu trữ dữ liệu bằng cơ sở dữ liệu SQL
  - Truy xuất và cập nhật dữ liệu nhanh chóng
  - Đảm bảo tính nhất quán của dữ liệu giữa hệ thống và cơ sở dữ liệu
## II. Hướng dẫn sử dụng
### 1. Cách cài đặt cục bộ
**Bước 1.** Cài Node.js: Tải từ nodejs.org, chọn bản LTS
**Bước 2.** Cài XAMPP: Để có MySQL + phpMyAdmin
**Bước 3.** Tạo Database: Copy nội dung database.sql dán vào trong tab SQL Go
**Bước 4.** Giải nén dự án + `npm install` để cài thư viện
**Bước 5.** `npm start` để mở chạy local ở: http://localhost:3000
### 2. Hướng dẫn sử dụng các tính năng
**Giao diện chính:**
![image](https://hackmd.io/_uploads/B1lcjU3tZe.png)
#### a. Quản lý thực đơn
Ở mục **Quản lý Menu** chọn nút `Thêm Món Mới` và điền các thông tin cần thiết để thêm món.
![image](https://hackmd.io/_uploads/rJaonInt-g.png)
![image](https://media.discordapp.net/attachments/1379781893829955604/1480577464098099487/image.png?ex=69b02eb7&is=69aedd37&hm=6a79a56eff57da8d93bed3f86789a8b6095c1933ad89128a48394d7af43b80cc&=&format=webp&quality=lossless&width=2694&height=1364)
#### b. Quản lý đơn hàng
Tính năng giúp tạo và quản lí đơn hàng, ở mục **Quản lí đơn hàng**, bấm vào nút **Tạo đơn hàng** để tạo đơn hàng mới.
![image](https://hackmd.io/_uploads/SkxKaLhKZg.png)
Lựa chọn thêm các món, chỉnh số lượng,...
![image](https://hackmd.io/_uploads/BJaC6IhFWg.png)
Tuỳ chỉnh Xem, Chuẩn bị hoặc Huỷ đơn hàng.
![image](https://hackmd.io/_uploads/SkT4CUhtbx.png)

#### c. Thống kê thu nhập
Ở mục **Thống kê thu nhập**, chúng ta có thể xem các thống kê doanh thu, món bán chạy nhất,... điều chỉnh xem theo khoảng thời gian tuỳ chỉnh.
![image](https://hackmd.io/_uploads/SykcALhFWg.png)
## III. Các công cụ đã dùng
### 1. Các ngôn ngữ lập trình và thư viện
- **Ngôn ngữ lập trình:** Node.js
- **Cơ sở dữ liệu:** MySQL
- **Giao diện:** HTML, CSS, JavaScript
- **Thư viện:** cors ``(2.8.5)``, express ``(4.21.0)``, mysql2 ``(3.11.0)``
### 2. Công cụ thứ ba
- **Gemini, Claude:** Hỗ trợ viết mã nguồn, chỉnh sửa lỗi,...
- **Các prompt đã sử dụng:**
[Hộp thoại Claude](https://claude.ai/share/2654eb23-9b03-478b-9a7c-3dc0c791c83f)

| Mục tiêu                                   | Nội dung Prompt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Kiến trúc & phân tích yêu cầu           | Tóm tắt và phân tích yêu cầu cho một "Hệ thống quản lý nhà hàng" dạng web dùng JavaScript (frontend + Node.js/Express backend) và SQL (MySQL/Postgres). Hãy trả về: 1) danh sách module chính (mỗi module kèm 2–4 chức năng con), 2) yêu cầu chức năng (functional requirements) dưới dạng bullet, 3) yêu cầu phi chức năng chính (performance, security, backup, availability) dưới dạng bullet ngắn, 4) mô tả sơ đồ kiến trúc (frontend → backend → database, kèm các boundary như API, auth, caching) và đề xuất stack công nghệ cụ thể (frontend libs, DB, hosting). Đầu ra súc tích, chuẩn để chèn vào báo cáo kỹ thuật. |
| 2. Thiết kế cơ sở dữ liệu & truy vấn SQL   | Thiết kế mô hình dữ liệu (ERD) cho hệ thống quản lý nhà hàng gồm: menu, categories, users (admin/staff), orders, order_items, inventory (nếu cần). Hãy trả về: 1) danh sách bảng với field, kiểu dữ liệu, ràng buộc PK/FK/unique và chỉ rõ các index cần thiết, 2) SQL DDL (CREATE TABLE) tương thích với MySQL và với PostgreSQL—ghi rõ khác biệt nếu có, 3) 3 truy vấn mẫu tối ưu kèm giải thích: a) tổng doanh thu theo ngày trong khoảng A..B, b) doanh thu theo tháng trong năm X, c) top 5 món bán chạy trong khoảng thời gian. Trả dạng rõ ràng, dễ chèn vào báo cáo.                                                  |
| 3. Backend API & logic (Node.js / Express) | Viết API specification cho module "Quản lý món ăn" và "Quản lý đơn hàng" theo chuẩn REST (Express). Với mỗi endpoint nêu: phương thức, route, tham số (body/query/path), ví dụ request/response JSON, mã lỗi tiêu biểu và mô tả. Thêm phần mô tả flow tạo đơn hàng chi tiết: kiểm tra tồn kho (nếu có), tính tổng, transaction để insert vào orders và order_items, rollback khi lỗi; nêu cách xử lý race condition, gợi ý lock/index và ví dụ pseudo-code Node.js/SQL cho phần transaction. Đầu ra dạng bảng + đoạn code mẫu ngắn.                                                                                           |
| 4. Frontend UI/UX & tương tác (JavaScript) | Mô tả wireframe và UX flow cho 3 trang: Quản lý món ăn, Tạo đơn hàng, Thống kê doanh thu. Với mỗi trang nêu thành phần UI chính, hành vi (thêm/sửa/xóa, validate, confirmation, toast), và flow người dùng. Kèm 1 ví dụ component React (hoặc vanilla JS nếu yêu cầu) để: a) hiển thị danh sách món từ GET /menu (fetch + xử lý lỗi), b) form thêm món POST /menu với validation client-side; include mẫu request/response và cách hiển thị lỗi cho người dùng.                                                                                                                                                               |
| 5. Kiểm thử, debug & tài liệu hóa          | Viết checklist test cases (unit + integration) cho các phần: API tạo đơn, truy vấn báo cáo doanh thu, UI form validation — mỗi test gồm mô tả, input mẫu, expected output, loại test. Thêm checklist debug khi Node.js không kết nối DB (env vars, connection string, network, pool, firewall, migration), mẫu log lỗi và đề xuất format log JSON (timestamp, level, service, msg, error_code, meta). Kèm phần "How to reproduce" cho 3 lỗi phổ biến và cách fix ngắn gọn.                                                                                                                                                    |


## IV. Mã nguồn
### 1. Mã nguồn:
Bấm vào liên kết mã GitHub để xem toàn bộ mã nguồn: [Liên kết]([...](https://github.com/nplorz/restaurant-management))
### 2. Cấu trúc tệp
```
Resautant Management/
├── database.sql
├── node_modules
├── package-lock.json
├── package.json/
├── public/
│   ├── index.html
│   ├── script.js
│   └── style.css
└── src/
    ├── config/
    │   └── database.js
    ├── routes/
    │   ├── menu.js
    │   ├── orders.js
    │   └── statistics.js
    └── server.js
```
### 3. Sơ đồ cơ sở dữ liệu
![data](https://hackmd.io/_uploads/SJOOuGitWl.png)
### 4. **Danh sách endpoint API:**
| Method | Endpoint | Mô tả |
|--------|----------|--------|
| GET    | `/api/menu?search=...&sort=price_asc` | Lấy menu (có tìm kiếm + sắp xếp) |
| POST   | `/api/menu` | Thêm món mới |
| PUT    | `/api/menu/:id` | Cập nhật món |
| PATCH  | `/api/menu/:id/toggle` | Bật/tắt trạng thái |
| DELETE | `/api/menu/:id` | Xóa món |
| GET    | `/api/orders` | Lấy đơn hàng |
| POST   | `/api/orders` | Tạo đơn hàng |
| PATCH  | `/api/orders/:id/status` | Cập nhật trạng thái |
| GET    | `/api/statistics?type=daily&date=...` | Thống kê |

## V. Tài liệu tham khảo
- [Dự án RestaurantMS](https://github.com/NHViet03/Java_Project_RestaurantMS) - Dự án quản lí nhà hàng của nhóm sinh viên.
- [XAMPP](https://www.apachefriends.org/download.html) - Tham khảo host database cục bộ.