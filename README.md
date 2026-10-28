# OPIM639 Exam Prep Quiz

171 MCQs (including 36 based on Prof Lim's slide diagrams and photos) + 36 short-answer questions, for OPIM639 (Prof LIM Yun Fong), arranged by topic T1–T9.

## Features
- **Personal progress on each device.** Each person types a name; their progress, flags and notes are saved in their own browser. Nothing is uploaded anywhere. Several people can share one device with different names. Backups can be downloaded and restored to move progress to another device.
- **Practice and exam modes.** Practice gives instant feedback, explains why each wrong option is wrong, and shows a trap to remember. Exam mode is timed (72 s per question) and ends with a score, weak topics and a full review.
- **Revise list.** Questions you got wrong, questions you flagged (📍), and questions you have since fixed.
- **Print / export.** Print (or save as PDF) or download all questions, wrong only, flagged only, or wrong + flagged, with or without answers.
- **Traps & tips.** Exam traps for each topic, scoring tips, and encouragement.
- **Filters.** Randomise questions, shuffle options, must-know only, slide-diagram questions only, and difficulty.
- **Extras.** Keyboard shortcuts (A–D, Enter, F), confetti for streaks, dark mode, and a phone-friendly layout.

## New in v3
- **Spaced repetition:** a question you get wrong comes back the next day, then 3 days later, then the day before the exam. Use the "Due for review" button.
- **"Why did you miss it?" tags:** misread, didn't know, mixed up two ideas, calculation slip, guessed, fell for a trap. The Profile tab shows your pattern and your #1 fix.
- **Daily 10:** a set of 10 questions weighted towards your weak topics and anything due for review. A 4-week study-streak calendar shows how much you practised each day.
- **Calculation drills:** new numbers every time for the bucket brigade, network-effect equilibria, no network effect, link counts, price optimisation, cash conversion cycle and revenue share.
- **Full mock paper:** 40 MCQs (spread across all topics) + 3 must-know short questions, with a 2-hour timer. You mark the short questions yourself against the rubric, then get a total score and a breakdown by topic.
- **Install as an app and use offline:** on a phone, open the link and choose "Add to Home Screen". It then works without internet, for example on the MRT.
- **Flashcards:** 72 cards of definitions, lists and key numbers. Tap to flip; "Again" brings a card back tomorrow and "Got it" spaces it out.

## Deploy / update
- **First time:**
  1. Create a GitHub repo and upload ALL files: `index.html`, `questions.json`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png` and `README.md`.
  2. On Vercel, choose **Add New → Project**, import the repo, pick the **Other** preset and leave the build command empty.
- **Updating:** on GitHub, use **Upload files** to replace all the files (if you change questions, also change `CACHE` in sw.js, e.g. opim639-v4, so phones fetch the new version). Vercel redeploys on its own. Users keep their progress, which stays in their browser.

## Editing questions
Edit `questions.json`. Each MCQ has these fields:
- `q`: the question
- `options`: the 4 answer choices
- `answer`: 0–3
- `explanation`
- `why_wrong`: use "" at the answer position
- `topic`
- `difficulty`: E, M or H
- `priority`: must, should or nice
- `visual`: optional

`traps`, `tips` and `cheers` hold the exam traps, tips and encouragement messages.
