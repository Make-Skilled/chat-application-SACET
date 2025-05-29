# ChatFlow - Real-time Chat Application

A modern, responsive chat application built with Flask and MongoDB, featuring real-time messaging, file sharing, and a beautiful UI.

## Features

- **User Authentication**: Secure registration and login system with bcrypt encryption
- **Dynamic Messaging**: Real-time message sending and receiving with database persistence
- **Conversation Management**: Create and manage conversations with multiple users
- **Dynamic Home Page**: Live conversation list with last messages and timestamps
- **Dynamic Chat Interface**: Real message history loaded from MongoDB
- **Responsive Design**: Beautiful UI that works on all devices
- **User Session Management**: Persistent login sessions with user context
- **API Integration**: RESTful APIs for all chat functionality

## Technology Stack

- **Backend**: Flask (Python)
- **Database**: MongoDB
- **Frontend**: HTML5, CSS3 (Tailwind CSS), JavaScript
- **Authentication**: bcrypt for password hashing
- **UI Framework**: Tailwind CSS with custom styling

## Prerequisites

- Python 3.7+
- MongoDB (running locally on port 27017)
- pip (Python package manager)

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd chat-application
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up MongoDB**
   - Install MongoDB on your system
   - Start MongoDB service
   - The application will automatically create the required database and collections

4. **Set environment variables (optional)**
   ```bash
   export SECRET_KEY="your-secret-key-here"
   ```
   Or create a `.env` file:
   ```
   SECRET_KEY=your-secret-key-here
   ```

5. **Create test data (optional)**
   ```bash
   python create_test_data.py
   ```
   This creates sample users and conversations for testing.

## Running the Application

1. **Start the Flask application**
   ```bash
   python app.py
   ```

2. **Access the application**
   - Open your web browser
   - Navigate to `http://localhost:5000`
   - You should see the ChatFlow landing page

## Usage

### **Quick Start with Test Data**
1. **Create test data**: `python create_test_data.py`
2. **Login with test account**: `alice@example.com` / `password123`
3. **See dynamic conversations** on the home page
4. **Click any conversation** to start chatting
5. **Send real messages** that persist in the database

### **Manual Testing**
1. **Registration**
   - Click "Get Started" or "Sign Up" on the landing page
   - Fill in your name, email, and password
   - Password must be at least 6 characters with letters and numbers

2. **Login**
   - Use your registered email and password
   - Check "Remember me" to stay logged in

3. **Dynamic Dashboard**
   - View your real conversations with last messages
   - Start new chats by clicking "New Chat"
   - See user avatars and timestamps
   - Access your profile settings

4. **Dynamic Chatting**
   - Click on a conversation to open the chat interface
   - Send messages that are saved to MongoDB
   - See real message history and timestamps
   - Messages persist across sessions

## Project Structure

```
chat-application/
├── app.py                 # Main Flask application with dynamic routes
├── create_test_data.py    # Script to create sample data
├── test_routes.py         # Route testing script
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation
├── TESTING_GUIDE.md      # Comprehensive testing guide
├── .env.example          # Environment variables template
├── templates/            # Dynamic HTML templates
│   ├── landing2.html     # Beautiful landing page
│   ├── login.html        # Dynamic login with Flask APIs
│   ├── register.html     # Dynamic registration with Flask APIs
│   ├── home.html         # Dynamic dashboard with real conversations
│   ├── chat.html         # Dynamic chat interface with real messages
│   ├── 404.html          # 404 error page
│   └── 500.html          # 500 error page
└── static/               # Static files (CSS, JS, images)
```

## API Endpoints

### **Page Routes**
- `GET /` - Dynamic landing page
- `GET/POST /register` - User registration with validation
- `GET/POST /login` - User authentication with session management
- `GET /logout` - User logout with session cleanup
- `GET /home` - Dynamic dashboard with real conversations (requires authentication)
- `GET /chat?id=<conversation_id>` - Dynamic chat interface with real messages (requires authentication)

### **API Routes**
- `POST /api/send_message` - Send a message in a conversation
- `GET /api/get_messages/<conversation_id>` - Get messages for a conversation
- `POST /api/create_conversation` - Create a new conversation with another user

## Security Features

- Password hashing with bcrypt
- Session management
- Input validation and sanitization
- CSRF protection (Flask built-in)
- Email format validation
- Password strength requirements

## Testing

For comprehensive testing instructions, see [TESTING_GUIDE.md](TESTING_GUIDE.md).

**Quick Test:**
1. Run `python create_test_data.py` to create sample data
2. Login with `alice@example.com` / `password123`
3. Test dynamic conversations and messaging

## Future Enhancements

- Real-time messaging with WebSocket (Flask-SocketIO)
- Group chat functionality
- Message encryption
- Push notifications
- Mobile app development
- Video calling integration
- Message search functionality
- File upload to cloud storage

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support or questions, please open an issue in the repository or contact the development team.
# chat-application-SACET
