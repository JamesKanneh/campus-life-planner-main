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

## File structure (short)

```
campus-life-planner/
├── index.html
├── tests.html
├── seed.json
├── README.md
├── M1_SPECIFICATION.md
├── styles/
└── scripts/
```

## Run tests

Open `tests.html` in your browser. The tests run automatically and include a small interactive tester for input patterns.

## Privacy

All data stays on your computer in the browser (localStorage). Nothing is sent to a server.

## Need help or want to share feedback

- GitHub: https://github.com/JamesKanneh
- Email: j.kannehii@alustudent.com
- Demo Video: https://youtu.be/WocPj49Cb0Q

Last updated: February 2026
