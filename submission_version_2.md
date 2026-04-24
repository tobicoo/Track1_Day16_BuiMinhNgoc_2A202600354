Bùi Minh Ngọc - 2A202600354
---

## 1. Idea reframed
Original idea:
> Ứng dụng OCR vào số hóa dữ liệu và dữ liệu hóa thông minh cho cơ quan nhà nước.

Reframed as a product opportunity:
> Các cơ quan hành chính nhà nước cấp sở, huyện, xã tại Việt Nam đang sở hữu hàng triệu trang hồ sơ giấy tích lũy qua nhiều thập kỷ (hộ tịch, đất đai, hộ khẩu, giấy phép xây dựng…) — phần lớn chưa được số hóa hoặc chỉ scan thành PDF "chết" không tìm kiếm được. **Observed gap:** Đề án 06 và Luật Chuyển đổi số (có hiệu lực 01/07/2026) yêu cầu "dữ liệu chạy thay cho dân", nhưng công cụ số hóa hiện tại chỉ dừng ở mức scan-to-PDF, không trích xuất metadata, không liên kết được với CSDL quốc gia. **Founding belief:** Một nền tảng OCR fine-tuned cho tài liệu hành chính tiếng Việt, kết hợp AI tự động trích xuất và chuẩn hóa metadata theo đúng chuẩn dữ liệu nhà nước, sẽ giúp cơ quan hành chính biến kho hồ sơ giấy thành cơ sở dữ liệu có cấu trúc — phục vụ tra cứu, liên thông, và cắt giảm thủ tục hành chính. Nếu làm tốt, sản phẩm không chỉ giảm tải vận hành mà còn trở thành lớp hạ tầng dữ liệu nền tảng cho toàn bộ chuyển đổi số cấp cơ sở.

---

## 2. Customer / Segment Card
- **Segment name:** Cán bộ văn thư – lưu trữ và bộ phận một cửa tại UBND cấp huyện/xã đang chịu áp lực số hóa theo Đề án 06
- **Operational context:** Mỗi đơn vị quản lý 10.000–100.000+ hồ sơ giấy tích lũy (hộ tịch, đất đai, xây dựng, tư pháp). Hàng ngày tiếp nhận 20–100 hồ sơ mới từ công dân, cần tra cứu hồ sơ cũ để đối chiếu. Nhân sự CNTT mỏng (thường 1–2 người kiêm nhiệm), ngân sách phụ thuộc phân bổ từ tỉnh.
- **Recurring workflow:** Công dân nộp hồ sơ → cán bộ tra cứu hồ sơ liên quan trong kho giấy (sổ cái → tủ → ngăn → cặp) → đối chiếu thủ công → nhập dữ liệu vào phần mềm một cửa → lưu trữ bản giấy theo thứ tự vật lý. Song song: nhận chỉ thị số hóa từ Sở Nội vụ → scan hồ sơ → nhập metadata thủ công → báo cáo tiến độ.
- **Pain moment:** Khi công dân yêu cầu cấp lại/xác nhận giấy tờ (xác nhận tình trạng hôn nhân, sao y bản chính, xác nhận nguồn gốc đất…), cán bộ phải lục tìm hồ sơ giấy trong kho lưu trữ — mất 30 phút đến nửa ngày, đôi khi không tìm được do hồ sơ bị thất lạc hoặc hư hỏng. Áp lực tăng khi có thanh tra hoặc deadline báo cáo số hóa.
- **Why now:** (1) Luật Chuyển đổi số 2025 quy định cán bộ sẽ bị xử lý nếu yêu cầu dân nộp giấy tờ đã được số hóa — tạo consequence pháp lý trực tiếp; (2) Thông tư 05/2025/TT-BNV quy định chi tiết quy trình số hóa tài liệu lưu trữ — tạo deadline cụ thể; (3) Đề án 06 đang chuyển trọng tâm từ hạ tầng sang khai thác giá trị dữ liệu; (4) Ngân sách CNTT công đang được phân bổ mạnh cho chuyển đổi số cấp cơ sở.
- **Access path:** Qua Sở Nội vụ / Sở TT&TT các tỉnh (đơn vị triển khai chuyển đổi số), chương trình đào tạo chuyển đổi số cho cán bộ cấp huyện/xã, đấu thầu dự án CNTT công, và quan hệ với các đơn vị tư vấn chuyển đổi số đã có hợp đồng với tỉnh.

