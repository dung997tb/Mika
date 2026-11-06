<div align="center">

<img src="../media/logo.png" alt="Mika" width="88" />

# Mika — Tiếng Việt

**Trợ lý AI trên điện thoại: bạn giao việc, Mika tự thao tác trên ứng dụng và trang web để hoàn thành.**

Mika làm việc trên màn hình ảo chạy nền. Trong lúc đó, bạn vẫn sử dụng điện thoại như bình thường.

**[Tải APK Mika tiếng Việt (bản Preview)](https://github.com/dung997tb/Mika/releases)** · **[Xem bản dịch trong mã nguồn](https://github.com/dung997tb/Mika/tree/feat/vietnamese-localization/app/src/main/res/values-vi)**

[English](../../README.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-Hant.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · **Tiếng Việt**

> Bản Việt hóa này do cộng đồng thực hiện trên fork `dung997tb/Mika`, **không phải bản phát hành chính thức của tác giả**. APK Preview được ký bằng khóa debug và có thể không cài đè lên bản chính thức; hãy sao lưu trước khi gỡ hoặc thay ứng dụng.

<br/>

<img src="../media/wechat-send-side.gif" alt="Mika thao tác WeChat trên màn hình nền theo yêu cầu của người dùng" width="640" />

<sub>Bên trái là cuộc trò chuyện với Mika; bên phải là các thao tác Mika thực hiện trên màn hình nền (video tăng tốc 4 lần).</sub>

</div>

## Mika có thể làm gì?

Mika có thể thực hiện các yêu cầu gồm nhiều bước bằng cách nhìn màn hình, xác định phần tử rồi chạm, nhập và cuộn giống người dùng. Ví dụ:

- “Mở WhatsApp, tóm tắt tin nhắn chưa đọc hôm nay và cho biết tin nào cần trả lời.”
- “Tìm ba mẫu tai nghe không dây dưới 100 USD, so sánh ưu nhược điểm.”
- “Đặt báo thức lúc 9:40 và 10:00 sáng mai.”
- “Mở ứng dụng, tìm tài khoản cụ thể rồi theo dõi.”

| Tính năng | Mô tả |
|---|---|
| **Điều khiển ứng dụng** | Thao tác trên màn hình ảo độc lập, không chiếm màn hình chính. Khi gặp đăng nhập, xác minh hay thanh toán, Mika có thể yêu cầu bạn tiếp quản. |
| **Trình duyệt tích hợp** | Đọc nội dung website, tìm kiếm, so sánh, tải lên và tải xuống tệp; có thể dùng các phiên đã đăng nhập. |
| **Hiểu màn hình hiện tại** | Gửi ảnh màn hình cho Mika qua thanh nổi để hỏi cách phản hồi hoặc giao tác vụ liên quan. |
| **Lập lịch** | Nhắc việc và chạy tác vụ hằng ngày, hằng tuần hoặc theo điều kiện. |
| **Tương tác khi đang chạy** | Bổ sung, sửa yêu cầu, tạm dừng hoặc dừng; Mika ghi lại những bước đã thực hiện. |
| **Giọng nói** | Nhấn giữ để nói, chuyển thành văn bản rồi chỉnh sửa hoặc gửi. |
| **Tệp và tính toán** | Dùng môi trường Linux sandbox cho Python, Node và shell; một số tính năng này cần chip ARM 64-bit. |
| **Kết nối máy tính** | Nhận yêu cầu từ công cụ AI trên máy tính thông qua CLI, Skill hoặc MCP. |
| **Bộ nhớ và kỹ năng** | Ghi nhớ tùy chọn, tích lũy các quy trình đã thành công để hỗ trợ những tác vụ về sau. |

Mika không bị giới hạn trong những ứng dụng có sẵn trong các video minh họa: khả năng sử dụng còn tùy thuộc quyền truy cập, giao diện ứng dụng, mô hình AI được kết nối và các hạn chế bảo mật của hệ thống.

## Cài đặt và bắt đầu

1. **Tải APK:** mở [GitHub Releases của fork](https://github.com/dung997tb/Mika/releases), chọn bản `Mika Tiếng Việt Preview` mới nhất rồi tải tệp `Mika-vi-preview-debug.apk`. Đối chiếu checksum với `SHA256SUMS.txt` nếu cần.
2. **Chọn tiếng Việt:** trong Mika, vào **Cài đặt → Ngôn ngữ & giao diện → Tiếng Việt**. Trên Android 13 trở lên, bạn cũng có thể chọn ngôn ngữ riêng của ứng dụng trong cài đặt hệ thống.
3. **Kết nối mô hình AI:** vào **Cài đặt → Mô hình AI**, thêm nhà cung cấp và khóa API hoặc chọn hình thức đăng nhập mà Mika hỗ trợ. Mô hình chính cần hỗ trợ gọi công cụ để thực hiện tác vụ.
4. **Thiết lập điều khiển điện thoại (nếu cần):** làm theo trình hướng dẫn **Điều khiển điện thoại** và ghép nối Gỡ lỗi không dây một lần. Nếu chỉ dùng chat, web và xử lý tệp thì có thể bỏ qua bước này.

**Lưu ý khi cài đặt:** APK Preview dùng khóa ký debug của GitHub Actions. Khóa này không trùng với bản chính thức và có thể thay đổi giữa các lần build. Vì vậy, không nên coi đây là kênh cập nhật không mất dữ liệu; hãy sao lưu các thông tin cần thiết trước khi gỡ bản cũ. Không cần root để dùng các tính năng thông thường.

## Yêu cầu thiết bị

| Tính năng | Yêu cầu |
|---|---|
| Chat, duyệt web, xử lý tệp | Android 11 trở lên |
| Điều khiển ứng dụng trên màn hình ảo | Android 12 trở lên; **khuyến nghị Android 14+** |
| Linux sandbox | Thiết bị ARM64 |

Nếu chưa chắc thiết bị tương thích, hãy vào **Cài đặt → Khôi phục & sửa chữa → Tự kiểm tra khả năng tương thích**. Mika sẽ chạy các bài kiểm tra mà không thao tác trên ứng dụng khác.

## Riêng tư và an toàn

- Mika không có máy chủ riêng để nhận dữ liệu cuộc trò chuyện. Nội dung người dùng gửi, dữ liệu màn hình và ảnh chụp có thể được chuyển tới nhà cung cấp mô hình AI mà bạn cấu hình.
- Khóa API và bộ nhớ được mã hóa trên điện thoại. Các cuộc trò chuyện và bản ghi thực thi được lưu cục bộ.
- Các thao tác chi tiền cần bạn xác nhận ở chế độ mặc định. **Chế độ Tự chủ** thay đổi hành vi này, vì vậy hãy cân nhắc kỹ trước khi bật.
- Tự động thao tác ứng dụng bên thứ ba có thể chịu giới hạn hoặc điều khoản sử dụng của chính ứng dụng đó. Với tác vụ quan trọng, hãy kiểm tra kết quả.

Xem thêm [tài liệu bảo mật và lưu ý sử dụng](../disclaimer.en.md).

## Câu hỏi thường gặp

**Có phải Mika chỉ hiểu tiếng Anh không?** Không. Giao diện có bản dịch tiếng Việt và bạn có thể giao tiếp bằng tiếng Việt nếu mô hình AI bạn kết nối hỗ trợ tiếng Việt. Dữ liệu kiến thức tích hợp của dự án có thể vẫn là tiếng Trung; việc Việt hóa không thay đổi toàn bộ dữ liệu chuyên môn đó.

**Gỡ lỗi không dây tự tắt?** Android có thể tắt tính năng sau khi đổi Wi-Fi hoặc khởi động lại. Làm theo hướng dẫn trong phần Điều khiển điện thoại để kết nối lại.

**Vì sao một số màn hình không đọc được?** Các màn hình có thông tin nhạy cảm như mật khẩu và thanh toán có thể chặn chụp ảnh. Khi đó Mika sẽ cần bạn tự thao tác.

**Có dùng mô hình chạy trên máy tính của mình được không?** Có. Chọn nhà cung cấp **Tùy chỉnh (Custom)** rồi nhập địa chỉ dịch vụ trong mạng nội bộ.

**Bản này có cập nhật trực tiếp từ Mika chính thức không?** Không chắc chắn. Do khác khóa ký debug và kênh phát hành, hãy sử dụng trang Releases của fork để tải bản phù hợp.

## Mã nguồn và đóng góp

- [Fork có tiếng Việt](https://github.com/dung997tb/Mika)
- [Repository của tác giả gốc](https://github.com/wangzan101/Mika)
- [Hướng dẫn cài đặt điện thoại](../setup-guide.en.md)
- [Tài liệu mô hình và đăng nhập](../models.en.md)
- [Đóng góp cho dự án](../../.github/CONTRIBUTING.md)

Mika được phát hành theo [giấy phép Apache-2.0](../../LICENSE).
