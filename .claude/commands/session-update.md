Update the current development session by:

1. Checking if `.claude/sessions/.current-session` exists, to find the current active session
2. If there is no active session, inform the user to start one with `/project:session-start`
3. If a session exists, append the work to the session file with:
    - Current timestamp
    - The update: $ARGUMENTS (or if no arguments, summarize recent activities)
    - Git status summary:
        * Files added/modified/deleted (from `git status --porcelain`)
        * Current branch and last commit
    - Todo list status:
        * Number of completed/in-progress/pending tasks
        * List any newly completed tasks
    - Any issues encountered
    - Solutions implemented
    - Code changes made

Keep updates concise but comprehensive for future reference.
Use the Europe/Bucharest timezone (UTC +3).

Example format:
```
### Update - 2025-06-16 12:15 PM

**Summary**: Implemented user authentication

**Git Changes**:
- Modified: src/middleware.ts, lib/auth.ts
- Added: src/app/[locale]/(auth)/sign-in/page.tsx
- Current branch: main (commit: abc123)

**Todo Progress**: 3 completed, 1 in progress, 2 pending
- ✓ Completed: Set up the auth middleware
- ✓ Completed: Create the sign-in and sign-out pages
- ✓ Completed: Add logout functionality

**Details**: [the user's update or automatic summary]
```