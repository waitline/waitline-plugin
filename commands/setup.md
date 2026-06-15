---
description: Activate WaitLine — write the sponsored statusLine + spinnerVerbs into your settings.json (with your consent)
---

The user wants to activate WaitLine. Do this:

1. Tell the user exactly what will be written to `~/.claude/settings.json`:
   - `statusLine` → runs the WaitLine status-line renderer (a single clickable "ad·" line)
   - `spinnerVerbs` → replaces the thinking verb with "Sponsored" (takes effect next session)
   A verbatim backup of their current settings.json is saved to `~/.waitline/settings.backup.json`.

2. Run the activation script:

   ```
   node "${CLAUDE_PLUGIN_ROOT}/dist/waitline.min.js" apply-settings "${CLAUDE_PLUGIN_ROOT}"
   ```

3. Report the result. Remind them: the status line appears immediately; the spinner
   verb changes on the next Claude Code session. They can deactivate anytime with
   `/waitline:uninstall`.
