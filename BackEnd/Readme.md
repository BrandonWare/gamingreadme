#Backend README for Gaming Web Application

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


