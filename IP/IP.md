# IP

## 1) `IP` là gì?

- `Địa chỉ IP`(Internet Protocol - giao thức Internet): Là một địa chỉ đơn nhất mà những thiết bị điện tử hiện nay đang sử dụng để nhận diện và liên lạc với nhau trên mạng máy tính bằng cách sử dụng giao thức Internet.

    - Giao thức Internet (Internet Protocol): Là một giao thức hướng dữ liệu được sử dụng bởi các máy chủ nguồn và đích để truyền dữ liệu trong một liên mạng chuyển mạch gói.

        - Liên mạng (internet): Là 2 hay nhiều mạng máy tính được kết nối với nhau bằng thiết bị Gateway cung cấp 1 phương thức phổ thông để định tuyến các gói thông tin giữa các mạng.

        - Chuyển mạch gói: là một kỹ thuật gửi dư liệu từ máy tính nguồn đến máy tính đích qua mạng dùng 1 loại giao thức thỏa mãn:

            - Dữ liệu được chia thành các gói nhỏ có kích thước và định dạng xác định.

            - Mỗi gói như vậy có thể được riêng rẽ và có thể đến nơi nhận bằng các đường truyền khác nhau từ đó chúng có chuyển cùng một thời điểm.

            - Khi toàn bộ các gói dữ  liệu được chuyển đến chúng sẽ đượcc hợp lại thành dữ liệu ban đầu 

            ```
            VD: Giao thức TCP/IP (Dùng trong Internet) thì kích thước tối đa của nó là 1500 byte.
            ``` 

- Bất kỳ thiết bị mạng nào  bao gồm bộ định tuyến (router), bộ chuyển mạng (switch), máy vi tính, máy chủ hạ tầng, máy in, máy fax qua Internet và vài loại điện thoại - tham gia vào mạng đều có địa chỉ riêng, và địa chỉ này là đơn nhất trong phạm vi của một mạng cụ thể.

- Địa chỉ IP do tổ chức cấp phát số liệu Internet tạo ra, nó phân chia những siêu khối điến cơ quan Internet khu vực, rồi từ đó phân chia lại thành những khối nhỏ hơn.

## 2) Cấu trúc của một địa chỉ IP.

### 2.1) `Ipv4`:

- Địa chỉ Ip được mã hóa theo phiên bản v4 sử dụng 32 bit để mã hóa dữ liệu do đó số địa chỉ tối đa có thể sử dụng là: 2^32

- Một địa chỉ Ipv4 thường được viết dưới dạng như sau: `198.35.26.96`. Những con số này do người sử dụng gán cho chúng.

- Cách biểu diễn địa chỉ: 32 bits địa chỉ của IP được chia thành 4 nhóm (dạng phân nhóm - dotted format), mỗi nhóm gồm 8 bits (gọi là một octet), các nhóm này phân cách nhau bởi dấu chấm. 

- Phân lớp địa chỉ: 
    - Ban đầu, một địa chỉ IP được chia thành hai phần:

        - Network ID: Xác lập bởi octet đầu tiên.

        - Host ID: Xác định bởi ba octet còn lại.
    
    - Ngày nay người ta phân địa chỉ IP ra làm 5 lớp phân biệt (class):

        - Lớp A: Lớp này bao gồm các địa chỉ IP có oc-tet đầu tiên có mang giá trị từ 1-126. Lớp A sẽ dành riêng cho địa chỉ của các tổ chức lớn trên thế giới. Lớp A có địa chỉ từ 1.0.0.1 đến 126.0.0.0.

        - Lớp B: Lớp này gồm các địa chỉ IP có oc-tet đầu tiên có giá trị từ 128-191. Lớp B sẽ dành cho tổ chức hạng trung trên thế giới. Lớp B có địa chỉ từ 128.1.0.0 đến 191.254.0.0.

        - Lớp C: Lớp này gồm các địa chỉ IP có oc-tet đầu tiên có giá trị từ 192-223. Lớp C được sử dụng trong các tổ chức nhỏ. Trong đó có cả máy tính cá nhân. Lớp C có địa chỉ từ 192.0.1.0 đến 223.255.254.0.

        - Lớp D: Lớp này gồm các địa chỉ IP có oc-tet đầu tiên có giá trị từ 224-239. Lớp D có 4 bit đầu tiên luôn là 1110. Đặc biệt lớp D được dành cho phát các thông tin (multicast/broadcast). Lớp này sẽ có địa chỉ từ 224.0.0.0 đến 239.255.255.255.

        - Lớp E: Lớp này gồm các địa chỉ IP có oc-tet đầu tiên có giá trị từ 240-255. Lớp E có 4 bit đầu tiên luôn là 1111. Lớp E được dành riêng cho việc nhiên cứu. Nó sẽ có địa chỉ từ 240.0.0.0 đến 254.255.255.255.

        - LOOPBACK: có địa chỉ 127.X.X.X được dùng riêng để kiểm tra vòng lặp quy hồi (loopback).

    - Trong thực tế, chỉ có các địa chỉ lớp A,B,C là được dùng để cài đặt cho các nút mạng. Địa chỉ lớp D được dùng trong một vài ứng dụng dạng truyền thông đa phương tiện. Riêng lớp E vẫn còn nằm trong phòng thí nghiệm và dự phòng.

