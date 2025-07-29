# 🤖 BrainWave AI - AI Chat Web Application with TypeScript

![BrainWave AI](https://github.com/user-attachments/assets/e6a4db39-1b94-41c0-86ba-cb0a64680a2f)

## 📋 Overview

BrainWave AI is a full-stack web application that provides an interactive AI chat experience powered by OpenAI's GPT models. Built with TypeScript, React, and Node.js, it offers a modern, secure, and responsive platform for AI-powered conversations.

## ✨ Features

### 🔐 Authentication & Security
- **User Registration & Login**: Secure user authentication with JWT tokens
- **Password Encryption**: Bcrypt hashing for secure password storage
- **Cookie-based Sessions**: HTTP-only signed cookies for enhanced security
- **Protected Routes**: Route protection for authenticated users only

### 💬 Chat Functionality
- **Real-time AI Chat**: Seamless conversation with OpenAI's GPT models
- **Chat History**: Persistent chat storage with MongoDB
- **Context Preservation**: Maintains conversation context across sessions
- **Chat Management**: Delete/clear chat history functionality

### 🎨 User Interface
- **Material-UI Components**: Modern and responsive design
- **Syntax Highlighting**: Code snippets with proper syntax highlighting
- **Typing Animation**: Engaging typing animations for responses
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Toast Notifications**: User-friendly error and success messages

### 🛠️ Technical Features
- **TypeScript**: Full type safety across frontend and backend
- **Input Validation**: Comprehensive form validation with express-validator
- **Error Handling**: Robust error handling and logging
- **CORS Support**: Cross-origin resource sharing configuration
- **Development Tools**: Hot reload and development optimizations

## 🚀 Technologies Used

### Frontend
- **React 18** - UI library with hooks and modern patterns
- **TypeScript** - Type-safe JavaScript
- **Material-UI (MUI)** - React component library
- **Vite** - Fast build tool and development server
- **React Router Dom** - Client-side routing
- **Axios** - HTTP client for API requests
- **React Hot Toast** - Toast notifications
- **React Syntax Highlighter** - Code syntax highlighting
- **React Type Animation** - Typing animation effects

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **TypeScript** - Type-safe server-side development
- **MongoDB & Mongoose** - NoSQL database and ODM
- **OpenAI API** - AI chat completion
- **JWT** - JSON Web Tokens for authentication
- **Bcrypt** - Password hashing
- **Express Validator** - Input validation middleware
- **Morgan** - HTTP request logger
- **CORS** - Cross-origin resource sharing
- **Cookie Parser** - Cookie parsing middleware

### Development Tools
- **Concurrently** - Run multiple commands simultaneously
- **Nodemon** - Auto-restart development server
- **TSC** - TypeScript compiler
- **ESLint** - Code linting

## 📁 Project Structure

```
ai-chat-gpt-web-application-with-typescript/
├── backend/
│   ├── src/
│   │   ├── config/
│   │   │   └── openai-config.ts      # OpenAI configuration
│   │   ├── controllers/
│   │   │   ├── chat-controllers.ts   # Chat-related endpoints
│   │   │   └── user-controllers.ts   # User authentication endpoints
│   │   ├── db/
│   │   │   └── connection.ts         # MongoDB connection
│   │   ├── models/
│   │   │   └── User.ts              # User and Chat schemas
│   │   ├── routes/
│   │   │   ├── chat-routes.ts       # Chat API routes
│   │   │   ├── user-routes.ts       # User API routes
│   │   │   └── index.ts             # Main router
│   │   ├── utils/
│   │   │   ├── constants.ts         # Application constants
│   │   │   ├── token-manager.ts     # JWT token management
│   │   │   └── validators.ts        # Input validation schemas
│   │   ├── app.ts                   # Express app configuration
│   │   └── index.ts                 # Server entry point
│   ├── package.json
│   └── tsconfig.json
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Header.tsx           # Navigation header
│   │   │   ├── chat/
│   │   │   │   └── ChatItem.tsx     # Individual chat message
│   │   │   ├── footer/
│   │   │   │   └── Footer.tsx       # Page footer
│   │   │   ├── shared/
│   │   │   │   ├── CustomizedInput.tsx
│   │   │   │   ├── Logo.tsx
│   │   │   │   └── NavigationLink.tsx
│   │   │   └── typer/
│   │   │       └── TypingAnim.tsx   # Typing animation component
│   │   ├── context/
│   │   │   └── AuthContext.tsx      # Authentication context
│   │   ├── helpers/
│   │   │   └── api-communicator.ts  # API service functions
│   │   ├── pages/
│   │   │   ├── Chat.tsx             # Main chat page
│   │   │   ├── Home.tsx             # Landing page
│   │   │   ├── Login.tsx            # Login page
│   │   │   ├── Signup.tsx           # Registration page
│   │   │   └── NotFound.tsx         # 404 page
│   │   ├── App.tsx                  # Main application component
│   │   └── main.tsx                 # Application entry point
│   ├── public/
│   ├── package.json
│   ├── tsconfig.json
│   └── vite.config.ts
└── README.md
```

## ⚙️ Installation & Setup

### Prerequisites
- Node.js (v18 or higher)
- MongoDB database
- OpenAI API key

### 1. Clone the Repository
```bash
git clone https://github.com/Chanuth-silva10/ai-chat-gpt-web-application-with-typescript.git
cd ai-chat-gpt-web-application-with-typescript
```

### 2. Backend Setup
```bash
cd backend
npm install
```

Create a `.env` file in the backend directory:
```env
PORT=5000
MONGODB_URL=your_mongodb_connection_string
OPEN_AI_SECRET=your_openai_api_key
OPENAI_ORAGANIZATION_ID=your_openai_organization_id
JWT_SECRET=your_jwt_secret_key
COOKIE_SECRET=your_cookie_secret_key
```

### 3. Frontend Setup
```bash
cd ../frontend
npm install
```

### 4. Start Development Servers

**Backend** (from backend directory):
```bash
npm run dev
```

**Frontend** (from frontend directory):
```bash
npm run dev
```

The application will be available at:
- Frontend: `http://localhost:5173`
- Backend API: `http://localhost:5000`

## 🎯 Usage

1. **Register/Login**: Create an account or log in with existing credentials
2. **Start Chatting**: Navigate to the chat page and start your conversation
3. **Ask Questions**: Type your questions or requests in the chat input
4. **View Responses**: Receive AI-generated responses with syntax highlighting
5. **Manage Chats**: Clear chat history or continue previous conversations

## 📚 API Endpoints

### Authentication
- `POST /api/v1/user/signup` - User registration
- `POST /api/v1/user/login` - User login
- `GET /api/v1/user/auth-status` - Check authentication status
- `GET /api/v1/user/logout` - User logout

### Chat
- `POST /api/v1/chat/new` - Send new chat message
- `GET /api/v1/chat/all-chats` - Get user's chat history
- `DELETE /api/v1/chat/delete` - Delete user's chat history

## 🔒 Security Features

- JWT-based authentication
- HTTP-only signed cookies
- Password hashing with bcrypt
- Input validation and sanitization
- CORS configuration
- Protected API routes

## 🚀 Deployment

### Backend Deployment
1. Build the TypeScript code: `npm run build`
2. Start the production server: `npm start`

### Frontend Deployment
1. Build the production bundle: `npm run build`
2. Serve the `dist` folder using a static file server

## 👨‍💻 Author

**Chanuth Silva**
- 📧 Email: [chanuth.silva2025@gmail.com](mailto:chanuth.silva2025@gmail.com)
- 🐙 GitHub: [@Chanuth-silva10](https://github.com/Chanuth-silva10)
- 🔗 LinkedIn: [Connect with me](https://linkedin.com/in/chanuth-silva)

## 🙏 Acknowledgments

- OpenAI for providing the GPT API
- Material-UI team for the excellent component library
- React and Node.js communities for the robust frameworks

---
