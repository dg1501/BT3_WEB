# BÀI TẬP 3     : MÔN PHÁT TRIỂN ỨNG DỤNG TRÊN NỀN WEB
## Giảng viên   : Đỗ Duy Cốp
## Lớp học phần : 58KTPM
### Ngày giao   : 2025-10-24 13:50
### Hạn nộp     : 2025-11-05 00:00
----------------------------------------------------</P>
# LẬP TRÌNH ỨNG DỤNG WEB TRÊN NỀN LINUX.</P>
## 1. Cài đặt môi trường linux
## 2. Cài đặt Docker
## 3. Sử dụng 1 file docker-compose.yml để cài đặt các docker container
## 4. Lập trình web frontend+backend
## 5. Nginx làm web-server</P>
----------------------------------------------------</P>
**1. CÀI ĐẶT MÔI TRƯỜNG LINUX**</p>
1.1. Cài đặt Ubuntu.</p>
a) Bật WSL2.</p>
- Mở CMD (Admin) -> dán `wsl --install`.</p>
<img width="1101" height="595" alt="image" src="https://github.com/user-attachments/assets/4f13037f-7f13-4b85-b13e-d52b9c809b7f" /></p>
b) Sử dụng Virtual Box cài Ubuntu.</p>
- Sau khi khởi động lại.</p>
- Truy cập link `https://www.virtualbox.org/wiki/Downloads` tiến hành dowload Virtual Box.</p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/edfbf7e2-c381-4bc1-b9f4-a364c272c4f3" /></p>
- Truy cập link `https://ubuntu.com/download/desktop` để tải ISO Ubuntu.</p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/daa6a3ae-c583-4e44-a1cd-4898008b7cce" /></p>
c) Tạo máy ảo Ubuntu.</p>
- Mở VirtualBox → bấm New.</p>
- Name: **Ubuntu**.</p>
- Type: **Linux**.</p>
- Version: **Ubuntu (64-bit)**.</p>
→ Bấm **Next**.</p>
<img width="1057" height="950" alt="image" src="https://github.com/user-attachments/assets/22555c9b-f98c-44bf-a6c5-773bcea9a51e" /></p>
- Chọn RAM.</p>
<img width="1061" height="943" alt="image" src="https://github.com/user-attachments/assets/3ec7e048-0e56-4afb-90ca-69d3163cf614" /></p>
d) Cài Ubuntu.</p>
- Chọn máy **Ubuntu** vừa tạo → bấm **Settings** → **Storage**.</p>
- Trong phần “Controller: IDE” → click biểu tượng đĩa → Choose a disk file.</p>
- Chọn file .iso Ubuntu.</p> 
→ OK.</p>
<img width="994" height="944" alt="image" src="https://github.com/user-attachments/assets/abd9c29a-529c-4cdb-a4e4-51156b29bf53" /></p>
- Bấm **Start with GUI để chạy khởi động.</p>
- Nhập usernam + password.</p>
<img width="1314" height="964" alt="image" src="https://github.com/user-attachments/assets/9b6c4a31-9c78-45da-95da-6cb9d7e6e1d0" /></p>
**2. CÀI ĐẶT DOCKER DESKTOP**.</p>
a) Truy cập Link `https://www.docker.com/`.</p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f604ace9-7d74-4a1f-b985-f08379e5e0a7" /></p>
**3. CÀI ĐẶT DOCKER CONTAINER**</p>
<img width="742" height="516" alt="image" src="https://github.com/user-attachments/assets/41dc76a1-4495-4268-aa4d-8c8de0024ef2" /></p>
a) **MARIADB (3306)**.</p>
b) **PHPADMIN (8080)**.</P>
<img width="1295" height="815" alt="image" src="https://github.com/user-attachments/assets/17bd64ba-db47-4770-bfba-0e9f70497add" /></p>
c) **Nodered/node-red (1880)**.</p>
<img width="1287" height="810" alt="image" src="https://github.com/user-attachments/assets/e4403668-9056-493f-b809-7a85beef2efd" /></p>
d) **influxdb (8086)**.</p>
<img width="1285" height="806" alt="image" src="https://github.com/user-attachments/assets/1bb7df96-d0bb-4f6d-8545-6dd1c606d830" /></p>
e) **grafana/grafana (3000)**.</p>
<img width="1309" height="874" alt="image" src="https://github.com/user-attachments/assets/adbd748f-9608-4192-9b72-68e3a83ac365" />.</p>
f) **nginx (80,443)**.</p>
<img width="1697" height="808" alt="image" src="https://github.com/user-attachments/assets/4b7467b1-f4f1-475d-9b2b-9f8f3f9da989" /></p>
**4. Lập trình web frontend+backend (Web IOT: Giám sát dữ liệu IOT)**.</p>
4.1. Tạo cơ sở dữ liệu trong MariaDB.</p>
a) Tạo Database.</p>
- Nhấn **New** → đặt tên **iot_db** → **Create**.</p>
<img width="1567" height="916" alt="image" src="https://github.com/user-attachments/assets/d8dad631-6db9-452d-abe8-713b09777ed3" /></p>
b) Tạo bảng.</p>
- Mở Tab **SQL** -> dán code tạo bảng vào khung -> **Perform**.</p>
<img width="1567" height="923" alt="image" src="https://github.com/user-attachments/assets/20280ca2-6355-43c3-af96-db7b8dad3c92" /></p>
- Kết quả.</p>
<img width="1867" height="713" alt="image" src="https://github.com/user-attachments/assets/ccc2f2b4-bd12-4449-ac21-d14f55a1b980" /></p>
4.2. Cấu hình Node-RED.</p>
a) Cài thêm các node.</p>
---Nhấn **Menu** → **Manage palette** → **Install** → tìm và cài:</p>
+ `node-red-node-mysql (kết nối MariaDB)`</p>
+ `node-red-contrib-influxdb (ghi dữ liệu vào InfluxDB)`</p>
<img width="889" height="862" alt="{D939435A-6614-4D98-BBC5-44C7F5473A73}" src="https://github.com/user-attachments/assets/c4494117-a1cb-4b03-a56e-2127f3380069" /></p>
<img width="905" height="868" alt="{BA471DF4-CB08-46B2-BDE3-DCF4060F7037}" src="https://github.com/user-attachments/assets/4621e3da-f7c5-4231-9e57-632c829c9cd4" /></p>
b) Tạo và điền thông tin cho MySQL connection node:</p>
<img width="659" height="915" alt="{66290410-BAE5-4D9D-85A0-C60EF8A1A4A6}" src="https://github.com/user-attachments/assets/3fa41d9f-641b-43db-83f0-f9cc3588d420" /></p>
c) Tạo và điền thông tin cho InfluxDB connection node:</p>
<img width="692" height="847" alt="{05DEB38F-9C13-459C-8520-F52A1C42ADFD}" src="https://github.com/user-attachments/assets/9c5f454d-c95b-4ee1-967a-0c039cd71291" /></p>
4.3. Tạo flow Node-RED.</p>
a) Tạo dữ liệu giả lập.</p>
--- Tạo và cấu hình node **inject**.</p>
- Payload: chọn `TimeStamp`.</p>
<img width="742" height="854" alt="{61FB9A39-15F0-4998-AE97-2A3878AA6961}" src="https://github.com/user-attachments/assets/b380fbb8-e5ab-40df-a5ee-fb8e150af547" /></p>
- Tick **Repeat** → **Interval**: every 5 seconds.-> Done </p>
<img width="661" height="757" alt="image" src="https://github.com/user-attachments/assets/b91712f1-6605-46bb-b1e5-f154522ce54b" /></p>
b) Kéo node **function** → nối với inject.</p>
- Cấu hình node Function.</p>
<img width="824" height="856" alt="{68B3122D-08E4-4FF8-8EDC-CE1EEE296E07}" src="https://github.com/user-attachments/assets/fe3eb3b0-3850-49da-a8a7-062220086a65" /></p>
c) Thêm node Functon -> kết nối với `Generate Sensor Data` -> đặt tên **Insert/Update MariaDB**.</p>
<img width="815" height="855" alt="image" src="https://github.com/user-attachments/assets/257729ba-10b0-4045-a45e-041cee1ff361" /></p>
d) Kéo node function khác → nối từ **Generate Sensor Data** -> tên là **Insert InfluxDB**.</p>
<img width="812" height="855" alt="{541E3EBC-439F-42E5-85CF-1996FD32041C}" src="https://github.com/user-attachments/assets/e314d9f3-0997-4598-a395-3fa4f601bb6f" /></p>
e) Thêm node `http in` phục vụ **frontend**.</p>
<img width="636" height="858" alt="{85CDC74B-328E-450B-B505-DEFF35085360}" src="https://github.com/user-attachments/assets/abe98b26-91a8-4417-a966-48ce02b2536a" /></p>
f) Thêm node `http response`.</p>
<img width="644" height="859" alt="image" src="https://github.com/user-attachments/assets/6bb0667f-0d92-4de8-b818-feb10300f492" /></p>
4.4. Tổng sơ đồ **NODERED**.</p>
<img width="1862" height="862" alt="{6F01A35D-5547-41A0-967A-8F97A7DC8BC5}" src="https://github.com/user-attachments/assets/b1b7bf73-8422-4bf5-9b5b-2e3ef2011a20" /></p>
4.5. Kết quả.</p>
<img width="822" height="230" alt="{EB628C80-F8DD-4CE6-A4CC-AEF95B6A37BA}" src="https://github.com/user-attachments/assets/c60ee542-2f64-4f74-a7cb-96a46e5835b4" /></p>
4.6. Tạo bảng **USER**.</p>
<img width="1581" height="864" alt="{BA7DFFDE-2145-49B5-A8CA-34408BFE85D6}" src="https://github.com/user-attachments/assets/df088306-02d9-4ca1-96a8-0e0d3413d015" /></p>
4.7. Tạo tài khoản **ADMIN**.</p>
<img width="1595" height="537" alt="{4B2A20D5-752A-4FAA-AE0A-6222D611A3A8}" src="https://github.com/user-attachments/assets/48f1fe6a-21d4-4780-9240-7219a4206203" /></p>
4.8. Dowload **XAMPP**.</p>
a) Truy cập link `https://www.apachefriends.org/download.html`.</p>
<img width="1852" height="902" alt="{D1359D0D-5DD0-474D-BDAB-E0D11EFE8C54}" src="https://github.com/user-attachments/assets/1fc291b5-93b1-470a-972b-a9c54d700907" /></p>
- kết quả</p>
<img width="834" height="728" alt="{F9CA5A4F-06C1-4304-B1E6-D72A728807BA}" src="https://github.com/user-attachments/assets/84f15fce-0090-416f-af4d-102af8ca15e7" /></p>
b) Tạo file **index.html**.</p>
<img width="1917" height="1023" alt="{6AFAFB8A-D395-42B1-BDD1-CE8BE4737CBA}" src="https://github.com/user-attachments/assets/4db8b6af-1e46-4ff3-84fa-64252cd9458e" /></p>














