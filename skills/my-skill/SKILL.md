---
name: my-skill
description: Explains how error handling should be implemented in microflows, including logging and rollback behavior. Apply this whenever creating or editing a microflow that performs a database commit, external call, or integration.
---

# Microflow Error Handling Standard

When building or editing a microflow that performs a database commit, external call, or integration:

- Add an error handler to catch exceptions rather than letting them propagate unhandled.
- On error, log a message including the microflow's name and the error text, using the Log Message activity.
- Roll back any uncommitted changes before showing an error message to the user.
- Show the user a friendly, non-technical message — never expose a raw stack trace or exception text.
- For microflows triggered by a scheduled event, log the error instead of showing a message, since there's no user present to see it.
