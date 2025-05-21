# Interview Prep AI App

## Project Structure

This project consists of two main components:
- Backend (Express.js)
- Frontend (React)

## Setup Instructions

### Backend Setup

1. Navigate to the backend folder in your terminal:
   ```
   cd backend
   ```

2. Install the required dependencies:
   ```
   npm install
   ```

3. **MongoDB Connection Setup:**
   - Visit [MongoDB](https://www.mongodb.com/)
   - Log in or create an account
   - Create a new project:
     - Click "New Project" button
     - Enter a project name and click "Next"
     - (Optional) Add team members, then click "Create Project"
   - Set up a database cluster:
     - Click on "Clusters" in the side menu
     - Click "Build a Cluster"
     - Select the Free Tier and enter a cluster name
     - Choose a cloud provider and region close to you
     - Click "Create Deployment"
   - Configure connection settings:
     - Add your IP address for access (use "Allow Access from Anywhere" if unsure)
     - Create a database user with a username and password
     - Click "Choose a connection method"
     - Select the "Drivers" option
     - Copy the Node.js connection string

4. **Environment Variable Setup:**
   - Create or update the `.env` file in the backend directory
   - Add your MongoDB connection string:
     ```
     MONGODB_URI=mongodb+srv://username:<password>@cluster0.example.mongodb.net/?retryWrites=true&w=majority
     ```
   - Replace `<password>` with the password of the database user created earlier

5. **Generate JWT Secret:**
   - Run the following command in your terminal:
     ```
     node -e "console.log(require('crypto').randomBytes(64).toString('hex'))"
     ```
   - Copy the output and add it to your `.env` file:
     ```
     JWT_SECRET=your_generated_secret_here
     ```

6. **Set Up Gemini API Key:**
   - Go to [Google AI Studio](https://ai.google.dev/)
   - Click "Get API Key" and then "Create API Key"
   - Copy the API key and add it to your `.env` file:
     ```
     GEMINI_API_KEY=your_gemini_api_key_here
     ```

7. **Start the Backend Server:**
   ```
   npm run dev
   ```

### Frontend Setup

1. Navigate to the frontend directory:
   ```
   cd frontend/interview-prep-ai
   ```

2. Install the required dependencies:
   ```
   npm install
   ```

3. Start the React development server:
   ```
   npm run dev
   ```

The application should now be running and will open automatically in your default web browser.

## Troubleshooting

If you encounter any issues during setup:
- Make sure you've followed all steps in the correct order
- Double-check that your MongoDB connection string is correct and the password has been properly replaced
- Verify that your JWT secret and Gemini API key are correctly set in the `.env` file
- Ensure you're using the recommended Node.js version

## Support

If you need additional help, please refer to the documentation or contact support through the channels provided with your purchase.

---

Happy interviewing!