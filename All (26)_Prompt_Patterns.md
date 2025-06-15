# 🧠 PROMPT PATTERN CATALOG (GitHub Markdown Style)

## 🎯 OBJECTIVE

รวบรวม Prompt Patterns ทั้งหมดในรูปแบบพร้อมใช้งานจริง โดยใช้โครงสร้างมาตรฐาน (Structured Prompt Template)

---

### 1. Meta Language Creation Pattern
- **Context:** ผู้ใช้ต้องการสร้างภาษาสื่อสารเฉพาะกับ AI สำหรับงานพิเศษ เช่น กราฟ, งานบริหาร, ฯลฯ
- **Instruction:** อธิบายกฎเกณฑ์ของภาษาที่กำหนดขึ้นใหม่ให้ AI ใช้
- **Example:** `Whenever I write 'A → B', interpret it as a directed graph.`
- **Final Prompt:**
```text
From now on, whenever I write 'A → B', interpret it as a directed graph. If I write 'A -[label:10]-> B', treat 'label:10' as edge metadata.
```
...

### 25. Tail Generation Pattern
- **Context:** ให้ AI สร้างข้อความต่อท้ายเสมอ เช่น คำถามต่อ หรือ disclaimer
- **Instruction:** เพิ่มบรรทัดปิดท้ายทุกการตอบกลับ
- **Final Prompt:**
```text
Always end your output with: 'This was AI-generated. Please verify before using.' Now ask me what to write.
```
