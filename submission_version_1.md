Bùi Minh Ngọc - 2A202600354
---

## 1. Idea reframed
Original idea:
> Ứng dụng OCR vào số hóa dữ liệu và dữ liệu hóa thông minh cho cơ quan nhà nước.

Reframed as a product opportunity:
> Các cơ quan hành chính nhà nước cấp huyện, xã tại Việt Nam đang sở hữu hàng triệu trang hồ sơ giấy tích lũy qua nhiều thập kỷ nhưng phần lớn chưa được số hóa hoặc chỉ scan thành PDF không tìm kiếm được. Đề án 06 và Luật Chuyển đổi số yêu cầu "dữ liệu chạy thay cho dân" nhưng công cụ hiện tại chỉ dừng ở mức scan-to-PDF. Chúng tôi tin rằng một nền tảng OCR fine-tuned cho tài liệu hành chính tiếng Việt, kết hợp AI trích xuất metadata, sẽ giúp biến kho hồ sơ giấy thành cơ sở dữ liệu có cấu trúc phục vụ tra cứu và liên thông.

---

## 2. Customer / Segment Card
- **Segment name:** Cán bộ văn thư – lưu trữ và bộ phận một cửa tại UBND cấp huyện/xã
- **Operational context:** Mỗi đơn vị quản lý 10.000–100.000+ hồ sơ giấy, hàng ngày tiếp nhận 20–100 hồ sơ mới từ công dân
- **Recurring workflow:** Công dân nộp hồ sơ → cán bộ tra cứu hồ sơ cũ trong kho giấy → đối chiếu thủ công → nhập dữ liệu → lưu trữ bản giấy
- **Pain moment:** Khi công dân yêu cầu cấp lại/xác nhận giấy tờ, cán bộ phải lục tìm hồ sơ giấy trong kho — mất 30 phút đến nửa ngày
- **Why now:** Luật Chuyển đổi số 2025 và Đề án 06 tạo áp lực pháp lý buộc phải số hóa
- **Access path:** Qua Sở Nội vụ / Sở TT&TT các tỉnh, chương trình đào tạo chuyển đổi số, đấu thầu dự án CNTT công

One-sentence description:
> Cán bộ văn thư–lưu trữ tại UBND cấp huyện/xã phải tra cứu thủ công kho hồ sơ giấy hàng chục nghìn trang để phục vụ thủ tục hành chính, trong bối cảnh bị áp lực số hóa từ Đề án 06.

---

### Need #1 (priority)
- **Statement (JTBD):** When công dân yêu cầu xác nhận hoặc cấp lại giấy tờ, I want tìm kiếm hồ sơ gốc bằng thông tin (tên, CCCD, số hồ sơ) và nhận kết quả trong vài giây, so I can giải quyết thủ tục trong ngày thay vì hẹn dân quay lại.
- **Current workaround:** Lục tìm thủ công theo sổ đăng ký giấy, xác định vị trí vật lý trong kho
- **Pain signal:** Mất 30 phút – 4 giờ mỗi lần tra cứu, công dân phải quay lại nhiều lần
- **Evidence / proxy evidence:** Báo cáo Đề án 06 ghi nhận nhiều CSDL chuyên ngành chưa hoàn thành hoặc chưa kết nối đồng bộ
- **Why underserved:** Phần mềm một cửa hiện tại chỉ quản lý hồ sơ mới, không giải quyết được kho hồ sơ cũ dạng giấy

### Need #2
- **Statement (JTBD):** When tôi nhận chỉ thị số hóa kho hồ sơ theo Thông tư 05/2025, I want hệ thống tự động trích xuất metadata từ tài liệu scan, so I can hoàn thành số hóa hàng chục nghìn hồ sơ trong vài tháng thay vì vài năm.
- **Current workaround:** Thuê nhân viên nhập liệu thủ công, tốn 3–5 phút/hồ sơ
- **Pain signal:** Chi phí nhân công cao, tiến độ chậm, tỷ lệ sai sót 5–10%
- **Evidence / proxy evidence:** Thông tư 05/2025/TT-BNV quy định chi tiết quy trình số hóa tài liệu lưu trữ
- **Why underserved:** Chưa có giải pháp OCR nào được train đặc thù cho mẫu biểu hành chính Việt Nam

