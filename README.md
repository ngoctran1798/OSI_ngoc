# Tìm hiểu mô hình OSI  
Tên: Hallen_Trần  
Ngày cập nhật: 16/04/2017 
---  
[1.OSI là gì?]( OSI)  
[2.Phương thức hoạt động của OSI?]( Phương_Thức)  

<aname OSI> <a\>  
## 1.OSI là gì?  

**Mô hình OSI (Open system interconnection – Mô hình kết nối các hệ thống mở) là một thiết kế dựa vào nguyên lý tầng cấp, lý giải một cách trừu tượng kỹ thuật kết nối truyền thông giữa các máy vi tính và thiết kế giao thức mạng giữa chúng.**   

![img](http://www.vnpro.vn/wp-content/uploads/2015/11/Osi-model-jb-600x639.png)

*Trong mô hình phân lớp:*

**Lớp 1 Physical (lớp vật lý):** truyền dòng bit thô qua đường truyền vật lý cụ thể. Nó định nghĩa các đặc tính kĩ thuật về điện, cơ, quang, đặc tính kỹ thuật trong việc thiết lập, giải phóng , duy trì một đường truyền nào đó.  

**Lớp 2 Data Link:** điều khiển dữ liệu truy nhập vào đường truyền vật lý,giao tiếp vớilớp Network, cung cấp cơ chế dò lỗi.  

**Lớp 3 Network:** phân bố dữ liệu ( định tuyến các gói dữ liệu),xác định đường đi tối ưu nhất để phân phối dữ liệu, định địa chỉ logic cho hệ thống mạng( địa chỉ IP).  

**Lớp 4 Transport:** quản lý các kết nối đầu cuối( end-to-end), xử lí vấn dề truyền dẫn giữa các host, đảm bảo dữ liệu truyền một cách tin cậy từ điểm này đến điểm khác trong mạng, thu hồi hoặc duy trì các kết nối ảo, cung cấp cơ chế dò lỗi, phục hồi dữ liệu.  

**Lớp 5 Session:** thiết lập, quản lý và giải phóng các session giữa các ứng dụng ( tổ chức các phiên kết nối giữa các ứng dụng).  

**Lớp 6 Presentation:** đảm bảo dữ liệu từ nơi guiẻ đến nơi nhận có thể đọc ddược, cung cấp cơ chế mã hóa.  

**Lớp 7 Application:** giao tiếp trực tiếp với người dùng,cung cấp các ứng dụng mạng,cung cấp cơ chế xác thực người dùng.  

<aname Phương_thức><a\n>  
## 2.Phương thức hoạt động của OSI?  
3. Phương thức hoạt động của mô hình OSI
– Mỗi tầng trong mô hình OSI, có hai phương thức hoạt động chính được áp dụng đó là: phương thức hoạt động có liên kết (connection–oriented) và không có liên kết (connectionless).  

– Với phương thức có liên kết, trước khi truyền dữ liệu cần thiết phải thiết lập một liên kết logic giữa các thực thể cùng lớp (layer). Còn với phương thức không có liên kết, thì không cần lập liên kết logic và mỗi đơn vị dữ liệu trước hoặc sau đó.  

– Phương thức có liên kết, quá trình truyền dữ liệu phải trải qua 3 giai đoạn theo thứ tự:  
  - Thiết lập liên kết: hai thực thể đồng mức ở hai hệ thống thương lượng với nhau về tập các tham số sẽ được sử dụng trong giai đoạn sau.  
  - Truyền dữ liệu: dữ liệu được truyền với các cơ chế kiểm soát và quản lý.  
  - Hủy bỏ liên kết: giải phóng các tài nguyên hệ thống đã cấp phát cho liên kết để dùng cho các liên kết khác.  



