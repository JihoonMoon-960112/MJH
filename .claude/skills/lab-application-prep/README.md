# lab-application-prep

A Claude Code skill for preparing an academic application to one specific lab:
recruiter/PI correspondence, a cover letter, and a night-before interview brief
published as an HTML artifact.

## Using it in another session

**In this repository** — nothing to do. Any Claude Code session with `JihoonMoon-960112/MJH`
checked out picks the skill up from `.claude/skills/`. Invoke with `/lab-application-prep`,
or just describe the task ("I'm interviewing with Prof. X next week") and it triggers on
its own.

**In any session, anywhere** — install it to the user-level skills directory:

```bash
mkdir -p ~/.claude/skills
cp -r /path/to/MJH/.claude/skills/lab-application-prep ~/.claude/skills/
```

Or, without a local clone of this repo:

```bash
mkdir -p ~/.claude/skills && cd ~/.claude/skills
git clone --depth 1 --filter=blob:none --sparse \
  https://github.com/JihoonMoon-960112/MJH.git _mjh
cd _mjh && git sparse-checkout set .claude/skills/lab-application-prep
mv .claude/skills/lab-application-prep ../ && cd .. && rm -rf _mjh
```

Note that cloud sessions are ephemeral — `~/.claude/skills` does not survive the
container. For cloud sessions, keeping the skill in the repo is the durable route.

## What is in it

| File | Holds |
|---|---|
| `SKILL.md` | The workflow, and the one rule that overrides everything |
| `references/01-sourcing.md` | Getting full text — Europe PMC, BioC, preprint rate limits, PDFs, talk captions |
| `references/02-gap-analysis.md` | Wants / Cannot / Unproven / Fit, and the textual tells for each |
| `references/03-brief-structure.md` | Brief section order, source grading, layout constraints |
| `references/04-correspondence.md` | Register, time zones, missed meetings, the recommendation-letter conversation |
| `references/05-candidate-profile.md` | Authorship accuracy, competence vs. tools, the background statement |

## The rule

The skill forbids proposing that the candidate's own prior tool or system be applied to
the target lab's research. If the connection is real, the PI draws it themselves — and
then it is their idea, which is worth more.