### Need #3 (optional)
- **Statement (JTBD):** When dữ liệu đã số hóa cần liên thông với CSDL quốc gia, I want hệ thống tự động chuẩn hóa theo đúng schema đích, so I can đẩy dữ liệu lên mà không kiểm tra thủ công từng record.
- **Current workaround:** Cán bộ CNTT so khớp thủ công giữa file Excel/PDF và CSDL đích
- **Pain signal:** Tốn nhiều tháng chỉ để "làm sạch" dữ liệu, trùng lặp gây lỗi khi kết nối
- **Evidence / proxy evidence:** Tình trạng thiếu chuẩn kỹ thuật thống nhất giữa các cơ quan dẫn đến phân mảnh dữ liệu
- **Why underserved:** Các phần mềm số hóa hiện tại không có module chuẩn hóa dữ liệu theo schema CSDL quốc gia

---

## 4. Strategy Statement
For cán bộ văn thư–lưu trữ và bộ phận một cửa tại UBND cấp huyện/xã
who struggle with việc tra cứu kho hồ sơ giấy và áp lực số hóa với nguồn nhân lực hạn chế,
our product helps them biến kho hồ sơ giấy thành cơ sở dữ liệu có cấu trúc, tìm kiếm được
through pipeline OCR fine-tuned cho tài liệu hành chính tiếng Việt + AI trích xuất metadata,
unlike các dự án số hóa thủ công (scan-to-PDF + nhập tay) hoặc tool OCR generic,
because we can leverage mô hình OCR được train trên mẫu biểu hành chính Việt Nam thực tế và domain knowledge về quy trình văn thư–lưu trữ.

---

## 5. Moat Hypothesis
**Moat mechanism:** domain-learning flywheel

If we deploy 50 times in government digitization contexts, the following improve:
1. Độ chính xác OCR cho từng loại mẫu biểu hành chính
2. Thư viện template mẫu biểu ngày càng mở rộng
3. Quy tắc chuẩn hóa dữ liệu chính xác hơn theo vùng miền

Why competitors cannot easily replicate this:
> Tập dữ liệu mẫu biểu hành chính Việt Nam qua nhiều giai đoạn là tài sản tích lũy đặc thù — không có trên thị trường mở, đối thủ quốc tế không có access.

---

## 6. Initial TAM / SAM / SOM view
| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | $200M–$400M/year | ~11.000 xã + ~700 huyện + 63 tỉnh, chi phí số hóa $20K–$50K/đơn vị | Low |
| SAM | $20M–$50M/year | Tập trung 15 tỉnh thành lớn nhất, 3.000–4.000 đơn vị | Low |
| SOM | $500K–$1.5M (12–24 tháng) | Pilot 5–10 đơn vị cấp huyện tại 2–3 tỉnh | Low–Med |

**Top 3 unknowns requiring further research:**
1. Quy trình đấu thầu CNTT công — chu kỳ bán hàng 6–18 tháng
2. Benchmark OCR accuracy trên tài liệu hành chính cũ (viết tay, giấy ố)
3. Mức độ sẵn sàng hạ tầng CNTT tại cấp xã vùng sâu vùng xa

**Judgment:**
- [x] Worth pursuing now
- [ ] Worth pursuing but not now (need to validate [...] first)
- [ ] Not worth pursuing as currently framed

---

## 7. Positioning Note (2 sentences)
**What we are:**
> Một nền tảng số hóa và dữ liệu hóa thông minh cho cơ quan nhà nước, biến kho hồ sơ giấy thành CSDL có cấu trúc bằng OCR và AI được thiết kế riêng cho tài liệu hành chính tiếng Việt.

**What we are not / not yet:**
> Chúng tôi không phải phần mềm một cửa điện tử, không phải giải pháp quản lý văn bản đi/đến, và chưa phục vụ khối tư nhân.

---

## 8. Self-assessment before Day 17
Trong 6 mắt xích (Idea → Customer → Need → Strategy → Moat → Market Size), mắt xích nào đang yếu nhất?

> Đang yếu nhất ở phần Market Size vì các con số TAM/SAM/SOM dựa nhiều trên assumptions, chưa có dữ liệu mở về chi tiêu CNTT công theo từng lĩnh vực.

Open questions tôi muốn khám phá thêm ở Day 17:
1. MVP nên bắt đầu với loại hồ sơ nào trước (hộ tịch? đất đai?) để có quick win?
2. Bán trực tiếp cho UBND hay partner với VNPT/Viettel?
3. Deploy on-premise hay dùng cloud chính phủ?
