# Lucky Mo To

A modern lottery gaming application with real-time features, built with React and Node.js. This application provides users with an engaging lottery experience with instant draws, betting capabilities, and account management.

## Features

- **Real-time Lottery System**: Participate in minute-based lottery draws with live updates
- **User Authentication**: Secure login and registration system with JWT tokens
- **Account Management**: Manage balance, view history, and track winnings
- **Live Betting**: Place bets on lottery numbers with instant confirmation
- **WebSocket Integration**: Real-time updates for draws and results
- **Responsive Design**: Modern UI built with Tailwind CSS and React
- **Transaction History**: Complete betting and winning history tracking

## Tech Stack

### Frontend
- **React 19** - Modern React with latest features
- **Vite** - Fast development and build tool
- **Tailwind CSS** - Utility-first CSS framework
- **React Router** - Client-side routing
- **Socket.IO Client** - Real-time communication
- **Axios** - HTTP client for API calls
- **Lucide React** - Modern icon library

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **Socket.IO** - Real-time bidirectional communication
- **MySQL2** - MySQL database driver
- **JWT** - JSON Web Tokens for authentication
- **Crypto-js** - Encryption utilities
- **Morgan** - HTTP request logger

### Database
- **MySQL** - Relational database for user data, tickets, and lottery draws

## Project Structure

```
Lucky-Mo-To/
|-- frontend/                 # React frontend application
|   |-- src/
|   |   |-- components/       # Reusable React components
|   |   |-- pages/           # Page components
|   |   |-- hooks/           # Custom React hooks
|   |   |-- api/             # API service functions
|   |   |-- socket/          # Socket.IO client setup
|   |   |-- utils/           # Utility functions
|   |   |-- layout/          # Layout components
|   |   `-- assets/          # Static assets
|   |-- public/              # Public assets
|   `-- package.json         # Frontend dependencies
|
|-- backend/                  # Node.js backend API
|   |-- src/
|   |   |-- controllers/     # Route controllers
|   |   |-- models/          # Database models
|   |   |-- routes/          # API routes
|   |   |-- middlewares/     # Express middlewares
|   |   `-- core/            # Database setup and utilities
|   |-- public/              # Public files
|   `-- package.json         # Backend dependencies
|
|-- LICENSE                   # MIT License
`-- README.md                 # This file
```

## Getting Started

### Prerequisites
- Node.js ^18
- MySQL database
- npm ^10.7.0

### Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd Lucky-Mo-To
```

2. **Install frontend dependencies**
```bash
cd frontend
npm install
```

3. **Install backend dependencies**
```bash
cd ../backend
npm install
```

4. **Database Setup**
   - Create a MySQL database
   - Import the database schema from `backend/lotto_db.sql`
   - Configure database connection in `.env` file

5. **Environment Variables**
   
   **Backend (.env)**
   ```env
   PORT=3000
   API_KEY={public_key}
   API_SECRET_KEY={private_key}
   
   DB_HOST=localhost
   DB_USER=root
   DB_PASS=example
   DB_NAME=lotto_db
   ```

   **Frontend (.env)**
   ```env
   VITE_API_URL=http://localhost:3000
   VITE_SOCKET_URL=http://localhost:3000
   ```

### Running the Application

1. **Start the backend server**
```bash
cd backend
npm run dev
```

2. **Start the frontend application**
```bash
cd frontend
npm run dev
```

The application will be available at:
- Frontend: http://localhost:3000
- Backend API: http://localhost:3000/api

## API Endpoints

### Authentication
- `POST /v1/account/login` - User login
- `POST /v1/account` - Create new account
- `GET /v1/account` - Get user information (requires token)

### Lottery
- `GET /v1/lotto` - Get current lottery information
- `POST /v1/lotto/bet` - Place a bet
- `GET /v1/lotto/draw` - Get draw results
- `GET /v1/lotto/history` - Get betting history

### Tickets
- `GET /v1/tickets` - Get user tickets
- `POST /v1/tickets` - Create new ticket

## Real-time Features

The application uses Socket.IO for real-time communication:
- **Live Draw Updates**: Instant notifications when draws occur
- **Betting Confirmations**: Real-time bet placement confirmation
- **Winning Notifications**: Instant win/loss notifications
- **Balance Updates**: Live balance updates after transactions

## Contributing

We welcome contributions to improve Lucky Mo To! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## Contributors

- **Raecell** - Frontend Development & UI/UX Design
  - React components and pages
  - Tailwind CSS styling
  - User interface design
  - User experience optimization

- **Wilson** - Backend Development & API Architecture
  - Node.js/Express server setup
  - Database design and management
  - API endpoint development
  - Authentication and security implementation

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support or questions, please reach out to the project maintainers or create an issue in the repository.

---

**Lucky Mo To** - Your lucky numbers are just a click away!
