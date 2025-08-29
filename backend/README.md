# MedSync Server

The backend API server for MedSync, handling all data operations, authentication, and business logic for the healthcare platform.

## 🔗 Links

- **Live API:** [https://medsync-server.onrender.com](https://medsync-server.onrender.com)
- **GitHub Repository:** [https://github.com/Lokesh-reddy18/MedSync-server](https://github.com/Lokesh-reddy18/MedSync-server)
- **Frontend Client:** [https://med-sync-client.vercel.app/](https://med-sync-client.vercel.app/)
- **Admin Panel:** [https://med-sync-admin.vercel.app/](https://med-sync-admin.vercel.app/)

## 🚀 Features

- RESTful API architecture
- User authentication and authorization
- Doctor management
- Appointment scheduling
- Payment processing with Stripe
- File uploads with Cloudinary
- MongoDB database integration
- Secure password hashing
- JWT token authentication

## 🛠️ Tech Stack

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- Bcrypt
- Stripe
- Cloudinary
- Multer

## 🏗️ Project Structure

```
backend/
├── config/
│   ├── mongodb.js
│   └── cloudinary.js
├── controllers/
│   ├── authController.js
│   ├── userController.js
│   └── doctorController.js
├── middlewares/
│   ├── auth.js
│   └── upload.js
├── models/
│   ├── User.js
│   └── Doctor.js
├── routes/
│   ├── userRoutes.js
│   └── doctorRoutes.js
└── server.js
```

## 🚀 Getting Started

1. Clone the repository:
```bash
git clone https://github.com/Lokesh-reddy18/MedSync-server.git
```

2. Install dependencies:
```bash
cd MedSync-server
npm install
```

3. Create a `.env` file:
```
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
STRIPE_SECRET_KEY=your_stripe_secret_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

4. Start the development server:
```bash
npm run dev
```

## 📦 Production Deployment

The server is deployed on Render. To deploy:

1. Create a new Web Service on Render
2. Connect your GitHub repository
3. Configure environment variables
4. Deploy

## 🔧 Environment Variables

- `MONGODB_URI`: MongoDB connection string
- `JWT_SECRET`: Secret key for JWT tokens
- `STRIPE_SECRET_KEY`: Stripe API secret key
- `CLOUDINARY_CLOUD_NAME`: Cloudinary cloud name
- `CLOUDINARY_API_KEY`: Cloudinary API key
- `CLOUDINARY_API_SECRET`: Cloudinary API secret

## 📚 API Documentation

### Authentication Endpoints
- POST `/api/user/register` - User registration
- POST `/api/user/login` - User login
- POST `/api/doctor/register` - Doctor registration
- POST `/api/doctor/login` - Doctor login

### User Endpoints
- GET `/api/user/profile` - Get user profile
- PUT `/api/user/profile` - Update user profile
- GET `/api/user/appointments` - Get user appointments

### Doctor Endpoints
- GET `/api/doctor/list` - Get all doctors
- GET `/api/doctor/profile` - Get doctor profile
- PUT `/api/doctor/profile` - Update doctor profile

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is licensed under the MIT License.