# HealthcareAI - AI-Powered Healthcare Management System

A comprehensive MERN stack healthcare management system with separate frontend and backend architecture, featuring AI-powered patient care, treatment scheduling, and medical workflow optimization.

## 🏗️ Project Structure

\`\`\`
healthcare-ai-system/
├── backend/                 # Node.js/Express API Server
│   ├── models/             # MongoDB Models
│   ├── routes/             # API Routes
│   ├── middleware/         # Authentication & Validation
│   ├── server.js           # Main server file
│   └── package.json        # Backend dependencies
├── frontend/               # Next.js React Application
│   ├── app/               # Next.js App Router
│   ├── components/        # React Components
│   ├── hooks/             # Custom React Hooks
│   ├── lib/               # Utilities & API Client
│   └── package.json       # Frontend dependencies
└── README.md              # This file
\`\`\`

## 🚀 Features

### Admin Dashboard
- **System Overview**: Real-time statistics and health monitoring
- **User Management**: Add, edit, and manage doctors and patients
- **Treatment Scheduling**: Coordinate treatments across the system
- **Medicine Management**: Oversee prescription and dosage scheduling
- **Analytics**: Comprehensive reporting and insights

### Doctor Dashboard
- **Patient Management**: View and manage assigned patients
- **Treatment Planning**: Schedule and track patient treatments
- **Prescription Management**: Create and monitor medication schedules
- **Schedule Overview**: Manage appointments and availability
- **Patient Communication**: Direct messaging with patients

### Patient Portal
- **Treatment Schedule**: View upcoming treatments and appointments
- **Medicine Reminders**: Automated medication adherence tracking
- **Awareness Videos**: Personalized educational content
- **Motivational Content**: AI-curated inspirational materials
- **Health Tracking**: Progress monitoring and vital signs
- **AI Chat Assistant**: 24/7 healthcare support
- **Care Team Communication**: Direct messaging with healthcare providers

## 🛠️ Technology Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **JWT** - Authentication
- **bcryptjs** - Password hashing
- **Helmet** - Security middleware
- **CORS** - Cross-origin resource sharing

### Frontend
- **Next.js 14** - React framework with App Router
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **SWR** - Data fetching and caching
- **Axios** - HTTP client
- **React Hook Form** - Form management
- **React Hot Toast** - Notifications
- **Lucide React** - Icons

## 📦 Installation & Setup

### Prerequisites
- Node.js (v18 or higher)
- MongoDB (local or cloud instance)
- npm or yarn package manager

### Backend Setup

1. **Navigate to backend directory**
   \`\`\`bash
   cd backend
   \`\`\`

2. **Install dependencies**
   \`\`\`bash
   npm install
   \`\`\`

3. **Environment Configuration**
   \`\`\`bash
   cp .env.example .env
   \`\`\`
   
   Update `.env` with your configuration:
   \`\`\`env
   MONGODB_URI=mongodb://localhost:27017/healthcare-ai
   JWT_SECRET=your-super-secret-jwt-key-here
   PORT=5000
   NODE_ENV=development
   FRONTEND_URL=http://localhost:3000
   \`\`\`

4. **Start the backend server**
   \`\`\`bash
   # Development mode
   npm run dev
   
   # Production mode
   npm start
   \`\`\`

   The backend will be available at `http://localhost:5000`

### Frontend Setup

1. **Navigate to frontend directory**
   \`\`\`bash
   cd frontend
   \`\`\`

2. **Install dependencies**
   \`\`\`bash
   npm install
   \`\`\`

3. **Environment Configuration**
   \`\`\`bash
   cp .env.local.example .env.local
   \`\`\`
   
   Update `.env.local`:
   \`\`\`env
   NEXT_PUBLIC_API_URL=http://localhost:5000/api
   NEXT_PUBLIC_APP_NAME=HealthcareAI
   \`\`\`

4. **Start the frontend development server**
   \`\`\`bash
   npm run dev
   \`\`\`

   The frontend will be available at `http://localhost:3000`

## 🔐 Authentication & Demo Accounts

The system includes role-based authentication with three user types:

### Demo Credentials
- **Admin**: admin@healthcare.ai / password123
- **Doctor**: doctor@healthcare.ai / password123  
- **Patient**: patient@healthcare.ai / password123

### User Roles & Permissions

#### Admin
- Full system access
- User management (create, edit, delete)
- System analytics and reporting
- Treatment and medicine scheduling oversight

