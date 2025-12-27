# Inventory Management System (Django) 📦

A Django-based Inventory Management System for managing products, stock, and users with a clean dashboard-style UI.

---


https://github.com/user-attachments/assets/40b8ec7e-0025-4f28-b752-ab70a7b2c117



## ✨ Features
- Product & stock management
- User authentication (login/register) *(if enabled)*
- Role-based access via Django Admin / users app *(if configured)*
- Dashboard UI with templates + static assets
- SQLite database for quick local setup

> Exact features depend on how `store/` and `users/` apps are implemented in this project.

---

## 🧰 Tech Stack
- Python 3.x
- Django
- SQLite (default local DB)
- Django Templates (HTML/CSS/JS)
- Static assets in `static/`

---

## 📁 Project Structure
.
├── manage.py
├── requirements.txt
├── db.sqlite3
├── inventory/ # project settings / urls / wsgi
├── store/ # inventory/store logic (products, stock, etc.)
├── users/ # authentication/user-related features
├── templates/ # HTML templates
└── static/ # CSS/JS/images/vendor assets

yaml
Copy code

---

## ✅ Prerequisites
- Python 3.9+ recommended
- pip

Check versions:
```bash
python --version
pip --version
🚀 Local Setup (Mac / Linux / Windows)
1) Clone the repo
bash
Copy code
git clone <YOUR_GITHUB_REPO_URL>
cd <REPO_FOLDER>
2) Create & activate virtual environment
macOS/Linux

bash
Copy code
python3 -m venv .venv
source .venv/bin/activate
Windows (PowerShell)

powershell
Copy code
py -m venv .venv
.\.venv\Scripts\Activate.ps1
3) Install dependencies
bash
Copy code
pip install --upgrade pip
pip install -r requirements.txt
4) Apply migrations
bash
Copy code
python manage.py makemigrations
python manage.py migrate
5) Create admin user (recommended)
bash
Copy code
python manage.py createsuperuser
6) Run the development server
bash
Copy code
python manage.py runserver
Open:

App: http://127.0.0.1:8000/

Admin: http://127.0.0.1:8000/admin/

🔐 Environment Variables (Optional)
If you use environment variables, create a .env file in the project root.

Example:

env
Copy code
DEBUG=True
SECRET_KEY=change-me
ALLOWED_HOSTS=127.0.0.1,localhost
🖼️ Static & Media
Static files are under static/ and served automatically during development.

If you add uploads later, configure MEDIA_URL and MEDIA_ROOT in inventory/settings.py.

For production:

bash
Copy code
python manage.py collectstatic
🧪 Running Tests (if available)
bash
Copy code
python manage.py test
🛠️ Common Commands
bash
Copy code
python manage.py check
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
📌 Deployment Notes (Quick)
For production deployment:

set DEBUG=False

configure ALLOWED_HOSTS

use PostgreSQL/MySQL for production database

use Gunicorn + Nginx (or a PaaS like Render/Railway)

serve static/media via Nginx or cloud storage

👤 Author
Shivam Gautam
GitHub: https://github.com/Sgautam0001

