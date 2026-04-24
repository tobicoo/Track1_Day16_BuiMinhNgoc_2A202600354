# Day 16 Submission — Bùi Minh Ngọc

## Members
- Bùi Minh Ngọc — Product Owner / Solo

---

## 1. Idea reframed

Original idea:
> Ứng dụng OCR vào số hóa dữ liệu và dữ liệu hóa thông minh cho cơ quan nhà nước.

Reframed as a product opportunity:
> Các cơ quan hành chính nhà nước cấp sở, huyện, xã tại Việt Nam đang sở hữu hàng triệu trang hồ sơ giấy tích lũy qua nhiều thập kỷ (hộ tịch, đất đai, hộ khẩu, giấy phép xây dựng…) — phần lớn chưa được số hóa hoặc chỉ scan thành PDF "chết" không tìm kiếm được. **Observed gap:** Đề án 06 và Luật Chuyển đổi số (có hiệu lực 01/07/2026) yêu cầu "dữ liệu chạy thay cho dân", nhưng công cụ số hóa hiện tại chỉ dừng ở mức scan-to-PDF, không trích xuất metadata, không liên kết được với CSDL quốc gia. **Founding belief:** Một nền tảng OCR fine-tuned cho tài liệu hành chính tiếng Việt, kết hợp AI tự động trích xuất và chuẩn hóa metadata theo đúng chuẩn dữ liệu nhà nước, sẽ giúp cơ quan hành chính biến kho hồ sơ giấy thành cơ sở dữ liệu có cấu trúc — phục vụ tra cứu, liên thông, và cắt giảm thủ tục hành chính.

---

## 2. Customer / Segment Card

- **Segment name:** Cán bộ văn thư – lưu trữ và bộ phận một cửa tại UBND cấp huyện/xã
- **Operational context:** Mỗi đơn vị quản lý 10.000–100.000+ hồ sơ giấy tích lũy (hộ tịch, đất đai, xây dựng, tư pháp). Hàng ngày tiếp nhận 20–100 hồ sơ mới từ công dân, cần tra cứu hồ sơ cũ để đối chiếu.
- **Recurring workflow:** Công dân nộp hồ sơ → cán bộ tra cứu hồ sơ liên quan trong kho giấy → đối chiếu thủ công → nhập dữ liệu vào phần mềm một cửa → lưu trữ bản giấy theo thứ tự vật lý.
- **Pain moment:** Khi công dân yêu cầu cấp lại/xác nhận giấy tờ (xác nhận tình trạng hôn nhân, sao y bản chính, xác nhận nguồn gốc đất…), cán bộ phải lục tìm hồ sơ giấy trong kho lưu trữ — mất 30 phút đến nửa ngày, đôi khi không tìm được do hồ sơ bị thất lạc hoặc hư hỏng.
- **Why now:** (1) Luật Chuyển đổi số 2025 quy định cán bộ sẽ bị xử lý nếu yêu cầu dân nộp giấy tờ đã được số hóa; (2) Thông tư 05/2025/TT-BNV quy định chi tiết quy trình số hóa tài liệu lưu trữ; (3) Đề án 06 đang chuyển trọng tâm từ hạ tầng sang khai thác giá trị dữ liệu — cần công cụ để biến hồ sơ giấy thành dữ liệu có cấu trúc.
- **Access path:** Qua Sở Nội vụ / Sở TT&TT các tỉnh (đơn vị triển khai chuyển đổi số), chương trình đào tạo chuyển đổi số cho cán bộ cấp huyện/xã, và đấu thầu dự án CNTT công.

One-sentence description:
> Cán bộ văn thư–lưu trữ và bộ phận một cửa tại UBND cấp huyện/xã, hàng ngày phải tra cứu thủ công kho hồ sơ giấy hàng chục nghìn trang để phục vụ thủ tục hành chính cho công dân, trong bối cảnh bị áp lực số hóa từ Đề án 06 và Luật Chuyển đổi số.

---

## 3. Need Map (2–3 needs)

