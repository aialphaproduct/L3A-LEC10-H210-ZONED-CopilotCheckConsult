# AI Consult — Bối cảnh và bằng chứng

*Phần của Mỹ: cung cấp dữ kiện nền và bằng chứng để nhóm dùng khi thảo luận. Đây chưa phải quyết định cuối cùng của nhóm về việc nên tiếp tục hay dừng công cụ.*

## Bối cảnh

Consult là công cụ do Incubator for AI (i.AI) phát triển để hỗ trợ công chức phân tích câu trả lời tự do trong các cuộc tham vấn công chúng. Công cụ dùng AI để tìm chủ đề trong lượng lớn phản hồi và gắn một phản hồi với một hoặc nhiều chủ đề; mục tiêu là giảm thời gian phân loại thủ công để chuyên viên tập trung hơn vào diễn giải và insight.

Bài viết của i.AI ngày 14/05/2025 giới thiệu một đánh giá được thực hiện cùng Chính phủ Scotland, nhằm xem Consult có thể giúp phân tích tham vấn nhanh hơn mà vẫn duy trì chất lượng insight hay không. Các số liệu đánh giá dưới đây được trích từ hồ sơ minh bạch thuật toán của DSIT; không nên hiểu chúng là kết quả riêng của thử nghiệm tại Scotland.

## Cách công cụ hoạt động

Theo hồ sơ DSIT, pipeline gồm các bước chính:

1. Mở rộng câu hỏi tham vấn bằng ngữ cảnh liên quan.
2. Phân loại phản hồi theo mức đồng ý/không đồng ý.
3. Sinh chủ đề từ các nhóm phản hồi.
4. Gộp chủ đề trùng hoặc gần nghĩa, rồi chuẩn hóa cách diễn đạt.
5. Gắn phản hồi vào một hoặc nhiều chủ đề; kết quả được trình bày để chuyên viên xem xét.

Hồ sơ mô tả công cụ ở giai đoạn tiền triển khai, với số người dùng thử còn hạn chế. Công dân không trực tiếp tương tác với công cụ; Consult không tự ra quyết định chính sách. Chuyên viên phải kiểm tra kết quả và có thể sửa nhãn/chủ đề trước khi sử dụng trong báo cáo.

## Bằng chứng đánh giá được công bố

Hồ sơ DSIT mô tả phép so sánh trên dữ liệu tham vấn: hai cố vấn chính sách gắn nhãn 200 phản hồi cho mỗi câu hỏi trong 3 câu hỏi; một cố vấn cấp cao cung cấp nhãn tham chiếu. Các chỉ số được báo cáo gồm:

| Khía cạnh | Kết quả được công bố | Cách đọc thận trọng |
|---|---|---|
| Mức liên quan của phản hồi | AI đồng thuận với nhãn tham chiếu khoảng 95%; AI có xu hướng đánh dấu “liên quan” rộng hơn người gán nhãn. | Không đồng nghĩa với việc nội dung được hiểu đúng hoàn toàn. |
| Mức đồng ý/không đồng ý | AI đồng thuận khoảng 85%. | Đây là phân loại lập trường, không phải đánh giá chất lượng lập luận. |
| Gắn chủ đề | AI khớp nhãn tham chiếu 62%; hai người gán nhãn đạt 70–73% so với tham chiếu. Người gán nhãn cũng chỉ đồng thuận với nhau 62%. | Chỉ số khớp cứng có thể bỏ qua trường hợp một phản hồi mang nhiều chủ đề hoặc khớp một phần. Theo hồ sơ, AI kém hơn một người và gần với người còn lại. |
| Thời gian và chi phí | Trên mẫu được thử, 3 phút so với 6 giờ; hồ sơ ước tính Consult nhanh hơn hơn 120 lần và rẻ hơn 400 lần. | Đây là kết quả của mẫu/thiết lập đánh giá được mô tả, không đảm bảo mọi tham vấn có cùng mức tiết kiệm. |
| Lỗi thao tác | Người gán nhãn mắc 29 lỗi trên 1.200 lượt gán (gần 2,5%); hồ sơ ghi nhận công cụ không mắc lỗi thao tác trong phép thử này. | Không nên suy rộng thành “AI không mắc lỗi phân tích”; sai chủ đề và lỗi thao tác là hai loại vấn đề khác nhau. |

## Rủi ro và giới hạn cần mang vào thảo luận

- Gắn chủ đề là phần khó hơn: điểm AI thấp hơn người gán nhãn tốt nhất; chủ đề có thể mơ hồ hoặc cần kiến thức chuyên môn để diễn giải.
- Mô hình nền là GPT-4o qua Azure OpenAI. Hồ sơ nêu rủi ro thiên lệch, tính khó giải thích của mô hình độc quyền, thuật ngữ chuyên ngành và câu hỏi pháp lý/quy trình.
- Biện pháp kiểm soát được mô tả gồm chuyên viên rà soát, chỉnh sửa đầu ra, bổ sung ngữ cảnh tham vấn và phối hợp với chuyên gia lĩnh vực.
- Hồ sơ không cho biết số lượng dữ liệu cụ thể; kết quả về thời gian/chi phí không tự chứng minh rằng kết luận chính sách sẽ tốt hơn.

## Gợi ý dùng bằng chứng

Điểm mạnh có bằng chứng là tốc độ và chi phí trên mẫu thử; bằng chứng về chất lượng chủ đề có kết quả pha trộn và vẫn cần con người kiểm tra. Khi nhóm chọn hướng ở Câu 3, nên cân nhắc riêng lợi ích năng suất, độ tin cậy của insight và mức độ giám sát cần thiết; phần quyết định là của nhóm.

## Nguồn

1. i.AI, [“Evaluating Consult: An AI Tool for Enhanced Public Consultation Analysis”](https://ai.gov.uk/blogs/evaluating-consult-an-ai-tool-for-enhanced-public-consultation-analysis/), 14/05/2025. Bài viết giới thiệu đánh giá cùng Chính phủ Scotland.
2. DSIT, [Algorithmic Transparency Record: Consult](https://www.gov.uk/algorithmic-transparency-records/dsit-consult), công bố 14/05/2025. Nguồn cho mô tả pipeline, giai đoạn triển khai, người giám sát, chỉ số đánh giá và rủi ro.
