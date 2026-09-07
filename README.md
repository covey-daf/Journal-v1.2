# Journal

A private nightly journal. One HTML file. No server, no account, no data leaving the device.

Five minutes at night, one screen in the morning. It tracks what you finish, what gives you
energy, what drains you, and what other people come to you for. Once a month it does arithmetic
on that and reads the pattern back.

Adapted from a template built by Francesca.

---

## Deploy it

You need a GitHub account. Nothing else.

1. Create a new repository. Public is fine — there is no data in the file.
2. Upload `index.html` to the root.
3. Settings → Pages → Source: **Deploy from a branch** → `main` / `/ (root)` → Save.
4. Wait a minute. The URL appears at the top of that same Pages screen.
   It looks like `https://<you>.github.io/<repo>/`.

## Install it

1. Open that URL in **Safari** on your phone.
2. Share → **Add to Home Screen**. Name it Journal.
3. Launch it from the icon, not from Safari.

Launching from the icon matters. iOS clears stored data for sites you have not opened in seven
days of browser use. Home screen web apps are outside that rule — they keep their own counter,
which your daily use resets.

## First launch

Four questions: your areas, how you want your time split across them, the decision you are
carrying, and two counters for books and activity. It takes about three minutes.

**On areas.** Divide by what the work feels like to do, not by who it is for. If one area holds
both writing you enjoy and scheduling you don't, the energy signal inside it cancels out. Give
admin its own line — it never appears on a calendar and will otherwise hide inside everything
else. Three to seven works. More than seven and you stop tagging honestly at 10pm.

**On intent.** These total 100, which is the uncomfortable part. Giving one area more takes it
from another. Set a real number for anything you want more of, even if it currently gets none.
An area with a number and no days under it is the most useful thing this will show you.

Everything is editable later on the `year` page.

---

## The rhythm

**Nightly.** Three things you finished, each tagged to an area. One rotating question. What gave
you energy. What someone came to you for. What drained you. How much was triage. Three things
for tomorrow. It saves as you type — you can stop halfway.

The floor is three accomplishments, the writing box, and three for tomorrow. Everything else is
optional on any given night. Blank fields are honest data. If you find yourself filling every
field, you have started inventing and the columns stop meaning anything.

**Morning.** What you finished yesterday, what you set for today, where you stand.

**Weekly.** One question about your professional direction, on the `year` page. Fourteen rotate.
Easiest thing to skip, usually the most useful.

**Monthly.** The `mirror` page. It holds you to last month's commitment before it lets you make
a new one.

---

## Backups

Every third entry a banner appears offering a backup. It writes
`journal-backup-YYYY-MM-DD.json` to Files. It contains everything, plus a plain-text digest at
the top of the file that is readable without any tooling.

Take it. It is the only thing standing between you and losing the lot if the phone goes in a
pool.

There is also a copy button on the `mirror` page that puts the current window's readings on the
clipboard as text.

## Talking to Claude about it

Either export works. The digest inside the backup JSON is the fuller one — it lists every logged
day with areas, energy, aptitude, drain and triage resolved to real names rather than ids, plus
the last thirty entries of each log.

Attach the JSON, or paste the mirror text. Then ask what it shows.

Worth waiting until there are two or three weeks in it. Before that the mirror is mostly empty
and there is nothing to discuss.

---

## Changing it

The whole app is `index.html`. Attach it to a Claude conversation and describe what you want
different.

Your entries survive edits as long as the storage keys stay the same. They all start `jc2:` —
`jc2:config`, `jc2:day:YYYY-MM-DD`, `jc2:rollup`, and one key per log. Change that prefix and the
app will look at an empty shelf and run first-launch setup again.

Don't change anything for the first two weeks. If something irritates you on night three, write
it down instead of fixing it.

## What it doesn't do

No notifications, no calendar access, no background anything. No model runs inside it — the
observations are conditional rules written in advance, waiting for numbers that satisfy them. It
will surprise you with arithmetic you had not done. It will not surprise you with an insight.

The fonts load from Google. Offline it falls back to system serif and sans. Everything else
works with no network at all.
