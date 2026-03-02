# Front-Backend_Projesi
BEUBlog
Modern full-stack blog platform.

Stack
Frontend: React 18, Vite, React Router, React Quill, Axios, Lucide
Backend: Node.js, Express 5, MongoDB, Mongoose, JWT, Multer, bcryptjs
DevOps: Docker, Docker Compose, Nginx
Categories
Default categories are seeded automatically on backend startup.
If no category is selected while creating/updating a post, backend auto-detects category from title/excerpt/content.
Project Structure
.
├── docker-compose.yml
├── backend
│   ├── server.js
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── make-admin.js
│   ├── migrate-slugs.js
│   └── uploads/
└── frontend
    └── src/
Environment
Create backend/.env:

PORT=5000
MONGODB_URI=mongodb://localhost:27017/blogdb
JWT_SECRET=change-this-secret
CLIENT_ORIGIN=http://localhost:5173
Run with Docker (recommended)
set JWT_SECRET=change-this-secret
docker compose up -d --build
Services:

Frontend: http://localhost
Backend: http://localhost:5000
MongoDB: mongodb://localhost:27017
Run manually
Backend:

cd backend
npm install
npm start
Frontend:

cd frontend
npm install
npm run dev
Helper scripts
Make user admin:

cd backend
node make-admin.js <email-or-username>
Migrate post slugs:

cd backend
node migrate-slugs.js
Seed default categories manually:

cd backend
npm run seed-categories
