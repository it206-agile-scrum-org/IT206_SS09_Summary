# Inspect & Adapt Event Pack – ShopCare AI

*Scrum Team ShopCare AI · Cuối Sprint 14 → Sprint 15*

**Sprint Goal Sprint 15:** CSKH nhận hội thoại AI không xử lý trong 2 phút, kèm trạng thái đơn và lịch sử.

**Nguyên tắc xuyên suốt:** Review kiểm tra *sản phẩm* (Increment, Feedback → Product Backlog). Retro kiểm tra *cách làm việc* (Data → Action → Sprint 15). Hai sự kiện tách biệt, chỉ liên kết bằng bằng chứng.

---

## 1. Kiểm tra Increment và phần chưa Done

**Definition of Done:** (1) lên staging; (2) kiểm thử quan trọng đạt; (3) không còn lỗi cao; (4) đạt kiểm tra quyền riêng tư.

Ký hiệu: ✔ có bằng chứng đạt · ✘ có bằng chứng không đạt · ? dữ liệu không nêu (chưa có bằng chứng = chưa tính là đạt).

| Mã | Kiểm thử | Lỗi cao | Quyền riêng tư | Staging | Kết luận |
| --- | --- | --- | --- | --- | --- |
| SC-61 | ✔ 80/80 | ✔ không còn | ? | ? | **Done** (xác nhận 2 mục “?” trước Review) |
| SC-62 | ✘ 70/78 (89,7%), còn 8 ca lỗi dịch vụ đơn hàng | ? | ? | ? | **Chưa Done** |
| SC-63 | ✘ 74/80 ca đúng (92,5%) | ✘ còn 1 lỗi nghiêm trọng cao | ? | ? | **Chưa Done** |
| SC-64 | ✔ 60/60 kiểm thử chính | ? | ✘ đang chờ kiểm tra che SĐT | ? | **Chưa Done** |
| SC-65 | ✔ 42/42 | ? | ✔ đạt | ? | **Done** (xác nhận lỗi cao và staging trước Review) |

**Kết luận:** 2/5 hạng mục Done (SC-61, SC-65); 3/5 chưa Done (SC-62, SC-63, SC-64). Chỉ SC-61 và SC-65 được gọi là Increment.

**Cách trình bày phần chưa Done tại Review:**

- Nói rõ “chưa Done”, nêu đúng tiêu chí còn thiếu: SC-62 thiếu 8 ca kiểm thử; SC-63 còn 1 lỗi cao; SC-64 thiếu kiểm tra che SĐT.
- Có thể demo như *công việc đang làm* để lấy Feedback sớm, gắn nhãn rõ, không tính là hoàn thành và không đưa vào phát hành.
- Trả về Product Backlog để PO sắp xếp lại ưu tiên cho Sprint 15; không chia nhỏ hay tính một phần giá trị.

**Điểm sai của Review cũ và tác động:**

| # | Điểm sai | Tác động |
| --- | --- | --- |
| 1 | PO gọi cả SC-61 → SC-65 là Done dù 3 hạng mục không đạt DoD | Mất minh bạch; stakeholder tin Increment đủ chất lượng → rủi ro phát hành lỗi cao và lộ SĐT |
| 2 | Biến Review thành nghiệm thu một chiều | Không có trao đổi hai chiều; Feedback bị bỏ sót hoặc bị coi là yêu cầu bắt buộc |
| 3 | PO hứa làm mọi Feedback | Cam kết vượt năng lực, làm Sprint 15 quá tải, phá vai trò sắp xếp Backlog của PO và quyền chọn việc của Developers |

---

## 2. Thiết kế Sprint Review (60 phút)

**Mục tiêu:** kiểm tra Increment theo Done, thu Feedback hai chiều, cập nhật hướng Product Backlog. **Thành phần:** Scrum Team + stakeholder liên quan (CSKH, vận hành…). **Vai trò:** PO chủ trì nội dung sản phẩm; Developers demo và trả lời kỹ thuật; SM giữ timebox, đảm bảo hai chiều và ghi Feedback Log; stakeholder phản hồi.

