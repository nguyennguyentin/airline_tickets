# airline_tickets
# Airline Tickets – Hệ thống đặt vé máy bay trực tuyến

Website hỗ trợ người dùng tìm kiếm chuyến bay, lựa chọn chỗ ngồi, đặt vé và quản lý thông tin vé máy bay. Hệ thống có các khu vực dành cho khách hàng và nhân viên/quản trị viên, cùng những chức năng hỗ trợ vận hành như quản lý chuyến bay, vé, người dùng và thanh toán.

> **Loại dự án:** Dự án nhóm học tập tại CodeGym  
> **Thời gian thực hiện:** 05/2025 – 06/2025  
> **Quy mô nhóm:** 6 thành viên

## Mục lục

- Giới thiệu
- Chức năng chính
- Công nghệ sử dụng
- Đóng góp cá nhân
- Cấu trúc dự án
- Yêu cầu môi trường
- Cài đặt và chạy dự án
- Cấu hình cần thiết
- Cơ sở dữ liệu
- Định hướng phát triển

## Giới thiệu

**Airline Tickets** là ứng dụng web đặt vé máy bay được xây dựng theo mô hình ứng dụng Java Spring Boot. Dự án cung cấp luồng nghiệp vụ từ tìm kiếm chuyến bay, lựa chọn ghế, đặt vé đến xem thông tin vé; đồng thời có các chức năng quản trị để quản lý dữ liệu hệ thống.

Dự án được thực hiện theo hình thức làm việc nhóm. README này mô tả các chức năng ở mức tổng quan; phần đóng góp cá nhân bên dưới tập trung vào các hạng mục mà tôi tham gia.

## Chức năng chính

### Khách hàng

- Tìm kiếm và xem thông tin chuyến bay.
- Xem thông tin chuyến bay và lựa chọn ghế.
- Thực hiện quy trình đặt vé.
- Xem thông tin vé đã đặt và xuất/in vé PDF.
- Đăng nhập bằng tài khoản hệ thống; hỗ trợ đăng nhập Google.
- Gửi đánh giá và nhận thông tin qua email theo các luồng được triển khai.
- Trao đổi hỗ trợ trực tuyến với bộ phận hỗ trợ.

### Nhân viên / Quản trị viên

- Quản lý chuyến bay và thông tin ghế.
- Quản lý vé và thông tin đặt vé.
- Quản lý tài khoản người dùng.
- Theo dõi, xử lý các nghiệp vụ liên quan đến khách hàng.
- Hỗ trợ thống kê/báo cáo và quản lý nội dung hệ thống.

### Một số chức năng kỹ thuật

- Giao diện đa ngôn ngữ (tiếng Việt và tiếng Anh).
- Xác thực và phân quyền bằng Spring Security.
- Gửi email thông qua cấu hình SMTP.
- Tích hợp các thành phần thanh toán trực tuyến theo cấu hình dự án.
- Hỗ trợ cập nhật dữ liệu/trao đổi thời gian thực ở một số chức năng.

## Công nghệ sử dụng

| Thành phần | Công nghệ |
|---|---|
| Ngôn ngữ | Java 17 |
| Backend | Spring Boot 3.4.4, Spring MVC |
| Tầng dữ liệu | Spring Data JPA, Hibernate |
| Cơ sở dữ liệu | MySQL |
| Giao diện | Thymeleaf, HTML, CSS, JavaScript |
| Bảo mật | Spring Security, OAuth2 Client |
| Build tool | Gradle |
| Email | Spring Boot Mail |
| PDF | iText html2pdf |
| Tích hợp khác | Firebase Admin, Google Cloud Storage, WebSocket, Pusher |
| Kiểm thử | JUnit / Spring Boot Test |

## Đóng góp cá nhân

Trong dự án nhóm, tôi tham gia phát triển các chức năng quản lý và xử lý thông tin người dùng/vé. Các hạng mục tôi đảm nhiệm gồm:

- **Quản lý người dùng:** thêm, sửa, xóa và tìm kiếm người dùng.
- **Quản lý quyền truy cập:** hỗ trợ phân quyền tài khoản.
- **Quản lý trạng thái tài khoản:** khóa và mở khóa người dùng.
- **Xuất/in PDF:** hoàn thiện chức năng tạo tài liệu PDF liên quan đến vé/hóa đơn.
- **Giao diện quản trị:** cập nhật các thành phần giao diện liên quan đến khu vực quản lý.

Tôi cũng tham gia xử lý lỗi và hoàn thiện các chức năng trong phạm vi được giao. Dự án được phát triển theo nhóm nên các chức năng tổng quan ở trên không đồng nghĩa toàn bộ đều do cá nhân tôi thực hiện.

## Cấu trúc dự án

