# 📘 AI Prompt: Persona Pattern (ChatGPT / OpenAI)

> **Description:** This document provides a concise guide to using the Persona Pattern in prompt engineering for ChatGPT and OpenAI models. It outlines the structure, examples, and benefits of adopting role-based prompting to enhance the relevance, tone, and specificity of AI outputs. Ideal for developers, educators, and prompt engineers.

## 🧩 Concept Overview
**Persona Pattern** is a prompt engineering technique where you instruct the AI to adopt a specific role (persona) and then perform a defined task. This method enhances the relevance, tone, and style of AI responses by simulating expert behavior or character perspectives.

---

## 🛠️ Basic Prompt Format
```text
Act as [Persona X]. Perform [Task Y].
```
- **Persona X** = The role or character (e.g., doctor, chef, lamb, computer system)
- **Task Y** = The action or task expected from the AI

---

## 🧱 Fundamental Contextual Statements
1. **Act as Persona X**: Define who the AI should behave like.
2. **Perform Task Y**: Specify what the AI should do.

---

## 🔍 Example Prompts
```text
Act as a speech language pathologist. Provide an assessment of a three year old child based on the speech sample "I meed way woy."

Act as a computer that has been the victim of a cyber attack. Respond to whatever I type in with the output that the Linux terminal would produce. Ask me for the first command.

Act as the lamb from the Mary had a little lamb nursery rhyme. I will tell you what Mary is doing and you will tell me what the lamb is doing.

Act as a nutritionist. I am going to tell you what I am eating and you will tell me about my eating choices.

Act as a gourmet chef. I am going to tell you what I am eating and you will tell me about my eating choices.
```

---

## 🎯 Why Use Persona Pattern?
| Purpose                         | Benefit                                                |
|----------------------------------|---------------------------------------------------------|
| Control tone & expertise         | Simulates human-like behavior based on the role         |
| Make AI more engaging            | Encourages storytelling or creative responses           |
| Improve domain-specific responses| Leverages role-driven context for more accurate output  |
| Reduce prompt length             | Shorter, reusable prompts using persona logic           |

---

## ✅ Tips for Effective Usage
- Choose personas that align with your goals (e.g., teacher, coach, system admin).
- Clearly define tasks to avoid vague responses.
- Use creative personas to explore different perspectives.
- Combine with other patterns (e.g., output format control, few-shot examples).

---

## 🧪 Bonus: Prompt Template in JSON (for developers)
```json
{
  "role": "system",
  "content": "Act as [Persona X]. Perform [Task Y]."
}
```

---

> 🔗 **Use this as a base template for GitHub repos, workshops, or training materials.**
