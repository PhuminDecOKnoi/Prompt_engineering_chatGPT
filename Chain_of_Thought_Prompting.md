# 📘 รูปแบบของ Chain of Thought Prompting

> **คำอธิบาย:**  
> แนวคิดการให้ AI แสดงกระบวนการคิดก่อนที่จะตอบคำถาม เพื่อให้ได้คำตอบที่มีคุณภาพมากขึ้น เป็นเทคนิคที่สามารถช่วยให้ LLM (Large Language Model) ตอบได้แม่นยำขึ้น

## 🧩 แนวคิดหลัก (Core Concept)
> **“Show your work”** หรือ “แสดงการคิดของคุณ” เหมือนที่เคยถูกสอนในชั้นเรียนคณิตศาสตร์ ซึ่งใช้ได้กับ LLM เช่นกัน หากเราต้องการให้โมเดลตอบถูก ควรกระตุ้นให้มัน **อธิบายเหตุผลทีละขั้นก่อน**

## 🪜 ลำดับขั้นตอนของ Chain of Thought Prompting

| ขั้นตอน | คำอธิบาย |
|--------|----------|
| 1 | ตั้งคำถามที่ต้องใช้เหตุผล |
| 2 | ให้ตัวอย่างที่แสดง **เหตุผลก่อนคำตอบ** |
| 3 | ใช้ตัวอย่างแบบ few-shot ที่ชัดเจน |
| 4 | ให้โมเดลเลียนแบบวิธีคิด (reasoning) ก่อนจะตอบ |
| 5 | เปรียบเทียบผลลัพธ์ระหว่างมีและไม่มี CoT |

## 📌 ตัวอย่างเปรียบเทียบ

### ❌ ไม่มี Chain of Thought Prompting
```
Q: I’m in a spaceship without gravity. I knocked over a cup with a needle. Is anything on the floor?

A: Yes, the cup and needle will fall on the floor.
```

> 🔍 **ปัญหา:** คำตอบผิดพลาด เพราะโมเดลไม่คิดลำดับเหตุผลเกี่ยวกับแรงโน้มถ่วง

### ✅ ใช้ Chain of Thought Prompting
```
Q: I’m in a spaceship without gravity. I knocked over a cup with a needle. Is anything on the floor?

Reasoning: In zero gravity, objects don’t fall. Instead, they float or move in the direction of applied force. Hence, the cup and needle will not rest on the floor.

Answer: No
```

> ✅ **ข้อดี:** โมเดลให้เหตุผลก่อน ซึ่งทำให้ได้คำตอบที่แม่นยำมากขึ้น

### 📘 ตัวอย่างอื่นในรูปแบบ Chain of Thought

#### 🚴 Bike Racer Example
```
Q: Four riders race at 30 mph for 2 hours. Is the total mileage > 200?

Reasoning: 30 mph × 2 hr = 60 miles per rider. 4 riders × 60 = 240 miles.

Answer: Yes
```

#### 🚲 Race Staging Example
```
Q: Each group takes 114 sec to stage. Can you start a new race every 30 sec with 8 groups?

Reasoning: 114 ÷ 30 = 3.8 → round up = 4 groups needed

Answer: No
```

## 🧠 สาระสำคัญ

| สิ่งที่ได้ | ประโยชน์ |
|------------|------------|
| สร้างเหตุผลก่อนคำตอบ | ช่วยให้โมเดลคิดเชิงตรรกะมากขึ้น |
| ได้ผลลัพธ์แม่นยำขึ้น | โดยเฉพาะคำถามที่ซับซ้อน |
| กระตุ้นการวิเคราะห์เป็นลำดับขั้น | ลดความคลาดเคลื่อนของคำตอบ |

## 🧪 โครงสร้าง Prompt แบบ Chain of Thought
```
### Prompt Template

Q: [คำถามของคุณ]

Reasoning: [อธิบายลำดับเหตุผลทีละขั้น]

Answer: [คำตอบ]
```

## 📚 รายการอ้างอิง (APA 7th Style)

Brown, T. B., Mann, B., Ryder, N., Subbiah, M., Kaplan, J. D., Dhariwal, P., ... & Amodei, D. (2020). *Language models are few-shot learners*. arXiv preprint arXiv:2005.14165.

Wei, J., Wang, X., Schuurmans, D., Bosma, M., Ichter, B., Xia, F., ... & Le, Q. V. (2022). *Chain of Thought Prompting Elicits Reasoning in Large Language Models*. arXiv:2201.11903.
