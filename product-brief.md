# Momentum: Product Brief (v0.1)

## 1. Problem statement
A student with a full semester can't start work. Motivation doesn't come first; it builds up once she starts. Her attention leaks through a predictable chain: curiosity → YouTube → Shorts → Facebook → Instagram. Planners that need manual logging get abandoned.

## 2. Jobs to be done
- **When** I sit down and don't feel like working, **help me** start within 2 minutes **so that** momentum takes over.
- **When** something interesting pops up mid-task, **let me** save it in one tap **so that** I don't open YouTube.
- **When** a big assignment lands, **turn it into** steps I can put on the calendar **so that** it stops feeling huge.
- **When** I plan my day, **keep** gym, meals and sleep fixed **so that** work fits around my health, not the other way round.

## 3. Success metrics
| Type | Metric | Target (4 weeks) |
|---|---|---|
| North star | % of planned blocks started within 10 min | ≥ 60% |
| Engagement | Days with a plan / days in the period | ≥ 5 of 7 |
| Friction | Time from opening the app to having a plan | < 2 min |
| Guardrail | Gym blocks kept | 7 of 7 |

## 4. Design principles
1. **Taps over typing.** Nothing daily needs more than one line of text.
2. **The app suggests, you confirm.** Auto-plan, auto-log starts.
3. **Fixed blocks come first.** Health constraints are scheduled before tasks.
4. **Start small.** Every task can carry a step that takes under 2 minutes.

## 5. MVP scope (MoSCoW)
- **Must:** brain dump, Eisenhower sort, task breakdown, auto time-blocking, Start 5 min, parking lot, Day view
- **Should:** Week, Month and Semester zoom levels, deadlines, ten-second check-in, copy as text
- **Could:** backup and restore, dark mode
- **Won't (yet):** app blocking, notifications, calendar sync, recurring tasks

## 6. Known risks and open questions
- **The sleep window is 5 h.** Evidence (7–9 h for adults) says this works against focus and self-control. The app makes it editable and shows a note when it's under 7 h.
- **localStorage can be wiped.** Mitigation: account sync when hosted on Claude, plus manual backup.
- **The scheduler is greedy.** It doesn't respect "only in the morning" preferences yet.

## 7. Validation plan
Use it daily for 2 weeks. Each Sunday, check the Week view: on-time start %, top distraction. Write down three things to change, then pick the next roadmap item based on the evidence, not on a hunch.
