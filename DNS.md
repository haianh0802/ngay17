# 1. DNS là gì?
DNS là viết tắt của từ Domain Name System (tạm dịch: Hệ thống phân giải tên miền), là một hệ thống cho phép thiết lập tương ứng giữa địa chỉ IP và tên miền trên Internet.
# 2. Chức năng của DNS
Mỗi website có một tên miền (đường dẫn URL: Uniform Resource Locator) và một địa chỉ IP. Địa chỉ IP gồm 4 nhóm số cách nhau bằng dấu chấm (IPv4).

Khi bạn nhập tên website bạn muốn tìm vào thanh trình duyệt, trình duyệt sẽ đến thẳng website mà bạn không cần phải thông qua việc nhập địa chỉ IP của trang web. Quá trình “dịch” tên miền thành địa chỉ IP để cho trình duyệt hiểu và truy cập được vào website là công việc của một DNS server.  Một DNS không thể “dịch” thành công mà các DNS sẽ trao đổi thông tin, trợ giúp qua lại với nhau để dịch tên miền thành địa chỉ IP và ngược lại. Nhờ DNS, người dùng chỉ cần nhớ tên miền, không cần phải nhớ địa chỉ IP.

Hiểu một cách đơn giản, domain (tên miền) là địa chỉ website của doanh nghiệp bạn. Nếu domain là địa chỉ nhà thì hosting chính là ngôi nhà mà địa chỉ đó dẫn tới. Tất cả các website trên Internet đều cần 1 web hosting. Khi khách hàng nhập tên miền của bạn vào trình duyệt, tên miền sẽ lập tức được chuyển đổi thành địa chỉ IP máy tính của công ty lưu trữ website của bạn. DNS chính là công cụ chuyển đổi tuyệt vời này.
# 3. Nguyên tắc hoạt động của DNS
Mỗi nhà cung cấp dịch vụ vận hành và duy trì DNS server riêng của mình, gồm các máy bên trong phần riêng của mỗi nhà cung cấp dịch vụ đó trong Internet. Tức là, nếu một trình duyệt tìm kiếm địa chỉ của một website thì DNS server phân giải tên website này phải là DNS server của chính tổ chức quản lý website đó chứ không phải là của một tổ chức (nhà cung cấp dịch vụ) nào khác.
INTERNIC (Internet Network Information Center) chịu trách nhiệm theo dõi các tên miền và các DNS server tương ứng. INTERNIC là một tổ chức được thành lập bởi NSF (National Science Foundation), AT&T và Network Solution, chịu trách nhiệm đăng ký các tên miền của Internet. INTERNIC chỉ có nhiệm vụ quản lý tất cả các DNS server trên Internet chứ không có nhiệm vụ phân giải tên cho từng địa chỉ.
DNS có khả năng truy vấn các DNS server khác để có được một cái tên đã được phân giải. DNS server của mỗi tên miền thường có hai việc khác biệt. Thứ nhất, chịu trách nhiệm phân giải tên từ các máy bên trong miền về các địa chỉ Internet, cả bên trong lẫn bên ngoài miền nó quản lý. Thứ hai, chúng trả lời các DNS server bên ngoài đang cố gắng phân giải những cái tên bên trong miền nó quản lý.
DNS server có khả năng ghi nhớ lại những tên vừa phân giải. Để dùng cho những yêu cầu phân giải lần sau. Số lượng những tên phân giải được lưu lại tùy thuộc vào quy mô của từng DNS.
# 4. Các loại DNS Server và tên miền
Trên thực tế, có đến tổng cộng khoảng 4 server tham gia vào trong hệ thống phân giải tên miền, bao gồm:

#### Root Name Servers
Cũng thường được gọi là Name Server. Đây là Server quan trọng nhất trong hệ thống cấp bậc của DNS. Bạn cũng có thể hiểu rằng, Root Name Server chính là một thư viện để định hướng tìm kiếm giúp bạn.

Theo quy trình thực tế, sau khi nhận yêu cầu từ DNS Recursive Resolver, Root Name Server sẽ phản hồi rằng nó cần tìm trong các top-level domain name servers ( TLD Name Servers ) cụ thể nào.

