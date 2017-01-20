# cấu hinh cơ bản trên router

## 1. Thành phần
- internal components (các thành phần bên trong) : CPU, ROM, FLASH , NVRAM, RAM
- external components ( các thành phần bên ngoài- interface) : WAN, LAN, console/AUX
- trong đó
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
  - các lệnh cơ bản:
    - user EXE mode : Router > enable [enter]: chuyển sang mode đặc biệt
    - privilege mode : router # : thự hiện hiển thị bất kỳ mọi thông số của router và có quyền đi đến bbất kỳ mode nào khác
    - router# configure terminal [enter] -> global configuratin router(config)#_ : cấu hình cho router 
    - sub-mode router(config-if)#_ : mọi câu lệnh được đưa ra chỉ ảnh hưởng tới interface cu thể nào đó
    - exit : từ mode trong ra ngòai
    - disable: để di từ privilege mode về User EXEC mode, nếu sử dụng lệnh exit tại đây thì sẽ đăng xuất ra khỏi router
    - router(config)#hostnam_ [tên][enter]: dổi tên router
    - Enable password: router(config)#enable_[pas][enter] ;  đặt mật khẩu từ lớp user vào privilege
    - router#show_running-config[enter] : xem file cấu hinh
    - console password:  router(config)#line_console_0[enter] -> router(config-line)#password_[pass]_[enter] -> router(config-line)#login[enter] : đặt password cho cổng console
    - router(config)#service_password-encryption[enter] : mã hóa toàn bộ password
    - router(config)#banner_motd_#khẩu hiệu# ;  đặt khẩu hiệu.
    - router#show_ip_interface_brief[emter]: kiểm tra xem router có những cổng nào và trạng thái của chúng
    - router(config-if)#no shutdown : mở cổng lên
    - router(config-if)#ip adress [ip][enter] : đặt địa chỉ ip cho cổng f0/0
    - router#copy running-config startup-config : lưu cấu hình
    - router#erase startup-config --> router#reload : xóa cấu hình cũ đã có trong router
    - router(config)#enable_secret_[pass] : đặt và đồng thời mã hóa mật khẩu.
    - router(config-line)# logging synchronous : ngăn chặn lệnh chen giữa 
