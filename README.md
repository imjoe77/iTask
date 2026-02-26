📝 Todo List App

A fully responsive and state-driven Todo application built with React, Tailwind CSS, and Vite.
The app demonstrates modern React patterns including Hooks-based state management, immutability principles, and persistent local storage integration.

✨ Features
Add, edit, and delete tasks
Toggle task completion with conditional styling
Filter completed tasks dynamically
Persistent storage using localStorage
Responsive UI built with Tailwind CSS

Component-driven architecture
⚙️ Architecture & Implementation Details
🔹 State Management & Persistence
The application uses useState with a lazy initializer to load previously saved todos from localStorage during initial render.
A useEffect hook watches the todos state and automatically synchronizes updates to localStorage, ensuring persistence across sessions.

🔹 Adding & Editing Tasks
A unified handleAdd function manages both creation and editing modes.
When eid (edit ID) is null, a new todo object is appended.
When eid is set, the existing todo is updated using .map() to return a new immutable array.
This ensures React's state immutability principles are maintained.

🔹 Toggling & Deleting
To preserve immutability:
handleToggle uses .map() to flip the isCompleted property.
handleDelete uses .filter() to remove the selected task.
No direct mutation of state occurs.

🔹 Rendering Logic

Before rendering:
A .filter() operation determines visibility based on the “Show Finished” toggle.
Conditional class application applies a line-through style when a task is completed.
The UI remains a direct reflection of component state.

🛠 Tech Stack
React (useState, useEffect)
Tailwind CSS
Vite
React Icons

🚀 Getting Started
Prerequisites
Node.js
npm / yarn / pnpm
Installation
git clone https://github.com/imjoe77/Todo-List.git
cd Todo-List
npm install
npm run dev

Runs on: http://localhost:5173
