# Lệnh Linux cơ bản #1: pwd

Sử dụng lệnh pwd để tìm ra đường dẫn của thư mục (folder) làm việc hiện tại mà bạn đang đứng.


Lệnh này sẽ trả về một đường dẫn tuyệt đối (đầy đủ), về cơ bản là đường dẫn của tất cả các thư mục bắt đầu bằng dấu gạch chéo lên (/).

Ví dụ về đường dẫn tuyệt đối là /home/haianh/Desktop

![image](https://user-images.githubusercontent.com/101684058/158772597-b9b4703d-981a-4520-b3e0-d70f51f90721.png)

# Lệnh tạo mới thư mục: mkdir
Ví dụ, nếu muốn tạo một thư mục mới có tên là tesst sử dụng lệnh: mkdir tesst

![image](https://user-images.githubusercontent.com/101684058/158776672-0a19088d-c8ff-4e14-9078-8a84ab1d76ed.png)

Để tạo nhiều thư mục cùng lúc ta dùng lệnh: mkdir test1 test2

![image](https://user-images.githubusercontent.com/101684058/158776968-3a0879b2-1605-4d28-841d-32053707b300.png)

# Lệnh tạo một file mới: touch
Sử dụng lệnh touch để tạo một file trống. 
Ví dụ: Tạo file có tên filename.txt sử dụng lệnh: touch filename.txt

![image](https://user-images.githubusercontent.com/101684058/158777856-46380f34-9905-4895-be1c-5c898edf563a.png)

Ngoài ra bạn có thể chỉ định nhiều tên file để tạo nhiều file cùng một lúc sử dụng lệnh: touch file1.txt file2.html

# Lệnh di chuyển các file: mv
Dùng lệnh mv để di chuyển file cụ thể vào thư mục. 
Ví dụ: di chuyển file filename.txt vào test1 sử dụng lệnh: mv filename.txt test1

![image](https://user-images.githubusercontent.com/101684058/158779770-2e5f3a03-3a97-4a01-bca5-7069a1795bdf.png)

Ngoài ra bạn còn có thể sử dụng lệnh mv để thay đổi tên file và thư mục. Chẳng hạn nếu muốn đổi tên tesst thành test3 sử dụng lệnh: mv test test3

![image](https://user-images.githubusercontent.com/101684058/158780297-1ac25989-b132-4dce-a4da-4a89b4ca8297.png)

# Lệnh sao chép: cp
Nhập lệnh cp hoặc copy nếu bạn muốn sao chép một file hay một thư mục.
Ví dụ muốn sao chép file filename.txt ở trong thư mục test1 cho file mới là filenew ta sử dụng lệnh: cp test1/filename.txt filenew.txt 

![image](https://user-images.githubusercontent.com/101684058/158781463-846f5195-5465-4159-ac13-4075ee77d14f.png)

# Lệnh xem nội dung của thư mục: ls
Xem nội dung thư mục làm việc hiện tại của bạn,sử dụng lệnh: ls

![image](https://user-images.githubusercontent.com/101684058/158783887-6bd3d351-1788-4075-9a67-9a954d2f33d0.png)

Có các biến thể bạn có thể sử dụng với lệnh ls:

 
ls -R cũng sẽ liệt kê tất cả các tệp trong các thư mục con
ls -a sẽ hiển thị các tệp ẩn
ls -al sẽ liệt kê các tệp và thư mục với thông tin chi tiết như quyền, kích thước, chủ sở hữu, v.v.

![image](https://user-images.githubusercontent.com/101684058/158785414-ae782215-1171-4050-bc9f-7c883441b4ce.png)



