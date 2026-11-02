# Bio Writer

Your profile bio written for every platform at the right length, from what you actually do and one real thing you've done.

A bio has two seconds to do one job. **Make the right person stay and the wrong person leave.** Most bios fail by trying to please both, which is how you end up "passionate about helping businesses grow." This one says what you do, who it's for, and one specific proof point — nothing else.

## Install

1. Copy the `bio-writer` folder into your Claude Code skills directory:
   ```bash
   cp -r bio-writer ~/.claude/skills/
   ```
2. Restart Claude Code (or start a new session).
3. Invoke it by typing `/bio-writer`.

## How to use

Run `/personalize` once first so it has your niche, offer, and audience. Then type `/bio-writer`.

It pulls what it can from your profile, asks for anything missing, and checks that your angle is sharp enough to be worth writing — if it isn't, it'll tell you to run `/positioning-filter` first instead of writing you a polished bad bio. You get five versions with character counts: Instagram (150), LinkedIn headline (220) plus a full About section, X (160), and a one-liner for your link-in-bio or email signature. Saved to `~/brand/bio.md`.
