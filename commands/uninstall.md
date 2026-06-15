---
description: Deactivate WaitLine — restore your settings.json from the backup
---

The user wants to deactivate WaitLine. Run:

```
node "${CLAUDE_PLUGIN_ROOT}/dist/waitline.min.js" remove-settings
```

Then confirm their `~/.claude/settings.json` was restored from the verbatim backup
(or that the two WaitLine keys were stripped if no backup existed).
