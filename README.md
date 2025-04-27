🚀 Full Stack TODO Management System
This project is a full-stack TODO Management System where:

Clients can register, log in, create, view, and manage their own TODOs.

Admins can view all TODOs created by all users, with simple pagination.

The system uses Node.js, Express, MongoDB, and JWT on the backend, and React with TailwindCSS on the frontend.

✨ Features
For Clients
Create a new account (register).

Log in securely using email and password.

Create new TODO tasks.

View the list of all their TODOs.

Update their profile information (name, phone number, password).

For Admins
View all TODOs created by all users.

See which user created each TODO.

Navigate through TODOs page-by-page using pagination.

🛠️ Technologies Used
Frontend: React.js, TailwindCSS, Axios

Backend: Node.js, Express.js, MongoDB (Mongoose)

Authentication: JWT (JSON Web Token)

🗂️ Project Structure
bash
Copy code
/backend
  ├── controllers/
  ├── middleware/
  ├── models/
  ├── routes/
  ├── server.js
/frontend
  ├── src/
      ├── pages/
      ├── App.jsx
      ├── index.js
backend/ → Node.js server files.

frontend/ → React app files.

⚙️ How to Run the Project
1. Clone the Repository
bash
Copy code
git clone https://github.com/your-username/todo-management-system.git
cd todo-management-system
2. Set up the Backend
bash
Copy code
cd backend
npm install
Create a .env file inside /backend with the following content:

env
Copy code
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
PORT=5000
Then start the backend server:

bash
Copy code
npm run dev
Server will run on http://localhost:5000

3. Set up the Frontend
Open a new terminal window and run:

bash
Copy code
cd frontend
npm install
npm run dev
Frontend will run on http://localhost:5173 (default Vite port)

📋 API Endpoints Summary
Method	Endpoint	Description
POST	/api/auth/register	Register a new client
POST	/api/auth/login	Client/Admin login
GET	/api/client/todos	Get all TODOs for logged-in client
POST	/api/client/todos	Create a new TODO for client
PUT	/api/client/profile	Update client profile
GET	/api/admin/todos?page=1	Admin view all TODOs (paginated)
👤 Roles
Client:
Role ID = 1

Admin:
Role ID = 0

You can manually insert an Admin user into the database if needed.

📌 Important Notes
Protected routes use JWT Authentication.

MongoDB stores all users and TODOs.

Frontend automatically redirects users based on their role (Client → /client, Admin → /admin).

Pagination is implemented for Admin TODO view (default 10 TODOs per page).

✨ Future Improvements (optional)
Add edit and delete TODOs for clients.

Add filters/search functionality in the admin dashboard.

Add forgot password & reset functionality.

💬 Contact
Feel free to reach out if you have any questions or need help setting it up!

Would you also like me to give you a small copy-paste badge section at the top like "Built with ❤️ by Anuj" or something? 🚀
(looks even more professional!)
Want me to add that too? 🎯







