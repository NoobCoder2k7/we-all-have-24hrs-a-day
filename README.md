# Momentum

**A daily planner for students who know what to do but can't make themselves start.**

Momentum turns a messy brain dump into a time-blocked to-do list for the day. It works around the things that don't move (gym, meals, sleep) and gets you into the first five minutes of work, because once you've started, keeping going is easier.

> Status: **v0.1 (MVP)**, a single HTML file with no build step and no dependencies.

---

## The problem

I'm a student with a lot to do and no motivation to start it. My usual day goes like this:

1. I sit down to work on coursework.
2. Something in it makes me curious, so I look it up on YouTube.
3. YouTube turns into Shorts (desserts, makeup), then Facebook, then Instagram.
4. An hour is gone and the task hasn't started.

Most planners make this worse because they expect me to **record everything by hand**. I quit them within a week.

### Who it's for

| | |
|---|---|
| **User** | University student with a semester full of deadlines |
| **Main pain** | Starting tasks, not knowing what the tasks are |
| **Fixed constraints** | 1 h of gym every day (ideally 15:00–16:00), 2 meal blocks, a fixed sleep window |
| **Anti-requirement** | No heavy manual logging. Every daily action is a tap or one line of text. |

### How I'll know it works

**North-star metric:** the share of planned focus blocks *started within 10 minutes of their scheduled time*. The app records this automatically when you tap **Start**.

---

## Features

| Feature | What it does | Why (evidence) |
|---|---|---|
| **Brain dump** | Type one task per line. `2h`, `45m`, `!i` (important) and `!u` (urgent) are parsed automatically. | Getting tasks out of your head first reduces the load of open loops (Masicampo & Baumeister, 2011). |
| **Eisenhower sort** | Tap a task and drop it into Do first / Schedule / Quick wins / Not today. | People pick urgent tasks over important ones even when the important ones pay off more: the *mere urgency effect* (Zhu, Yang & Hsee, 2018). |
| **Break it down** | Split a big task into steps with time estimates. Each step becomes its own block. | Vague, unpleasant tasks get put off the most; concrete steps reduce that (Steel, 2007, procrastination meta-analysis). |
| **Auto time-blocking** | One tap schedules the day around gym, meals and sleep, important work first, in focus blocks with short breaks. | Planning *when* and *where* you'll act (implementation intentions) strongly improves follow-through (Gollwitzer & Sheeran, 2006). |
| **Time buffer** | Pads every estimate (25% by default). | The planning fallacy: we routinely underestimate how long tasks take (Buehler, Griffin & Ross, 1994). |
| **First tiny move** | Each task can carry a step that takes under 2 minutes ("open the doc and write the heading"). | Lowers the cost of starting; in behavioural activation, action comes before motivation. |
| **Start 5 min** | A five-minute focus timer. Afterwards: "Keep going?" | Commit only to starting. Most people keep going once the start is behind them. |
| **Parking lot** | When something sparks curiosity mid-task, write it down in one tap instead of searching for it. Look it up later at a meal or on the treadmill. | Breaks the curiosity → YouTube → Shorts → social chain at its first link. |
| **Temptation bundling** | Gym and meal blocks suggest saving C-dramas and Shorts for those times. | Pairing a "want" with a "should" increased gym attendance (Milkman, Minson & Volpp, 2014). |
| **Ten-second check-in** | Tap what pulled you off track. No journaling. | Gives you data on your distractions without manual logging. |
| **Zoom levels** | Semester → Month → Week → Day. Deadlines are entered once and show up as "Coming up" in the Day view. | Long-range goals work better when tied to near-term ones (goal-setting theory, Locke & Latham, 2002). |

---

## How a day works

```
Dump tasks  →  Sort into 4 boxes  →  Break big ones down  →  Plan my day  →  Start 5 min  →  Check in
 (10 sec)          (taps)              (optional)            (1 tap)        (1 tap)        (taps)
```

The result is a timeline of the day: your tasks fill the gaps between the fixed blocks, each with a checkbox and a **Start** button.

---

## Run it

There is no build step. Choose one:

- **Open the file:** download `index.html` and open it in any browser.
- **GitHub Pages:** go to Settings → Pages → Deploy from branch → `main` / root. The app will be at `https://<you>.github.io/momentum/`.
- **On your phone:** open the Pages URL and use "Add to Home Screen".

### Where your data lives

- **Standalone (GitHub Pages or a local file):** saved in your browser's `localStorage`. Use **Semester → Backup → Copy backup** now and then, because clearing site data deletes it.
- **Hosted as a Claude artifact:** synced privately to your Claude account, with `localStorage` as the offline fallback.

---

## Project structure

```
momentum/
├── index.html          # the whole app: HTML, CSS and JS in one file
├── README.md
├── docs/
│   └── product-brief.md  # problem, users, metric, scope, roadmap
└── LICENSE
```

## Tech choices

- **Vanilla JS, no framework.** One file is easy to fork and works offline from `file://`. React can come in when there's more than one person working on it.
- **The scheduler is a greedy algorithm** (`planDay`). It sorts units by quadrant, walks free time between fixed blocks, splits long units at the focus length with 10-minute breaks, and lists whatever doesn't fit before lights-out under "Didn't fit today".
- **Storage adapter.** Saves locally first; if account sync is available it syncs one document per day, so documents stay small.

## Roadmap

- [ ] **v0.2:** recurring tasks (weekly lectures, tutorials) and import of semester deadlines from a pasted syllabus
- [ ] **v0.3:** a weekly review screen (wins, slips, next week's top three)
- [ ] **v0.4:** PWA (installable, offline, notifications at the start of each block)
- [ ] **v0.5:** a phone-friction companion (iOS Shortcuts automation that shows your current block when you open YouTube or Instagram)
- [ ] Explore: calendar sync (Google Calendar) for classes

## References

- Buehler, R., Griffin, D., & Ross, M. (1994). Exploring the "planning fallacy". *Journal of Personality and Social Psychology, 67*(3), 366–381.
- Gollwitzer, P. M., & Sheeran, P. (2006). Implementation intentions and goal achievement: A meta-analysis. *Advances in Experimental Social Psychology, 38*, 69–119.
- Locke, E. A., & Latham, G. P. (2002). Building a practically useful theory of goal setting and task motivation. *American Psychologist, 57*(9), 705–717.
- Masicampo, E. J., & Baumeister, R. F. (2011). Consider it done! Plan making can eliminate the cognitive effects of unfulfilled goals. *JPSP, 101*(4), 667–683.
- Milkman, K. L., Minson, J. A., & Volpp, K. G. M. (2014). Holding the Hunger Games hostage at the gym. *Management Science, 60*(2), 283–299.
- Steel, P. (2007). The nature of procrastination: A meta-analytic and theoretical review. *Psychological Bulletin, 133*(1), 65–94.
- Zhu, M., Yang, Y., & Hsee, C. K. (2018). The mere urgency effect. *Journal of Consumer Research, 45*(3), 673–690.

## License

MIT
