# Wizard Application

[![Python](https://img.shields.io/badge/python-3.9%2B-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/flask-2.0%2B-green.svg)](https://flask.palletsprojects.com/)
[![License](https://img.shields.io/badge/license-MIT-yellow.svg)](LICENSE)
[![Made with Markdown](https://img.shields.io/badge/content-Markdown-lightgrey.svg)](https://daringfireball.net/projects/markdown/)

A configurable multi-step wizard built with **Flask**.  
Each step can display Markdown/HTML content and run custom Python logic.  
The application supports user authentication, admin tools, multi-language UI, PDF report generation, and company branding.

---

## ✨ Features

- 🧩 **Multi-step wizard** with forward/backward navigation  
- 📝 **Markdown/HTML** content for each step  
- ⚙️ **Step-specific Python logic** for validation and execution  
- 🔒 **User authentication** with hashed passwords (SQLite backend)  
- 👨‍💼 **Admin panel** to manage users and JSON configuration files  
- 🌍 **Multi-language support** (English, Italian by default)  
- 📄 **PDF report generation** with configurable output path and timestamped filename  
- 🏢 **Company branding** with configurable logo  

---

## 📂 Project Structure

```
wizard_app/
│
├── app.py               # Main Flask app
├── db_manager.py        # Database responses manager
├── user_manager.py      # User management (SQLite + password hashing)
├── report_generator.py  # PDF generation
├── wizard_config.json   # Wizard configuration
├── db_config.json       # DB backend config
├── translations.json    # UI translations
│
├── templates/           # HTML templates (wizard, login, admin, base)
├── steps/               # Step contents (Markdown/HTML)
├── logic/               # Python logic for each step
└── static/              # Static files (CSS, logo, etc.)
```

---

## 🚀 Getting Started

### 1. Clone repository
```bash
git clone https://github.com/YOUR-USERNAME/wizard-app.git
cd wizard-app
```

### 2. Install dependencies
```bash
pip install flask markdown reportlab mysql-connector-python psycopg2-binary
```

### 3. Run the app
```bash
python app.py
```

Open [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

---

## ⚙️ Configuration

- **`wizard_config.json`** → steps, language, report path, logo, auto-login  
- **`db_config.json`** → database backend (SQLite/MySQL/Postgres)  
- **`translations.json`** → UI translations  
- **`static/logo.png`** → replace with your company logo  

---

## 🛡️ Security Notes

- Change `app.secret_key` in `app.py` before production use  
- Change default admin password (`admin123`) immediately  
- Consider enabling HTTPS in production  

---

## 📄 License

MIT License.  
Feel free to use, modify, and distribute.
