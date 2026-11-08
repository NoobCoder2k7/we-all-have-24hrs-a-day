# Notes:

This is also the byproduct of being distracted. But hopefully, one day, I can come back and refine this product more.

I'm shadowing the job of a Product Manager, with the end user being myself :) Will keep me in the loop for the entire stage of this product development. Hopefully, my client will benefit and grow better and understand more about themselves from this product; and I, as a PM and Full-Stack Engineer working alongside Claude at any point Im awake, will receive good money (as in developing my technical skill and fostering a more efficient bond with my fellow AI worker and knowing more about the client).

Some random shower thoughts on scaling part (nothing technical here):
- Customized planner:
  + How to make the onboarding process more smoothly for different types of people (people with ADHD like me, or people with really high level of discipline then passion)? Which frameworks should I use to categorize the type of users to make them live their life to the fullest?
- Also, from the usage pattern, we can further design our app more.
- How to systematically design this?

# Momentum

A planner with exactly one user, and she has a C-drama to get back to.

I'm Trang. I'm a student, I have too many things to do, and my usual day goes like this: I open my coursework, something in it makes me curious, I look it up on YouTube, YouTube becomes dessert Shorts, then Facebook, then Instagram, and an hour later the task still hasn't started.

I tried planners. They all wanted me to write down everything I did, all day. I lasted about a week each time.

So I'm building my own. The goal isn't productivity porn. It's simpler: I want to organise my life, put my goals somewhere I'll actually see them, and get better at starting.

## What it does right now

You type out everything on your mind, one line per task. You sort each one into a box: do it first, schedule it, quick win, or not today. Then you press one button and get today's plan, built around the things I don't negotiate on: gym, meals and sleep.

Every task has a **Start 5 min** button. Five minutes is a promise I can keep, and once I've started I usually keep going.

When something makes me curious mid-task, I park it in one tap instead of searching for it. I look it up later, at dinner or on the treadmill.

That's it. There are also week, month and semester views for deadlines, but the day view is the point.

## How I want it to grow

I get tired when an app throws twenty features at me on day one. So the rule for this project is:

**Show less at the start, unlock more as I use it.**

Day 1 is just: dump tasks, get a plan, press start. Things like task breakdowns, weekly stats and the semester view should show up once I'm actually using the basics, not before.

The other rule: **it shouldn't look like it was generated.** No emoji, no "AI-powered" anything, no dashboards full of numbers I didn't ask for. It should look like something a person made for herself, because that's what it is.

## Roadmap

Small steps, in the order I'll probably need them.

**Next**
- Goals. A place to write what I want this semester (not just what's due), and see which of today's tasks moves each goal forward.
- Progressive unlocking. New features appear after I've used the app for a few days, with one short line explaining each.
- Recurring tasks, for weekly lectures and tutorials.

**Later**
- Learn how long my tasks really take, from my Start and Done taps, and adjust the time buffer automatically. No manual timesheets.
- Paste in a syllabus and get the semester's deadlines filled in.
- A nudge when I open YouTube or Instagram during a focus block, probably through iOS Shortcuts.
- Install it on my phone's home screen, with the current block on the lock screen.

**Someday, if it works for me**
- Let a few friends try it, interview them, and write up what I learned. One user is a diary; ten users is a product.
- Study-together rooms, where friends start the same focus block at the same time.
- Use my own data to argue myself into more sleep.

## Run it

It's one HTML file. No install, no build.

- Open `index.html` in a browser, or
- Turn on GitHub Pages (Settings → Pages → deploy from `main`), then open the link on your phone and add it to your home screen.

Your data is saved in your browser. Use **Semester → Backup** now and then, because clearing your browser data clears your plans too.

## Why it's built this way

Most of the features come from research on procrastination and planning, not from other apps:

- Deciding *when and where* you'll do something makes you far more likely to do it (Gollwitzer & Sheeran, 2006). That's why the plan has times, not just a list.
- We consistently underestimate how long things take (Buehler et al., 1994). That's why every estimate gets a buffer.
- Big, vague tasks are the ones we put off most (Steel, 2007). That's why you can break a task into steps.
- People pick urgent over important even when important pays off more (Zhu et al., 2018). That's why the sorting boxes exist.
- Saving a treat for something you're avoiding helps you do it (Milkman et al., 2014). That's why the gym block says to save the C-drama for the treadmill.

Full references are in [`docs/product-brief.md`](docs/product-brief.md).

## License

MIT