```text
airline_tickets/
├── src/
│   └── main/
│       ├── java/com/codegym/airline_tickets/
│       │   ├── annotation/       # Annotation tùy chỉnh
│       │   ├── aspect/           # AOP và logging
│       │   ├── config/           # Cấu hình ứng dụng
│       │   ├── controller/       # Điều phối request web/API
│       │   ├── dto/              # Data Transfer Objects
│       │   ├── entity/           # Các entity
│       │   ├── repository/       # Truy cập dữ liệu
│       │   ├── security/         # Thành phần bảo mật
│       │   ├── service/          # Nghiệp vụ
│       │   └── util/             # Tiện ích
│       └── resources/
│           ├── i18n/             # Tài nguyên đa ngôn ngữ
│           ├── static/           # CSS, JavaScript, hình ảnh
│           ├── templates/        # Thymeleaf templates
│           └── application.properties
├── airline_tickets.sql           # Script cơ sở dữ liệu
├── build.gradle
├── gradlew
└── gradlew.bat
```

## Yêu cầu môi trường

Để chạy dự án, cần chuẩn bị:

- JDK 17
- MySQL
- Git
- IDE hỗ trợ Java/Gradle (IntelliJ IDEA, Eclipse hoặc VS Code có extension Java)

Một số chức năng tích hợp bên ngoài (email, OAuth Google, thanh toán, Firebase/Pusher) cần thông tin cấu hình tương ứng. Nếu chưa cấu hình các dịch vụ này, những chức năng liên quan có thể không hoạt động đầy đủ.

## Cài đặt và chạy dự án

### 1. Clone repository

```bash
git clone https://github.com/nguyennguyentin/airline_tickets.git
cd airline_tickets
```

### 2. Tạo cơ sở dữ liệu

Tạo database MySQL, sau đó import file `airline_tickets.sql` trong thư mục gốc dự án.

Ví dụ với MySQL:

```sql
CREATE DATABASE airline_ticket;
```

Có thể import bằng MySQL Workbench hoặc dòng lệnh:

```bash
mysql -u root -p airline_ticket < airline_tickets.sql
```

### 3. Cấu hình kết nối

Mở `src/main/resources/application.properties` và cập nhật thông tin kết nối MySQL theo môi trường của bạn:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/airline_ticket?createDatabaseIfNotExist=true
spring.datasource.username=YOUR_DB_USERNAME
spring.datasource.password=YOUR_DB_PASSWORD
```

**Lưu ý:** Không đưa mật khẩu database, mật khẩu email, OAuth client secret hoặc khóa API thật lên GitHub. Nên dùng biến môi trường hoặc file cấu hình riêng không được commit.

### 4. Chạy ứng dụng

Trên Windows:

```bash
gradlew.bat bootRun
```

Trên macOS/Linux:

```bash
./gradlew bootRun
```

Hoặc mở dự án bằng IDE, đồng bộ Gradle và chạy lớp:

```text
com.codegym.airline_tickets.AirlineTicketsApplication
```

Sau khi ứng dụng khởi động, truy cập địa chỉ localhost với cổng được cấu hình trong ứng dụng (mặc định Spring Boot là `8080`):

```text
http://localhost:8080
```

> **Ghi chú:** Dự án có sử dụng một số dịch vụ ngoài và cấu hình riêng. Các bước trên là hướng dẫn khởi chạy cơ bản; có thể cần bổ sung cấu hình trước khi sử dụng toàn bộ chức năng.

## Cấu hình cần thiết

Các cấu hình thường cần kiểm tra trong `application.properties` hoặc cấu hình môi trường:

- MySQL: URL, username, password.
- SMTP: máy chủ email và thông tin xác thực.
- OAuth Google: client ID và client secret.
- Dịch vụ thanh toán: thông tin môi trường/khóa tích hợp.
- Firebase, Google Cloud Storage hoặc Pusher: thông tin xác thực và cấu hình tương ứng nếu sử dụng các chức năng liên quan.

Không sử dụng thông tin xác thực có sẵn trong bản mã nguồn để triển khai thật. Hãy thay bằng thông tin của môi trường cá nhân.

## Cơ sở dữ liệu

Dự án sử dụng MySQL và cung cấp script khởi tạo dữ liệu tại `airline_tickets.sql`.

Các nhóm dữ liệu chính liên quan đến nghiệp vụ gồm người dùng, chuyến bay, sân bay, ghế, đặt vé/vé và các dữ liệu hỗ trợ nghiệp vụ. Cấu trúc cụ thể được thể hiện trong script SQL đi kèm.

## Định hướng phát triển

- Hoàn thiện tài liệu API và mô tả rõ các luồng nghiệp vụ.
- Bổ sung kiểm thử đơn vị và kiểm thử tích hợp cho các nghiệp vụ chính.
- Tách thông tin nhạy cảm khỏi file cấu hình và chuẩn hóa cấu hình theo môi trường.
- Cải thiện trải nghiệm giao diện trên thiết bị di động.
- Bổ sung hướng dẫn triển khai và ảnh chụp giao diện thực tế.

## Thông tin dự án

- **Tên dự án:** Airline Tickets
- **Hình thức:** Dự án nhóm học tập
- **Đơn vị đào tạo:** CodeGym
- **Thời gian:** 05/2025 – 06/2025
- **GitHub:** [nguyennguyentin/airline_tickets](https://github.com/nguyennguyentin/airline_tickets)
