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

### Accessibility Features

- Semantic HTML landmarks (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`)
- Proper heading hierarchy (h1, h2, h3)
- Keyboard-only navigation (Tab, Enter, Escape)
- Visible focus indicators on all interactive elements
- ARIA live regions for status updates (polite and assertive)
- Screen reader compatible labels and descriptions
- Skip-to-content link
- Color contrast ratio ≥4.5:1 (WCAG AA)
- Touch targets ≥44px × 44px on mobile

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
│   ├── responsive.css        # Media queries for tablet/desktop
│   └── animations.css        # Transitions and animations
└── scripts/
    ├── main.js               # Event handlers & initialization
    ├── ui.js                 # DOM rendering & updates
    ├── state.js              # Application state management
    ├── storage.js            # localStorage persistence
    ├── validators.js         # Regex validation patterns
    ├── search.js             # Search & filtering logic
    └── utils.js              # Helper functions
```

##  Regex Validation Patterns

The application includes 5 regex patterns for comprehensive input validation:

### Pattern 1: Title Validation

```regex
/^\S(?:.*\S)?$/
```

- **Purpose:** Forbid leading/trailing spaces and collapse consecutive spaces
- **Matches:** "Valid Title", "Multi Word Title"
- **Rejects:** "  Invalid  ", "Title  with  double"

### Pattern 2: Duration Validation

```regex
/^(0|[1-9]\d*)(\.\d{1,2})?$/
```

- **Purpose:** Positive numbers with up to 2 decimal places
- **Matches:** "120", "90.5", "45.75", "0"
- **Rejects:** "-10", "abc", "12.345", "090"

### Pattern 3: Date Validation

```regex
/^\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12]\d|3[01])$/
```

- **Purpose:** YYYY-MM-DD format with valid month (01-12) and day (01-31)
- **Matches:** "2025-09-29", "2025-01-01", "2025-12-31"
- **Rejects:** "29-09-2025", "2025-13-01", "2025-09-32"

### Pattern 4: Tag Validation

```regex
/^[A-Za-z]+(?:[ -][A-Za-z]+)*$/
```

- **Purpose:** Letters, spaces, and hyphens only
- **Matches:** "Academic", "Computer Science", "Work-Related"
- **Rejects:** "Tag123", "Tag@Work", " Academic"

### Pattern 5: Duplicate Word Detection (Advanced)

```regex
/\b(\w+)\s+\1\b/i
```

- **Purpose:** Back-reference pattern to detect repeated consecutive words
- **Matches:** "finish finish", "The THE", "hello hello world"
- **Rejects:** "finish task", "assignment"
- **Feature:** Case-insensitive with back-reference capture group

##  Keyboard Navigation

| Key | Action |
|-----|--------|
| `Tab` | Navigate through form fields and buttons |
| `Shift + Tab` | Navigate backwards |
| `Enter` | Submit form, activate button |
| `Escape` | Close modal, cancel action |
| `Space` | Toggle checkbox, activate button |
| `Arrow Keys` | Navigate in lists (when focused) |

### Keyboard Flows

1. **Add Task:** Tab to "Add Task" button → Enter → Fill form (Tab between fields) → Enter to submit
2. **Search:** Tab to search input → Type regex pattern → Results update live
3. **Sort:** Tab to sort buttons → Enter to toggle sort order
4. **Settings:** Tab to setting controls → Modify values → Auto-save
5. **Delete:** Tab to delete button → Enter → Confirm dialog → Delete

##  Design System

### Color Palette

| Color | Usage | Value |
|-------|-------|-------|
| Primary | Links, buttons, active states | #0066cc |
| Background | Main page background | #f8f9fa |
| Card | Card backgrounds | #ffffff |
| Text | Body text | #1a1a1a |
| Border | Dividers, borders | #e0e0e0 |
| Success | Confirmations | #28a745 |
| Warning | Alerts | #ffc107 |
| Error | Errors | #dc3545 |

### Typography

- **Display Font:** Georgia (headings)
- **Body Font:** System fonts (Segoe UI, Roboto, sans-serif)
- **Base Size:** 14px
- **Heading Sizes:** h1: 32px, h2: 24px, h3: 20px

### Spacing

- **Base Unit:** 8px
- **Padding:** 8px, 16px, 24px, 32px
- **Margin:** 8px, 16px, 24px, 32px
- **Gap:** 16px (flex/grid)

### Animations

- **Fade In:** 300ms ease-in-out
- **Slide Up:** 300ms ease-in-out
- **Highlight:** 500ms ease-in-out
- **Bounce:** 200ms ease-out

##  Responsive Breakpoints

| Breakpoint | Width | Layout |
|-----------|-------|--------|
| Mobile | ~360px | Single column, stacked cards, hamburger nav |
| Tablet | ~768px | Two columns, flexible grid, sidebar nav |
| Desktop | ~1024px+ | Three columns, full table, fixed sidebar |

##  Testing

### Running Tests

1. Open `tests.html` in your browser
2. Tests run automatically on page load
3. View test results and interactive regex tester

### Test Coverage

-  Title validation (6 tests)
-  Duration validation (8 tests)
-  Date validation (7 tests)
-  Tag validation (6 tests)
-  Duplicate word detection (5 tests)
- **Total:** 32 automated tests

### Interactive Testing

The tests page includes an interactive regex tester where you can:

- Select any validation pattern
- Enter test input
- See real-time results with match highlighting

##  Data Model

### Task Object

```javascript
{
  id: "task_001",              // Unique identifier (auto-generated)
  title: "Finish CS101 Assignment",  // Task title (1-100 chars)
  dueDate: "2025-09-29",       // Due date (YYYY-MM-DD format)
  duration: "120",             // Duration in minutes (numeric)
  tag: "Academic",             // Task category/tag
  createdAt: "2025-09-15T10:30:00Z",  // ISO 8601 timestamp
  updatedAt: "2025-09-15T10:30:00Z"   // ISO 8601 timestamp
}
```

### Settings Object

```javascript
{
  unit: "minutes",             // Duration unit (minutes or hours)
  weeklyCap: 20,              // Weekly time cap in hours
  caseSensitiveSearch: false   // Search case sensitivity
}
```

### Default Tags

- Academic
- Personal
- Social
- Work
- Deadline
- Project

##  Getting Started

### Installation

1. Clone or download the repository
2. Open `index.html` in a modern web browser
3. No build process or dependencies required

### First Steps

1. **Dashboard:** View statistics and upcoming tasks
2. **Add Task:** Click "+ Add Task" button to create your first task
3. **Search:** Use regex patterns to find tasks (e.g., `^Academic`, `2025-09-2[5-9]`)
4. **Settings:** Customize tags, weekly cap, and unit preferences
5. **Export:** Backup your data as JSON

### Sample Data

To load sample data:

1. Go to Settings page
2. Click "Import JSON"
3. Select `seed.json` file
4. Confirm import

##  Search Examples

| Pattern | Purpose |
|---------|---------|
| `academic` | Find all Academic tasks (case-insensitive) |
| `^Academic` | Tasks starting with "Academic" |
| `2025-09-2[5-9]` | Tasks due Sep 25-29 |
| `assignment\|project` | Tasks with "assignment" or "project" |
| `\d{2}:\d{2}` | Find time tokens (HH:MM format) |
| `@tag:Academic` | Filter by tag (special command) |
| `@date:2025-09-29` | Filter by exact date (special command) |

##  Privacy & Data

- **Local Storage:** All data stored in browser's localStorage (no server)
- **No Tracking:** No analytics, cookies, or external requests
- **Export:** Download your data anytime as JSON
- **Import:** Restore data from exported JSON files
- **Clear:** Delete all data with one click (irreversible)

##  Accessibility Compliance

### WCAG 2.1 Level AA Compliance

-  Semantic HTML structure
-  Keyboard navigation (all features)
-  Focus indicators (visible and clear)
-  Color contrast (4.5:1 minimum)
-  ARIA labels and live regions
-  Skip-to-content link
-  Responsive touch targets (44px minimum)
-  Reduced motion support

### Screen Reader Support

- Tested with NVDA and JAWS
- Proper landmark navigation
- Descriptive button labels
- Status announcements
- Form error messages

##  Development

### Technologies Used

- **HTML5:** Semantic markup with proper landmarks
- **CSS3:** Mobile-first responsive design with media queries
- **JavaScript (ES6+):** Modular architecture with IIFE pattern
- **localStorage:** Client-side data persistence

### Module Architecture

- `utils.js` - Utility functions (formatting, DOM, etc.)
- `validators.js` - Regex patterns and validation logic
- `storage.js` - localStorage operations
- `state.js` - Application state management
- `search.js` - Search and filtering logic
- `ui.js` - DOM rendering and updates
- `main.js` - Event handlers and initialization

### Code Style

- ES6 modules with IIFE pattern
- Descriptive variable and function names
- Comprehensive comments and JSDoc
- Error handling with try/catch
- Debounced/throttled event handlers

##  Milestones

| Milestone | Status | Description |
|-----------|--------|-------------|
| M1 |  Complete | Specification & wireframes |
| M2 |  Complete | Semantic HTML & base CSS |
| M3 |  Complete | Forms & regex validation |
| M4 |  Complete | Rendering, sorting, search |
| M5 |  Complete | Stats dashboard & cap logic |
| M6 |  Complete | Persistence & import/export |
| M7 |  Complete | Polish, a11y, README, seed data |

##  License

This project is created for educational purposes as part of a web development assignment.

##  Acknowledgments

- Regex patterns inspired by common validation best practices
- Accessibility guidelines based on WCAG 2.1 standards
- Design principles from modern web applications
- Semantic HTML structure following HTML5 standards

##  Contact

For questions or feedback about this project:

- **GitHub:** [My GitHub Profile](https://github.com/JamesKanneh)
- **Email:** <j.kannehii@alustudent.com>

---

**Last Updated:** February 2025  
**Version:** 1.0.0
