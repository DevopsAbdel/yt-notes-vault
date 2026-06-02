# 🧠 yt-notes-vault

An immutable, text-based knowledge repository for archiving highly structured insights, concepts, and technical summaries from YouTube videos. 

This repository serves as a permanent local-first brain, transforming passive media consumption into a searchable, atomic, and structured knowledge asset.

---

## 📂 Repository Architecture

The vault is organized using a flat category system to keep file paths predictable, highly scannable, and fully compatible with markdown-based knowledge engines.

```text
yt-notes-vault/
│
├── 00-Templates/               # Core templates for uniform note creation
│   └── youtube-note-template.md
│
├── 01-Inbox/                   # Raw captures, scratchpads, and unreviewed notes
│
├── Tech-Infrastructure/        # System admin, infrastructure, and virtualization
├── Business-Automation/        # Scripts, automation workflows, and business systems
├── Accounting-Finance/         # Professional training, frameworks, and core concepts
│
├── README.md                   # Repository documentation and protocols
└── .gitignore                  # Local environment and editor exclusion rules
```

---

## 🛠 Note Capture Protocol

To maintain maximum consistency and ensure the vault remains programmatically parsable, every note must adhere to the following standard structure.

### 1. File Naming Convention
Files must be named using the following pattern to ensure alphabetical sorting and prevent collisions:
`[Channel Name] - [Clean Video Title].md`

*   *Good:* `NetworkChuck - Docker Containers Explained Simply.md`
*   *Bad:* `docker notes from network chuck video.md`

### 2. Mandatory Note Anatomy
Every new file should be instantiated using the core template found in `00-Templates/`. It must contain structured YAML frontmatter for metadata tracking and deep-linked markdown timestamps for context preservation.

```yaml
---
title: "Video Title As Written"
channel: "Channel Name"
video_url: "https://www.youtube.com/watch?v=..."
category: "Sub-Folder-Name"
tags: [tag1, tag2]
captured_date: 2026-06-02
status: "Inbox | Reviewed"
---

# Video Title As Written

## 🎯 High-Level Overview
A 2-3 sentence summary explaining exactly what this video covers and its practical utility.

## 🔑 Key Takeaways & Timestamps
* [00:03:15](https://youtu.be/EXAMPLE?t=195) — Core concept or architecture map explained.
* [00:12:45](https://youtu.be/EXAMPLE?t=765) — Specific execution step, code fragment, or strategy.

## 📝 Detailed Insights & Code
Use this section for diagrams, code snippets, step-by-step procedures, or explicit concept breakdowns.
```

---

## 🚀 Workflow & Sync Automation

### Working Locally
Because this vault is entirely built on local-first raw text, it is fully compatible with open knowledge tools:
*   **Local Editor Graph Integration:** Perfect for opening directly as an isolated workspace or vault in apps like Obsidian.
*   **Side-by-Side Playback:** Utilize markdown plugins (like *Media Extended* or *Media Notes*) to anchor the YouTube player directly alongside your active workspace text pane.

### Daily Sync Script
To ensure local captures are backed up safely without manual Git overhead, run the local sync protocol:
```bash
git add .
git commit -m "sync: update vault insights $(date +'%Y-%m-%d')"
git push origin main
```

---
> **System Rule:** Keep notes concise, emphasize actionable code snippets or direct frameworks, and always link back to the source timestamp. Passive watching gets forgotten; structured tracking remains permanent.
