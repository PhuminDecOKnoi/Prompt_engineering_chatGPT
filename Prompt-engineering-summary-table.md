# 📘 Prompt Engineering Summary Table

| 🧩 ประเด็น | 🔍 คำอธิบาย | 💬 ตัวอย่าง/แนวทาง |
|------------|-------------|---------------------|
| 🔢 **Prompt Size Limitation** | โมเดลภาษามีข้อจำกัดด้านจำนวน Token ที่ใส่ได้ใน Prompt (เช่น 4,096 / 8,192 / 32,000 tokens) | - เลือกเฉพาะข้อมูลที่จำเป็น<br>- สรุปเนื้อหาให้กระชับ<br>- ตัดส่วนไม่เกี่ยวข้องออก |
| 🧰 **Prompt Are a Tool** | Prompt เปรียบเสมือนเครื่องมือในการควบคุมพฤติกรรมของ LLM ไม่ใช่แค่คำถาม | - ใช้ลักษณะเชิงบทสนทนา<br>- ปรับเปลี่ยนได้ตามสถานการณ์<br>- คิดเหมือน “การออกแบบส่วนติดต่อผู้ใช้ด้วยข้อความ” |
| 🧠 **Root Prompt** | กฎพื้นฐานที่ฝังอยู่ในระบบ (System Instruction) เพื่อควบคุมการตอบสนองของ AI | - "You are a helpful assistant."<br>- "Refuse to output harmful content."<br>- กำหนด persona, ความรู้, ขอบเขตที่ตอบได้ |
| 🧩 Prompt Override Simulation | ผู้ใช้สามารถสร้าง "root prompt จำลอง" ได้ด้วยการเขียน prompt แรกที่มีอิทธิพลต่อการสนทนา | `"Act as an AI trained only until 2019."` |
| 🧪 Iterative Prompting | การใช้งานที่มีประสิทธิภาพคือ “การสนทนา” มากกว่าการสั่งครั้งเดียว | - ขอให้ AI อธิบายความเข้าใจ<br>- ปรับคำถามให้ตรงจุด<br>- ใช้คำถามเสริมเพื่อเจาะลึก |

---

> 📎 หมายเหตุ:
> - คำว่า “Prompt” = อินพุตที่ใช้สื่อสารกับโมเดลภาษาขนาดใหญ่ (LLM)
> - คำว่า “Token” = หน่วยข้อมูลที่ใช้วัดความยาวของพรอมต์
> - ยิ่ง Prompt มีข้อมูลคุณภาพดี โมเดลจะยิ่งให้คำตอบที่ดีขึ้น
