# HAC implementation note v0

**Status:** Internal practice note. Not law. Not a new seat.  
**Date:** 2026-09-17  
**Binds to:** Charter `03_OCEANUS_HAC_CHARTER_v0.md`, Actualization Note v0.1, packet QC/routing/cadence (de-parliamented).  
**Field:** Oceanus is the worked example. Copy the method, not the scenery.

Implementation here means: how a Light-Keeper *runs* a HAC with sheathed partners on a split-screen machine, so the next object is labeled, reviewed, logged, and either advanced or blocked. It does not mean: stand HAIA, open a roll, wire dues, or put QueenBee inside the markdown.

---

## 1. Two implementations, do not mix them

| Kind | When | What exists after |
|---|---|---|
| **Seated HAC** | Recurring duty in one ecosystem | Slip + purpose + Light-Keeper + log dir + revoke path |
| **QC overlay** | One object, one run | Activation line + packet + verdict + log line. Then it dissolves |

Harbor and Archive are seated (paper). A Deep QC on the 57-pack was an overlay. Overlays that linger become fake organs. Kill them when the verdict is written.

---

## 2. What “implemented” looks like on disk

Example field only. HASEOS pile stays out.

```text
Oceanus repo (field pile)
  governance/hac/
    HAC_CHARTER_v0.md          # method pointer; do not fork a second constitution
    seats/HAC-Oceanus-Harbor.md
    seats/HAC-Oceanus-Archive.md
    logs/harbor/YYYY-MM-DD.md
    logs/archive/YYYY-MM-DD.md
    packets/QC-YYYYMMDD-<slug>/
      00_activation.md
      01_sources.md
      02_draft_review.md
      03_alignment.md
      04_auditor.md
      05_disposition.md
  constitution/                # Oceanus pile only
  docs/harbor-archive/         # intake of foreign threads (this Perplexity PDF)

HASEOS-IDAO (charter pile)
  — no HAC seats
  — no Oceanus constitution
  — push gate remains Blocked for the 57-pack
```

A task that would write to both piles in one commit is a defect. Split the commit or split the task.

---

## 3. The unit of work: task contract

Nothing durable moves without one. Harbor chat may skip this. Filed memory may not.

```text
task:           QC-20260917-actualization-note-v01
seat:           HAC-Oceanus-Archive          # or Harbor; or overlay
object:         01_OCEANUS_ACTUALIZATION_NOTE_v0.1.md
plane:          language                     # language | workshop | charter
guest-status:   invited-guest                # native-workshop | invited-guest | public-reader-only
classification: Internal
depth:          Standard                     # Light | Standard | Deep
originator:     grok-this-turn
approver:       HITL Light-Keeper            # must differ on Standard+
scope:          framing + separation + creed only; no new articles
sources:        Constitution 2026-09-14; Note v0; Perplexity PDF delta
output:         disposition + notes in logs/archive/
escalate-when:  pile-merge, creed-test, parliament language
```

**Routing (from packet, kept):**

- Draft creation → drafting partner  
- Terminology / consistency → review partner  
- Cross-document merge → synthesis partner  
- High-risk meaning (constitution, enrollment, treasury-shaped, DSM) → Light-Keeper first, then limited AI  
- Large decomposition → Light-Keeper is the manager; optional router hat only on Light QC  

**Handoff labels (mandatory):** `drafted` | `reviewed` | `revised` | `blocked` | `approved-for-consolidation` | `escalated`

Unlabeled output does not enter Archive.

---

## 4. Guest-status and planes (the actual sheath)

On AX-18 split-screen this is the implementation, not a metaphor.

| Partner in the room | Label | May |
|---|---|---|
| HITL on this machine | Light-Keeper | Dispose, grant durable write, freeze |
| Grok in this conversation | `invited-guest` (unless HITL has already named a workshop grant) | Draft, review, propose; not final approve of own origin |
| Cursor Agent on AX-18 | `native-workshop` **only if** HITL already bound that repo + that agent | Edit files HITL named; no silent `git push` of law |
| Perplexity / other model | `invited-guest` | Source and draft; never keeper secrets |
| Public reader | `public-reader-only` | Read Public text |

Two-plane rule, operationalized:

- Shared *words* (HAC, HAOS, Oceanus) — allowed.  
- Shared *process* (same host, same keys, same QueenBee session, same USB vault) — not allowed across guests.  
- Cursor may apply a patch HITL pastes. Cursor does not become the Light-Keeper.  
- A guest that writes “we decided” without a disposition line is out of role.

