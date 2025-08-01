# SpotWise - All in One Service Provider

[cite_start]SpotWise is an innovative, location-based web platform designed to seamlessly connect service seekers with local service providers within a defined 5km radius[cite: 63, 78]. [cite_start]It addresses the inefficiencies found in traditional service platforms, such as poor geolocation accuracy, insecure transactions, and scalability issues[cite: 66, 90].

## Project Overview

[cite_start]SpotWise's primary objective is to bridge the gap between service seekers and service providers like plumbers, electricians, and carpenters[cite: 78, 18, 71]. [cite_start]By focusing on hyper-local interactions, the platform ensures faster response times and higher service quality[cite: 67]. [cite_start]The platform is designed for scalability and can handle a growing user base without compromising performance[cite: 68].

## Key Features

* [cite_start]**5km Radius Matching**: The platform utilizes the Google Maps API for precise geolocation and MongoDB's geospatial indexing for efficient proximity-based searches, prioritizing providers closest to the seeker[cite: 64, 85, 86, 114, 115].
* [cite_start]**JWT Authentication**: SpotWise integrates JSON Web Tokens (JWT) for secure, role-based access control (RBAC), with tokens configured to expire after 24 hours[cite: 65, 84, 116, 117, 122]. [cite_start]All API calls are secured via TLS 1.3 to prevent attacks[cite: 123, 214].
* [cite_start]**Real-Time Alerts**: WebSockets are implemented to provide instant notifications to providers when a new request matches their skills and location[cite: 87, 127, 128]. [cite_start]A fallback to HTTP polling is in place if the WebSocket connection fails[cite: 132, 133].
* [cite_start]**PIN-based Verification**: A unique 6-digit PIN is automatically generated when a provider accepts a request, which is securely stored with SHA-256 hashing[cite: 65, 135, 137]. [cite_start]This PIN is used to verify service completion and prevent fraud[cite: 95, 138, 139, 140, 141].
* [cite_start]**Cross-Platform Responsiveness**: The user interface is developed using Bootstrap 5, guaranteeing a responsive design that adapts seamlessly to smartphones, tablets, and desktops[cite: 81, 145, 147].
* [cite_start]**Service History & Analytics**: User dashboards allow seekers to view past requests and provider ratings, while providers can track completed jobs, earnings, and customer feedback[cite: 154, 155, 156].

## Technology Stack

### Backend
* [cite_start]**Framework**: Node.js (v16.x) with Express.js (v4.17.x)[cite: 64, 80, 166, 167].
* [cite_start]**Database**: MongoDB (v5.0) with Mongoose ODM (v6.x) for efficient data management and native geospatial support[cite: 64, 80, 170].
* [cite_start]**Authentication**: JSON Web Tokens (JWT) using the `jsonwebtoken` library (v8.5.x)[cite: 65, 172, 173, 194].

### Frontend
* [cite_start]**Framework**: The front end uses HTML5 for structure and CSS3 with media queries for styling[cite: 206, 207].
* [cite_start]**Geolocation**: Google Maps JavaScript API (v3.52) for geolocation services[cite: 64, 208].

### Deployment
* [cite_start]**Backend**: The server is deployed on Vercel[cite: 200].
* [cite_start]**Database**: The primary datastore is hosted on MongoDB Atlas[cite: 200].
* [cite_start]**Frontend**: The frontend is hosted on GitHub Pages[cite: 201].
