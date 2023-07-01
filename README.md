# Hướng dẫn setup

Theo sát các bước này để cấu hình project trên Eclipse. Các bước sau giả sử máy đích chạy trên Windows.


## Yêu cầu cài đặt trước

Cài **Adoptium OpenJDK 11**: [Latest Releases | Adoptium](https://adoptium.net/temurin/releases/?version=11). Tải bản JDK .msi.

Cài **Scene Builder**: [Scene Builder - Gluon (gluonhq.com)](https://gluonhq.com/products/scene-builder/#download). Tải bản 20, Windows Installer. 

Nhớ đường dẫn cài đặt cho cả hai thứ.

## Cấu hình project

 1. `git clone` project này về, với git client tùy chọn.
 2. Cấu hình Eclipse sử dụng **Adoptium OpenJDK 11**:
	 - Trong Eclipse, Windows > Preferences > Java > Installed JREs, chọn nút Add...
	 - Chọn Standard VM > Next
	 - Chọn Directory là đường dẫn cài đặt. (Thường sẽ nằm tại `C:\Program Files\Eclipse Adoptium\jdk-11.0.19.7-hotspot`), rồi Finish để kết thúc.
	 - Tiếp tục từ Installed JREs > Execution Environments, chọn JavaSE-11, và chọn JDK mình vừa cài đặt (thường sẽ là jdk-11.0.19.7-hotspot).
	 - Thoát bằng nút Apply and Close.
 3. Cấu hình **SceneBuilder**:
	 - Trong Eclipse, Windows > Preferences > JavaFX
	 - Ở SceneBuilder executable, chọn Browse
	 - Trỏ đến file .exe trong đường dẫn cài đặt. (Thường sẽ ở `C:\Users\<tên máy>\AppData\Local\SceneBuilder\SceneBuilder.exe`)
	 - Thoát bằng nút Apply and Close.
 4. Cấu hình **e(fx)clipse**:
	 - Trong Eclipse, Help > Eclipse Marketplace
	 - Ô Find, tìm `fx` và Enter
	 - Click Install e(fx)clipse bản mới nhất
	 - Tiếp tục Confirm để tải
 5. Cấu hình JavaFx và Mysql-connector-j có trong thư mục lib:
	 - JavaFx: Trong Eclipse > Windows > Preferences > Java > Build Path > User Libraries > New > Nhập "javafx" > Add External Jars >                               
	 H:\Code\KtpmProject\quan_li_nhan_khau\QuanLyNhanKhau\lib\javafx-sdk-11.0.2\lib
	 - Mysql-connnector-j: Trong Eclipse: Chọn Configure Build Path > Libraries > Add External JARs >  
         H:\Code\KtpmProject\quan_li_nhan_khau\QuanLyNhanKhau\lib\mysql-connector-j-8.0.33/mysql-connector-j-8.0.33.jar
