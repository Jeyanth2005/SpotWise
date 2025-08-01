# SpotWise - Urban Service Matching System

SpotWise is an innovative, location-based web platform designed to seamlessly connect service seekers with local service providers within a defined 5km radius. It addresses the inefficiencies found in traditional service platforms, such as poor geolocation accuracy, insecure transactions, and scalability issues.

## Project Overview

SpotWise's primary objective is to bridge the gap between service seekers and service providers like plumbers, electricians, and carpenters. By focusing on hyper-local interactions, the platform ensures faster response times and higher service quality. The platform is designed for scalability and can handle a growing user base without compromising performance.

## Key Features

* **5km Radius Matching**: The platform utilizes the Google Maps API for precise geolocation and MongoDB's geospatial indexing for efficient proximity-based searches, prioritizing providers closest to the seeker.
* **JWT Authentication**: SpotWise integrates JSON Web Tokens (JWT) for secure, role-based access control (RBAC), with tokens configured to expire after 24 hours. All API calls are secured via TLS 1.3 to prevent attacks.
* **Real-Time Alerts**: WebSockets are implemented to provide instant notifications to providers when a new request matches their skills and location. A fallback to HTTP polling is in place if the WebSocket connection fails.
* **PIN-based Verification**: A unique 6-digit PIN is automatically generated when a provider accepts a request, which is securely stored with SHA-256 hashing. This PIN is used to verify service completion and prevent fraud.
* **Cross-Platform Responsiveness**: The user interface is developed using Bootstrap 5, guaranteeing a responsive design that adapts seamlessly to smartphones, tablets, and desktops.
* **Service History & Analytics**: User dashboards allow seekers to view past requests and provider ratings, while providers can track completed jobs, earnings, and customer feedback.

## Technology Stack

### Backend
* **Framework**: Node.js (v16.x) with Express.js (v4.17.x).
* **Database**: MongoDB (v5.0) with Mongoose ODM (v6.x) for efficient data management and native geospatial support.
* **Authentication**: JSON Web Tokens (JWT) using the `jsonwebtoken` library (v8.5.x).

### Frontend
* **Framework**: The front end uses HTML5 for structure and CSS3 with media queries for styling.
* **Geolocation**: Google Maps JavaScript API (v3.52) for geolocation services.

### Deployment
* **Backend**: The server is deployed on Vercel.
* **Database**: The primary datastore is hosted on MongoDB Atlas.
* **Frontend**: The frontend is hosted on GitHub Pages.