| Phút | Nội dung | Phụ trách | Câu hỏi mở / trao đổi hai chiều |
| --- | --- | --- | --- |
| 0–5 | Mở đầu: Sprint Goal, mục tiêu Review, quy tắc “Feedback chưa là cam kết” | SM, PO | Mọi người kỳ vọng nhận được gì hôm nay? |
| 5–10 | Bảng Done: SC-61, SC-65 Done; SC-62/63/64 chưa Done và lý do | PO, Developers | Có bằng chứng nào chưa rõ về tiêu chí Done không? |
| 10–25 | Demo SC-61, SC-65; trình bày trạng thái SC-62/63/64 (nhãn “chưa Done”) | Developers | CSKH sẽ dùng bước này trong ca thật như thế nào? |
| 25–45 | Thảo luận và thu Feedback, ghi vào Feedback Log | Stakeholder, SM ghi | Với hội thoại AI không xử lý, CSKH cần thấy gì trong 2 phút đầu? Thiếu gì để xử lý ngay? |
| 45–55 | Ảnh hưởng đến Product Backlog: nhóm Feedback theo mục tiêu; stakeholder cho biết mức quan trọng | PO | Nếu chỉ làm được 1–2 việc, việc nào giúp CSKH nhiều nhất? |
| 55–60 | Tóm tắt: Feedback nào vào Backlog để PO cân nhắc (chưa cam kết); bước tiếp theo | PO, SM | Còn điều gì cần làm rõ trước Planning? |

### Feedback Log (F-01 → F-05)

*Nguồn là giả định từ nội dung Feedback; xác nhận lại tại Review. Trạng thái ban đầu của tất cả: “Ghi nhận – chưa cam kết”.*

| Mã | Nội dung | Nguồn (giả định) | Bằng chứng hiện có | Điểm cần làm rõ | Hướng xử lý |
| --- | --- | --- | --- | --- | --- |
| F-01 | Tự động hóa 90% | Quản lý/stakeholder kinh doanh | Dữ liệu chưa có tỷ lệ tự động hóa hiện tại (74/80 của SC-63 là độ đúng phân loại, không phải tỷ lệ tự động hóa) | “90%” tính trên tập nào, theo cách đo nào, hạn khi nào? | Làm rõ → PO đưa vào Backlog như mục tiêu, không đưa vào Sprint 15 khi chưa có số đo |
| F-02 | Chuyển sớm sang CSKH | CSKH | Liên quan trực tiếp Sprint Goal (2 phút) | “Sớm” = sau bao nhiêu lượt/điều kiện nào? | PO sắp xếp ưu tiên; ứng viên cho Sprint 15 |
| F-03 | Còn lộ SĐT | CSKH/bảo mật | Khớp SC-64: đang chờ kiểm tra che SĐT | Trường hợp nào còn lộ (kênh, định dạng)? | Gắn vào SC-64 chưa Done; ưu tiên cao vì ảnh hưởng quyền riêng tư |
| F-04 | Thiếu lịch sử | CSKH | Khớp vấn đề đầu Sprint 14 (thiếu lịch sử đa kênh) và Sprint Goal | Cần bao nhiêu lịch sử, từ kênh nào? | Ưu tiên cao; ứng viên chính của Sprint 15 (xem truy vết §5) |
| F-05 | Lệch P95 | Kỹ thuật/vận hành | Chưa có số P95 thực tế và ngưỡng mục tiêu trong dữ liệu | P95 của chỉ số nào, lệch bao nhiêu so với mục tiêu? | Thu số đo trước; sau đó PO quyết định ưu tiên |

**Trạng thái Feedback:** Ghi nhận → Đã làm rõ → Trong Backlog → Chọn vào Sprint (cam kết chỉ phát sinh ở bước này, tại Sprint Planning) → Đã kiểm tra → Đóng.

---

## 3. Thiết kế Sprint Retrospective (60 phút)

**Mục tiêu:** cải tiến cách làm việc của nhóm cho Sprint 15. **Thành phần:** chỉ Scrum Team (PO, SM, Developers); **không mời quản lý vận hành**. Diễn ra sau Review, SM điều phối. Feedback sản phẩm đã xử lý ở Review nên không bàn lại ở đây; Retro chỉ lấy *bằng chứng* từ Review.

| Phút | Giai đoạn | Nội dung |
| --- | --- | --- |
| 0–5 | Mở | Mục tiêu, quy tắc không đổ lỗi; chấm an toàn ẩn danh (1–5) |
| 5–15 | **Follow-up (rà Action cũ)** | Từng Action cũ: đã làm / chưa làm / bỏ. Action mơ hồ hoặc gán cho cá nhân → viết lại thành hành động cụ thể cho nhóm hoặc đóng |
| 15–30 | **Data** | Dữ kiện: 3/5 hạng mục chưa Done; staging Ngày 4, Integration Test Ngày 8; quy tắc đổi qua tin nhắn; an toàn 2,8/5 |
| 30–45 | **Insight** | Nhóm dữ kiện thành nguyên nhân hệ thống (hỏi “quy trình nào cho phép việc này xảy ra?”); bỏ phiếu chọn tối đa 2 nguyên nhân gốc |
| 45–55 | **Action** | Chuyển nguyên nhân gốc thành tối đa 2 Action Item (mẫu bên dưới) |
| 55–60 | **Follow-up (chốt)** | Xác nhận nhóm theo dõi, thời điểm, bằng chứng; ghi vào Sprint 15 Backlog; chấm lại mức hữu ích của Retro |

