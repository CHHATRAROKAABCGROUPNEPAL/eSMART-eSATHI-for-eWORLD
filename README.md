By following these steps and using the provided files, you should be able to set up, install, and run the demo project on your local machine. If you encounter any issues, refer to the project documentation or seek assistance from the community.
please guide me how to run on my laptop?
Sure, I'll guide you through the process of running the demo project on your laptop. Follow these steps carefully.
Prerequisites
Before you start, ensure you have the following installed on your machine:
1.	Node.js (v14.x or higher)
2.	npm (v6.x or higher)
3.	MongoDB (running instance)
Step-by-Step Guide
1. Clone the Repository
First, clone the repository to your local machine:
bash
git clone https://github.com/CHHATRAROKAABCGROUPNEPAL/money-earning-app.git
cd money-earning-app
2. Backend Setup
Navigate to the backend directory and install the dependencies:
bash
cd backend
npm install
Create a .env file in the backend directory and add the following variables:
backend/.envv4
MONGO_URI=mongodb://localhost:27017/money-earning-app
PORT=5000
Start the backend server:
bash
npm start
3. Frontend Setup
Navigate to the frontend directory and install the dependencies:
bash
cd ../frontend
npm install
Start the frontend development server:
bash
npm start
4. Running the App
1.	Start the Backend Server:
In the terminal where you navigated to the backend directory, start the backend server:
bash
npm start
This will start the backend server on port 5000.
2.	Start the Frontend Development Server:
In a separate terminal, navigate to the frontend directory and start the frontend development server:
bash
npm start
This will start the frontend development server on port 3000.
3.	Open Your Browser:
Open your browser and go to http://localhost:3000 to see the app in action.
Project Structure
Here is the structure of the demo project:
Code
demo-project/
├── backend/
│   ├── controllers/
│   │   └── userController.js
│   ├── models/
│   │   └── userModel.js
│   ├── routes/
│   │   └── userRoutes.js
│   ├── config/
│   │   └── db.js
│   ├── .env
│   ├── server.js
├── frontend/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── components/
│   │   │   └── App.js
│   │   ├── pages/
│   │   │   └── HomePage.js
│   │   ├── App.css
│   │   ├── index.js
│   └── package.json
├── README.md
├── package.json
└── .gitignore
 Public code references from 3 repositories
•	

•	

•	

Files
backend/server.js
backend/server.jsv3
const express = require('express');
const dotenv = require('dotenv');
const mongoose = require('mongoose');
const userRoutes = require('./routes/userRoutes');

 Public code references from 1 repository
•	

backend/config/db.js
backend/config/db.jsv3
const mongoose = require('mongoose');

