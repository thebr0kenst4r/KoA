# CONTRIBUTING.md

# King of Avalon Guide Book

Contributor Guide

---

## Purpose

This project aims to create the definitive offline King of Avalon Guide Book.

The focus is accuracy, maintainability, and consistency—not flashy code.

When in doubt, choose the simplest solution.

---

# Project Structure

```
/
│
├── index.html
│
├── data/
│     guide-library.js
│
├── guides/
│     template-guide.html
│     under-construction.html
│     *.html
│
└── CONTRIBUTING.md
```

---

# Guide Library

All guide entries are stored in:

```
data/guide-library.js
```

Do **NOT** place guide entries inside `index.html`.

The guide library is the single source of truth.

---

# Guide Entry Format

```
{
    title:"Guide Title",

    keywords:"search keywords",

    file:"guides/guide-file.html",

    status:"draft"
},
```

Status values:

```
complete
draft
planned
```

---

# Visibility

```
const SHOW_UNFINISHED = false;
```

false

Only completed guides appear.

true

Draft and planned guides are also visible.

---

# Categories

Current category structure:

1. Getting Started
2. Kingdom Development
3. Heroes
4. Dragons
5. Combat
6. Alliance
7. Events
8. Kingdom vs Kingdom
9. Fae Realm
10. Reference

Do not create additional categories unless discussed by the team.

---

# Guide Philosophy

One guide = One topic.

Do **NOT** create separate Solar and Lunar guides.

Realm-specific information belongs inside a single guide using the Guide Engine.

Example:

Portal Guide

✓ Solar content

✓ Universal content

✓ Lunar content

---

# File Naming

Guide files use:

- lowercase
- hyphens
- html extension

Examples

```
building-progression.html

hero-development.html

portal-guide.html

battle-formations.html
```

Do not use spaces.

Do not use underscores.

---

# Creating a New Guide

1. Copy

```
guides/template-guide.html
```

2. Rename the file.

3. Write the guide.

4. Update

```
guide-library.js
```

Replace

```
guides/under-construction.html
```

with the new filename.

Change

```
status:"draft"
```

to

```
status:"complete"
```

---

# Realm Support

All guides must support the Guide Engine.

Use the existing CSS classes:

```
solar

universal

lunar
```

The Guide Engine automatically displays the correct content based on the selected realm.

---

# Coding Style

Keep code readable.

Prefer whitespace over compact code.

Leave helpful comments.

Avoid unnecessary complexity.

---

# Category Headers

Each category begins with:

```
/**********************************************************************
CATEGORY NAME

Purpose:

Category Maintainer:

Contributing Mods:

**********************************************************************/
```

Please update contributor names when appropriate.

---

# Design Credit

Guide Engine

Author & Design Credit

K10651.The Winged Cradler.AMod

Please preserve authorship comments in all engine files.

---

# Future Ideas

These items are intentionally deferred until after the core guide library is complete.

- Favorites
- Recently Viewed Guides
- Advanced Search Filters
- Guide Statistics
- Related Guide Automation
- Theme Improvements
- Additional Navigation Enhancements

The current priority is completing the guide library and guide content.