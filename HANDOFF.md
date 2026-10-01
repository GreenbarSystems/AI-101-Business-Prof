# AI Business 101 Professor: project handoff (one source of truth)

Merged from two earlier handoffs. Where they conflicted, the owner's decisions below win. Lesson scripts live in `scripts/`.

## The channel
- **Name:** AI Business 101 Professor (YouTube long-form and Shorts, TikTok). Playlist: "Accounting 101 in Plain English".
- **Owner:** Ryan. 25+ years in accounting and finance (senior accountant through VP of Finance), now working in AI for accounting. Profile says **former CPA**: never present as a current CPA, and avoid offering tax, audit or attest services unless licensed.
- **Topics:** accounting basics, AI in accounting, accounting standards, business, FP&A.
- **Audience:** small business owners first, finance and accounting pros second (AI in Excel).
- **Brand pattern for AI videos:** "AI drafts, you approve." AI produces the entry; the human checks it against an accounting rule. Equal debits and credits do not prove an entry is right; unequal ones prove it is wrong.

## How videos get made (owner's time: reading scripts only)
1. Claude writes the script and scene plan. Facts are checked against free sources such as OpenStax *Principles of Accounting*, never made up.
2. Ryan reads the script in one take on his phone and sends the audio.
3. Claude handles noise cleanup, caption timing, chalkboard animation (Remotion), quizzes, render, QC and private upload.
- **Voiceover only.** No on-camera work. His photo appears as a picture in a circle or badge, never video of him. He does not time, screen-record or appear on camera.
- Render only when asked or at a milestone.

## Formats (decided)
- **Long-form lessons:** 4–6 minutes, written in clip-ready sections (below).
- **Shorts:** **20–25 seconds**, cut from lesson sections, about 55–60 spoken words each.

## Clip-ready lesson rule (so clips make good Shorts)
Long-form cut-ups often make weak Shorts because mid-lesson sections have no hook or payoff. Every lesson is written to avoid that:
1. **One idea per section.** Each section has a heading in the script.
2. **Stands alone.** The first line works with no earlier context (no "this", "as we saw", "like I said").
3. **Has its own payoff.** The last line lands the point.
4. **Clip candidates are 55–60 spoken words or fewer.** Longer sections get a trimmed cut point in the clip map.
5. **Every lesson file ends with a clip map:** the section, the on-screen banner hook, and cut notes. The banner is text over the first 2 seconds, so the hook never depends on the recording.
6. **Quizzes are clips by design:** question, 5-second countdown, answer.
7. **One reusable outro line,** recorded once and reused on every Short, plus an outro card.
- Sections that are definitions only, or that need earlier context (the cascade, recaps), are marked "not clip material".
- **Open test:** no data shows clips beat native Shorts. Cut a few, compare views, average view duration and subscribers gained against a native Short on the same topic, and keep what wins.

