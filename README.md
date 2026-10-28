# OPIM639 Quiz (static web app)

135 MCQs + 36 short-answer questions for OPIM639 (Prof LIM Yun Fong), arranged by topic T1–T9.

**Features**
- Pick topics in course order.
- Practice mode: instant feedback, plus why each wrong option is wrong.
- Exam mode: timed at 72 s per question, with a score, weak topics and a full review at the end.
- Randomise questions and shuffle options.
- "Must-know only" and difficulty filters.
- Short questions: model answer, self-marking checklist and common mistakes.
- "Retry my wrong answers".
- Progress is saved on each device.
- Works on phone and laptop, with dark mode.

## Deploy (about 5 minutes, no coding)
1. On GitHub, click **New repository** and name it `opim639-quiz`. Private is fine.
2. In the new repo, click **Add file → Upload files**. Drag in `index.html`, `questions.json` and `README.md`, then click **Commit**.
3. On vercel.com, click **Add New → Project**. Import `opim639-quiz` and set the framework preset to **Other**. Leave the build command empty and the output directory as the root. Then click **Deploy**.
4. Open the URL on your phone and choose **Add to Home Screen** so it works like an app.

## Editing questions
Edit `questions.json` on GitHub (pencil icon) and commit. Vercel redeploys on its own in about 30 s.
Each MCQ has: `q`, `options` (4), `answer` (0 = A … 3 = D), `explanation`, `why_wrong` (with "" at the answer position), `topic`, `difficulty` (E/M/H), `priority` (must/should/nice).

Note: opening `index.html` straight from your disk will not load the questions, because browsers block that. Use the Vercel link instead, or run `python3 -m http.server` in this folder and open http://localhost:8000.
