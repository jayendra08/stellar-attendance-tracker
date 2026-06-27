<img width="1899" height="951" alt="Screenshot 2026-04-11 183338" src="https://github.com/user-attachments/assets/e4922ecf-2d2e-4b17-8158-5b307f843da4" />
<img width="1919" height="989" alt="Screenshot 2026-04-11 183242" src="https://github.com/user-attachments/assets/5e725e22-aa0c-4a0f-8a67-3817dc721152" />

# 📍 Attendance Tracker Smart Contract (Soroban - Rust)

A decentralized **Attendance Tracking System** built using **Rust** and **Soroban SDK** on the **Stellar blockchain**.

This smart contract provides a secure way to:

* 📅 Create event sessions
* 👥 Track attendee check-ins
* 🔒 Prevent duplicate entries
* 📊 Monitor attendance in real-time

---

## 🌐 Live Contract (Testnet)

🔗 https://stellar.expert/explorer/testnet/contract/CB6KIIY3G2SHO4EMLPATNMZFYP32DWWEADYJIA57XHY3UMWPSKS5KY4U

---

## 🧠 Overview

This project implements a **blockchain-based attendance system** where:

* Organizers create sessions/events
* Participants check in using their wallet identity
* Attendance is stored securely and immutably on-chain

---

## ⚙️ Features

### 📅 1. Create Session

* Organizer creates a session with:

  * Title
  * Location
  * Session time
* Session status starts as **open**

---

### 👥 2. Attendee Check-In

* Users can check in to a session
* Requires authentication
* Updates attendance count

---

### 🔒 3. Duplicate Prevention

* Each attendee can check in **only once**
* Prevents fake or repeated entries

---

### 🛑 4. Close Session

* Only the organizer can close a session
* No check-ins allowed after closing

---

### 📊 5. Query Functions

* Fetch session details
* List all sessions
* Get total attendee count

---

## 🏗️ Tech Stack

* 🦀 Rust (`#![no_std]`)
* ⭐ Soroban SDK
* 🌐 Stellar Blockchain

---

## 📁 Smart Contract Structure

### 🔹 Session Struct

```rust id="sx82kp"
Session
```

Includes:

* Organizer address
* Title & location
* Status (`open` / `closed`)
* Attendee count
* Timestamps (created & closed)

---

### 🔹 Storage Keys

```rust id="mz91ql"
SessionDataKey
```

* `IdList` → Stores all session IDs
* `Session(Symbol)` → Session data
* `CheckedIn(Symbol, Address)` → Attendance record

---

### 🔹 Errors

```rust id="tr83wn"
AttendanceError
```

Handles:

* Invalid title or timestamp
* Unauthorized actions
* Session not found
* Duplicate check-ins
* Closed session access

---

## 🔐 Security Features

* ✅ Authentication using `require_auth()`
* ✅ Prevents duplicate check-ins
* ✅ Organizer-only controls
* ✅ Safe state transitions

---

## 📌 Core Functions

| Function             | Description              |
| -------------------- | ------------------------ |
| `create_session`     | Create a new session     |
| `check_in`           | Check in to session      |
| `close_session`      | Close session            |
| `get_session`        | Retrieve session details |
| `list_sessions`      | List all sessions        |
| `get_attendee_count` | Get attendance count     |

---

## 🚀 How It Works

1. Organizer creates a session
2. Session becomes **open**
3. Users check in
4. Attendance is recorded on-chain
5. Organizer closes session
6. Session becomes immutable

---

## 📈 Future Improvements

* 📱 Frontend dashboard (React / Next.js)
* 📷 QR code-based attendance
* 🪪 Wallet-based identity system
* 📊 Analytics & reporting
* 🔔 Real-time notifications

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch
3. Commit your changes
4. Open a Pull Request

---

## 📜 License

This project is open-source under the **MIT License**.

---

## 💡 Author

Built with ❤️ using Rust & Web3 innovation.

---

⭐ If you like this project, don’t forget to **star the repository!**
