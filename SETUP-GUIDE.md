# LinkedIn Daily Routine — Setup Guide (Pelvic Floor Edition)

Oct 15, 2026 · by Daniela Peeva

## What this routine does

Every weekday at 9:00, Claude opens your LinkedIn in your own Chrome. In about 30 to 45 minutes it does the business-development work you would otherwise skip. It finds gynecologists, clinics and pelvic floor specialists who could buy or use an Emsella chair, warms them up and keeps the conversations moving. Three days a week it also publishes a short article for doctors about pelvic floor care.

It runs as two commands back to back:

- **dailyconnect** (relationships): reads your messages, replies, sends connection requests, welcomes new connections and follows up with quiet ones.
- **dailyauthority** (visibility): leaves thoughtful comments on your target audience's posts and publishes a post on Tue, Wed and Thu.

At the end it hands you a report: who wrote, what was sent, which comments went out, and anything it held back for your approval. Daniela has run this for her own business since July 2026. This guide is her setup, rebuilt for the pelvic floor market.

## Before you start (about 20 minutes)

You need five things in place. Without all five the routine can't run.

- [ ] **A paid Claude plan** (Pro or Max) at claude.ai.
- [ ] **The Claude desktop app** (Windows or Mac), installed and signed in. The routine runs from its **Code** tab.
- [ ] **Google Chrome with the Claude in Chrome extension**, installed from the Chrome Web Store and connected to the desktop app. This is how Claude reads and clicks on LinkedIn as you.
- [ ] **LinkedIn logged in** in that same Chrome. Fill your profile first: a clear photo, a headline that says who you help (e.g. "Helping gynecology practices add pelvic floor care"), and an About section. People check your profile before they accept.
- [ ] **One project folder** on your computer, e.g. `Documents/PelvicFloor-LinkedIn`. Copy everything from the `templates` folder of this repository into it. In the Claude app, open a Code session pointed at this folder.

The computer has to be on, with the Claude app and Chrome open, at 9:00. If it isn't, the routine tells you it couldn't run and waits for you to start it by hand.

## Step 1: Build the folder and its files

The routine is only as good as the files it reads. Claude doesn't remember from one day to the next. These files are its memory, so write them once and keep them up to date. Templates for every file are in the `templates` folder. The quickest way to fill them: open each one in the Code session and ask Claude to *"interview me and fill in this file"*.

| File | What goes in it | Who updates it |
| --- | --- | --- |
| `business-profile.md` | What you sell (the device, how it works, pricing model for clinics, training, support), your country/region, your languages, what you may and may not claim | You, once, then when something changes |
| `outreach-playbook.md` | Who you target (Step 2), the tiers, what you offer each tier, your message templates, your booking link | You |
| `dailyconnect-command.md` | The 7 relationship steps (Step 4) and your daily numbers | You, once |
| `dailyauthority-command.md` | Post days, content pillars (Step 3), comment rules, your voice samples | You, once |
| `lead-tracker.csv` (open in Excel or Google Sheets) | One row per contact: name, clinic, city, role, tier, stage, last touch, next step | Claude, every run |
| `comment-log.md` | Date + person for every comment, so nobody gets two within 15 days | Claude, every run |
| `content-log.md` | Date, pillar and first line of every post, so topics rotate | Claude, on post days |
| `do-not-message.md` | People you have met or know well. Claude never messages them, only flags them to you | You |

**Your voice samples matter most.** Paste 5 to 10 real messages you've written into `dailyauthority-command.md`, with typos and all. Daniela's biggest lesson: comments that are too polished read as AI. Tell Claude to write like those samples: short, warm, a little imperfect, no long dashes, no semicolons.

## Step 2: Decide who to target

Split your targets into two pipelines and track them separately. A **buyer** is someone who could put a chair in their practice. A **referrer** is someone who sends patients to a practice that has one. Spend about 70% of daily effort on buyers.

| Tier | Who | How to find them on LinkedIn | Pipeline |
| --- | --- | --- | --- |
| 1 | Owners and medical directors of private gynecology / OB-GYN clinics and maternity hospitals | Search "gynecology clinic owner", "медицински директор АГ", filter by country; check the clinic's company page → People | Buyer |
| 1 | Urogynecologists and urologists in private practice | Search titles "urogynecologist", "уролог"; posts tagged #pelvicfloor #urogynecology | Buyer |
| 2 | Aesthetic and intimate-health clinics, women's health centres, medical spas | Company pages for "women's health", "aesthetic gynecology"; their staff lists | Buyer |
| 2 | Practice managers and clinic group operations leads | Title search "practice manager", "operations director" + clinic | Buyer |
| 3 | Pelvic floor physiotherapists, midwives, doulas, postpartum coaches | Hashtags #pelvichealth #postpartum; people who comment on Tier 1 posts | Referrer |
| 3 | Investors and franchise groups building women's health chains | "women's health" + "founder" / "investor" | Buyer |

**Warm signals** to look for before you send a request: they post or comment about pelvic floor, incontinence, postpartum recovery, women's health, or growing their practice. Someone who posts weekly beats a bigger name who never logs in. Write the list of target cities and clinic names into `outreach-playbook.md` so Claude works through it instead of guessing.

**The list runs out.** In a country like Bulgaria there may only be 80 to 150 real buyer clinics. At 7 a day that's three to five weeks. When the local names run low, widen to neighbouring countries instead of padding with weak fits.

