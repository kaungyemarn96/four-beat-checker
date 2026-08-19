---
name: four-beat-checker
description: Diagnoses whether a guide or how-to draft actually has the four-beat structure — wrong question, escape hatch, who uses it, your turn — and names the one fix that would do the most. Use when reviewing a draft's structure, when a piece "reads flat" without an obvious cause, or before publishing long-form explanatory content.
---

# Four-Beat Checker

Diagnostic only. This does not rewrite the piece, propose hooks, or edit voice.
It answers one question: **does this draft have the shape a guide needs, and if
not, which beat is missing?**

## When to run

Guides, how-tos, and pieces that mean to change what a reader does.

**Not every well-argued piece is one of those.** News roundups, comparisons,
listicles, and commentary or analysis are different shapes, and forcing this
check on them produces a failing grade for a piece that is working. Say which
shape you think it is and stop, rather than reporting three missing beats.

The distinction that matters: a guide exists to change what the reader does, and
commentary exists to change what the reader thinks. If the piece never intended
to hand over an action, its lack of one is not a fault. Ask before grading, when
it is genuinely unclear.

## The four beats

1. **Wrong question** — the assumption the reader arrived with, named and shown
   to be the wrong thing to be asking.
2. **Escape hatch** — the real mechanism, tool, or move that the better question
   leads to.
3. **Who actually uses it** — real people, real numbers, woven into prose.
4. **Your turn** — what the reader does now, concretely enough to start today.

Order matters. A draft with all four in the wrong order fails differently from
one missing a beat, and the fix is not the same.

## Procedure

Work through this in order. Do not skip to the verdict.

1. **Read the whole draft once before judging anything.** A beat often lives in
   a different section than its heading suggests.
2. **For each beat, quote the line that carries it.** If you cannot quote a
   line, the beat is missing — not weak. That distinction drives the fix.
3. **Grade each beat** as `present`, `weak`, or `missing`:
   - `present` — a reader would take the point without being told to.
   - `weak` — the beat is gestured at but a reader could miss it.
   - `missing` — no line carries it.
4. **Check the order.** Note any beat that appears before the one that should
   set it up.
5. **Name one fix.** The single change that would do the most, not a list. If
   two beats are missing, the earlier one is nearly always the cause of the
   later one looking thin — fix that first and re-check.

## Output

Keep it short. A table of the four beats with grade and quoted evidence, then
two or three sentences on the one fix. No rewrite unless asked, and no praise
padding.

State the verdict plainly: **ship**, **one fix first**, or **restructure**.

## Loading rules

These are the point of the package. Read them before reaching for a file.

| File | Load when |
|---|---|
| `knowledge-base/four-beats.md` | Any beat is graded `weak` or `missing` — it carries the diagnosis questions and the failure patterns for each beat. Not needed when everything is `present`. |
| `knowledge-base/worked-examples.md` | You need to show what a fixed version looks like, or the author disputes a grade. Never on a first pass. |
| `client/voice-profile.md` | Only if asked to draft replacement copy. The check itself is voice-agnostic. |

Loading everything on every run is the failure this structure exists to
prevent: it triples the cost of a routine check and buries the rules that
actually decide the verdict.

## Boundaries

- Do not grade the writing. Flat prose with four solid beats gets a passing
  structural verdict, and says so.
- Do not invent the missing beat. Name what is absent; writing it is separate
  work with a different brief.
- One quote per beat. Quoting three lines to prove a beat exists means it does
  not.
- A piece ending on tension rather than a summary has not thereby failed beat 4.
  Check whether an action is present anywhere in the close before grading it.
