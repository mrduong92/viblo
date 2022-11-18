# Tìm hiểu về WebRTC

## WebRTC là gì?
WebRTC (Web Realtime Communication) là WebRTC là một bộ API JavaScript cho phép chúng tôi thiết lập kết nối ngang hàng giữa hai trình duyệt (peer to peer connection) để trao đổi dữ liệu như âm thanh và video, cho phép chúng ta tạo các ứng dụng có tính năng gọi âm thanh và video.

Điều làm cho WebRTC trở nên đặc biệt là sau khi kết nối được thiết lập, dữ liệu có thể được truyền trực tiếp giữa các trình duyệt trong thời gian thực mà không cần sử dụng server. Bằng cách này, chúng ta có thể giảm độ trễ do dữ liệu không phải chuyển đến máy chủ trước, điều này làm cho webRTC trở nên tuyệt vời để trao đổi âm thanh và video.
WebRTC được duy trì bởi nhóm **Google Webrtc** dưới sự hỗ trợ của Apple, Google, Microsoft và Mozilla cùng những ông lớn trong lĩnh vực công nghệ khác.

## WebRTC có thể làm gì?
Tính năng nổi bật nhất của WebRTC là khả năng truyền tải video, âm thanh, dữ liệu. Hoạt động trao đổi giữa hai hay nhiều thiết bị diễn ra trong thời gian thực. Quá trình cũng không cần các bên trung gian hay cài đặt Plugin bổ sung.
Ngoài ra, tính ứng dụng còn được thấy trong việc tạo ra các tựa game trên trình duyệt. Nhờ đó, trải nghiệm của người chơi và sự thao tác trở nên thuận tiện, thú vị hơn rất nhiều.

- Dùng được cho cả trang web có đuôi HTML và PHP do khả năng hỗ trợ đa nền tảng và đa ngôn ngữ. 

- Hỗ trợ cho native app.

- Cho phép chia sẻ màn hình, bạn hoàn toàn có thể tích hợp tính năng này trong ứng dụng. 

- Cho phép người dùng nhắn tin trong lúc đang gọi video trực tuyến. 

## Ưu, nhược điểm
### Ưu điểm
- Hình thức mã nguồn mở miễn phí:
Google cho biết đây là công cụ truyền thông thời gian thực hoàn toàn không mất phí. Bạn luôn thấy sự xuất hiện sẵn sàng trên mọi trình duyệt.
- **Hỗ trợ trên đa nền tảng khác nhau:** Dù vẫn đang trong giai đoạn phát triển nhưng khả năng hoạt động tốt trên mọi trình duyệt, hệ điều hành. Điều này còn cho phép developer viết các đoạn HTML làm việc với máy tính, thiết bị di động.

- **Bảo mật âm thanh và video:** WebRTC sử dụng giao thức SRTP (Secure Real-Time Transport Protocol). Mục đích để mã hóa và xác thực dữ liệu Media.Trong quá trình thực hiện tác vụ video hay voice đảm bảo chống lại hoạt động nghe trộm.

- **Không cần Plugin hoặc phần mềm hỗ trợ:** Điều này là quá rõ ràng ngay từ khi bạn bắt đầu tìm hiểu. Công cụ được đánh giá cao về khả năng linh hoạt. Nhờ đó, người dùng có trải nghiệm tiện lợi, tối ưu tốc độ, tiết kiệm chi phí,…

- **Dễ sử dụng:** WebRTC được tích hợp trong các hàng loạt dịch vụ web bằng cách dùng JavaScript APIs, các Framework có sẵn.

- **Dùng băng thông hiệu quả:** WebRTC sử dụng băng thông hiệu quả, hoạt động tốt trong mọi điều kiện đường truyền mạng.
- **Ưu điểm khác:** Viết bằng JavaScripts nên dễ dàng tiếp cận và sử dụng. hoàn toàn miễn phí, bảo mật cao…

### Nhược điểm
- WebRTC có thể bị ngăn cản bởi NAT và và tường lửa khi cố gắng thực hiện kết nối P2P.
- Không có cơ chế báo hiệu cài sẵn khi ứng dụng tạo kết nối P2P giữa các trình duyệt.
- Chưa chính thức đi vào hoàn thiện, trong số đó có IE, Safari chưa thực sự được hỗ trợ tốt nhất.
- Giữa các trình duyệt thiếu tính thống nhất được chuẩn chất lượng video.
- Số lượng hàm API cho mỗi trình duyệt là khác nhau, tăng rủi ro phát sinh lỗi.

