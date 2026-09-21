# unearthed
A full-stack web application that serves and dynamically renders a collection of gifts. This project bridges a modern frontend build tool (Vite) with a custom Node.js/Express backend API to seamlessly deliver and display data to users.

Features & What I Built
Over the course of this project, I implemented both the server-side API and the client-side rendering logic. Key milestones include:

Express Backend Server: Built a custom Node.js backend using Express to serve application data.

Modular API Routing: Utilized express.Router() to separate gift-related routes (e.g., /gifts) from the main server.js file for cleaner architecture.

Vite Proxy Configuration: Configured vite.config.js to proxy frontend fetch requests to the local Express server, allowing the frontend and backend to communicate seamlessly during development.

Dynamic DOM Rendering: Wrote frontend JavaScript to fetch JSON data from the backend and dynamically construct HTML elements (div, h3, img) to display gift cards on the page without hardcoding them.

Client-Side URL Handling: Implemented custom logic to parse the current window.location.href and automatically redirect users to a 404.html page if they attempt to navigate to a non-existent route.

Production Build Setup: Configured Vite to output the bundled frontend files directly into a server/public directory (npm run build), allowing the Express server to host the entire application in production.

Tech Stack
Frontend: HTML, CSS, JavaScript (ES Modules)

Backend: Node.js, Express.js

Build Tool / Bundler: Vite

Installation and Setup
1. Clone the repository and navigate into the project directory:

Bash
git clone <your-repo-url>
cd <your-project-folder>
2. Install dependencies for both the server and the client:
You will need to run the installation command in both the server and client directories (depending on your exact folder structure).

Bash
# Example if using separate folders:
cd server
npm install
cd ../client
npm install
3. Run the development environment:
You will need to start both the Express server (usually running on localhost:3001 or 3000) and the Vite development server (localhost:5173).

Bash
# Start the backend server
npm start 

# In a new terminal, start the Vite frontend
npm run dev
4. Build for Production:
To generate the production-ready frontend files inside the server/public directory, run:

Bash
npm run build
