# 📘 How the Chatbot LibroBot Works

This chatbot is designed to simulate an intelligent book assistant using IBM Watsonx Assistant.

---

## 🔧 Modules Created

### 1. Intents
- `recommend_by_genre`
- `recommend_by_mood`
- `recommend_by_level`
- `recommend_by_author`
- `top_books`
- `thank_you`
- `goodbye`
- `fallback`

### 2. Entities
- `@genre`: mystery, romance, thriller, sci-fi, etc.
- `@mood`: sad, happy, bored, excited
- `@reading_level`: beginner, intermediate, advanced

---

## 🔄 Dialog Flow Logic

- Main parent node: `recommend_book`
  - Skip user input ✅
  - Has child nodes like:
    - `@genre:mystery` → Mystery suggestions
    - `@mood:sad` → Uplifting books
    - `@reading_level:beginner` → Easy reads
    - `"dan brown" in input.text` → Author-specific

- Fallback node handles:
  - Unmatched input
  - Guides user with example commands

---

## 🧪 Sample Inputs You Can Try

| User Says                           | Bot Response                       |
|------------------------------------|------------------------------------|
| "Suggest a romance book"           | Romance suggestions                |
| "I'm sad, give me a book"          | Mood: Sad → uplifting book         |
| "Any good sci-fi?"                 | Sci-fi recommendation              |
| "I'm a beginner reader"            | Beginner-level suggestions         |
| "Thanks!"                          | Gratitude response                 |
| "Bye"                              | Goodbye + ending note              |

---

## ✅ Deployment Summary

- Entirely built inside Watsonx Assistant
- Exported as `.json` for easy import/share
- Submitted with GitHub repo for evaluation