## WebRTC Vs WebSockets
Trước khi chúng ta nói về cách thức hoạt động của tất cả những thứ này, hãy so sánh WebRTC và WebSockets vì tôi biết nhiều bạn đang nghĩ "cái này nghe rất giống WebSockets, vậy tại sao chúng ta lại cần WebRTC?" và ngược lại.

![how-does-webrtc-work-2-1024x449](https://user-images.githubusercontent.com/26781288/202675118-be7bb674-b6f4-4f32-80e2-427cecf10344.jpg)
Với websockets, chúng ta cũng có thể thiết lập kết nối giữa các peer để trao đổi dữ liệu trong thời gian thực, nhưng kết nối này là giữa client và server.
Vì vậy, nếu chúng gửi tin nhắn đến một máy ngang hàng (peer) khác, trước tiên tin nhắn sẽ đến server, sau đó server sẽ gửi tin nhắn đó đến máy ngang hàng (peer) khác.
Quá trình trao đổi này thường diễn ra rất nhanh nên mặc dù có một số độ trễ, bạn có thể thậm chí sẽ không nhận thấy điều đó nếu bạn đang gửi nội dung nào đó như tin nhắn trò chuyện hoặc một số loại thông báo (notification).

Bây giờ, giả sử chúng ta muốn trao đổi một số âm thanh hoặc video bằng cách sử dụng websockets, khi mà tất cả điều này là có thể.
Vấn đề ở đây là ngay cả khi độ trễ nhỏ nhất khi nói đến âm thanh và video cũng có thể rất đáng chú ý và gây ra nhiều vấn đề. Vì vậy, vào thời điểm dữ liệu video của bạn đến server và quay lại máy peer của bạn, bạn sẽ thấy độ trễ đáng kể.

Đó là lúc WebRTC có ý nghĩa. Bằng cách thiết lập kết nối và trao đổi dữ liệu giữa hai trình duyệt, chúng tôi không thấy bất kỳ độ trễ nào từ phía server.
WebRTC cũng sử dụng giao thức UDP (User Datagram Protocol) rất phù hợp để truyền dữ liệu cực nhanh và hơn thế nữa trong giây lát.

## WebRTC hoạt động thế nào?
Mạng peer to peer (P2P) - mạng ngang hàng/đồng đẳng là một kiến trúc ứng dụng phân tán nhằm phân vùng nhiệm vụ hoặc khối lượng công việc giữa các peer. Các peer là những thiết bị tham gia trong ứng dụng có đặc quyền như nhau. Chúng tạo thành một mạng lưới các node ngang hàng.
Trong WebRTC, kết nối peer–to–peer được tạo ra, đại diện bởi interface RTCPeerConnection. 

![how-does-webrtc-work-3](https://user-images.githubusercontent.com/26781288/202676883-81106de7-5004-4da4-a5f8-08a92b333c53.gif)

Ở góc độ cấp cao, để thiết lập kết nối, ngang hàng 1 sẽ gửi một loại tin nhắn nào đó đến ngang hàng 2 nói rằng “này, tôi muốn kết nối với bạn, đây là một số thông tin về tôi và cách bạn có thể kết nối với tôi, bạn có chấp nhận không lời đề nghị?"
Đây có thể là một email, một tweet hoặc bạn có thể báo hiệu nó cho peer 2, điều đó tùy thuộc vào bạn.
Khi peer 2 nhận được thông tin này từ peer 1, họ có cơ hội chấp nhận kết nối. Nếu peer 2 chấp nhận, họ sẽ thu thập một số thông tin về mạng của họ và cách kết nối với mạng, sau đó gửi thông tin này lại cho peer 1.
Khi cả hai peer có thông tin của nhau, họ được kết nối và có thể bắt đầu trao đổi dữ liệu âm thanh và video hoặc bất kỳ thứ gì khác mà họ muốn gửi trực tiếp giữa các trình duyệt của họ mà không cần máy chủ nữa.

## Ứng dụng Video Chat bằng Firebase
Sẽ trình bày chi tiết trong seminar quý.
