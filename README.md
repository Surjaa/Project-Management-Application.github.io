# Project Management Application

A project board where every task shows how much attention it needs right now. Cards glow from cool teal to blazing red-orange as they become more urgent.

**Live demo:** https://surjaa.github.io/Project-Management-Application.github.io/

## Features

- **Heat engine:** each task gets a score from 0 to 100, based on priority, due date and how long it has been untouched. Done tasks are always cold.
- **Kanban board:** drag and drop between Backlog, To do, In progress, Review and Done. A blue line shows where a card will land.
- **WIP limits:** set a maximum number of cards per column. The board warns you when a column is over its limit.
- **Time Machine:** drag a slider to rewind the board and see what was open and done at any moment, with a play button to replay it.
- **Tasks and subtasks:** priorities, labels, assignees, due dates, descriptions and a checklist of subtasks.
- **Calendar and timeline views:** see tasks by due date or across time.
- **Standup writer:** builds a daily standup from the history of your cards and copies it to the clipboard.
- **Reports:** where work waits, plus overdue and hot tasks.
- **Team:** add members, assign them to tasks, and filter the board by person.
- **Command palette:** press `Ctrl + K` to create tasks, switch pages, toggle the theme or search tasks.
- **Notifications and undo:** deleting a task or moving a card shows an Undo option.
- **Light and dark themes.**
- **Backup and restore:** export all data as JSON, and import a backup later.

## Run it locally

No install or build step is needed. The app is plain HTML, CSS and JavaScript.

1. Download or clone the repository.
2. Open `index.html` in a modern browser.

Some browsers block features on `file://` pages. If something does not work, serve the folder with any static server, for example:

```bash
npx serve .
```

The page loads fonts from Google Fonts, so an internet connection is needed for the correct typefaces.

## Demo account

Click **Try the demo account** on the sign-in screen, or sign in with:

- Email: `demo@pm-app.dev`
- Password: `Demo@123`

You can also sign up with your own email, or fill your workspace with demo projects.

## Data storage

This is a browser-only demo. Accounts and tasks are stored in the browser's `localStorage` on the device you use. Nothing is sent to a server.

Passwords are salted and hashed in the browser, but there is no server-side security, so do not use a real password you care about.

## Project structure

| File | Purpose |
| --- | --- |
| `index.html` | Page shell, header and navigation |
| `styles.css` | Layout, theme colours and responsive rules |
| `store.js` | Data model, storage, the heat engine and the seed data |
| `views.js` | Renders each page: workspace, kanban, calendar, timeline, team, reports and settings |
| `auth.js` | Sign-in, sign-up, password checks and the demo account |
| `app.js` | Controller: clicks, keyboard shortcuts, drag and drop, modals and the Time Machine |

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `Ctrl + K` | Open the command palette |
| `N` | Create a task |
| `Enter` on a card | Open the card |
| `Shift + ←` / `Shift + →` | Move a focused card to the previous or next column |
| `Esc` | Close the open dialog, menu or panel |

## Browser support

Recent versions of Chrome, Edge, Firefox and Safari. The layout adapts to phones, tablets and desktops, and respects the reduced-motion setting.

## License

No license has been set. Add one before reusing the code.
