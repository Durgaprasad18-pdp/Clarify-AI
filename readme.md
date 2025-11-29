# 🧠 AI Summary for Articles — Chrome Extension (ClarifyAI)

A Chrome extension that extracts text from any webpage and generates **brief, detailed, or bullet-point summaries** using **Google Gemini AI**. Useful for quickly understanding articles, blogs, research papers, and long online content.

---

## 🚀 Features

- One-click article summarization  
- Supports **Brief**, **Detailed**, and **Bullet-Point** summaries  
- Automatically extracts article text from webpages  
- Uses **Google Gemini API (gemini-2.5-flash)**  
- **Copy Summary** button  
- Saves user’s API key securely via Chrome Storage  
- Works on **all websites**

---

## 📁 Project Structure

📦 AI Summary Chrome Extension
├── background.js
├── content.js
├── manifest.json
├── options.html
├── options.js
├── popup.html
├── popup.js
└── AI.png

2. Load into Chrome:
a.Open chrome://extensions
b.Toggle Developer mode
c.Click Load unpacked
d.Select the project folder

--->🔑 Add Your Gemini API Key:

a.The extension automatically opens the Settings page on first install

b.Enter your Google Gemini API key

c.Click Save Settings

Get your API key here:
https://makersuite.google.com/app/apikey



------> 📝 How It Works
1. Extracts text

Content script collects text from:

<article> elements

OR all <p> elements (fallback)

2. Sends text to Gemini

The popup calls:

gemini-2.5-flash:generateContent


--->Prompt varies based on summary type:

a.Brief summary

b.Detailed summary

c.5–7 bullet points (- prefix)

3. Displays summary

Summary appears instantly in the popup, with a Copy button.


| Mode              | Description                 |
| ----------------- | --------------------------- |
| **Brief**         | 2–3 sentence summary        |
| **Detailed**      | Full, detailed explanation  |
| **Bullet Points** | 5–7 key insights using `- ` |


--->⚙️ Tech Used:

a.JavaScript

b.Chrome Extensions API (Manifest V3)

c.HTML + CSS

d.Google Gemini API

e.Background Service Worker

f.Content Script

g.Popup UI


--->⚠️ Limitations

a.Text is truncated at 20,000 characters for API limits

b.Requires internet access

c.Only supports Google Gemini API keys


--->📌 Possible Future Improvements

a.Add OpenAI / Anthropic model support

b.Add text-selection “Right-Click → Summarize” option

c.Add history of summaries

d.Add dark mode


--->🤝 Contributing

Pull requests and suggestions are welcome.

--->📄 License

MIT License
Free to use, modify, and distribute.