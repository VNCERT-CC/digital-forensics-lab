<details open>
  <summary>Giới thiệu chung</summary>

DFLab xây dựng một chuỗi kịch bản tấn công sát với thực tế và đưa ra các mẫu bằng chứng, tệp nhật ký,... cho các chuyên gia ứng cứu, điều tra, phân tích sự cố giả định.

Sự cố được giả định tại một Công ty có tên DFCorp có trụ sở tại Việt Nam. Công ty có tên miền dfcorp.com và sử dụng các máy chủ, được thiết kế và lắp đặt, kết nối theo sơ đồ sau:

![DFCorp Network](images/dfcorp-net.png)

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

Hình ảnh Máy chủ Email:
![EXCH Screenshot](challenge1/exchange-screenshot.png)

Hình ảnh Máy chủ ADDS:
![DC Screenshot](challenge1/dc-screenshot.png)

Hình ảnh do người dùng cung cấp:
![User Screenshot](challenge1/user-screenshot.png)

<details open>
<summary>Câu hỏi</summary>

1. Kẻ tấn công đã sử dụng công cụ gì để rà quét hệ thống của DFCorp? IP của kẻ tấn công sử dụng để rà quét là gì?
2. Kẻ tấn công có phát hiện được lỗ hổng gì trong đợt rà quét đó không? Nếu có hãy chỉ ra lỗ hổng.
3. Kẻ tấn công đã tấn công qua email nào của hệ thống? Có thành công hay không?
4. Kẻ tấn công có lấy được dữ liệu quan trọng nào của DFCorp không?
5. Đường dẫn kẻ tấn công thực hiện để khai thác lỗ hổng và sử dụng shell? Kẻ tấn công có sử dụng shell thành công hay không?
6. CnC server của kẻ tấn công là gì?
7. Quá trình mà kẻ tấn công thực hiện gây ra hậu quả như các hình ảnh trên.
</details>

<details open>
<summary>Tệp đính kèm</summary>

1. [Tệp pcap khi phát hiện dấu hiệu tấn công (part 1)](https://github.com/VNCERT-CC/digital-forensics-lab-frontend/releases/download/challenge1/DFLab-challenge1-network1.zip.001)
2. [Tệp pcap khi phát hiện dấu hiệu tấn công (part 2)](https://github.com/VNCERT-CC/digital-forensics-lab-frontend/releases/download/challenge1/DFLab-challenge1-network1.zip.002)
3. [Tệp pcap (tiếp)](https://github.com/VNCERT-CC/digital-forensics-lab-frontend/releases/download/challenge1/DFLab-challenge1-network2.pcap.gz)
4. [Tệp logs ADDS](https://github.com/VNCERT-CC/digital-forensics-lab-frontend/releases/download/challenge1/DFLab-challenge1-Logs-ADDS.zip)
5. [Tệp logs User](https://github.com/VNCERT-CC/digital-forensics-lab-frontend/releases/download/challenge1/DFLab-challenge1-Logs-User.zip)
6. [Tệp logs Exchange](https://github.com/VNCERT-CC/digital-forensics-lab-frontend/releases/download/challenge1/DFLab-challenge1-Logs-EXCH01.zip)
</details>


</details>
