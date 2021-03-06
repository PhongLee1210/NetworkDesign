## Quân Y 87 Hospital
### Step 1. Gather Information
__Yêu cầu__: Bệnh viện Quân y 87 được xây dựng với quy mô của Bệnh viện hạng I tầm cỡ khu vực, có 350 giường, tổng diện tích sàn 34.000m2, có 7 hạng mục công trình chính trong đó có 2 khối nhà (cao 10 tầng) điều trị của các khoa. Bệnh viện được đầu tư các trang thiết bị y tế hiện đại.Hệ thống mạng yêu cầu hỗ trợ được trên 500 bệnh nhân, và trên 100 nhân viên trong bệnh viên. <br />
Vì cơ sở hạ tầng CNTT còn thực hiện hỗ trợ hoạt động quân sự, tập trận , bảo đảm duy trì thông tin liên lạc cho nhân viên với mức độ ưu tiên cao về bảo mật và quyền riêng tư thông tin khách hàng. <br />

__Giả định__: <br />
•	Mỗi máy trạm sẽ chỉ có một giao diện Ethernet. <br />
•	Tất cả các giao diện sẽ được nối cáp cho Ethernet 1 Gbps. <br />
•	Mạng không cần hỗ trợ 1 Gbps cho tất cả người dùng cùng một lúc. <br />
•	Mỗi người dùng sẽ có một điện thoại hỗ trợ không dây. <br />
•	Tất cả các điện thoại sẽ không phải là điện thoại IP. <br />
•	VoIP sẽ không được chạy trên mạng trong tương lai gần. <br />
•	Mỗi người dùng sẽ bằng một khối lập phương hoặc văn phòng. <br />
•	Mỗi khối lập phương hoặc văn phòng sẽ có bốn giắc cắm dữ liệu. <br />
•	Mỗi tầng sẽ có 3 AccessPoints và 3 Camera. <br />
•	Tất cả các hoạt động của hệ thống cáp sẽ kết thúc vào phòng IT/Core. <br />
•	Số lượng bệnh nhân và nhân viên tăng thêm 5% mỗi năm. <br />

### Step 2. Prepare
Table 1.1: **Business Constraint** <br />
![image](https://user-images.githubusercontent.com/81057831/132111256-791fa88f-5143-4410-862a-943e4c14a0cf.png) <br />
Table 1.2: **Business Application** <br />
![image](https://user-images.githubusercontent.com/81057831/132111321-cda23130-4e9c-4afe-917a-821badccc4fa.png) <br />
**Technical Constraint** <br />
Ràng buộc: <br />
•	Hệ thống xác thực. <br />
•	Giải pháp remote bên ngoài. <br />
•	Giới hạn băng thông không dây. <br />
•	Phát hiện hoặc ngăn chặn xâm nhập đối với các hệ thống chứa dữ liệu khách hàng. <br />
Rủi ro: Ngoài ra, cần có cơ chế sao lưu để thực hiện sao lưu dữ liệu định kỳ để đối phó với bất kỳ tình huống không mong muốn nào: lỗi hệ thống, tấn công của kẻ xâm nhập, phát tán mã độc,… <br />
### Step 3. Plan
**VLAN** <br />

-	Phòng ban. <br />
-	Quản trị. <br />
-	Khách hàng. <br />
-	Camera. <br />

Table 3.1: **Device Port Planning** <br />
![image](https://user-images.githubusercontent.com/81057831/132111500-53a92cea-0e35-4ce1-a2da-dd15fdf759f4.png) <br />
Table 3.2: **VLAN Subnetting** <br />
![image](https://user-images.githubusercontent.com/81057831/132111545-3e7393e1-7a3b-43ac-83b2-f642e369493e.png) <br />
### Step 4. Design
Image 4.1: **Logic Diagram Design** <br />
![image](https://user-images.githubusercontent.com/81057831/132111632-fca2ae0c-9862-4d86-9c7c-0925456c4de5.png) <br />
Image 4.2: **Physical Diagram Design** <br />
![image](https://user-images.githubusercontent.com/81057831/132111645-2de6311f-61b4-4f8e-beb7-77cfe6f07162.png) <br />
Image 4.3: **Physical Layout Design** <br />
![Rackdia](https://user-images.githubusercontent.com/81057831/132111579-ad6a3fde-79be-4ea3-80b1-07032c371812.png) <br />
Image 4.4: **EIGRP Routing Design** <br />
![image](https://user-images.githubusercontent.com/81057831/132111596-0a624f34-0ad8-4d27-a199-d33e9b1ad189.png) <br />