### 2.2) `Ipv6`:

- Địa chỉ Ip được mã hóa theo phiên bản v6 sử dụng 128 bit để mã hóa dữ liệu.

- Ipv6 cho phép người dùng có thể sử dụng nhiều địa chỉ hơn so với Ipv4 

- Ipv6 được biểu diễn dưới dạng cụm số hexa phân cách bởi dấu : (ví dụ 2001:0DC8:1005:2F43:0BCD:FFFF).

- Khi nguồn tài nguyên Ipv4 đang dần cạn kiệt thì Ipv6 là sự lựa chọn vô cùng tuyệt vời.

- Lộ trình chuyển đổi ipv6 thay thế cho ipv4 đang dần dần bắt đầu, nhưng còn khá khó khăn do ipv4 tương thích với nhiều thiết bị cũ.

### 2.3) `Một số dòng Ip khác`

- Địa chỉ IP phiên bản từ 0 đến 3 bị hạn chế hoặc không sử dụng vì sự giới hạn và không thuận tiện của nó.

- Phiên bản v5 thường áp dụng chủ yếu làm giao thức dòng thử nghiệm.

- Một số phiên Bản khác cũng được thiết kế nhưng chỉ dừng lại ở mức thử nghiệm và không được sử dụng rộng rãi.

## 3) `Phân loại Ip`:

### 3.1) `Ip private`:

- Ip private (Ip nội bộ): là dãy các IP chỉ được sử dụng cho những máy tính thuộc một mạng nội bộ như mạng nhà trường, công ty, tổ chức…

- Ip privata hỗ trợ các máy tính trong hệ thống kết nối với nhau, chúng sẽ không được kết nối trực tiếp với các máy tính ngoài hệ thống.

- Ip private được thiết lập thủ công hoặc do router thiết lập tự động.

### 3.2) `Ip public`:

- Ip public là địa chỉ Ip cộng đồng, đây là Ip sử dụng trong mạng gia đình hoặc doanh nghiệp để kết nối Internet.

- Địa chỉ IP Public là yếu tố thiết yếu với bất kỳ phần cứng mạng có thể truy cập công khai nào (VD: Router gia đình  hoặc server).

- Các thông số của IP Public cần được ghi nhớ chính xác. Đặc biệt khi thuê máy chủ để thiết lập kết nối chính xác cho website của mình.


## 4) `Quản lý địa chỉ IP ở các cấp độ mạng`:

Địa chỉ IP cần được quản lý một cách hợp lý nhằm tránh xảy ra các xung đột khi đồng thời có hai địa chỉ IP giống nhau trên cùng một cấp mạng máy tính.

- Địa chỉ IP cần được quản lý một cách hợp lý nhằm tránh xảy ra các xung đột khi đồng thời có hai địa chỉ IP giống nhau trên cùng một cấp mạng máy tính.

- Ở các cấp mạng nhỏ hơn (WAN), người quản trị mạng cung cấp đến các lớp cho các mạng nhỏ hơn thông qua máy chủ DHCP.

- Ở các mạng nhỏ hơn nữa (LAN) thì việc quản lý địa chỉ IP nội bộ thường do các modem ADSL (có DHCP) gán địa chỉ IP cho từng máy tính (khi thiết đặt chế độ tự động trong hệ điều hành) hoặc do người sử dụng tự thiết đặt.

## 5) `Dùng chung IP trên Internet`:

- Do địa chỉ IP phiên bản IPv4 đang trở nên không đủ cung cấp cho tất cả những người đăng ký kết nối vào Internet nên rất nhiều máy tính đã phải dùng chung một địa chỉ IP ở cấp độ mạng toàn cầu.

- Do địa chỉ IP phiên bản IPv4 đang trở nên không đủ cung cấp cho tất cả những người đăng ký kết nối vào Internet nên rất nhiều máy tính đã phải dùng chung một địa chỉ IP ở cấp độ mạng toàn cầu.

