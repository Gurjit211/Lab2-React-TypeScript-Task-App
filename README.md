# Lab2-React-TypeScript-Task-App
React + TypeScript Task App


 **Overall Functionality:**
Your app allows the user to:
•	✅ See a list of tasks
•	➕ Add a new task
•	❌ Delete any task
•	🔁 Mark a task as complete or undo it
•	🎨 See everything styled using CSS
________________________________________
📂 File-by-File Functionality
________________________________________
1. App.tsx (Main App Component)
📌 Controls the entire app
Key Functions:
•	Holds the task list using useState.
•	Defines:
o	deleteTask() → removes a task by id
o	toggleTask() → toggles completed status
o	addTask() → adds a new task to the list
•	Renders:
o	The header
o	The new task input form
o	A list of <TaskItem /> components (one for each task)
________________________________________
2. TaskItem.tsx (Reusable Task Display Component)
🧩 Displays a single task row
Key Functions:
•	Receives props like id, task, completed, onDelete, onToggle
•	Displays:
o	Task text (strikethrough if completed)
o	Two buttons:
	✅ Complete/Undo (calls onToggle)
	❌ Delete (calls onDelete)
This file keeps your UI modular and clean.
________________________________________
3. App.css (App Styling)
🎨 Styles all visible UI
What it does:
•	Styles:
o	The main container box
o	Task rows
o	Input form
o	Buttons and completed tasks
•	Also includes:
o	Centering the app
o	Responsive layout
o	Sea green background (from earlier step)
You use external CSS for maintainable, scalable design.
________________________________________
4. main.tsx (App Bootstrapper)
🚀 Launches the app
What it does:
•	Connects your React app to the HTML <div id="root">
•	Looks like:
tsx
CopyEdit
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';
import './index.css'; // (optional global styles)

ReactDOM.createRoot(document.getElementById('root')!).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
You rarely change this file — it just starts the app.
________________________________________
5. index.html
📄 HTML entry point
What it does:
•	Holds <div id="root"></div> where your React app is mounted.
•	Required by Vite and React.
⚠️ Never delete this file.
________________________________________
6. (Optional) index.css
💡 Global CSS
•	Optional file for base styles like font resets.
•	Only used if imported in main.tsx.
________________________________________
✅ Summary Table
File	Purpose
App.tsx	Main logic: task list, add/delete/toggle
TaskItem.tsx	Reusable component to show a task
App.css	All styling for the app UI
main.tsx	Mounts the React app to the DOM
index.html	HTML shell with root div
index.css	Optional global styling

