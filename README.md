<div align="center">

<img src="./assets/terminal.svg" width="100%" alt="Terminal. whoami: Akshay Nagar, founding engineer at Reacher. Focus: ClickHouse, Postgres ops, data pipelines, agentic dev tooling. Since Nov 2024: 1,222 PRs opened, 1,016 merged, 444 teammate PRs reviewed; 3,078 contributions in the last 12 months."/>

<br/>

[![LinkedIn](https://img.shields.io/badge/linkedin-aky9821-1d2021?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iIzgzYTU5OCIgZD0iTTIwLjQ1IDIwLjQ1aC0zLjU1di01LjU3YzAtMS4zMyAwLTMuMDQtMS44NS0zLjA0LTEuODUgMC0yLjEzIDEuNDUtMi4xMyAyLjk0djUuNjdIOS4zNVY5aDMuNDF2MS41NmguMDVjLjQ4LS45IDEuNjQtMS44NSAzLjM3LTEuODUgMy42IDAgNC4yNyAyLjM3IDQuMjcgNS40NnY2LjI4ek01LjM0IDcuNDNhMi4wNiAyLjA2IDAgMSAxIDAtNC4xMiAyLjA2IDIuMDYgMCAwIDEgMCA0LjEyek03LjEyIDIwLjQ1SDMuNTZWOWgzLjU2djExLjQ1ek0yMi4yMiAwSDEuNzdDLjc5IDAgMCAuNzcgMCAxLjcydjIwLjU2QzAgMjMuMjMuNzkgMjQgMS43NyAyNGgyMC40NWMuOTggMCAxLjc4LS43NyAxLjc4LTEuNzJWMS43MkMyNCAuNzcgMjMuMiAwIDIyLjIyIDB6Ii8+PC9zdmc+&labelColor=282828&color=1d2021)](https://www.linkedin.com/in/aky9821/)
[![X](https://img.shields.io/badge/x-@Aky__9821-1d2021?style=for-the-badge&logo=x&logoColor=ebdbb2&labelColor=282828)](https://x.com/Aky_9821)
[![Email](https://img.shields.io/badge/email-akshay.nagar0101-1d2021?style=for-the-badge&logo=gmail&logoColor=fb4934&labelColor=282828)](mailto:akshay.nagar0101@gmail.com)
![Profile views](https://komarev.com/ghpvc/?username=Aky9821&label=views&color=fe8019&style=for-the-badge)

</div>

### `$ cat about.md   # about me`

Founding engineer at **[Reacher](https://www.reacherapp.com)**, the affiliate platform TikTok Shop brands use to find, message and manage creators on autopilot.
Most of my work is the data layer: the ClickHouse analytics stack, the production Postgres underneath it, the pipelines that pull TikTok Shop data in, and the pager when any of it breaks.
The rest of the time I build tooling that lets a small team ship like a large one.

### `$ git log --highlights   # what I've shipped`

#### ⚡ Postgres ➜ ClickHouse

Moved the product's analytics reads from Postgres onto ClickHouse with a staged, flag-gated rollout. A strict parity harness had to match prod before anything switched over, and once it did, I deleted the old read paths.

- Worst-case dashboard loads got **an order of magnitude faster**: what used to take tens of seconds now comes back in a second or two.
- Heavy CRM recomputes that ran for most of a minute now **finish in seconds**.
- Matched prod on **every request** before cutover.

#### 🐘 Postgres in production

- **Led our production Postgres migration** to a new managed provider. Logical replication kept the new copy in sync until cutover, new connection pooling went in front of it, and the switch happened inside one short planned maintenance window.
- Query tuning on the hot paths. Some searches went from **tens of seconds to well under a second** with the right indexes and caching, and an auth cache took a big chunk of DB work off every dashboard load.
- Safe-by-default prod access, for engineers and for AI agents.

#### 🛰️ Pipelines & on-call

- TikTok Shop data pipelines, real-time and batch, feeding the analytics layer.
- Observability for the whole pipeline graph: lineage, freshness, and alerts that fire on state instead of noise.
- First responder on production incidents. I find the cause, ship the fix, write the blameless postmortem, and then add the guard that stops it from happening again.

#### 🤖 Agentic engineering

- **Claude Code and OpenAI Codex, side by side.** Claude does most of the driving. Codex runs read-only as an adversarial reviewer that tries to break each diff, and because it's a different model family it catches bugs Claude's own review misses.
- A personal Claude Code harness:
  - hooks that block destructive SQL against prod
  - a commit gate that audits comments first
  - auto-backgrounding for long commands
  - per-session state piped into my tmux sidebar
- A looping review agent that reads every PR requested from me and leaves inline comments. It never approves.
- Contributor to Reacher's shared AI dev tooling: agents, skills and guardrails that every repo picks up.
- On a normal day I have about **20 Claude Code sessions** running in parallel, each in its own git worktree, with Codex sessions alongside them.

### `$ cat stack.toml   # tech I use`

| | |
| :-- | :-- |
| `lang` | ![Python](https://img.shields.io/badge/Python-1d2021?style=flat-square&logo=python&logoColor=fabd2f) ![TypeScript](https://img.shields.io/badge/TypeScript-1d2021?style=flat-square&logo=typescript&logoColor=83a598) ![SQL](https://img.shields.io/badge/SQL-1d2021?style=flat-square&logo=postgresql&logoColor=83a598) ![Bash](https://img.shields.io/badge/Bash-1d2021?style=flat-square&logo=gnubash&logoColor=b8bb26) ![C++](https://img.shields.io/badge/C++-1d2021?style=flat-square&logo=cplusplus&logoColor=83a598) |
| `data` | ![ClickHouse](https://img.shields.io/badge/ClickHouse-1d2021?style=flat-square&logo=clickhouse&logoColor=fabd2f) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1d2021?style=flat-square&logo=postgresql&logoColor=83a598) ![BigQuery](https://img.shields.io/badge/BigQuery-1d2021?style=flat-square&logo=googlebigquery&logoColor=83a598) ![Redis](https://img.shields.io/badge/Redis-1d2021?style=flat-square&logo=redis&logoColor=fb4934) ![pandas](https://img.shields.io/badge/pandas-1d2021?style=flat-square&logo=pandas&logoColor=d3869b) |
| `backend` | ![FastAPI](https://img.shields.io/badge/FastAPI-1d2021?style=flat-square&logo=fastapi&logoColor=8ec07c) ![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-1d2021?style=flat-square&logo=sqlalchemy&logoColor=fb4934) ![Pydantic](https://img.shields.io/badge/Pydantic-1d2021?style=flat-square&logo=pydantic&logoColor=d3869b) |
| `frontend` | ![React](https://img.shields.io/badge/React-1d2021?style=flat-square&logo=react&logoColor=83a598) ![Redux](https://img.shields.io/badge/Redux_Toolkit-1d2021?style=flat-square&logo=redux&logoColor=d3869b) ![TanStack Query](https://img.shields.io/badge/TanStack_Query-1d2021?style=flat-square&logo=reactquery&logoColor=fb4934) ![Tailwind](https://img.shields.io/badge/Tailwind-1d2021?style=flat-square&logo=tailwindcss&logoColor=8ec07c) ![Radix](https://img.shields.io/badge/Radix_UI-1d2021?style=flat-square&logo=radixui&logoColor=ebdbb2) |
| `infra` | ![Google Cloud](https://img.shields.io/badge/Google_Cloud-1d2021?style=flat-square&logo=googlecloud&logoColor=83a598) ![AWS](https://img.shields.io/badge/AWS-1d2021?style=flat-square) ![Docker](https://img.shields.io/badge/Docker-1d2021?style=flat-square&logo=docker&logoColor=83a598) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-1d2021?style=flat-square&logo=githubactions&logoColor=ebdbb2) |
| `ai` | ![Claude Code](https://img.shields.io/badge/Claude_Code-1d2021?style=flat-square&logo=claude&logoColor=fe8019) ![Codex](https://img.shields.io/badge/OpenAI_Codex-1d2021?style=flat-square) ![Anthropic API](https://img.shields.io/badge/Anthropic_API-1d2021?style=flat-square&logo=anthropic&logoColor=ebdbb2) ![MCP](https://img.shields.io/badge/MCP-1d2021?style=flat-square&logo=modelcontextprotocol&logoColor=ebdbb2) |
| `desk` | ![Ubuntu](https://img.shields.io/badge/Ubuntu_24.04-1d2021?style=flat-square&logo=ubuntu&logoColor=fe8019) ![tmux](https://img.shields.io/badge/tmux-1d2021?style=flat-square&logo=tmux&logoColor=b8bb26) ![zsh](https://img.shields.io/badge/zsh-1d2021?style=flat-square&logo=zsh&logoColor=ebdbb2) ![Linear](https://img.shields.io/badge/Linear-1d2021?style=flat-square&logo=linear&logoColor=83a598) |

### `$ tmux attach   # my workspace`

<img src="./assets/dock.svg" width="100%" alt="Mock of my tmux setup: an outer 'dock' tmux server with a sidebar listing workspace windows and Claude Code sessions grouped by status, open PRs, next meeting, CPU, network and a pomodoro, an ASCII cat, and four panes of Claude Code sessions in separate git worktrees."/>

- **The machine:** ASUS ROG Strix G15 with a Ryzen 9 5900HX, 40 GB of RAM, an RTX 3050 Ti plus a Radeon iGPU, running Ubuntu 24.04. It's my dev box and also the homelab server.
- **Keys:** tmux with Zellij-style modal bindings. `Alt-hjkl` moves between panes; `Ctrl-p`, `Ctrl-t`, `Ctrl-n` and `Ctrl-s` switch to the pane, tab, resize and scroll modes.
- **The dock:** an outer tmux server wraps the real session. Its clickable sidebar lists every Claude session by status (working, needs you, idle) and shows widgets for Slack and Linear focus, open PRs, my next meeting, now playing, weather, CPU and network.
- **The rest:** gruvbox everywhere, resurrect and continuum so sessions survive reboots, `lazygit`, `btop`, and an ASCII cat that panics when CPU goes over 70%.

### `$ docker ps   # homelab`

```text
jellyfin      movies & tv
navidrome     music streaming (subsonic api)
sonarr        tv library automation
radarr        movie library automation
slskd         soulseek -> beets (musicbrainz match) -> navidrome
wolf          games-on-whales: streams games from the iGPU to any moonlight client
```

An earlier version of the music setup is public as [**soularr-stack**](https://github.com/Aky9821/soularr-stack), and the old [**neoted**](https://github.com/Aky9821/neoted) is a terminal text editor I wrote in C++.

### `$ cat ~/.fun   # off the clock`

```text
🥦  vegetarian, and serious about fitness
🎸  learning electric guitar — slowly, loudly
🐈  the cat in my tmux sidebar has better uptime than most services
```

<div align="center">

<sub>Happy to talk ClickHouse, Postgres migrations, data pipelines, or agent tooling: <a href="mailto:akshay.nagar0101@gmail.com">akshay.nagar0101@gmail.com</a></sub>

</div>
