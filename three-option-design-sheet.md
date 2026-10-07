# Three Option Design Sheet
## Case C — AI Support Radar

---

## 1. Shared Problem

### Hypothesis Problem

Khi hỗ trợ một lớp có nhiều learner, Instructor/Lab Coach gặp khó khăn trong việc xác định ai thực sự đang cần hỗ trợ vì không phải learner nào cũng chủ động hỏi hoặc thể hiện rõ điểm vướng, dẫn đến một số learner có thể được phát hiện và hỗ trợ muộn.

---

## 2. Shared Decisions

| Thành phần | Quyết định chung |
|---|---|
| Target user | Instructor/Lab Coach + Learner |
| Situation | Trong hoặc sau một buổi học/lab trên VLearn |
| Task | Xác định learner có thể cần hỗ trợ và quyết định bước tiếp theo |
| Desired outcome | Hỗ trợ đúng learner, đúng lúc, hạn chế bỏ sót |
| Content fixture | Cùng session, cùng learner, cùng nội dung bài và tín hiệu mẫu |

---

# 3. Option A — Learner-initiated Help Request

## Solution mechanism

Learner chủ động gửi yêu cầu hỗ trợ.

## User làm gì?

- Nhận ra mình đang gặp khó khăn.
- Bấm “Cần hỗ trợ”.
- Chọn topic hoặc nhập vấn đề.
- Review request.
- Gửi cho Lab Coach.

## AI làm gì?

- Có thể tóm tắt context.
- Không suy đoán learner cần hỗ trợ.
- Không tự gửi request.

## Trigger

Learner chủ động.

## Trade-off chính

**Ưu điểm**
- Intent chính xác.
- Privacy tốt.
- Learner có toàn quyền.

**Hạn chế**
- Không giải quyết được learner im lặng.
- Có thể bỏ sót người không biết nên hỏi gì.

## AI Act / Ask / Don't Act

**Don't Act**

AI chỉ hỗ trợ sau khi learner initiate.

## Control / Recovery

- Edit
- Cancel
- Return to learning
- Withdraw request

---

# 4. Option B — AI Detects, Learner Confirms

## Solution mechanism

AI nhận thấy tín hiệu có khả năng learner đang gặp khó khăn và thực hiện check-in.

## User làm gì?

Learner chọn:

- Có, mình cần hỗ trợ
- Mình tự xử lý được
- Nhắc lại sau

Nếu cần hỗ trợ:

- review summary;
- chọn context được chia sẻ;
- edit;
- gửi.

## AI làm gì?

- Detect possible struggle signals
- Explain why it is checking in
- Ask
- Summarize context
- Không tự escalate

## Trigger

Một tập hợp tín hiệu như:

- xem lại slide nhiều lần;
- đổi câu trả lời nhiều lần;
- dành nhiều thời gian ở cùng một bước;
- hỏi AI nhiều câu liên quan cùng concept.

## Trade-off chính

**Ưu điểm**
- Có thể bắt được learner không chủ động hỏi.
- Learner vẫn có quyền xác nhận.
- Giảm false escalation.

**Hạn chế**
- Có thể gây interruption.
- Learner có thể cảm thấy bị theo dõi.
- Tín hiệu có thể sai.

## AI Act / Ask / Don't Act

**Ask**

AI chỉ check-in, không tự đưa learner sang Support Queue.

## Evidence / uncertainty

Ví dụ:

> Có vẻ bạn đang dành khá nhiều thời gian ở phần Human–AI Decision Table.

> Đây chỉ là tín hiệu gợi ý và có thể không phản ánh chính xác việc bạn có cần hỗ trợ hay không.

## Control / Recovery

- I'm okay
- Remind me later
- Edit summary
- Select data to share
- Cancel
- Return to learning

---

# 5. Option C — AI-generated Support Queue

## Solution mechanism

AI tự phân tích tín hiệu và tạo danh sách learner có thể cần hỗ trợ cho Instructor/Lab Coach.

## User làm gì?

Instructor:

- xem queue;
- mở evidence;
- review learner;
- contact / dismiss / mark incorrect.

## AI làm gì?

- Detect
- Rank
- Explain
- Recommend action

## Trigger

Sau phiên học hoặc sau một khoảng thời gian.

## Trade-off chính

**Ưu điểm**
- Scalable.
- Instructor chủ động biết ai có thể cần support.
- Phù hợp lớp đông.

**Hạn chế**
- False positive.
- Privacy concern.
- Instructor có thể over-trust AI ranking.

## AI Act / Ask / Don't Act

AI **recommends**, human decides.

## Control / Recovery

- Dismiss
- Mark incorrect
- Review evidence
- Contact learner manually

---

# 6. Distance Check

### A khác B vì

A chỉ hoạt động khi learner chủ động yêu cầu; B cho phép AI chủ động check-in nhưng learner giữ quyền xác nhận.

### B khác C vì

B yêu cầu learner xác nhận trước khi escalate; C đưa recommendation trực tiếp cho Instructor/Lab Coach.

### A khác C vì

A gần như không dùng inference; C phụ thuộc nhiều vào inference và prioritization của AI.

---

# 7. Human–AI Decision Table

| Decision | Option A | Option B | Option C |
|---|---|---|---|
| User làm gì? | Chủ động request | Confirm / decline | Review recommendation |
| AI làm gì? | Tóm tắt | Detect + ask + summarize | Detect + rank + recommend |
| Act / Ask / Don't Act | Don't Act | Ask | Recommend |
| Evidence | User-provided context | Behavioral signals | Behavioral signals + ranking |
| Uncertainty | Ít cần | Hiển thị rõ | Confidence + evidence |
| Control | Edit/cancel | Decline/snooze/edit/cancel | Dismiss/mark incorrect |
| Recovery | Withdraw request | Return to learning | Ignore/remove recommendation |

---

# 8. Option được chọn làm sâu

## Option B — AI Detects, Learner Confirms

### Lý do chọn

Option B cân bằng tốt nhất giữa:

- proactive support;
- learner agency;
- false positive risk;
- privacy;
- transparency;
- human control.

Option này cũng tạo ra critical interaction rõ ràng để usability test:

AI detect  
→ AI ask  
→ learner interpret  
→ learner decide  
→ learner review what is shared