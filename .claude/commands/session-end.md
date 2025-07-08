End the current development session by:

1. Check `.claude/sessions/.current-session` for the active session
2. If there is no active session, inform the user there's no session to end
3. If a session exists, append a comprehensive description including:
    - The session duration
    - The session summary — a brief summary, in at most three lines
    - Key accomplishments
    - All features implemented
    - Problems encountered and their solutions
    - Breaking changes or important findings
    - Dependencies added/removed
    - Configuration changes
    - Lessons learned
    - What wasn't completed
    - Git summary:
        * Total files changed (added/modified/deleted)
        * List all the changed files, with the type of change
        * Number of commits made (if any)
        * Final git status
    - Todo summary:
        * Total tasks completed/remaining
        * List all completed tasks
        * List any incomplete tasks with their status and the reason why they were not completed

    The description must be thorough enough that another developer (or AI) can understand everything that was changed and added, without reading the entire session.
    
4. Empty the `.claude/sessions/.current-session` file (don't remove it, just clear its contents)
5. Inform the user the session has been documented
6. Generate a Git commit of the performed changes, use the instructions from the `.claude/commands/generate-commit.md` document
