# Four-Beat Checker

[![Downloads](https://img.shields.io/github/downloads/kaungyemarn96/four-beat-checker/total?label=downloads&color=2f6f4e)](https://github.com/kaungyemarn96/four-beat-checker/releases/latest)
[![Latest release](https://img.shields.io/github/v/release/kaungyemarn96/four-beat-checker?label=release&color=2f6f4e)](https://github.com/kaungyemarn96/four-beat-checker/releases/latest)

A free, complete Claude Skill. It reads a guide or how-to draft and tells you
whether it has the shape a guide needs — and if not, which single fix would do
the most.

It does one narrow thing. It does not rewrite your draft, propose hooks, or
edit your voice.

**Version 1.0.0 · Knowledge base current as of August 2026 · Free, no expiry**

---

Source: [github.com/kaungyemarn96/four-beat-checker](https://github.com/kaungyemarn96/four-beat-checker)

## Install

1. Download or clone this directory.
2. Upload it to your Claude workspace as a skill (Settings → Capabilities →
   Skills → Upload, or drop the folder into `.claude/skills/` in a project).
3. Ask for a structure check on a draft.

That is the whole install. Filling in `client/voice-profile.md` is optional and
only matters if you later ask it to draft replacement copy.

## Use it

> Run a four-beat check on this draft.

You get back a table of the four beats with a grade and the line that carries
each one, then two or three sentences naming one fix, then a verdict: **ship**,
**one fix first**, or **restructure**.

If you disagree with a grade, say so — it will pull up worked examples and
argue the case, or concede it.

## What the four beats are

1. **Wrong question** — the assumption the reader arrived with, corrected.
2. **Escape hatch** — the real mechanism the better question leads to.
3. **Who actually uses it** — named people, traceable numbers, in prose.
4. **Your turn** — what the reader does now, concretely.

Order matters as much as presence. A draft with all four in the wrong order
fails differently from one missing a beat, and the fix is not the same.

## What is in the box

```
four-beat-checker/
├── SKILL.md                     The orchestration — read every time
├── skill-manifest.json          Version, dates, changelog
├── LICENCE.md
├── knowledge-base/              Reference — loaded only when needed
│   ├── four-beats.md            Diagnosis questions and failure patterns
│   └── worked-examples.md       A pass, a fail with its fix, an order failure
└── client/                      Yours — blank, and never overwritten
    └── voice-profile.md
```

**Those three directories are the point**, and they are the same architecture as
every package I build.

`SKILL.md` is read on every invocation, so it holds only what is always true.
`knowledge-base/` holds the long reference material and is loaded *conditionally* —
the failure patterns only when a beat is actually weak, the worked examples only
when you push back. `client/` is the part that differs per company; it ships
blank, you fill it in, and an update replaces the first two directories without
touching it.

Loading everything on every run is the failure this structure exists to prevent.
It triples the cost of a routine check and buries the rules that decide the
verdict under material you did not need. Knowing which file to load, and which
not to, is the engineering — not the length of the prompt.

## Why this exists

It is a working sample. If it is useful, the same method scales to a full
editorial system: a workflow catalog, a router deciding where any new
instruction goes, rule files that load conditionally, and a paper trail of what
changed and why. That is described at
[kaungyemarn.vercel.app/products/guide](https://kaungyemarn.vercel.app/products/guide).

No signup, no email capture, no upsell inside the skill. If you never speak to
me and just use it, that is a fine outcome.

## Limits worth knowing

- **It grades structure, not writing.** A flat draft with four solid beats
  passes, and it will say so.
- **It will not invent the missing beat.** Naming what is absent and writing it
  are different jobs.
- **It is a judgement, not a fact.** Overrule it when you have a reason.
- **News roundups, comparisons and listicles are a different shape.** It says so
  and stops rather than forcing the check.

## Licence

Free to use and modify inside your company. Not to resell or offer as a service.
Full terms in [LICENCE.md](LICENCE.md).

Built by [Kaung Ye Marn](https://kaungyemarn.vercel.app).
