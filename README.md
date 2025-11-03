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
**3.CÀI ĐẶT DOCKER CONTAINER**</p>
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



