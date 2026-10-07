# Track1_Day18_MHV_HoVaTen

## 1. Thông tin cá nhân và nhóm

- **MHV:** 2A202602736
- **Họ và tên:** Nguyễn Duy Khánh
- **Tên nhóm:** [Điền tên nhóm]
- **Thành viên:**
  - Nguyễn Phạm Oanh Oanh - 2A202602518
  - Nguyễn Duy Khánh - 2A202602736
  - Hoàng Bích Ngọc - 2A202602766
- **Case:** Case C — AI Support Radar

---

## 2. Hypothesis Problem

### Problem Hypothesis

Khi hỗ trợ một lớp có nhiều learner, Instructor/Lab Coach gặp khó khăn trong việc xác định ai thực sự đang cần hỗ trợ vì không phải learner nào cũng chủ động hỏi hoặc thể hiện rõ điểm vướng, dẫn đến một số learner có thể được phát hiện và hỗ trợ muộn.

### Evidence ban đầu từ Day 17

Practice interview Day 17 cho thấy:

- Có learner không biết nên hỏi gì nên không chủ động hỏi.
- Lab Coach đôi khi phải dựa vào biểu hiện như ngập ngừng hoặc “đăm chiêu” để đoán learner đang gặp vấn đề.
- Trong lớp đông, người hỗ trợ khó quan sát toàn bộ learner.
- Một số learner có thể tự xử lý khá tốt bằng tài liệu, AI và Lab Coach, vì vậy không phải mọi tín hiệu bất thường đều đồng nghĩa learner cần được can thiệp.

Một Practice Note từ phía hỗ trợ ghi nhận rằng một số learner “không biết nên hỏi cái gì” nên không hỏi, trong khi việc phát hiện các trường hợp này trong lớp đông còn hạn chế. :chatgpt-content-reference{index="0"}

Ở phía learner, participant được phỏng vấn lại có một workflow tự xử lý khá rõ qua tài liệu, AI, checkpoint và Lab Coach; nếu tool giải quyết được thì learner không cần hỏi người khác. :chatgpt-content-reference{index="1"}

### Điều vẫn chưa được chứng minh

- Tình trạng learner bị phát hiện muộn xảy ra với tần suất bao nhiêu.
- Hậu quả của việc phát hiện muộn có đủ lớn hay không.
- Các tín hiệu hành vi có đủ đáng tin để suy đoán learner cần hỗ trợ hay không.
- Learner có cảm thấy thoải mái khi hệ thống chủ động check-in hay không.
- Cơ chế nào cân bằng tốt nhất giữa chủ động hỗ trợ và quyền kiểm soát của learner.

> Practice evidence của Day 17 chưa được xem là validation của problem.

---

## 3. Three Solution Options

Nhóm thiết kế ba solution hypothesis cùng giải quyết một problem, cùng context và cùng task.

### Shared context

- **Target user:** Instructor/Lab Coach và learner
- **Context:** Một phiên học/lab trên VLearn đang diễn ra hoặc vừa kết thúc
- **Task:** Xác định learner nào có thể cần hỗ trợ và quyết định bước tiếp theo
- **Desired outcome:** Giảm nguy cơ bỏ sót learner cần hỗ trợ nhưng vẫn giữ quyền kiểm soát cho con người
- **Fixture:** Cùng một buổi học, cùng nội dung, cùng learner và cùng dữ liệu mẫu

### Option A — Learner-initiated Help Request

Learner chủ động chọn “Cần hỗ trợ”, mô tả vấn đề và gửi yêu cầu cho Lab Coach.

- User initiates
- AI chỉ hỗ trợ cấu trúc hoặc tóm tắt request
- Không tự suy đoán learner cần hỗ trợ

**Trade-off:** intent rõ nhưng có thể bỏ sót learner im lặng.

### Option B — AI Detects, Learner Confirms

AI phát hiện một số tín hiệu có thể cho thấy learner đang gặp khó khăn, sau đó hỏi learner xác nhận.

Flow:

AI detects  
→ AI check-in  
→ learner confirms / declines  
→ learner reviews context  
→ request sent to Lab Coach

**Trade-off:** chủ động hơn Option A nhưng có thể gây interruption hoặc false positive.

### Option C — AI-generated Support Queue

AI phân tích tín hiệu và đưa learner vào Support Queue để Instructor/Lab Coach review.

- AI prioritizes
- Instructor reviews evidence
- Instructor decides whether to intervene

**Trade-off:** scalable hơn nhưng có rủi ro AI suy đoán sai learner.

### Link prototype

Xem:

`prototype-link.md`

---

## 4. Đóng góp của tôi trong nhóm

Trong Day 18, tôi phụ trách:

- Tham gia tổng hợp evidence từ Day 17.
- Tham gia chốt Hypothesis Problem.
- Tham gia thiết kế sự khác biệt giữa Option A/B/C.
- Phụ trách chính **Option B — AI Detects, Learner Confirms**.
- Thiết kế Human–AI interaction của Option B:
  - AI detect
  - AI ask
  - learner confirm
  - learner preview/edit
  - learner decide whether to share
- Tham gia xây shared context và content fixture.
- Chuẩn bị prototype Option B.
- Facilitate một phiên usability test với Tester [ID].
- Ghi Prototype Feedback Note của phiên mình điều phối.
- Tham gia Group Feedback Synthesis.

---

## 5. Prototype Feedback

### Phiên tôi facilitate

- **Tester ID:** [T01]
- **Relevant context:** [Điền context thật]

Xem chi tiết:

`prototype-feedback-note.md`

### Observation chính

- **First action:** [Điền sau test]
- **Breakdown:** [Điền sau test]
- **Evidence read/ignored:** [Điền sau test]
- **Recovery behavior:** [Điền sau test]
- **Option chosen:** [A/B/C]
- **Trade-off tester quan tâm:** [Điền sau test]

### Group synthesis

Sau ba phiên test, nhóm tổng hợp tại:

`group-feedback-synthesis.md`

### Next Change

> [Điền quyết định thật sau khi tổng hợp 3 tester]

Ví dụ cấu trúc:

> Nhóm sẽ giữ cơ chế của Option B nhưng giảm mức độ interruption, làm rõ lý do AI check-in và cho learner kiểm soát rõ hơn context được gửi sang Lab Coach.

### Still Unproven

> Chưa thể kết luận rằng các tín hiệu học tập hiện tại đủ chính xác để phát hiện learner cần hỗ trợ trong môi trường thật.

---

## 6. AI Support Log

AI được sử dụng để:

- gợi ý cách phân biệt ba solution mechanisms;
- rà soát Human–AI interaction;
- gợi ý nội dung prototype;
- hỗ trợ viết microcopy;
- hỗ trợ prompt cho công cụ thiết kế prototype;
- rà soát tính dẫn dắt của câu hỏi usability test.

AI không được sử dụng để:

- tạo fake tester;
- tạo observation giả;
- tạo quote giả;
- viết thay feedback thực tế;
- tuyên bố solution đã được validated.

Chi tiết xem:

`ai-support-log.md`