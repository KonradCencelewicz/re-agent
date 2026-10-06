# re-agent
Research Engineer Agent

## About

This repository hosts an **RE (Research Engineer) agent** whose job is to research new features for my apps.
For each app it keeps track of what the project is about, explores ideas, and collects feature proposals
in a structured, per-project backlog.

The agent also researches the **competition**: it identifies competing apps, records them in `COMPETITION.md`,
and analyses which features those apps offer. These findings feed into the feature ideas in the backlog.

You can add as many projects as you want. Each project gets its own directory inside the `projects/` folder,
so research for different apps stays separated.

## Structure

```
re-agent/
├── README.md
└── projects/
    ├── <project-a>/
    │   ├── PROJECT.md       # what the app is, goals, tech stack, link to the GitHub repo
    │   ├── BACKLOG.md       # researched feature ideas, prioritized
    │   ├── COMPETITION.md   # competing apps and the features they offer
    │   └── ...              # other research notes for this project
    └── <project-b>/
        ├── PROJECT.md
        ├── BACKLOG.md
        ├── COMPETITION.md
        └── ...
```

- **`projects/`** – root folder for all researched apps.
- **`projects/<project-name>/`** – one directory per app, created by the agent when a new project is added.
- **`PROJECT.md`** – project description and context the agent uses as the basis for research. It also stores
  a **link to the app's GitHub repository**, so the agent can check the existing code: what is already
  implemented, how it is built, and which new features fit the current codebase.
- **`BACKLOG.md`** – list of proposed features resulting from the research.
- **`COMPETITION.md`** – list of competing apps found by the agent, with the features each one offers.
- Additional files (research notes, etc.) can be added per project as needed.

## Adding a project

Ask the agent to add a new project. It will create `projects/<project-name>/` with the base files
(`PROJECT.md`, `BACKLOG.md`, `COMPETITION.md`, ...), which you can then fill in or let the agent populate during research.
