LIGHT TV 0.1 — DỰ ÁN MÃ NGUỒN ANDROID TV / GOOGLE TV
====================================================

Đây là dự án Android mẫu khởi đầu, chưa phải file APK đã build.
Giao diện dùng nền tối, banner giới thiệu và danh sách ứng dụng cài trên tivi.
Có khai báo LAUNCHER, LEANBACK_LAUNCHER và HOME; việc đặt làm launcher mặc định
phụ thuộc vào phiên bản Android TV/Google TV và chính sách của nhà sản xuất.

CẤU TRÚC
- settings.gradle
- build.gradle
- app/build.gradle
- app/src/main/AndroidManifest.xml
- app/src/main/java/com/lighttv/launcher/MainActivity.java

BUILD
1. Giải nén ZIP trên điện thoại.
2. Mở thư mục dự án bằng AndroidIDE tương thích.
3. Chờ Gradle sync và tải Android SDK cần thiết.
4. Build APK debug.
5. APK thường được tạo ở app/build/outputs/apk/debug/app-debug.apk.

YÊU CẦU THAM KHẢO
- Android Gradle Plugin 8.6.1
- Gradle 8.7
- JDK 17
- Android SDK Platform 35

LƯU Ý
- Đây là bản khởi đầu, không phải launcher thương mại hoàn chỉnh.
- Build có thể cần sửa đổi tùy phiên bản AndroidIDE/Gradle và thiết bị.
- Hãy thử chạy ứng dụng trước khi đổi launcher mặc định.
- Không dùng thao tác ADB hoặc thay đổi hệ thống nếu chưa hiểu rõ cách khôi phục.
