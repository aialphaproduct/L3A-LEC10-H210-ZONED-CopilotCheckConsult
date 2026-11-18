# PHÂN TÍCH CASE STUDY: SLIMME CHECK (AMSTERDAM, 2019–2024)

**Hành trình từ POC đến Pilot và lý do thất bại trước ngưỡng cửa Production**

## 1. Dòng thời gian (2019–2024): Mục tiêu ban đầu và báo cáo thực tế không khớp nhau

Tương tự như việc đối chiếu giữa thông cáo báo chí và hồ sơ IPO của Klarna, câu chuyện của Slimme Check lộ rõ khoảng cách giữa tuyên bố thiết kế ban đầu và báo cáo tổng kết (*Eindevaluatie*) sau khi va chạm với thực tế:

- **2019 – Cuối 2021 (Giai đoạn R&D / POC):** Thành phố Amsterdam dành 3 năm phát triển thuật toán Slimme Check nhằm hỗ trợ nhân viên sàng lọc các hồ sơ xin trợ cấp xã hội có dấu hiệu không hợp lệ. Cuối năm 2021, nhóm dự án trình bày mô hình trước Hội đồng công dân (*Participatieraad* - phụ trách Việc làm, Sự tham gia và Thu nhập).
- **Tháng 3/2022 (Cảnh báo đỏ đầu tiên):** Sau khi thảo luận, *Participatieraad* ra khuyến nghị chính thức yêu cầu dừng sử dụng thuật toán vì lo ngại xâm phạm quyền cơ bản của công dân mà không mang lại giá trị gia tăng đáng kể.
- **Cuối 2022 (Tinh chỉnh mô hình):** Thay vì dừng lại, nhóm R&D sử dụng phản hồi của hội đồng để loại bỏ một số biến số nhạy cảm trực tiếp khỏi thuật toán và chuẩn bị đưa ra chạy thử nghiệm.
- **Đầu tháng 4/2023 (Điểm quyết định – Gate 1):** Chính quyền Amsterdam quyết định bấm nút chạy Pilot trong 4 tháng (17/4/2023 – 31/8/2023) trên quy trình xét duyệt hồ sơ thực tế.
- **Ngày 2/11/2023 (Khuyến nghị từ chuyên gia độc lập):** Nhà nghiên cứu Hans de Zwart (Đại học Khoa học Ứng dụng Amsterdam - HvA), người được mời giám sát đạo đức của dự án, gửi báo cáo lên Hội đồng thành phố khuyên chấm dứt hoàn toàn Slimme Check, nhấn mạnh rủi ro áp dụng AI lên nhóm công dân yếu thế và hội chứng "tin mù quáng vào máy" (*automation bias*).
- **Ngày 14/12/2023 (Báo cáo tổng kết Pilot – Eindevaluatie):** Báo cáo nội bộ thừa nhận: dù thuật toán bắt trúng nhiều đơn sai phạm hơn cách làm thủ công, nhưng dữ liệu không đủ chất lượng để kết luận mô hình có thiên kiến (*bias*) hay không, đồng thời tính năng giải thích lý do gắn cờ lại gây bối rối cho nhân viên.
- **Tháng 2 – Tháng 3/2024 (Kết cục):** Dự án bị đình chỉ triển khai rộng rãi (Production).

## 2. Đọc thẻ Case Slimme Check: Đâu là bằng chứng, đâu là nhiễu?

Khi đọc đoạn giới thiệu dự án trên OpenResearch Amsterdam tại thời điểm chuẩn bị mở rộng mô hình, ta cần phân loại các dữ kiện theo 3 mức độ giống như bài tập thẻ Klarna:

| Dữ kiện trên thẻ Case Slimme Check | Phân loại | Giải thích / Lý do |
|---|---|---|
| "Sau 3 năm nghiên cứu & phát triển (R&D), có sự tham gia đóng góp của Hội đồng công dân (*Participatieraad*)" | NHIỄU / BỐI CẢNH | Nỗ lực đầu tư thời gian và việc mở hội thảo lấy ý kiến không trả lời được câu hỏi "thuật toán có an toàn và hiệu quả không". Thực tế, Hội đồng công dân đã khuyên dừng dự án từ tháng 3/2022. |
| "Thuật toán được thiết kế để hỗ trợ nhân viên (*support employees*), không tự động ra quyết định" | NHIỄU / BỐI CẢNH | Đây là cách định vị pháp lý để lách quy định cấm ra quyết định tự động. Nó không chứng minh được nhân viên sẽ giữ được sự độc lập khi thấy hồ sơ bị máy gắn cờ đỏ. |
| "Tỷ lệ phát hiện hồ sơ không hợp lệ trong kỳ Pilot (4–8/2023) cao hơn quy trình thủ công trước đó" | BẰNG CHỨNG | Đo lường được qua dữ liệu thực nghiệm của kỳ Pilot (tự công bố trong báo cáo 12/2023). Tuy nhiên, đây mới chỉ là chỉ số về "sản lượng bắt lỗi", chưa nói lên chi phí sai số. |
| "Thuật toán làm rõ và giải thích được (*transparent and explainable*) dữ liệu nào dẫn đến quyết định điều tra" | CẦN HỎI LẠI | Giải thích bằng cách nào và ai là người đọc hiểu nó? Thực tế khi vận hành, máy chỉ liệt kê "Top 3 đặc trưng (*features*)" có trọng số cao nhất, khiến nhân viên xét duyệt bị rối và không biết phải xác minh gì tiếp theo. |
| "Nhằm mục tiêu giảm thiên kiến (*aimed to reduce bias*) so với cách làm việc trước đây" | CẦN HỎI LẠI | "Mục tiêu" không phải là "kết quả đã kiểm chứng". Đến tháng 12/2023, báo cáo đánh giá thừa nhận dữ liệu thu thập được không đủ chất lượng để kết luận mô hình có phân biệt đối xử hay không. |
| "Khảo sát nhân viên: Top 3 lý do gắn cờ gây khó hiểu và không có tính định hướng điều tra" | BẰNG CHỨNG | Bằng chứng thực tế duy nhất về trải nghiệm của người dùng nội bộ (*caseworkers*) khi tích hợp mô hình vào luồng công việc hàng ngày. |

