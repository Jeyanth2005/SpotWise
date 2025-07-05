SpotWise - All-in-One Service Provider Platform
Overview
SpotWise is a location-based web platform designed to connect service seekers with local service providers (e.g., plumbers, electricians, carpenters, cleaners) within a 5 km radius. Developed as part of the AICTE Activity Point Programme by students of PSG College of Technology, SpotWise leverages modern web technologies to deliver a seamless, secure, and efficient user experience. The platform addresses inefficiencies in traditional service marketplaces by offering real-time geolocation, secure authentication, and instant notifications.
Features

5 km Radius Matching: Utilizes Google Maps API and MongoDB geospatial queries for precise, proximity-based service provider matching.
JWT Authentication: Secure role-based access control (RBAC) for seekers and providers using JSON Web Tokens with 24-hour expiry.
Real-Time Notifications: WebSocket-based alerts for instant updates on service requests, with fallback to HTTP polling.
PIN Verification System: 6-digit PIN generation and validation for secure transaction completion.
Responsive Design: Built with Bootstrap 5 for a mobile-first, cross-platform user interface.
Service History & Analytics: User dashboards to track past requests, provider ratings, and admin analytics for system monitoring.
Interactive Service Map: Dynamic map interface for creating and managing service requests with real-time location updates.
Scalability: Handles 1,000+ concurrent users with MongoDB Atlas and Vercel deployment.

Tech Stack
Frontend

HTML5, CSS3, JavaScript: Core web technologies for structure and interactivity.
Bootstrap 5: Responsive UI framework for mobile, tablet, and desktop compatibility.
Google Maps JavaScript API (v3.52): Geolocation, mapping, and Places API for location search and autocomplete.
jQuery (3.4.1): DOM manipulation and AJAX requests.
Font Awesome: Icons for enhanced UI.
Custom CSS: Additional styling for map and request interfaces (map-styles.css).

Backend

Node.js (v16.x): Asynchronous server-side runtime.
Express.js (v4.17.x): RESTful API routing and middleware.
MongoDB (v5.0): NoSQL database with geospatial indexing (2dsphere).
Mongoose ODM (v6.x): MongoDB object modeling.
JSON Web Tokens (jsonwebtoken v8.5.x): Stateless authentication with HS256 algorithm.
Bcryptjs: Password hashing for secure user authentication.
Socket.IO: Real-time bidirectional communication.
Object-Assign: Polyfill for Object.assign to ensure compatibility with older browsers.

Deployment

MongoDB Atlas: Cloud-hosted database with M0 free tier.
Vercel: Backend hosting with environment variable management.
GitHub Pages: Frontend static site hosting.
GitHub Actions: CI/CD pipeline for automated deployment.

Project Structure
SpotWise/
├── frontend/
│   ├── public/
│   │   ├── index.html           # Main landing page
│   │   ├── service.html          # Services page
│   │   ├── service-map.html      # Interactive service map interface
│   │   ├── css/
│   │   │   ├── bootstrap.css     # Bootstrap framework styles
│   │   │   ├── style.css         # Custom styles
│   │   │   └── map-styles.css    # Map-specific styles
│   │   ├── js/
│   │   │   ├── auth.js           # Authentication handling
│   │   │   └── custom.js         # Custom client-side scripts
│   │   └── images/               # Static assets (e.g., plumbing.jpeg, electrical.png)
├── models/
│   ├── UserModel.js              # User schema (seeker/provider roles, location)
│   └── ServiceRequest.js         # Service request schema
├── controllers/
│   ├── authController.js         # Authentication routes (register, login, logout)
│   └── serviceController.js      # Service request handling
├── node_modules/
│   └── object-assign/           # Polyfill for Object.assign
├── index.js                     # Main server entry point
├── package.json                 # Node.js dependencies and scripts
└── vercel.json                  # Vercel deployment configuration

Installation and Setup
Prerequisites

Node.js (v16.x or higher)
MongoDB Atlas account
Google Maps API key with Places library enabled
Git

Steps

Clone the Repository:
git clone https://github.com/<your-username>/SpotWise.git
cd SpotWise


Install Dependencies:
npm install


Set Up Environment Variables: Create a .env file in the root directory with the following:
JWT_SECRET=your_jwt_secret_key
DB_URI=your_mongodb_atlas_connection_string
MAPS_API_KEY=your_google_maps_api_key


Run the Backend:
npm start


Host the Frontend:

Deploy static files in frontend/public/ to GitHub Pages or another static hosting service.

Update service-map.html, index.html, and service.html with your Google Maps API key in the script tag:
<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&libraries=places&callback=initMapsCallback" async defer></script>




Access the Application:


Lilliadis:

Backend: http://localhost:3000 (or Vercel URL)
Frontend: Hosted URL (e.g., GitHub Pages)

Usage

Sign Up / Sign In:

Register as a service seeker or provider via the sign-up page (index.html or service.html).
Log in with email and password to receive a JWT token.


Service Request (Seekers):

Access the Service Map (service-map.html) to create a request.
Select a service category (e.g., plumbing), provide a description, contact number, and location.
Receive real-time updates on provider acceptance and job status.


Service Acceptance (Providers):

View and accept requests within a 5 km radius on the Service Map.
Complete jobs using a 6-digit PIN for verification.


Profile and Service Management:

Update availability status and service location via the profile page.
View service history and ratings in the dashboard.


Service Map:

Interactive map interface to set service locations and view active requests.
Supports location search via Google Maps Places API and manual pin-drop.



Development Timeline

Phase 1: Research and Foundation (3 weeks)
Tech stack selection and competitor analysis.


Phase 2: Frontend Implementation (4 weeks)
UI development, including service request forms and interactive map.


Phase 3: Backend Development (7 weeks)
JWT authentication, MongoDB schemas, and geospatial matching algorithm.


Phase 4: Deployment (2 weeks)
MongoDB Atlas, Vercel, and GitHub Pages setup with CI/CD pipeline.



Contributors

Abishek J,
Dhanushkumar M,
Jeyanth V P,
Jothiswarar S,
Santhosh G.

Acknowledgments

Dr. V Santhi: Programme Coordinator
Dr. G. Sudha Sadasivam: Head of the Department
Dr. K. Sathiya Priya: Department Placement Coordinator
Ms. J. Adlene Anusha: Project Guide
Panel Members: Ms. S K Abirami, Dr. V Santhi, Ms. J. Adlene Anusha

License
This project is licensed under the MIT License. See the LICENSE file for details.
