# BÀI TẬP 3     : MÔN PHÁT TRIỂN ỨNG DỤNG TRÊN NỀN WEB
## Giảng viên   : Đỗ Duy Cốp
## Lớp học phần : 58KTPM
### Ngày giao   : 2025-10-24 13:50
### Hạn nộp     : 2025-11-06 23:59
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

b) Tạo Folder BT3_WEB.</p>
<img width="869" height="104" alt="image" src="https://github.com/user-attachments/assets/2b9e8ec8-c3fa-4aa5-b438-d92351587442" /></p>

c) Trong BT3_WEB.</p> 
--- Tạo file `docker-compose.yml`.</p>
<img width="449" height="396" alt="image" src="https://github.com/user-attachments/assets/00105f19-d046-425a-b8aa-4900d2255978" /></p>

--- Tạo Folder nginx.</p>
+ Tạo file nginx.conf.</p>
<img width="1123" height="950" alt="image" src="https://github.com/user-attachments/assets/293e3b79-39ae-4cd9-b3dd-98ac5d131629" /></p>

+ Tạo Foler html.</p>
+ Trong html tạo:</p>
1. **index.html**.</p>
<img width="1106" height="917" alt="image" src="https://github.com/user-attachments/assets/35249a92-98b3-40a5-81db-961bf070fb28" /></p></p>

2. **images**.</p>
<img width="1149" height="482" alt="image" src="https://github.com/user-attachments/assets/d6a6635a-73e2-417e-85ef-dd50093403b8" /></p></p>

**2. CÀI ĐẶT DOCKER DESKTOP**.</p>
a) Truy cập Link `https://www.docker.com/`.</p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f604ace9-7d74-4a1f-b985-f08379e5e0a7" /></p>

b) Tiến hành chạy file .yml.</p>
- Sử dụng lệnh `docker-compose up -d`.</p>
<img width="1108" height="966" alt="image" src="https://github.com/user-attachments/assets/cbcdd70e-784d-49d5-8759-f32f9bd02b57" /></p>

c) Kết quả.</p>
<img width="1133" height="351" alt="image" src="https://github.com/user-attachments/assets/fb879c77-424c-488e-96fc-9846f00ad032" /></p>

**3. DOCKER CONTAINER**</p>

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

**4. LẬP TRÌNH WEBSITE THƯƠNG MẠI ĐIỆN THỬ**.</p>
4.1. Tạo cơ sở dữ liệu trong MariaDB.</p>
a) Tạo CSDL.</p>
- Tạo bảng **USERS**.</p>
<img width="1172" height="633" alt="image" src="https://github.com/user-attachments/assets/b94fdb09-f5ab-49d9-8a2e-1088c20c1e56" /></p>

b) Tạo bảng **PRODUCTS**.</p>
<img width="1390" height="708" alt="image" src="https://github.com/user-attachments/assets/222a51f3-158b-4f09-ade7-5739ccf703ac" /></p>

c) Tạo bảng **ODER_ITEMS**.</p>
<img width="1242" height="345" alt="image" src="https://github.com/user-attachments/assets/95aa5166-4965-42e4-9eb5-b561694fa7db" /></p>

d) Tạo bảng **ODERS**.</p>
<img width="1107" height="413" alt="image" src="https://github.com/user-attachments/assets/d0da8247-ce45-49a4-bdf8-ec452ce755d1" /></p>

e) Tạo bảng **CATEGORIES**</p>
<img width="1255" height="697" alt="image" src="https://github.com/user-attachments/assets/6fd19aaf-a07b-4d57-84e6-49151ec3a701" /></p>

4.2. Cấu hình NODE-RED.</p>
a) Cài thêm các Node Thư Viện.</p>
<img width="770" height="928" alt="image" src="https://github.com/user-attachments/assets/24b56dff-b513-4257-865c-fd42730c9bc9" /></p>

b) Thêm Node Login.</p>
<img width="1859" height="858" alt="image" src="https://github.com/user-attachments/assets/9de0f6e8-bba7-449d-b00d-3cdbd74dd16d" /></p>

c) Thêm Node Shop API.</p>
<img width="1857" height="863" alt="image" src="https://github.com/user-attachments/assets/02c8e914-118c-4a05-a712-3508d1fc55b5" /></p>

d) Thêm Node Oder API.</p>
<img width="1857" height="858" alt="image" src="https://github.com/user-attachments/assets/b4fce8d9-de78-4571-8ad7-14c5050b8fb7" /></p>

e) Thêm Node Admin API.</p>
<img width="1858" height="863" alt="image" src="https://github.com/user-attachments/assets/c711ba6c-3a8a-481c-b1e0-c2107859d01f" /></p>

4.3. Thêm Code HTML.</p>
<img width="1106" height="917" alt="image" src="https://github.com/user-attachments/assets/c78fcbc9-984e-4bb7-8284-a00a8471202c" /></p>

4.4. Form HTML.</p>
a) Login
<img width="1546" height="1002" alt="image" src="https://github.com/user-attachments/assets/c517282e-aec3-4b64-8e15-2403d7bc4291" /></p>

b) Giao diện User.</p>
<img width="1659" height="976" alt="image" src="https://github.com/user-attachments/assets/3850d9d1-d8fe-4a5a-8d33-fd36f340108e" /></p>

c) Giao diện Admin.</p>
<img width="1689" height="922" alt="image" src="https://github.com/user-attachments/assets/3af841fe-a099-461e-8954-c2e83c998040" /></p>

