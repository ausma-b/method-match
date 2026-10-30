# Method Match

A three-round classroom game for undergraduate qualitative research methods. Groups of 5–6 sort data collection methods, match one to a real research question, adapt to a curveball, and pitch their choice to the class in 45 seconds.

It's designed for the end of a first tutorial and takes about 22 minutes. It runs in any modern browser on a laptop, tablet or projector, with nothing to install.

**Play it:** `https://YOUR-USERNAME.github.io/method-match/` *(replace with your GitHub Pages link)*

---

## How it works

| Round | Time | What groups do |
|---|---|---|
| Team | 1–2 min | Enter a team name and members; the game deals roles at random |
| 1. Sort | 5 min | Sort eight method cards by **who creates the data**: the researcher with participants, no one (it happens anyway), or it already exists |
| Worked example | 2 min | Tutor models a full answer using a demo question |
| 2. Match | 10 min | Draw a research question, choose a method, answer three prompts, then handle a curveball |
| 3. Pitch | 45 sec per group | Read the auto-filled speaking frame to the class |

### Roles

Roles are dealt at random from the names entered:

- **Card reader:** reads every card and question aloud.
- **Scribe:** types the group's answers.
- **Speaker:** presents in Round 3.
- **Devil's advocate:** argues for a different method before the group locks in.
- **Ethics checker:** asks "who could be harmed?" before anything is locked in.
- **Timekeeper:** runs the timer. With 5 players, this merges with the card reader.

### Scoring (maximum 180)

| Item | Points |
|---|---|
| Round 1: each card in an accepted column | 10 (up to 80) |
| Round 2: method fit | Strong 40 · could work 20 · weak 5 |
| Round 2: each of the three prompts answered (15+ characters) | 10 (up to 30) |
| Round 2: "Why not another method?" bonus | 15 |
| Round 2: curveball answered | 15 |

Ranks: Honours student · Research assistant (70+) · Research fellow (110+) · Principal investigator (150+).

---

## Running it in class

1. Share the link (or a QR code) before the activity. One device per group.
2. Groups set up their team and roles, then start Round 1.
3. When groups reach the worked example screen, pause the class and model the example aloud. This is the most important scaffold, so don't skip it.
4. During Round 2, circulate. Common traps to nudge on:
   - **Choosing a survey:** "That tells you how many. Your question asks how or why."
   - **Defaulting to interviews without a reason:** "Why not a focus group?"
   - **Unrealistic access:** "How would you actually recruit them?"
   - **Vague ethics:** "Who specifically could be harmed?"
5. For Round 3, each speaker reads the frame on their screen. Give one line of feedback per group: one strength or one question back.

**Tips**

- To control which questions groups get, give each group a shortlist of question numbers and have them use **Choose from the list** instead of **Draw a question**.
- Groups that finish early can use **Try another question** for a second round. Their Round 1 score is kept.
- Progress is saved in each device's browser, so a refresh won't lose work. **New game** clears it.
- Scores stay on each device. There's no shared class leaderboard.

---

## Customising

Everything is in one file, `index.html`. Search for these names to edit the content:

| To change | Find | Notes |
|---|---|---|
| Method cards | `const METHODS` | Each card needs an `id`, `name` and short description `d` |
| Round 1 answer key | `const SORTKEY` | `ok` lists the accepted columns (`A`, `B`, `C`); `debate: true` marks a card as contested (yellow) |
| Research questions | `const QS` | `c` category, `q` question, `s` strong-fit method ids, `w` weak-fit method ids, `n` feedback note. Any method not in `s` or `w` scores as "could work" |
| Curveballs | `const CURVES` | One sentence each, ending with a question |
| Roles | `const ROLES` | Name `r` and task `t` |
| Round timers | `const TIMES` | In seconds |

After editing, commit the change on GitHub and the live page updates within a couple of minutes.

---

## Hosting

The game is a single static HTML file, so it runs on GitHub Pages or any web host:

1. Upload `index.html` to a public GitHub repository.
2. Go to **Settings → Pages**, set **Source** to *Deploy from a branch*, and choose **main** and **/ (root)**.
3. Your link appears at the top of the Pages settings after a minute or two.

Fonts load from Google Fonts. If they're blocked on your network, the page falls back to standard system fonts and still works.

---

## Accessibility

- Atkinson Hyperlegible body font, with high-contrast colours.
- Light and dark mode follow the device setting.
- Fully keyboard operable: Tab to a card or column, then Enter to select or place it.
- Animations are switched off for users who prefer reduced motion.
