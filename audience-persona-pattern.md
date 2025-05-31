# 🗣️ Audience Persona Pattern (Prompt Engineering)

> **Description:**  
> A prompt pattern where you ask the AI to explain a concept (X) assuming the user has a specific persona (Y). This helps tailor tone, depth, and language to the audience's background—great for education, roleplay, or accessibility use cases.

---

## 📌 Prompt Format

| Element         | Description                                              | Example                                         |
|------------------|----------------------------------------------------------|--------------------------------------------------|
| Topic X          | Concept you want the AI to explain                      | `large language models`, `supply chains`        |
| Persona Y        | Audience's identity, background, or role                | `a bird`, `Genghis Khan`, `a 5-year-old child`  |

---

## 🧪 Prompt Examples

| Prompt | Description |
|--------|-------------|
| `Explain large language models to me. Assume that I am a bird.` | 🐦 Uses metaphorical language, simplifies tech terms |
| `Explain how the supply chains for US grocery stores work to me. Assume that I am Genghis Khan.` | 🏇 Uses historical references, avoids modern jargon |

---

## 🎯 Benefits

| Benefit                         | Explanation |
|----------------------------------|-------------|
| 🎨 Personalization                | Adapts tone and content to suit listener |
| 📚 Educational Versatility        | Ideal for explaining complex topics to novices |
| 🧩 Creative Roleplay              | Supports storytelling and fictional scenarios |
| 🧠 Enhanced Understanding         | Engages users through relatable perspectives |

---

## ✅ Tips for Use

- Be specific with personas (e.g., “a first-year law student” instead of just “student”)
- Can be combined with other patterns (e.g., Output Format or Cognitive Verifier)
- Great for creating engaging educational or onboarding materials

---

## 🔁 JSON Template

```json
{
  "role": "user",
  "content": "Explain [Topic X] to me. Assume that I am [Persona Y]."
}
