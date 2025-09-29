# ZohoBiginCRMCallCenterPlugin

A Deluge script for Zoho Bigin that turns a custom button into a First-In-First-Out (FIFO) lead assignment tool. It lets confirmers click once to be assigned the oldest available lead to call.

## How It Works
- Detects the current logged-in user.
- Fetches all open tasks sorted by `Created_Time` (oldest first).
- If the user already has an “In Progress” task, returns that task.
- Otherwise reassigns the oldest task from a designated pool user (default “Shane Bogue”) to the current user.
- Opens the related contact automatically in a new browser tab for quick call-out.

## Benefits
- True FIFO lead distribution.
- Eliminates double-assignments.
- Works with Zoho Bigin tasks and contacts.

## Configuration
- Update `connection` to your OAuth connection name.
- Change `"Shane Bogue"` to the user holding the task queue.
- Adjust `Status` from `"In Progress"` to match your workflow if needed.

## Installation
1. Create a custom button or custom function in Zoho Bigin.
2. Paste the code from `fifo_callout_button.deluge`.
3. Save and test.

## Roadmap Ideas
- Add logging of click events to a custom module.
- Parameterize queue owner via a custom setting.
- Extend to handle multiple queues or pipelines.

## License
MIT License. See `LICENSE` for details.