d) Tính năng liệt kê các sản phẩm bán chạy ra trang chủ.</p>
<img width="1605" height="561" alt="image" src="https://github.com/user-attachments/assets/75a1c4c1-eb17-424d-bd59-3eee35f1f740" /></p>

e) Tính năng liệt kê các nhóm sản phẩm.</p>
<img width="1540" height="908" alt="image" src="https://github.com/user-attachments/assets/0ff375a1-e6cc-49ae-ad40-be40ebb74b90" /></p>

f) Tính năng tìm kiếm theo tên sản phẩm.</p>
<img width="1622" height="966" alt="image" src="https://github.com/user-attachments/assets/362fcdbd-fe91-4049-b72c-1f1221798612" /></p>

g) Tính năng chọn sản phẩm (đưa sản phẩm vào giỏ hàng, thay đổi số lượng sản phẩm trong giỏ, cập nhật tổng tiền).</p>
<img width="1623" height="916" alt="image" src="https://github.com/user-attachments/assets/72df5f59-0715-46e7-81c8-5148640d633a" /></p>

i) Tính năng đặt hàng, nhập thông tin giao hàng => được 1 đơn hàng.</p>
<img width="1621" height="918" alt="image" src="https://github.com/user-attachments/assets/e16fa3bb-20b0-47fb-b28a-0e6765fabcec" /></p>

<img width="1659" height="968" alt="image" src="https://github.com/user-attachments/assets/f1aec4ef-4de7-4934-a8e3-c8adf9adbf8d" /></p>

k) Tính năng dành cho **ADMIN**.</p>
- Thống kê xem có bao nhiêu đơn hàng, call để xác nhận và cập nhật thông tin đơn hàng. chuyển cho bộ phận đóng gói, gửi bưu điện, cập nhật mã COD, tình trạng giao hàng, huỷ hàng,....</p>
<img width="1822" height="920" alt="image" src="https://github.com/user-attachments/assets/a73abed2-30ef-4b5e-a4b9-248b719acd9d" /></p>

4.5. Thiết kế biểu đồ sử dụng Grafana.</p>
a) Vào Grafana -> http://localhost:3001.</p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c9a89a8e-470b-49d8-8958-dc20aa9e79f4" /></p>

b) Thêm Panel -> Add visualization.</p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2cc8a307-415c-4e82-9ae3-76ab52e0768b" /></p>

c) Tiến hành thiết lập -> điền đúng thông tin.</p>
<img width="1861" height="922" alt="image" src="https://github.com/user-attachments/assets/5addc02f-1c39-49d1-a0cf-d36cd169d904" /></p>

d) Save & Test.</p>
<img width="1604" height="929" alt="image" src="https://github.com/user-attachments/assets/96246cfe-0152-424d-a60e-d17d7a7cc15e" /></p>

e) Quay lại Dashboards -> Chọn Panel vừa tạo.</p>
<img width="1865" height="419" alt="image" src="https://github.com/user-attachments/assets/8da1b385-51cc-4cb6-bfaf-d1f9687eba0b" /></p>

f) Edit biểu đồ theo ý thích.</p>
<img width="874" height="387" alt="image" src="https://github.com/user-attachments/assets/b60adf1f-ee9c-4293-bfde-f79759c48e03" /></p>

`from(bucket: "shop-data")
  |> range(start: v.timeRangeStart, stop: v.timeRangeStop)
  |> filter(fn: (r) => r["_measurement"] == "sales")
  |> filter(fn: (r) => r["_field"] == "items_count") 
  |> aggregateWindow(every: 1d, fn: sum, createEmpty: false) // Tính tổng số lượng bán ra mỗi ngày
  |> yield(name: "Số lượng mặt hàng bán ra")`</p>

- Biểu đồ thống kê số lượng mặt hàng bán được trong từng ngày. (sử dụng grafana).</p>

**5. NGINX LÀM WEB-SERVER**.<?p>
a) Cấu hình ***nginx*** để chạy được website qua url http://fullname.com (nguyenducduong.com).</p>
- Theo đường dẫn `C:\Windows\System32\drivers\etc\host` bằng quyền admin
<img width="1029" height="311" alt="image" src="https://github.com/user-attachments/assets/e69d0dac-8da5-49d6-92db-111827a92ecd" /></p>

- Thêm *127.0.0.1 nguyenducduong.com* vào cuối file -> save.</p>
<img width="787" height="53" alt="image" src="https://github.com/user-attachments/assets/29115162-f550-48ca-8497-6d386fbd42a5" /></p>

b) Thay đổi server name trong **nginx.conf**.</p>
<img width="1125" height="362" alt="image" src="https://github.com/user-attachments/assets/b719e052-b51b-41f7-9c12-23c36a570109" /></p>

c) Thay đổi Host Grafana trong **docker-compose.yml**.</p>
<img width="1042" height="351" alt="image" src="https://github.com/user-attachments/assets/67ebd7a8-f422-4be4-a180-4430f89ef3f1" /></p>

**6. TEST**.</p>
a) Nodered.</p>
<img width="1813" height="964" alt="image" src="https://github.com/user-attachments/assets/6c469f84-7578-4b9a-864d-57df352b703b" /></p>

b) WEB.</p>
<img width="1717" height="967" alt="image" src="https://github.com/user-attachments/assets/5f361aca-33bb-4c23-a75d-0bcf17854297" /></p>

c) GRAFANA.</p>
<img width="1827" height="962" alt="image" src="https://github.com/user-attachments/assets/c377aa05-ee5a-431f-894e-dd3507a224fc" /></p>
