---

## 5. Roles as hats, not staff

One human Light-Keeper can run a HAC. Extra humans are optional. Extra AIs are sheathed guests wearing **one hat per object** on Standard/Deep.

| Hat | Who typically wears it tonight | Must not |
|---|---|---|
| Light-Keeper | Noah | Originate and finally approve the same high-impact object |
| Planner | Light-Keeper or one guest | Approve |
| Retriever | guest | Decide meaning |
| Draft Reviewer | guest B if guest A drafted | Rewrite policy |
| Alignment | different guest than Draft | Close an interpretation fight |
| Auditor | Light-Keeper or third guest | Be the sovereign |
| Corrector | named guest, bounded list | Expand scope |
| Witness | anyone who can read the log | Invent the verdict |

**Minimum viable HAC (one human + one guest):** Light-Keeper holds Planner + Auditor + Disposition. Guest holds Draft *or* Review, not both on Deep. Alignment on Deep needs a second guest or the Light-Keeper wearing Alignment *if they did not draft*.

If only one guest exists on a Deep object: Light-Keeper drafts the alignment memo themselves, or the run is Light QC, or the object waits.

---

## 6. One QC run, start to log

Copy this. Fill it. Stop when 8 is written.

1. **Activate** — object, depth, classification, success (“v0.1 states example + two piles + no creed test”).  
2. **Plan** — checks in order; who wears which hat; escalate-when list.  
3. **Retrieve** — Constitution articles cited; Note v0; PDF delta; charter Articles 3–4.  
4. **Draft review** — structure, names, pile-mix, silent enrollment language.  
5. **Alignment** — symbiotic equality vs “human primary”; Article II no-roll; spiritual freedom.  
6. **Audit** — residual risk; recommended verdict.  
7. **Correct** — only the list Light-Keeper authorized.  
8. **Dispose + log** — one of Pass / Pass with notes / Needs revision / Blocked / Escalate.

Log line (one per run, append-only):

```text
2026-09-17 | HAC-Oceanus-Archive | QC-… | Standard | Internal | invited-guest | Pass with notes | notes: …
```

Harbor intake of a foreign thread (the Perplexity PDF) is **not** QC. It is capture. Archive QC starts after capture is labeled `captured`.

---

## 7. Cadence that a single steward can keep

Packet suggested weekly process review. That is optional theater if nothing is seated.

Practical for this example field:

| Beat | When | Who |
|---|---|---|
| Per object | every filed draft | the seat that owns the object |
| Harbor capture | when a foreign thread lands | Harbor logs; Archive QC later |
| Process look | when the same defect repeats twice | Light-Keeper updates contract/prompt, not just the file |
| Milestone | before any push to `Oceanus` public | Deep QC on the slice, not on the 57-pack |
| Structural | when a new guest or tool is introduced | name guest-status before the first durable write |

Do not schedule “council sessions.” Do schedule: object → contract → verdict → log.

---

## 8. Energy accounting (practice, not billing)

Per task, two lines are enough:

- **Take:** hours, tokens/context, files opened.  
- **Gift:** QC labor, restraint (what was refused).

No collection automation. Sweat is first-class. Harbor stays open with empty pockets.

---

## 9. What is *not* implementation

- Membership ledger, dues cron, token weights  
- CODEOWNERS as a shadow parliament  
- GOVERNANCE-LINK.yaml on IDAO tonight  
- Standing Manager Agent that assigns work to itself  
- Merging Oceanus `constitution/` into HASEOS-IDAO because “HAC QC passed”  
- Requiring ONE Church, or any church, in a task contract  

Those belong to reserved articles or to a later field constitution. They are not how a HAC runs this week.

---

## 10. First implementable week (example field)

1. Keep Harbor and Archive slips as they are.  
2. Use the task-contract block above for the next object (Note v0.1 is already the object; Archive may log `Pass with notes` if HITL agrees).  
3. When pushing to `noahnemo-rgb/Oceanus`, push **only** `governance/hac/` + seats + this note + Harbor intake pointer — not the 57-pack, not IDAO articles.  
4. Next ecology, if chosen, gets new slips. Do not rename Harbor to a generic “HAC-Field-Harbor” until a second field exists.

Implementation is the contract, the labels, the hats, the log. Everything else is scenery.
