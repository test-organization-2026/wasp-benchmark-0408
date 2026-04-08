The application uses Wasp's built-in authentication system but is currently missing a way for users to log out manually from their custom dashboard interface.

You need to implement a custom "Logout" button component within `Dashboard.jsx` that securely logs out the current authenticated user and redirects them to the login page in the Wasp frontend environment. 

**Constraints:**
- Import and use the built-in `logout` action directly from Wasp's auth module (`wasp/client/auth`).
- Do NOT create a custom Node.js server-side action or manual API route for the logout process.
- Ensure the user is explicitly redirected to the `/login` route upon successful logout.