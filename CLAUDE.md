# Book Launch Playbook

Governed by the [TheShaneBrain Constitution](https://github.com/thebardchat/constitution).

## What This Repo Is

An open-source playbook for launching a self-published book with zero budget, zero industry connections, and zero excuses. Built for indie authors, AI-assisted creators, and anyone who made something in a closet and needs to get it in front of people.

This playbook was built to launch **"You Probably Think This Book Is About You"** — a noir detective book co-written with Claude AI on a Raspberry Pi 5 in Hazel Green, Alabama. Everything here is real. Everything was tested. The results are documented.

## Sacred Rules

### Content
1. **No manuscript content.** This is the launch playbook, not the book. No excerpts, no chapters, no scenes, no tracks.
2. **No spoilers.** The book has structural tricks and a hidden finale. Don't reveal them. Sell the mystery, not the answer.
3. **Templates are generic.** Every template in this repo should work for ANY self-published book, not just this one. Shane's book is the case study. The playbook is universal.

### Tone
1. **Honest.** No fake marketing speak. No "unlock your potential." Real numbers, real tactics, real results.
2. **Accessible.** Written for the person who has never marketed anything. If your mom couldn't follow it, rewrite it.
3. **Scrappy.** This is a zero-budget playbook. Every tactic assumes you have a phone, an internet connection, and nothing else. No ad spend. No PR firm. No bookstagrammer contacts.

### Structure
1. **One file per topic.** Campaign templates in one file. Schedule in another. Platform guides separate. Don't merge.
2. **Copy-paste ready.** Every post template should be immediately usable. No placeholders like [INSERT TITLE]. Use real examples with clear instructions on how to adapt.
3. **Mobile-first.** The author is posting from their phone between dispatch calls. Everything must be scannable, scrollable, and copyable on a 6-inch screen.

## Repo Structure

```
book-launch-playbook/
  CLAUDE.md              — this file (the rules)
  README.md              — the pitch, the story, the entry point
  campaign/
    TEMPLATES.md         — 10+ ready-to-post social media templates
    SCHEDULE.md          — 2-week launch calendar + evergreen rotation
    DISCORD.md           — Discord-specific announcements and drops
    REDDIT.md            — subreddit targets, rules, post formats
    HASHTAGS.md          — platform-specific hashtag blocks
  guides/
    ZERO-BUDGET.md       — marketing with $0 and a phone
    AI-ANGLE.md          — how to talk about AI co-writing without scaring people
    PLATFORM-GUIDE.md    — what works where (Facebook vs Twitter vs Reddit vs Discord)
    REPLY-TEMPLATES.md   — responses for common questions and DMs
    AMAZON-KDP.md        — lessons from publishing on KDP
  case-study/
    TIMELINE.md          — how this book went from voice memo to Amazon
    NUMBERS.md           — real metrics (updated as they come in)
    MISTAKES.md          — what we got wrong and what we'd do differently
```

## Who This Is For

- Indie authors who just hit "publish" and don't know what comes next
- AI-assisted creators who need to explain the collaboration without apologizing for it
- Self-published authors with no marketing budget
- Anyone who built something real and needs the world to find it
- The ~800 million people Big Tech is about to leave behind who also have stories to tell

## The Philosophy

Marketing is not lying. Marketing is telling the truth loud enough for the right people to hear it.

This book was written by a dump truck dispatcher on the drive home from work. That's not a gimmick. That's the story. The marketing IS the story. The story IS the marketing. The person who would love this book is the person who hears "a dispatcher in Alabama wrote a noir detective book on a Raspberry Pi with an AI" and says *tell me more*.

Find that person. Tell them.

That's the whole playbook.

## Claude Code Rules
- Commit and push directly to `main`
- Never commit manuscript content or book text
- Keep templates universal — this playbook should work for any indie book
- Update case-study/NUMBERS.md when real metrics come in


## Networking / Deployment
- When working with Tailscale Funnel, remember it strips URL path prefixes. Always use hardcoded base paths rather than server-side form action prefixing for routing.

## Creative Writing
- Never overwrite or rewrite the user's creative voice, prose style, or intentional structural choices (e.g., missing notes, dialogue rhythm). Ask before making stylistic changes to creative writing files.

## General Workflow Rules
- Before setting up repos, SSH keys, or services, check what's already configured on the current machine. Run `ls ~/.ssh/`, `git remote -v`, `tailscale status`, etc. before assuming fresh setup is needed.
- Let's focus on one thing at a time. Don't suggest other improvements until the current goal is fully verified working.
- Before applying changes to all files, show the result on one file first so Shane can verify the approach.

## Git
- For git conflicts, always verify --theirs vs --ours semantics before applying. State which version you're keeping and why before running the command.

## Raspberry Pi Environment
- This user runs services on Raspberry Pi. Be aware: Python 3.13 removed the `cgi` module, Piper TTS needs careful noise_scale tuning to avoid clipping, and aplay conflicts with PipeWire. Prefer `pw-play` or `paplay` for audio playback.
