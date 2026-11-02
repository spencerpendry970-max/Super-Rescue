---
name: bio-writer
description: Get your profile bio written for every platform at the right length — Instagram (150 characters), LinkedIn headline plus About section, X (160 characters), and a one-liner for your link-in-bio or email signature. Says what you do, who it's for, and one real proof point, with no "passionate about" anything. Use when the user says "write my bio", "fix my Instagram bio", "LinkedIn headline", "what should my bio say", "my profile is bad", "write my About section", "bio for my profile", "how do I describe myself", or "/bio-writer".
---

# Bio Writer — make the right person stay and the wrong person leave

Your bio has about two seconds to do one job: tell the right person they're in the right place, and tell everyone else to keep scrolling. Most bios fail by trying to please both. This skill writes a bio for each platform at the correct length and register, built from what you actually do and one real thing you've done.

## Personalization
This skill works in *your* brand voice. Before running, load the brand profile at `~/.claude/brand-profile.md`.
- If it doesn't exist, run the **personalize** skill first (or just tell me your name, niche, offer, and audience — I'll create it).
- If a field this skill needs is blank, I'll ask one or two quick questions and save the answers back to the profile so you only answer once.
- Never invent facts or results about the user — use only what's in the profile, or ask.

## Steps

### 1. Get the three ingredients
Every good bio is built from three things. Pull them from the profile first, and only ask for what's missing.

1. **What you do, in plain words.** Not your title. The thing that happens because of you. "I build simple websites for local trades" beats "Digital Solutions Consultant."
2. **Who it's for.** Specific enough that someone reads it and thinks "that's me" or "that's not me." Both outcomes are wins.
3. **One proof point.** A real number, a real result, a real credential, or a real thing they made. One. Not three.

If they have no proof point yet, that's fine and common. Use a **current build** instead: "Building [thing] in public." That is a legitimate proof point for someone early — it shows motion. Never invent a number, a client count, or a revenue figure.

### 2. Run the mush check
Before writing anything, test their answer to "what do you do."

It's too mushy if:
- It could describe fifty other people in their niche.
- It uses a category name instead of an outcome ("content creator", "entrepreneur", "AI enthusiast").
- Their audience is "everyone", "businesses", or "people who want to grow."

If two or more of those are true, stop writing bios. Tell them plainly: the bio isn't the problem, the angle is. Hand off to **positioning-filter**, then come back. A well-written bio for a mushy angle is still a bad bio.

### 3. Write the Instagram bio — 150 characters
Instagram is scanned, not read. Write it in short lines, not a sentence.

- 3 lines maximum, each one a fragment.
- Line 1: what you do, for whom.
- Line 2: the proof point.
- Line 3: what to do next (only if there's a link, and keep it to a few words).
- No hashtags. No emoji. Count the characters and state the count.

Shape to aim for:
> Simple websites for local trades
> 40+ built, none took more than a week
> Free quote below

### 4. Write the LinkedIn headline (220 characters) and the About section
**Headline** — this shows up everywhere on LinkedIn, including in comments and search. It is the highest-value 220 characters they own.
- Lead with the outcome they create, not the job title.
- Include who it's for.
- One proof point if it fits.
- Pipe separators are fine and read cleanly on LinkedIn.
- Never "Helping businesses achieve their goals." State the actual thing.

**About section** — 4 to 6 short paragraphs, first person, first 2 lines visible before the "see more" cut so front-load the point.
Structure it like this:
1. The problem their audience has, in the audience's own words.
2. What they do about it, plainly.
3. One specific story or proof — how they got here, or a result.
4. Who this is for, and who it isn't for. Naming who it isn't for is what makes the right person trust it.
5. One line on what to do next.

Register note: LinkedIn rewards plain and specific far more than people expect. Do not switch into corporate voice. No "seasoned professional", no "proven track record", no "results-driven".

### 5. Write the X bio — 160 characters
X is the tightest and the most personality-driven.
- One line, or two fragments separated by a period.
- Sharpest version of what they do. Cut every qualifying word.
- A single specific detail earns more follows here than a credential does.
- No links (the profile has a link field), no hashtags.

Shape:
> I build small tools that solve one annoying problem. 11 shipped. Currently: a rent checker.

### 6. Write the one-liner
One sentence, under 15 words, that works in a link-in-bio header, an email signature, or when someone asks what they do at a party.

This is the compressed version of everything above. It should be sayable out loud without embarrassment. Test it: read it aloud. If it sounds like a LinkedIn ad, rewrite it shorter and more concrete.

### 7. Run the final checks on all five
- **Character counts:** state the count next to each one. Over the limit means rewrite, not trim mid-word.
- **The stranger test:** could someone read this and know whether to keep following? If not, it's too vague.
- **The repel test:** does anything here tell the wrong person to leave? If nothing does, it's too safe.
- **Banned:** "passionate about", "helping people", "on a mission to", "obsessed with", "lover of", unlock, leverage, elevate, journey, empower, "wearer of many hats". No emoji unless the user asks.
- **No invented facts.** Every number must be one they gave you.

## Output — save it
Write the result to `~/brand/bio.md` (create `~/brand/` if needed).

The file contains all five versions in copy-ready blocks with character counts: Instagram, LinkedIn headline, LinkedIn About, X, and the one-liner. Add a short note listing the three ingredients used, so they can rewrite these themselves later when the proof point changes.

Tell the user the path, then the one next action: update the LinkedIn headline first — it's the one that shows up in the most places.

## Example (input → output)
**Input:** "I help people who work full-time jobs build small apps at night using AI. I've done it myself, took me about 6 months, and I've helped 12 people do it now."

**Output (saved to `~/brand/bio.md`):**

**Instagram (139 chars):**
> Small apps, built at night, around a 9-5
> I did it in 6 months. 12 people after me.
> Start here ↓

**LinkedIn headline (118 chars):**
> I help people with full-time jobs build their first real app at night | 12 people shipped so far | No coding required

**X (128 chars):**
> Building software at night around a day job. Did it in 6 months, then taught 12 other people to. You do not need to learn to code.

**One-liner (11 words):**
> I teach people with day jobs to build real apps at night.

## Notes / edge cases
- The failure mode this prevents: a bio that lists what someone IS instead of what someone GETS. Nobody follows a job title.
- If they're brand new with no results, use the current build as the proof point. "Building X in public, day 14" is honest and it works. Never fake a number to fill the slot.
- If they do three unrelated things, the bio must pick one. Say so directly — a bio that hedges across three lanes converts on none of them.
- If the angle is still mushy after step 2, hand off to **positioning-filter** before writing anything.
- Bios go stale. Tell them to rewrite the proof point every time they finish something worth naming.
