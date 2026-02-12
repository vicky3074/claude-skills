# /ss - Screenshot Tool

When the user types `/ss`, take a screenshot and analyze it.

## Instructions

1. Run `screencapture -i /tmp/claude-screenshot.png` to let user select area
2. If that fails, try `screencapture /tmp/claude-screenshot.png` for full screen
3. Read the screenshot file using the Read tool: `/tmp/claude-screenshot.png`
4. Describe what you see or answer any follow-up questions
5. **Delete the screenshot after reading**: Run `rm /tmp/claude-screenshot.png`

## Options

- `/ss` - Interactive selection (user picks area)
- `/ss full` - Full screen capture
- `/ss window` - Capture a specific window (use `-w` flag)

## Example Usage

User: `/ss`
Action: Take screenshot, read it, describe what's shown, delete file

User: `/ss` then "what's the error here?"
Action: Take screenshot, read it, explain the error visible, delete file
