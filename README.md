# VidyaSutra

**A smarter way to discover and manage scholarships.**

VidyaSutra is a scholarship discovery and application management platform designed to help students identify suitable scholarships, understand eligibility requirements, manage supporting documents, and track applications through the review process.

🏆 **2nd Prize — Code Breaker Challenge (CBC 2.0)**  
👥 **Team:** FluxWave  
🌐 **Live Demo:** https://vidyasutra.onrender.com/

## Features

- **Eligibility Matching:** Identify scholarships relevant to student profiles.
- **Scholarship Discovery:** Explore scholarship opportunities and eligibility criteria.
- **Document Management:** Upload and organize application documents.
- **OCR Verification:** Detect inconsistencies in uploaded documents.
- **Application Tracking:** Monitor application status and review history.
- **Deadline Notifications:** Receive reminders before scholarship deadlines.
- **Reviewer Dashboard:** Manage scholarships, eligibility rules, and applications.
- **Help Assistant:** Access guidance on platform features and applications.

## Technology Stack

| Component | Technologies |
|---|---|
| Frontend | React 19, Vite, Tailwind CSS 4 |
| UI & Animation | Framer Motion, Three.js, Lenis |
| Backend | Node.js, Express 5 |
| Database | PostgreSQL |
| Authentication | JWT, bcrypt |
| OCR | Tesseract.js |
| Email | Nodemailer (optional) |
| Deployment | Render |

## Getting Started

### Prerequisites

- Node.js 20+
- Docker Compose or a running PostgreSQL instance
- Git

### Installation

Clone the repository:

```bash
git clone https://github.com/ItsShannu44/CBC044.git
cd CBC044
```

Start the database and install project dependencies:

```bash
docker compose up -d
npm run setup
```

Configure the environment:

```bash
cp backend/.env.example backend/.env
```

Set the required `DATABASE_URL` and `JWT_SECRET` values in `backend/.env`.

### Run the Application

Start the backend:

```bash
npm run dev:api
```

In a separate terminal, start the frontend:

```bash
npm run dev:web
```

Access the application at **http://localhost:5173**.

To reload the demonstration data, run `npm run seed`.

## Demo Access

| Role | Email | Password |
|---|---|---|
| Student | `student@vidyasutra.test` | `Student@12345` |
| Reviewer | `admin@vidyasutra.test` | `Admin@12345` |

**Security notice:** These are public demonstration credentials. Use fictional data only and do not upload real identity documents or banking information.

## Testing

Run the automated test suite:

```bash
npm test
```

API tests require a separately configured test database through `TEST_DATABASE_URL`. The API test suite may clear its target database, so never point it at production data.

## Project Structure

```text
CBC044/
├── backend/
│   ├── src/
│   │   ├── engine/       # Eligibility rules
│   │   ├── models/       # Database models
│   │   ├── routes/       # API endpoints
│   │   └── services/     # Application services
│   └── test/             # Backend tests
├── frontend/
│   └── src/
│       ├── pages/        # Application pages
│       ├── components/   # Reusable UI components
│       └── lib/          # API client and utilities
├── test-user/            # Fictional OCR test documents
└── render.yaml           # Deployment configuration
```

## Deployment

VidyaSutra is configured for deployment on Render.

- **Build:** `npm run build`
- **Start:** `npm start`
- **Health Check:** `/api/health`
- **Database:** PostgreSQL

Configure the required environment variables in the deployment environment. Never commit secrets or production credentials to version control.

*Note: The live demonstration uses Render's free plan. Initial loading may take up to a minute after inactivity.*

## Acknowledgements

Some interface components are adapted from [React Bits](https://reactbits.dev) by David Haz, subject to the terms specified in `LICENSE-react-bits.md`.

---

**VidyaSutra — Making scholarship discovery simpler, clearer, and more accessible.**

Developed by **Team FluxWave** for **CBC 2.0 · Problem Statement 29**.

**Recognition:** 2nd Prize Winner at the Code Breaker Challenge (CBC 2.0).
