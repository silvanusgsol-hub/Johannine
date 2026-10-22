# Johannine Writings: The Games

Interactive review games for the **Johannine Writings** course (Master of Divinity, Global School of Open Learning, course guide by Joe Thomas). There is one standalone game for each of the six units, plus a homepage that links to them all.

## Files

```text
course-games/
├── index.html    Homepage with a card for each unit
├── unit_1.html   The Beloved Disciple Files      (Lessons 1–2, 13 challenges)
├── unit_2.html   The Seven Lamps                 (Lessons 3–4, 15 challenges)
├── unit_3.html   The Foyer and the Feast         (Lessons 5–6, 14 challenges)
├── unit_4.html   Signs on Trial                  (Lessons 7–8, 14 challenges)
├── unit_5.html   The Towel and the Empty Tomb    (Lessons 9–10, 13 challenges)
├── unit_6.html   Letters from the Elder          (Lessons 11–12, 13 challenges)
└── README.md
```

Each file is plain HTML with its CSS and JavaScript built in. There is no server, database, external library or API key. Each unit file works on its own and links back to `index.html` with a relative link.

## Activity types

Every unit uses all eight types:

| Type | What students do |
|---|---|
| 🔍 Narrative Detective | Read a clue and choose the point it proves (answer options are shuffled each time) |
| ⇅ Story Sequencer | Put events, scenes or sayings in order (arrow buttons, or drag on a computer) |
| ⇄ Theme & Character Matcher | Match characters, sayings or images to their meaning or reference |
| 🗂 Arrange the Evidence | Sort clues into categories |
| 🛤 Choose Your Path | Respond to a church situation drawn from the lesson's opening story and see the consequence. The scenario is clearly labelled as hypothetical, and a box shows what the course actually says |
| 📜 Unlock the Scroll | Type a missing word or phrase. Close wording and spelling variants are accepted; a hint appears after the first try |
| 🏛 Build the Story | Rebuild an outline, chiasm, map or prayer structure slot by slot |
| ✍ Reflection Challenge | Write a short answer, then compare it with a model response and checklist from the lesson. This earns a completion point and is **not** machine-marked |

### What each unit covers

- **Unit I:** internal and external evidence, eliminating candidates for the author, John's life, five dating clues and the Rylands Fragment, place of writing, purpose, genre, differences from the Synoptics, Exodus 15–17, literary techniques, the Gospel's outline.
- **Unit II:** "believe", already and not yet, the "hour", the seven "I am" sayings, misunderstandings, living water, the Paraclete, criteria for a sign, Word, Revealer, Redeemer and Son, the Son of Man sayings, Jesus's humanity, how the cross works, Exodus 3:14.
- **Unit III:** the prologue's chiasm, space, time and being, three backgrounds of the *logos*, Sandmel's "parallelomania", 1:17, gnostic denials, Cana to Cana, the temple clearing (two abuses, two cleansings), the seventh hour, Greek word study.
- **Unit IV:** where each sign takes place, the Sabbath and the mat, the circumcision precedent, the lame man and the blind man compared, the blind man's growing sight, messianic expectations, water and light at Tabernacles, the good shepherd, John 11–12 in order, Mary and Judas, Martha's confession, the Greeks.
- **Unit V:** the upper room in order, the meaning of the footwashing, the "helping Presence", the Spirit's works, Isaiah 5 and John 15, the structure of John 17, the Passion in order, who said what, Mary Magdalene as first witness, 20:22, Domitian.
- **Unit VI:** three strands of false teaching, John's four affirmations, Dodd's three differences, Ephesus and Trajan, the spiral structure of 1 John, 5:13, the elect lady, how 2 and 3 John are built, Gaius, Diotrephes and Demetrius, hospitality and discernment, gains and losses of single leadership.

## Scoring

- Each challenge is worth 1 point.
- Choice questions: 1 point for the correct answer. Choose Your Path: 1 point for the path the lesson supports; some paths earn half a point.
- Sequencing, matching, sorting and building: the whole answer is checked at once, and students earn credit for each item placed correctly (for example, 5 of 7 correct = 0.71).
- Unlock the Scroll: 1 point on the first try, half a point on the second.
- Reflections: 1 completion point.
- Answers lock after submission. **Play again** reshuffles every question and resets the score.
- Ranks at the end are themed for each unit and set at 90%, 75% and 55%.
- Each student's best score is saved in their own browser (`localStorage`) and shown on the homepage. Nothing is sent anywhere.

## Publishing on GitHub Pages

1. Sign in to GitHub and create a new repository (for example `johannine-games`), or open an existing one. Make it **Public** (GitHub Pages on a free account needs a public repository).
2. Choose **Add file → Upload files**. Drag in `index.html`, all six `unit_N.html` files and `README.md`. Put them all at the top level of the repository, in the same folder, not inside a subfolder. Click **Commit changes**.
3. Keep the homepage named exactly `index.html` (lower case).
4. Open the repository's **Settings → Pages**.
5. Under **Build and deployment**, set **Source** to *Deploy from a branch*. Choose the branch **main** and the folder **/ (root)**, then click **Save**.
6. Wait a minute or two. Refresh the Pages settings screen until it shows "Your site is live at https://YOUR-USERNAME.github.io/johannine-games/". Open that link.
7. Check that the homepage shows all six unit cards, that each card opens the right game, and that **All units** in each game returns to the homepage.

To update a game later, upload the changed file again with the same name. The site redeploys automatically.

## Testing notes

All six games were played automatically in headless Chromium (Playwright). Each was played once answering everything correctly (every unit scored 100%) and once answering everything wrongly, after a replay. The tests confirmed that controls lock after submission, replay resets the score and state, the shuffled options keep their correct answers, there are no JavaScript errors, all homepage links resolve, and there is no sideways scrolling at phone width (375 px). Light and dark colour schemes were both checked.
