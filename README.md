# Tìm hiểu mô hình OSI  
Tên: Hallen_Trần  
Ngày cập nhật: 16/04/2017 
---  
## 1.OSI là gì?  

**Mô hình OSI (Open system interconnection – Mô hình kết nối các hệ thống mở) là một thiết kế dựa vào nguyên lý tầng cấp, lý giải một cách trừu tượng kỹ thuật kết nối truyền thông giữa các máy vi tính và thiết kế giao thức mạng giữa chúng.**   

![img](http://www.vnpro.vn/wp-content/uploads/2015/11/Osi-model-jb-600x639.png)

*Trong mô hình phân lớp:*

**Lớp 1 Physical (lớp vật lý):** truyền dòng bit thô qua đường truyền vật lý cụ thể. Nó định nghĩa các đặc tính kĩ thuật về điện, cơ, quang, đặc tính kỹ thuật trong việc thiết lập, giải phóng , duy trì một đường truyền nào đó.  

**Lớp 2 Data Link (lớp liên kết dữ liệu):** điều khiển dữ liệu truy nhập vào đường truyền vật lý,giao tiếp vớilớp Network, cung cấp cơ chế dò lỗi.  

**Lớp 3 Network (lớp mạng):** phân bố dữ liệu ( định tuyến các gói dữ liệu),xác định đường đi tối ưu nhất để phân phối dữ liệu, định địa chỉ logic cho hệ thống mạng( địa chỉ IP).  

**Lớp 4 Transport (lớp giao vận):** quản lý các kết nối đầu cuối( end-to-end), xử lí vấn dề truyền dẫn giữa các host, đảm bảo dữ liệu truyền một cách tin cậy từ điểm này đến điểm khác trong mạng, thu hồi hoặc duy trì các kết nối ảo, cung cấp cơ chế dò lỗi, phục hồi dữ liệu.  

**Lớp 5 Session (lớp phiên):** thiết lập, quản lý và giải phóng các session giữa các ứng dụng ( tổ chức các phiên kết nối giữa các ứng dụng).  

**Lớp 6 Presentation (lớp trình diễn):** đảm bảo dữ liệu từ nơi guiẻ đến nơi nhận có thể đọc ddược, cung cấp cơ chế mã hóa.  

**Lớp 7 Application (lớp ứng dụng):** giao tiếp trực tiếp với người dùng,cung cấp các ứng dụng mạng,cung cấp cơ chế xác thực người dùng.  
![img](http://2.bp.blogspot.com/-PEx2b0DNHY4/U4_p1YtCTZI/AAAAAAAAAB4/EzujsHncwKA/s1600/1.PNG)  


## 2.Phương thức hoạt động của OSI?  
–  Mỗi tầng trong mô hình OSI, có hai phương thức hoạt động chính được áp dụng đó là: phương thức hoạt động có liên kết (connection–oriented) và không có liên kết (connectionless).  

–  Với phương thức có liên kết, trước khi truyền dữ liệu cần thiết phải thiết lập một liên kết logic giữa các thực thể cùng lớp (layer). Còn với phương thức không có liên kết, thì không cần lập liên kết logic và mỗi đơn vị dữ liệu trước hoặc sau đó.  

–  Phương thức có liên kết, quá trình truyền dữ liệu phải trải qua 3 giai đoạn theo thứ tự:  
  - Thiết lập liên kết: hai thực thể đồng mức ở hai hệ thống thương lượng với nhau về tập các tham số sẽ được sử dụng trong giai đoạn sau.  
  - Truyền dữ liệu: dữ liệu được truyền với các cơ chế kiểm soát và quản lý.  
  - Hủy bỏ liên kết: giải phóng các tài nguyên hệ thống đã cấp phát cho liên kết để dùng cho các liên kết khác.  
-  Quá trình đóng gói dữ liệu gửi :  
  -  Người gửi: Gửi một dữ liệu người dùng,dữ liệu này đi đầu tiên vào tầngứng dụng và được đóng thêm một nhãnởtầngưng dụng, sau đó đi xuống tầng trình diễn lúc này toàn bộ nội dung của gói tin ở tầngứng dụng trở thành data của gói tin tầng trình diễn và tầng trình diễn đóng thêm một nhãn vào gói tin, tương tự với các tầng còn lại, tức là toàn bộ gói tin tầng trên sẽ là dữ liệu gói tin tầng dưới, riêng tầng mạng sẽ được đóng IP header, còn tầng kết nối dữ liệu sẽ được đóng Frame header và bọc thêm phần kiễm tra lỗi FCS, sau khi gói tin đến tầng vật lý sẽ được chuyển sang dạng tín hiệu điện và được truyền dưới dạng bit 1 và bit 0.  
  ![img](http://3.bp.blogspot.com/-CRy6O9uSMLo/U4_p1WCpEMI/AAAAAAAAACA/-1vkyw0MUrk/s1600/2.PNG)  
- Quá trình mở gói dữ liệu:  
  Người Nhận: Lúc này quá trình diễn ra ngược lại so với quá trình người gửi, lúc này dòng bit nhị phân đi vào đường truyền vật lý và được đưa dần lên trên, đầu tiên khi đưa lên tầng liên kết dữ liệu nó sẽ được chuyển thành cấu trúc khung thành một đơn vị dữ liệu tầng liên kết dữ liệu, sau đó dữ liệu bắt đầu gỡ bỏ Frame header và FCS ở tầng liên kết dữ liệu để chuyển lên tầng mạng, tầng mạng tiếp tục gỡ bỏ IP header để chuyển lên tầng phiên cứ như thế mỗi lần đi lên lần lượt dữ liệu lại bỏ đi một header và cuối cùng khi đến tay người nhận thì nó trả lại nguyên vẹn dữ liệu ban đầu.  
  ![img](http://4.bp.blogspot.com/-GLwwpCGieWo/U4_p1glHwpI/AAAAAAAAAB8/DippepZn-XY/s1600/3.PNG)

## 3.Quá trình truyền thông ngang hàng: 
  Quá trình truyền thông ngang hàng mô phỏng cuộc nói chuyện đồng cấp chứ không phải di chuyển từ trên suống, lúc này ta có tầngứng dụng như thể đang nói chuyện với ứng dụng vậy, tương tự cho các tầng còn lại, lúc này chúng ta có đơn vị dữ liệu của các kết nối ngang hàng là có tên riêng, đơn vị của tầng Giao vận là Segment hoạc Datagram, đơn vị của tầng Mạng là Packet, đơn vị của tầng Liên kết dữ liệu là Frame, đơn vị của tầng Vật lý là Bit.    
  ![img](http://3.bp.blogspot.com/-eF3I6Z5k2hc/U4_p2OCuPGI/AAAAAAAAABg/6FeNp9qDyeM/s1600/4.PNG)
  
  