### Need #1 (priority)
- **Statement (JTBD):** When công dân đến yêu cầu xác nhận hoặc cấp lại giấy tờ và tôi cần tra cứu hồ sơ gốc trong kho lưu trữ giấy hàng chục nghìn trang, I want tìm kiếm bằng thông tin (tên, CCCD, số hồ sơ, năm) và nhận kết quả trong vài giây, so I can giải quyết thủ tục trong ngày thay vì hẹn dân quay lại, giảm phiền hà và đúng quy định về thời hạn giải quyết hồ sơ.
- **Current workaround:** Lục tìm thủ công theo sổ đăng ký giấy (sổ cái) → xác định vị trí vật lý (tủ, ngăn, cặp) → lấy hồ sơ ra kiểm tra. Nếu sổ đăng ký bị mất hoặc ghi thiếu, phải tìm tuần tự từng cặp.
- **Pain signal:** Mất 30 phút – 4 giờ mỗi lần tra cứu. Công dân phải quay lại nhiều lần. Cán bộ bị áp lực vì quy định thời hạn giải quyết TTHC (thường 3–5 ngày làm việc).
- **Evidence / proxy evidence:** Báo cáo Đề án 06 (2025) ghi nhận nhiều CSDL chuyên ngành chưa hoàn thành xây dựng hoặc chưa kết nối đồng bộ. Thông tin từ báo Công an nhân dân cho thấy một số nhiệm vụ số hóa còn chậm, quá hạn tại nhiều bộ, ngành. (Proxy evidence — chưa có khảo sát định lượng thời gian tra cứu cụ thể tại cấp xã, cần field research.)
- **Why underserved:** Phần mềm một cửa điện tử hiện tại (VNPT iGate, Viettel...) quản lý hồ sơ **mới** nhập vào hệ thống, nhưng không giải quyết được kho hồ sơ **cũ** đã tồn tại dạng giấy. Các dự án số hóa thường chỉ scan-to-PDF mà không trích xuất dữ liệu có cấu trúc.

### Need #2
- **Statement (JTBD):** When tôi nhận chỉ thị phải số hóa kho hồ sơ lưu trữ theo Thông tư 05/2025, I want hệ thống tự động trích xuất metadata (họ tên, ngày sinh, số CCCD, loại hồ sơ, ngày lập) từ tài liệu scan thay vì nhập tay từng trường, so I can hoàn thành số hóa hàng chục nghìn hồ sơ trong vài tháng thay vì vài năm với nguồn nhân lực hạn chế.
- **Current workaround:** Thuê nhân viên hợp đồng nhập liệu thủ công từ bản scan. Tốn 3–5 phút/hồ sơ × 50.000 hồ sơ = ~4.000 giờ = ~2 năm với 1 người full-time.
- **Pain signal:** Chi phí nhân công cao, tiến độ chậm so với yêu cầu, tỷ lệ sai sót nhập tay 5–10% gây dữ liệu "bẩn" ngay từ đầu.
- **Evidence / proxy evidence:** Thông tư 05/2025/TT-BNV quy định chi tiết quy trình số hóa tài liệu lưu trữ — tạo áp lực pháp lý buộc phải số hóa. Báo cáo Kyanon Digital (2025) ghi nhận OCR + AI giảm 70% thời gian nhập liệu với độ chính xác 98–99% (cho tài liệu tiếng Anh/Trung — assumption: cần benchmark riêng cho tiếng Việt hành chính).
- **Why underserved:** Các dự án số hóa hiện tại thường sử dụng nhân công thủ công hoặc tool OCR generic không hiểu cấu trúc tài liệu hành chính Việt Nam (mẫu hộ tịch, sổ đỏ, giấy phép xây dựng…). Chưa có giải pháp OCR nào được train đặc thù cho các form/mẫu hành chính nhà nước Việt Nam.

