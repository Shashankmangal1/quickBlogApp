# Copilot Instructions for QuickBlog

## Project Overview
QuickBlog is a full-stack blogging platform with a React/Vite frontend (`client/`) and a Node.js/Express backend (`server/`). The backend manages blogs, comments, admin features, and image uploads via ImageKit. The frontend provides user and admin interfaces for blog creation, listing, and management.

## Architecture & Data Flow
- **Frontend (`client/`)**: Built with React, organized by `src/components/` (UI elements), `src/pages/` (views), and `src/assets/` (static files/images).
  - Admin features are under `src/components/admin/` and `src/pages/admin/`.
  - Data is fetched from the backend via REST APIs.
- **Backend (`server/`)**: Node.js/Express app with modular structure:
  - `controllers/`: Business logic for blogs and admin actions
  - `models/`: Mongoose models (e.g., `Blog.js`)
  - `routes/`: API endpoints (`adminRoutes.js`, `blogRoutes.js`)
  - `middleware/`: Auth, file upload (multer), etc.
  - `configs/`: DB and ImageKit setup

## Developer Workflows
- **Frontend**: Run with `npm run dev` in `client/` (uses Vite)
- **Backend**: Start with `node server.js` or `npm start` in `server/`
- **Install dependencies**: Use `npm install` in each subfolder as needed
- **Image Uploads**: Integrated via ImageKit (see `configs/imageKit.js`)

## Key Patterns & Conventions
- **API Communication**: Frontend uses fetch/axios to call backend REST endpoints
- **Admin Separation**: Admin UI and logic are isolated in `admin/` subfolders
- **Component Structure**: Prefer functional React components, organized by feature
- **Error Handling**: Backend uses Express error middleware; frontend shows loaders/errors via components
- **Environment Variables**: Backend expects DB/ImageKit config in `configs/`

## Integration Points
- **ImageKit**: Used for image uploads (see `server/configs/imageKit.js`)
- **MongoDB**: Database connection in `server/configs/db.js`

## Examples
- To add a new blog, see `client/src/pages/admin/AddBlog.jsx` and backend `server/controllers/blogController.js`
- For authentication, see `server/middleware/auth.js` and admin UI in `client/src/components/admin/Login.jsx`

## Tips for AI Agents
- Always check both `client/` and `server/` for cross-feature changes
- When adding features, follow the existing folder/module conventions
- Reference existing components and controllers for implementation patterns
- For new API endpoints, update both backend routes/controllers and frontend API calls

---
For questions or unclear conventions, ask for clarification or examples from maintainers.
