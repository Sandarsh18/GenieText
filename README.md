🌐 Multi-Language Translator
<p align="center">
<img src="https://img.shields.io/badge/python-3.7+-blue.svg" alt="Python Version">
<img src="https://img.shields.io/badge/license-MIT-green.svg" alt="License">
</p>


A beautiful and responsive web application for translating text between multiple Indian languages using the Google Translate API. This application is built with Flask and modern web technologies, and now includes text-to-speech for translated output.

✨ Features

🌐 Multi-language Support: Translate between 11 languages including Hindi, Kannada, Tamil, Telugu, Bengali, English, Marathi, Gujarati, Malayalam, Punjabi, and Urdu.

🔊 Text-to-Speech: Listen to the translated text with a single click, supporting language-specific pronunciations via the Web Speech API.

🎨 Beautiful UI: Modern, responsive design with gradient backgrounds and smooth animations.

✒️ Font Support: Optimized typography for Indic scripts with the Noto Sans font family.

⚡ Real-time Translation: Fast and accurate translations powered by Google Translate.

🎛️ Interactive Controls: Language swap, copy to clipboard, and clear functions.

📝 Font Testing: Built-in Kannada font testing feature to ensure proper rendering.

💻📱 Responsive Design: Works seamlessly on desktop and mobile devices.

🛡️ Error Handling: Comprehensive error handling with user-friendly messages.

🛠️ Tech Stack
<p align="center">
<a href="https://www.python.org" target="_blank">
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
</a>
<a href="https://flask.palletsprojects.com/" target="_blank">
<img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
</a>
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML" target="_blank">
<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
</a>
<a href="https://developer.mozilla.org/en-US/docs/Web/CSS" target="_blank">
<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
</a>
<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank">
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
</a>
</p>

🚀 Quick Start
Prerequisites

Python 3.7 or higher

pip package manager

A modern web browser with Web Speech API support (e.g., Chrome, Firefox, Edge)

Installation

Clone or download the project files

Generated bash
# Create project directory
mkdir multi-language-translator
cd multi-language-translator


Set up the project structure

Generated code
Gen AI/
├── 📂 templates/
│   └── index.html      # Frontend template
├── 🐍 app.py              # Main Flask application
└── 📋 requirement.txt      # Dependencies
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
IGNORE_WHEN_COPYING_END

Install dependencies

Generated bash
pip install -r requirement.txt
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

Run the application

Generated bash
python app.py
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

Open in your browser
http://localhost:5000

📦 Dependencies

The application requires the following Python packages:

Generated code
Flask==2.3.3
deep-translator==1.11.4
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
IGNORE_WHEN_COPYING_END
🎯 Usage
Basic Translation

Select Source Language: Choose the language of your input text.

Select Target Language: Choose the language you want to translate to.

Enter Text: Type or paste your text in the input area.

Translate: Click "Translate" or press Ctrl+Enter.

Listen to Result: Click the "🔊 Listen" button to hear the translation.

Copy Result: Use the "Copy Result" button to copy the translation.

Advanced Features

Language Swap: Click the ⇄ button to quickly swap source and target languages.

Font Selection: Choose from different Noto Sans fonts for better Indic script display.

Kannada Testing: Use the "Test Kannada" button to verify font rendering.

Clear All: Reset both input and output areas.

🔧 API Endpoints
GET /

Description: Renders the main translator page.

Response: HTML page with the translator interface.

POST /translate

Description: Handles translation requests.

Request Body:

Generated json
{
  "text": "Text to translate",
  "source_lang": "English",
  "target_lang": "Hindi"
}
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Json
IGNORE_WHEN_COPYING_END

Response:

Generated json
{
  "success": true,
  "translated_text": "Translated text",
  "source_lang": "English",
  "target_lang": "Hindi",
  "target_lang_speech_code": "hi-IN"
}
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Json
IGNORE_WHEN_COPYING_END
GET /test_kannada

Description: Returns sample Kannada text for font testing.

Response:

Generated json
{
  "sample_text": "Sample Kannada text",
  "message": "Kannada font test sample"
}
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Json
IGNORE_WHEN_COPYING_END
🌍 Supported Languages
Language	Code	Speech Code	Script
English	en	en-US	Latin
Hindi	hi	hi-IN	Devanagari
Kannada	kn	kn-IN	Kannada
Tamil	ta	ta-IN	Tamil
Telugu	te	te-IN	Telugu
Bengali	bn	bn-IN	Bengali
Marathi	mr	mr-IN	Devanagari
Gujarati	gu	gu-IN	Gujarati
Malayalam	ml	ml-IN	Malayalam
Punjabi	pa	pa-IN	Gurmukhi
Urdu	ur	ur-IN	Arabic
🚀 Deployment
Local Development
Generated bash
python app.py
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

The application will run on http://localhost:5000 with debug mode enabled.

Production Deployment

For production deployment, consider:

Using a WSGI server like Gunicorn.

Setting up a reverse proxy with Nginx.

Configuring environment variables.

Implementing proper logging.

Example with Gunicorn:

Generated bash
pip install gunicorn
gunicorn -w 4 -b 0.0.0.0:5000 app:app
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END
📱 Browser Compatibility
Browser	Compatibility
<img src="https://raw.githubusercontent.com/alrra/browser-logos/main/src/chrome/chrome_48x48.png" alt="Chrome" width="24">	Chrome 70+
<img src="https://raw.githubusercontent.com/alrra/browser-logos/main/src/firefox/firefox_48x48.png" alt="Firefox" width="24">	Firefox 65+
<img src="https://raw.githubusercontent.com/alrra/browser-logos/main/src/safari/safari_48x48.png" alt="Safari" width="24">	Safari 12+
<img src="https://raw.githubusercontent.com/alrra/browser-logos/main/src/edge/edge_48x48.png" alt="Edge" width="24">	Edge 79+

Text-to-speech functionality relies on browser implementation of the Web Speech API.

🤝 Contributing

Fork the project.

Create a feature branch.

Make your changes.

Test thoroughly.

Submit a pull request.

📄 License

This project is open source and available under the MIT License.

🐛 Known Issues

Translation accuracy depends on the Google Translate API.

Some complex text formatting may not be preserved.

Font rendering may vary across different operating systems.

Availability of high-quality voices for the Web Speech API depends on the user's browser and OS.

🆘 Support

For issues or questions:

Check the browser console for error messages.

Verify your internet connection for the translation API.

Ensure all dependencies are properly installed.

Check Python version compatibility.

🔮 Future Enhancements

Add more languages

Implement offline translation

Add text-to-speech functionality

Include translation history

Add file upload support

Implement user authentication

Add translation confidence scores

Support for document translation

Made with ❤️ for multilingual communication
