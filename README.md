# 75 Hard Squad

A web app I built to keep my crew honest through the 75 Hard challenge. Everyone logs their daily tasks, the squad sees it, and nobody gets to quietly disappear on day 23 and pretend it never happened.

**Live app:** https://nicolas-angarita.github.io/75-Hard-Squad

## What it does

75 Hard is a mental toughness program: 75 straight days of two workouts (one outdoors), a gallon of water, 10 pages of a non-fiction book, a progress photo, and sticking to a diet. Miss a task, you start over from day one. It's brutal on purpose, and it's a lot easier to quit when nobody's watching.

This app makes sure somebody's watching. Each member of the squad has their own tracker where they check off the day's tasks, and everyone else can see the board. Streaks, misses, who's on what day — all of it's visible to the whole group. If you fall off, the squad knows before you've finished making up an excuse for it.

The squad currently spans Texas, California, Arizona, and the Carolinas, so this is basically the only way we can actually hold each other accountable across four time zones.

## How it works

The front end is plain HTML, CSS, and JavaScript — no framework, no build step, just files you can open in a browser. It's hosted on GitHub Pages straight off the repo, which is why deploying changes is as simple as pushing to main.

Data lives in JSONBin, which acts as a lightweight cloud database for the squad's daily logs. When someone checks off a task, it writes to the bin. When you load the page, it pulls everyone's latest state down. It's not fancy, but for a group tracker with a handful of users, it's rock solid and costs nothing.

## Using it

Open the site, pick your profile, and check off your tasks for the day as you complete them. The board updates for everyone else in close to real time. Progress photos, day counters, and completion streaks all render from the shared data, so the view everyone sees is the same view.

If you break the chain, the tracker resets you to day one, same as the real program. No soft-resets, no grace days, no negotiating with yourself at 11:47 PM.

## Why I built it

Group chats are where accountability goes to die. People post a workout selfie on day three and then the thread slowly turns into memes by day ten. I wanted something where the state of the challenge was the first thing you saw, not something you had to scroll past old messages to find. Once the squad could glance at a single page and see exactly where everyone stood, the challenge got a lot harder to quietly bail on.

## Tech notes

- Static site — HTML, CSS, vanilla JS
- Hosted on GitHub Pages
- JSONBin for persistence
- No auth layer beyond profile selection, since this is a trusted private squad

## Repo

https://github.com/nicolas-angarita/75-Hard-Squad