One-sentence description:
> Cán bộ văn thư–lưu trữ và bộ phận một cửa tại UBND cấp huyện/xã, hàng ngày phải tra cứu thủ công kho hồ sơ giấy hàng chục nghìn trang để phục vụ thủ tục hành chính cho công dân, trong bối cảnh bị áp lực số hóa có deadline và consequence pháp lý từ Đề án 06 và Luật Chuyển đổi số.

---

### Need #1 (priority)
- **Statement (JTBD):** When công dân đến yêu cầu xác nhận hoặc cấp lại giấy tờ và tôi cần tra cứu hồ sơ gốc trong kho lưu trữ giấy hàng chục nghìn trang, I want tìm kiếm bằng thông tin (tên, CCCD, số hồ sơ, năm) và nhận kết quả trong vài giây, so I can giải quyết thủ tục trong ngày thay vì hẹn dân quay lại, giảm phiền hà và đúng quy định về thời hạn giải quyết hồ sơ.
- **Current workaround:** Lục tìm thủ công theo sổ đăng ký giấy (sổ cái) → xác định vị trí vật lý (tủ, ngăn, cặp) → lấy hồ sơ ra kiểm tra. Nếu sổ đăng ký bị mất hoặc ghi thiếu, phải tìm tuần tự từng cặp.
- **Pain signal:** Mất 30 phút – 4 giờ mỗi lần tra cứu. Công dân phải quay lại nhiều lần. Cán bộ bị áp lực vì quy định thời hạn giải quyết TTHC (thường 3–5 ngày làm việc). Có trường hợp hồ sơ không tìm được do thất lạc/hư hỏng → phải làm lại từ đầu.
- **Evidence / proxy evidence:** Báo cáo Đề án 06 (2025) ghi nhận nhiều CSDL chuyên ngành chưa hoàn thành xây dựng hoặc chưa kết nối đồng bộ. Thông tin từ báo Công an nhân dân cho thấy một số nhiệm vụ số hóa còn chậm, quá hạn tại nhiều bộ, ngành. **[Assumption cần validate]:** Chưa có khảo sát định lượng thời gian tra cứu cụ thể tại cấp xã — cần field research.
- **Why underserved:** Phần mềm một cửa điện tử hiện tại (VNPT iGate, Viettel...) quản lý hồ sơ **mới** nhập vào hệ thống, nhưng không giải quyết được kho hồ sơ **cũ** đã tồn tại dạng giấy. Các dự án số hóa thường chỉ scan-to-PDF mà không trích xuất dữ liệu có cấu trúc → PDF "chết" không tìm kiếm được.

### Need #2
- **Statement (JTBD):** When tôi nhận chỉ thị phải số hóa kho hồ sơ lưu trữ theo Thông tư 05/2025, I want hệ thống tự động trích xuất metadata (họ tên, ngày sinh, số CCCD, loại hồ sơ, ngày lập) từ tài liệu scan thay vì nhập tay từng trường, so I can hoàn thành số hóa hàng chục nghìn hồ sơ trong vài tháng thay vì vài năm với nguồn nhân lực hạn chế.
- **Current workaround:** Thuê nhân viên hợp đồng nhập liệu thủ công từ bản scan. Tốn 3–5 phút/hồ sơ × 50.000 hồ sơ = ~4.000 giờ = ~2 năm với 1 người full-time.
- **Pain signal:** Chi phí nhân công cao (ước tính 200–500 triệu VND cho 50.000 hồ sơ), tiến độ chậm so với yêu cầu deadline từ tỉnh, tỷ lệ sai sót nhập tay 5–10% gây dữ liệu "bẩn" ngay từ đầu — phải clean lại sau.
- **Evidence / proxy evidence:** **[Fact]** Thông tư 05/2025/TT-BNV quy định chi tiết quy trình số hóa tài liệu lưu trữ — tạo áp lực pháp lý buộc phải số hóa. **[Fact]** Báo cáo Kyanon Digital (2025) ghi nhận OCR + AI giảm 70% thời gian nhập liệu với độ chính xác 98–99% cho tài liệu in sạch. **[Assumption]** Cần benchmark riêng cho tài liệu hành chính tiếng Việt — tài liệu cũ viết tay, giấy ố có thể cho accuracy thấp hơn đáng kể.
- **Why underserved:** Các dự án số hóa hiện tại thường sử dụng nhân công thủ công hoặc tool OCR generic (Google Vision, Tesseract) không hiểu cấu trúc tài liệu hành chính Việt Nam (mẫu hộ tịch, sổ đỏ, giấy phép xây dựng…). Chưa có giải pháp OCR nào được train đặc thù cho các form/mẫu hành chính nhà nước Việt Nam qua nhiều giai đoạn (mẫu 1990s vs mẫu 2020s).

