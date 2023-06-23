# Tình huống 6: Tình huống điều tra tấn công chuyển hướng website

Cấp độ: Chuyên viên

> Được đóng góp bởi: [Công ty Cổ phần BKAV](https://www.bkav.com.vn/)

## Tổng quan

Hệ thống giám sát IDS ghi nhận có 1 lượng lớn nỗ lực tấn công vào website trangchu.habinh.gov. Sau khi ghi nhận thông báo từ SOC, quản trị viên thực hiện bật Wireshark và bắt các gói tin, lưu lượng truy cập trong mạng.

Tuy nhiên do năng lực hạn chế đội ngũ quản trị đã không thể phát hiện sâu hơn các hành vi của kẻ tấn công. Một khoảng thời gian sau đó, quản trị viên nhận được thông báo từ người dùng rằng website chuyển thành trang cờ bạc online. 

Quản trị viên sau đó đã thực hiện stop dịch vụ, ngắt kết nối mạng và chuyển mã nguồn sang 1 server khác. Sau khi chuyển thì không còn ghi nhận hiện tượng trên. 

Quản trị viên sau đó cũng thực hiện nén các thư mục quan trọng liên quan đến website và file lưu lượng mạng ghi nhận được cho đội điều tra. 

Bạn, với vai trò là chuyên viên điều tra, ứng cứu sự cố, hãy giúp đơn vị điều tra sự cố này.

## Mô tả hiện trường

<div style="width:100%;height:0px;position:relative;padding-bottom:54.147%;"><iframe src="https://streamable.com/e/q8elc5?autoplay=1" frameborder="0" width="100%" height="100%" allowfullscreen allow="autoplay" style="width:100%;height:100%;position:absolute;left:0px;top:0px;overflow:hidden;"></iframe></div>

## Câu hỏi

1.  Điều gì khiến hệ thống bị thay đổi giao diện thành trang cờ bạc online?
2.  URL của Website cờ bạc online này là gì?
3.  Kẻ tấn công đã khai thác lỗ hổng có định danh nào vào server? (Format: CVE-XXXX-XXXXX)
4.  Thư mục mà Kẻ tấn công đã tải những file độc hại lên server?
5.  File đầu tiền giúp Kẻ tấn công dành quyền truy cập lần đầu vào hệ thống?
6.  Tên của file gây ra hiện tượng này thay đổi giao diện này?
7.  Kẻ tấn công đã đạt được quyền SYSTEM hay chưa?


## Tệp đính kèm

1. [Tệp image (part 1)](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge6/DFLab-challenge6-image.ad1)
2. [Tệp image (part 2)](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge6/DFLab-challenge6-image.ad2)
3. [Tệp image (part 3)](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge6/DFLab-challenge6-image.ad3)
4. [Tệp image (part 4)](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge6/DFLab-challenge6-image.ad4)
5. [Tệp image (part 5)](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge6/DFLab-challenge6-image.ad5)
6. [Tệp image (part 6)](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge6/DFLab-challenge6-image.ad6)
7. [Tệp image (part 7)](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge6/DFLab-challenge6-image.ad7)
8. [Tệp image (part 8)](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge6/DFLab-challenge6-image.ad8)
9. [Tệp pcap](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge6/DFLab-challenge6-network.pcapng)