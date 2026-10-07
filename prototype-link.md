# Prototype Links

## Common context

Các prototype mô phỏng VLearn trong một buổi học/lab của:

- **Course:** Human-Centered AI Design
- **Session:** Day 18+19 — Design the Experiment

Task chung:

> Xác định learner nào có thể cần hỗ trợ và quyết định bước tiếp theo.

---

## Option A — Learner-initiated Help Request

**Prototype link:**
https://stitch.withgoogle.com/projects/2774299646077061359

### Start state

Normal VLearn learning page.

### Critical interaction

Learner chủ động bấm “Cần hỗ trợ”.

### Expected test path

Learning page  
→ Need Help  
→ Add context  
→ Review  
→ Send request

---

## Option B — AI Detects, Learner Confirms

**Prototype link:**

https://stitch.withgoogle.com/projects/2774299646077061359

### Start state

Learner đang học/làm lab trên VLearn.

### Critical interaction

AI check-in khi nhận thấy một số possible struggle signals.

### Expected test paths

#### Need support

Learning  
→ AI check-in  
→ Need help  
→ Review context  
→ Send  
→ Confirmation

#### No support

Learning  
→ AI check-in  
→ I'm okay  
→ Return to learning

#### Snooze

Learning  
→ AI check-in  
→ Remind me later  
→ Return to learning

---

## Option C — AI-generated Support Queue

**Prototype link:**
https://stitch.withgoogle.com/projects/2774299646077061359
### Start state

Instructor/Lab Coach view.

### Critical interaction

AI provides a prioritized support queue with evidence.

### Expected test path

Support Queue  
→ Review learner  
→ Inspect evidence  
→ Contact / Dismiss

---

## Recommended test order

Để tránh order bias, có thể đổi thứ tự giữa các tester:

- Tester 1: A → B → C
- Tester 2: B → C → A
- Tester 3: C → A → B

---

## Prototype scope

Các prototype là micro-prototype phục vụ usability test.

Không bao gồm:

- backend thật;
- AI model thật;
- authentication;
- production database;
- complete VLearn flow.

AI output trong prototype là canned/synthetic output.