# T Solar-meter
**T-Solar Meter là công tơ điện tử đo 2 điểm ứng dụng trên công nghệ Wifi IoT được thiết kế dễ dàng lắp đặt vào nguồn cung cấp điện mà không phải tháo hay đấu nối phức tạp.**
<img src="https://github.com/Tpro4391/Solar-meter/blob/master/Home%20solar.jpg">
giao diện Web local có thể truy cập bằng IP hoặc địa chỉ: solar-meter.local/ hoặc solar-meter/
<img src="https://github.com/Tpro4391/Solar-meter/blob/master/hop-chuan.jpg">
# SƠ ĐỒ KẾT NỐI
 | ESP8266 | PZEM Solar | Pzem Tải | Nút reset | Led stt | 
 |-----------|-----------|-----------|-----------|-----------| 
 | D1 | TX |  |  |  | 
 | D2 | RX |  |  |  | 
 | D3 |  |  | X |  | 
 | D4 |  |  |  | X | 
 | TX |  | TX |  |  | 
 | RX |  | RX |  |  | 
 | GND | GND | GND | GND | GND | 
 | VCC | VCC | VCC |  |  | 

# I. LẮP ĐẶT
-	Chân CT1 đấu vào kẹp dòng được kèm theo. Kẹp dòng này được kẹp sau inverter của Solar (đầu ra của solar đấu nối vào lưới điện).
-	Chân CT2 đấu vào kẹp dòng được kèm theo. Kẹp dòng này được kẹp vào đầu vào của phụ tải, sau đầu kết nối của solar (kẹp vào đường điện vào nhà mình tiêu thụ, sau phía đấu nối solar)
-	Các chân cấp nguồn có thể cấp độc lập (phần solar đấu nối điện ra solar, phần tải tiêu thụ đấu nối vào tải liêu thụ) Hoặc cũng có thể đấu nối chung nhau và chung vào phần tải tiêu thụ.
<img src="https://github.com/Tpro4391/Solar-meter/blob/master/nhan%20vo%20hop.png">
 
## QUAN TRỌNG:

*** 1.	Thiết bị này chỉ dùng với sơ đồ đấu nối lưới điện đầu nguồn (Inverter đấu nối phía đầu nguồn với tải như hình). Không sử dụng được với sơ đồ đầu nối cuối nguồn. ***

*** 2.	Kẹp dòng vào 1 trong 2 dây của nguồn điên, không được kẹp vào cả 2 dây của nguồn điện. ***
# II. THÔNG SỐ KỸ THUẬT
## 1.1 Điện áp (U)
    1.1.1 Điện áp: 80~260V
    1.1.2 Độ phân giải: 0.1V
    1.1.3 Độ chính xác của phép đo: 0,5%
## 1.2 Dòng điện (A)
    1.2.1 Phạm vi đo: 0 ～ 100A
    1.2.2 Dòng đo khởi động: 0,02A
    1.2.3 Độ phân giải: 0,001A
    1.2.4 Độ chính xác của phép đo: 0,5%
## 1.3 Công suất (kW)
    1.3.1 Phạm vi đo: 0 ~23kW
    1.3.2 Công suất đo khởi động: 0.4W
    1.3.3 Độ phân giải: 0.1W
    1.3.5 Độ chính xác của phép đo: 0,5%
## 1.4 Hệ số công suất (PF)
    1.4.1 Phạm vi đo: 0,00 ~ 1,00
    1.4.2 Độ phân giải: 0,01
    1.4.3 Độ chính xác của phép đo: 1%
## 1.5 tần số (Hz)
    1.5.1 Phạm vi đo: 45Hz ~ 65Hz
    1.5.2 Độ phân giải 0.1Hz
    1.5.3 Độ chính xác đo: 0,5%
## 1.6 Điện năng tiêu thụ (kWh)
    1.6.1 Phạm vi đo: 0 ~ 9999,99kWh
    1.6.2 Độ phân giải: 1Wh
    1.6.3 Độ chính xác đo: 0,5%