### Need #3 (optional)
- **Statement (JTBD):** When dữ liệu đã được số hóa và cần liên thông với CSDL quốc gia (dân cư, đất đai), I want hệ thống tự động chuẩn hóa dữ liệu theo đúng format/schema của CSDL đích và phát hiện xung đột dữ liệu, so I can đẩy dữ liệu lên hệ thống liên thông mà không cần kiểm tra thủ công từng record.
- **Current workaround:** Cán bộ CNTT so khớp thủ công giữa file Excel/PDF và CSDL đích, sửa format (tên, ngày tháng, địa chỉ) bằng tay.
- **Pain signal:** Tốn nhiều tháng chỉ để "làm sạch" dữ liệu trước khi đẩy lên hệ thống. Dữ liệu trùng lặp, xung đột gây lỗi khi kết nối CSDL quốc gia.
- **Evidence / proxy evidence:** **[Fact]** Báo cáo World Bank và VNU chỉ ra tình trạng thiếu chuẩn kỹ thuật thống nhất và format dữ liệu chung giữa các cơ quan. **[Unknown]** Chưa rõ schema CSDL quốc gia có API chuẩn hóa hay mỗi tỉnh tự quy định format riêng.
- **Why underserved:** Các phần mềm số hóa hiện tại không có module chuẩn hóa dữ liệu theo schema CSDL quốc gia. Việc mapping/transform dữ liệu phải làm thủ công bởi đơn vị triển khai CNTT — tạo bottleneck nghiêm trọng.

---

## 4. Strategy Statement
For cán bộ văn thư–lưu trữ và bộ phận một cửa tại UBND cấp huyện/xã đang chịu áp lực số hóa theo Đề án 06 và Luật Chuyển đổi số
who struggle with việc tra cứu kho hồ sơ giấy tích lũy hàng chục nghìn trang và phải hoàn thành số hóa trong thời hạn pháp lý với nguồn nhân lực hạn chế,
our product helps them biến kho hồ sơ giấy thành cơ sở dữ liệu có cấu trúc, tìm kiếm được trong vài giây, và sẵn sàng liên thông với CSDL quốc gia,
through pipeline OCR fine-tuned cho tài liệu hành chính tiếng Việt (bao gồm mẫu cũ viết tay) + AI tự động trích xuất metadata theo đúng mẫu biểu nhà nước + module chuẩn hóa dữ liệu theo schema CSDL quốc gia + giao diện tra cứu tích hợp vào quy trình một cửa,
unlike các dự án số hóa thủ công (scan-to-PDF + nhập tay tốn 2 năm cho 50.000 hồ sơ) hoặc tool OCR generic (Google Vision, Tesseract) không hiểu cấu trúc mẫu biểu hành chính Việt Nam,
because we can leverage (1) mô hình OCR được train trên tập dữ liệu mẫu biểu hành chính Việt Nam thực tế qua nhiều giai đoạn, (2) domain knowledge sâu về quy trình văn thư–lưu trữ và chuẩn metadata nhà nước, (3) khả năng tích hợp với hệ thống một cửa điện tử và CSDL quốc gia hiện có.

---

## 5. Moat Hypothesis
**Moat mechanism:** Domain-learning flywheel + Workflow embedding + Data compounding

If we deploy 50+ lần tại các UBND cấp huyện/xã, the following improve:
1. **OCR accuracy tăng dần cho từng loại mẫu biểu:** Mỗi đợt triển khai, hệ thống học thêm các biến thể mẫu hộ tịch, sổ đỏ, giấy phép qua nhiều giai đoạn (mẫu cũ 1990s, mẫu mới 2020s) → nhận diện chính xác hơn mà không cần cấu hình lại. Đây là data compounding — mỗi đơn vị mới đóng góp thêm vào bộ training data mà đối thủ không có.
2. **Thư viện template hành chính mở rộng:** Tích lũy được bộ template cho hàng trăm loại mẫu biểu hành chính khác nhau theo từng lĩnh vực (hộ tịch, đất đai, xây dựng, tư pháp) → đơn vị mới triển khai nhanh hơn, ít cần customize → giảm cost-to-serve, tăng margin.
3. **Quy tắc chuẩn hóa dữ liệu chính xác hơn:** Hệ thống học được pattern địa chỉ, tên riêng, format ngày tháng đặc thù theo vùng miền → chuẩn hóa dữ liệu tự động chính xác hơn trước khi đẩy vào CSDL quốc gia → giảm rejection rate khi liên thông.

