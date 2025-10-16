# 🏦 Bank Account Transaction System (with SMS Alerts & Logging)

This Python script simulates basic bank account operations — deposit and withdrawal — with integrated **Twilio SMS alerts** and detailed **logging** for all actions and errors.

---

## 📜 Features

- ✅ Bank account creation with balance and phone number
- 💸 Deposit & withdrawal methods with validation
- 📲 SMS notifications via **Twilio**
- 📁 Logs every action to a `bank_transactions.log` file
- ⚠️ Custom exception handling (`InvalidAccountError`)
- 🔐 Safe and extendable architecture for future use

---

## 📂 Logging Details

Logging is a central feature of this script. It records:

- Account creation
- All deposit and withdrawal attempts
- Success or failure of SMS notifications
- Warnings and errors related to invalid operations
- Unexpected exceptions at runtime

### 📝 Log File

Logs are saved to:log file

### 🔧 Logging Configuration

```python
import logging

logging.basicConfig(filename='bank_transactions.log', level=logging.INFO)
logging.getLogger("twilio").setLevel(logging.WARNING)