# III. SỬ DỤNG
## 1.	Khởi động và kết nối wifi
-	Khi bắt đầu cấp nguồn sau 15~30 giây nếu chưa có kết nối wifi được thiết lập. Thiết bị tự động phát wifi “T-Meter_XXXX” trong đó XXXX là ID của công tơ.
-	Người dùng sử dụng máy tính hoặc điện thoại di động thực hiện kết nối đến Wifi của công tơ, mật khẩu mặc định là “12345678”
-	Sau khi kết nối thành công, sử dụng trình duyệt truy cập đến địa chỉ: “http://192.168.4.1” để vào trang web của công tơ.
-	Vào mục “CONNECT”, chọn “Scan wifi” Sau đó chọn wifi cần kết nối. Nhập mật khẩu wifi cần kết nối và ấn “Save”.
-	Ấn tiếp “Khởi động lại” để thực hiện khởi động lại thiết bị và kết nối tới wifi được cài đặt.
-	Sau khi kết nối nếu Wifi “T-Meter_XXXX” không còn nữa thì thiết bị đã kết nối thành công. Lúc này người dùng truy cập cùng wifi với công tơ sau đó truy cập địa chỉ: “http://solar-meter.local/”  hoặc “http://solar-meter/” hoặc  địa chỉ IP trong mạng wifi mới để truy cập vào xem chỉ số của công tơ.

- Chú ý 1: Người dùng có thể truy cập địa chỉ: “http://solar-meter.local/” hoặc “http://solar-meter/”  bằng máy tính, laptop win 10 hoặc trên điện thoại sử dụng hệ điều 	hành IOS (Iphone).  Điện thoại Androi chỉ truy cập theo địa chỉ IP được do bị chặn DNS local.

- Chú ý 2: Truy cập bằng IP sẽ nhanh hơn so với truy cập bằng địa chỉ http://solar-meter.local/” . Có thể lấy địa chỉ IP bằng cách dùng điện thoại Iphone truy cập “http://solar-meter.local/” sau đó kéo xuống phần IP để lấy địa chỉ ip. Ngoài ra cũng có thể dùng phần mềm Scan IP.
## 2.	Kết nối tới ứng dụng “Blynk”
Blynk là ứng dụng IoT trên điện thoại di động, người dùng có thể tìm kiếm và cài đặt phần mềm trên cả Androi và IOS.
### Bước 1: Nhập giao điện xem chỉ số công tơ trên ứng dụng blynk:
Quét mã QR sau tương ứng với blynk free (bị giới hạn 2000 điểm energy):
   <img src="https://github.com/Tpro4391/Solar-meter/blob/master/blynk%20freee.png">
   <img src="https://github.com/Tpro4391/Solar-meter/blob/master/blynk%20fee.jpg">

Quét mã QR sau tương ứng với blynk đã mua thêm energy (liên hệ mình để mua thêm điểm energy):
   <img src="https://github.com/Tpro4391/Solar-meter/blob/master/blynk%20full.png">
   <img src="https://github.com/Tpro4391/Solar-meter/blob/master/Blynk%20Full.jpg">
   
Chú ý: Ngoài ra các bạn có thể tự thiết lập giao diện blynk theo sở thích của mình với địa chỉ được cung cấp như mục 3


### Bước 2: Lấy mã Auth Blynk, từ giao diện của phần mềm:
       
	Người dùng có thể copy auth token hoặc gửi auth token qua mail!
	Bước 3: Dán mã Auth token đã lấy vào cài đặt thiết bị:
 
## 3.	Kết nối tới nền tảng, hệ sinh thái khác qua MQTT (hass io,..)
Để gửi dữ liệu qua MQTT vào mục connect và chọn kết nối MQTT
 