Why competitors cannot easily replicate this:
> Tập dữ liệu mẫu biểu hành chính Việt Nam qua nhiều giai đoạn là tài sản tích lũy đặc thù — không có trên thị trường mở, đối thủ quốc tế (Google, AWS) không có access và không có incentive để build cho vertical nhỏ này. Khi hệ thống đã được tích hợp vào quy trình một cửa điện tử và kết nối CSDL quốc gia tại một tỉnh (workflow embedding), switching cost rất cao vì phải migrate toàn bộ dữ liệu đã số hóa, re-configure kết nối liên thông, và đào tạo lại cán bộ. Đối thủ nội địa có thể copy giao diện nhưng không thể copy bộ training data và domain knowledge tích lũy từ hàng chục đợt triển khai thực tế.

---

## 6. Initial TAM / SAM / SOM view
| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | $200M–$400M/year | **[Fact]** ~11.000 đơn vị cấp xã + ~700 cấp huyện + ~63 cấp tỉnh + các Sở ban ngành. **[Assumption]** Chi phí số hóa trung bình $20K–$50K/đơn vị (bao gồm phần mềm, triển khai, bảo trì). **[Fact]** Ngân sách CNTT công Việt Nam tăng mạnh theo Chương trình CĐSQG. | Low |
| SAM | $20M–$50M/year | **[Assumption]** Tập trung UBND cấp huyện/xã tại 15 tỉnh thành lớn nhất — khoảng 3.000–4.000 đơn vị. **[Assumption]** Pricing SaaS: $400–$1.000/đơn vị/tháng hoặc theo dự án $10K–$30K/đơn vị. | Low–Med |
| SOM | $500K–$1.5M (12–24 tháng) | **[Assumption]** Pilot 5–10 đơn vị cấp huyện tại 2–3 tỉnh, qua kênh Sở Nội vụ/TT&TT. **[Assumption]** Contract trung bình $50K–$150K/đơn vị (bao gồm triển khai + 1 năm vận hành). | Low–Med |

**Top 3 unknowns requiring further research:**
1. **Quy trình đấu thầu CNTT công** — chu kỳ bán hàng cho nhà nước thường 6–18 tháng. Cần hiểu rõ quy trình phê duyệt ngân sách và đấu thầu để ước tính SOM chính xác hơn.
2. **Benchmark OCR accuracy trên tài liệu hành chính Việt Nam thực tế** — tài liệu cũ (viết tay, giấy ố, mực nhòe) có thể khiến accuracy thấp hơn nhiều so với 98–99% trên tài liệu in sạch. Cần pilot thực tế để đo.
3. **Mức độ sẵn sàng hạ tầng CNTT tại cấp xã** — nhiều xã vùng sâu vùng xa có thể thiếu máy scan, mạng, server, ảnh hưởng đến khả năng triển khai và phải tính thêm chi phí hạ tầng.

**Judgment:**
- [x] Worth pursuing now
- [ ] Worth pursuing but not now
- [ ] Not worth pursuing as currently framed

> **Lý do:** Áp lực pháp lý rõ ràng với deadline và consequence (Luật CĐS 2025, Thông tư 05/2025, Đề án 06), ngân sách nhà nước đang được phân bổ cho chuyển đổi số, và chưa có giải pháp OCR nào được thiết kế đặc thù cho mẫu biểu hành chính Việt Nam. Rủi ro chính: chu kỳ bán hàng dài và phụ thuộc ngân sách nhà nước — nhưng đây là rủi ro về timing, không phải về product-market fit.

---

## 7. Positioning Note (2 sentences)
**What we are:**
> Nền tảng số hóa và dữ liệu hóa thông minh cho cơ quan nhà nước — biến kho hồ sơ giấy thành cơ sở dữ liệu có cấu trúc, tìm kiếm được, và sẵn sàng liên thông CSDL quốc gia, bằng OCR và AI được thiết kế riêng cho tài liệu hành chính tiếng Việt.

