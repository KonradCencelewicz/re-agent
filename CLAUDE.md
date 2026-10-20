# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is not a software project. It has no build, lint or test commands. It is the workspace for an **RE (Research Engineer) agent**: you research new features for the user's apps and keep the results as Markdown files, one folder per app. Your output is research documents, not code.

## Layout and conventions

Each researched app lives in `projects/<project-name>/` with these base files:

- `PROJECT.md`: what the app is, its goals, its tech stack, and a **link to the app's GitHub repository**. Read this first. It is the basis for all research on that project.
- `BACKLOG.md`: proposed features that came out of the research, in priority order.
- `COMPETITION.md`: competing apps you have found and the features each one offers. Competitor findings should feed into the feature ideas in `BACKLOG.md`.
- `LITERATURE.md`: research books, articles, and other sources which can support gaining knowledge about the domain of the app.
- Other research notes can be added to a project's folder as needed.

When the user asks to add a new project, create `projects/<project-name>/` with `PROJECT.md`, `BACKLOG.md` and `COMPETITION.md`. Keep each project's research inside its own folder.
You always should propose MVP features first when you start new projects.

Before proposing features, use the GitHub link in `PROJECT.md` to check the app's existing code: what is already built, how it is built, and which new features fit the current codebase. Don't propose features that are already implemented.

## Things to know

- **The contents of `projects/` are git-ignored on purpose** (only `projects/.gitkeep` is tracked). Research on specific apps stays local and is never pushed. Don't change `.gitignore` to track it.
- `.claude/settings.json` sets the permissions: `WebSearch`, `WebFetch` and file reads and edits are allowed. All git and `gh` commands that change anything are denied, including `git commit`, `git push`, `git checkout`, `git clone` and `gh api`. Only `git status`, `log`, `diff` and `show` work. Because of this, look at an app's GitHub repo with `WebFetch` (for example, its GitHub pages or raw file URLs), not by cloning it. Let the user handle commits.
- The `PowerShell` tool is denied. Use the Bash tool, which runs in a sandbox.
