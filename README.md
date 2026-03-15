Ramanuja Vidya – Content Repository

This repository contains the structured lesson content used by the Ramanuja Vidya learning platform.

The repository is dedicated to content management only. All lessons are stored in JSON format so they can be easily consumed by the application frontend.

The goal is to maintain a clean, structured, and scalable content system for traditional Śrī Vaiṣṇava learning materials.

Purpose

This repository manages:

Lesson metadata

Chapter structure

Titles and descriptions

Multilingual content (Tamil / English)

Logical ordering of lessons

The Flutter application reads these JSON files and renders the lessons inside the app.

Content Structure

Each subject follows a consistent structure:

One index.json file to define the list and order of chapters

Individual chapter JSON files for each lesson

Example:

content/
│
├── sribhashyam/
│   ├── index.json
│   ├── sb_saaram_01.json
│   ├── sb_saaram_02.json
│   └── ...
│
├── thiruvaimozhi_saaram/
│   ├── index.json
│   ├── tvs_01.json
│   ├── tvs_02.json
│   └── ...
│
├── tmk/
│   ├── index.json
│   ├── tmk_01.json
│   ├── tmk_02.json
│   └── ...
File Roles
index.json

The index.json file acts as the table of contents for the lesson series.

It defines:

Lesson order

Chapter IDs

Titles

Basic metadata

Example:

{
  "series": "sribhashyam_saaram",
  "chapters": [
    "sb_saaram_01",
    "sb_saaram_02",
    "sb_saaram_03"
  ]
}
Chapter Files

Each chapter file contains the actual lesson content.

Example:

sb_saaram_01.json
sb_saaram_02.json

Typical structure:

{
  "id": "sb_saaram_01",
  "type": "default",
  "title": {
    "en": "Introduction to the Inquiry into Brahman",
    "ta": "பிரம்மத்தை அறிய தொடக்கம்"
  },
  "description": "...",
  "content": [...]
}
Naming Convention

To keep the repository organized, follow these rules:

Series prefix	Example
Sri Bhashyam Saaram	sb_saaram_01.json
Thiruvaimozhi Saaram	tvs_01.json
TMK	tmk_01.json

Rules:

Use lowercase

Use underscores _

Number lessons sequentially

Editing Guidelines

When editing content:

Do not change existing chapter IDs

Maintain consistent JSON formatting

Ensure valid JSON syntax

Update index.json when adding new chapters

Keep translations aligned between languages

Used By

This repository is consumed by the Ramanuja Vidya mobile application, which renders the structured lessons for learners.
