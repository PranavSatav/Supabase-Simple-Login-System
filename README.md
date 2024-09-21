# Supabase Authentication Project

This project demonstrates how to use Supabase for user registration and login functionality, utilizing a PostgreSQL database for storing user information. This guide outlines the steps taken to set up the project and configure Supabase.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Setting Up Supabase](#setting-up-supabase)
3. [Creating the Project](#creating-the-project)
4. [Configuring the Database](#configuring-the-database)
5. [Disabling Row-Level Security](#disabling-row-level-security)
6. [Running the Project](#running-the-project)

## Prerequisites

- Basic knowledge of HTML and JavaScript
- A web browser
- An internet connection

## Setting Up Supabase

1. **Go to Supabase URL**: Navigate to [Supabase](https://supabase.io) in your web browser.
2. **Create an Account**: Click on the "Start your project" button. If you don't have an account, sign up using your email address or through GitHub.
3. **Log In**: After creating your account, log in to your Supabase dashboard.

## Creating the Project

1. **Create a New Project**:
   - Click on the "New Project" button.
   - Enter a name for your project in the "Project Name" field.
   - Select a region closest to you for better performance.
   - Click on "Create new project."

2. **Obtain API Key and URL**:
   - Once the project is created, go to the "Settings" tab in your project.
   - Under "API," you'll find your `supabaseUrl` and `supabaseKey` (anon key). Note these down for use in your project.

## Configuring the Database

1. **Creating the Users Table**:
   - Navigate to the "Table Editor" in the Supabase dashboard.
   - Click on "Create a new table."
   - Name your table `users`.

2. **Adding Columns to the Users Table**:
   - Add the following columns to the `users` table:
     - `id`: Type - **Integer** (selected `8 int` instead of `bigint` as it was not available)
     - `email`: Type - **Text**
     - `password`: Type - **Text**
   - Ensure the `id` column is set as the primary key.

3. **Save the Table**: Once you've added the columns, save the changes.

## Disabling Row-Level Security

1. **Disable Row-Level Security**:
   - Go to the "Authentication" section of your project.
   - Find the option for "Row Level Security" and disable it. This step is crucial for allowing unrestricted access for the operations in this example.

## Running the Project

1. **Clone the Repository**: Clone the GitHub repository containing the project files to your local machine.
   ```bash
   git clone <your-repository-url>