### Need #3
- **Statement (JTBD):** When dữ liệu đã được số hóa và cần liên thông với CSDL quốc gia (dân cư, đất đai), I want hệ thống tự động chuẩn hóa dữ liệu theo đúng format/schema của CSDL đích và phát hiện xung đột dữ liệu, so I can đẩy dữ liệu lên hệ thống liên thông mà không cần kiểm tra thủ công từng record.
- **Current workaround:** Cán bộ CNTT so khớp thủ công giữa file Excel/PDF và CSDL đích, sửa format (tên, ngày tháng, địa chỉ) bằng tay.
- **Pain signal:** Tốn nhiều tháng chỉ để "làm sạch" dữ liệu trước khi đẩy lên hệ thống. Dữ liệu trùng lặp, xung đột gây lỗi khi kết nối CSDL quốc gia.
- **Evidence / proxy evidence:** Báo cáo chỉ ra tình trạng thiếu chuẩn kỹ thuật thống nhất và format dữ liệu chung giữa các cơ quan, dẫn đến phân mảnh dữ liệu và khó tích hợp. (Proxy evidence từ đánh giá của World Bank và VNU.)
- **Why underserved:** Các phần mềm số hóa hiện tại không có module chuẩn hóa dữ liệu theo schema CSDL quốc gia. Việc mapping/transform dữ liệu phải làm thủ công bởi đơn vị triển khai CNTT.

---

## 4. Strategy Statement

For cán bộ văn thư–lưu trữ và bộ phận một cửa tại UBND cấp huyện/xã
who struggle with việc tra cứu kho hồ sơ giấy tích lũy hàng chục nghìn trang và áp lực số hóa theo Đề án 06 + Luật Chuyển đổi số với nguồn nhân lực hạn chế,
our product helps them biến kho hồ sơ giấy thành cơ sở dữ liệu có cấu trúc, tìm kiếm được, và sẵn sàng liên thông với CSDL quốc gia,
through pipeline OCR fine-tuned cho tài liệu hành chính tiếng Việt + AI tự động trích xuất metadata theo đúng mẫu biểu nhà nước + module chuẩn hóa dữ liệu theo schema CSDL quốc gia,
unlike các dự án số hóa thủ công (scan-to-PDF + nhập tay) hoặc tool OCR generic không hiểu cấu trúc mẫu biểu hành chính Việt Nam,
because we can leverage (1) mô hình OCR được train trên tập dữ liệu mẫu biểu hành chính Việt Nam thực tế, (2) domain knowledge về quy trình văn thư–lưu trữ và chuẩn metadata nhà nước, (3) khả năng tích hợp với hệ thống một cửa điện tử và CSDL quốc gia hiện có.

---

## 5. Moat Hypothesis

**Moat mechanism:** Domain-learning flywheel + Workflow embedding

If we deploy 50+ lần tại các UBND cấp huyện/xã, the following improve:
1. **OCR accuracy tăng dần cho từng loại mẫu biểu:** Mỗi đợt triển khai, hệ thống học thêm các biến thể mẫu hộ tịch, sổ đỏ, giấy phép qua nhiều giai đoạn (mẫu cũ 1990s, mẫu mới 2020s) → nhận diện chính xác hơn mà không cần cấu hình lại.
2. **Thư viện template hành chính mở rộng:** Tích lũy được bộ template cho hàng trăm loại mẫu biểu hành chính khác nhau theo từng lĩnh vực (hộ tịch, đất đai, xây dựng, tư pháp) → đơn vị mới triển khai nhanh hơn, ít cần customize.
3. **Quy tắc chuẩn hóa dữ liệu chính xác hơn:** Hệ thống học được pattern địa chỉ, tên riêng, format ngày tháng đặc thù theo vùng miền → chuẩn hóa dữ liệu tự động chính xác hơn trước khi đẩy vào CSDL quốc gia.

Why competitors cannot easily replicate this:
> Tập dữ liệu mẫu biểu hành chính Việt Nam qua nhiều giai đoạn là tài sản tích lũy đặc thù — không có trên thị trường mở, đối thủ quốc tế không có access. Khi hệ thống đã được tích hợp vào quy trình một cửa điện tử và kết nối CSDL quốc gia tại một tỉnh, switching cost rất cao vì phải migrate toàn bộ dữ liệu đã số hóa và re-configure kết nối liên thông.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | $200M–$400M/year | ~11.000 đơn vị cấp xã + ~700 cấp huyện + ~63 cấp tỉnh + các Sở ban ngành. Chi phí số hóa trung bình $20K–$50K/đơn vị (bao gồm phần mềm, triển khai, bảo trì). Tham chiếu: ngân sách CNTT công Việt Nam tăng mạnh theo Chương trình CĐSQG. | Low |
| SAM | $20M–$50M/year | Tập trung UBND cấp huyện/xã tại 15 tỉnh thành lớn nhất (HCM, HN, ĐN, HP, CT…) — khoảng 3.000–4.000 đơn vị. Pricing SaaS: $400–$1.000/đơn vị/tháng hoặc theo dự án $10K–$30K/đơn vị. | Low–Med |
| SOM | $500K–$1.5M (12–24 tháng) | Mục tiêu pilot 5–10 đơn vị cấp huyện tại 2–3 tỉnh, qua kênh Sở Nội vụ/TT&TT. Contract trung bình $50K–$150K/đơn vị (bao gồm triển khai + 1 năm vận hành). | Low–Med |

