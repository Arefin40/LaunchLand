# LAUNCHLAND - Tech Product Discovery Platform

A tech product discovery and launch platform designed to help users explore, showcase, and share innovative digital products, including web applications, AI tools, software, games, and mobile apps. LaunchLand provides a community-driven platform where users can submit products, engage through upvotes and reviews, and discover trending innovations.

**Live Demo:** [LaunchLand](https://sa-launchland.web.app/)

**Frontend Repository:** [LaunchLand](https://github.com/Arefin40/LaunchLand)

**Backend Repository:** [LaunchLand Server](https://github.com/Arefin40/LaunchLand-server)

**Backend API:** [LaunchLand API](https://launchland-server.vercel.app/)

## Tech Stack

**Prerequisites** 
Make sure you have the following installed:

- Git
- Node.js 18+
- pnpm
- MongoDB Atlas Account
- Firebase Account
- Stripe Account

**Frontend**
- React 18 - Component-based UI development
- Vite 5 - Fast development server and build tool
- JavaScript - Application logic
- Tailwind CSS v3 - Responsive styling
- React Router DOM - Client-side routing and protected routes
- Firebase Authentication - User authentication and social login
- TanStack React Query - Server state management and data fetching
- Axios - HTTP requests and API communication
- React Hook Form - Form handling and validation
- Stripe.js - Secure payment integration
- React Hot Toast - Notifications and user feedback
- React Datepicker - Date selection
- Recharts - Data visualization and dashboard charts
- Swiper - Responsive sliders and carousels

**Backend**
- Node.js - Server-side JavaScript runtime
- Express.js - REST API development
- MongoDB - Database management
- Mongoose - MongoDB object modeling
- JWT - Authentication and authorization
- Stripe - Payment processing
- CORS - Cross-origin resource sharing
- dotenv - Environment variable management
- Nodemon - Automatic server restarting during development

**Hosting**
- Firebase Hosting - Frontend deployment
- Vercel - Backend deployment

## Key Features

- Role-based authentication and authorization for Users, Moderators, and Admins using Firebase Authentication and JWT.
- Product submission and moderation workflow, allowing moderators to review, approve, or reject submissions and manage reported products.
- Community-driven product ranking through upvotes, with duplicate voting prevention.
- Product discovery with Featured and Trending sections, search, and pagination.
- Stripe payment integration to unlock premium features.

**Problems Solved**

- Difficulty discovering innovative digital products across different platforms.
- Limited visibility and exposure for newly launched applications and tech products.
- Lack of a centralized platform for developers to showcase their products.
- Limited community engagement and feedback for product creators.
- Difficulty maintaining product quality without a structured moderation system.
- Lack of organized product ranking based on community engagement.
- Limited opportunities for creators to access premium product submission features.

## Run Locally

**1. Clone the frontend repository**

```bash
git clone https://github.com/Arefin40/LaunchLand.git
cd LaunchLand
```

**2. Install frontend dependencies**

```bash
pnpm install
```

**3. Configure Firebase and frontend environment variables**

Create a `.env.local` file in the frontend root directory.

```env
APP_API_URL=http://localhost:3000

APP_API_KEY=your_firebase_api_key
APP_AUTH_DOMAIN=your_firebase_auth_domain
APP_PROJECT_ID=your_firebase_project_id
APP_STORAGE_BUCKET=your_firebase_storage_bucket
APP_MESSAGING_SENDER_ID=your_messaging_sender_id
APP_APP_ID=your_firebase_app_id
```

Replace the placeholder values with your Firebase project credentials. Enable Email/Password, Google, GitHub, and Facebook authentication providers in Firebase Console.

Configure the Stripe publishable key in the frontend payment configuration if required.

**4. Clone and configure the backend**

Open another terminal:

```bash
git clone https://github.com/Arefin40/LaunchLand-server.git
cd LaunchLand-server
pnpm install
```

Create a `.env` file in the backend root directory.

```env
PORT=3000
MONGO_DB_URI=your_mongodb_connection_string
DB_NAME=your_database_name
ACCESS_TOKEN_SECRET=your_jwt_secret
STRIPE_SECRET_KEY=your_stripe_secret_key
```

Replace the placeholder values with your actual MongoDB, JWT, and Stripe credentials.

**5. Start the backend server**

```bash
pnpm run serve
```

The backend will run at `http://localhost:3000`.

**6. Start the frontend development server**

Return to the frontend terminal:

```bash
pnpm run dev
```

Visit: `http://localhost:5173`

**7. Production build**

```bash
pnpm run build
pnpm run preview
```

## Challenges Faced During Development
- **Role-Based Authorization:** Implementing different permission levels for Users, Moderators, and Admins while securing both frontend routes and backend API endpoints. Firebase Authentication, JWT, and role-based authorization helped establish controlled access.
- **Product Moderation Workflow:** Managing the lifecycle of submitted products, including review, approval, rejection, and reported content. A structured moderation system helped maintain control over published products.
- **Voting Integrity:** Preventing users from voting multiple times on the same product while maintaining reliable community-driven rankings. Backend-side vote validation helped ensure voting consistency.
- **Payment Integration:** Connecting Stripe payment processing with premium feature access. Integrating the payment flow with backend services and user subscription information enabled premium functionality.

**Live Demo:** https://sa-launchland.web.app/

**LAUNCHLAND - Discover, Launch, and Grow Innovative Ideas.**
