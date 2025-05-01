# iTeam Management Application

A full-stack web application for managing student team members, built with the MERN stack (MongoDB, Express.js, React.js, Node.js).

## 🚀 Features

- **Member Management:**
  - Add new team members with detailed information
  - View all team members in a beautiful grid layout
  - View detailed information about each member
  - Upload and manage profile photos

- **Responsive Design:**
  - Dark theme with orange accents
  - Mobile-friendly interface
  - Smooth animations and transitions
  - Modern UI components

## 🛠️ Tech Stack

### Frontend
- React.js
- Material-UI (MUI)
- Axios for API calls
- React Router for navigation

### Backend
- Node.js
- Express.js
- MongoDB
- Multer for file uploads

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14 or higher)
- MongoDB
- Git

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/iTeam.git
   cd iTeam
   ```

2. **Install Backend Dependencies**
   ```bash
   cd server
   npm install
   ```

3. **Install Frontend Dependencies**
   ```bash
   cd ../client
   npm install
   ```

4. **Environment Setup**
   
   Create a `.env` file in the server directory:
   ```env
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/iteam
   ```

## 🚀 Running the Application

1. **Start MongoDB**
   ```bash
   # Start your MongoDB service
   mongod
   ```

2. **Start Backend Server**
   ```bash
   cd server
   npm start
   # Server will run on http://localhost:5000
   ```

3. **Start Frontend Development Server**
   ```bash
   cd client
   npm start
   # Client will run on http://localhost:3000
   ```

## 📡 API Endpoints

### Members

#### GET `/api/members`
- Get all team members
- Response: Array of member objects

#### GET `/api/members/:id`
- Get specific member details
- Response: Single member object

#### POST `/api/members`
- Add new team member
- Request: Multipart form data
- Fields:
  - name (required)
  - rollNumber (required)
  - year (required)
  - degree (required)
  - email (required)
  - aboutProject
  - hobbies
  - certificate
  - internship
  - aboutAim
  - image (file)

### Member Object Structure
```javascript
{
  _id: String,
  name: String,
  rollNumber: String,
  year: String,
  degree: String,
  email: String,
  aboutProject: String,
  hobbies: String,
  certificate: String,
  internship: String,
  aboutAim: String,
  imagePath: String,
  createdAt: Date
}
```

## 📁 Project Structure

```
iTeam/
├── client/                 # Frontend React application
│   ├── public/
│   └── src/
│       ├── components/     # Reusable components
│       ├── pages/         # Page components
│       └── App.js         # Main application component
│
├── server/                 # Backend Node.js application
│   ├── models/            # MongoDB models
│   ├── routes/            # API routes
│   ├── uploads/           # Uploaded files
│   └── server.js          # Main server file
│
└── README.md              # Project documentation
```

## 🎨 Features in Detail

### Home Page
- Welcome message
- Navigation buttons to add/view members
- Responsive design with dark theme

### Add Member Page
- Comprehensive form for member details
- Image upload with preview
- Form validation
- Loading states and error handling

### View Members Page
- Grid layout of all members
- Member cards with images
- Click to view detailed information
- Smooth animations

### Member Details Page
- Detailed view of member information
- Professional photo display
- Organized sections for different information
- Back navigation

## 🔒 Security

- Input validation on both frontend and backend
- Secure file upload handling
- Environment variable usage for sensitive data
- Error handling for API requests

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Team

- Aditya Raj - Developer
- Aryaman Deolia - Developer
- Heer Mehta - Developer

## 🙏 Acknowledgments

- Material-UI for the beautiful components
- MongoDB for the database
- React.js community for the amazing tools 