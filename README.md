# WebAssistant · AI-powered web companion

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen?style=for-the-badge&logo=vercel)](https://your-demo-link.vercel.app)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

> **A sleek, responsive, and interactive AI assistant interface** — built with pure HTML, CSS, and vanilla JavaScript. No frameworks, no dependencies. Just a smart chat UI ready to integrate with your backend or use as a standalone demo.

![WebAssistant Screenshot](screenshot.png) <!-- Replace with actual screenshot -->

---

##  Features

-  **Smart chat interface** with contextual responses (keyword-based logic)
-  **Glassmorphism design** — modern, clean, and visually appealing
-  **Fully responsive** — works flawlessly on desktop, tablet, and mobile
-  **Quick action buttons** for instant questions (Trends, CSS Grid, SEO, HTTP vs HTTPS)
-  **Keyboard shortcuts** — hit `Enter` to send messages
-  **Timestamped messages** for both user and assistant
-  **Privacy-first** — no data storage, no external tracking
-  **Beautiful animations** — smooth transitions and micro-interactions
-  **Extensible** — easily swap the response logic to call any LLM API (OpenAI, Claude, Gemini, etc.)

---

## 🚀 Live Demo

Check out the live demo here: [**WebAssistant Live**](https://your-demo-link.vercel.app)

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **HTML5** | Semantic structure |
| **CSS3** | Glassmorphism, responsive design, animations |
| **Vanilla JavaScript** | Dynamic chat, event handling, logic |
| **Font Awesome** | Icon library for clean UI elements |

**No build tools, no package managers, no frameworks.** Open `index.html` and it runs.

---

## 📦 Installation

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/webassistant.git
cd webassistant
```

### 2. Open the project
Simply open `index.html` in your favorite browser.

```bash
# On macOS
open index.html

# On Windows
start index.html

# On Linux
xdg-open index.html
```

That's it! No installation, no dependencies.

---

## 🧩 Customization

### 🤖 Change the Assistant's Personality
Edit the `getAssistantReply()` function in the `<script>` section (around line 240). You can add more keywords, integrate with an external API, or even replace it with a call to OpenAI's GPT.

```javascript
function getAssistantReply(userText) {
  // Add your custom logic here
  if (userText.includes('your keyword')) {
    return 'Your custom response';
  }
  // ...
}
```

### 🎨 Styling
Modify the CSS variables in the `<style>` section to match your brand colors.

```css
:root {
  --primary: #2a7de1;
  --glass-bg: rgba(255, 255, 255, 0.7);
  /* ... */
}
```

### ➕ Add Quick Actions
Add new buttons in the `.quick-actions` div:

```html
<button class="quick-btn" data-prompt="Your prompt here">
  <i class="fas fa-icon"></i> Button Label
</button>
```

---

## 📂 Project Structure

```
webassistant/
├── index.html          # Full application (HTML + CSS + JS)
├── screenshot.png      # Optional: preview image
├── LICENSE             # MIT License
└── README.md           # This file
```

---

## 🔌 Integration with Real AI APIs

To connect this UI to a real LLM (OpenAI, Claude, Gemini, etc.):

1. Replace the `getAssistantReply()` function with an `async` function that calls your API.
2. Add your API key (server-side only — never expose keys in frontend code).
3. Handle loading states and errors.

Example with OpenAI (using `fetch`):
```javascript
async function getAssistantReply(userText) {
  const response = await fetch('/api/chat', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ message: userText })
  });
  const data = await response.json();
  return data.reply;
}
```

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please ensure your code follows the existing style and is well-documented.

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- [Font Awesome](https://fontawesome.com/) for the beautiful icons
- The open-source community for inspiration
- Glassmorphism design trend for the aesthetic

---

## 📬 Contact

- **Your Name** — [@yourtwitter](https://twitter.com/yourtwitter) — email@example.com
- Project Link: [https://github.com/yourusername/webassistant](https://github.com/yourusername/webassistant)

---

## ⭐ Show Your Support

If you found this helpful, please give it a ⭐ on GitHub — it helps a lot!

---

**Built with ❤️ for the developer community.**
```
