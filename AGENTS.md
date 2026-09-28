# AGENTS.md

## Project
A simple todo list web app. Users add tasks, tick them off, filter by All / Active / Done, and clear completed ones. Tasks are saved in the browser with localStorage.

## Stack and constraints
- Plain HTML, CSS and JavaScript in a single `index.html`. No build step, no frameworks.
- Must work when hosted as a static site (GitHub Pages).
- Must work on a phone screen first, then desktop.

## How to work
1. Before changing code, state the plan in 3 bullets or fewer.
2. Make one change at a time. Keep each change small enough to review.
3. After each change, say how to test it (what to click, what should happen).
4. Do not add libraries or new files unless asked.
5. Keep the code readable: short functions, clear names, comments only where the reason is not obvious.

## Definition of done
- Adding, completing, deleting, filtering and clearing tasks all work.
- Tasks are still there after a page refresh.
- Empty input is rejected.
- Buttons and inputs work with keyboard and have labels.

## Backlog (work top to bottom)
- [x] Add, complete and delete tasks
- [x] Filters and clear completed
- [ ] Edit a task by double-tapping it
- [ ] Due dates
- [ ] Drag to reorder

## Rules for agents
- Never delete the user's saved tasks without an explicit action from the user.
- Ask before changing the file structure or the stack.
- When a task is finished, tick it in the Backlog above.