## Tone
Candid practitioner, not textbook. Short personal stories (his manager drawing T's on the whiteboard). Contrarian titles. Everyday examples (the $1 bottle of water, the house and mortgage, the water stand). One memory hook per idea.

## Visual design (locked)
- One chalkboard for the whole video: green board, wood frame, brown surround, slow push-in, eraser wipes between sections.
- Fonts (from @fontsource): Cabin Sketch for titles and big words, Kalam for everything else.
- Colors: chalk white `#f3f1e7`, **yellow `#ffe27a` (credits, emphasis)**, **blue `#9fd4ff` (debits)**, pink `#ff9b8a` (warnings).
- Chalk lines reveal left to right with a chalk stick riding the edge; T-accounts, circles and underlines draw themselves.
- Quizzes: "Quick quiz!" board, 5-second chalk countdown (5 to 1), answer circled.
- Photo: yellow-ringed circle on the intro, then a top-left badge with the lesson name. The cutout (rembg `isnet-general-use`, chalkboard-green background) is not in git; Ryan re-attaches it.
- Captions: sans-serif bar at the bottom (Kalam undecided).
- Code lives in the old repo `animation/src/` (`chalk.tsx` holds Board, Chalk, Stroke, Eraser). Needs Remotion 4 and React 19; versions vs. mythic-lore-factory are **unchecked**. Media files are not committed.

## Audio
- ffmpeg cleanup: `highpass=f=80,arnndn=m=sh.rnnn:mix=0.9,afftdn=nf=-30,loudnorm=I=-16:TP=-1.5:LRA=11` (RNNoise model `sh.rnnn` from GregorR/rnnoise-models). The earlier "8 dB" improvement is **unverified**.
- Recording: soft room (closet or bedroom), phone 6–8 inches from the mouth and slightly off to the side, fans off, notifications silenced, 2 seconds of silence at the start and end.
- Local transcription: sherpa-onnx with Whisper small.en (Hugging Face is blocked).

## Launch plan
Launch lessons 1–3 together plus a channel trailer. Every lesson stands alone with a 10-second recap; in-lesson intros about 15 seconds. **Lesson order is fixed.**

| # | Lesson | Status |
|---|---|---|
| 1 | What the hell is A = L + E? | Script and clip map in `scripts/lesson-01-a-equals-l-plus-e.md` |
| 2 | Why debits and credits suck (and how they click) | Script and clip map in `scripts/lesson-02-debits-and-credits.md` |
| 3 | Your first journal entries: buy, sell, pay | To write |
| 4 | Profit vs cash: why profitable businesses go broke | To write |
| 5 | The 3 financial statements in 5 minutes | To write |
| 6 | Accrual vs cash accounting | To write |

After that, an AI track (below). Check YouTube's advertiser-friendly guidelines on "hell" in Lesson 1's title before publishing; fallback title "What Is A = L + E? (The Equation Every Business Runs On)".

## Accuracy rules
- Debit = left, credit = right. Neither means good or bad.
- Assets and expenses increase with a debit. Liabilities, equity and revenue increase with a credit. The opposite side decreases them.
- Dividends and owner withdrawals are **not** taught in these lessons. Retained earnings is described as "the profit the business keeps."
- Buying inventory: Dr Inventory / Cr Accounts Payable. Selling it: Dr COGS / Cr Inventory, plus Dr Cash / Cr Revenue.
- Accrual example: Dr Wages Expense / Cr Accrued Wages, then Dr Accrued Wages / Cr Cash when paid.
- Define every term before using it: revenue, expenses, net income, Cost of Goods Sold.

## AI track (video ideas, each with the "AI drafts, you approve" check)
- Can Claude do my bookkeeping? (show the prompt; what it got wrong)
- AI bookkeeping: what to trust and what to check
- AI month-end close: what to hand off and what to check
- Ask AI to build a starter balance sheet, then check A = L + E
- AI sorts transactions into categories; you review
- AI writes spreadsheet formulas; you test them on known numbers
- Why profit isn't cash (AI summary checked against the bank balance)
- What your CPA checks that you don't

## Research (directional only)
- vidIQ is connected only to Ryan's Mythic Lore Labs channel, so there is no analytics for this channel. All figures are vidIQ keyword estimates, not proof.
- Keywords (searches/month, competition 0–100): small business bookkeeping 21,065 (14.7); ai accounting 17,775 (31.4, up 164%); ai bookkeeping 13,876 (27.1, down 18%); how to make income statement 6,733 (15.1); balance sheet vs income statement vs cash flow 5,395 (17.8); how can claude do my bookkeeping 5,193 (28.5); why debits and credits still confuse you 4,392 (5.3). Broad "accounting basics for beginners" is falling and crowded.
- Hook patterns seen in five Shorts (small sample): a claim or correction in the first second; debunk, then the real rule with a hard number; follow one dollar through the process; a new visual every 2–4 seconds; word-by-word captions; a follow line at the end. One of the five (Eric Tech) was a paid partnership, so it is not a benchmark.
- Avoid copyrighted film clips; use generic, no-name examples.
- YouTube search demand is not buying intent.

## Consulting (secondary goal)
- Position as "AI applied to the accounting close and finance workflows, from someone who has run them," not "AI consultant". First offer: one fixed-scope paid review of a company's close process. Do not guess a price; test it.
- Build proof first: two or three end-to-end workflows written up with before/after time and error checks, using anonymized or own data only.
- Put a free checklist or short intake form in the description and a pinned comment. Reply helpfully in public to comments; do not scrape contacts.
- Start with the warm network.
- Before taking money: check any employer agreement for outside-work limits, get an engagement letter and an entity, ask about liability coverage, and never put client data into a public AI tool without written agreement.

## Production practices (from the first handoff)
1. **Stills gate:** render about 4 key frames before the full render.
2. **Phone-size critique:** 2 fps contact sheet and a 360 px-wide phone sheet, scored on hook in 2 s, readability, motion, variety, composition and accounting accuracy. **Cap at 3 rounds.** Sound sync is checked by waveform or peak analysis, not from images.
3. **Frame-range re-renders** only for the seconds that changed.
4. **Sound:** place effects on the measured peak, add a soft chalk scratch under each write-on, duck any music under the voice.
- Skip 8x motion blur and beat-synced cutting.

## Status
- Done: Lesson 1 and 2 scripts (review fixes applied) with clip maps.
- Not done: Lessons 3–6, the trailer, the AI-track scripts, all visuals, recordings.
- Unknown: whether Lessons 1 and 2 have been recorded. If so, the script changes since the recording mean short re-records of the changed lines.

## Open decisions
1. **Mythic Lore Labs:** the first handoff said this channel replaces the Mythic Lore Shorts (views declining); the second said Mythic Lore Labs is still active and separate. Unresolved; it decides whether the old pipeline (mythic-lore-factory) is reused or kept running.
2. **"Module" naming:** "Module 1/Module 2" was used in earlier notes and never defined. Do not use the word in scripts until it is.
3. Posting cadence, success metric, disclaimer wording (educational, not accounting advice), OpenStax attribution.

## Dropped
- The 5–7 minute "Why Debits and Credits Still Matter" long-form script (superseded by Lesson 2).
- The 43- and 60-second Short scripts for debits and credits, A = L + E and the income statement (they exceed the 20–25 s format; rewrite as clips if wanted).
- Orange for credits (credits are yellow), on-camera split screens, and the DiLucci 1M–3.8M views claim.

## Working preferences (owner)
American English. Short, direct answers. No guesses; say when something is unverified. Push back on bad ideas. No narration while working.
