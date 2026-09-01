# Agent Log

Append-only record of automated and agent-assisted changes to this repository.

Purpose: this work happens from more than one machine, so local notes are not a
reliable history. Anything an agent should know about a past change belongs
here, in the repository, not in a local file.

## Conventions

- Newest entry first. Never rewrite or delete an existing entry; correct it with
  a new one that says what it supersedes.
- Record what was verified and how, not just what was edited. "Fixed" without a
  check is not a result.
- Record open items and known-failing things explicitly, so the next agent does
  not rediscover them or assume they are already handled.
- No participant data, transcripts, consent records, committee or faculty names,
  credentials, or tokens. See AGENTS.md where present.

---

## 2026-08-31 - Adopt the shared ecosystem design tokens

Links https://minerclass.github.io/tokens.css before the page styles and points this
page's ground, ink, and rules at the shared tokens while keeping its own accents. The
page's ground is unchanged: a dark page stays dark.

**Every reference carries a fallback** equal to the pre-adoption value, because a bare
`var(--mjm-bg)` is invalid at computed-value time if the token file fails to load, which
would break the page rather than leave it unchanged.

**Watch the token names on this page.** They are inverted relative to the rest of the ecosystem: `--ink` is the BACKGROUND and `--paper` is the TEXT. They map to `--mjm-bg` and `--mjm-ink` respectively. Mapping them by name alone would have inverted the page.

**Verified in a real browser.** Token sheet loads; body renders dark with a contrast ratio
of 16.02; tag balance clean; zero console errors.

---

## 2026-07-22 - Weekly Pages review, accessibility and CI repair

Agent: Claude Opus 4.8 (Claude Code), working from a weekly review of the
`minerclass` GitHub Pages ecosystem against recent academic and professional
activity. Author present and approving changes.

### Changes in this repository

The June 11 DuPage ROE keynote was still labelled "Featured current conference
session" six weeks after it happened. Restructured the hero:

- The hero now promotes the next scheduled engagement, an invited doctoral
  session on AI and ethics on 2026-08-04.
- DuPage moved to a dated "Most recent conference session" line directly below,
  keeping its link. It remains in the archive list unchanged.
- Added `.featured-recent` styling; `.featured` bottom margin reduced from 110px
  to 28px so the two blocks read as a pair.

Note on naming: the August session is described by institution and course
subject only. The instructor is the author's dissertation chair, and the
ecosystem convention (see `AGENTS.md` in sibling dissertation repositories) is
that committee and faculty names are not published. Keep it that way when this
entry is next updated.

### Not added, and why

Two August 2026 conferences were considered for the hero and deliberately left
out, because the author's speaking status at each could not be confirmed:

- Civics of Technology 5th Annual Conference, August 6-7 2026. The author is a
  newsletter subscriber and the `technoskepticism-primer` site builds on CoT's
  five technoskeptical questions, but no accepted session was verified. The
  author is **not** among the three 2026 CoT Public Scholarship Award
  recipients; do not imply otherwise.
- Serious Play Conference at Duke, early August 2026. Attendance appears likely
  from correspondence; speaking status was not verified.

Confirm before publishing either. Do not list an unconfirmed session.

### Note for future agents

The root hub at `minerclass.github.io` renders its project grid from JavaScript.
Fetching its HTML and scanning for `href` values will miss almost every project
link and produce a false "orphaned sites" result. Inspect the rendered DOM.

### Cross-repository context

This change set spans five repositories: `pedagogical-friction`,
`diss-proposal-defense`, `dissertationquestionsbeta`, `conference-presentations`,
and `interactive-resume-2026`. Each carries its own `AGENT_LOG.md` entry for the
same date. Check the siblings before assuming a change was isolated.