#### DNS Recursor
Như đã nhắc đến ở trên, “cạ cứng” này đóng vai trò như một nhân viên cần mẫn, nhận nhiệm vụ lấy và trả thông tin về cho trình duyệt để tìm đúng thông tin mà chúng cần. Nói cách khác, DNS Recursor giữ trách nhiệm liên lạc với các Server khác để phản hồi đến trình duyệt người dùng. Tất nhiên là trong quá trình lấy thông tin, đôi khi nó cũng sẽ cần đến sự giúp đỡ của Root DNS Server.

#### TLD Nameserver
Khi bạn muốn truy cập Google hay Facebook, thường, phần mở rộng của bạn sẽ là “.com” đúng không? Vậy tôi muốn bạn biết rằng, nó chính là một trong các Top-level Domain đấy. Và Server cho loại Top-level domain này gọi là TLD Nameserver. Đây là nhà quản lý toàn bộ hệ thống thông tin của một phần mở rộng tên miền chung.

Theo trình tự, TLD Name Server sẽ phản hồi từ DNS Resolver, sau đó giới thiệu nó cho một Authoritative DNS Server – hay nơi chứa chính thức nguồn dữ liệu của tên miền đó.

#### Authoritative Nameserver
Khi DNS Resolver tìm thấy Authoritative Nameserver, đó là lúc mà việc phân giải tên miền diễn ra.
Mặt khác, Authoritative Name Server có chứa thông tin cho biết tên miền đang gắn với địa chỉ nào. Nó sẽ cung cấp cho Recursive Resolver địa chỉ IP cần thiết tìm thấy trong danh mục những bản ghi của nó.
# 5. Các loại bản ghi DNS
#### A Record
Là DNS Record đơn giản nhất, được sử dụng nhiều nhất để trỏ tên Website tới một địa chỉ IP cụ thể.
Bạn có thể thêm một tên mới, thêm Time to Live ( thời gian tự động tái lại bản ghi ) và Points to ( Trỏ tới IP nào ).
#### CNAME Record
Là bản ghi đóng vai trò như đặt một hoặc nhiều tên khác cho tên miền chính
Bạn có thể tạo một tên mới, điều chỉnh trỏ tới tên gốc là gì và đặt TTL
#### MX Record
Là bản ghi chỉ định Server nào quản lý các dịch vụ Email của tên miền đó
Bạn có thể trỏ tên miền đến Mail Server, Đặt mức độ ưu tiên ( Priority ), đặt TTL
#### TXT Record
Là bản ghi giúp bạn chứa các thông tin định dạng văn bản của tên miền
Bạn có thể thêm host mới, giá trị TXT, TTL, Points to.
#### AAAA Record
Cùng là A Record, tuy nhiên, AAA Record được sử dụng để trỏ domain đến 1 địa chỉ IPV6 Address
Bạn có thể thêm host mới, IPv6, TTL
#### NS Record
Là DNS Server Records của tên miền, cho phép bạn chỉ định Name Server cho từng tên miền phụ
Bạn có thể tạo host mới, tên Name Server, TTL
#### SRV Record
Là bản ghi đặc biệt trong Domain Name System, dùng để xác định chính xác dịch vụ nào chạy port nào
Bạn có thể thêm Priority, Name, Port, Points to,Weight, TTL.
![image](https://user-images.githubusercontent.com/101684058/158720122-e2c7e187-b967-4eab-bc36-30d17580c220.png)
# 6.Các bước thay đổi DNS trong máy tính
1: Chọn Start – Setting – Network Connection
2: Double click vào Local Area Connection, chọn Properties – Internet Protocol (TCP/IP) – Properties
3: Điền thông số DNS Server bạn muốn vào 2 ô “Preferred DNS Server” & “Alternate DNS Server”.
# 7. Tại sao DNS dễ bị tấn công
Quay lại phần Sử dụng DNS như thế nào, bạn có thấy một cảnh báo nhỏ của tôi về độ “mong manh, dễ vỡ” và dễ bị tấn côngkhông? Để tôi lý giải giúp bạn tại sao nhé!

Quá trình tên miền được dịch thành địa chỉ IP, được gọi là phân giải DNS.

Khi ai đó nhập một tên miền nào đó, chẳng hạn www.google.com vào Web Browser, thì trình duyệt lập tức liên hệ với 1 máy chủ tên, để lấy địa chỉ IP tương ứng. Có 2 loại máy chủ tên:

Máy chủ tên có thẩm quyền: Nơi lưu trữ thông tin đầy đủ về một vùng
Máy chủ tên đệ quy: Nơi trả lời các truy vấn DNS cho người dùng Internet, đồng thời lưu trữ kết quả phản hồi của DNS trong một khoảng thời gian.
Vậy thì vấn đề mà chúng ta đang muốn nhấn mạnh, nằm ở bộ máy chủ tên đệ quy.

Khi một máy chủ đệ quy nhận được phản hồi, nó sẽ lưu vào bộ nhớ tạm phản hồi đó, để tăng tốc độ của các truy vấn tiếp theo. Ưu điểm của việc lưu trữ là sẽ giảm số lượng yêu cầu thông tin cần thiết, nhưng đồng thời cũng phát sinh một rủi ro “đáng gờm” là dễ bị tấn công bởi man-in-the-middle, tạm dịch là người trung gian.

Thông quan các màn battle “ngoài sáng trong tối” này, tội phạm mạng sẽ có thể:

Cướp Email
Can thiệp Voice Over IP ( VoIP )
Mạo danh các trang web
Đánh cắp thông tin đăng nhập và mật khẩu
Trích xuất dữ liệu thẻ tín dụng và một số thông tin mật khác
![image](https://user-images.githubusercontent.com/101684058/158720419-2ec3e8e8-ac00-4f0e-845f-77bf5c1a1304.png)
# Một số nhà cung cấp tại Việt Nam và quốc tế
### iNET
iNET sở hữu hệ thống máy chủ tên miền hiện đại, luôn được cập nhật mới nhất, hệ quản trị tên miền của iNET sử dụng công nghệ Ajax cho tốc độ xử lý nhanh, chính xác, mang lại trải nghiệm tuyệt vời cho người dùng. Tên miền được bảo vệ và bảo mật bởi công nghệ DNSSEC, Registry lock, iNET hỗ trợ ẩn thông tin tên miền miễn phí, đăng ký được nhiều đuôi tên miền mới, mở rộng.

iNET được nhiều khách hàng trên khắp cả nước tin tưởng lựa chọn, đánh giá cao, đặc biệt là các doanh nghiệp, tổ chức.

### GoDaddy
Nói đến tên miền thì GoDaddy đã quá nổi tiếng, bởi đây là nhà cung cấp dịch vụ tên miền quốc tế lớn nhất trên thế giới. GoDaddy được thành lập từ năm 1997, tính đến hiện tại công ty đã phục vụ 20 triệu khách hàng và chịu trách nhiệm hơn 80 triệu domain.

Thời gian cập nhật DNS nhanh, miễn phí chuyển đổi tên miền trong nội bộ GoDaddy là những ưu điểm nổi bật nhất của Go Daddy.

Nhược điểm của Go Daddy so với các nhà cung cấp tên miền trong danh sách này là chi phí cao, nhưng đổi lại khách hàng sẽ có chế độ bảo hành và chất lượng dịch vụ hàng đầu.

### PA Việt Nam
Nhắc đến nhà cung cấp tên miền, dịch vụ hosting lớn và lâu đời ở Việt Nam thì không thể bỏ qua PA Việt Nam. Với bề dày kinh nghiệm và mức độ uy tín, PA Việt Nam thường được khách hàng nhắc đến khi tìm nhà cung cấp tên miền.

Khách hàng có thể đăng ký và kích hoạt tên miền tự động, nhanh chóng và dễ dàng, quản lý và cập nhật DNS nhanh. Hệ thống của PA Việt Nam hỗ trợ IPv6, DNSSEC, Whois Protect, Registry Lock đảm bảo sự vận hành, sao lưu và bảo mật cao nhất. Đội ngũ nhân viên được đào tạo theo tiêu chuẩn quốc tế, cơ sở hạ tầng riêng, kho thiết bị dự phòng lớn, cấu hình mạnh mẽ.

### Tenten.vn
Khi nhắc đến tên miền giá rẻ chắc chắn không thể nhắc tới Tenten.vn. TENTEN. VN thuộc đơn vị chủ quản là công ty GMO RUNSYSTEM, thuộc tập đoàn GMO Internet (Nhật Bản) là nhà đăng ký tên miền Việt Nam của VNNIC và đại lý tên miền quốc tế Onamae.com (Nhật Bản) TENTEN.VN ra mắt vào tháng 4/2012.

Tham gia vào thị trường tên miền muộn hơn so với các đối thủ, nhưng Tenten đã khẳng định được vị trí của mình khi thuộc top 3 nhà cung cấp chiếm thị phần tên miền lớn nhất Việt Nam với mức giá rẻ nhất trên thị trường, chất lượng Nhật Bản được đầu tư và thừa hưởng từ công ty mẹ là Onamae.com hiện đang chiếm vị trí độc tôn trong lĩnh vực tên miền - hosting tại Nhật Bản với thị phần lên tới 80%.

Ngoài ra Tenten thường xuyên cập nhật các mã giảm giá tên miền hấp dẫn cho khách hàng mới, các chương trình ưu đãi hấp dẫn tri ân khách hàng cũ.

### Google Public DNS Server
Google Public DNS Server là một trong những DNS Server nhanh nhất và được nhiều người dùng sử dụng nhất. Sử dụng DNS server của Google giúp bạn trải nghiệm duyệt Web tốt hơn và độ bảo mật cũng cao hơn.

Preferred DNS server: 8.8.8.8

Alternate DNS server: 8.8.4.4

### OpenDNS
OpenDNS là một DNS Server nhanh nhất dựa trên đám mây. Open DNS sẽ bảo vệ tối đa máy tính của bạn từ các cuộc tấn công độc hại bởi những kẻ tấn công trên mạng Internet.

OpenDNS là một trong những máy chủ DNS công cộng tốt nhất và không có thời gian chết. OpenDNS cũng cung cấp 2 giải pháp miễn phí cho người dùng tùy chỉnh: OpenDNS Family Shield và OpenDNS Home.

OpenDNS Family Shield được cấu hình sẵn để chặn nội dung người lớn. Để sử dụng OpenDNS Family Shield , chúng ta cấu hình cài đặt hệ thống mạng bằng địa chỉ IP dưới đây:

Preferred DNS server: 208.67.222.123

Alternate DNS server: 208.67.220.123

OpenDNS Home đi kèm với bộ lọc tùy chỉnh, bảo vệ máy tính của bạn khỏi hacker và phishing.

### Domain name (tên miền) là gì?
Tên miền là địa chỉ trang web, là thứ mà mọi người gõ vào thanh URL của trình duyệt để truy cập website.

Nói một cách dễ hiểu hơn thì máy tính sử dụng địa chỉ IP (66.249.66.2), là một dãy số. Tuy nhiên, rất khó để con người nhớ các chuỗi số. Do đó, tên miền được phát triển và được sử dụng để xác định các thực thể trên Internet thay vì sử dụng địa chỉ IP.

Tên miền có thể là bất kỳ sự kết hợp nào của các chữ cái và số, đồng thời nó có thể được sử dụng kết hợp với các phần mở rộng tên miền khác nhau, chẳng hạn như .com, .net và hơn thế nữa.

Tên miền phải được đăng ký trước khi chúng ta có thể sử dụng nó. Mỗi tên miền là duy nhất. Không có hai trang web có thể có cùng một tên miền

Subdomain:là phần mở rộng của một tên miền. Subdomain có thể được tạo hoàn toàn miễn phí và nó có thể hoạt động như một tên miền thực thụ



