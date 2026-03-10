# AI Knowledge Management System

## The Big Picture

Think of it like a **professional kitchen**:
- The **template** is the recipe book — the standard
- The **raw** folder is the prep table — ingredients dumped and roughly sorted
- The **processed** folder is the finished plate — the AI-cooked result
- The **skills** folder is the chef's training manual — rules the AI follows

---

## Folder Tree

```
ai-workspace/
│
├── _template/                        ← The master blueprint (never touch this)
│   ├── folder-structure.md           ← Required folders and what goes in each
│   ├── naming-conventions.md         ← How to name files (dates, prefixes, etc.)
│   ├── output-examples/              ← Example of what a perfect finished result looks like
│   │   ├── example-report.pdf
│   │   └── example-summary.docx
│   └── quality-checklist.md          ← What "done" looks like
│
├── _skills/                          ← AI instruction manuals (rules it reads before working)
│   ├── rule-01-how-to-handle-vocal.md     ← Transcribe, clean filler words, tag speakers...
│   ├── rule-02-how-to-handle-paper.md     ← OCR, correct scan errors, extract key data...
│   ├── rule-03-how-to-handle-text.md      ← Email/chat cleanup, extract action items...
│   ├── rule-04-how-to-summarize.md        ← Tone, length, structure of summaries
│   └── rule-05-output-formatting.md       ← Font, headers, language (FR/EN), export format
│
├── clients/
│   │
│   ├── dupont-sa/
│   │   ├── raw/                      ← Dump everything here, roughly sorted
│   │   │   ├── vocal/                ← Voice memos, meeting recordings (.mp3, .m4a)
│   │   │   ├── text/                 ← Emails, chat exports, notes (.txt, .docx)
│   │   │   ├── paper/                ← Scanned documents (.pdf, .jpg)
│   │   │   └── other/                ← Anything that doesn't fit above
│   │   │
│   │   └── processed/                ← AI output, ready to deliver
│   │       ├── summaries/
│   │       ├── reports/
│   │       └── action-items/
│   │
│   └── martin-consulting/
│       ├── raw/
│       │   ├── vocal/
│       │   ├── text/
│       │   ├── paper/
│       │   └── other/
│       └── processed/
│           ├── summaries/
│           ├── reports/
│           └── action-items/
```

---

## Do you need the `_skills` folder?

**Yes, absolutely** — and it's actually the most important part.

Without rules, AI produces inconsistent results. The skills folder is what makes the system **repeatable and professional**. Think of it as onboarding a new employee: you don't just hand them files and hope for the best — you give them a procedure manual.

Key rules to write from day one:

| Rule file | What it solves |
|---|---|
| `rule-01-how-to-handle-vocal` | How to transcribe recordings, handle crosstalk, identify speakers |
| `rule-02-how-to-handle-paper` | How to read scanned docs, what to ignore (headers/footers), what to extract |
| `rule-03-how-to-summarize` | Length, tone (formal/casual), language, what to always include |
| `rule-04-output-formatting` | File naming, folder placement, export format (PDF vs Word) |

---

## How it flows

```
[Client meeting / site visit]
        ↓
  raw/ ← team dumps everything (voice memo, photo of whiteboard, email thread)
        ↓
  AI reads _skills/ rules + _template/ blueprint
        ↓
  processed/ ← clean summaries, reports, action items ready to send
```

The team only needs to do step 1. Everything else is the AI's job.

---

## Notes

- Adding a new client = just create a new folder under `clients/`
- Rules and template stay the same → consistent quality across all clients
- The `_` prefix on `_template/` and `_skills/` keeps them at the top of the file browser and signals "system files — don't touch"