## 3. Ba câu hỏi đọc Case: Đã biết gì, Quyết gì, Vì sao?

### Câu 1: Đến điểm quyết định (Tháng 4/2023), ta đã biết gì và ai nói?

- **Nhóm phát triển nội bộ (WPI Amsterdam):** Tuyên bố đã dành 3 năm xây dựng mô hình có khả năng giải thích minh bạch, đã loại bỏ các biến số nhạy cảm trực tiếp sau khi nghe góp ý, và kỳ vọng tăng hiệu quả phát hiện gian lận.
- **Hội đồng công dân (*Participatieraad*):** Đã ra văn bản từ tháng 3/2022 khẳng định việc dùng thuật toán này xâm phạm quyền cơ bản của người dân và không tạo ra giá trị gia tăng rõ ràng, khuyên dừng dự án.
- **Bối cảnh xã hội Hà Lan:** Cả nước vừa trải qua chấn động chính trị từ bê bối trợ cấp trẻ em (*Toeslagenaffaire*), nơi các thuật toán đánh giá rủi ro đã đẩy hàng chục nghìn gia đình vô tội vào cảnh phá sản.

### Câu 3 (Đặt trước khi mở kết cục): Nếu là người ra quyết định lúc đó, bạn quyết gì?

#### Phương án A (Vẫn chạy Pilot trên hồ sơ thật)

Chấp nhận rủi ro chính trị để lấy dữ liệu thực tế kiểm chứng xem mô hình có thực sự tốt hơn con người không.

#### Phương án B (Chặn lại ở Gate 1 – Chưa chạy Pilot trực tiếp)

Tạm dừng việc đưa lên luồng hồ sơ thật. Yêu cầu nhóm R&D phải giải quyết xong 2 điều kiện tiên quyết:

1. Thiết lập bộ dữ liệu chuẩn để đo lường và kiểm toán thiên kiến (*Bias Audit*) một cách chặt chẽ.
2. Thử nghiệm giao diện giải thích (*Explainability UI*) với nhân viên nghiệp vụ trên hồ sơ giả lập để xem họ có hiểu "Top 3 lý do" của máy hay không.

### Câu 2 (Sau khi mở kết cục): Vì sao Slimme Check không thể đi từ POC lên Product?

Nhìn từ cấu trúc đánh giá Gate 1 (như trường hợp của Klarna):

#### Lập luận "Qua Gate 1"

Mô hình chỉ điểm các hồ sơ đáng ngờ nhạy hơn quy trình thủ công của chuyên viên thu nhập; không tự động cắt trợ cấp mà vẫn có người thật kiểm tra bước cuối.

#### Lập luận "Không qua Gate 1" (Lý do dự án bị khai tử)

1. **Ảo tưởng về Explainable AI (XAI) trong phòng Lab:** Ở giai đoạn POC, các kỹ sư dữ liệu cho rằng chỉ cần xuất ra 3 biến số có trọng số cao nhất dẫn tới điểm rủi ro là đạt chuẩn "minh bạch và giải thích được". Nhưng khi lên Product, nhân viên xét duyệt cần một giả thuyết nghiệp vụ có thể kiểm chứng (ví dụ: nghi ngờ khai thiếu thu nhập từ việc làm thêm), chứ không phải 3 con số thống kê rời rạc của mô hình học máy.
2. **Thiếu hạ tầng dữ liệu để kiểm toán thiên kiến (*Bias Audit*):** Nhóm dự án hứa hẹn "giảm bias", nhưng khi kết thúc Pilot vào tháng 12/2023, chính họ lại kết luận rằng chất lượng dữ liệu không đủ để tính toán xem mô hình có phân biệt đối xử hay không. Trong dịch vụ công, "không chứng minh được là vô tư" đồng nghĩa với "không được phép sử dụng".
3. **Không đặt trước ngưỡng dừng (*Kill-switch*) về đạo đức và pháp lý:** Dù Hội đồng công dân đã tuýt còi từ tháng 3/2022, dự án vẫn cố đi tiếp thêm gần 2 năm nữa trước khi đi đến cùng một kết luận từ chuyên gia độc lập Hans de Zwart (11/2023) rằng: chi phí đạo đức và nguy cơ định kiến tự động hóa (*automation bias*) lên nhóm người nghèo lớn hơn rất nhiều so với lợi ích tiết kiệm thời gian.
