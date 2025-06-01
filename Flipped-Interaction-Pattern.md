# 🔁 Flipped Interaction Pattern  
**รูปแบบการโต้ตอบกลับด้าน**

> **EN Description:**  
> This prompt pattern reverses the traditional interaction. Instead of the user asking the question, the **LLM becomes the one asking questions** in order to gather enough information before generating a final output.  

> **TH คำอธิบาย:**  
> รูปแบบพรอมต์นี้จะสลับบทบาทของผู้ใช้และโมเดลภาษา โดยให้ **LLM เป็นฝ่ายถามคำถามกับผู้ใช้** เพื่อเก็บข้อมูลที่จำเป็นก่อนสร้างคำตอบสุดท้าย เหมาะอย่างยิ่งในกรณีที่ผู้ใช้ไม่แน่ใจว่าจะเริ่มอย่างไร

---

## 🧩 Prompt Structure  
**EN Format:**


> Ask me questions about [topic] until you have enough information to [goal]. Ask me the first question.
> ถามฉันเกี่ยวกับ [หัวข้อ] จนกว่าคุณจะมีข้อมูลเพียงพอที่จะ [เป้าหมาย] ถามคำถามแรกมาเลย
> Ask me questions about fitness goals until you have enough information to suggest a strength training regimen for me. Ask me the first question.

> Ask me questions about what type of story I’d like to read. When you have enough information, write me a short story. Ask me the first question.

> Ask me questions about the ingredients I have in my kitchen. When you have enough information, suggest a recipe I can cook with them. Ask me the first question.
> ถามฉันเกี่ยวกับเป้าหมายด้านฟิตเนสจนกว่าคุณจะมีข้อมูลเพียงพอที่จะเสนอแผนการฝึกกล้ามเนื้อ ถามคำถามแรกมาเลย

> ถามฉันเกี่ยวกับประเภทของเรื่องที่ฉันอยากอ่าน เมื่อคุณมีข้อมูลเพียงพอ ให้เขียนเรื่องสั้นให้ฉัน ถามคำถามแรกมาเลย

> ถามฉันเกี่ยวกับวัตถุดิบที่ฉันมีในครัว เมื่อคุณมีข้อมูลเพียงพอ ให้แนะนำสูตรอาหารที่ฉันสามารถทำได้ ถามคำถามแรกมาเลย
#{
 # "role": "user",
 # "content": "Ask me questions about [topic] until you have enough information to [goal]. Ask me the first question."
#}
# Perez, E., Ribeiro, M. T., & Eisenschlos, J. (2023). A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT. arXiv. https://arxiv.org/abs/2302.11382
