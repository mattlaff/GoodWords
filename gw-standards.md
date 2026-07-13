# GoodWords Standards

## Purpose

GoodWords is a kind of digital commonplace book: a personal library of poems, quotations, and brief reflections, with a public reading room. The goal is not simply to archive texts, but to curate lightly and think publicly about why the texts are important to me.

Preferences: simplicity, readability, long-term maintainability

---

# File Naming

## General

- Use all lowercase.
- Separate words with hyphens
- Do not use spaces.
- Do not use underscores.
- Do not include punctuation.
- Filenames should be descriptive enough to identify the work without opening the file.

### Poems

Use: [author's last name]-[poem's title].md

Examples:
- levertov-witness.md
- rile-go-to-the-limits-of-your-longing.md

### Quotes

Use: [author's last name]-[first 3-5 words of quote].md

The filename is for organization, not presentation. It does not need to contain the entire quotation.

---

# Front Matter

## Poems

```toml
+++
title = ''
author = ''
date_added = '{{ .Date | time.Format "2006-01-02" }}'
date_updated = '{{ .Date | time.Format "2006-01-02" }}'
draft = true
has_reflection = false
+++
```

Poems do **not** use categories.


## Quotes

```toml
+++
title = ''
author = ''
category = ''
date_added = '{{ .Date | time.Format "2006-01-02" }}'
date_updated = '{{ .Date | time.Format "2006-01-02" }}'
draft = true
has_reflection = false
+++
```

Allowed categories:

- beauty
- love
- mystery
- presence
- truth

---

# Dates

Dates use ISO format: YYYY-MM-DD

## date_added

The date the entry was first added to the GoodWords library (does not change).

## date_updated

The date the entry was last meaningfully updated.

Dates are **not** intended to be displayed on individual poem or quote pages.

---

# Reflections

Entries do not require reflections when first added.

When a reflection is added:

1. Set: has_reflection = true
2. Update: date_updated = 'YYYY-MM-DD'
3. Add a Reflection section beneath the poem or quote:

```
## Reflection

Reflection text...
```

---

# Drafts

New entries: draft = true

When the entry is ready to appear publicly: draft=false

---

# Author Names

Use normal display order: [First] [Last]

---

# Content Philosophy

GoodWords is intended to function as a living commonplace book rather than a blog.

Content is divided into two collections:

- Poems
- Quotes

Although both belong to the same library, they remain distinct collections with different browsing experiences.

Poems are organized primarily by author.

Quotes are organized by both author and one of five categories.

---

# Public Website Philosophy

The public site should feel less like a news feed and more like entering a quiet reading room.

Priority is given to discovery rather than chronology.

Potential navigation includes:

- Featured Selection
- Random Poem
- Random Quote
- Browse Poetry
- Browse Quotes
- Recently Added
- Recently Updated

Dates should remain behind the scenes. The emphasis should be on the works themselves rather than when they were added.

---

# Repository Philosophy

The repository is the library.

The website is the reading room.

Repository files should remain pleasant to read, easy to browse, and understandable years from now.

Ideals:
- Clarity
- Readability
- Stability

Future design decisions should align with these principles. Conflicts should be resolved by choosing the option that best supports the long-term experience of maintaining a curated personal library.

---

# Future Ideas

Ideas that have not yet been adopted as standards.

- Related GoodWords links between entries.
- Recently reflected upon page.
- Recently added page.
- Featured selection.
- Random poem.
- Random quote.
- Personal reading lists.