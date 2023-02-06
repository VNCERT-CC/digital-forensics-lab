<details open>
  <summary>Giới thiệu chung</summary>

DFLab xây dựng một chuỗi kịch bản tấn công sát với thực tế và đưa ra các mẫu bằng chứng, tệp nhật ký,... cho các chuyên gia ứng cứu, điều tra, phân tích sự cố giả định.

Sự cố được giả định tại một Công ty có tên DFCorp có trụ sở tại Việt Nam. Công ty có tên miền dfcorp.com và sử dụng các máy chủ, được thiết kế và lắp đặt, kết nối theo sơ đồ sau:

![DFCorp Network](dfcorp-net.png)

Danh sách các dải mạng:
  * DMZ: 10.0.9.0/24
  * WZ: 10.0.8.0/24
  * USERLAN: 10.0.10.0/24

Danh sách các thiết bị tham gia hệ thống mạng:
  * Máy chủ ADDS (WZ): 10.0.8.2 cài đặt Windows Server 2019
  * Máy chủ Database (WZ): 10.0.8.5 cài đặt 
  * Máy chủ MS Exchange (DMZ): 10.0.9.3 cài đặt Window Server 2019 và MS Exchange 2019
  * Máy chủ IIS (DMZ): 10.0.9.4 cài đặt Windows Server 2019
  * Máy chủ Firewall: 10.10.2.136 cài đặt pfSense
  * Các nhân viên tham gia với dải mạng USERLAN
  * Máy chủ IDS tham gia dải mạng USERLAN

Các máy chủ MS Exchange và IIS được NAT ra ngoài mạng internet và được proxy thông qua haproxy đã được bật header x-forwarded-for.
</details>

<details open>
  <summary>Tình huống 1: Tấn công đào tiền ảo</summary>

Qua hệ thống giám sát IDS, đội ngũ quản trị, vận hành hệ thống phát hiện một cuộc tấn công tới hệ thống mạng, máy chủ của DFCorp.
Quản trị viên nhanh chóng thực hiện các công việc sau:

1. Tiếp tục kiểm tra, theo dõi cuộc tấn công
2. Bật tcpdump và bắt các gói tin, lưu lượng truy cập trong mạng

Tuy nhiên, do năng lực hạn chế, đội ngũ quản trị đã không thể phát hiện sâu hơn các hành vi của kẻ tấn công.
Vài ngày sau đó, đội ngũ quản trị nhận được báo cáo từ người dùng rằng máy tính của họ cặp trục trặc, hay bị đơ, không làm việc được.
Cùng thời gian đó, máy chủ Email của hệ thống hoạt động chập chờn, CPU luôn ở mức 99%.

Bạn, với vai trò là chuyên viên điều tra, ứng cứu sự cố, hãy giúp công ty DFCorp điều tra sự cố này.

<details open>
<summary>Câu hỏi</summary>

1. Đây có phải là một cuộc tấn công nhắm vào DFCorp hay không?
2. Đây là loại tấn công gì?
3. Địa chỉ IP của kẻ tấn công là gì?
</details>

<details open>
<summary>Tệp đính kèm</summary>

1. [Tệp pcap lưu trữ các gói tin qua hệ thống](/challenge-1-pcap.zip)
</details>


</details>

