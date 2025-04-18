README
🔐 Secure Data Encryption App – Project Overview Project Title: Secure Data Encryption System using Streamlit and Python

✅ Description: This project is a simple yet effective web-based application built using Streamlit that allows users to securely store and retrieve secret information. The app uses Fernet symmetric encryption (from the cryptography library) to protect the data, and stores it in a SQLite database. Access to the stored secrets is protected using a hashed passkey.

💡 Technologies Used:

Technology Purpose Python Programming Language Streamlit Building the web-based user interface SQLite Lightweight database to store encrypted secrets Fernet (Cryptography) Encrypting and decrypting sensitive data OS module Managing key file creation and file paths 🛠️ Features: Store a secret:

User provides a label, secret text, and a passkey.

Secret is encrypted using Fernet.

Passkey is hashed (for secure storage).

Data is saved to a local SQLite database.

Retrieve a secret:

User provides the label and passkey.

App fetches the encrypted secret from the database.

If the passkey matches, the secret is decrypted and shown.

Key management:

Encryption key is auto-generated and saved to a local file (simple_secret.key).

Key is reused on future app runs.

📂 Folder Structure: vbnet Copy Edit secure_data_encryption_assignment/ ├── secure_data_encryption_assignment/ │ └── secure_app.py │ └── simple_secret.key ← encryption key (auto-generated) │ └── simple_data.db ← database file (auto-created) 🚀 How It Works: When the app starts, it checks if the encryption key file exists.

If not, a new key is generated and saved.

The user chooses whether to store or retrieve a secret.

The app encrypts the data before saving it and decrypts it when retrieving — only if the correct passkey is entered.