- Ở mức độ sử dụng gia đình, các modem ADSL ngày nay (có nhiều hơn một cổng, có thể là RJ-45+USB hoặc 3-5 cổng RJ-45) cũng được tích hợp sẵn bộ định tuyến và cho phép nhiều máy tính cùng kết nối Internet dùng chung một IP làm đại diện.

- Các phương thức kết nối vào Internet bằng modem quay số (dial-up) trước đây không được tích hợp router. Việc chia sẻ kết nối Internet thường phải thông qua một máy tính đầu tiên, các máy tính sau kết nối qua router, switch, hub hoặc bằng các bo mạch mạng trên máy tính đó.

## 6) `Các thức truyền IP`:

### 6.1) `Unicast`:

- Unicast là 1 thuật ngữ được sử dụng để mô tả cách thức truyền tin được gửi từ 1 điểm đến 1 điểm khác. Trong trường hợp này chỉ có 1 nguồn gửi và 1 nguồn nhận.

- Việc truyền Unicast, trong đó 1 gói tin được gửi từ 1 nguồn duy nhất đến 1 địa điểm được quy định, vẫn là hình thức truyền chủ yếu trong mạng LAN và Internet.Tất cả các mạng LAN (VD: Ethernet) và mạng IP hỗ trợ chế độ Unicast, các ứng dụng sử dụng phương thức vận chuyển giao thức TCP ví dụ như Http, Smtp, Ftp, Telnet).

### 6.2) `Broadcast`:

- Broadcasr là thuật ngữ được sử dụng để mô tả cách thức truyền tin được gửi từ 1 điểm đến tất cả các điểm khác. Trong trường hợp này, có 1 nguồn gửi nhưng thông tin được gửi đến tất cả các nguồn nhận trong cùng 1 kết nối.

- Broadcast được hỗ trợ trong hầu hết các mạng LAN (VD: Ethernet), được sử dụng để gửi cùng 1 thông điệp cho tất cả các máy tính trong mạng LAN (ví dụ như bản tin ARP: giao thức phân giải địa chỉ, truy vấn địa chỉ của tất cả các máy tính trong cùng 1 mạng LAN).
- Giao thức lớp mạng (Ipv4) cũng hỗ trợ kiểu truyền Broadcast, cho phép các gói tin được gửi đến mọi thiết bị trong cùng 1 mạng.

### 6.3) `Multicast`:

- Multicast là thuật ngữ được sử dụng để mô tả cách thức truyền tin được gửi từ 1 hoặc nhiều điểm đến 1 tập hợp các điểm khác.

- Trong trường hợp này có thể là 1 hoặc nhiều người gửi, và thông tin được phân phối cho 1 tập hợp các điểm thu.Multicast hữu ích nếu 1 nhóm khách hàng yêu cầu 1 bộ dữ liệu chung cùng 1 lúc.

- Việc truyền Multicast sẽ có thể tiết kiệm băng thông 1 cách đáng kể.

### 6.4) `Anycast`:

- Anycast là một phương thức định tuyến mạng đến nhiều vị trí hoặc nút mạng khác nhau.

- Anycast được đặc trưng bởi 1 đến nhiều liên kết.

- Anycast luôn sẵn có 1 bản sao lưu trong trường hợp một nút bị quá tải hoặc truy cập thất bại.

## Ip tĩnh, động:
### 7.1) `Địa chỉ Ip tĩnh `:

- Địa chỉ ip tĩnh có thể hình dung là một địa chỉ IP cố định dành riêng cho một người, nhóm người sử dụng.

- Lúc này thiết bị kết nối đến internet của họ luôn luôn được đặt một địa chỉ IP.

    > Một số ISP sẽ yêu cầu khách hàng khai báo (hoặc cam kết) về mục đích của việc sử dụng IP tĩnh để quản lý khi cung cấp dịch vụ IP tĩnh cho khách hàng (nhằm tránh tạo ra các máy chủ cung cấp dịch vụ mà không đăng ký hoặc không được phép theo quy định riêng của từng quốc gia).

- Địa chỉ ip tĩnh sẽ được cung cấp cho một máy chủ với mục đích riêng, có thể là máy chủ web, mail… Từ đó cho phép nhiều người dùng có thể truy cập mà không bị gián đoạn quá trình.

### 7.2) `Địa chỉ ip động` :

- Trong trường hợp không sử dụng các dịch vụ đặc biệt cần sử dụng Ip tĩnh các nhà cung cấp ISP sẽ gán IP khác nhau cho mỗi lần kết nối, hoặc trong một phiên kết nối, đây được gọi là Ip động.

- Khi máy tính ngừng kết nối vào mạng Internet thì nhà cung cấp sẽ sử dụng Ip cho một người khác sử dụng, hành động này nhằm tiết kiệm nguồn địa chỉ Ip đang dần cạn kiện.

