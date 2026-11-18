# Zone D / AI Consult: phân tích case i.AI và quyết định nhóm

## 1. Câu 1: Chuyện gì đã xảy ra đến lúc này? Bằng chứng nào, ai đưa ra?

### Diễn biến

[i.AI](https://ai.gov.uk/) (Incubator for AI, thuộc Bộ Khoa học, Đổi mới và Công nghệ Anh) phát triển [Consult](https://ai.gov.uk/projects/consult/) để hỗ trợ phân tích phản hồi tham vấn công chúng: xác định chủ đề chính rồi gắn một hoặc nhiều chủ đề cho từng câu trả lời.

Ngày 14/05/2025, i.AI công bố đánh giá cùng Chính phủ Scotland trên một cuộc tham vấn thực tế về quy định đối với các thủ thuật thẩm mỹ không phẫu thuật. Mục tiêu là xem liệu Consult có thể tăng tốc phân tích mà vẫn giữ được chất lượng insight hay không.

### Bằng chứng định lượng và định tính

- **Khớp chủ đề:** Consult khớp hoàn toàn với đánh giá chuyên gia ở khoảng 60% câu trả lời. Bài viết cũng nêu mức đồng thuận giữa hai chuyên gia là khoảng 62%. Đây là các mức gần nhau, nhưng không nên xem hai phép so sánh là cùng một thước đo.
- **F1 trung bình:** 0,76/1 khi tính cả các trường hợp khớp một phần, chẳng hạn khớp 3 trong 4 chủ đề.
- **Thứ hạng chủ đề:** Các chủ đề dịch chuyển trung bình dưới một vị trí; những chủ đề đứng đầu hầu như không đổi.
- **Thời gian rà soát:** Trung vị 23 giây mỗi câu trả lời; 77% câu trả lời được rà soát trong dưới một phút.
- **Chỉnh sửa của chuyên gia:** Trên 5.354 câu trả lời, chuyên gia thêm chủ đề 1.671 lần và xóa 763 lần. Nhãn “Khác” được chuyên gia dùng 793 lần so với 47 lần từ AI (xấp xỉ 17 lần).
- **Quy trình:** Việc chốt danh sách chủ đề ban đầu cần nhiều vòng lặp hơn dự kiến.

### Ai đưa ra bằng chứng?

Các số liệu trên được công bố trong bài đánh giá của i.AI, do Lucy Makinson (Trưởng bộ phận Tác động và Đánh giá tại i.AI) viết. Đánh giá kết hợp các phép đo định lượng với phỏng vấn người dùng là các chuyên gia phân tích tham gia thử nghiệm.

## 2. Câu 3: Quyết định trước khi mở kết cục

**Đề xuất để nhóm thống nhất:** Đi tiếp ở phạm vi hẹp hơn, có điều kiện.

**Lý do:** Thử nghiệm cho thấy tiềm năng tiết kiệm thời gian và F1 0,76, trong khi thứ hạng các chủ đề chính ít thay đổi; tuy nhiên, chuyên gia vẫn phải chỉnh sửa chủ đề đáng kể, nên cần tiếp tục thử nghiệm có giám sát thay vì mở rộng ngay không điều kiện.

## 3. Câu 2: Vì sao họ dừng lại, hoặc vì sao họ đi tiếp được?

i.AI cho biết sẽ tiếp tục phát triển Consult và thử nghiệm trên các cuộc tham vấn khác trong những tháng tiếp theo. Bằng chứng về tốc độ, F1 và thứ hạng chủ đề cho thấy công cụ có tiềm năng hỗ trợ chuyên viên, nhưng lượng chỉnh sửa của chuyên gia cũng cho thấy cần giữ con người trong quy trình.

Các hướng cải tiến được nêu gồm hoàn thiện trải nghiệm người dùng, hướng dẫn rõ hơn cách rà soát/chốt chủ đề, chuẩn hóa việc đối chiếu giữa hai chuyên gia trong đánh giá sau này và bổ sung công cụ để nhà hoạch định chính sách khai thác insight sâu hơn.

## 4. Sticky notes

### 2–3 tờ vàng — Điều còn thiếu

1. Cần chuẩn đối chiếu với hai chuyên gia độc lập trên cùng tập dữ liệu để đo độ đồng thuận ổn định hơn.
2. Cần hướng dẫn rõ cho bước tinh chỉnh và chốt danh sách chủ đề; thử nghiệm ghi nhận bước này mất nhiều vòng lặp.
3. Tần suất dùng nhãn “Khác” cao ở chuyên gia cho thấy cần xem lại cách thiết kế danh sách chủ đề và cách xử lý các câu trả lời chưa được bao phủ.

### 1 tờ xanh — Điều làm tốt

Consult kết hợp tự động hóa với quyền kiểm soát của con người: công cụ giúp tổng hợp và gợi ý chủ đề nhanh, còn chuyên gia có thể thêm, xóa hoặc sửa trước khi sử dụng kết quả.

## Nguồn

1. i.AI, [“Evaluating Consult: An AI Tool for Enhanced Public Consultation Analysis”](https://ai.gov.uk/blogs/evaluating-consult-an-ai-tool-for-enhanced-public-consultation-analysis/), 14/05/2025.
2. i.AI, [báo cáo đánh giá Consult cùng Chính phủ Scotland (PDF)](https://ai.gov.uk/docs/Scot_Gov_NSCP_Evaluation_Report.pdf).
3. DSIT, [Algorithmic Transparency Record: Consult](https://www.gov.uk/algorithmic-transparency-records/dsit-consult), dùng để xác nhận bối cảnh và quy trình human-in-the-loop của Consult.