#### Doctor
- Patient management (assigned patients only)
- Treatment planning and scheduling
- Prescription management
- Patient communication
- Medical record access

#### Patient
- Personal health dashboard
- Treatment schedule viewing
- Medicine adherence tracking
- Educational content access
- AI chat assistant
- Care team communication

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/register` - User registration
- `GET /api/auth/profile` - Get user profile
- `PUT /api/auth/profile` - Update user profile
- `POST /api/auth/logout` - User logout

### Users Management
- `GET /api/users` - Get all users (Admin only)
- `GET /api/users/:id` - Get user by ID
- `PUT /api/users/:id` - Update user (Admin only)
- `DELETE /api/users/:id` - Delete user (Admin only)
- `GET /api/users/stats/overview` - User statistics (Admin only)

### Patients
- `GET /api/patients` - Get patients list
- `GET /api/patients/:id` - Get patient details
- `POST /api/patients` - Create patient record (Admin only)
- `PUT /api/patients/:id` - Update patient record
- `POST /api/patients/:id/vitals` - Add vital signs

### Treatments
- `GET /api/treatments` - Get treatments list
- `POST /api/treatments` - Schedule new treatment
- `PUT /api/treatments/:id` - Update treatment
- `GET /api/treatments/upcoming` - Get upcoming treatments (Patient)

### Medicines
- `GET /api/medicines` - Get prescriptions list
- `POST /api/medicines` - Create prescription
- `POST /api/medicines/:id/adherence` - Record medicine adherence
- `GET /api/medicines/active` - Get active medicines (Patient)

### Videos & Content
- `GET /api/videos` - Get educational videos
- `GET /api/videos/:id` - Get video details
- `GET /api/videos/recommendations/personalized` - Get personalized recommendations
- `POST /api/videos/:id/progress` - Record viewing progress

### Chat & Communication
- `POST /api/chat/ai-assistant` - Send message to AI assistant
- `GET /api/chat/history` - Get chat history
- `POST /api/chat/care-team` - Send message to care team
- `GET /api/chat/care-team/messages` - Get care team messages

## 🎨 Design System

The application uses a custom "Blue Jungle" color palette:

- **Primary**: #011D4D (Deep Navy)
- **Secondary**: #034078 (Medium Blue)  
- **Accent**: #1282A2 (Teal Blue)
- **Neutral**: #E4DFDA (Light Beige)
- **Tertiary**: #63372C (Brown)

### UI Components
- Consistent design tokens for colors, spacing, and typography
- Responsive design with mobile-first approach
- Accessible components with proper ARIA labels
- Dark mode support with semantic color variables

## 🔒 Security Features

- **JWT Authentication** - Secure token-based authentication
- **Password Hashing** - bcrypt with salt rounds
- **Rate Limiting** - API request throttling
- **CORS Protection** - Cross-origin request security
- **Helmet Security** - HTTP headers protection
- **Input Validation** - Server-side validation with express-validator
- **Role-based Access Control** - Granular permissions system

## 📱 Responsive Design

The application is fully responsive and optimized for:
- **Desktop** - Full-featured dashboard experience
- **Tablet** - Optimized layouts for medium screens
- **Mobile** - Touch-friendly interface for on-the-go access

## 🚀 Deployment

### Backend Deployment
1. Set up MongoDB Atlas or your preferred MongoDB hosting
2. Configure environment variables for production
3. Deploy to your preferred platform (Heroku, DigitalOcean, AWS, etc.)
4. Ensure CORS settings allow your frontend domain

### Frontend Deployment
1. Update `NEXT_PUBLIC_API_URL` to your backend URL
2. Build the application: `npm run build`
3. Deploy to Vercel, Netlify, or your preferred platform
4. Configure environment variables in your deployment platform

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/new-feature`
3. Commit your changes: `git commit -am 'Add new feature'`
4. Push to the branch: `git push origin feature/new-feature`
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue in the GitHub repository
- Contact the development team
- Check the documentation for common solutions

## 🔮 Future Enhancements

- **AI Integration**: Advanced ML models for treatment recommendations
- **Telemedicine**: Video consultation capabilities
- **IoT Integration**: Wearable device data synchronization
- **Advanced Analytics**: Predictive health insights
- **Mobile Apps**: Native iOS and Android applications
- **Multi-language Support**: Internationalization
- **Advanced Reporting**: Custom report generation
- **Integration APIs**: Third-party healthcare system connections
