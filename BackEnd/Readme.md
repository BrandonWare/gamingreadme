# BackEnd ReadME for Gaming

# Overview
This is the backend API for the gaming web application. It is built using Node.js and Express.js, serving dynamic content and  game data management, and more. The backend connects to a PostgreSQL database and exposes various API endpoints for the frontend to interact with. The goal of the backend is to manage the application’s data and provide the necessary functionality for the frontend.

# Technologies Used:

- Node.js

- Express

- PostgreSQL 

# Table of Contents

- Project Title & Overview

- Installation & Setup

- API Documentation

- Database Setup

- Authentication & Security

- Deployment Guide

- License & Contribution Guidelines

# Installation & Setup

Required Dependencies:

- Node.js

- Express.js

- PostgreSQL

# Steps to Install Dependencies and Run Locally:

Clone the repository: git@github.com:BrandonWare/gamingapp.git

Navigate into the project folder:

cd gamingapp

# Install the required dependencies:

Database Setup
PostgreSQL Setup:
Install PostgreSQL: If you don’t have PostgreSQL installed, you can follow the installation guide here:[ PostgreSQL Installation Guide.](https://www.postgresql.org/download/)

Create a Database: After installing PostgreSQL, create a new database for the project:


createdb gamingdb
Configure the Database: The database connection is configured in the .env file with the following variable:


DATABASE_URL=postgres://username:password@localhost:5432/gamingdb
Replace username, password, and gamingdb with your actual PostgreSQL credentials and database name.


Start the Backend Server: Once the database is set up, start the backend server by running:

npm start
This will start the backend API server at http://localhost:5000 (or another specified port).

# create tables in pgadmin

Right-click on the "Tables" section under your database (gamingdb) in the left sidebar.

Choose Create -> Table from the context menu.

In the dialog box that appears, give your table a name (e.g., users).

Click on the Columns tab to start adding columns.

Add id as a SERIAL column and set it as the Primary Key.

Add gamename as a VARCHAR(100) column and check the NOT NULL option.

Click Save to create the table.

Repeat the process for the games table.


7.)
API Documentation
GET /users
Description: Fetches a list of all users in the system.

Response Example:

[
  { "id": 1, "gamename": "John Doe" },
  { "id": 2, "gamename": "Jane Smith" }
]
POST /users
Description: Creates a new user.

Request Example:

{
  "gamename": "New User"
}
Response Example:

json
Copy
{ "id": 3, "gamename": "New User" }
GET /games
Description: Fetches a list of all games.

Response Example:


[
  { "id": 1, "gamename": "Game 1" },
  { "id": 2, "gamename": "Game 2" }
]
POST /games
Description: Adds a new game to the system.

Request Example:


{
  "gamename": "New Game"
}
Response Example:


{ "id": 3, "gamename": "New Game" }

8.)

Database Setup

PostgreSQL Setup:

Install PostgreSQL: If you don’t have PostgreSQL installed, you can follow the installation guide here: PostgreSQL Installation Guide.

Create a Database: After installing PostgreSQL, create a new database for the project:

createdb gamingdb
Configure the Database: The database connection is configured in the .env file with the following variable:


DATABASE_URL=postgres://username:password@localhost:5432/gamingdb

Replace username, password, and gamingdb with your actual PostgreSQL credentials and database name.

Set Up the Database Schema: Use Sequelize to create the necessary database tables. After you’ve set the models in the models/ directory, run the following command to create the tables:

npx sequelize-cli db:migrate
This will create the tables based on the models you’ve defined (e.g., User, Game).

Start the Backend Server: Once the database is set up, start the backend server by running:


npm start

This will start the backend API server at http://localhost:8008 (or another specified port).

9.)

Deployment Guide

Initialize a Git Repository: If you haven’t already initialized a Git repository in the project, run the following commands:


git init
Add Your Remote GitHub Repository: Create a new repository on GitHub (e.g., https://github.com/BrandonWare/gamingapp.git

Add this repository as the remote:


git remote add origin git@github.com:BrandonWare/gamingapp.git
Commit Your Code: Add all the files to the staging area and commit them:


git add .
git commit -m "Initial commit"

Push Code to GitHub:

git push -u origin main
This will upload the project to the GitHub repository you just created.










