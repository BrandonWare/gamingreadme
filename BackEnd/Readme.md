# Backend README for Gaming Web Application

# Overview
This is the backend API for the gaming web application. It is built using Node.js and Express.js, providing dynamic content, game data management, and other functionalities. The backend interacts with a PostgreSQL database and exposes various API endpoints for the frontend to interact with. The goal of the backend is to manage the application’s data and provide the necessary functionality for the frontend.

# Technlogies Used
- Node.js

- Express.js

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

# Navigate into the project folder:

cd gamingapp

# Install the required dependencies:

npm install

# Database Setup
PostgreSQL Setup:
Install PostgreSQL:
If you don’t have PostgreSQL installed, you can follow the installation guide here: PostgreSQL Installation Guide.

# Create a Database:
After installing PostgreSQL, create a new database for the project:

createdb gamingdb

# Configure the Database:
The database connection is configured in the .env file with the following variable:

DATABASE_URL=postgres://username:password@localhost:5432/gamingdb

Replace username, password, and gamingdb with your actual PostgreSQL credentials and database name.

# Steps to Set Up Tables in pgAdmin 4 UI
Open pgAdmin 4:

Launch pgAdmin 4 on your computer.

Connect to your PostgreSQL server by entering your credentials (username and password).

Select the Database:

In the left sidebar, expand the server where your PostgreSQL is running.

Under the Databases section, find and click on your database (gamingdb). If you haven't created it yet, right-click on "Databases" and select Create -> Database to create a new one. You can name it gamingdb (or any name of your choice).

Navigate to the "Tables" Section:

After selecting your database, expand the Schemas section, then the public schema.

Under public, find the Tables section. Right-click on Tables and select Create -> Table.

Create the users Table:

Table Name: In the "General" tab, enter the name for your first table: users.

Define Columns:

Click on the Columns tab.

Click the + button to add a new column.

For each column, provide the following:

Column Name: id

Data Type: SERIAL

Check the Primary Key option to make this column the primary key.

Click Save to add the column.

Now, add another column:

Column Name: gamename

Data Type: VARCHAR(100)

Check the NOT NULL option to ensure the gamename field cannot be empty.

After adding both columns, click Save to create the users table.

Create the games Table:

Table Name: In the "General" tab, enter the name for your second table: games.

Define Columns:

Click on the Columns tab.

Click the + button to add a new column.

For each column, provide the following:

Column Name: id

Data Type: SERIAL

Check the Primary Key option to make this column the primary key.

Click Save to add the column.

Now, add another column:

Column Name: gamename

Data Type: VARCHAR(100)

Check the NOT NULL option to ensure the gamename field cannot be empty.

After adding both columns, click Save to create the games table.

Verify the Tables:

After you’ve created the tables, you should see the users and games tables listed under the Tables section in the public schema.

You can expand each table to see the columns and their details.

# Start the Backend Server

Once the database is set up and the tables are created, start the backend server by running:

npm start

This will start the backend API server at http://localhost:5000 (or another specified port).

# API Documentation

Endpoints:

GET /gaming

Description: Fetches a list of all games in the system.

Response Example:

[
  { "id": 1, "gamename": "John Doe" },
  { "id": 2, "gamename": "Jane Smith" }
]

POST /gaming

Description: Creates a new user.

Request Example:

{
  "gamename": "New User"
}

Response Example

{ "id": 3, "gamename": "New User" }

GET /games

Description: Fetches a list of all games.

Response Example:

[
  { "id": 1, "gamename": "Game 1" },
  { "id": 2, "gamename": "Game 2" }
]

POST /gaming

Description: Adds a new game to the system.

Request Example:

{
  "gamename": "New Game"
}

Response Example:

{ "id": 3, "gamename": "New Game" }

# Deployment Guide

Initialize a Git Repository:
If you haven’t already initialized a Git repository in the project, run the following commands:

git init

Add Your Remote GitHub Repository:
Create a new repository on GitHub (e.g., https://github.com/BrandonWare/gamingapp.git) and add it as the remote:

git remote add origin git@github.com:BrandonWare/gamingapp.git

Commit Your Code:
Add all the files to the staging area and commit them:

git add .
git commit -m "Initial commit"

Push Code to GitHub:
Push the code to GitHub:

git push  origin 

This will upload the project to the GitHub repository you created.

# Coding Standards:
Follow JavaScript ES6+ syntax.

Use functional components with hooks.

Ensure proper indentation and code formatting.

Write meaningful commit messages.

# License

This project is licensed under the MIT License - see the LICENSE file for details.




