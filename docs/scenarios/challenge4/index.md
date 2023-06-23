# Tình huống 4: Tấn công chiếm quyền trong môi trường domain

Cấp độ: Chuyên viên

## Tổng quan

Quản trị viên hệ thống ghi nhận có những dấu hiệu truy cập bất thường vào Domain Controller với đặc quyền cao nhưng chưa rõ nguyên nhân. Đơn vị phản ứng tại chỗ đã nhanh chóng tiếp cận hiện trường và thu thập những dữ liệu cần thiết phục vụ cho quá trình điều tra. 

Hãy vào vai nhà phân tích sự cố và tìm hiểu xem kẻ tấn công đã truy cập được vào hệ thống thông qua những con đường nào, và nhiệm vụ của bạn là tìm bằng chứng hoặc dấu hiệu của các IoC. 

Vì vậy, câu hỏi tiếp theo sẽ là bạn nên tìm kiếm những chỉ số nào để phát hiện cuộc tấn công?

## Câu hỏi

1.  Kẻ tấn công đã tấn công vào hệ thống Domain Controller thông qua con đường gì?
2.	Phân tích, tìm kiếm những tiến trình có liên quan đến cuộc tấn công?
3.	Xác định dịch vụ bị lạm dụng để tiến hành tấn công RCE vào Domain Controller?
4.	Xác định hostname và local domain bị tấn công ?
5.	Kẻ tấn công đã sử dụng giao thức gì để phát tán mã thực thi vào hệ thống?
6.	Sự kiện FileCreated đã được tạo và ghi lại. Cung cấp đường dẫn đầy đủ đến tệp đọc hại và thời gian tạo file thực thi đó?
7.	Kẻ tấn công đã thực hiện những lệnh khai thác với đặc quyền gì trong hệ thống? Cố gắng thu thập thông tin, bằng chứng những lệnh mà kẻ tấn công đã thực thi?
8.	Tìm kiếm địa chỉ IP của máy bị lạm dụng để tấn công vào Domain Controller?
9.	Bạn có xác định được tên lỗ hổng mà kẻ tấn công đã lạm dụng để thực hiện cuộc tấn công này hay không?
10.	Đưa ra các biện pháp khắc phục sự cố.

## Tệp đính kèm

1. [Tệp logfile giám sát](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge4/DFLab-challenge4-Logfile.PML)
2. [Tệp pcap giám sát](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge4/DFLab-challenge4-network.pcapng)
3. [Tệp Sysmon log](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge4/DFLab-challenge4-Sysmon-log.evtx)
4. [Tệp System log](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge4/DFLab-challenge4-System-log.evtx)
5. [Tệp System Idle Process](https://github.com/VNCERT-CC/digital-forensics-lab/releases/download/challenge4/DFLab-challenge4-SystemIdleProcess.txt)