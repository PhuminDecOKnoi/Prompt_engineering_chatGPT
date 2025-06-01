
# 📘 React Prompt Pattern (Reasoning + Acting Pattern)

> **รูปแบบการตั้ง Prompt แบบ React เพื่อให้ AI เรียนรู้การคิดเป็นขั้นตอนและใช้เครื่องมือภายนอกประกอบการตอบ**  
> *(อ้างอิง: LangChain และแนวคิด React pattern จาก arXiv)*

---

## ✅ หลักการพื้นฐาน (Key Concepts)

| ลำดับ | แนวคิดสำคัญ                                                                 |
|--------|-----------------------------------------------------------------------------|
| 1️⃣    | LLM ไม่สามารถตอบคำถามทุกอย่างได้ด้วยตัวเอง จึงต้องเรียนรู้การใช้เครื่องมือเสริม |
| 2️⃣    | เราสามารถสอนให้ AI “คิดเป็นขั้นตอน” และรู้ว่าเมื่อใดต้องใช้ “external tools”     |
| 3️⃣    | ใช้ “ตัวอย่าง (few-shot)” ที่แสดงโครงสร้างคำสั่ง เช่น `Action:` และ `Result:` เพื่อฝึกแบบมีโครงสร้าง |

---

## 🔧 โครงสร้างของ Prompt (Prompt Structure)

```txt
Task: [ระบุภารกิจหรือคำถาม]

Example:
Task: [คำถามตัวอย่าง]
Think: [AI แสดงกระบวนการคิดเป็นลำดับ]
Action: [ใช้เครื่องมือ เช่น Web Search, Video Analysis]
Result: [ผลลัพธ์ของการกระทำ]
...
[ดำเนินการซ้ำจนถึงผลลัพธ์สุดท้าย]
```

---

## 🧠 ตัวอย่าง Prompt (Example)

```txt
Task: คำนวณว่าฉันต้องไปถึงสนามแข่ง BMX ที่ Music City เวลาใด เพื่อให้ลูกชายเข้าร่วมการแข่งขันช่วง 9:00-10:00 ได้ทัน

Example:
Think: ฉันต้องหาว่าเวลาที่การแข่งขันเริ่มคือกี่โมง
Action: search www.musiccitybmx.com
Result: การแข่งขันเริ่มเวลา 09:00 น.

Think: ฉันต้องหาว่ามีการแข่งกี่รอบ (moto) ก่อนถึงรอบของลูกชาย
Action: search www.musiccitybmx.com
Result: มี 30 รอบก่อนรอบของลูก

Think: แต่ละรอบใช้เวลาเท่าไหร่
Action: video analysis จากวิดีโอปีที่แล้ว
Result: 10 รอบใช้เวลา 5 นาที

Think: ถ้า 10 รอบใช้เวลา 5 นาที แสดงว่า 30 รอบใช้เวลา 15 นาที
Final Answer: ฉันควรไปถึงก่อน 08:45 น. เพื่อความปลอดภัย
```

---

## 🛠️ ตัวอย่าง Code: React Prompt Template (GitHub Style)

```json
{
  "prompt": [
    {
      "task": "คำนวณเวลาสิ้นสุดของการแข่งขันรุ่น 36-40 novice ที่ USA BMX Grand Nationals",
      "steps": [
        {
          "think": "ฉันต้องหาว่าเวลาที่การแข่งขันเริ่มต้น",
          "action": "search www.usabmx.com/events/grands",
          "result": "การแข่งขันเริ่มเวลา 08:00 น."
        },
        {
          "think": "มีทั้งหมดกี่ motos ก่อนถึงรุ่นนี้",
          "action": "search www.usabmx.com/motos",
          "result": "มีทั้งหมด 120 motos"
        },
        {
          "think": "แต่ละ moto ใช้เวลากี่นาที",
          "action": "video analysis",
          "result": "10 motos ใช้เวลา 6 นาที"
        },
        {
          "final_calculation": "120 motos ≈ 72 นาที → รุ่นนี้เริ่มประมาณ 09:12 น. และจบที่ 09:15 น."
        }
      ]
    }
  ]
}
```

---

## 🔎 ประโยชน์ของ React Pattern

| จุดเด่น                        | ประโยชน์                                           |
|-------------------------------|----------------------------------------------------|
| 🧠 Reasoning แบบมีขั้นตอน      | สร้าง AI ที่สามารถอธิบายขั้นตอนคิดของตนเองได้     |
| 🔗 เชื่อมต่อ External Tools   | ใช้ข้อมูลจากภายนอก เช่น Web, APIs, Video ได้     |
| 💡 แก้ปัญหาที่ยากกว่าเดิม    | เช่น คำนวณเวลา, วางแผน, วิเคราะห์หลายปัจจัย      |

---

## 📚 รายการอ้างอิง (References)

- Yao, S., Zhao, J., Wang, D., et al. (2022). [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629). arXiv.
- LangChain Framework – [https://www.langchain.com](https://www.langchain.com)
