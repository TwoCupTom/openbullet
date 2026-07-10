# App Lab

All my apps and games in one repo — **one folder per project**. Built and iterated with
Claude Code, edited from any device.

## Projects

| Folder | What it is | Status |
|---|---|---|
| [`pocket-arcade/`](pocket-arcade/) | All-in-one revival of classic one-tap mobile games — six games, XP progression, leaderboards, $2.99 unlock flow | Playable prototype |

## Workflow (any device)

**First time on a machine:**
```
git clone https://github.com/TwoCupTom/app-lab
```
Open the folder in VS Code. Every project here is web-first with no build step unless its
own README says otherwise — open the project's `index.html` in a browser to run it
(the VS Code "Live Server" extension gives auto-reload while editing).

**Sitting down to work (always do this first):**
```
git pull
```

**Done for the day (always do this last):**
```
git add -A
git commit -m "what changed"
git push
```

Pull before you start, push when you stop — that's the whole trick to hopping between
devices without conflicts. Claude Code (in VS Code, the terminal, or on the web) follows
the same rule, so ask it to commit and push whenever it finishes something.

## Adding a new project

Make a new folder at the repo root, give it a `README.md`, and add a row to the table
above. Keep each project self-contained — no shared code between folders until something
truly earns it.
