# AGENTS.md

## Project
A simple todo list web app. Users add tasks, tick them off, filter by All / Active / Done, set reminders, add notes, and clear completed ones. Tasks are saved in the browser with localStorage.

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
- Reminders can be set, show on the task, and are marked due when the time passes.
- Tasks and reminders are still there after a page refresh.
- Empty input is rejected.
- Buttons and inputs work with keyboard and have labels.

## Testing rules
Apply these after every change, and report the results before calling a task finished.

### App testing
1. **Test the new change first.** Give exact steps and the expected result.
2. **Then run the regression check.** Confirm these still work: add, complete, delete, filter (All / Active / Done), clear completed, reminders, refresh persistence.
3. **Test edge cases:** empty input, very long text, special characters like `<script>` and quotes (they must show as plain text), 50+ tasks, and a reminder set in the past.
4. **Test on a phone-sized screen and on desktop.** Nothing may scroll sideways or overlap.
5. **Check the browser console.** There must be no red errors.
6. **Test with saved data missing.** If localStorage is empty or blocked, the app must still load and work.
7. **Never say "it should work."** Say what was tested and what the result was. If something was not tested, say so.
8. **The task is finished only when the user confirms the tests pass.**

### API endpoint testing
Apply these when the app gets a backend or calls an API. Today it has none.
1. **Test every endpoint on its own** before connecting it to the page. Use a tool such as curl, Postman or Thunder Client.
2. **For each endpoint, test:**
   - the success case (correct status code, e.g. 200 or 201, and the expected response body)
   - missing or invalid input (expect 400 with a clear error message)
   - a resource that does not exist (expect 404)
   - a missing or wrong login or API key (expect 401 or 403)
   - the wrong HTTP method (expect 405)
3. **Check the response shape.** Field names and types must match what the front end expects.
4. **Handle failure in the UI.** Test with the network off and with the API returning an error. The app must show a plain message and must not lose the user's tasks.
5. **Never put secrets in the code.** API keys go in environment variables, never in `index.html` or the GitHub repo.
6. **Write down every endpoint** in an `API.md` file: method, path, input, output, and error codes. Keep it updated when an endpoint changes.
7. **Test after every change to an endpoint,** then re-run the app regression check above.

## Backlog (work top to bottom)
- [x] Add, complete and delete tasks
- [x] Filters and clear completed
- [x] Reminders
- [x] Notes on tasks
- [ ] Edit a task by double-tapping it
- [ ] Drag to reorder

## Rules for agents
- Never delete the user's saved tasks without an explicit action from the user.
- Ask before changing the file structure or the stack.
- When a task is finished, tick it in the Backlog above.