**What we are not / not yet:**
> Chúng tôi không phải phần mềm một cửa điện tử (không thay VNPT iGate hay Viettel), không phải giải pháp quản lý văn bản đi/đến, và chưa phải nền tảng phục vụ khối tư nhân — giai đoạn đầu tập trung hoàn toàn vào kho hồ sơ lưu trữ của cơ quan hành chính nhà nước.

---

## 8. Self-assessment before Day 17
Trong 6 mắt xích (Idea → Customer → Need → Strategy → Moat → Market Size), mắt xích nào đang yếu nhất?

> **Market Size** vẫn là mắt xích yếu nhất. So với version 1, đã phân tách rõ hơn facts vs assumptions, nhưng các con số TAM/SAM/SOM vẫn dựa nhiều trên ước lượng vì thị trường CNTT công không có dữ liệu mở về chi tiêu theo từng lĩnh vực. Đặc biệt, chu kỳ bán hàng B2G rất khác B2B thông thường — SOM phụ thuộc vào quy trình đấu thầu, phê duyệt ngân sách, và yếu tố chính trị mà chưa validate được. Ngoài ra, chưa field research trực tiếp tại UBND cấp xã/huyện để validate pain intensity và willingness to pay.

Open questions tôi muốn khám phá thêm ở Day 17:
1. **MVP scope:** Bắt đầu với loại hồ sơ nào trước (hộ tịch? đất đai? tư pháp?) để có quick win và demo được giá trị nhanh nhất cho lãnh đạo Sở? Trade-off giữa volume (hộ tịch nhiều nhất) và value (đất đai quan trọng nhất).
2. **Go-to-market cho B2G:** Bán trực tiếp cho UBND hay partner với VNPT/Viettel (đã có kênh phân phối sẵn) — trade-off giữa margin và tốc độ tiếp cận? Hay bắt đầu bằng pilot miễn phí để tạo case study?
3. **On-premise vs Cloud:** Dữ liệu hành chính nhà nước có yêu cầu bảo mật cao — deploy on-premise (tăng trust nhưng tăng cost triển khai) hay dùng cloud chính phủ (nếu có)? Ảnh hưởng thế nào đến scalability và unit economics?

---

## 9. Iteration Reflection (A → B)

### Những thay đổi chính từ Version 1 sang Version 2:

| Mắt xích | Version 1 (A) | Version 2 (B) | Lý do thay đổi |
|---|---|---|---|
| **Customer** | Mô tả chung về cán bộ văn thư | Thêm chi tiết về nhân sự CNTT mỏng, ngân sách phụ thuộc tỉnh, workflow song song (vừa phục vụ dân vừa số hóa) | Customer cần đủ sắc để hình dung được constraint thực tế |
| **Need** | Evidence chung chung | Phân tách rõ [Fact] vs [Assumption] vs [Unknown] cho mỗi evidence | Rubric yêu cầu research rigor — không được trộn lẫn facts và assumptions |
| **Strategy** | Liệt kê approach | Thêm so sánh định lượng với alternative (2 năm cho 50.000 hồ sơ) | Strategy phải cho thấy tại sao approach của mình tốt hơn status quo |
| **Moat** | Domain-learning flywheel | Thêm Data compounding + Workflow embedding, giải thích cơ chế cụ thể hơn | Moat cần nhiều lớp, không chỉ 1 cơ chế đơn lẻ |
| **Market** | Con số + assumptions | Gắn tag [Fact]/[Assumption] cho từng con số, thêm reasoning về rủi ro timing vs PMF | Market sizing có trách nhiệm = phân biệt rõ điều mình biết và điều mình đoán |

### Honest reflection:
> Điểm mạnh nhất của bài: Customer segment rất cụ thể (cán bộ văn thư cấp xã/huyện) với pain moment rõ ràng và áp lực pháp lý có deadline. Điểm yếu nhất: chưa có field research trực tiếp — toàn bộ evidence đều là proxy từ báo cáo và văn bản pháp luật, chưa nói chuyện với cán bộ thực tế. Day 17 cần ưu tiên validate pain intensity và willingness to pay bằng cách tiếp cận ít nhất 2–3 UBND cấp huyện.
