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
├── app.py
├── db_manager.py
├── user_manager.py
├── report_generator.py
├── wizard_config.json
├── db_config.json
├── translations.json
│
├── templates/
│   ├── base.html
│   ├── wizard.html
│   ├── login.html
│   ├── admin_list.html
│   ├── admin_edit.html
│   ├── admin_users.html
│   └── admin_add_user.html
│
├── steps/
│   ├── step1.md
│   ├── step2.html
│   └── step3.md
│
├── logic/
│   ├── step1.py
│   ├── step2.py
│   └── step3.py
│
└── static/
    ├── style.css
    └── logo.png
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
