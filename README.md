TasteQuest
Restaurant Discovery Platform

TasteQuest is a full-stack restaurant discovery web application that helps users explore authentic restaurants across Karnataka. The platform allows users to discover restaurants city-wise, book tables online, save favourite restaurants, participate in an interactive food quiz and contact the administrators through a responsive and user-friendly interface.
The project was developed as an academic team project using HTML, CSS, JavaScript, Node.js, Express.js, and MongoDB Atlas.

Live Demo: https://sinchanahemanth.github.io/FWD_TasteQuest/ 

Project Features
•	Discover authentic restaurants across multiple cities in Karnataka.
•	Browse restaurants city-wise through an intuitive interface.
•	View restaurant details and menu highlights.
•	Book restaurant tables online.
•	Receive booking confirmation emails using Nodemailer.
•	Save favourite restaurants for quick access.
•	Participate in an interactive food quiz.
•	Contact the administrators through the Contact Us form.
•	Fully responsive web interface.
•	Frontend deployed using GitHub Pages.

Technologies Used
Frontend
•	HTML5
•	CSS3
•	JavaScript
Backend
•	Node.js
•	Express.js
Database
•	MongoDB Atlas
•	Mongoose
Additional Packages
•	Nodemailer
•	CORS
•	Dotenv
Deployment
•	GitHub Pages

Project Structure
FWD_TasteQuest
|
|-- backend
|   |-- app.js
|   |-- package.json
|   |-- package-lock.json
|
|-- docs
|   |-- assets
|   |-- index.html
|   |-- citiespage.html
|   |-- favourites.html
|   |-- quizpage.html
|   |-- script.js
|   |-- quiz.js
|   |-- style.css
|
|-- .gitignore
|-- README.md

How the System Works
1.	User opens the TasteQuest website.
2.	User explores restaurants across different Karnataka cities.
3.	Restaurant information is displayed through the frontend.
4.	User selects a restaurant and books a table.
5.	Booking details are sent to the Express backend.
6.	Backend validates slot availability.
7.	Booking details are stored in MongoDB Atlas.
8.	A confirmation email is automatically sent to the user.
9.	Users can submit queries through the Contact Us form.
10.	Contact messages are stored in MongoDB and forwarded via email.

Database
MongoDB Atlas is used to store application data.
Booking Collection
Each booking stores:
•	Restaurant Name
•	Location
•	Booking Date
•	Number of People
•	Time Slot
•	Email Address
Contact Collection
Each message stores:
•	Name
•	Phone Number
•	Message

Backend API Endpoints
POST /book
Creates a new restaurant booking.
Request Body
•	Restaurant Name
•	Location
•	Booking Date
•	Number of People
•	Time Slot
•	Email
Functionality
•	Checks booking availability.
•	Stores booking in MongoDB.
•	Sends booking confirmation email.
POST /contact
Submits a contact request.
Request Body
•	Name
•	Phone Number
•	Message
Functionality
•	Stores contact information.
•	Sends notification email to the administrator.

Local Setup
Clone Repository
git clone https://github.com/SinchanaHemanth/FWD_TasteQuest.git
Backend Setup
cd backend
npm install
Create a .env file.
Example:
PORT=5000
MONGODB_URI=your_mongodb_connection_string
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_email_password
Start the server:
node app.js
Frontend
Open
docs/index.html
or use the GitHub Pages deployment.

Project Highlights
•	Full-stack web application.
•	Responsive UI.
•	MongoDB Atlas integration.
•	REST-based backend architecture.
•	Booking availability validation.
•	Automatic email confirmations.
•	Contact form with database storage.
•	GitHub Pages deployment.

Future Enhancements
•	User Authentication
•	Restaurant Reviews & Ratings
•	Search & Advanced Filters
•	AI-Based Restaurant Recommendation System
•	Online Payment Gateway
•	User Booking History
•	Restaurant Owner Dashboard
•	Admin Panel
•	Google Maps Integration

