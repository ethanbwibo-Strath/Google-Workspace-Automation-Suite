# Google Workspace Automation Suite

A comprehensive Python-based toolkit for managing the user lifecycle within a Google Workspace domain. Developed during my IT internship at MOHI to automate onboarding, access control, and offboarding.

## 🚀 Features
- **Onboarding:** Automatically sends HTML-formatted welcome emails to new staff with login credentials.
- **Access Control:** Bulk-adds users to Google Groups based on department or role.
- **Offboarding:** Automates the deletion of archived or departed user accounts.
- **Security:** Uses OAuth 2.0 and `.gitignore` to protect sensitive admin credentials.

## 🛠️ Technologies Used
- **Language:** Python 3.x
- **APIs:** Google Admin SDK (Directory API), Gmail API
- **Libraries:** `google-api-python-client`, `google-auth-oauthlib`

## 🔧 Project Structure
```text
User-Management/
├── scripts/
│   ├── delete_users.py         # Offboarding logic
│   ├── manage_groups.py         # Group management logic
│   └── send_welcome_emails.py   # Onboarding/Gmail logic
├── templates/
│   └── welcome_template.html    # Email HTML template
├── requirements.txt             # Dependencies
└── .gitignore                   # Security exclusions
```

## 📖 Setup & Usage

1. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Execution:**
   - **To Offboard:** `python scripts/delete_users.py`
   - **To Manage Groups:** `python scripts/manage_groups.py`
   - **To Onboard:** `python scripts/send_welcome_emails.py`

3. **Customization:**
   Edit `templates/welcome_template.html` to change the branding of onboarding emails without modifying the Python logic.

## 🔒 Security
Sensitive files (`credentials.json`, `token.json`, and CSV data) are excluded from version control to maintain domain security.