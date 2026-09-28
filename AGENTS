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
- The checks in Testing below pass, including any API endpoint you added or changed.

## Testing
No test framework, no new files. Test by hand in the browser, on a phone-width screen (about 375px) first, then desktop. Run the checks below after every change and report what you clicked and what happened.

### App checks
1. Add a task: it appears at the top and the counter updates.
2. Submit empty and whitespace-only input: nothing is added.
3. Tick and untick a task: the strike-through and counter update.
4. Delete a task: only that task disappears.
5. Filters: All, Active and Done each show the right tasks, and the empty message shows when none match.
6. Clear completed: removes done tasks only.
7. Refresh the page: all tasks and their done state are still there.
8. Keyboard only: Tab reaches every control, Enter submits, Space ticks, focus is visible.
9. Check the browser console: no errors during any of the above.

### API endpoints
The app has no backend today, so there are no endpoints to test. Adding one changes the stack, so ask first (see Rules). If one is approved, list it in the table below and test every row before calling the work done.

| Method | Path | Success | Errors to test |
|--------|------|---------|----------------|
| GET | /api/todos | 200 + JSON array | 500 |
| POST | /api/todos | 201 + created task | 400 empty `text` |
| PATCH | /api/todos/:id | 200 + updated task | 400 bad body, 404 unknown id |
| DELETE | /api/todos/:id | 204 | 404 unknown id |

The rows above are an example shape. Replace them with the real endpoints.

For each endpoint:
- Test with `curl` before wiring it to the UI, and paste the command and response in your report.
  `curl -i -X POST /api/todos -H "Content-Type: application/json" -d '{"text":"test"}'`
- Check the happy path, the status code, and that the response is valid JSON in the documented shape.
- Check each error case in the table returns the right status and a JSON error message, not an HTML page or a stack trace.
- Check the round trip: create, then GET shows it; delete, then GET no longer shows it.
- Check the UI when the request fails or the network is offline: show a clear error and keep the tasks already saved in the browser. Never drop saved tasks because a request failed.
- Check the endpoint works from the hosted origin (CORS), since the site is static.

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