const connectDB = async () => {
  try {
    await mongoose.connect(process.env.MONGO_URI, {
 Public code references from 1 repository
•	

backend/models/userModel.js
backend/models/userModel.jsv3
const mongoose = require('mongoose');

const userSchema = new mongoose.Schema({
  name: {
    type: String,
 Public code references from 5 repositories
•	

•	

•	

•	

•	

backend/controllers/userController.js
backend/controllers/userController.jsv3
const User = require('../models/userModel');

// Register a new user
const registerUser = async (req, res) => {
  const { name, email, password } = req.body;
 Public code references from 13 repositories
•	

•	

•	

•	

•	

•	

•	

•	

•	

•	

•	

•	

•	

backend/routes/userRoutes.js
backend/routes/userRoutes.jsv3
const express = require('express');
const { registerUser, getUsers } = require('../controllers/userController');

const router = express.Router();

backend/.env
backend/.envv5
MONGO_URI=mongodb://localhost:27017/demo-project
PORT=5000
 Public code references from 3 repositories
•	

•	

•	

frontend/public/index.html
frontend/public/index.htmlv3
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
 Public code references from 6 repositories
•	

•	

•	

•	

•	

•	

frontend/src/components/App.js
frontend/src/components/App.jsv3
import React from 'react';
import HomePage from '../pages/HomePage';

const App = () => {
  return (
 Public code references from 3 repositories
•	

•	

•	

frontend/src/pages/HomePage.js
frontend/src/pages/HomePage.jsv3
import React from 'react';

const HomePage = () => {
  return (
    <div>
 Public code references from 4 repositories
•	

•	

•	

•	

frontend/src/App.css
frontend/src/App.cssv3
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f0f0f0;
 Public code references from 3 repositories
•	

•	

•	

frontend/src/index.js
frontend/src/index.jsv3
import React from 'react';
import ReactDOM from 'react-dom';
import App from './components/App';
import './App.css';

 Public code references from 1 repository
•	

frontend/package.json
frontend/package.jsonv3
{
  "name": "frontend",
  "version": "1.0.0",
  "private": true,
  "dependencies": {
 Public code references from 5 repositories
•	

•	

•	

•	

•	

package.json
package.jsonv3
{
  "name": "demo-project",
  "version": "1.0.0",
  "scripts": {
    "start": "node backend/server.js",
 Public code references from 4 repositories
•	

•	

•	

•	

.gitignore
.gitignorev3
# Node modules
node_modules/

# Environment variables
backend/.env
README.mdv3
# Demo Project

This is a full-stack demo project designed to demonstrate how to set up, install, and run a Node.js and React application. The project includes both backend and frontend components.

## Project Structure
 Public code references from 6 repositories
•	

•	

•	

•	

•	

•	

By following these steps and using the provided files, you should be able to set up, install, and run the demo project on your local machine. If you encounter any issues, refer to the project documentation or seek assistance from the community.
how to install node.js, npm and mongodb in my laptop?
Sure! Here are the step-by-step instructions to install Node.js, npm, and MongoDB on your laptop.
1. Install Node.js and npm
Node.js comes with npm (Node Package Manager) automatically. Follow the instructions based on your operating system.
For Windows:
1.	Download the installer:
o	Go to the official Node.js website: https://nodejs.org/
o	Download the LTS (Long-Term Support) version.
2.	Run the installer:
o	Run the downloaded .msi installer.
o	Follow the installation steps and ensure that the "Add to PATH" option is checked.
3.	Verify the installation:
o	Open Command Prompt and type the following commands to check the installed versions:sh
o	node -v
o	npm -v
For macOS:
1.	Using Homebrew:
o	If you don't have Homebrew installed, you can install it by running the following command in Terminal:
sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
o	Once Homebrew is installed, you can install Node.js by running:
sh
brew install node
2.	Verify the installation:
o	Open Terminal and type the following commands to check the installed versions:sh
o	node -v
o	npm -v
For Linux (Ubuntu/Debian):
1.	Update the package index:
sh
sudo apt update
2.	Install Node.js and npm:
o	You can install Node.js from the NodeSource repository. Run the following commands:sh
o	curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -
o	sudo apt-get install -y nodejs
3.	Verify the installation:
o	Open Terminal and type the following commands to check the installed versions:sh
o	node -v
o	npm -v
2. Install MongoDB
For Windows:
1.	Download the installer:
o	Go to the official MongoDB website: https://www.mongodb.com/try/download/community
o	Download the MongoDB Community Server for Windows.
2.	Run the installer:
o	Run the downloaded .msi installer.
o	Follow the installation steps and ensure that the "Install MongoDB as a Service" option is checked.
3.	Verify the installation:
o	Open Command Prompt and type the following command to check the installed version:sh
o	mongod --version
For macOS:
1.	Using Homebrew:
o	If you have Homebrew installed, you can install MongoDB by running:sh
o	brew tap mongodb/brew
o	brew install mongodb-community@5.0
2.	Start MongoDB:
o	To start the MongoDB service, run:sh
o	brew services start mongodb/brew/mongodb-community
3.	Verify the installation:
o	Open Terminal and type the following command to check the installed version:sh
o	mongod --version
For Linux (Ubuntu/Debian):
1.	Import the MongoDB public GPG key:
sh
wget -qO - https://www.mongodb.org/static/pgp/server-5.0.asc | sudo apt-key add -
2.	Create the /etc/apt/sources.list.d/mongodb-org-5.0.list file:
sh
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/5.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-5.0.list
3.	Update the package index:
sh
sudo apt update
4.	Install MongoDB packages:
sh
sudo apt-get install -y mongodb-org
5.	Start MongoDB:
sh
sudo systemctl start mongod
6.	Verify the installation:
o	Open Terminal and type the following command to check the installed version:sh
o	mongod --version
Conclusion
By following these instructions, you should be able to install Node.js, npm, and MongoDB on your laptop. If you have any issues or need further assistance, feel free to ask!