## Step 3: Plan what you post

Post three times a week (Tue, Wed, Thu) and write for the gynecologist, not the patient. Each post makes one point in 600 to 1,300 characters. Open with a strong first line and end with a question doctors want to answer. Every other week, also publish one longer **LinkedIn article** (800 to 1,500 words) that goes deeper on one pillar. Rotate the pillars so two posts in a row never share one. Claude checks `content-log.md` for this.

| Pillar | The angle | Example first line |
| --- | --- | --- |
| P1 Practice growth | A new self-pay service line that uses rooms and staff you already have; returning patients; standing out from other clinics | "Most gynecology practices already see the patients for a whole new service line. They just don't ask the question." |
| P2 After the birth | What happens to pelvic floor care after the 6-week check, and who owns it | "The 6-week check says she's fine. Six months later she still won't jump on the trampoline with her kids." |
| P3 Do we really care? | Patients rarely bring up leaking or intimacy problems. Is it on the intake form? Does anyone ask? | "If we don't ask about bladder leaks, most women will never tell us." |
| P4 The evidence, plainly | What published studies show about pelvic floor muscle training and non-invasive options, with the source linked | "What the research actually says about non-invasive pelvic floor treatment (and what it doesn't)." |
| P5 Inside a clinic | How a practice set up the service: room, staff training, patient flow. Only with the clinic's written consent | "Here's how one clinic fit a pelvic floor service into a single room." |
| P6 Myths | "Leaking is normal after kids", "it's just ageing", "surgery is the only fix" | "'It's normal after two kids' is the most expensive sentence in women's health." |

P1 and P2 are your sales pillars, so weight them most heavily. Write P1 in a confident, ROI voice and P2 and P3 in a warm, patient-first voice.

## Step 4: Write the daily steps

These steps are already written into `templates/dailyconnect-command.md` and `templates/dailyauthority-command.md`. Claude follows them in this order every run.

**dailyconnect**

1. **Precheck.** Open LinkedIn in a new tab and confirm you're logged in. If you aren't, stop and tell the owner.
2. **Triage messages.** Read unread threads, summarise who wrote and what they want, and flag the important ones (buyers, clinic owners, anything time-sensitive).
3. **Reply.** Send routine replies directly. Draft-only for high-value or tricky contacts, and hold those for approval.
4. **Send connection requests.** Send 10 a day, about 7 to buyers and 3 to referrers, taken from the target list. Add a short personal note that mentions something real from their profile or posts. Never pitch in the note.
5. **Welcome new connections** within 24 hours. Thank them and ask one genuine question about their practice. Offer a demo or a call only when it fits, and end with your booking link.
6. **Follow up** once with contacts who went quiet 7 to 10 days ago. Never send more than two nudges in total.
7. **Update the tracker** with every request, accept and reply.

**dailyauthority**

1. **Post** on Tue, Wed and Thu only. Draft from the next pillar, run the safety check (Step 6), publish or hold for approval, and log it.
2. **Comment** on 10 posts from your target audience. Each comment is 1 to 3 sentences and adds something the post didn't say. Comment on buyers *before* sending them a request, so your name is already familiar.
3. **Spread comments out** with natural gaps. Never post them back to back.
4. **Log every comment** in `comment-log.md`. Never comment on the same person twice within 15 days.
5. **Report.** List messages, replies, requests, welcomes, comments (with the full text) and anything held for approval, plus pipeline counts.

## Step 5: Turn it into a daily scheduled task

First, run it by hand twice. In the Code session type `Run dailyconnect, then dailyauthority, in DRAFT MODE` and watch what it does. Fix the files wherever it gets something wrong. When two runs look right, paste the contents of `scheduled-task-prompt.txt` into the same session. Claude will create the scheduled task for you.

To change the time, pause it or delete it later, just ask in the Code session, e.g. *"pause my linkedin-daily-routine for a week"*.

## Step 6: Safety rules and your first two weeks

**Know the risk.** LinkedIn's user agreement doesn't allow automated activity. Accounts that look automated get warnings or temporary restrictions. The rules below keep the routine human-paced, but they can't make it risk-free. The decision to run it is yours.

**Ramp up slowly**

| Days | Requests / day | Comments / day | Publishing |
| --- | --- | --- | --- |
| 1–5 | 3–5 | 3–5 | Draft only: Claude writes everything, you approve and send |
| 6–10 | 5–7 | 5–7 | Routine replies and comments go out automatically; posts still need your approval |
| 11+ | 10 | 10 | Full routine; anything sensitive is still held for you |

**Rules that never change**

- **Medical claims.** Emsella is a medical device, so every claim must match its approved use and link a published source. Never promise results, cure rates or "guaranteed" revenue. Never invent statistics.
- **Patients.** No patient names, photos or stories without written consent. No patient data in messages.
- **People you know.** Claude never messages anyone you've met or had a real conversation with. It flags them and asks you.
- **No pitching in public.** Comments add value. No links, prices, "DM me" lines or emoji strings.
- **Stop on any warning.** If LinkedIn shows "you're doing that too often", the routine stops for the day.
- **Check the report every day** (5 minutes). Correct what you don't like, and ask Claude to update the files so the mistake doesn't happen again. That's how the routine gets better.

**Every Friday,** ask Claude for a short weekly review: requests sent and accepted, replies, demos booked, which post pillar got the most response, and how many buyer names are left on the list.
