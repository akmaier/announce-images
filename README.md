# announce-images

Image-hosting repo for the AI Morning News dashboard `/announce` flow.

When the operator fires an `/announce` from the dashboard, the local
clone of this repo on the publishing host copies the uploaded image
into `announce/<YYYY>/<MM>/<job-id>-<filename>`, commits, and pushes
via SSH. The social platforms (Buffer X + Facebook, Threads) then
fetch the image as a `raw.githubusercontent.com` URL.

**Why this exists (in three lines):** catbox.moe blocks the FAU exit IP;
litterbox is now caught by FAU's phishing-warning URL filter; GitHub
raw content URLs are universally accessible and never blocked.

This repo is intentionally minimal — no application code, no review
process, just append-only image uploads. Cleanup of old uploads is
manual.

License: image uploads are operator-supplied; ownership and licensing
follow whatever the operator's source material requires.
