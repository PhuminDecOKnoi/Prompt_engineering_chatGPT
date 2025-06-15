# 🧠 PROMPT PATTERN CATALOG (GitHub Markdown Style)

## 📘 DESCRIPTION

This repository is a comprehensive catalog of reusable prompt engineering patterns for Large Language Models (LLMs). Inspired by software design patterns, these structured prompts help improve clarity, consistency, and effectiveness when interacting with AI. Each pattern includes context, instructions, examples, and ready-to-copy prompt formats.

Use this guide to build robust and smart LLM-based applications, automate reasoning workflows, debug prompt failures, and teach others about effective AI prompting.

## 🎯 OBJECTIVE

รวบรวม Prompt Patterns ทั้งหมดในรูปแบบพร้อมใช้งานจริง โดยใช้โครงสร้างมาตรฐาน (Structured Prompt Template)

---

### 1. Meta Language Creation Pattern

* **Context:** ผู้ใช้ต้องการสร้างภาษาสื่อสารเฉพาะกับ AI สำหรับงานพิเศษ เช่น กราฟ, งานบริหาร, ฯลฯ
* **Instruction:** อธิบายกฎเกณฑ์ของภาษาที่กำหนดขึ้นใหม่ให้ AI ใช้
* **Example:** `Whenever I write 'A → B', interpret it as a directed graph.`
* **Final Prompt:**

```text
From now on, whenever I write 'A → B', interpret it as a directed graph. If I write 'A -[label:10]-> B', treat 'label:10' as edge metadata.
```

---

### 2. Template Pattern

* **Context:** ต้องการให้ผลลัพธ์มีรูปแบบตามที่กำหนดไว้ เช่น API URL, workout format
* **Instruction:** กำหนด template ที่ชัดเจนให้ AI ใช้
* **Example:** `NAME, REPS @ SETS, DIFFICULTY`
* **Final Prompt:**

```text
I am going to provide a template. Everything in ALL CAPS is a placeholder. Try to generate output that matches this template exactly: https://myapi.com/NAME/profile/JOB
```

---

### 3. Persona Pattern

* **Context:** ต้องการให้ AI ตอบในบทบาทเฉพาะ เช่น นักวิเคราะห์, ครู, นักข่าว
* **Instruction:** บอกให้ AI สวมบทบาทนั้น
* **Example:** `Act as a cybersecurity expert.`
* **Final Prompt:**

```text
From now on, act as a security reviewer. Evaluate all code with security-first principles.
```

---

### 4. Visualization Generator Pattern

* **Context:** ผู้ใช้ต้องการสร้าง prompt สำหรับเครื่องมือสร้างภาพ
* **Instruction:** ให้ AI สร้าง Graphviz/DALL·E prompt
* **Example:** `digraph G { node1 -> node2; }`
* **Final Prompt:**

```text
Create a Graphviz DOT file to visualize the following structure: A → B → C
```

---

### 5. Recipe Pattern

* **Context:** ต้องการขั้นตอนการทำสิ่งใดสิ่งหนึ่ง เช่น deploy app, อบเค้ก
* **Instruction:** ขอให้ AI สร้างขั้นตอนทีละลำดับ
* **Example:** `1. Preheat oven...`
* **Final Prompt:**

```text
I want to deploy a React app to AWS. Please provide a complete step-by-step guide and fill in any missing steps.
```

---

### 6. Output Automater Pattern

* **Context:** ต้องการให้ AI สร้าง script หรือโค้ดที่สามารถใช้งานได้เลย
* **Instruction:** ให้สร้าง automation script
* **Final Prompt:**

```text
Whenever you generate code that spans files, generate a Python script to create the files automatically.
```

---

### 7. Fact Check List Pattern

* **Context:** ต้องการให้ AI สร้างรายการข้อเท็จจริงที่ควรตรวจสอบ เพื่อให้ผลลัพธ์แม่นยำขึ้น
* **Instruction:** ให้ AI สรุปข้อเท็จจริงหลักท้ายคำตอบ
* **Example:** `1. The capital of Australia is Sydney.`
* **Final Prompt:**

```text
From now on, when you generate an answer, list 2–3 key facts from your response that a user should verify.
```

---

### 8. Reflection Pattern

* **Context:** ต้องการให้ AI ตรวจสอบและปรับปรุงคำตอบของตนเอง
* **Instruction:** ให้ AI ระบุจุดอ่อนหรือข้อผิดพลาดหลังตอบคำถาม
* **Final Prompt:**

```text
After giving your answer, analyze your response and suggest any possible improvements or corrections.
```

---

### 9. Question Refinement Pattern

* **Context:** ต้องการให้ AI เสนอเวอร์ชันที่ดีขึ้นของคำถาม
* **Instruction:** ให้ AI เสนอคำถามทางเลือกและสอบถามผู้ใช้ว่าจะใช้คำไหน
* **Final Prompt:**

```text
After I ask a question, suggest a better version that would help you answer more precisely. Ask me if I want to use your version.
```

---

### 10. Alternative Approaches Pattern

* **Context:** ต้องการให้ AI เสนอตัวเลือกหลายวิธีในการแก้ปัญหา
* **Instruction:** เปรียบเทียบข้อดีข้อเสียของแต่ละวิธี
* **Final Prompt:**

```text
When I ask for a solution, offer 2–3 alternative approaches, compare pros/cons, and ask me which one to proceed with.
```

---

### 11. Cognitive Verifier Pattern

* **Context:** สำหรับคำถามซับซ้อน ต้องการแยกเป็นคำถามย่อยก่อนตอบ
* **Instruction:** ให้ AI สร้างคำถามย่อย 3 ข้อและรวมคำตอบ
* **Final Prompt:**

