# BÀI 1: Phân tích và Lựa chọn công cụ tối ưu

## 1. Đáp án lựa chọn

Phương án tối ưu nhất là: C.

## 2. Phân tích vì sao phương án C tối ưu

Phương án C là cách phân bổ công cụ hợp lý nhất vì mỗi công cụ được dùng đúng với phạm vi ngữ cảnh và tính chất công việc.

Với tác vụ viết tài liệu hướng dẫn sử dụng API, Web Chat như ChatGPT hoặc Claude phù hợp vì đây là công việc cần khả năng tổng hợp, diễn đạt, sắp xếp nội dung và lý giải bằng ngôn ngữ tự nhiên. Lập trình viên có thể cung cấp mô tả nghiệp vụ, endpoint, input, output và quy tắc xử lý để AI phác thảo tài liệu Markdown. Tác vụ này không nhất thiết phải đọc toàn bộ mã nguồn của repository nếu người dùng đã đưa đủ thông tin cần thiết.

Với tác vụ tái cấu trúc lớp dữ liệu Book trên nhiều tệp như Book.java, BookService.java, BookController.java và BookRepository.java, cần một trợ lý lập trình cấp cao có khả năng hiểu ngữ cảnh repository rộng. Việc refactor một đối tượng dữ liệu thường ảnh hưởng đến model, service, controller, repository, DTO, validation và test. Nếu chỉ sửa từng file riêng lẻ, nguy cơ lệch kiểu dữ liệu, lỗi biên dịch hoặc bỏ sót nơi phụ thuộc rất cao. Agentic hoặc repository-wide assistant phù hợp hơn vì nó có thể đọc, lập kế hoạch và cập nhật đồng bộ nhiều file trong cùng ngữ cảnh dự án.

Với tác vụ sửa lỗi cú pháp nhỏ tại một dòng đang mở, inline completion là lựa chọn năng suất cao nhất. Lỗi thiếu dấu chấm phẩy hoặc khai báo sai kiểu dữ liệu chỉ cần ngữ cảnh cục bộ quanh dòng hiện tại. Dùng Web Chat hay agent repository-wide cho lỗi này sẽ tạo thêm thao tác thừa, làm chậm tiến độ và tăng chuyển đổi ngữ cảnh không cần thiết.

Xét về quản lý context window, phương án C tránh việc đưa quá nhiều nội dung không cần thiết vào một công cụ duy nhất. Nội dung cần lập luận ngôn ngữ được đưa vào Web Chat, nội dung cần hiểu quan hệ nhiều file được giao cho assistant có khả năng đọc repository, còn lỗi cục bộ được xử lý ngay trong IDE. Cách này giảm copy-paste, giảm mất ngữ cảnh, giảm rủi ro AI không nhìn thấy file liên quan và tăng tốc độ lập trình.

Xét về context switching, phương án C cũng giảm việc lập trình viên phải liên tục rời IDE, sao chép mã nguồn sang trình duyệt, nhận kết quả rồi dán ngược lại. Càng ít chuyển đổi môi trường làm việc, lập trình viên càng giữ được dòng suy nghĩ và tránh lỗi do sao chép thiếu file, thiếu dòng hoặc dùng phiên bản mã nguồn cũ.

## 3. Nhược điểm của phương án A

Phương án A dùng Web Chat cho cả 3 tác vụ nên không tối ưu về ngữ cảnh và năng suất.

Thứ nhất, với refactor Book trên nhiều file, Web Chat không tự động thấy được cấu trúc repository, quan hệ phụ thuộc, import, test và các nơi sử dụng khác. Lập trình viên phải sao chép từng file vào chat, rất dễ thiếu thông tin hoặc đưa lên phiên bản đã cũ.

Thứ hai, việc copy-paste liên tục giữa IDE và Web Chat làm tăng context switching. Mỗi lần chuyển cửa sổ, lập trình viên phải tải nạp lại trạng thái công việc trong đầu, dễ mất tập trung và dễ tạo lỗi thủ công.

Thứ ba, nếu trong mã nguồn có thông tin nhạy cảm như API key, token, cấu hình database, việc dán trực tiếp lên Web Chat công cộng có thể gây rủi ro bảo mật.

Thứ tư, với lỗi cú pháp nhỏ tại một dòng, dùng Web Chat là quá nặng. Tác vụ này nên được xử lý ngay tại IDE bằng inline assistant hoặc chỉnh tay.

## 4. Nhược điểm của phương án B

Phương án B dùng inline code assistant cho cả 3 tác vụ cũng không phù hợp.

Inline assistant rất mạnh với hoàn thành mã cục bộ, sửa nhanh một dòng, gợi ý tên biến hoặc bổ sung một đoạn nhỏ. Tuy nhiên, nó thường không có đủ ngữ cảnh toàn bộ repository để đảm bảo refactor Book trên 4 file được đồng bộ chính xác. Nếu thay đổi cấu trúc Book mà không cập nhật đúng service, controller và repository, dự án có thể bị lỗi biên dịch hoặc lỗi logic.

Với tác vụ viết API Guide, inline assistant cũng không phải lựa chọn tốt nhất. Tài liệu API cần cấu trúc Markdown rõ ràng, mô tả nghiệp vụ, ví dụ request/response và giải thích cho thành viên trong nhóm. Công việc này cần khả năng tổng hợp ngôn ngữ và lập luận tài liệu nhiều hơn là gợi ý mã tại dòng hiện tại.

Do đó, phương án B làm giảm chất lượng ở các tác vụ cần ngữ cảnh rộng hoặc cần diễn đạt tài liệu, dù có thể nhanh với tác vụ Quick Fix.

## 5. Kết luận

Chọn phương án C vì đây là cách dùng đúng công cụ cho đúng phạm vi công việc:

- Web Chat cho tài liệu API.
- Agentic hoặc repository-wide assistant cho refactor nhiều file.
- Inline completion cho lỗi cú pháp nhỏ tại chỗ.

Cách phân bổ này quản lý context window tốt hơn, giảm context switching và tăng năng suất lập trình trong tình huống thời gian ngắn.
