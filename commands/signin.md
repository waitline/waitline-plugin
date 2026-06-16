---
description: Sign in to WaitLine — pair this machine with your account so impressions attribute to your earnings
---

The user wants to sign in to WaitLine so their delivered impressions attribute to
their real account (earnings follow them across machines).

1. Run:

   ```
   node "${CLAUDE_PLUGIN_ROOT}/dist/waitline.min.js" signin
   ```

2. It prints a single sign-in URL (a stable link for this machine). Show that URL
   to the user and tell them to open it and sign in with Google. That's it — there
   is no code to enter and nothing to wait for here; don't poll or re-run anything.

The server merges this machine's earnings (before and after) into their account
once they sign in at that link.