Cấu trúc dữ liệu gửi qua MQTT là dạng json với 2 data như sau:
 | Chỉ số | Đơn vị | Blynk virutal | MQTT Topic | MQTT Json | 
 |------------------|---------|--------------|-------------|-------------| 
 | Trạng thái |  | V0 | "Topic"/data1 | stt | 
 | Điện áp solar | V | V1 | "Topic"/data1 | V1 | 
 | Dòng điện solar | A | V2 | "Topic"/data1 | A1 | 
 | Công suất solar | kW | V3 | "Topic"/data1 | kW1 | 
 | Tần số solar | Hz | V4 | "Topic"/data1 | Hz1 | 
 | Cos Pi solar | PF | V5 |  |  | 
 | Chỉ số điện solar | kWh | V6 |  |  | 
 | Điện áp tải | V | V7 | "Topic"/data1 | V2 | 
 | Dòng điện tải | A | V8 | "Topic"/data1 | A2 | 
 | Công suất tải | kW | V9 | "Topic"/data1 | kW2 | 
 | Tần số tải | Hz | V10 |  |  | 
 | Cos Pi tải | PF | V11 |  | PF | 
 | Chỉ số điện tải | kWh | V12 |  |  | 
 | Sản lượng Solar hôm qua | kWh | V13 | "Topic"/data2 | E_slhn | 
 | Sản lượng solar hôm nay | kWh | V14 | "Topic"/data2 | E_slhq | 
 | Sản lượng Solar tháng trước | kWh | V15 | "Topic"/data2 | E_sltt | 
 | Sản lượng solar tháng này | kWh | V16 | "Topic"/data2 | E_sltn | 
 | Điện mua vào EVN (Chiều thuận) hôm qua | kWh | V17 | "Topic"/data2 | E_vhq | 
 | Điện xuất ra lưới (Chiều nghịch) hôm qua | kWh | V18 | "Topic"/data2 | E_xhq | 
 | Tiền mua điện EVN hôm qua | VNĐ | V19 | "Topic"/data2 | T_mhq | 
 | Tiền bán điện cho EVN hôm qua | VNĐ | V20 | "Topic"/data2 | T_bhq | 
 | Tiền phải trả EVN hôm qua | VNĐ | V21 | "Topic"/data2 | T_thq | 
 | Điện mua vào EVN (Chiều thuận) hôm nay | kWh | V22 | "Topic"/data3 | E_vhn | 
 | Điện xuất ra lưới (Chiều nghịch) hôm nay | kWh | V23 | "Topic"/data3 | E_xhn | 
 | Tiền mua điện EVN hôm nay | VNĐ | V24 | "Topic"/data3 | T_mhn | 
 | Tiền bán điện cho EVN hôm nay | VNĐ | V25 | "Topic"/data3 | T_bhn | 
 | Tiền phải trả EVN hôm nay | VNĐ | V26 | "Topic"/data3 | T_thn | 
 | Điện mua vào EVN (Chiều thuận) tháng trước | kWh | V27 | "Topic"/data3 | E_vtt | 
 | Điện xuất ra lưới (Chiều nghịch) tháng trước | kWh | V28 | "Topic"/data3 | E_xtt | 
 | Tiền mua điện EVN tháng trước | VNĐ | V29 | "Topic"/data3 | T_mtt | 
 | Tiền bán điện cho EVN tháng trước | VNĐ | V30 | "Topic"/data4 | T_btt | 
 | Tiền phải trả EVN tháng trước | VNĐ | V31 | "Topic"/data4 | T_ttt | 
 | Điện mua vào EVN (Chiều thuận) tháng này | kWh | V32 | "Topic"/data4 | E_vtn | 
 | Điện xuất ra lưới (Chiều nghịch) tháng này | kWh | V33 | "Topic"/data4 | E_xtn | 
 | Tiền mua điện EVN tháng này | VNĐ | V34 | "Topic"/data4 | T_mtn | 
 | Tiền bán điện cho EVN tháng này | VNĐ | V35 | "Topic"/data4 | T_btn | 
 | Tiền phải trả EVN tháng này | VNĐ | V36 | "Topic"/data4 | T_ttn | 
 | Đèn báo chiều (blynk) |  | V37 |  |  | 

## Ví dụ đọc dữ liệu cho hassio sẽ được cấu hình ở file .yaml như sau: (với ABC là topic được cài đặt)
	sensor:
	  - platform: mqtt
	    name: "01.Điện Áp"
	    state_topic: "ABC/data1"
	    value_template: "{{ value_json.V }}"
	    unit_of_measurement: "V"
	    icon: mdi:flash-circle

# IV. NÂNG CẤP CHƯƠNG TRÌNH (UPDATE FIRMWARE)
### Bước 1:  Vào “SETUP” Chọn “UPDATE”
 
### Bước 2: Tại trang web update rồi nhập mật khẩu và tài khoản là “admin”

### Bước 3: Chọn tên ở mục “Firmware” rồi ấn update và đợi báo update thành công!
            


 