```text
Break my question into 3 sub-questions. When I answer them, synthesize the final response based on all inputs.
```

---

### 12. Refusal Breaker Pattern

* **Context:** เมื่อ AI ปฏิเสธตอบ ต้องการให้เสนอคำถามที่ตอบได้แทน
* **Instruction:** ให้ AI อธิบายเหตุผลและเสนอเวอร์ชันที่สามารถตอบได้
* **Final Prompt:**

```text
If you ever refuse to answer, explain why and suggest an alternative version that you can respond to.
```

---

### 13. Flipped Interaction Pattern

* **Context:** ผู้ใช้ต้องการให้ AI เป็นฝ่ายถามคำถามเพื่อรวบรวมข้อมูลก่อนให้คำตอบ
* **Instruction:** ให้ AI เป็นผู้นำบทสนทนา ถามทีละคำถาม
* **Final Prompt:**

```text
Ask me questions to help you gather everything needed to complete the task. Ask one question at a time. Begin with the first question.
```

---

### 14. Game Play Pattern

* **Context:** เปลี่ยนงานให้เป็นเกม เพื่อเพิ่มความน่าสนใจ
* **Instruction:** ออกแบบเกมที่มีเนื้อหาเกี่ยวข้องกับหัวข้อเป้าหมาย
* **Final Prompt:**

```text
Create a story-based game where I explore a cave to discover parts of a lost language. Start with the first room.
```

---

### 15. Infinite Generation Pattern

* **Context:** ผู้ใช้ต้องการให้ AI สร้างข้อมูลต่อเนื่องจนกว่าจะสั่งหยุด
* **Instruction:** สร้างผลลัพธ์ซ้ำแบบอัตโนมัติ
* **Final Prompt:**

```text
Keep generating random names and job titles in the format: https://api.com/NAME/profile/JOB until I say 'stop'.
```

---

### 16. Context Manager Pattern

* **Context:** ควบคุมบริบทที่ AI ใช้ เช่น จำกัดหรือเปลี่ยน
* **Instruction:** ระบุว่าจะใช้หรือไม่ใช้บริบทใดบ้าง
* **Final Prompt:**

```text
From now on, only consider security aspects when analyzing this code. Ignore formatting or naming conventions.
```

---

### 17. Chain-of-Thought (CoT) Pattern

* **Context:** ต้องการให้ AI คิดเป็นลำดับ เพื่อให้เหตุผลซับซ้อนถูกต้องขึ้น
* **Instruction:** ให้ AI คิดเป็นขั้นตอน (step by step)
* **Final Prompt:**

```text
Let’s think step by step. Q: What is the net growth of 1000 users +200 -50?
```

---

### 18. Few-Shot Prompting Pattern

* **Context:** สอน AI ด้วยตัวอย่าง 2-3 ตัวอย่างใน prompt
* **Instruction:** ใส่ตัวอย่าง แล้วให้ AI ทำตามรูปแบบเดียวกัน
* **Final Prompt:**

```text
Example: 'Great product!' → Positive. Now classify: 'Terrible experience.'
```

---

### 19. Zero-Shot Prompting Pattern

* **Context:** ไม่มีตัวอย่าง ให้ AI ตอบตามความเข้าใจภาษาธรรมชาติ
* **Instruction:** อธิบายภารกิจชัดเจนด้วยคำสั่งภาษาอังกฤษ
* **Final Prompt:**

```text
Translate the following English sentence into French: 'I love learning languages.'
```

---

### 20. Tree-of-Thought (ToT) Pattern

* **Context:** ให้ AI สำรวจหลายทางเลือกก่อนสรุป
* **Instruction:** ให้ AI เสนอหลายแนวคิด ประเมิน แล้วสรุปวิธีที่ดีที่สุด
* **Final Prompt:**

```text
Analyze 3 strategies for spending a $100K marketing budget. Compare pros/cons, then choose the best one.
```

---

### 21. ReAct Pattern (Reasoning and Acting)

* **Context:** ใช้เหตุผล + การกระทำ (search/click/observe)
* **Instruction:** ให้ AI แสดง reasoning step + action step
* **Final Prompt:**

```text
Search for the best budget phone in 2024. Retrieve data, reason on specs, and suggest the best deal.
```

---

### 22. Audience Persona Pattern

* **Context:** ให้ AI อธิบายตามระดับความรู้หรือมุมมองของผู้ฟัง
* **Instruction:** ระบุ persona เช่น เด็กประถม, นักวิทยาศาสตร์
* **Final Prompt:**

```text
Explain blockchain to me as if I were a 10-year-old.
```

---

### 23. Ask for Input Pattern

* **Context:** ต้องการ input จากผู้ใช้ก่อนดำเนินงาน
* **Instruction:** ให้ AI รอรับข้อมูลก่อนเริ่ม
* **Final Prompt:**

```text
I will paste email chains. You summarize them with bullet points. Ask me for the first email.
```

---

### 24. Menu Actions Pattern

* **Context:** กำหนดคำสั่งเฉพาะให้ผู้ใช้เรียก action ได้ทันที
* **Instruction:** ตั้ง command ที่ AI ตอบสนองทันที เช่น add/remove
* **Final Prompt:**

```text
When I type 'add ITEM', add to list. When 'remove ITEM', delete from list. Ask what action I want to take.
```

---

### 25. Tail Generation Pattern

* **Context:** ให้ AI สร้างข้อความต่อท้ายเสมอ เช่น คำถามต่อ หรือ disclaimer
* **Instruction:** เพิ่มบรรทัดปิดท้ายทุกการตอบกลับ
* **Final Prompt:**

```text
Always end your output with: 'This was AI-generated. Please verify before using.' Now ask me what to write.
```

---
