---
description: Sign in to WaitLine — pair this machine with your account so impressions attribute to your earnings
---

The user wants to sign in to WaitLine so their delivered impressions attribute to
their real account (earnings follow them across machines).

1. Run the sign-in script:

   ```
   node "${CLAUDE_PLUGIN_ROOT}/dist/waitline.min.js" signin
   ```

2. The script prints a short code and a URL. Relay them to the user and tell them
   to open the URL in their browser and approve the code. The script waits and
   polls until they approve (or the code expires after 10 minutes).

3. On success it stores a developer token in `~/.waitline/identity.json` and the
   client starts sending it on `/ad/next`. Report who they signed in as. If it
   fails (expired/timeout), tell them to run `/waitline:signin` again.
