# TasteQuest – Restaurant Discovery Platform

TasteQuest is a full-stack restaurant discovery web application developed to help users explore authentic restaurants across Karnataka. The platform enables users to browse restaurants city-wise, book tables online, save favourite restaurants, participate in an interactive food quiz and contact the administrators through a responsive and user-friendly interface.

The project was developed as an academic team project using **HTML, CSS, JavaScript, Node.js, Express.js, and MongoDB Atlas**.

# Live Demo 
Frontend: https://sinchanahemanth.github.io/FWD_TasteQuest/

Backend API: https://fwd-tastequest.onrender.com

# Project Features

- Browse restaurants across multiple cities in Karnataka.
- View city-wise restaurant listings.
- View restaurant details and menu highlights.
- Book restaurant tables online.
- Receive booking confirmation emails using Nodemailer.
- Save favourite restaurants.
- Participate in an interactive food quiz.
- Contact the administrators through the Contact Us form.
- Responsive user interface.
- Frontend deployed using GitHub Pages.
- Backend REST API deployed as a Node web service on Render.

# Project Structure

```
FWD_TasteQuest
│
├── backend
│   ├── app.js
│   ├── package.json
│   └── package-lock.json
│
├── docs
│   ├── assets
│   ├── index.html
│   ├── citiespage.html
│   ├── favourites.html
│   ├── quizpage.html
│   ├── script.js
│   ├── quiz.js
│   └── style.css
│
├── .gitignore
└── README.md
```

# Technologies Used

## Frontend

- HTML5
- CSS3
- JavaScript

## Backend

- Node.js
- Express.js

## Database

- MongoDB Atlas
- Mongoose

## Additional Packages

- Nodemailer
- CORS
- Dotenv

## Deployment

- GitHub Pages (static frontend, served from the docs folder)
- Render (Node.js backend web service)
- MongoDB Atlas (managed cloud database)

# System Workflow

1. User opens the TasteQuest website.
2. User explores restaurants across different Karnataka cities.
3. Restaurant information is displayed on the frontend.
4. User selects a restaurant and books a table.
5. Booking details are sent to the Express backend.
6. Backend validates booking availability.
7. Booking information is stored in MongoDB Atlas.
8. A confirmation email is sent to the user.
9. Users can submit queries through the Contact Us form.
10. Contact details are stored in MongoDB and forwarded via email.

# Database

MongoDB Atlas is used to store application data.

## Booking Collection

Each booking stores:

- Restaurant Name
- Location
- Booking Date
- Number of People
- Time Slot
- Email Address

## Contact Collection

Each contact request stores:

- Name
- Phone Number
- Message

# Backend API Endpoints

## POST /book

Creates a new restaurant booking.

### Request Body

- Restaurant Name
- Location
- Booking Date
- Number of People
- Time Slot
- Email Address

### Functionality

- Checks booking availability.
- Stores booking information in MongoDB.
- Sends booking confirmation email.

## POST /contact

Submits a contact request.

### Request Body

- Name
- Phone Number
- Message

### Functionality

- Stores contact information in MongoDB.
- Sends notification email to the administrator.

# Local Setup

## Clone the Repository

```bash
git clone https://github.com/Shreya-Raj08/FWD_TasteQuest.git
```

## Backend Setup

Navigate to the backend folder.

```bash
cd backend
```

Install all dependencies.

```bash
npm install
```

Create a `.env` file inside the backend folder.

Example:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_gmail_app_password
```

Note: `EMAIL_PASS` must be a Gmail **App Password**, not your regular account password. Enable 2-Step Verification on the Google account and generate a 16-character App Password for Nodemailer to authenticate.

Start the backend server.

```bash
node app.js
```

## Frontend

Open:

```
docs/index.html
```

or access the deployed GitHub Pages website.

### Pointing the Frontend at a Local Backend

By default the frontend calls the deployed Render API. To test against the backend you just started locally, replace the API base URL in `docs/script.js` (2 occurrences) and `docs/quiz.js` (2 occurrences):

```js
// from
https://fwd-tastequest.onrender.com
// to
http://localhost:5000
```

Without this change the page will keep hitting the production API and your local server will receive no requests.

# Project Highlights

- Full-stack web application
- Responsive user interface
- MongoDB Atlas integration
- REST-based backend architecture
- Booking availability validation
- Automatic email confirmations using Nodemailer
- Contact form with database storage
- Frontend deployed on GitHub Pages
- Backend deployed on Render

# Future Enhancements

- User Authentication
- Restaurant Reviews and Ratings
- Search and Advanced Filters
- AI-based Restaurant Recommendation System
- Online Payment Gateway
- User Booking History
- Restaurant Owner Dashboard
- Admin Panel
- Google Maps Integration
