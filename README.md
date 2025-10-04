# QuickBlog

QuickBlog is a full-stack blogging platform that allows users and admins to create, manage, and view blog posts with image uploads and comments. It features a modern React frontend and a Node.js/Express backend with MongoDB and ImageKit integration.

## Features
- User and admin interfaces for blog management
- Add, edit, delete, and list blogs
- Image upload via ImageKit
- Commenting system
- Admin dashboard for blog and comment moderation
- Responsive UI built with React and Vite
- RESTful API endpoints
- MongoDB database integration

## Project Structure

```
QuickBlog/
├── client/         # React/Vite frontend
│   ├── src/
│   │   ├── components/      # UI components
│   │   ├── pages/           # Page views
│   │   └── assets/          # Images and static files
│   └── public/
├── server/         # Node.js/Express backend
│   ├── controllers/         # Business logic
│   ├── models/              # Mongoose models
│   ├── routes/              # API endpoints
│   ├── middleware/          # Auth, file upload
│   └── configs/             # DB and ImageKit setup
└── README.md
```

## Setup Instructions

### Prerequisites
- Node.js & npm
- MongoDB database
- ImageKit account (for image uploads)

### Backend Setup
1. Navigate to the `server/` directory:
	```sh
	cd server
	```
2. Install dependencies:
	```sh
	npm install
	```
3. Configure environment variables in `server/configs/db.js` and `server/configs/imageKit.js`.
4. Start the backend server:
	```sh
	npm start
	# or
	node server.js
	```

### Frontend Setup
1. Navigate to the `client/` directory:
	```sh
	cd client
	```
2. Install dependencies:
	```sh
	npm install
	```
3. Start the frontend development server:
	```sh
	npm run dev
	```

## Usage
- Access the frontend at `http://localhost:5173` (default Vite port)
- Backend API runs at `http://localhost:3000`
- Admin features are available via the admin dashboard
- Blogs and comments can be managed through the UI

## Integration
- **ImageKit**: Used for image uploads (see `server/configs/imageKit.js`)
- **MongoDB**: Database connection in `server/configs/db.js`

## Contributing
Pull requests and issues are welcome! Please follow the existing code structure and conventions.

## License
MIT