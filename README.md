# Campus Life Planner

A fully accessible, responsive task and event management application for college and university students. Built with vanilla HTML, CSS, and JavaScript—no frameworks required.

##  Project Overview

**Campus Life Planner** helps students organize their academic work, events, and personal tasks with powerful search, filtering, and time management features. All data is stored locally in your browser using localStorage, ensuring privacy and offline functionality.

**Theme:** Campus Life Planner (tasks/events with title, dueDate, duration, tag)

## Deployed URL 
[https://jameskanneh.github.io/campus-life-planner-main/](https://jameskanneh.github.io/campus-life-planner-main/)

##  Features

### Core Features

-  **Task Management:** Create, read, update, and delete tasks with title, due date, duration, and tags
-  **Dashboard:** Real-time statistics including total tasks, upcoming tasks, total hours, and tag distribution
-  **Weekly Cap/Target:** Set a weekly time commitment goal with visual progress tracking and ARIA live alerts
-  **Advanced Search:** Regex-based search with case-insensitive toggle and match highlighting
-  **Sorting:** Sort tasks by title, due date, or duration in ascending/descending order
-  **Responsive Design:** Mobile-first design with 3 breakpoints (360px, 768px, 1024px)
-  **Local Storage:** Automatic saving of all tasks and settings to browser localStorage
-  **Import/Export:** JSON import/export with full data validation
-  **Settings:** Customize unit conversion, weekly cap, and manage tags
-  **Accessibility:** Full keyboard navigation, ARIA live regions, semantic HTML, high contrast



##  File Structure

```
campus-life-planner/
├── index.html                 # Main application page
├── tests.html                 # Regex validation tests page
├── seed.json                  # Sample data (12 diverse records)
├── README.md                  # This file
├── M1_SPECIFICATION.md         # Detailed specification & wireframes
├── styles/
│   ├── main.css              # Main styles (mobile-first)
# Campus Life Planner

A small, easy-to-use web app that helps you keep track of tasks and events for school.

It's built with plain HTML, CSS, and JavaScript and stores your data in the browser. No installation or account is needed.

## Quick start

1. Open `index.html` in your browser (or `client/index.html` if you're working in the `client` folder).
2. Click the "+ Add Task" button to create your first task.
3. Fill in Title, Due Date (YYYY-MM-DD), Duration (minutes), and Tag, then save.

That's it — your data is saved in your browser automatically.

## Main features (short)

- Add, edit, and delete tasks (title, due date, duration, tag).
- Dashboard shows counts and upcoming tasks.
- Search and sort tasks (you can use simple words or regular expressions if you want).
- Import/Export your tasks as JSON (`seed.json` can be used as sample data).
- Everything is stored locally (no server, no account).

## Simple example

- Title: Finish math homework
- Due Date: 2026-02-25
- Duration: 60
- Tag: Academic

Click Save and the task will appear in your list.

## Files you'll care about

- `index.html` — open this to run the app.
- `tests.html` — open to try validation tests and the regex tester.
- `seed.json` — sample data you can import from Settings.
- `styles/` and `scripts/` — where the app code and styles live.

## Run tests

Open `tests.html` in your browser. The tests run automatically and include a small interactive tester for input patterns.

## Privacy

All data stays on your computer in the browser (localStorage). Nothing is sent to a server.

## Need help or want to share feedback

- GitHub: https://github.com/JamesKanneh
- Demo Video: 
Last updated: February 2026
