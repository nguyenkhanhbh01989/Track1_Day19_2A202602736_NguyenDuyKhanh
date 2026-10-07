# AI Support Log

## 1. Công cụ AI đã sử dụng

- ChatGPT
- Google Stitch
- [Công cụ khác nếu có]

---

## 2. AI được sử dụng ở giai đoạn nào?

### Problem framing

AI được dùng để rà soát cách diễn đạt Hypothesis Problem và kiểm tra xem problem có đang chứa solution hay không.

### Solution ideation

AI hỗ trợ:

- gợi ý cách phân biệt ba solution mechanisms;
- so sánh mức độ agency giữa user và AI;
- kiểm tra A/B/C có khác nhau đủ rõ hay không.

### Human–AI Design

AI hỗ trợ rà soát:

- Expectation
- Role and Agency
- Act / Ask / Don't Act
- Evidence
- Uncertainty
- Control
- Recovery

### Prototype

AI hỗ trợ:

- viết prompt cho Google Stitch;
- gợi ý microcopy;
- tạo synthetic fixture;
- tạo canned AI output;
- gợi ý interaction states.

### Test preparation

AI hỗ trợ:

- rà soát test task;
- phát hiện câu hỏi dẫn dắt;
- gợi ý observation focus.

---

## 3. Ví dụ AI đã giúp

### Ví dụ 1

AI gợi ý spectrum:

User initiates  
→ AI asks, user confirms  
→ AI initiates, human reviews

Nhóm dùng spectrum này để kiểm tra ba options có đủ khác nhau hay không.

### Ví dụ 2

AI đề xuất với Option B rằng AI nên:

**Ask**

thay vì tự:

**Act**

vì false positive có thể ảnh hưởng tới privacy và learner agency.

### Ví dụ 3

AI hỗ trợ tạo prompt cho Google Stitch để prototype Option B thể hiện:

- AI check-in;
- explanation;
- uncertainty;
- learner confirmation;
- preview before sharing;
- cancel/recovery.

---

## 4. Điểm AI sai / hời hợt / cần chỉnh

AI có xu hướng:

- giả định solution cần AI nhiều hơn mức cần thiết;
- tạo flow quá hoàn chỉnh so với micro-prototype;
- đưa ra nhiều feature ngoài phạm vi lab;
- diễn giải observation mạnh hơn evidence thật;
- có thể vô tình biến hypothesis thành conclusion.

Nhóm đã tự chỉnh bằng cách:

- giữ scope 2–3 critical states;
- không build full product;
- tách fact khỏi interpretation;
- không dùng AI-generated feedback làm evidence;
- giữ các câu “có thể”, “chưa biết”, “still unproven”.

---

## 5. AI không được sử dụng cho

AI không được dùng để:

- tạo tester giả;
- tạo quote giả;
- tạo observation giả;
- sửa lời tester thành evidence “đẹp hơn”;
- viết thay personal reflection dựa trên dữ liệu không có thật;
- tuyên bố solution validated.

---

## 6. Synthetic Data Disclosure

Prototype sử dụng synthetic data cho mục đích test.

Ví dụ:

- learner name;
- slide revisit count;
- answer change count;
- AI chat count;
- confidence;
- support summary.

Các dữ liệu này chỉ dùng để mô phỏng interaction, không được coi là evidence về hành vi user thật.

---

## 7. Phần do cá nhân tự làm

Tôi tự chịu trách nhiệm:

- quyết định nội dung cuối cùng đưa vào prototype;
- kiểm tra prompt AI;
- facilitate usability test;
- ghi observation;
- phân biệt observed / interpreted;
- viết feedback note dựa trên phiên test thật;
- tham gia chốt Next Change.

---

## 8. Kết luận về việc dùng AI

AI được dùng như công cụ hỗ trợ thiết kế và rà soát.

AI không thay thế:

- user evidence;
- tester feedback;
- observation;
- quyết định cuối cùng của nhóm.