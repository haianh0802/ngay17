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

# Lệnh xóa một thư mục: rmdir 
Ví dụ: Xóa thư mục có tên thu, ta dùng lệnh: rmdir thu

![image](https://user-images.githubusercontent.com/101684058/158918736-41031bd3-e014-4ffc-bd4e-681716e10027.png)

# Lệnh xóa file: rm
Ví dụ: Để xóa file tên file.txt ta dùng lệnh: rm file.txt


![image](https://user-images.githubusercontent.com/101684058/158919168-4801a7ee-8239-4918-b6e0-9e9b0c367fb9.png)

Ngoài ra để xóa thư mục và toàn bộ dữ liệu trong thư mục đó ta dùng lệnh: rm -r 

![image](https://user-images.githubusercontent.com/101684058/158919893-24efce08-13b2-4e07-958b-788b41f6cda8.png)

# Lệnh đọc và in ra nội dung của file trên màn hình: cat

Ví dụ: In ra nội dung file có tên filenew.txt ta dùng lệnh: cat filenew.txt

![image](https://user-images.githubusercontent.com/101684058/158920189-9dd36d94-071d-4ec4-b6bc-569a504c45f7.png)

# Đọc và in ra N dòng cuối cùng: tail
Để in ra 5 dòng cuối cùng của file filenew.txt ta dùng lệnh: tail -n 5 filenew.txt 
![image](https://user-images.githubusercontent.com/101684058/158921236-493a882e-8725-47da-99a6-ccef7cd00081.png)

# Đọc và in ra N dòng đầu tiên: head

Đọc in ra 5 dòng đầu tiên của file filenew.txt ta dùng lệnh: head -n 5 filenew.txt

![image](https://user-images.githubusercontent.com/101684058/158921536-65243a31-3d48-46a5-b51a-8f1822ccc379.png)

# Lệnh tar
 tar -cvf    tạo file nén (.tar) từ các file có sẵn. 
 
  ![image](https://user-images.githubusercontent.com/101684058/158923883-fa1cf42d-572c-4b41-8ffd-06913c19b06e.png)

 tar -tvf   xem nội dung file nén (.tar).  
 
 ![image](https://user-images.githubusercontent.com/101684058/158923998-052c4a3d-d102-4cbe-ac13-432d6a2c4e28.png)


 tar -xvf   giải nén (file .tar).
 
 ![image](https://user-images.githubusercontent.com/101684058/158924083-7974e1ab-e884-4aa2-a1be-211a18f9af45.png)


 






