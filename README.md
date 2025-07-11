# PDF Tools Web App

A web-based application that provides PDF manipulation features like merging and splitting files. Built using **Node.js**, **Express**, and **vanilla HTML/JS** to start with. More features will be added following the Software Development Life Cycle (SDLC) process.

---

## 📁 Project Structure (Initial MVP)

```
pdf-tools-app/
│
├── backend/
│   ├── index.js              # Express server setup
│   ├── routes/
│   │   └── pdf.js            # PDF endpoints: merge, split
│   ├── uploads/              # Temporary uploaded PDF files
│   ├── utils/                # Helper functions (e.g., merging logic)
│   └── package.json
│
├── frontend/
│   ├── index.html            # User interface for PDF upload
│   ├── script.js             # JS logic for handling form submission
│   └── style.css             # Optional: UI styling
│
├── README.md
└── .gitignore
```

---

## 🎯 Features (MVP)

Future features will include:

* Compressing PDFs
* Rotating pages
* Adding watermarks or text
* PDF → Image conversion
* (Optional) User history tracking with database

---

## 🛠️ Tech Stack

### Backend:

* Node.js + Express
* `pdf-merger-js` or `pdf-lib` for PDF handling
* `multer` for file uploads

### Frontend:

* HTML + JavaScript (vanilla to start)
* Optional: React (for future scalability)

### Optional (Planned):

* MongoDB Atlas or SQLite for logging/uploads
* Unit testing (Jest or Mocha)
* GitHub Actions for CI

---

## 🔗 API Endpoints

| Method | Endpoint         | Description         |
| ------ | ---------------- | ------------------- |
| POST   | `/api/pdf/merge` | Merge multiple PDFs |
| POST   | `/api/pdf/split` | Split by page range |

---

## 🚀 Deployment Plan

| Platform        | Use         | Status          |
| --------------- | ----------- | --------------- |
| Railway         | Backend API | Planned         |
| Vercel          | Frontend UI | Planned         |
| Azure (Student) | Backend     | Optional backup |

Deployment will be done **early** to test MVP, and then updated progressively.
Use branching and PRs to manage pushes to `dev` and `main`. After the folder structure is ready, it will be pushed to `feature/setup-structure`, reviewed, and merged into `dev`.

Later on, we'll consider Dockerized deployments for better reproducibility and hosting compatibility.

Example Docker setup for backend:

```
docker build -t pdf-backend ./backend
docker run -p 3000:3000 pdf-backend
```

---

## 🌱 Development Workflow

* Branching:

  * `main` → Production-ready code
  * `dev` → Ongoing development
  * `feature/merge`, `feature/split`, etc. → Feature branches

* Workflow:

  1. Develop feature in `feature/*`
  2. Merge into `dev` via PR
  3. Merge tested `dev` into `main` for production

---

## 🧠 SWE Engineering Roadmap

### ✅ Right Now (Early Dev Phase)

* Git/GitHub setup with branches + PRs
* README and project structure
* API route planning
* nodemon for fast dev
* .gitignore
* Use environment variables (dotenv) for port, secrets
* Start planning for modularity
* Start Dockerizing

### 📌 Soon / After MVP

* Add unit/integration tests (jest, supertest)
* Add logger (morgan, winston)
* CI/CD pipeline (GitHub Actions)
* API documentation (Swagger, Postman collection)
* Error handling middleware
* Use dotenv for secrets (port, DB URL)
* Setup DB COnnection pool (MongoDB Atlas)

### 🚀 Before Production / v1 Release

* Rate-limiting middleware
* Add file size limits (in multer)
* Auto-delete temp files after processing
* HTTPS support
* CORS management
* Code linitng (eslint)
* Secrets + config managed via .env

---

## ✅ To Do (Initial Checklist)

*

---

## 📄 License

MIT
