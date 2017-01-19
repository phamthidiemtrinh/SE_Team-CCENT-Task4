# cấu hinh cơ bản trên router

## 1. Thành phần
- internal components (các thành phần bên trong) : CPU, ROM, FLASH , NVRAM, RAM
- external components ( các thành phần bên ngoài- interface) : WAN, LAN, console/AUX
- trong đónvram
    - CPU : thực hiện chỉ thị của hệ điều hành, khởi tạo hệ thống, định tuyến, điều khiển các cạc mạng
    - ROM : chỉ có thể sử dụng tạm thời, chứa các chương trình kiểm tra phần cứng cho router, hệ điều hành phụ dự phòng cho trường hợp hệ điều hành chinh bị lỗi,  chương trình bootrap
    - RAM : gồm bộ nhớ chính và bộ nhớ chia sẻ. Bộ nhớ chính sử dụng các chức năng của router  nhứ lưu file, run, chứa bản định tuyến, running- config, bộ nhớ chia sẻ dùng để bffer tiến trình đang xử lý. có thể năng cấp ram
    - NVRAM : để lưu trữ file đặc biệt là startup configuration, chứa cấu hình được lưu của router, khi tắt router nội dung trong NVRAM vẫn còn
    - FLASH: tương đương với ổ cứng trên PC . chứa nguồn tài nguyên của router, chứa hệ điều hành chính thức của router (IOS) dưới dạng nén, thực hiện được các thao tác trên dữ liệu
    - các system bus, CPU bus : dùng ddể truyền dữ liệu
    - interface :  các cổng mạng ( giao diện) gồm có : LANs, WANs, console/AUX
    
  ## 2. cấu hình trên router
  - dùng cáp console, đầu RJ45 đấu vào router, chú ý không cắm cáp vào nhầm cổng
  - khởi động chương trình đặc biệt ( Hyper Terminal ) để thực hiện cấu hình cơ bản và truyền lệnh cho router
  - start--> all programs --> Accessories--> communicatións --> hyper terminal
  - mô tả tên tùy ý cho router
  - tiến hành thiết lập thông số cho router --->restore default --> ok
  
  
    
   
