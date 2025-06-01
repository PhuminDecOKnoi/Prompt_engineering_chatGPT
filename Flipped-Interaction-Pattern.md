# 🔁 Flipped Interaction Pattern  
**รูปแบบการโต้ตอบกลับด้าน (Flipped Interaction Prompt Design)**

> **EN Description:**  
> This prompt pattern reverses the traditional role—LLM asks questions to gather info before generating an output. This helps when users aren’t sure how to structure prompts or what info is needed.  

> **TH คำอธิบาย:**  
> รูปแบบพรอมต์นี้เปลี่ยนบทบาทจากที่ผู้ใช้เป็นผู้ถาม ให้โมเดลภาษาขนาดใหญ่ (LLM) เป็นฝ่ายสอบถามเพื่อรวบรวมข้อมูลก่อนให้คำตอบ เหมาะสำหรับสถานการณ์ที่ผู้ใช้ไม่แน่ใจว่าจะเริ่มคำสั่งอย่างไร

---

## 🧩 Format (รูปแบบพื้นฐานของคำสั่ง)

**EN Format:**

I would like you to ask me questions to achieve [X].  
Ask questions until [Y]. Ask me the first question.
ฉันต้องการให้คุณถามฉันคำถามเพื่อให้บรรลุ [X]  
ถามคำถามจนกระทั่ง [Y] ถามคำถามแรกมาเลย
I would like you to ask me questions to help me create variations of my marketing materials.  
You should ask questions until you have sufficient information about my current draft messages, audience, and goals. Ask me the first question.

I would like you to ask me questions to help me diagnose a problem with my Internet.  
Ask me questions until you have enough information to identify the two most likely causes. Ask me one question at a time. Ask me the first question.
ฉันต้องการให้คุณถามฉันคำถามเพื่อช่วยฉันสร้างรูปแบบใหม่ ๆ ให้กับสื่อการตลาดของฉัน  
ถามฉันจนกว่าคุณจะมีข้อมูลเพียงพอเกี่ยวกับข้อความฉบับร่างในปัจจุบัน กลุ่มเป้าหมาย และวัตถุประสงค์  
ถามคำถามแรกมาเลย

ฉันต้องการให้คุณช่วยวิเคราะห์ปัญหาอินเทอร์เน็ตโดยการถามคำถาม  
ถามทีละคำถามจนกว่าคุณจะระบุได้ว่าสาเหตุที่เป็นไปได้ 2 อันดับแรกคืออะไร  
ถามคำถามแรกมาเลย
{
  "role": "user",
  "content": "I would like you to ask me questions to achieve [X]. Ask questions until [Y]. Ask me the first question."
}
```text
