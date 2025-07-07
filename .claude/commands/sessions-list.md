List all the previous development sessions, by:

1. Checking if the `.claude/sessions/` directory exists
2. Listing all the `.md` files (excluding hidden files and `.current-session`)
3. For each session file:
    - Show the filename
    - Extract and show the session title
    - Show the date/time
    - Show the first three lines of the overview, if available
4. If `.claude/sessions/.current-session` exists, highlight which session is currently active
5. Sort by the most recent session first

Present in a clean, readable format. Use the Europe/Bucharest timezone (UTC +3).