**Xử lý đổ lỗi:** SM nhắc quy tắc và đổi câu hỏi từ “ai” sang “quy trình/điều kiện nào”; chuyện liên quan cá nhân ghi vào parking lot để trao đổi riêng, không thảo luận trước nhóm. **PO tự chọn giải pháp:** Action cách làm việc do cả Scrum Team chọn; cách làm của Developers do Developers quyết định, PO tham gia như một thành viên.

### Tối đa 2 Action Item

|  | Action 1 – Kiểm thử tích hợp sớm | Action 2 – Quy tắc làm việc có kiểm soát |
| --- | --- | --- |
| **Nguyên nhân gốc** | Staging Ngày 4 nhưng Integration Test Ngày 8 → lỗi dịch vụ đơn hàng/lỗi cao lộ muộn; 3/5 hạng mục chưa Done | Quy tắc đổi qua tin nhắn → không ai thống nhất bản hiện hành; an toàn 2,8/5 |
| **Hành động** | Chạy Integration Test ngay sau khi lên staging, sớm nhất Ngày 5, cho mọi hạng mục Sprint 15 chạm dịch vụ đơn hàng và phân loại | Mọi thay đổi DoD/quy tắc chỉ được quyết định tại Planning hoặc Retro, ghi vào một tài liệu chung có lịch sử thay đổi |
| **Nhóm theo dõi** | Developers (SM hỗ trợ) | Scrum Team (SM quản lý tài liệu) |
| **Thời điểm** | Bắt đầu từ Sprint 15 Ngày 1; kiểm tra ở Ngày 5 và Review/Retro 15 | Áp dụng ngay từ Planning 15; kiểm tra ở Retro 15 |
| **Bằng chứng** | Lịch và kết quả Integration Test; số lỗi cao tìm thấy trước và sau Ngày 5 | Tài liệu quy tắc có lịch sử; kết quả chấm an toàn Retro 15 |
| **Tiêu chí đạt** | 100% hạng mục liên quan chạy Integration Test trước Ngày 6; 0 lỗi cao khi đóng Sprint | 0 thay đổi quy tắc ngoài sự kiện; an toàn ≥ 3,5/5 (mục tiêu của nhóm) |

Các ý tưởng thứ ba trở đi đưa vào parking lot cho Retro sau, không thêm Action.

---

## 4. Chọn kỹ thuật Retro

| Tiêu chí | Phương án A: Start–Stop–Continue | Phương án B: 4Ls (Liked, Learned, Lacked, Longed for) |
| --- | --- | --- |
| An toàn tâm lý | Thấp–trung bình: cột “Stop” dễ thành đổ lỗi khi an toàn đã 2,8/5 | Cao hơn: bắt đầu từ điều tích cực, “Lacked/Longed for” nói về thiếu hụt hệ thống |
| Tìm nguyên nhân | Hạn chế; thiên về liệt kê hành vi | Tốt hơn: “Lacked” lộ điều thiếu (kiểm thử sớm, quy tắc rõ) |
| Ra hành động | Nhanh, trực tiếp (Start/Stop thành Action) | Cần thêm bước chuyển đổi từ “Lacked/Longed for” sang Action |
| Thời lượng | Ngắn (khoảng 15–20 phút) | Dài hơn (khoảng 25–30 phút) |
| Người ít nói | Trung bình: dễ bị người nói nhiều dẫn dắt | Tốt: viết im lặng, ẩn danh trước khi thảo luận |

**Quyết định:** chọn **4Ls làm kỹ thuật chính** cho giai đoạn Data–Insight, kết thúc bằng bước **Start–Stop–Continue rút gọn (5 phút)** để biến “Lacked/Longed for” thành Action.

**Lý do (từ dữ liệu):** an toàn 2,8/5 và Retro cũ có đổ lỗi → cần kỹ thuật bắt đầu ẩn danh và nói về hệ thống; Action cũ mơ hồ → cần bước cuối thu hẹp thành hành động cụ thể.

**Trade-off:** 4Ls tốn thêm khoảng 10 phút và có thể dàn trải; giảm bằng cách giới hạn mỗi người 2–3 ghi chú mỗi nhóm và bỏ phiếu chọn tối đa 2 nguyên nhân.

**Điều kiện đổi/kết hợp:**

- Chuyển sang Start–Stop–Continue hoàn toàn khi an toàn ≥ 3,5/5 trong 2 Sprint liên tiếp và nhóm cần Retro nhanh.
- Giữ 4Ls đầy đủ nếu đổ lỗi tái diễn hoặc an toàn vẫn < 3/5.
- Nếu Retro bị nén thời gian, dùng Start–Stop–Continue nhưng vẫn viết ẩn danh.

