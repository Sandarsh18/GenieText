
# 🌐 Multi-Language Translator

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-Web_Framework-lightgrey?logo=flask)](https://flask.palletsprojects.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Web Speech API](https://img.shields.io/badge/Web%20Speech%20API-Supported-yellow)](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API)

> A beautiful and responsive web application built with Python and Flask that translates text between multiple languages, with a special focus on 11 Indian languages. It uses the `deep-translator` library to interface with the Google Translate API. Key features include a modern UI, specialized fonts for Indic scripts, and client-side text-to-speech functionality using the Web Speech API.

---

## ✨ Features

- 🌍 **Multi-language Support**: 11 Indian languages supported
- 🔊 **Text-to-Speech**: Listen to translated text in the correct accent
- 🎨 **Beautiful UI**: Modern responsive design with animations and gradients
- 🖋️ **Optimized Fonts**: Noto Sans for crisp Indic script rendering
- ⚡ **Real-time Translation**: Powered by Google Translate via deep-translator
- 🧭 **Interactive Controls**: Swap, copy, clear, and listen functionalities
- 🆎 **Font Testing**: Built-in Kannada font rendering tester
- 📱 **Responsive Design**: Works great on mobile and desktop
- 🧠 **Error Handling**: Friendly user messages and validations

---

## 🧰 Tech Stack

| Layer        | Technology |
|--------------|------------|
| Backend      | Python, Flask |
| Frontend     | HTML5, CSS3, JavaScript (ES6+) |
| Fonts        | Google Fonts (Noto Sans) |
| Translation  | deep-translator, Google Translate API |
| TTS          | Web Speech API (client-side) |

---

## 📂 File Structure

```
Gen AI/
├── app.py
├── requirement.txt
└── templates/
    └── index.html
```

---

## 🚀 Setup & Usage

### 🔧 Prerequisites
- Python 3.7+
- `pip` package manager

### ⚙️ Installation
```bash
# Clone the repo
git clone <repo-url>
cd Gen\ AI/

# Install dependencies
pip install -r requirement.txt
```

### ▶️ Run the App
```bash
python app.py
```
Visit: [http://localhost:5000](http://localhost:5000)

---

## 📡 API Endpoints

| Method | Endpoint           | Description                            |
|--------|--------------------|----------------------------------------|
| GET    | `/`                | Renders the translator interface       |
| POST   | `/translate`       | Handles translation request            |
| GET    | `/test_kannada`    | Returns sample Kannada text            |

#### Example Request (POST `/translate`)
```json
{
  "text": "Hello",
  "source_lang": "English",
  "target_lang": "Hindi"
}
```

#### Example Response
```json
{
  "success": true,
  "translated_text": "नमस्ते",
  "target_lang_speech_code": "hi-IN"
}
```

---

## 🗣️ Supported Languages

| Language   | Code | Speech Code |
|------------|------|-------------|
| English    | en   | en-US       |
| Hindi      | hi   | hi-IN       |
| Kannada    | kn   | kn-IN       |
| Tamil      | ta   | ta-IN       |
| Telugu     | te   | te-IN       |
| Bengali    | bn   | bn-IN       |
| Marathi    | mr   | mr-IN       |
| Gujarati   | gu   | gu-IN       |
| Malayalam  | ml   | ml-IN       |
| Punjabi    | pa   | pa-IN       |
| Urdu       | ur   | ur-IN       |

---

## 🌐 Browser Compatibility

| Browser   | Logo | Version |
|-----------|------|---------|
| Chrome    | ![chrome](https://img.icons8.com/color/24/chrome.png) | 70+ |
| Firefox   | ![firefox](https://img.icons8.com/color/24/firefox.png) | 65+ |
| Safari    | ![safari](https://img.icons8.com/color/24/safari.png) | 12+ |
| Edge      | ![edge](https://img.icons8.com/color/24/ms-edge-new.png) | 79+ |

> 🔔 **Note**: Text-to-speech support depends on each browser's Web Speech API implementation.

---

## 🛠️ Deployment

### 🧪 Local Development
```bash
python app.py
```

### ⚙️ Production (Gunicorn + Nginx)
```bash
pip install gunicorn
gunicorn -w 4 -b 0.0.0.0:5000 app:app
```

---

## 🤝 Contributing

1. Fork this repository
2. Create a new feature branch (`git checkout -b feature-name`)
3. Make your changes and commit (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature-name`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the **MIT License**.

---

## 🐛 Known Issues

- Translation accuracy depends on Google Translate API.
- Font rendering may vary across operating systems.
- TTS voices depend on the browser's capabilities.

---

## 🔮 Future Enhancements

- [x] Add text-to-speech functionality
- [ ] Add more Indian and international languages
- [ ] Translation history with export option
- [ ] File upload for document translation
- [ ] User authentication for personal preferences
- [ ] Offline translation using local models
- [ ] Confidence scores for translations

---

## ❤️ Final Note

**Made with ❤️ for multilingual communication**

