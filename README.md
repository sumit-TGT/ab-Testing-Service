# 🧪 A/B Testing & UI Experimentation Service

A backend service to test and analyze the performance of different QR code templates (or UI formats) by serving them randomly and tracking user interactions. Built with Node.js and MongoDB.

---

## 🎯 Purpose

To help teams experiment with multiple UI/QR code variations and automatically determine which performs best based on real user engagement (e.g., opens, shares).

---

## 🛠 Tech Stack

- **Backend:** Node.js, Express.js
- **Database:** MongoDB (Mongoose)
- **Others:** dotenv, cors

---

## 🚀 Key Features

- 🎲 Randomly serve 2 active templates
- 📝 Track user events like `open` and `share`
- 📊 Generate reports showing which template performed better

---

## ⚙️ Setup Instructions

1. **Clone the Repository**
     ```bash

       git clone https://github.com/sumit-TGT/ab-testing-service.git
       cd ab-testing-service

2. Install Dependencies
   npm install

3. Configure Environment
    Create a .env file in the root:
    ```bash

     PORT=3000
     MONGO_URI=mongodb://localhost:27017/ab_test_db

4. Run the server 
   npm start

📡 API Endpoints
🔁 Serve Random Templates
GET /api/templates/pair?userId=123

Returns two random active templates and logs an exposure event for that user.

🧩 Track User Engagement
POST /api/templates/track

```bash
{
  "templateId": "TEMPLATE_OBJECT_ID",
  "userId": "USER_ID",
  "eventType": "open"   // or "share"
}

📊 Report on Template Performance
GET /api/templates/report

Returns a breakdown of how many open and share events each template received.

🌱 Seeding the Database
Run this to insert sample templates:
```bash
node seed/seed.js

📁 Project Structure
.
├── app.js
├── .env
├── .gitignore
├── LICENSE
├── README.md
├── seed/
│   └── seed.js
├── models/
│   ├── Template.js
│   └── Event.js
├── controllers/
│   └── templateController.js
├── services/
│   └── templateService.js
└── routes/
    └── templateRoutes.js

    👨‍💻 Author
Built by [Sumit Kumar]
     Terra Grid Tech
 
