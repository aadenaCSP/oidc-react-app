# OIDC React App


## Setup Instructions

### 1. Clone the repository

Clone the repository to your local machine using the following command:

```bash
git clone https://github.com/aadenaCSP/oidc-react-app.git
```

### 2. Navigate into the project directory
After cloning the repository, go to the project directory:

```bash
cd oidc-react-app
```

### 3. Install dependencies
Once inside the project folder, install the necessary dependencies using npm:

```bash
npm install
```
This will install all the packages required for the frontend React app and the backend server.

### 4. Set up GitHub OAuth credentials
You need to create OAuth credentials with GitHub for authentication:

Go to GitHub OAuth Applications.
Register a new OAuth application by filling out the form (e.g., for Application Name, use "OIDC React App").
After registering, note down the Client ID and Client Secret from the GitHub OAuth application page.
In the src/server.js file of the project, replace the placeholders for GITHUB_CLIENT_ID and GITHUB_CLIENT_SECRET with your actual credentials:

```bash
const GITHUB_CLIENT_ID = 'your-client-id';
const GITHUB_CLIENT_SECRET = 'your-client-secret';
```
### 5. Start the backend server
Run the backend server using Node.js:

```bash
node src/server.js
This will start the server on http://localhost:4000.
```
### 6. Start the React app
In another terminal window, run the React frontend:

```bash
npm start
This will open the app in your default web browser, usually at http://localhost:3000.
```
### 7. Logging in
When you open the app in the browser, you will see a "Log In with GitHub" button. Click this button to authenticate with GitHub. After successful authentication, your GitHub username, email, and profile details will be displayed.

## How it Works
The app uses OpenID Connect (OIDC) to authenticate users via GitHub.
After authentication, the app retrieves the user's information (e.g., name, email, username) using the GitHub API.
The retrieved information is displayed on the homepage of the app.