**Top 3 unknowns requiring further research:**
1. **Quy trình đấu thầu CNTT công** — chu kỳ bán hàng cho nhà nước thường 6–18 tháng. Cần hiểu rõ quy trình phê duyệt ngân sách và đấu thầu để ước tính SOM chính xác hơn.
2. **Benchmark OCR accuracy trên tài liệu hành chính Việt Nam thực tế** — tài liệu cũ (viết tay, giấy ố, mực nhòe) có thể khiến accuracy thấp hơn nhiều so với 98–99% trên tài liệu in sạch.
3. **Mức độ sẵn sàng hạ tầng CNTT tại cấp xã** — nhiều xã vùng sâu vùng xa có thể thiếu máy scan, mạng, server, ảnh hưởng đến khả năng triển khai.

**Judgment:**
- [x] Worth pursuing now
- [ ] Worth pursuing but not now
- [ ] Not worth pursuing as currently framed

> **Lý do:** Áp lực pháp lý rõ ràng (Luật CĐS 2025, Thông tư 05/2025, Đề án 06), ngân sách nhà nước đang được phân bổ cho chuyển đổi số, và chưa có giải pháp OCR nào được thiết kế đặc thù cho mẫu biểu hành chính Việt Nam. Rủi ro chính: chu kỳ bán hàng dài và phụ thuộc ngân sách nhà nước.

---

## 7. Positioning Note (2 sentences)

**What we are:**
> Nền tảng số hóa và dữ liệu hóa thông minh cho cơ quan nhà nước — biến kho hồ sơ giấy thành cơ sở dữ liệu có cấu trúc, tìm kiếm được, và sẵn sàng liên thông CSDL quốc gia, bằng OCR và AI được thiết kế riêng cho tài liệu hành chính tiếng Việt.

**What we are not / not yet:**
> Chúng tôi không phải phần mềm một cửa điện tử (không thay VNPT iGate hay Viettel), không phải giải pháp quản lý văn bản đi/đến, và chưa phải nền tảng phục vụ khối tư nhân — giai đoạn đầu tập trung hoàn toàn vào kho hồ sơ lưu trữ của cơ quan hành chính nhà nước.

---

## 8. Self-assessment before Day 17

Trong 6 mắt xích (Idea → Customer → Need → Strategy → Moat → Market Size), mắt xích đang yếu nhất:

> **Market Size.** Các con số TAM/SAM/SOM dựa nhiều trên assumptions vì thị trường CNTT công không có dữ liệu mở về chi tiêu theo từng lĩnh vực. Đặc biệt, chu kỳ bán hàng B2G (business-to-government) rất khác B2B thông thường — cần hiểu rõ quy trình đấu thầu, phê duyệt ngân sách, và ảnh hưởng chính trị để ước tính SOM thực tế. Ngoài ra, chưa field research trực tiếp tại UBND cấp xã/huyện để validate pain và willingness.

Open questions tôi muốn khám phá thêm ở Day 17:
1. **MVP scope:** Bắt đầu với loại hồ sơ nào trước (hộ tịch? đất đai? tư pháp?) để có quick win và demo được giá trị nhanh nhất cho lãnh đạo Sở?
2. **Go-to-market cho B2G:** Bán trực tiếp cho UBND hay partner với VNPT/Viettel (đã có kênh phân phối sẵn) — trade-off giữa margin và tốc độ tiếp cận?
3. **On-premise vs Cloud:** Dữ liệu hành chính nhà nước có yêu cầu bảo mật cao — deploy on-premise (tăng trust nhưng tăng cost triển khai) hay dùng cloud chính phủ (nếu có)?
