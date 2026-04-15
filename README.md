# AI Study Planner

An intelligent study planning application that helps students create personalized study plans, manage notes, and prepare effectively for exams using AI-powered features.

## Features

- **User Authentication** - Login and signup with role-based access (student/admin)
- **Study Plan Management** - Create and manage personalized study plans
- **Notes Maker** - Create and organize study notes
- **Q&A Component** - Generate questions and answers from study material
- **Flash Cards** - Create flashcards for quick revision
- **MCQ Practice** - Practice multiple choice questions
- **Subjective Questions** - Practice subjective/essay-type questions
- **AI Tutor** - Get AI-powered tutoring assistance
- **Image Generator** - Generate visual study aids
- **Theory Memorizer** - Memorize theory concepts effectively
- **Admin Dashboard** - Admin panel for managing users

## Tech Stack

- **Frontend:** React, TypeScript, Vite
- **Styling:** Tailwind CSS, shadcn/ui
- **Backend:** Node.js, Express
- **Database:** MongoDB (with Mongoose)
- **Authentication:** JWT tokens

## Prerequisites

- Node.js (v18 or higher)
- MongoDB (local or cloud instance)
- npm or yarn

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Abhijeet-dhotre/AI-TUTOR.git
   cd AI-TUTOR
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure environment variables:**

   Create a `.env` file in the root directory:
   ```env
   # Server (backend)
   PORT=3001
   MONGO_URI=mongodb://127.0.0.1:27017/studyplanner
   JWT_SECRET=your_jwt_secret_key

   # Frontend (Vite)
   VITE_SUPABASE_URL=your_supabase_url
   VITE_SUPABASE_PUBLISHABLE_KEY=your_supabase_key
   VITE_GEMINI_API_KEY=your_gemini_api_key
   ```

4. **Start MongoDB** (if running locally):
   ```bash
   mongod
   ```

## Running the Application

### Option 1: Run both frontend and backend together
```bash
npm run dev:all
```
This will start both the Vite development server and the Express backend concurrently.

### Option 2: Run separately

**Frontend only:**
```bash
npm run dev
```

**Backend only:**
```bash
npm run server
```

The frontend will be available at `http://localhost:5173` and the backend at `http://localhost:3001`.

## Default Admin Account

After starting the server, create an admin account:

1. Open a new terminal
2. Run: `node server/create-admin.ts`
3. Login with:
   - Email: `admin@studyplanner.com`
   - Password: `admin123`

## Project Structure

```
AI-TUTOR/
├── public/              # Static assets
├── server/             # Express backend
│   ├── index.ts        # Server entry point
│   ├── models/         # Mongoose models
│   └── routes/         # API routes
├── src/                # React frontend
│   ├── components/     # UI components
│   ├── hooks/          # Custom React hooks
│   ├── lib/           # Utility functions
│   └── pages/         # Page components
├── .env                # Environment variables
├── package.json        # Dependencies
├── tailwind.config.ts   # Tailwind configuration
└── vite.config.ts      # Vite configuration
```

## Building for Production

```bash
npm run build
```

The build output will be in the `dist` folder.

## License

MIT