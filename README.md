# **SampleApi với Net Core ws - MongoDB Driver**

---

## **1. Mục tiêu**
Triển khai một API RESTful để quản lý dữ liệu sách, sử dụng cơ sở dữ liệu MongoDB và công nghệ ASP.NET Core. Chức năng bao gồm:
- Lấy danh sách sách.
- Tìm sách theo ID.
- Thêm sách mới.
- Cập nhật thông tin sách.
- Xóa sách.

---

## **2. Kiến thức áp dụng**

### **2.1. MongoDB**
- Là cơ sở dữ liệu NoSQL dạng document.
- Dữ liệu được lưu trữ dưới dạng JSON-like (BSON).
- Các thành phần chính:
  - **Database:** Tập hợp các collections.
  - **Collection:** Tập hợp các documents.
  - **Document:** Đơn vị cơ bản lưu trữ dữ liệu.

### **2.2. ASP.NET Core**
- Sử dụng Dependency Injection (DI) để quản lý các dịch vụ.
- Áp dụng IOptions Pattern để nạp cấu hình từ file `appsettings.json`.
- Sử dụng Controller để xây dựng các endpoint RESTful.

### **2.3. Swagger**
- Công cụ tạo tài liệu API.
- Cung cấp giao diện trực quan để kiểm tra và tương tác với các endpoint.

---

## **3. Hướng dẫn sử dụng**

### **3.1. Cấu hình cơ sở dữ liệu**
- Đảm bảo MongoDB đang chạy trên máy (localhost) hoặc sử dụng MongoDB Atlas nếu cần kết nối từ xa.
- Cấu hình thông tin kết nối trong tệp cấu hình ứng dụng `appsettings.json`.

### **3.2. Khởi chạy ứng dụng**
- Sử dụng lệnh `dotnet run` để khởi chạy ứng dụng ASP.NET Core.
- Truy cập Swagger thông qua đường dẫn: ```https://localhost:7149/swagger/index.html ```

### **3.3. Thao tác với API qua Swagger**
- **Lấy danh sách sách:** Sử dụng endpoint `GET /api/Books`.
- **Tìm sách theo ID:** Gửi yêu cầu đến `GET /api/Books/{id}` với giá trị ID của sách cần tìm.
- **Thêm sách mới:** Gửi yêu cầu `POST /api/Books` với nội dung sách mới trong phần body.
- **Cập nhật thông tin sách:** Gửi yêu cầu `PUT /api/Books/{id}` với thông tin sách cập nhật.
- **Xóa sách:** Gửi yêu cầu `DELETE /api/Books/{id}` để xóa sách theo ID.

---

## **4. Kết quả mong đợi**

### **4.1. Khi lấy danh sách sách**
- API trả về danh sách các sách hiện có trong cơ sở dữ liệu.
![Image](https://github.com/user-attachments/assets/e3c51fcd-728a-4013-916a-1358598ed9f9)

### **4.2. Khi lấy danh sách sách theo ID**
- API trả về danh sách các sách hiện có trong cơ sở dữ liệu theo ID.
![Image](https://github.com/user-attachments/assets/006bbcd2-aed8-4e39-afd7-8d23a6ea6afe)

### **4.3. Khi thêm sách mới**
- API trả về trạng thái thành công, và sách mới sẽ xuất hiện trong danh sách.
![Image](https://github.com/user-attachments/assets/21cb1436-9be6-4d95-aea8-68ff47b810ef)
![Image](https://github.com/user-attachments/assets/f952f75d-77ea-4a66-8ad3-d42a92dd022e)
![Image](https://github.com/user-attachments/assets/1ef14929-35f8-4677-913b-381f88191cab)

### **4.4. Khi cập nhật thông tin sách**
- Thông tin sách được cập nhật trong cơ sở dữ liệu và có thể kiểm tra lại qua endpoint `GET /api/Books/{id}`.
![Image](https://github.com/user-attachments/assets/3c63f763-1a88-4512-837e-5c5ca172fad2)
![Image](https://github.com/user-attachments/assets/d2a31aff-2749-4b43-ac69-29873dde63f8)
![Image](https://github.com/user-attachments/assets/70418801-3a16-4b2d-82db-584ceb881f9b)

### **4.5. Khi xóa sách**
- API trả về trạng thái thành công, và sách không còn tồn tại trong danh sách.
![Image](https://github.com/user-attachments/assets/37a44b61-2afe-409e-9079-9407755d8f2a)
![Image](https://github.com/user-attachments/assets/cbbb3113-7a25-4ad0-ad84-7ff5ff8ba91b)
---

## **5. Hình ảnh minh họa**

### **5.1. Giao diện Swagger**

![Image](https://github.com/user-attachments/assets/279fb9bd-35d3-4a28-bae9-b53aba157305)

### **5.2. Dữ liệu MongoDB hiển thị qua Compass**

![Image](https://github.com/user-attachments/assets/a367df97-bc04-4d65-8b76-dc4f61024050)

---

## Tham khảo
Bài làm được tham khảo bởi [https://learn.microsoft.com/en-us/aspnet/core/tutorials/min-web-api?view=aspnetcore-9.0&tabs=visual-studio-code](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mongo-app?view=aspnetcore-9.0&tabs=visual-studio)
