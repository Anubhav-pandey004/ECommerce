# 🛒 E-Commerce Website  

An **E-Commerce web application** built with the **MERN stack (MongoDB, Express.js, React.js, Node.js)**.  
This project was created as part of the **Associate Software Engineer (ASE) Challenge** to demonstrate skills in fullstack development, clean coding, and problem-solving.  

---

## 📌 Features  
- User authentication (signup/login with JWT)  
- Product listing with details (title, price, description, image)  
- Add to cart & remove from cart  
- Cart management with quantity updates  
- Checkout flow (order placement simulation)  
- Backend APIs with validation and error handling  
- Responsive frontend with **React + Tailwind CSS**  

---

## ⚙️ Tech Stack  
- **Frontend:** React.js, Vite, Tailwind CSS, Fetch API  
- **Backend:** Node.js, Express.js, MongoDB  
- **Database:** MongoDB (Atlas/local)  
- **Authentication:** JSON Web Tokens (JWT)  


---

## 🚀 Getting Started  

### 1️⃣ Clone the Repository  
bash
```git clone https://github.com/Anubhav-pandey004/Ecommerce.git```

cd Ecommerce

2️⃣ Backend Setup
cd backend
npm install

Create a .env file in the backend folder with:

PORT=5000
MONGO_URI=your-mongodb-uri
JWT_SECRET=your-secret-key

Run backend server:

node app.js

3️⃣ Frontend Setup
cd frontend
npm install


Run frontend app:
npm run dev


## 💳 Stripe Local Setup  

This project integrates **Stripe** for handling payments (currently in test mode).  

### 1️⃣ Install Stripe CLI  
Download the Stripe CLI for Windows from the official releases page:  
🔗 [Stripe CLI v1.19.5](https://github.com/stripe/stripe-cli/releases/tag/v1.19.5)  

Unzip the folder and open it in your terminal.  

### 2️⃣ Login to Stripe  
bash
stripe login

This will give you a pairing code and open a browser window to authenticate with your Stripe account.
After success, your CLI will be linked to your Stripe account.

3️⃣ Listen for Webhooks
In a separate terminal, run:

bash
Copy code
stripe listen --forward-to localhost:8080/webhook
This forwards Stripe events to your local backend endpoint (/webhook).

4️⃣ Test a Payment

Use Stripe test cards to simulate transactions (e.g., 4242 4242 4242 4242 with any valid expiry & CVC).

📹 Demo Video

I’ve recorded a short walkthrough explaining my thought process, architecture, and demo of core features.
🔗 https://drive.google.com/file/d/1bq4TG1bVQ0QUasqsbZ5LCdzdEP_-YvkW/view?usp=sharing

📝 Design Choices & Assumptions

Separation of Concerns – Followed a modular structure (pages/, components/, routes/, models/) for maintainability.

Scalability – APIs are built in RESTful style with error handling for real-world extensibility.

State Management – Used React hooks & context for cart and auth handling.

Security – Implemented JWT-based authentication, input validation, and bcrypt password hashing.

Testing Approach – Wrote unit tests for APIs & UI components to ensure reliability.


🧑‍💻 Author

👋 Hi, I’m Anubhav pandey, an aspiring software engineer passionate about building scalable web apps.
This project was built as part of the ASE Challenge 2025.
Portfolio: https://anubhavpandey.netlify.app/
