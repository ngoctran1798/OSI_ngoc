# OSI_ngoc
## OSI là gì?  

**Mô hình OSI (Open system interconnection – Mô hình kết nối các hệ thống mở) là một thiết kế dựa vào nguyên lý tầng cấp, lý giải một cách trừu tượng kỹ thuật kết nối truyền thông giữa các máy vi tính và thiết kế giao thức mạng giữa chúng.**  
!(http://www.vnpro.vn/wp-content/uploads/2015/11/Osi-model-jb-600x639.png) (<img/>) 

*Trong mô hình phân lớp:*

**Lớp 1 Physical (lớp vật lý):** truyền dòng bit thô qua đường truyền vật lý cụ thể. Nó định nghĩa các đặc tính kĩ thuật về điện, cơ, quang, đặc tính kỹ thuật trong việc thiết lập, giải phóng , duy trì một đường truyền nào đó.  

**Lớp 2 Data Link:** điều khiển dữ liệu truy nhập vào đường truyền vật lý,giao tiếp vớilớp Network, cung cấp cơ chế dò lỗi.  

**Lớp 3 Network:** phân bố dữ liệu ( định tuyến các gói dữ liệu),xác định đường đi tối ưu nhất để phân phối dữ liệu,định địa chỉ logic cho hệ thống mạng( địa chỉ IP).  

**Lớp 4 Transport:** quản lý các kết nối đầu cuối( end-to-end), xử lí vấn dề truyền dẫn giữa các host, đảm bảo dữ liệu truyền một cách tin cậy từ điểm này đến điểm khác trong mạng, thu hồi hoặc duy trì các kết nối ảo, cung cấp cơ chế dò lỗi, phục hồi dữ liệu.  

**Lớp 5 Session:** thiết lập, quản lý và giải phóng các session giữa các ứng dụng ( tổ chức các phiên kết nối giữa các ứng dụng).  

**Lớp 6 Presentation:** đảm bảo dữ liệu từ nơi guiẻ đến nơi nhận có thể đọc ddược, cung cấp cơ chế mã hóa.  

**Lớp 7 Application:** giao tiếp trực tiếp với người dùng,cung cấp các ứng dụng mạng,cung cấp cơ chế xác thực người dùng.  