---

## 5. Chu trình Inspect and Adapt

```
Sprint Review (Sprint 14)
   │  Feedback sản phẩm F-01..F-05 (chưa cam kết)
   ▼
Feedback Log ──► Product Backlog (PO sắp xếp, Developers ước lượng)
   │                         │
   │ bằng chứng cách làm     ▼
   │ việc (lỗi muộn,    Sprint 15 Planning (Developers chọn việc theo năng lực)
   ▼ quy tắc, an toàn)       ▲
Sprint Retrospective ──► Action Item (tối đa 2) ──┘
                                  │
                                  ▼
              Kiểm tra trong Sprint 15 (Ngày 5, Daily)
                                  │
                                  ▼
          Review 15 (sản phẩm) + Retro 15 (cách làm việc): đo lại
```

### Truy vết 1 Feedback: F-04 “Thiếu lịch sử”

| Bước | Nội dung | Ai có quyền cập nhật | Bằng chứng |
| --- | --- | --- | --- |
| Review 14 | Ghi vào Feedback Log, làm rõ cần lịch sử gì, kênh nào | SM ghi; stakeholder làm rõ | Dòng F-04 trong log |
| Backlog | Thêm/tinh chỉnh mục “Hiển thị lịch sử đa kênh khi chuyển CSKH” | **PO** | Mục Backlog có tiêu chí chấp nhận |
| Planning 15 | Chọn vào Sprint Backlog | **Developers** (theo năng lực), PO đề xuất | Sprint Backlog |
| Sprint 15 | Thực hiện, kiểm thử, đạt DoD | Developers | Kết quả kiểm thử, staging |
| Review 15 | Stakeholder xác nhận; trạng thái chuyển “Đã kiểm tra” → “Đóng” | PO | Demo, Feedback mới |

**Tiêu chí đo:** hội thoại AI không xử lý đến CSKH trong ≤ 2 phút, kèm trạng thái đơn và lịch sử đa kênh ở mọi ca kiểm thử chấp nhận.

### Truy vết 1 Action: Action 1 “Kiểm thử tích hợp sớm”

| Bước | Nội dung | Ai có quyền cập nhật | Bằng chứng |
| --- | --- | --- | --- |
| Retro 14 | Từ Data: Integration Test Ngày 8, 3/5 chưa Done → chọn Action | Cả Scrum Team | Biên bản Retro |
| Planning 15 | Đưa vào Sprint Backlog như một hạng mục | **Developers** (PO không áp đặt cách làm) | Sprint Backlog |
| Sprint 15, Ngày 5 | Kiểm tra Integration Test đã chạy chưa | Developers; SM theo dõi | Lịch và kết quả test |
| Retro 15 | Đánh giá theo tiêu chí; giữ/chỉnh/bỏ | Cả Scrum Team | Số lỗi cao, % hạng mục kịp test |

**Tiêu chí đo:** 100% hạng mục liên quan chạy Integration Test trước Ngày 6; 0 lỗi cao khi đóng Sprint.

---

## 6. Xử lý dữ liệu thiếu, đổ lỗi và cam kết sớm

| Tình huống | Cách xử lý |
| --- | --- |
| **Dữ liệu thiếu** (staging/quyền riêng tư của SC-61..64, lỗi cao của SC-65, nguồn F-01..05, số đo F-01/F-05, danh sách Action cũ, độ dài Sprint) | Không suy đoán: “chưa có bằng chứng” = chưa tính là đạt. SM yêu cầu bổ sung trước Review ít nhất 24 giờ; mục nào vẫn thiếu thì trình bày là “chưa xác nhận”, ghi giả định rõ ràng |
| **Đổ lỗi** | Đổi câu hỏi từ “ai” sang “quy trình nào”; ghi parking lot để nói riêng; SM có quyền tạm dừng 2 phút và nhắc quy tắc |
| **Cam kết sớm** | PO dùng câu chuẩn: “Đã ghi nhận, PO sẽ cân nhắc ưu tiên, chưa cam kết”. Cam kết chỉ phát sinh khi Developers chọn vào Sprint Backlog tại Planning |
| **Stakeholder đòi nghiệm thu** | Review không phải cổng nghiệm thu; việc phát hành do PO quyết định dựa trên Done |
| **Quản lý vận hành xin dự Retro** | Từ chối để giữ an toàn; nếu nhóm đồng ý, chia sẻ tóm tắt Action sau Retro |
| **Nhiều hơn 2 Action** | Giữ 2 Action có tác động lớn nhất; phần còn lại vào parking lot |
| **Action Sprint 15 không đạt** | Retro 15 xem lại nguyên nhân (thiếu nguồn lực, mơ hồ, sai ưu tiên), điều chỉnh hoặc đóng, không giữ nguyên danh sách cũ |
