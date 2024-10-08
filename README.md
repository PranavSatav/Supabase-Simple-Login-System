# 🚀 Supabase Authentication Project

Welcome to the **Supabase Authentication Project**! This project showcases how to utilize Supabase for user registration and login functionality, all backed by a PostgreSQL database. In this guide, we'll walk you through the steps to set up the project and configure Supabase.

## 📚 Table of Contents

1. [Prerequisites](#prerequisites)
2. [Setting Up Supabase](#setting-up-supabase)
3. [Creating the Project](#creating-the-project)
4. [Configuring the Database](#configuring-the-database)
5. [Disabling Row-Level Security](#disabling-row-level-security)
6. [Running the Project](#running-the-project)

## ✅ Prerequisites

- Basic knowledge of HTML and JavaScript
- A web browser 🌐
- An internet connection 💻

## 🌟 Setting Up Supabase

1. **Go to Supabase URL**: Navigate to [Supabase](https://supabase.com) in your web browser.
2. **Create an Account**: Click on the "Start your project" button. If you don't have an account, sign up using your email address or through GitHub.
3. **Log In**: After creating your account, log in to your Supabase dashboard. 🎉

## 📦 Creating the Project

1. **Create a New Project**:
   - Click on the "New Project" button.
   - Enter a name for your project in the "Project Name" field.
   - Select a region closest to you for better performance. 🌍
   - Click on "Create new project." 🚀

2. **Obtain API Key and URL**:
   - Once the project is created, go to the "Settings" tab in your project.
   - Under "API," you'll find your `supabaseUrl` and `supabaseKey` (anon key). Note these down for use in your project. 🔑

## 🗄️ Configuring the Database

1. **Creating the Users Table**:
   - Navigate to the "Table Editor" in the Supabase dashboard.
   - Click on "Create a new table."
   - Name your table `users`.

2. **Adding Columns to the Users Table**:
   - Add the following columns to the `users` table:
     - `id`: Type - **Integer** (selected `8 int` instead of `bigint` as it was not available)
     - `email`: Type - **Text**
     - `password`: Type - **Text**
   - Ensure the `id` column is set as the primary key. 🏷️

3. **Save the Table**: Once you've added the columns, save the changes. 💾
_____________________________________________________________________
   <u>**[OPTIONAL IF YOU LAZY TO CREATE TABLE MANUALLY]**</u>
_____________________________________________________________________
   
 **Adding Columns to the Users Table**:
   - Instead of manually adding each column, you can create the entire table using a simple SQL command. 
   - Navigate to the **SQL Editor** in your Supabase dashboard.
   - Paste the following SQL code and hit **Run**:

   
 ```sql
   CREATE TABLE users (
       id SERIAL PRIMARY KEY,
       email TEXT NOT NULL,
       password TEXT NOT NULL
   );
 ```

And **Press RUN**, That's it..

## 🔒 Disabling Row-Level Security

1. **Disable Row-Level Security**:
   - Go to the "Authentication" section of your project.
   - Find the option for "Row Level Security" and disable it. This step is crucial for allowing unrestricted access for the operations in this example. 🚫

## 🏃‍♂️ Running the Project

1. **Open the Project File**: 
   - Locate the `login.html` file in your project directory. You can use any code editor you prefer, such as Visual Studio Code, Sublime Text, or Notepad++. Right-click on the `login.html` file and select "Open with" to choose your code editor.

2. **Configure Supabase Credentials**: 
   - In the code editor, scroll down to find the section where the Supabase client is initialized. You should see something like this:
     ```javascript
     const supabaseUrl = '[your project url]';
     const supabaseKey = '[your big anon api key]';
     ```
   - Replace `[your project url]` with the URL of your Supabase project that you noted down earlier. This will typically look something like `https://your-project-ref.supabase.co`.
   - Replace `[your big anon api key]` with the Anon public API key from your Supabase project settings. This key allows your front-end application to communicate with your Supabase backend.

3. **Save Your Changes**: 
   - After updating the credentials, make sure to save the changes in your code editor. This is usually done by pressing `Ctrl + S` (Windows) or `Command + S` (Mac). 💾

4. **Run the HTML File**: 
   - Once you've saved the changes, you can run the HTML file. Simply navigate to the location of the `login.html` file in your file explorer, and double-click on it. This will open the file in your default web browser.
   - Alternatively, you can right-click the `login.html` file and choose "Open with" followed by your preferred web browser.

5. **Test the Application**: 
   - When the browser opens the file, you should see the registration and login forms. You can now register a new user by filling out the registration form and then log in with the credentials you created. 📝

By following these steps, your application should be up and running, allowing you to register and log in using Supabase! 🎉
