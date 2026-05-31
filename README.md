# 🌌 UPOS Interactive Quiz

An interactive web application designed to help learners and linguistic enthusiasts master the **Universal Part-of-Speech (UPOS)** tagset. Built with a sleek, premium dark-mode interface, rich responsiveness, and comprehensive hotkey navigation.

🚀 **Live Demo**: [upos-quiz.vercel.app](https://upos-quiz.vercel.app)

---

## 🌟 Key Features

- **Interactive Word-by-Word Tagging**: Each sentence is parsed into separate tokens. Select the correct UPOS tag for each word using elegant dropdown controls.
- **Instant Linguistic Feedback**: Receive real-time assessment of your selections. Correct answers turn green, incorrect ones turn red, and a detailed markdown-formatted linguistic breakdown explains the syntax and grammar rules behind each sentence.
- **Difficulty Grading**: Sentences are grouped into three distinct categories:
  - **🟢 Simple**: Foundational sentence structures (Sentences 1–15).
  - **🟡 Hard**: Challenging sentences with more complex nesting (Sentences 16–50).
  - **💗 Tricky**: Sentences featuring idiomatic expressions, homonyms, and subtle linguistic traps (Sentences 51–100).
- **Live Statistics & Tracking**: Track your accuracy score and total progress in real time as you complete the sentences.
- **Universal Tags Reference**: A convenient, scrollable reference list for all 17 Universal POS tags is accessible directly from the sidebar.
- **Custom Sentence Navigator**: Jump to any specific sentence instantly using the overlay navigator.

---

## 🎹 Keyboard Shortcuts

Boost your efficiency by navigating the quiz entirely from your keyboard:

| Shortcut | Action |
| :--- | :--- |
| `ArrowLeft` | Go to the previous sentence |
| `ArrowRight` | Go to the next sentence |
| `ArrowLeft` / `ArrowRight` | Move focus between adjacent word dropdowns (when a dropdown is active) |
| `Enter` or `Space` | Check answers for the current sentence |
| `S` | Toggle randomized sentence ordering (**Shuffle**) |
| `G` | Open the **Jump to Sentence** overlay |

---

## 🚀 Getting Started

Because the application fetches the quiz dataset asynchronously from a local file (`data.json`), modern browsers require the project to be run via a local web server (instead of opening `index.html` directly via the `file://` protocol).

### Options to Run Locally

#### Option 1: Using Python (Simplest)
Open your terminal in the repository directory and run:
```bash
python3 -m http.server 8000
```
Then, visit `http://localhost:8000` in your web browser.

#### Option 2: Live Server (VS Code Extension)
1. Open the repository in Visual Studio Code.
2. Install the **Live Server** extension.
3. Click the **Go Live** button in the status bar (starts at port `5500` by default).

---

## 📊 Dataset Schema

The quiz dynamically renders questions using the clean JSON structure defined in `data.json`. Below is an example structure:

```json
[
  {
    "id": 1,
    "difficulty": "simple",
    "text": "The dog barked at the cat .",
    "tokens": [
      { "word": "The", "tag": "DET" },
      { "word": "dog", "tag": "NOUN" },
      { "word": "barked", "tag": "VERB" },
      { "word": "at", "tag": "ADP" },
      { "word": "the", "tag": "DET" },
      { "word": "cat", "tag": "NOUN" },
      { "word": ".", "tag": "PUNCT" }
    ],
    "explanation": "🔍 **Linguistic Breakdown:** *The dog* is the subject (the one performing the action), and *barked* is the action verb..."
  }
]
```

---

## 🎨 Tech Stack

- **Core**: HTML5, Vanilla JavaScript (ES6+)
- **Styling**: Modern CSS3 (featuring HSL variables, custom glassmorphism, smooth animations, and responsive flexbox/grid layout)
- **Typography**: Google Fonts (*Outfit* and *Plus Jakarta Sans*)