# Mahabharata Illustrated Edition — Volume 1 Image Production Spec

This document is a GitHub-ready production specification for the **illustrated Bengali Mahabharata reader**.
It consolidates the visual direction, quality rules, chapter-image system, character-continuity requirements, app-integration structure, file naming, and the **master illustration prompts for all 199 chapters of Volume 1**.

---

## Project Goal

Build a high-quality, publication-oriented, fully illustrated **Mahabharata Volume 1** reading experience where:

- every chapter can have a dedicated hero image,
- every parva can have a dedicated cover image,
- recurring characters remain visually consistent,
- images remain extractable/downloadable from the app,
- filenames clearly identify the source location,
- the illustrated system can scale chapter by chapter and volume by volume.

---

## Core Visual Direction

### Style

- **Cinematic painterly-realistic ancient Indian epic**
- visually rich but readable for app use
- historically inspired classical Indian setting
- warm, elegant, mythic atmosphere
- high-detail textiles, ornaments, weapons, architecture and landscapes
- dramatic but controlled lighting
- no modern objects, no modern clothing, no random fantasy drift

### Output Defaults

- **Primary aspect ratio:** 16:9 landscape for chapter hero images and parva covers
- **No text inside image** unless explicitly needed for UI mockups
- **Offline-app friendly** assets
- **Consistent visual language** across all images

### Tone

- dignified, epic, literary, emotionally expressive
- suitable for a high-quality Bengali illustrated edition
- avoid cartoonish, low-detail, or generic fantasy imagery

---

## Non-Negotiable Character Continuity Rules

1. If a recurring character already has an approved design, **do not redesign casually**.
2. Maintain consistency in:
   - facial structure
   - skin tone
   - body type
   - hair style
   - age band / maturity stage
   - costume identity
   - ornaments and signature props
   - weapons / tools
3. A character may age or change contextually, but must remain recognizably the same person.
4. New characters must be created only when needed by the story.
5. A new recurring character should ideally be introduced through a **character card / bible entry** before being reused repeatedly in chapter illustrations.

---

## Illustration Types

### 1. Parva Cover
Use one strong, iconic scene or symbolic tableau for the whole parva.

### 2. Chapter Hero Image
A single visually clear hero illustration placed before the chapter text.

### 3. Character Card / Character Bible Entry
A character portrait/reference asset used to preserve continuity.

### 4. Optional Supporting Visuals
Use only when needed:
- family tree support art
- object / ritual illustration
- place establishing shot
- battle composition
- ceremonial scene

---

## Chapter Image Quality Standard

Every chapter illustration should:

- accurately reflect the chapter's actual content
- privilege the chapter's **main event or emotional pivot**
- include only the relevant characters
- avoid stuffing too many disconnected incidents into a single frame
- preserve visual clarity on desktop and mobile screens
- support the reader before they enter the full text
- align with the chapter's "অধ্যায়ের প্রেক্ষাপট" / context note

### Preferred Composition Logic

- one dominant subject or event
- one clear emotional center
- secondary figures only if narratively necessary
- background should support story, not distract from it

---

## App Integration Requirements

The app should keep the illustrations **embedded and downloadable**.

### Required App Behaviors

- parva cover displayed in parva list and parva page
- chapter hero image displayed before chapter text
- character gallery / atlas visible in a dedicated section
- chapter page lists associated characters
- each available image has a save / download option
- image names should identify source location clearly
- unfinished images must be visibly marked as planned / pending

---

## File Naming Convention

Use this structure:

`V01_P07_CH094_Bhishma_Vow.webp`

Where:
- `V01` = Volume 1
- `P07` = Parva 7
- `CH094` = Chapter 94
- remaining text = concise English scene label

### Other asset patterns

- `V01_P07_Sambhava_COVER.webp`
- `V01_CHAR_Bhishma_Anchor.webp`
- `V01_CHAR_SHEET_Pandavas.webp`

---

## Suggested GitHub Repository Structure

```text
Mahabharata-Illustrated/
├── README.md
├── docs/
│   ├── Mahabharata_Volume1_Illustration_Spec.md
│   ├── Mahabharata_V01_199_Illustration_Plan.csv
│   └── Mahabharata_V01_Illustration_Master_Plan.json
├── app/
│   └── Mahabharata_Volume_1_Illustration_Studio.html
├── assets/
│   ├── covers/
│   ├── chapters/
│   ├── characters/
│   └── sheets/
└── exports/
    └── Mahabharata_V01_Ready_Illustrations.zip
```

---

## Prompt Templates

### A. Chapter Hero Prompt Template

```text
V01 PXX CHYYY: [Scene title].
Chapter context: [Bengali context].
Cinematic painterly-realistic ancient Indian epic, 16:9 landscape,
detailed textiles and natural lighting, no text, no modern objects.
Maintain the approved character reference faces and body types;
adapt age, costume and equipment to the chapter.
Generate and review missing reference designs first.
Verify the full chapter before rendering.
Reference IDs: [reference ids].
```

### B. Parva Cover Prompt Template

```text
Create a high-quality parva cover for Volume 1, Parva [number], [Parva name].
Use a cinematic painterly-realistic ancient Indian epic style, 16:9 landscape,
no text. Focus on the central narrative identity of this parva, using the approved
character references where available. Keep the image elegant, iconic, emotionally
clear, and suitable for use as a cover in an offline illustrated reading app.
```

### C. Character Card Prompt Template

```text
Create a clean character reference illustration for [Character Name].
Show the approved face, body type, costume, ornaments, and iconic props.
Use a consistent painterly-realistic epic Indian style.
Make the character easy to recognize and reuse across future lesson images.
```

---

## Workflow Rules

1. Verify chapter content before generating art.
2. Check whether needed characters already exist.
3. If a needed recurring character is missing, create the character card first.
4. Generate the chapter image using approved references.
5. Review for:
   - instruction following
   - continuity
   - narrative accuracy
   - readability in app
6. Embed image into app and register it in export/download systems.

---

## Volume 1 Parva Map


- **Parva 01 — অনুক্রমণিকা পর্ব**: Chapters 1–1 (1 chapter)
- **Parva 02 — পর্বসংগ্রহ পর্ব**: Chapters 2–2 (1 chapter)
- **Parva 03 — পৌষ্য পর্ব**: Chapters 3–3 (1 chapter)
- **Parva 04 — পৌলোম পর্ব**: Chapters 4–12 (9 chapters)
- **Parva 05 — আস্তীক পর্ব**: Chapters 13–53 (41 chapters)
- **Parva 06 — আদিবংশাবতরণ পর্ব**: Chapters 54–58 (5 chapters)
- **Parva 07 — সম্ভব পর্ব**: Chapters 59–123 (65 chapters)
- **Parva 08 — জতুগৃহদাহ পর্ব**: Chapters 124–138 (15 chapters)
- **Parva 09 — হিড়িম্ববধ পর্ব**: Chapters 139–144 (6 chapters)
- **Parva 10 — বকবধ পর্ব**: Chapters 145–152 (8 chapters)
- **Parva 11 — চৈত্ররথ পর্ব**: Chapters 153–173 (21 chapters)
- **Parva 12 — দ্রৌপদীস্বয়ংবর পর্ব**: Chapters 174–185 (12 chapters)
- **Parva 13 — বৈবাহিক পর্ব**: Chapters 186–191 (6 chapters)
- **Parva 14 — বিদুরাগমন পর্ব**: Chapters 192–198 (7 chapters)
- **Parva 15 — রাজ্যলাভ পর্ব**: Chapters 199–199 (1 chapter)

---

## Master Illustration Plan — All 199 Chapter Prompts


## Parva 01 — অনুক্রমণিকা পর্ব

**Chapters:** 1–1  
**Count:** 1

### Chapter 001 — Sauti at Naimisha sacrifice

- **Filename:** `V01_P01_CH001_Sauti_at_Naimisha_sacrifice.webp`
- **Status:** Shared cover
- **Parva:** অনুক্রমণিকা পর্ব
- **Bengali Context:** উগ্রশ্রবা সৌতি ঋষিসভায় মহাভারতের আবৃত্তির পটভূমি, কাহিনির উৎস এবং কুরুক্ষেত্রযুদ্ধের ঘটনাসমূহের পরিচয় দেন।
- **Reference IDs:** sauti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P01 CH001: Sauti at Naimisha sacrifice. Chapter context: উগ্রশ্রবা সৌতি ঋষিসভায় মহাভারতের আবৃত্তির পটভূমি, কাহিনির উৎস এবং কুরুক্ষেত্রযুদ্ধের ঘটনাসমূহের পরিচয় দেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: sauti.
```


## Parva 02 — পর্বসংগ্রহ পর্ব

**Chapters:** 2–2  
**Count:** 1

### Chapter 002 — Epic overview of Vyasa and Kurukshetra

- **Filename:** `V01_P02_CH002_Epic_overview_of_Vyasa_and_Kurukshetra.webp`
- **Status:** Draft
- **Parva:** পর্বসংগ্রহ পর্ব
- **Bengali Context:** মহাভারতের একশো উপপর্ব ও আঠারো প্রধান পর্বের বিন্যাস, যুদ্ধের প্রেক্ষাপট এবং সমগ্র মহাকাব্যের সংক্ষিপ্ত ঘটনাক্রম জানা যাবে।
- **Reference IDs:** vyasa
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P02 CH002: Epic overview of Vyasa and Kurukshetra. Chapter context: মহাভারতের একশো উপপর্ব ও আঠারো প্রধান পর্বের বিন্যাস, যুদ্ধের প্রেক্ষাপট এবং সমগ্র মহাকাব্যের সংক্ষিপ্ত ঘটনাক্রম জানা যাবে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa.
```


## Parva 03 — পৌষ্য পর্ব

**Chapters:** 3–3  
**Count:** 1

### Chapter 003 — Uttanka begins earrings quest

- **Filename:** `V01_P03_CH003_Uttanka_begins_earrings_quest.webp`
- **Status:** Planned
- **Parva:** পৌষ্য পর্ব
- **Bengali Context:** জনমেজয়ের পটভূমি থেকে আরুণি, উপমন্যু ও উত্তঙ্কের গুরুসেবা—সর্পযজ্ঞের পূর্বসূত্র এখানে গড়ে ওঠে।
- **Reference IDs:** janamejaya, uttanka
- **Pending New References:** uttanka
- **Detailed Prompt:**

```text
V01 P03 CH003: Uttanka begins earrings quest. Chapter context: জনমেজয়ের পটভূমি থেকে আরুণি, উপমন্যু ও উত্তঙ্কের গুরুসেবা—সর্পযজ্ঞের পূর্বসূত্র এখানে গড়ে ওঠে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: janamejaya, uttanka.
```


## Parva 04 — পৌলোম পর্ব

**Chapters:** 4–12  
**Count:** 9

### Chapter 004 — Shaunaka asks about Bhrigu lineage

- **Filename:** `V01_P04_CH004_Shaunaka_asks_about_Bhrigu_lineage.webp`
- **Status:** Planned
- **Parva:** পৌলোম পর্ব
- **Bengali Context:** শৌনক সৌতির কাছে ভৃগুবংশের কাহিনি শুনতে চান; পৌলোম পর্বের মূল আখ্যানের সূচনা হয়।
- **Reference IDs:** sauti, shaunaka, bhrigu
- **Pending New References:** bhrigu
- **Detailed Prompt:**

```text
V01 P04 CH004: Shaunaka asks about Bhrigu lineage. Chapter context: শৌনক সৌতির কাছে ভৃগুবংশের কাহিনি শুনতে চান; পৌলোম পর্বের মূল আখ্যানের সূচনা হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: sauti, shaunaka, bhrigu.
```

### Chapter 005 — Puloma confronts Agni

- **Filename:** `V01_P04_CH005_Puloma_confronts_Agni.webp`
- **Status:** Planned
- **Parva:** পৌলোম পর্ব
- **Bengali Context:** পুলোমা ও ভৃগুর সংসারে রাক্ষস পুলোমার আবির্ভাব ঘটে; অগ্নির সাক্ষ্য নিয়ে একটি কঠিন সংকট তৈরি হয়।
- **Reference IDs:** puloma, agni
- **Pending New References:** puloma, agni
- **Detailed Prompt:**

```text
V01 P04 CH005: Puloma confronts Agni. Chapter context: পুলোমা ও ভৃগুর সংসারে রাক্ষস পুলোমার আবির্ভাব ঘটে; অগ্নির সাক্ষ্য নিয়ে একটি কঠিন সংকট তৈরি হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: puloma, agni.
```

### Chapter 006 — Chyavana birth and abduction

- **Filename:** `V01_P04_CH006_Chyavana_birth_and_abduction.webp`
- **Status:** Planned
- **Parva:** পৌলোম পর্ব
- **Bengali Context:** রাক্ষসের হাতে পুলোমার অপহরণ, চ্যবনের জন্ম এবং ভৃগুর ক্রোধের ঘটনাগুলি সামনে আসে।
- **Reference IDs:** chyavana
- **Pending New References:** chyavana
- **Detailed Prompt:**

```text
V01 P04 CH006: Chyavana birth and abduction. Chapter context: রাক্ষসের হাতে পুলোমার অপহরণ, চ্যবনের জন্ম এবং ভৃগুর ক্রোধের ঘটনাগুলি সামনে আসে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: chyavana.
```

### Chapter 007 — Agni appeals against curse

- **Filename:** `V01_P04_CH007_Agni_appeals_against_curse.webp`
- **Status:** Planned
- **Parva:** পৌলোম পর্ব
- **Bengali Context:** অগ্নি ভৃগুর অভিশাপের প্রতিবাদ করেন; তাঁর ভূমিকা ও পবিত্রতা নিয়ে দেবতাদের মধ্যে আলোচনা হয়।
- **Reference IDs:** agni
- **Pending New References:** agni
- **Detailed Prompt:**

```text
V01 P04 CH007: Agni appeals against curse. Chapter context: অগ্নি ভৃগুর অভিশাপের প্রতিবাদ করেন; তাঁর ভূমিকা ও পবিত্রতা নিয়ে দেবতাদের মধ্যে আলোচনা হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: agni.
```

### Chapter 008 — Ruru finds Pramadvara

- **Filename:** `V01_P04_CH008_Ruru_finds_Pramadvara.webp`
- **Status:** Planned
- **Parva:** পৌলোম পর্ব
- **Bengali Context:** ভৃগুবংশে রুরুর জন্ম এবং প্রমদ্বরার সঙ্গে তাঁর প্রেমের কথা শুরু হয়; এক আকস্মিক দুর্ঘটনা বিপর্যয় ডেকে আনে।
- **Reference IDs:** ruru, pramadvara
- **Pending New References:** ruru, pramadvara
- **Detailed Prompt:**

```text
V01 P04 CH008: Ruru finds Pramadvara. Chapter context: ভৃগুবংশে রুরুর জন্ম এবং প্রমদ্বরার সঙ্গে তাঁর প্রেমের কথা শুরু হয়; এক আকস্মিক দুর্ঘটনা বিপর্যয় ডেকে আনে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: ruru, pramadvara.
```

### Chapter 009 — Ruru offers half his lifespan

- **Filename:** `V01_P04_CH009_Ruru_offers_half_his_lifespan.webp`
- **Status:** Planned
- **Parva:** পৌলোম পর্ব
- **Bengali Context:** প্রমদ্বরার মৃত্যুশোকে রুরুর বিলাপ ও প্রিয়জনকে ফিরে পাওয়ার ত্যাগময় সংকল্পের কাহিনি রয়েছে।
- **Reference IDs:** ruru
- **Pending New References:** ruru
- **Detailed Prompt:**

```text
V01 P04 CH009: Ruru offers half his lifespan. Chapter context: প্রমদ্বরার মৃত্যুশোকে রুরুর বিলাপ ও প্রিয়জনকে ফিরে পাওয়ার ত্যাগময় সংকল্পের কাহিনি রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: ruru.
```

### Chapter 010 — Ruru encounters cursed serpent

- **Filename:** `V01_P04_CH010_Ruru_encounters_cursed_serpent.webp`
- **Status:** Planned
- **Parva:** পৌলোম পর্ব
- **Bengali Context:** রুরু একটি সাপকে আঘাত করতে গিয়ে জানতে পারেন, সেটি প্রকৃতপক্ষে এক অভিশপ্ত ঋষি।
- **Reference IDs:** ruru
- **Pending New References:** ruru
- **Detailed Prompt:**

```text
V01 P04 CH010: Ruru encounters cursed serpent. Chapter context: রুরু একটি সাপকে আঘাত করতে গিয়ে জানতে পারেন, সেটি প্রকৃতপক্ষে এক অভিশপ্ত ঋষি।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: ruru.
```

### Chapter 011 — Sahasrapat teaches nonviolence

- **Filename:** `V01_P04_CH011_Sahasrapat_teaches_nonviolence.webp`
- **Status:** Planned
- **Parva:** পৌলোম পর্ব
- **Bengali Context:** অভিশপ্ত ঋষি সহস্রপাৎ তাঁর অতীত বর্ণনা করে রুরুকে অহিংসা ও ধর্মের শিক্ষা দেন।
- **Reference IDs:** sahasrapat
- **Pending New References:** sahasrapat
- **Detailed Prompt:**

```text
V01 P04 CH011: Sahasrapat teaches nonviolence. Chapter context: অভিশপ্ত ঋষি সহস্রপাৎ তাঁর অতীত বর্ণনা করে রুরুকে অহিংসা ও ধর্মের শিক্ষা দেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: sahasrapat.
```

### Chapter 012 — Ruru hears of snake sacrifice

- **Filename:** `V01_P04_CH012_Ruru_hears_of_snake_sacrifice.webp`
- **Status:** Planned
- **Parva:** পৌলোম পর্ব
- **Bengali Context:** রুরু জানতে চান জনমেজয়ের সর্পযজ্ঞ এবং আস্তীকের ভূমিকা; পরবর্তী বৃহৎ আখ্যানের সঙ্গে সংযোগ তৈরি হয়।
- **Reference IDs:** janamejaya, ruru
- **Pending New References:** ruru
- **Detailed Prompt:**

```text
V01 P04 CH012: Ruru hears of snake sacrifice. Chapter context: রুরু জানতে চান জনমেজয়ের সর্পযজ্ঞ এবং আস্তীকের ভূমিকা; পরবর্তী বৃহৎ আখ্যানের সঙ্গে সংযোগ তৈরি হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: janamejaya, ruru.
```


## Parva 05 — আস্তীক পর্ব

**Chapters:** 13–53  
**Count:** 41

### Chapter 013 — Prophecy of Astika

- **Filename:** `V01_P05_CH013_Prophecy_of_Astika.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** সর্পজাতির বিপদের পূর্বাভাস এবং জরৎকারু–আস্তীক সম্পর্কিত কাহিনির সূত্রপাত ঘটে।
- **Reference IDs:** astika
- **Pending New References:** astika
- **Detailed Prompt:**

```text
V01 P05 CH013: Prophecy of Astika. Chapter context: সর্পজাতির বিপদের পূর্বাভাস এবং জরৎকারু–আস্তীক সম্পর্কিত কাহিনির সূত্রপাত ঘটে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: astika.
```

### Chapter 014 — Kadru Vinata and Aruna

- **Filename:** `V01_P05_CH014_Kadru_Vinata_and_Aruna.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** কদ্রু ও বিনতার পরিবার, অরুণের জন্ম এবং দুই ভগিনীর জীবনে অভিশাপের প্রভাব উঠে আসে।
- **Reference IDs:** kadru, vinata, aruna
- **Pending New References:** kadru, vinata, aruna
- **Detailed Prompt:**

```text
V01 P05 CH014: Kadru Vinata and Aruna. Chapter context: কদ্রু ও বিনতার পরিবার, অরুণের জন্ম এবং দুই ভগিনীর জীবনে অভিশাপের প্রভাব উঠে আসে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: kadru, vinata, aruna.
```

### Chapter 015 — Uchchaihshravas and Meru

- **Filename:** `V01_P05_CH015_Uchchaihshravas_and_Meru.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** অমৃতমন্থন থেকে উদ্ভূত উচ্চৈঃশ্রবা অশ্বকে ঘিরে কদ্রু–বিনতার পণ ও মেরুর পরিচয় শুরু হয়।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P05 CH015: Uchchaihshravas and Meru. Chapter context: অমৃতমন্থন থেকে উদ্ভূত উচ্চৈঃশ্রবা অশ্বকে ঘিরে কদ্রু–বিনতার পণ ও মেরুর পরিচয় শুরু হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```

### Chapter 016 — Churning of the ocean

- **Filename:** `V01_P05_CH016_Churning_of_the_ocean.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** মন্দর পর্বতকে ঘিরে দেবতা ও অসুরদের সমুদ্রমন্থন এবং অমৃত লাভের দীর্ঘ আখ্যান বর্ণিত হয়।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P05 CH016: Churning of the ocean. Chapter context: মন্দর পর্বতকে ঘিরে দেবতা ও অসুরদের সমুদ্রমন্থন এবং অমৃত লাভের দীর্ঘ আখ্যান বর্ণিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```

### Chapter 017 — Vishnu guards amrita

- **Filename:** `V01_P05_CH017_Vishnu_guards_amrita.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** অমৃতের অধিকার নিয়ে দেবতা–দানব সংঘর্ষ এবং বিষ্ণুর হস্তক্ষেপের কাহিনি রয়েছে।
- **Reference IDs:** vishnu
- **Pending New References:** vishnu
- **Detailed Prompt:**

```text
V01 P05 CH017: Vishnu guards amrita. Chapter context: অমৃতের অধিকার নিয়ে দেবতা–দানব সংঘর্ষ এবং বিষ্ণুর হস্তক্ষেপের কাহিনি রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vishnu.
```

### Chapter 018 — Kadru commands serpents

- **Filename:** `V01_P05_CH018_Kadru_commands_serpents.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** উচ্চৈঃশ্রবার লেজের রং নিয়ে দুই ভগিনীর পণের পরে কদ্রুর পুত্রদের ওপর অভিশাপ নেমে আসে।
- **Reference IDs:** kadru
- **Pending New References:** kadru
- **Detailed Prompt:**

```text
V01 P05 CH018: Kadru commands serpents. Chapter context: উচ্চৈঃশ্রবার লেজের রং নিয়ে দুই ভগিনীর পণের পরে কদ্রুর পুত্রদের ওপর অভিশাপ নেমে আসে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: kadru.
```

### Chapter 019 — Sisters cross ocean

- **Filename:** `V01_P05_CH019_Sisters_cross_ocean.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** কদ্রু ও বিনতা সমুদ্র পেরিয়ে উচ্চৈঃশ্রবার সন্ধানে রওনা দেন; প্রকৃতির বিস্তৃত বর্ণনা রয়েছে।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P05 CH019: Sisters cross ocean. Chapter context: কদ্রু ও বিনতা সমুদ্র পেরিয়ে উচ্চৈঃশ্রবার সন্ধানে রওনা দেন; প্রকৃতির বিস্তৃত বর্ণনা রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```

### Chapter 020 — Vinata enslaved and Garuda born

- **Filename:** `V01_P05_CH020_Vinata_enslaved_and_Garuda_born.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** পণের ফল প্রকাশিত হয়, বিনতার দাসত্ব শুরু হয় এবং মহাবলশালী গরুড়ের জন্মের আভাস মেলে।
- **Reference IDs:** vinata, garuda
- **Pending New References:** vinata, garuda
- **Detailed Prompt:**

```text
V01 P05 CH020: Vinata enslaved and Garuda born. Chapter context: পণের ফল প্রকাশিত হয়, বিনতার দাসত্ব শুরু হয় এবং মহাবলশালী গরুড়ের জন্মের আভাস মেলে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vinata, garuda.
```

### Chapter 021 — Garuda seeks freedom for Vinata

- **Filename:** `V01_P05_CH021_Garuda_seeks_freedom_for_Vinata.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** মাকে দাসত্ব থেকে মুক্ত করার পথ খুঁজতে গরুড় কদ্রুর সর্পপুত্রদের সঙ্গে কথা বলেন।
- **Reference IDs:** vinata, garuda
- **Pending New References:** vinata, garuda
- **Detailed Prompt:**

```text
V01 P05 CH021: Garuda seeks freedom for Vinata. Chapter context: মাকে দাসত্ব থেকে মুক্ত করার পথ খুঁজতে গরুড় কদ্রুর সর্পপুত্রদের সঙ্গে কথা বলেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vinata, garuda.
```

### Chapter 022 — Indra sends rain

- **Filename:** `V01_P05_CH022_Indra_sends_rain.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** সর্পদের দুর্দশায় কদ্রুর প্রার্থনা ও ইন্দ্রের প্রবল বৃষ্টিবর্ষণের ঘটনা বর্ণিত হয়।
- **Reference IDs:** indra
- **Pending New References:** indra
- **Detailed Prompt:**

```text
V01 P05 CH022: Indra sends rain. Chapter context: সর্পদের দুর্দশায় কদ্রুর প্রার্থনা ও ইন্দ্রের প্রবল বৃষ্টিবর্ষণের ঘটনা বর্ণিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: indra.
```

### Chapter 023 — Garuda carries serpents to island

- **Filename:** `V01_P05_CH023_Garuda_carries_serpents_to_island.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** গরুড় সর্পদের বহন করে দ্বীপে নিয়ে যান এবং মায়ের মুক্তির জন্য অমৃত আনতে সম্মত হন।
- **Reference IDs:** garuda
- **Pending New References:** garuda
- **Detailed Prompt:**

```text
V01 P05 CH023: Garuda carries serpents to island. Chapter context: গরুড় সর্পদের বহন করে দ্বীপে নিয়ে যান এবং মায়ের মুক্তির জন্য অমৃত আনতে সম্মত হন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: garuda.
```

### Chapter 024 — Garuda seeks food

- **Filename:** `V01_P05_CH024_Garuda_seeks_food.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** অমৃত সংগ্রহের অভিযানের আগে গরুড় আহারের সন্ধানে বেরিয়ে তাঁর অতিমানবীয় শক্তি প্রকাশ করেন।
- **Reference IDs:** garuda
- **Pending New References:** garuda
- **Detailed Prompt:**

```text
V01 P05 CH024: Garuda seeks food. Chapter context: অমৃত সংগ্রহের অভিযানের আগে গরুড় আহারের সন্ধানে বেরিয়ে তাঁর অতিমানবীয় শক্তি প্রকাশ করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: garuda.
```

### Chapter 025 — Garuda spares Brahmin

- **Filename:** `V01_P05_CH025_Garuda_spares_Brahmin.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** গরুড়ের অন্নান্বেষণ, ব্রাহ্মণ রক্ষার কর্তব্য এবং দুই অভিশপ্ত প্রাণীর কাহিনি জানা যাবে।
- **Reference IDs:** garuda
- **Pending New References:** garuda
- **Detailed Prompt:**

```text
V01 P05 CH025: Garuda spares Brahmin. Chapter context: গরুড়ের অন্নান্বেষণ, ব্রাহ্মণ রক্ষার কর্তব্য এবং দুই অভিশপ্ত প্রাণীর কাহিনি জানা যাবে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: garuda.
```

### Chapter 026 — Garuda carries elephant tortoise and sages

- **Filename:** `V01_P05_CH026_Garuda_carries_elephant_tortoise_and_sages.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** গরুড় গজ ও কচ্ছপ ভক্ষণ করেন, ঋষিদের রক্ষা করেন এবং দেবতাদের অমৃতরক্ষার প্রস্তুতি শুরু হয়।
- **Reference IDs:** garuda
- **Pending New References:** garuda
- **Detailed Prompt:**

```text
V01 P05 CH026: Garuda carries elephant tortoise and sages. Chapter context: গরুড় গজ ও কচ্ছপ ভক্ষণ করেন, ঋষিদের রক্ষা করেন এবং দেবতাদের অমৃতরক্ষার প্রস্তুতি শুরু হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: garuda.
```

### Chapter 027 — Valakhilya sages sacrifice

- **Filename:** `V01_P05_CH027_Valakhilya_sages_sacrifice.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** ইন্দ্রের সঙ্গে বালখিল্য ঋষিদের বিরোধ থেকে গরুড়ের জন্মপরম্পরার পটভূমি স্পষ্ট হয়।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P05 CH027: Valakhilya sages sacrifice. Chapter context: ইন্দ্রের সঙ্গে বালখিল্য ঋষিদের বিরোধ থেকে গরুড়ের জন্মপরম্পরার পটভূমি স্পষ্ট হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```

### Chapter 028 — Garuda battles gods

- **Filename:** `V01_P05_CH028_Garuda_battles_gods.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** গরুড় দেববাহিনীর বিরুদ্ধে প্রচণ্ড যুদ্ধ শুরু করেন এবং অমৃতের কঠোর প্রতিরক্ষা ভেদ করতে এগোন।
- **Reference IDs:** garuda
- **Pending New References:** garuda
- **Detailed Prompt:**

```text
V01 P05 CH028: Garuda battles gods. Chapter context: গরুড় দেববাহিনীর বিরুদ্ধে প্রচণ্ড যুদ্ধ শুরু করেন এবং অমৃতের কঠোর প্রতিরক্ষা ভেদ করতে এগোন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: garuda.
```

### Chapter 029 — Garuda retrieves amrita

- **Filename:** `V01_P05_CH029_Garuda_retrieves_amrita.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** গরুড় অমৃতরক্ষার যন্ত্র ও প্রহরীদের অতিক্রম করে অমৃত সংগ্রহ করেন; বিষ্ণু ও ইন্দ্রের সঙ্গে তাঁর সাক্ষাৎ হয়।
- **Reference IDs:** garuda
- **Pending New References:** garuda
- **Detailed Prompt:**

```text
V01 P05 CH029: Garuda retrieves amrita. Chapter context: গরুড় অমৃতরক্ষার যন্ত্র ও প্রহরীদের অতিক্রম করে অমৃত সংগ্রহ করেন; বিষ্ণু ও ইন্দ্রের সঙ্গে তাঁর সাক্ষাৎ হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: garuda.
```

### Chapter 030 — Garuda frees Vinata

- **Filename:** `V01_P05_CH030_Garuda_frees_Vinata.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** গরুড় ও ইন্দ্র বন্ধুত্ব স্থাপন করেন; সর্পদের জন্য আনা অমৃতের পরিণতি ও তাদের জিহ্বার বৈশিষ্ট্য ব্যাখ্যাত হয়।
- **Reference IDs:** vinata, garuda
- **Pending New References:** vinata, garuda
- **Detailed Prompt:**

```text
V01 P05 CH030: Garuda frees Vinata. Chapter context: গরুড় ও ইন্দ্র বন্ধুত্ব স্থাপন করেন; সর্পদের জন্য আনা অমৃতের পরিণতি ও তাদের জিহ্বার বৈশিষ্ট্য ব্যাখ্যাত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vinata, garuda.
```

### Chapter 031 — Serpent lineages

- **Filename:** `V01_P05_CH031_Serpent_lineages.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** কদ্রুর অসংখ্য সর্পপুত্রের মধ্যে প্রধান নাগদের নাম ও বংশপরিচয় বিস্তারিতভাবে তালিকাভুক্ত হয়েছে।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P05 CH031: Serpent lineages. Chapter context: কদ্রুর অসংখ্য সর্পপুত্রের মধ্যে প্রধান নাগদের নাম ও বংশপরিচয় বিস্তারিতভাবে তালিকাভুক্ত হয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```

### Chapter 032 — Shesha supports earth

- **Filename:** `V01_P05_CH032_Shesha_supports_earth.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** মাতৃশাপের পরে শেষনাগ তপস্যায় রত হন এবং পৃথিবী ধারণের গুরুদায়িত্ব লাভ করেন।
- **Reference IDs:** shesha
- **Pending New References:** shesha
- **Detailed Prompt:**

```text
V01 P05 CH032: Shesha supports earth. Chapter context: মাতৃশাপের পরে শেষনাগ তপস্যায় রত হন এবং পৃথিবী ধারণের গুরুদায়িত্ব লাভ করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: shesha.
```

### Chapter 033 — Vasuki consults serpent council

- **Filename:** `V01_P05_CH033_Vasuki_consults_serpent_council.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** নাগরাজ বাসুকি অভিশাপ থেকে পরিত্রাণের জন্য ভাইদের নিয়ে পরামর্শ করেন; নানা উপায় আলোচিত হয়।
- **Reference IDs:** vasuki
- **Pending New References:** vasuki
- **Detailed Prompt:**

```text
V01 P05 CH033: Vasuki consults serpent council. Chapter context: নাগরাজ বাসুকি অভিশাপ থেকে পরিত্রাণের জন্য ভাইদের নিয়ে পরামর্শ করেন; নানা উপায় আলোচিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vasuki.
```

### Chapter 034 — Elapatra prophecy

- **Filename:** `V01_P05_CH034_Elapatra_prophecy.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** এলাপত্র নাগরাজকে জানান, এক ঋষিপুত্রের জন্মের মধ্য দিয়ে সর্পজাতির রক্ষার পথ খুলবে।
- **Reference IDs:** elapatra
- **Pending New References:** elapatra
- **Detailed Prompt:**

```text
V01 P05 CH034: Elapatra prophecy. Chapter context: এলাপত্র নাগরাজকে জানান, এক ঋষিপুত্রের জন্মের মধ্য দিয়ে সর্পজাতির রক্ষার পথ খুলবে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: elapatra.
```

### Chapter 035 — Vasuki protects Jaratkaru

- **Filename:** `V01_P05_CH035_Vasuki_protects_Jaratkaru.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** বাসুকি নিজের ভগিনী জরৎকারুকে সেই ভবিষ্যৎ পরিত্রাণের জন্য প্রস্তুত রাখেন।
- **Reference IDs:** vasuki, jaratkaru
- **Pending New References:** vasuki, jaratkaru
- **Detailed Prompt:**

```text
V01 P05 CH035: Vasuki protects Jaratkaru. Chapter context: বাসুকি নিজের ভগিনী জরৎকারুকে সেই ভবিষ্যৎ পরিত্রাণের জন্য প্রস্তুত রাখেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vasuki, jaratkaru.
```

### Chapter 036 — Jaratkaru ascetic pilgrimage

- **Filename:** `V01_P05_CH036_Jaratkaru_ascetic_pilgrimage.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** জরৎকারু ঋষির পরিচয় ও নামের ব্যাখ্যার সঙ্গে শৃঙ্গী ও পরীক্ষিতের ঘটনার ভূমিকা শুরু হয়।
- **Reference IDs:** jaratkaru
- **Pending New References:** jaratkaru
- **Detailed Prompt:**

```text
V01 P05 CH036: Jaratkaru ascetic pilgrimage. Chapter context: জরৎকারু ঋষির পরিচয় ও নামের ব্যাখ্যার সঙ্গে শৃঙ্গী ও পরীক্ষিতের ঘটনার ভূমিকা শুরু হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: jaratkaru.
```

### Chapter 037 — Shringi curses Parikshit

- **Filename:** `V01_P05_CH037_Shringi_curses_Parikshit.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** শৃঙ্গী রাজা পরীক্ষিতকে অভিশাপ দেন; শমীক ঋষির সংযত প্রতিক্রিয়ায় কর্তব্যের প্রশ্ন সামনে আসে।
- **Reference IDs:** parikshit, shringi
- **Pending New References:** parikshit, shringi
- **Detailed Prompt:**

```text
V01 P05 CH037: Shringi curses Parikshit. Chapter context: শৃঙ্গী রাজা পরীক্ষিতকে অভিশাপ দেন; শমীক ঋষির সংযত প্রতিক্রিয়ায় কর্তব্যের প্রশ্ন সামনে আসে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: parikshit, shringi.
```

### Chapter 038 — Takshaka approaches Kashyapa

- **Filename:** `V01_P05_CH038_Takshaka_approaches_Kashyapa.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** শৃঙ্গীর অভিশাপের পর পরীক্ষিতের বিপদ ঘনিয়ে আসে; তক্ষক ও বিষনিবারণে পারদর্শী কশ্যপের কাহিনি শুরু হয়।
- **Reference IDs:** takshaka, kashyapa
- **Pending New References:** takshaka, kashyapa
- **Detailed Prompt:**

```text
V01 P05 CH038: Takshaka approaches Kashyapa. Chapter context: শৃঙ্গীর অভিশাপের পর পরীক্ষিতের বিপদ ঘনিয়ে আসে; তক্ষক ও বিষনিবারণে পারদর্শী কশ্যপের কাহিনি শুরু হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: takshaka, kashyapa.
```

### Chapter 039 — Kashyapa restores burned tree

- **Filename:** `V01_P05_CH039_Kashyapa_restores_burned_tree.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** তক্ষক ও কশ্যপের মধ্যে বিষশক্তি ও প্রতিকারের পরীক্ষা হয়; পরীক্ষিতের মৃত্যুর পূর্বমুহূর্তের ঘটনা রয়েছে।
- **Reference IDs:** kashyapa
- **Pending New References:** kashyapa
- **Detailed Prompt:**

```text
V01 P05 CH039: Kashyapa restores burned tree. Chapter context: তক্ষক ও কশ্যপের মধ্যে বিষশক্তি ও প্রতিকারের পরীক্ষা হয়; পরীক্ষিতের মৃত্যুর পূর্বমুহূর্তের ঘটনা রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: kashyapa.
```

### Chapter 040 — Takshaka reaches Parikshit

- **Filename:** `V01_P05_CH040_Takshaka_reaches_Parikshit.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** তক্ষকের দংশনে পরীক্ষিতের মৃত্যু ও পরবর্তী সময়ে জনমেজয়ের রাজ্যশাসনের প্রেক্ষাপট বর্ণিত হয়।
- **Reference IDs:** janamejaya, parikshit, takshaka
- **Pending New References:** parikshit, takshaka
- **Detailed Prompt:**

```text
V01 P05 CH040: Takshaka reaches Parikshit. Chapter context: তক্ষকের দংশনে পরীক্ষিতের মৃত্যু ও পরবর্তী সময়ে জনমেজয়ের রাজ্যশাসনের প্রেক্ষাপট বর্ণিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: janamejaya, parikshit, takshaka.
```

### Chapter 041 — Jaratkaru encounters ancestors

- **Filename:** `V01_P05_CH041_Jaratkaru_encounters_ancestors.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** জরৎকারু ঋষি তপস্যার পথে নিজের দুর্দশাগ্রস্ত পূর্বপুরুষদের সাক্ষাৎ পান।
- **Reference IDs:** jaratkaru
- **Pending New References:** jaratkaru
- **Detailed Prompt:**

```text
V01 P05 CH041: Jaratkaru encounters ancestors. Chapter context: জরৎকারু ঋষি তপস্যার পথে নিজের দুর্দশাগ্রস্ত পূর্বপুরুষদের সাক্ষাৎ পান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: jaratkaru.
```

### Chapter 042 — Jaratkaru agrees to marry

- **Filename:** `V01_P05_CH042_Jaratkaru_agrees_to_marry.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** পূর্বপুরুষদের মুক্তির জন্য জরৎকারু বিবাহে সম্মত হন; নাগরাজ বাসুকি এই সুযোগ জানতে পারেন।
- **Reference IDs:** jaratkaru
- **Pending New References:** jaratkaru
- **Detailed Prompt:**

```text
V01 P05 CH042: Jaratkaru agrees to marry. Chapter context: পূর্বপুরুষদের মুক্তির জন্য জরৎকারু বিবাহে সম্মত হন; নাগরাজ বাসুকি এই সুযোগ জানতে পারেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: jaratkaru.
```

### Chapter 043 — Jaratkaru wedding

- **Filename:** `V01_P05_CH043_Jaratkaru_wedding.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** ঋষি জরৎকারু ও নাগকন্যা জরৎকারুর বিবাহ, সংসারের শর্ত এবং গর্ভস্থ সন্তানের ভবিষ্যৎ উঠে আসে।
- **Reference IDs:** jaratkaru
- **Pending New References:** jaratkaru
- **Detailed Prompt:**

```text
V01 P05 CH043: Jaratkaru wedding. Chapter context: ঋষি জরৎকারু ও নাগকন্যা জরৎকারুর বিবাহ, সংসারের শর্ত এবং গর্ভস্থ সন্তানের ভবিষ্যৎ উঠে আসে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: jaratkaru.
```

### Chapter 044 — Astika born

- **Filename:** `V01_P05_CH044_Astika_born.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** নাগকন্যা জরৎকারুর গর্ভে আস্তীকের জন্ম হয়; সর্পজাতির রক্ষক হিসেবে তাঁর ভূমিকার ভিত্তি স্থাপিত হয়।
- **Reference IDs:** astika
- **Pending New References:** astika
- **Detailed Prompt:**

```text
V01 P05 CH044: Astika born. Chapter context: নাগকন্যা জরৎকারুর গর্ভে আস্তীকের জন্ম হয়; সর্পজাতির রক্ষক হিসেবে তাঁর ভূমিকার ভিত্তি স্থাপিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: astika.
```

### Chapter 045 — Janamejaya questions ministers

- **Filename:** `V01_P05_CH045_Janamejaya_questions_ministers.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** জনমেজয় মন্ত্রীদের কাছে পিতা পরীক্ষিতের জীবন ও মৃত্যুর পূর্ণ বিবরণ জানতে চান।
- **Reference IDs:** janamejaya
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P05 CH045: Janamejaya questions ministers. Chapter context: জনমেজয় মন্ত্রীদের কাছে পিতা পরীক্ষিতের জীবন ও মৃত্যুর পূর্ণ বিবরণ জানতে চান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: janamejaya.
```

### Chapter 046 — Ministers recount Parikshit death

- **Filename:** `V01_P05_CH046_Ministers_recount_Parikshit_death.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** মন্ত্রীদের মুখে পরীক্ষিতের অভিশাপ ও মৃত্যুর বিবরণ শুনে জনমেজয়ের প্রতিশোধস্পৃহা তীব্র হয়।
- **Reference IDs:** janamejaya, parikshit
- **Pending New References:** parikshit
- **Detailed Prompt:**

```text
V01 P05 CH046: Ministers recount Parikshit death. Chapter context: মন্ত্রীদের মুখে পরীক্ষিতের অভিশাপ ও মৃত্যুর বিবরণ শুনে জনমেজয়ের প্রতিশোধস্পৃহা তীব্র হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: janamejaya, parikshit.
```

### Chapter 047 — Janamejaya orders sacrifice

- **Filename:** `V01_P05_CH047_Janamejaya_orders_sacrifice.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** তক্ষকের প্রতিশোধ নিতে জনমেজয় সর্পযজ্ঞের আয়োজন করেন; যজ্ঞের বিধান ও প্রস্তুতি বর্ণিত হয়।
- **Reference IDs:** janamejaya
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P05 CH047: Janamejaya orders sacrifice. Chapter context: তক্ষকের প্রতিশোধ নিতে জনমেজয় সর্পযজ্ঞের আয়োজন করেন; যজ্ঞের বিধান ও প্রস্তুতি বর্ণিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: janamejaya.
```

### Chapter 048 — Vasuki hears of sacrifice

- **Filename:** `V01_P05_CH048_Vasuki_hears_of_sacrifice.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** সর্পযজ্ঞের ঋত্বিক ও সদস্যদের পরিচয় এবং নাগরাজ বাসুকির আতঙ্কের কাহিনি রয়েছে।
- **Reference IDs:** vasuki
- **Pending New References:** vasuki
- **Detailed Prompt:**

```text
V01 P05 CH048: Vasuki hears of sacrifice. Chapter context: সর্পযজ্ঞের ঋত্বিক ও সদস্যদের পরিচয় এবং নাগরাজ বাসুকির আতঙ্কের কাহিনি রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vasuki.
```

### Chapter 049 — Jaratkaru sends Astika

- **Filename:** `V01_P05_CH049_Jaratkaru_sends_Astika.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** মা জরৎকারু আস্তীককে নাগবংশের বিপদের কথা জানান; আস্তীক যজ্ঞসভায় যাওয়ার সংকল্প নেন।
- **Reference IDs:** astika, jaratkaru
- **Pending New References:** astika, jaratkaru
- **Detailed Prompt:**

```text
V01 P05 CH049: Jaratkaru sends Astika. Chapter context: মা জরৎকারু আস্তীককে নাগবংশের বিপদের কথা জানান; আস্তীক যজ্ঞসভায় যাওয়ার সংকল্প নেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: astika, jaratkaru.
```

### Chapter 050 — Astika enters sacrificial hall

- **Filename:** `V01_P05_CH050_Astika_enters_sacrificial_hall.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** আস্তীক জনমেজয়ের যজ্ঞসভায় প্রবেশ করে রাজা ও যজ্ঞের মহিমা বর্ণনা করে সকলের মন জয় করেন।
- **Reference IDs:** janamejaya, astika
- **Pending New References:** astika
- **Detailed Prompt:**

```text
V01 P05 CH050: Astika enters sacrificial hall. Chapter context: আস্তীক জনমেজয়ের যজ্ঞসভায় প্রবেশ করে রাজা ও যজ্ঞের মহিমা বর্ণনা করে সকলের মন জয় করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: janamejaya, astika.
```

### Chapter 051 — Astika requests boon

- **Filename:** `V01_P05_CH051_Astika_requests_boon.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** রাজা আস্তীককে বর দিতে চান; আস্তীক সোনা নয়, সর্পযজ্ঞ বন্ধের বর প্রার্থনা করেন।
- **Reference IDs:** astika
- **Pending New References:** astika
- **Detailed Prompt:**

```text
V01 P05 CH051: Astika requests boon. Chapter context: রাজা আস্তীককে বর দিতে চান; আস্তীক সোনা নয়, সর্পযজ্ঞ বন্ধের বর প্রার্থনা করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: astika.
```

### Chapter 052 — Serpent clans drawn to fire

- **Filename:** `V01_P05_CH052_Serpent_clans_drawn_to_fire.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** যজ্ঞে পতিত বিভিন্ন নাগবংশের সর্পদের নাম ও পরিচয় বিস্তৃতভাবে বর্ণিত হয়েছে।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P05 CH052: Serpent clans drawn to fire. Chapter context: যজ্ঞে পতিত বিভিন্ন নাগবংশের সর্পদের নাম ও পরিচয় বিস্তৃতভাবে বর্ণিত হয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```

### Chapter 053 — Astika stops sacrifice

- **Filename:** `V01_P05_CH053_Astika_stops_sacrifice.webp`
- **Status:** Planned
- **Parva:** আস্তীক পর্ব
- **Bengali Context:** আস্তীকের বরে তক্ষক রক্ষা পায়; সর্পযজ্ঞের সমাপ্তি এবং আস্তীকের মাহাত্ম্য আলোচিত হয়।
- **Reference IDs:** astika
- **Pending New References:** astika
- **Detailed Prompt:**

```text
V01 P05 CH053: Astika stops sacrifice. Chapter context: আস্তীকের বরে তক্ষক রক্ষা পায়; সর্পযজ্ঞের সমাপ্তি এবং আস্তীকের মাহাত্ম্য আলোচিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: astika.
```


## Parva 06 — আদিবংশাবতরণ পর্ব

**Chapters:** 54–58  
**Count:** 5

### Chapter 054 — Vyasa commissions Vaishampayana

- **Filename:** `V01_P06_CH054_Vyasa_commissions_Vaishampayana.webp`
- **Status:** Planned
- **Parva:** আদিবংশাবতরণ পর্ব
- **Bengali Context:** ব্যাসদেব জনমেজয়ের যজ্ঞে উপস্থিত হন; বৈশম্পায়নকে কুরু-পাণ্ডবদের ইতিহাস আবৃত্তির দায়িত্ব দেন।
- **Reference IDs:** vyasa, vaishampayana, janamejaya
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P06 CH054: Vyasa commissions Vaishampayana. Chapter context: ব্যাসদেব জনমেজয়ের যজ্ঞে উপস্থিত হন; বৈশম্পায়নকে কুরু-পাণ্ডবদের ইতিহাস আবৃত্তির দায়িত্ব দেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa, vaishampayana, janamejaya.
```

### Chapter 055 — Vaishampayana recounts rivalry

- **Filename:** `V01_P06_CH055_Vaishampayana_recounts_rivalry.webp`
- **Status:** Planned
- **Parva:** আদিবংশাবতরণ পর্ব
- **Bengali Context:** কুরু-পাণ্ডব বিরোধের ইতিহাস, পাশাখেলা ও নির্বাসনের দিকে অগ্রসর হওয়া ঘটনাক্রমের সংক্ষিপ্ত বিবরণ রয়েছে।
- **Reference IDs:** vaishampayana
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P06 CH055: Vaishampayana recounts rivalry. Chapter context: কুরু-পাণ্ডব বিরোধের ইতিহাস, পাশাখেলা ও নির্বাসনের দিকে অগ্রসর হওয়া ঘটনাক্রমের সংক্ষিপ্ত বিবরণ রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vaishampayana.
```

### Chapter 056 — Janamejaya requests complete epic

- **Filename:** `V01_P06_CH056_Janamejaya_requests_complete_epic.webp`
- **Status:** Planned
- **Parva:** আদিবংশাবতরণ পর্ব
- **Bengali Context:** জনমেজয় বিস্তারিত মহাভারত শুনতে চান; মহাকাব্যের পরিসর ও ধর্ম–অর্থ–কাম–মোক্ষের মাহাত্ম্য আলোচিত হয়।
- **Reference IDs:** janamejaya
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P06 CH056: Janamejaya requests complete epic. Chapter context: জনমেজয় বিস্তারিত মহাভারত শুনতে চান; মহাকাব্যের পরিসর ও ধর্ম–অর্থ–কাম–মোক্ষের মাহাত্ম্য আলোচিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: janamejaya.
```

### Chapter 057 — Satyavati and origins of Vyasa

- **Filename:** `V01_P06_CH057_Satyavati_and_origins_of_Vyasa.webp`
- **Status:** Planned
- **Parva:** আদিবংশাবতরণ পর্ব
- **Bengali Context:** উপরিচর বসু থেকে সত্যবতী, ব্যাস এবং প্রধান রাজবংশগুলির জন্মপরম্পরা বিস্তারিতভাবে বর্ণিত হয়েছে।
- **Reference IDs:** vyasa, satyavati
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P06 CH057: Satyavati and origins of Vyasa. Chapter context: উপরিচর বসু থেকে সত্যবতী, ব্যাস এবং প্রধান রাজবংশগুলির জন্মপরম্পরা বিস্তারিতভাবে বর্ণিত হয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa, satyavati.
```

### Chapter 058 — Gods relieve burden of Earth

- **Filename:** `V01_P06_CH058_Gods_relieve_burden_of_Earth.webp`
- **Status:** Planned
- **Parva:** আদিবংশাবতরণ পর্ব
- **Bengali Context:** পৃথিবীর ভার লাঘবের জন্য দেবতা ও অসুরদের মানবজন্মের পরিকল্পনা এবং তার পটভূমি জানা যাবে।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P06 CH058: Gods relieve burden of Earth. Chapter context: পৃথিবীর ভার লাঘবের জন্য দেবতা ও অসুরদের মানবজন্মের পরিকল্পনা এবং তার পটভূমি জানা যাবে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```


## Parva 07 — সম্ভব পর্ব

**Chapters:** 59–123  
**Count:** 65

### Chapter 059 — Divine genealogies

- **Filename:** `V01_P07_CH059_Divine_genealogies.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** দেবতা, দানব, নাগ, গন্ধর্ব ও অপ্সরাদের সৃষ্টি ও বংশপরিচয়ের বিস্তৃত সূচনা রয়েছে।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH059: Divine genealogies. Chapter context: দেবতা, দানব, নাগ, গন্ধর্ব ও অপ্সরাদের সৃষ্টি ও বংশপরিচয়ের বিস্তৃত সূচনা রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```

### Chapter 060 — Brahma and celestial creation

- **Filename:** `V01_P07_CH060_Brahma_and_celestial_creation.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** ব্রহ্মার মানসপুত্র, একাদশ রুদ্র, অষ্টবসু, বিশ্বকর্মা ও বিভিন্ন জীবের উৎপত্তির বংশতালিকা রয়েছে।
- **Reference IDs:** brahma
- **Pending New References:** brahma
- **Detailed Prompt:**

```text
V01 P07 CH060: Brahma and celestial creation. Chapter context: ব্রহ্মার মানসপুত্র, একাদশ রুদ্র, অষ্টবসু, বিশ্বকর্মা ও বিভিন্ন জীবের উৎপত্তির বংশতালিকা রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: brahma.
```

### Chapter 061 — Divine incarnations

- **Filename:** `V01_P07_CH061_Divine_incarnations.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** দেবতা ও অসুরেরা মানবজন্মে মহাভারতের যেসব চরিত্ররূপে অবতীর্ণ হন, তাঁদের পরিচয় দেওয়া হয়েছে।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH061: Divine incarnations. Chapter context: দেবতা ও অসুরেরা মানবজন্মে মহাভারতের যেসব চরিত্ররূপে অবতীর্ণ হন, তাঁদের পরিচয় দেওয়া হয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```

### Chapter 062 — Dushyanta surveys kingdom

- **Filename:** `V01_P07_CH062_Dushyanta_surveys_kingdom.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** রাজা দুঃষন্তের রাজত্ব, প্রজাপালন, বীরত্ব ও সমৃদ্ধ সাম্রাজ্যের পরিচয় পাওয়া যায়।
- **Reference IDs:** dushyanta
- **Pending New References:** dushyanta
- **Detailed Prompt:**

```text
V01 P07 CH062: Dushyanta surveys kingdom. Chapter context: রাজা দুঃষন্তের রাজত্ব, প্রজাপালন, বীরত্ব ও সমৃদ্ধ সাম্রাজ্যের পরিচয় পাওয়া যায়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dushyanta.
```

### Chapter 063 — Dushyanta royal hunt

- **Filename:** `V01_P07_CH063_Dushyanta_royal_hunt.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** দুঃষন্তের বিশাল রাজবাহিনী নিয়ে অরণ্যে শিকারে যাওয়া এবং বনের প্রকৃতির বর্ণনা রয়েছে।
- **Reference IDs:** dushyanta
- **Pending New References:** dushyanta
- **Detailed Prompt:**

```text
V01 P07 CH063: Dushyanta royal hunt. Chapter context: দুঃষন্তের বিশাল রাজবাহিনী নিয়ে অরণ্যে শিকারে যাওয়া এবং বনের প্রকৃতির বর্ণনা রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dushyanta.
```

### Chapter 064 — Dushyanta reaches Kanva hermitage

- **Filename:** `V01_P07_CH064_Dushyanta_reaches_Kanva_hermitage.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** শিকার করতে করতে দুঃষন্ত কণ্ব ঋষির মনোরম আশ্রমে পৌঁছে আশ্রমজীবনের পরিচয় পান।
- **Reference IDs:** dushyanta, kanva
- **Pending New References:** dushyanta, kanva
- **Detailed Prompt:**

```text
V01 P07 CH064: Dushyanta reaches Kanva hermitage. Chapter context: শিকার করতে করতে দুঃষন্ত কণ্ব ঋষির মনোরম আশ্রমে পৌঁছে আশ্রমজীবনের পরিচয় পান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dushyanta, kanva.
```

### Chapter 065 — Dushyanta meets Shakuntala

- **Filename:** `V01_P07_CH065_Dushyanta_meets_Shakuntala.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** দুঃষন্তের সঙ্গে শকুন্তলার পরিচয় হয়; তাঁর জন্ম নিয়ে বিশ্বামিত্র–মেনকার কাহিনি শুরু হয়।
- **Reference IDs:** dushyanta, shakuntala
- **Pending New References:** dushyanta, shakuntala
- **Detailed Prompt:**

```text
V01 P07 CH065: Dushyanta meets Shakuntala. Chapter context: দুঃষন্তের সঙ্গে শকুন্তলার পরিচয় হয়; তাঁর জন্ম নিয়ে বিশ্বামিত্র–মেনকার কাহিনি শুরু হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dushyanta, shakuntala.
```

### Chapter 066 — Kanva finds infant Shakuntala

- **Filename:** `V01_P07_CH066_Kanva_finds_infant_Shakuntala.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** মেনকা ও বিশ্বামিত্রের কন্যা শকুন্তলার জন্ম এবং কণ্বের আশ্রমে তাঁর প্রতিপালনের ইতিহাস জানা যাবে।
- **Reference IDs:** shakuntala, kanva
- **Pending New References:** shakuntala, kanva
- **Detailed Prompt:**

```text
V01 P07 CH066: Kanva finds infant Shakuntala. Chapter context: মেনকা ও বিশ্বামিত্রের কন্যা শকুন্তলার জন্ম এবং কণ্বের আশ্রমে তাঁর প্রতিপালনের ইতিহাস জানা যাবে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: shakuntala, kanva.
```

### Chapter 067 — Dushyanta and Shakuntala marriage promise

- **Filename:** `V01_P07_CH067_Dushyanta_and_Shakuntala_marriage_promise.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** দুঃষন্ত শকুন্তলাকে বিবাহের প্রস্তাব দেন; গান্ধর্ববিবাহ ও রাজবংশের উত্তরাধিকার নিয়ে তাঁদের আলোচনা হয়।
- **Reference IDs:** dushyanta, shakuntala
- **Pending New References:** dushyanta, shakuntala
- **Detailed Prompt:**

```text
V01 P07 CH067: Dushyanta and Shakuntala marriage promise. Chapter context: দুঃষন্ত শকুন্তলাকে বিবাহের প্রস্তাব দেন; গান্ধর্ববিবাহ ও রাজবংশের উত্তরাধিকার নিয়ে তাঁদের আলোচনা হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dushyanta, shakuntala.
```

### Chapter 068 — Shakuntala brings Sarvadamana to court

- **Filename:** `V01_P07_CH068_Shakuntala_brings_Sarvadamana_to_court.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** দুঃষন্তের পুত্র সর্বদমনের শৈশব এবং পুত্রের স্বীকৃতি চেয়ে শকুন্তলার রাজসভায় উপস্থিতি রয়েছে।
- **Reference IDs:** shakuntala
- **Pending New References:** shakuntala
- **Detailed Prompt:**

```text
V01 P07 CH068: Shakuntala brings Sarvadamana to court. Chapter context: দুঃষন্তের পুত্র সর্বদমনের শৈশব এবং পুত্রের স্বীকৃতি চেয়ে শকুন্তলার রাজসভায় উপস্থিতি রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: shakuntala.
```

### Chapter 069 — Shakuntala defends son's lineage

- **Filename:** `V01_P07_CH069_Shakuntala_defends_son_s_lineage.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** শকুন্তলা সত্য, ধর্ম ও পিতৃত্বের দায়িত্ব নিয়ে যুক্তি দেন; ভরতকে রাজার পুত্ররূপে স্বীকৃতি দেওয়া হয়।
- **Reference IDs:** shakuntala
- **Pending New References:** shakuntala
- **Detailed Prompt:**

```text
V01 P07 CH069: Shakuntala defends son's lineage. Chapter context: শকুন্তলা সত্য, ধর্ম ও পিতৃত্বের দায়িত্ব নিয়ে যুক্তি দেন; ভরতকে রাজার পুত্ররূপে স্বীকৃতি দেওয়া হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: shakuntala.
```

### Chapter 070 — Royal descent from Manu to Yayati

- **Filename:** `V01_P07_CH070_Royal_descent_from_Manu_to_Yayati.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** দক্ষ, মনু, পুরূরবা, নহুষ ও যযাতি পর্যন্ত প্রাচীন রাজবংশের সূত্র ও উত্তরাধিকার আলোচনা করা হয়েছে।
- **Reference IDs:** manu, yayati
- **Pending New References:** manu, yayati
- **Detailed Prompt:**

```text
V01 P07 CH070: Royal descent from Manu to Yayati. Chapter context: দক্ষ, মনু, পুরূরবা, নহুষ ও যযাতি পর্যন্ত প্রাচীন রাজবংশের সূত্র ও উত্তরাধিকার আলোচনা করা হয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: manu, yayati.
```

### Chapter 071 — Kacha learns from Shukra

- **Filename:** `V01_P07_CH071_Kacha_learns_from_Shukra.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** কচ শুক্রাচার্যের কাছে সঞ্জীবনী বিদ্যা শিখতে গিয়ে বারবার মৃত্যুবরণ ও পুনর্জীবনের মুখোমুখি হন।
- **Reference IDs:** kacha, shukra
- **Pending New References:** kacha, shukra
- **Detailed Prompt:**

```text
V01 P07 CH071: Kacha learns from Shukra. Chapter context: কচ শুক্রাচার্যের কাছে সঞ্জীবনী বিদ্যা শিখতে গিয়ে বারবার মৃত্যুবরণ ও পুনর্জীবনের মুখোমুখি হন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: kacha, shukra.
```

### Chapter 072 — Kacha and Devayani exchange curses

- **Filename:** `V01_P07_CH072_Kacha_and_Devayani_exchange_curses.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** শিক্ষা শেষ করে কচ ফিরে যেতে চাইলে দেবযানীর সঙ্গে তাঁর সংলাপ ও পরস্পরের অভিশাপ ঘটে।
- **Reference IDs:** kacha, devayani
- **Pending New References:** kacha, devayani
- **Detailed Prompt:**

```text
V01 P07 CH072: Kacha and Devayani exchange curses. Chapter context: শিক্ষা শেষ করে কচ ফিরে যেতে চাইলে দেবযানীর সঙ্গে তাঁর সংলাপ ও পরস্পরের অভিশাপ ঘটে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: kacha, devayani.
```

### Chapter 073 — Yayati rescues Devayani

- **Filename:** `V01_P07_CH073_Yayati_rescues_Devayani.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** দেবযানী ও শর্মিষ্ঠার বিরোধ, দেবযানীর কূপে পতন এবং যযাতির সঙ্গে তাঁর প্রথম সাক্ষাৎ ঘটে।
- **Reference IDs:** yayati, devayani
- **Pending New References:** yayati, devayani
- **Detailed Prompt:**

```text
V01 P07 CH073: Yayati rescues Devayani. Chapter context: দেবযানী ও শর্মিষ্ঠার বিরোধ, দেবযানীর কূপে পতন এবং যযাতির সঙ্গে তাঁর প্রথম সাক্ষাৎ ঘটে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yayati, devayani.
```

### Chapter 074 — Shukra counsels Devayani

- **Filename:** `V01_P07_CH074_Shukra_counsels_Devayani.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** শুক্রাচার্য দেবযানীকে ক্রোধসংযম, ক্ষমা এবং অপমানের প্রতিক্রিয়া সম্পর্কে উপদেশ দেন।
- **Reference IDs:** shukra, devayani
- **Pending New References:** shukra, devayani
- **Detailed Prompt:**

```text
V01 P07 CH074: Shukra counsels Devayani. Chapter context: শুক্রাচার্য দেবযানীকে ক্রোধসংযম, ক্ষমা এবং অপমানের প্রতিক্রিয়া সম্পর্কে উপদেশ দেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: shukra, devayani.
```

### Chapter 075 — Shukra confronts Vrishaparva

- **Filename:** `V01_P07_CH075_Shukra_confronts_Vrishaparva.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** দেবযানীর অপমানে শুক্র বৃষপর্বাকে তিরস্কার করেন; শর্মিষ্ঠা দেবযানীর সেবায় সম্মত হন।
- **Reference IDs:** shukra, vrishaparva
- **Pending New References:** shukra, vrishaparva
- **Detailed Prompt:**

```text
V01 P07 CH075: Shukra confronts Vrishaparva. Chapter context: দেবযানীর অপমানে শুক্র বৃষপর্বাকে তিরস্কার করেন; শর্মিষ্ঠা দেবযানীর সেবায় সম্মত হন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: shukra, vrishaparva.
```

### Chapter 076 — Yayati and Devayani discuss marriage

- **Filename:** `V01_P07_CH076_Yayati_and_Devayani_discuss_marriage.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** যযাতি দেবযানীর সঙ্গে পুনরায় সাক্ষাৎ করেন; বিবাহ ও সামাজিক বিধান নিয়ে তাঁদের কথোপকথন হয়।
- **Reference IDs:** yayati, devayani
- **Pending New References:** yayati, devayani
- **Detailed Prompt:**

```text
V01 P07 CH076: Yayati and Devayani discuss marriage. Chapter context: যযাতি দেবযানীর সঙ্গে পুনরায় সাক্ষাৎ করেন; বিবাহ ও সামাজিক বিধান নিয়ে তাঁদের কথোপকথন হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yayati, devayani.
```

### Chapter 077 — Sharmishtha approaches Yayati

- **Filename:** `V01_P07_CH077_Sharmishtha_approaches_Yayati.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** যযাতির অন্তঃপুরে দেবযানী ও শর্মিষ্ঠার জীবনে পরিবর্তন আসে; শর্মিষ্ঠার সন্তানলাভের ঘটনা ঘটে।
- **Reference IDs:** yayati, sharmishtha
- **Pending New References:** yayati, sharmishtha
- **Detailed Prompt:**

```text
V01 P07 CH077: Sharmishtha approaches Yayati. Chapter context: যযাতির অন্তঃপুরে দেবযানী ও শর্মিষ্ঠার জীবনে পরিবর্তন আসে; শর্মিষ্ঠার সন্তানলাভের ঘটনা ঘটে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yayati, sharmishtha.
```

### Chapter 078 — Shukra curses Yayati

- **Filename:** `V01_P07_CH078_Shukra_curses_Yayati.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** শর্মিষ্ঠার সন্তানদের পরিচয় প্রকাশিত হলে দেবযানী ক্ষুব্ধ হন; শুক্রের অভিশাপে যযাতি অকালে বৃদ্ধ হয়ে পড়েন।
- **Reference IDs:** yayati, shukra
- **Pending New References:** yayati, shukra
- **Detailed Prompt:**

```text
V01 P07 CH078: Shukra curses Yayati. Chapter context: শর্মিষ্ঠার সন্তানদের পরিচয় প্রকাশিত হলে দেবযানী ক্ষুব্ধ হন; শুক্রের অভিশাপে যযাতি অকালে বৃদ্ধ হয়ে পড়েন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yayati, shukra.
```

### Chapter 079 — Puru accepts father's old age

- **Filename:** `V01_P07_CH079_Puru_accepts_father_s_old_age.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** যযাতি পাঁচ পুত্রের কাছে নিজের বার্ধক্যের বিনিময়ে যৌবন চান; কনিষ্ঠ পুরু তাঁর প্রস্তাবে সম্মত হন।
- **Reference IDs:** puru
- **Pending New References:** puru
- **Detailed Prompt:**

```text
V01 P07 CH079: Puru accepts father's old age. Chapter context: যযাতি পাঁচ পুত্রের কাছে নিজের বার্ধক্যের বিনিময়ে যৌবন চান; কনিষ্ঠ পুরু তাঁর প্রস্তাবে সম্মত হন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: puru.
```

### Chapter 080 — Yayati crowns Puru

- **Filename:** `V01_P07_CH080_Yayati_crowns_Puru.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** পুরুর যৌবন নিয়ে যযাতি দীর্ঘকাল সুখভোগ করেন; পরে বার্ধক্য ফিরিয়ে দিয়ে পুরুকে রাজ্যাভিষিক্ত করেন।
- **Reference IDs:** yayati, puru
- **Pending New References:** yayati, puru
- **Detailed Prompt:**

```text
V01 P07 CH080: Yayati crowns Puru. Chapter context: পুরুর যৌবন নিয়ে যযাতি দীর্ঘকাল সুখভোগ করেন; পরে বার্ধক্য ফিরিয়ে দিয়ে পুরুকে রাজ্যাভিষিক্ত করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yayati, puru.
```

### Chapter 081 — Yayati ascends from forest

- **Filename:** `V01_P07_CH081_Yayati_ascends_from_forest.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** পুত্রকে রাজ্য দিয়ে যযাতি বনবাস ও কঠোর তপস্যা করেন; স্বর্গে গিয়েও তাঁর পতনের পটভূমি তৈরি হয়।
- **Reference IDs:** yayati
- **Pending New References:** yayati
- **Detailed Prompt:**

```text
V01 P07 CH081: Yayati ascends from forest. Chapter context: পুত্রকে রাজ্য দিয়ে যযাতি বনবাস ও কঠোর তপস্যা করেন; স্বর্গে গিয়েও তাঁর পতনের পটভূমি তৈরি হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yayati.
```

### Chapter 082 — Yayati and Indra discuss virtue

- **Filename:** `V01_P07_CH082_Yayati_and_Indra_discuss_virtue.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** ইন্দ্রের সঙ্গে কথোপকথনে যযাতি সত্য, ক্ষমা, সংযম ও মধুর বাক্যের গুরুত্ব ব্যাখ্যা করেন।
- **Reference IDs:** indra, yayati
- **Pending New References:** indra, yayati
- **Detailed Prompt:**

```text
V01 P07 CH082: Yayati and Indra discuss virtue. Chapter context: ইন্দ্রের সঙ্গে কথোপকথনে যযাতি সত্য, ক্ষমা, সংযম ও মধুর বাক্যের গুরুত্ব ব্যাখ্যা করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: indra, yayati.
```

### Chapter 083 — Yayati falls and meets Ashtaka

- **Filename:** `V01_P07_CH083_Yayati_falls_and_meets_Ashtaka.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** তপস্যায় নিজের শ্রেষ্ঠত্ব দাবি করায় যযাতির পুণ্য ক্ষয় হয়; পতনের সময় রাজর্ষি অষ্টকের সঙ্গে সাক্ষাৎ ঘটে।
- **Reference IDs:** yayati, ashtaka
- **Pending New References:** yayati, ashtaka
- **Detailed Prompt:**

```text
V01 P07 CH083: Yayati falls and meets Ashtaka. Chapter context: তপস্যায় নিজের শ্রেষ্ঠত্ব দাবি করায় যযাতির পুণ্য ক্ষয় হয়; পতনের সময় রাজর্ষি অষ্টকের সঙ্গে সাক্ষাৎ ঘটে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yayati, ashtaka.
```

### Chapter 084 — Yayati counsels Ashtaka

- **Filename:** `V01_P07_CH084_Yayati_counsels_Ashtaka.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** অষ্টকের প্রশ্নে যযাতি বিনয়, দৈব ও সুখদুঃখের অনিত্যতা ব্যাখ্যা করেন; স্বর্গের বিভিন্ন লোকে তাঁর অবস্থান ও পতনের কারণ বলেন।
- **Reference IDs:** yayati, ashtaka
- **Pending New References:** yayati, ashtaka
- **Detailed Prompt:**

```text
V01 P07 CH084: Yayati counsels Ashtaka. Chapter context: অষ্টকের প্রশ্নে যযাতি বিনয়, দৈব ও সুখদুঃখের অনিত্যতা ব্যাখ্যা করেন; স্বর্গের বিভিন্ন লোকে তাঁর অবস্থান ও পতনের কারণ বলেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yayati, ashtaka.
```

### Chapter 085 — Yayati explains karma and rebirth

- **Filename:** `V01_P07_CH085_Yayati_explains_karma_and_rebirth.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** অষ্টক জানতে চান পুণ্যক্ষয়, পুনর্জন্ম ও গর্ভধারণের প্রকৃতি; যযাতি কর্মফল, সংযম ও উচ্চতর লোকপ্রাপ্তির পথ আলোচনা করেন।
- **Reference IDs:** yayati
- **Pending New References:** yayati
- **Detailed Prompt:**

```text
V01 P07 CH085: Yayati explains karma and rebirth. Chapter context: অষ্টক জানতে চান পুণ্যক্ষয়, পুনর্জন্ম ও গর্ভধারণের প্রকৃতি; যযাতি কর্মফল, সংযম ও উচ্চতর লোকপ্রাপ্তির পথ আলোচনা করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yayati.
```

### Chapter 086 — Yayati explains four stages of life

- **Filename:** `V01_P07_CH086_Yayati_explains_four_stages_of_life.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** অষ্টক চার আশ্রমের কর্তব্য জানতে চাইলে যযাতি ব্রহ্মচর্য, গার্হস্থ্য, বনপ্রস্থ ও ভিক্ষুজীবনের আদর্শ ব্যাখ্যা করেন।
- **Reference IDs:** yayati
- **Pending New References:** yayati
- **Detailed Prompt:**

```text
V01 P07 CH086: Yayati explains four stages of life. Chapter context: অষ্টক চার আশ্রমের কর্তব্য জানতে চাইলে যযাতি ব্রহ্মচর্য, গার্হস্থ্য, বনপ্রস্থ ও ভিক্ষুজীবনের আদর্শ ব্যাখ্যা করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yayati.
```

### Chapter 087 — Yayati refuses heavenly gifts

- **Filename:** `V01_P07_CH087_Yayati_refuses_heavenly_gifts.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** গৃহী ও সন্ন্যাসীর মুক্তির পথ নিয়ে প্রশ্নের পর অষ্টক ও প্রতর্দন যযাতিকে নিজেদের স্বর্গলোক দান করতে চান; যযাতি তা প্রত্যাখ্যান করেন।
- **Reference IDs:** yayati
- **Pending New References:** yayati
- **Detailed Prompt:**

```text
V01 P07 CH087: Yayati refuses heavenly gifts. Chapter context: গৃহী ও সন্ন্যাসীর মুক্তির পথ নিয়ে প্রশ্নের পর অষ্টক ও প্রতর্দন যযাতিকে নিজেদের স্বর্গলোক দান করতে চান; যযাতি তা প্রত্যাখ্যান করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yayati.
```

### Chapter 088 — Five celestial chariots

- **Filename:** `V01_P07_CH088_Five_celestial_chariots.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** বসুমনা ও শিবির দানের প্রস্তাব, পাঁচটি দিব্য রথের আবির্ভাব এবং যযাতির সঙ্গে চার রাজর্ষির স্বর্গারোহণের কাহিনি রয়েছে।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH088: Five celestial chariots. Chapter context: বসুমনা ও শিবির দানের প্রস্তাব, পাঁচটি দিব্য রথের আবির্ভাব এবং যযাতির সঙ্গে চার রাজর্ষির স্বর্গারোহণের কাহিনি রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```

### Chapter 089 — Puru dynasty and Samvarana

- **Filename:** `V01_P07_CH089_Puru_dynasty_and_Samvarana.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** পুরুবংশের প্রাচীন রাজাদের বংশধারা, ভরত ও ভূমন্যুর উত্তরাধিকার, সংবরণের রাজ্যচ্যুতি ও প্রত্যাবর্তন এবং কুরুর জন্মের বৃত্তান্ত।
- **Reference IDs:** puru, samvarana
- **Pending New References:** puru, samvarana
- **Detailed Prompt:**

```text
V01 P07 CH089: Puru dynasty and Samvarana. Chapter context: পুরুবংশের প্রাচীন রাজাদের বংশধারা, ভরত ও ভূমন্যুর উত্তরাধিকার, সংবরণের রাজ্যচ্যুতি ও প্রত্যাবর্তন এবং কুরুর জন্মের বৃত্তান্ত।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: puru, samvarana.
```

### Chapter 090 — Manu to Pandavas royal lineage

- **Filename:** `V01_P07_CH090_Manu_to_Pandavas_royal_lineage.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** মনু থেকে পুরু, ভরত, কুরু, শান্তনু ও পাণ্ডবদের বিস্তৃত বংশপরিচয়; পাণ্ডবপুত্রদের পরিচয় এবং পরীক্ষিৎ ও জনমেজয়ের উত্তরাধিকার।
- **Reference IDs:** janamejaya, shantanu, manu, yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** manu
- **Detailed Prompt:**

```text
V01 P07 CH090: Manu to Pandavas royal lineage. Chapter context: মনু থেকে পুরু, ভরত, কুরু, শান্তনু ও পাণ্ডবদের বিস্তৃত বংশপরিচয়; পাণ্ডবপুত্রদের পরিচয় এবং পরীক্ষিৎ ও জনমেজয়ের উত্তরাধিকার।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: janamejaya, shantanu, manu, yudhishthira, bhima, arjuna, nakula, sahadeva.
```

### Chapter 091 — Vasus appeal to Ganga

- **Filename:** `V01_P07_CH091_Vasus_appeal_to_Ganga.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** রাজা মহাভীষের ব্রহ্মার অভিশাপ, অষ্টবসুর বশিষ্ঠের অভিশাপ এবং গঙ্গার কাছে তাঁদের মানবজন্ম থেকে মুক্তির প্রার্থনা।
- **Reference IDs:** ganga
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH091: Vasus appeal to Ganga. Chapter context: রাজা মহাভীষের ব্রহ্মার অভিশাপ, অষ্টবসুর বশিষ্ঠের অভিশাপ এবং গঙ্গার কাছে তাঁদের মানবজন্ম থেকে মুক্তির প্রার্থনা।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: ganga.
```

### Chapter 092 — Shantanu stops Ganga

- **Filename:** `V01_P07_CH092_Shantanu_stops_Ganga.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** প্রতীপের সঙ্গে গঙ্গার সাক্ষাৎ, শান্তনু–গঙ্গার শর্তসাপেক্ষ বিবাহ, সাত সন্তানের বিসর্জন এবং অষ্টম পুত্র গঙ্গাদত্তের রক্ষা।
- **Reference IDs:** shantanu, ganga
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH092: Shantanu stops Ganga. Chapter context: প্রতীপের সঙ্গে গঙ্গার সাক্ষাৎ, শান্তনু–গঙ্গার শর্তসাপেক্ষ বিবাহ, সাত সন্তানের বিসর্জন এবং অষ্টম পুত্র গঙ্গাদত্তের রক্ষা।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: shantanu, ganga.
```

### Chapter 093 — Vasishtha discovers stolen cow

- **Filename:** `V01_P07_CH093_Vasishtha_discovers_stolen_cow.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** বশিষ্ঠের ইচ্ছাপূরণকারী গাভী চুরির জন্য অষ্টবসুর অভিশাপ, দ্যৌর দীর্ঘ মানবজীবন এবং দেবব্রত তথা গাঙ্গেয়ের পরিচয়।
- **Reference IDs:** vasishtha
- **Pending New References:** vasishtha
- **Detailed Prompt:**

```text
V01 P07 CH093: Vasishtha discovers stolen cow. Chapter context: বশিষ্ঠের ইচ্ছাপূরণকারী গাভী চুরির জন্য অষ্টবসুর অভিশাপ, দ্যৌর দীর্ঘ মানবজীবন এবং দেবব্রত তথা গাঙ্গেয়ের পরিচয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vasishtha.
```

### Chapter 094 — Young Devavrata takes Bhishma vow

- **Filename:** `V01_P07_CH094_Young_Devavrata_takes_Bhishma_vow.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** দেবব্রতকে শিক্ষিত যুবকরূপে ফিরিয়ে দিয়ে গঙ্গা তাঁকে শান্তনুর হাতে সমর্পণ করেন। পরে সত্যবতীকে বিবাহের জন্য তাঁর পিতা উত্তরাধিকারসংক্রান্ত শর্ত দিলে দেবব্রত রাজ্য ও সন্তানলাভের অধিকার ত্যাগের দুরূহ প্রতিজ্ঞা করেন; এখানেই তাঁর ‘ভীষ্ম’ নামের উৎপত্তি।
- **Reference IDs:** shantanu, ganga, satyavati, bhishma
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH094: Young Devavrata takes Bhishma vow. Chapter context: দেবব্রতকে শিক্ষিত যুবকরূপে ফিরিয়ে দিয়ে গঙ্গা তাঁকে শান্তনুর হাতে সমর্পণ করেন। পরে সত্যবতীকে বিবাহের জন্য তাঁর পিতা উত্তরাধিকারসংক্রান্ত শর্ত দিলে দেবব্রত রাজ্য ও সন্তানলাভের অধিকার ত্যাগের দুরূহ প্রতিজ্ঞা করেন; এখানেই তাঁর ‘ভীষ্ম’ নামের উৎপত্তি।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: shantanu, ganga, satyavati, bhishma.
```

### Chapter 095 — Chitrangada and Gandharva duel

- **Filename:** `V01_P07_CH095_Chitrangada_and_Gandharva_duel.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** শান্তনু ও সত্যবতীর দুই পুত্র চিত্রাঙ্গদ ও বিচিত্রবীর্যের পরিচয় দিয়ে কাহিনি এগোয়। শান্তনুর মৃত্যুর পরে চিত্রাঙ্গদের রাজত্ব, সমনামী গন্ধর্বরাজের সঙ্গে দীর্ঘ যুদ্ধ ও তাঁর মৃত্যু এবং অল্পবয়সী বিচিত্রবীর্যের রাজ্যাভিষেক বর্ণিত হয়।
- **Reference IDs:** shantanu, satyavati, chitrangada
- **Pending New References:** chitrangada
- **Detailed Prompt:**

```text
V01 P07 CH095: Chitrangada and Gandharva duel. Chapter context: শান্তনু ও সত্যবতীর দুই পুত্র চিত্রাঙ্গদ ও বিচিত্রবীর্যের পরিচয় দিয়ে কাহিনি এগোয়। শান্তনুর মৃত্যুর পরে চিত্রাঙ্গদের রাজত্ব, সমনামী গন্ধর্বরাজের সঙ্গে দীর্ঘ যুদ্ধ ও তাঁর মৃত্যু এবং অল্পবয়সী বিচিত্রবীর্যের রাজ্যাভিষেক বর্ণিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: shantanu, satyavati, chitrangada.
```

### Chapter 096 — Bhishma leaves Kashi svayamvara

- **Filename:** `V01_P07_CH096_Bhishma_leaves_Kashi_svayamvara.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** কনিষ্ঠ ভ্রাতা বিচিত্রবীর্যের জন্য ভীষ্ম কাশীরাজের তিন কন্যাকে স্বয়ংবরসভা থেকে নিয়ে আসেন এবং সমবেত রাজাদের সঙ্গে যুদ্ধ করেন। অম্বার পূর্বনির্বাচিত পাত্রের বিষয়টি প্রকাশ পাওয়ার পর তাঁর মুক্তি, অম্বিকা–অম্বালিকার বিবাহ এবং বিচিত্রবীর্যের অকালমৃত্যুর ঘটনা আসে।
- **Reference IDs:** bhishma, ambika, ambalika
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH096: Bhishma leaves Kashi svayamvara. Chapter context: কনিষ্ঠ ভ্রাতা বিচিত্রবীর্যের জন্য ভীষ্ম কাশীরাজের তিন কন্যাকে স্বয়ংবরসভা থেকে নিয়ে আসেন এবং সমবেত রাজাদের সঙ্গে যুদ্ধ করেন। অম্বার পূর্বনির্বাচিত পাত্রের বিষয়টি প্রকাশ পাওয়ার পর তাঁর মুক্তি, অম্বিকা–অম্বালিকার বিবাহ এবং বিচিত্রবীর্যের অকালমৃত্যুর ঘটনা আসে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhishma, ambika, ambalika.
```

### Chapter 097 — Satyavati asks Bhishma to preserve lineage

- **Filename:** `V01_P07_CH097_Satyavati_asks_Bhishma_to_preserve_lineage.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** বিচিত্রবীর্যের নিঃসন্তান মৃত্যুতে কুরুবংশের উত্তরাধিকার সংকটে পড়ে। সত্যবতী ভীষ্মকে বংশরক্ষার জন্য অনুরোধ করেন; ভীষ্ম নিজের অটল প্রতিজ্ঞা বজায় রেখে বিপৎকালীন ধর্ম সম্পর্কে অন্য উপায় খোঁজার প্রস্তাব দেন।
- **Reference IDs:** satyavati, bhishma
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH097: Satyavati asks Bhishma to preserve lineage. Chapter context: বিচিত্রবীর্যের নিঃসন্তান মৃত্যুতে কুরুবংশের উত্তরাধিকার সংকটে পড়ে। সত্যবতী ভীষ্মকে বংশরক্ষার জন্য অনুরোধ করেন; ভীষ্ম নিজের অটল প্রতিজ্ঞা বজায় রেখে বিপৎকালীন ধর্ম সম্পর্কে অন্য উপায় খোঁজার প্রস্তাব দেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: satyavati, bhishma.
```

### Chapter 098 — Bhishma recounts Dirghatamas and Bali

- **Filename:** `V01_P07_CH098_Bhishma_recounts_Dirghatamas_and_Bali.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** বংশরক্ষার বিকল্প পথ বোঝাতে ভীষ্ম পরশুরামের ক্ষত্রিয়বিনাশের পর ক্ষত্রিয়বংশ পুনরুজ্জীবনের কথা বলেন। বৃহস্পতি–মমতা, ঋষি দীর্ঘতমা, রাজা বলি ও সুদেষ্ণার ঘটনায় প্রাচীন বংশধারা ও পিতৃত্বের বিধান আলোচিত হয়।
- **Reference IDs:** bhishma, dirghatamas, bali
- **Pending New References:** dirghatamas, bali
- **Detailed Prompt:**

```text
V01 P07 CH098: Bhishma recounts Dirghatamas and Bali. Chapter context: বংশরক্ষার বিকল্প পথ বোঝাতে ভীষ্ম পরশুরামের ক্ষত্রিয়বিনাশের পর ক্ষত্রিয়বংশ পুনরুজ্জীবনের কথা বলেন। বৃহস্পতি–মমতা, ঋষি দীর্ঘতমা, রাজা বলি ও সুদেষ্ণার ঘটনায় প্রাচীন বংশধারা ও পিতৃত্বের বিধান আলোচিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhishma, dirghatamas, bali.
```

### Chapter 099 — Satyavati reveals Parashara encounter

- **Filename:** `V01_P07_CH099_Satyavati_reveals_Parashara_encounter.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** কুরুবংশের উত্তরাধিকার-সংকটে ভীষ্মের পরামর্শ শুনে সত্যবতী ঋষি পরাশরের সঙ্গে তাঁর অতীত সাক্ষাৎ, কৃষ্ণদ্বৈপায়ন ব্যাসের জন্ম এবং বেদবিভাগের কথা প্রকাশ করেন। ভীষ্মের অনুমতিতে ব্যাসকে ডেকে অম্বিকা–অম্বালিকার মাধ্যমে বংশরক্ষার ব্যবস্থা করা হয়।
- **Reference IDs:** vyasa, satyavati, bhishma, ambika, ambalika, krishna, parashara
- **Pending New References:** parashara
- **Detailed Prompt:**

```text
V01 P07 CH099: Satyavati reveals Parashara encounter. Chapter context: কুরুবংশের উত্তরাধিকার-সংকটে ভীষ্মের পরামর্শ শুনে সত্যবতী ঋষি পরাশরের সঙ্গে তাঁর অতীত সাক্ষাৎ, কৃষ্ণদ্বৈপায়ন ব্যাসের জন্ম এবং বেদবিভাগের কথা প্রকাশ করেন। ভীষ্মের অনুমতিতে ব্যাসকে ডেকে অম্বিকা–অম্বালিকার মাধ্যমে বংশরক্ষার ব্যবস্থা করা হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa, satyavati, bhishma, ambika, ambalika, krishna, parashara.
```

### Chapter 100 — Births of Dhritarashtra Pandu Vidura

- **Filename:** `V01_P07_CH100_Births_of_Dhritarashtra_Pandu_Vidura.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** সত্যবতীর অনুরোধে ব্যাস প্রথমে অম্বিকার, পরে অম্বালিকার এবং শেষে অম্বিকার পাঠানো এক দাসীর সঙ্গে মিলিত হন। তাঁদের গর্ভে যথাক্রমে ধৃতরাষ্ট্র, পাণ্ডু ও বিদুরের জন্ম হয়; তাঁদের জন্মপরিস্থিতি ও ভবিষ্যৎ গুণাবলি বর্ণিত হয়েছে।
- **Reference IDs:** vyasa, satyavati, ambika, ambalika, dhritarashtra, pandu, vidura
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH100: Births of Dhritarashtra Pandu Vidura. Chapter context: সত্যবতীর অনুরোধে ব্যাস প্রথমে অম্বিকার, পরে অম্বালিকার এবং শেষে অম্বিকার পাঠানো এক দাসীর সঙ্গে মিলিত হন। তাঁদের গর্ভে যথাক্রমে ধৃতরাষ্ট্র, পাণ্ডু ও বিদুরের জন্ম হয়; তাঁদের জন্মপরিস্থিতি ও ভবিষ্যৎ গুণাবলি বর্ণিত হয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa, satyavati, ambika, ambalika, dhritarashtra, pandu, vidura.
```

### Chapter 101 — Mandavya questions Dharma

- **Filename:** `V01_P07_CH101_Mandavya_questions_Dharma.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** বিদুর কেন ধর্মের অবতার, তা জানতে চাইলে বৈশম্পায়ন ঋষি মাণ্ডব্যের কাহিনি বলেন। চোরদের আশ্রয় দেওয়ার মিথ্যা অভিযোগে শূলবিদ্ধ হওয়া ঋষি ধর্মের কাছে নিজের শাস্তির কারণ জানতে চান এবং অন্যায় দণ্ডের জন্য ধর্মকে মানুষ হয়ে জন্মানোর অভিশাপ দেন।
- **Reference IDs:** vaishampayana, vidura, mandavya, dharma
- **Pending New References:** mandavya, dharma
- **Detailed Prompt:**

```text
V01 P07 CH101: Mandavya questions Dharma. Chapter context: বিদুর কেন ধর্মের অবতার, তা জানতে চাইলে বৈশম্পায়ন ঋষি মাণ্ডব্যের কাহিনি বলেন। চোরদের আশ্রয় দেওয়ার মিথ্যা অভিযোগে শূলবিদ্ধ হওয়া ঋষি ধর্মের কাছে নিজের শাস্তির কারণ জানতে চান এবং অন্যায় দণ্ডের জন্য ধর্মকে মানুষ হয়ে জন্মানোর অভিশাপ দেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vaishampayana, vidura, mandavya, dharma.
```

### Chapter 102 — Pandu accepts royal throne

- **Filename:** `V01_P07_CH102_Pandu_accepts_royal_throne.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** ধৃতরাষ্ট্র, পাণ্ডু ও বিদুরের জন্মের পরে কুরুরাজ্যের সমৃদ্ধি, ভীষ্মের শাসনরক্ষা, তিন রাজপুত্রের শিক্ষা ও দক্ষতার পরিচয় দেওয়া হয়েছে। ধৃতরাষ্ট্রের অন্ধত্ব এবং বিদুরের জন্মপরিচয়ের কারণে পাণ্ডু রাজ্যভার গ্রহণ করেন।
- **Reference IDs:** bhishma, dhritarashtra, pandu, vidura
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH102: Pandu accepts royal throne. Chapter context: ধৃতরাষ্ট্র, পাণ্ডু ও বিদুরের জন্মের পরে কুরুরাজ্যের সমৃদ্ধি, ভীষ্মের শাসনরক্ষা, তিন রাজপুত্রের শিক্ষা ও দক্ষতার পরিচয় দেওয়া হয়েছে। ধৃতরাষ্ট্রের অন্ধত্ব এবং বিদুরের জন্মপরিচয়ের কারণে পাণ্ডু রাজ্যভার গ্রহণ করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhishma, dhritarashtra, pandu, vidura.
```

### Chapter 103 — Gandhari binds her eyes

- **Filename:** `V01_P07_CH103_Gandhari_binds_her_eyes.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** বংশের ভবিষ্যৎ নিরাপদ করার জন্য ভীষ্ম বিদুরের সঙ্গে তিন রাজকন্যার বিবাহসংক্রান্ত আলোচনা করেন। গান্ধাররাজ সুবল ধৃতরাষ্ট্রের সঙ্গে গান্ধারীর বিবাহে সম্মত হন; স্বামীর অন্ধত্বের কথা জেনে গান্ধারী নিজের চোখ বেঁধে রাখার সংকল্প নেন।
- **Reference IDs:** bhishma, dhritarashtra, gandhari, vidura
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH103: Gandhari binds her eyes. Chapter context: বংশের ভবিষ্যৎ নিরাপদ করার জন্য ভীষ্ম বিদুরের সঙ্গে তিন রাজকন্যার বিবাহসংক্রান্ত আলোচনা করেন। গান্ধাররাজ সুবল ধৃতরাষ্ট্রের সঙ্গে গান্ধারীর বিবাহে সম্মত হন; স্বামীর অন্ধত্বের কথা জেনে গান্ধারী নিজের চোখ বেঁধে রাখার সংকল্প নেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhishma, dhritarashtra, gandhari, vidura.
```

### Chapter 104 — Kunti sets infant Karna afloat

- **Filename:** `V01_P07_CH104_Kunti_sets_infant_Karna_afloat.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** যাদব রাজা শূরের কন্যা পৃথা কুন্তিভোজের পালিত কন্যা হন। দুর্বাসা ঋষির কাছ থেকে দেবতা আহ্বানের মন্ত্র পেয়ে তিনি সূর্যদেবের অনুগ্রহে কর্ণের জন্ম দেন। গোপনে শিশুকে ভাসিয়ে দেওয়া, অধিরথ–রাধার কাছে তাঁর লালনপালন এবং ইন্দ্রকে সহজাত কবচ-কুণ্ডল দানের ঘটনা এখানে বর্ণিত।
- **Reference IDs:** karna, kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH104: Kunti sets infant Karna afloat. Chapter context: যাদব রাজা শূরের কন্যা পৃথা কুন্তিভোজের পালিত কন্যা হন। দুর্বাসা ঋষির কাছ থেকে দেবতা আহ্বানের মন্ত্র পেয়ে তিনি সূর্যদেবের অনুগ্রহে কর্ণের জন্ম দেন। গোপনে শিশুকে ভাসিয়ে দেওয়া, অধিরথ–রাধার কাছে তাঁর লালনপালন এবং ইন্দ্রকে সহজাত কবচ-কুণ্ডল দানের ঘটনা এখানে বর্ণিত।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: karna, kunti.
```

### Chapter 105 — Pandu and Madri wedding

- **Filename:** `V01_P07_CH105_Pandu_and_Madri_wedding.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** কুন্তীর স্বয়ংবরে পাণ্ডুর সঙ্গে তাঁর বিবাহ এবং ভীষ্মের উদ্যোগে মাদ্রীর সঙ্গে পাণ্ডুর দ্বিতীয় বিবাহ হয়। এরপর পাণ্ডু দশার্ণ, মগধ, বিদেহসহ একাধিক রাজ্য জয় করে বিপুল ধনসম্পদ নিয়ে হস্তিনাপুরে বিজয়ীর বেশে ফেরেন।
- **Reference IDs:** bhishma, pandu, kunti, madri
- **Pending New References:** madri
- **Detailed Prompt:**

```text
V01 P07 CH105: Pandu and Madri wedding. Chapter context: কুন্তীর স্বয়ংবরে পাণ্ডুর সঙ্গে তাঁর বিবাহ এবং ভীষ্মের উদ্যোগে মাদ্রীর সঙ্গে পাণ্ডুর দ্বিতীয় বিবাহ হয়। এরপর পাণ্ডু দশার্ণ, মগধ, বিদেহসহ একাধিক রাজ্য জয় করে বিপুল ধনসম্পদ নিয়ে হস্তিনাপুরে বিজয়ীর বেশে ফেরেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhishma, pandu, kunti, madri.
```

### Chapter 106 — Pandu distributes wealth before forest exile

- **Filename:** `V01_P07_CH106_Pandu_distributes_wealth_before_forest_exile.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** পাণ্ডু দিগ্বিজয়ে প্রাপ্ত ধনসম্পদ ভীষ্ম, সত্যবতী, মাতা ও আত্মীয়দের মধ্যে বিতরণ করেন। পরে কুন্তী ও মাদ্রীকে নিয়ে হিমালয়ের অরণ্যে বসবাস শুরু করেন। এদিকে ভীষ্ম রাজা দেবকের এক কন্যার সঙ্গে বিদুরের বিবাহের ব্যবস্থা করেন।
- **Reference IDs:** satyavati, bhishma, pandu, vidura, kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH106: Pandu distributes wealth before forest exile. Chapter context: পাণ্ডু দিগ্বিজয়ে প্রাপ্ত ধনসম্পদ ভীষ্ম, সত্যবতী, মাতা ও আত্মীয়দের মধ্যে বিতরণ করেন। পরে কুন্তী ও মাদ্রীকে নিয়ে হিমালয়ের অরণ্যে বসবাস শুরু করেন। এদিকে ভীষ্ম রাজা দেবকের এক কন্যার সঙ্গে বিদুরের বিবাহের ব্যবস্থা করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: satyavati, bhishma, pandu, vidura, kunti.
```

### Chapter 107 — Vyasa oversees jars of Kuru heirs

- **Filename:** `V01_P07_CH107_Vyasa_oversees_jars_of_Kuru_heirs.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** জনমেজয়ের প্রশ্নের জবাবে বৈশম্পায়ন গান্ধারীর দুই বছরের গর্ভধারণ, ব্যাসের নির্দেশে মাংসপিণ্ডের খণ্ডগুলি ঘিয়ের পাত্রে রাখা, দুর্যোধনের জন্মের অমঙ্গললক্ষণ এবং যুযুৎসু ও দুঃশলার জন্ম ব্যাখ্যা করেন।
- **Reference IDs:** vyasa, vaishampayana, janamejaya, gandhari, duryodhana, kuru
- **Pending New References:** kuru
- **Detailed Prompt:**

```text
V01 P07 CH107: Vyasa oversees jars of Kuru heirs. Chapter context: জনমেজয়ের প্রশ্নের জবাবে বৈশম্পায়ন গান্ধারীর দুই বছরের গর্ভধারণ, ব্যাসের নির্দেশে মাংসপিণ্ডের খণ্ডগুলি ঘিয়ের পাত্রে রাখা, দুর্যোধনের জন্মের অমঙ্গললক্ষণ এবং যুযুৎসু ও দুঃশলার জন্ম ব্যাখ্যা করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa, vaishampayana, janamejaya, gandhari, duryodhana, kuru.
```

### Chapter 108 — Kuru princes and Duhshala

- **Filename:** `V01_P07_CH108_Kuru_princes_and_Duhshala.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** জনমেজয় ধৃতরাষ্ট্রের সন্তানদের নাম জানতে চান। বৈশম্পায়ন জন্মক্রম অনুযায়ী তাঁদের দীর্ঘ নামতালিকা দেন; এরপর রাজপুত্রদের শিক্ষা ও বিবাহ এবং দুঃশলার সঙ্গে সিন্ধুরাজ জয়দ্রথের বিবাহের কথা বলেন। উৎসের তালিকায় থাকা সংখ্যাগত অসংগতিও টীকায় চিহ্নিত।
- **Reference IDs:** vaishampayana, janamejaya, dhritarashtra, kuru, duhshala
- **Pending New References:** kuru, duhshala
- **Detailed Prompt:**

```text
V01 P07 CH108: Kuru princes and Duhshala. Chapter context: জনমেজয় ধৃতরাষ্ট্রের সন্তানদের নাম জানতে চান। বৈশম্পায়ন জন্মক্রম অনুযায়ী তাঁদের দীর্ঘ নামতালিকা দেন; এরপর রাজপুত্রদের শিক্ষা ও বিবাহ এবং দুঃশলার সঙ্গে সিন্ধুরাজ জয়দ্রথের বিবাহের কথা বলেন। উৎসের তালিকায় থাকা সংখ্যাগত অসংগতিও টীকায় চিহ্নিত।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vaishampayana, janamejaya, dhritarashtra, kuru, duhshala.
```

### Chapter 109 — Pandu hears Kindama curse

- **Filename:** `V01_P07_CH109_Pandu_hears_Kindama_curse.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** পাণ্ডু এক মৃগদম্পতিকে মিলনরত অবস্থায় বধ করলে জানা যায় মৃগটি কিন্দম ঋষি। মৃত্যুর আগে তিনি পাণ্ডুকে অভিশাপ দেন—স্ত্রীর সঙ্গে মিলন করলেই তাঁর মৃত্যু ঘটবে।
- **Reference IDs:** pandu, kindama
- **Pending New References:** kindama
- **Detailed Prompt:**

```text
V01 P07 CH109: Pandu hears Kindama curse. Chapter context: পাণ্ডু এক মৃগদম্পতিকে মিলনরত অবস্থায় বধ করলে জানা যায় মৃগটি কিন্দম ঋষি। মৃত্যুর আগে তিনি পাণ্ডুকে অভিশাপ দেন—স্ত্রীর সঙ্গে মিলন করলেই তাঁর মৃত্যু ঘটবে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: pandu, kindama.
```

### Chapter 110 — Pandu Kunti Madri reach hermitage

- **Filename:** `V01_P07_CH110_Pandu_Kunti_Madri_reach_hermitage.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** ঋষির অভিশাপে শোকাহত পাণ্ডু রাজভোগ ত্যাগ করে কঠোর তপস্যা ও বনবাসের সংকল্প করেন। কুন্তী ও মাদ্রী তাঁর সঙ্গে যান; তাঁরা শতশৃঙ্গ পর্বতে পৌঁছান।
- **Reference IDs:** pandu, kunti, madri
- **Pending New References:** madri
- **Detailed Prompt:**

```text
V01 P07 CH110: Pandu Kunti Madri reach hermitage. Chapter context: ঋষির অভিশাপে শোকাহত পাণ্ডু রাজভোগ ত্যাগ করে কঠোর তপস্যা ও বনবাসের সংকল্প করেন। কুন্তী ও মাদ্রী তাঁর সঙ্গে যান; তাঁরা শতশৃঙ্গ পর্বতে পৌঁছান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: pandu, kunti, madri.
```

### Chapter 111 — Pandu discusses ancestral debt

- **Filename:** `V01_P07_CH111_Pandu_discusses_ancestral_debt.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** শতশৃঙ্গে তপস্যারত পাণ্ডু পুত্রহীনতার কারণে পিতৃঋণ শোধ করতে না পারার দুঃখ প্রকাশ করেন। সন্তানলাভের বিভিন্ন শাস্ত্রসম্মত পথ ব্যাখ্যা করে কুন্তীকে তাঁর অনুরোধ জানান।
- **Reference IDs:** pandu, kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH111: Pandu discusses ancestral debt. Chapter context: শতশৃঙ্গে তপস্যারত পাণ্ডু পুত্রহীনতার কারণে পিতৃঋণ শোধ করতে না পারার দুঃখ প্রকাশ করেন। সন্তানলাভের বিভিন্ন শাস্ত্রসম্মত পথ ব্যাখ্যা করে কুন্তীকে তাঁর অনুরোধ জানান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: pandu, kunti.
```

### Chapter 112 — Kunti recounts Bhadra and Vyushitashva

- **Filename:** `V01_P07_CH112_Kunti_recounts_Bhadra_and_Vyushitashva.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** কুন্তী অন্য পুরুষের মাধ্যমে সন্তানলাভে আপত্তি জানিয়ে ব্যুষিতাশ্ব ও তাঁর স্ত্রী ভদ্রার অলৌকিক পুত্রলাভের উপাখ্যান শোনান; তিনি পাণ্ডুর যোগশক্তিতেই সন্তানের আশা করেন।
- **Reference IDs:** pandu, kunti, bhadra
- **Pending New References:** bhadra
- **Detailed Prompt:**

```text
V01 P07 CH112: Kunti recounts Bhadra and Vyushitashva. Chapter context: কুন্তী অন্য পুরুষের মাধ্যমে সন্তানলাভে আপত্তি জানিয়ে ব্যুষিতাশ্ব ও তাঁর স্ত্রী ভদ্রার অলৌকিক পুত্রলাভের উপাখ্যান শোনান; তিনি পাণ্ডুর যোগশক্তিতেই সন্তানের আশা করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: pandu, kunti, bhadra.
```

### Chapter 113 — Kunti reveals Durvasa mantra

- **Filename:** `V01_P07_CH113_Kunti_reveals_Durvasa_mantra.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** পাণ্ডু শ্বেতকেতুর প্রবর্তিত বিবাহনীতি ও বংশরক্ষার পুরোনো দৃষ্টান্ত দেন। কুন্তী দুর্বাসার দেওয়া দেবতাদের আহ্বানের মন্ত্রের কথা জানান; পাণ্ডু ধর্মদেবকে আহ্বান করতে বলেন।
- **Reference IDs:** pandu, kunti, durvasa
- **Pending New References:** durvasa
- **Detailed Prompt:**

```text
V01 P07 CH113: Kunti reveals Durvasa mantra. Chapter context: পাণ্ডু শ্বেতকেতুর প্রবর্তিত বিবাহনীতি ও বংশরক্ষার পুরোনো দৃষ্টান্ত দেন। কুন্তী দুর্বাসার দেওয়া দেবতাদের আহ্বানের মন্ত্রের কথা জানান; পাণ্ডু ধর্মদেবকে আহ্বান করতে বলেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: pandu, kunti, durvasa.
```

### Chapter 114 — Births of Yudhishthira Bhima Arjuna

- **Filename:** `V01_P07_CH114_Births_of_Yudhishthira_Bhima_Arjuna.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** কুন্তী ধর্ম, বায়ু ও ইন্দ্রকে আহ্বান করে যুধিষ্ঠির, ভীম ও অর্জুনের জন্ম দেন। তাঁদের জন্মের দৈববাণী, অর্জুনের জন্মোৎসবে দেবতা–গন্ধর্ব–অপ্সরাদের সমাগম ও কুন্তীর চতুর্থ সন্তান সম্পর্কে আপত্তি বর্ণিত।
- **Reference IDs:** yudhishthira, bhima, arjuna, kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH114: Births of Yudhishthira Bhima Arjuna. Chapter context: কুন্তী ধর্ম, বায়ু ও ইন্দ্রকে আহ্বান করে যুধিষ্ঠির, ভীম ও অর্জুনের জন্ম দেন। তাঁদের জন্মের দৈববাণী, অর্জুনের জন্মোৎসবে দেবতা–গন্ধর্ব–অপ্সরাদের সমাগম ও কুন্তীর চতুর্থ সন্তান সম্পর্কে আপত্তি বর্ণিত।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yudhishthira, bhima, arjuna, kunti.
```

### Chapter 115 — Madri welcomes Nakula and Sahadeva

- **Filename:** `V01_P07_CH115_Madri_welcomes_Nakula_and_Sahadeva.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** মাদ্রী নিজের সন্তানলাভের আকাঙ্ক্ষা পাণ্ডুকে জানান। কুন্তীর দেওয়া মন্ত্রে অশ্বিনীকুমারদ্বয়ের মাধ্যমে নকুল ও সহদেবের জন্ম হয়; পাঁচ পাণ্ডবের নামকরণ এবং কুন্তী–মাদ্রীর প্রতিদ্বন্দ্বিতার বিবরণ আসে।
- **Reference IDs:** pandu, nakula, sahadeva, kunti, madri
- **Pending New References:** madri
- **Detailed Prompt:**

```text
V01 P07 CH115: Madri welcomes Nakula and Sahadeva. Chapter context: মাদ্রী নিজের সন্তানলাভের আকাঙ্ক্ষা পাণ্ডুকে জানান। কুন্তীর দেওয়া মন্ত্রে অশ্বিনীকুমারদ্বয়ের মাধ্যমে নকুল ও সহদেবের জন্ম হয়; পাঁচ পাণ্ডবের নামকরণ এবং কুন্তী–মাদ্রীর প্রতিদ্বন্দ্বিতার বিবরণ আসে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: pandu, nakula, sahadeva, kunti, madri.
```

### Chapter 116 — Kunti and Madri grieve for Pandu

- **Filename:** `V01_P07_CH116_Kunti_and_Madri_grieve_for_Pandu.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** বসন্তের অরণ্যে পাণ্ডু কিন্দম ঋষির অভিশাপ বিস্মৃত হয়ে বলপূর্বক মাদ্রীর সঙ্গে মিলিত হন এবং মৃত্যুবরণ করেন। কুন্তী ও মাদ্রীর শোক, সন্তানদের ভবিষ্যৎ নিয়ে আলোচনা এবং মাদ্রীর চিতায় আরোহণের ঘটনা বর্ণিত।
- **Reference IDs:** pandu, kunti, madri
- **Pending New References:** madri
- **Detailed Prompt:**

```text
V01 P07 CH116: Kunti and Madri grieve for Pandu. Chapter context: বসন্তের অরণ্যে পাণ্ডু কিন্দম ঋষির অভিশাপ বিস্মৃত হয়ে বলপূর্বক মাদ্রীর সঙ্গে মিলিত হন এবং মৃত্যুবরণ করেন। কুন্তী ও মাদ্রীর শোক, সন্তানদের ভবিষ্যৎ নিয়ে আলোচনা এবং মাদ্রীর চিতায় আরোহণের ঘটনা বর্ণিত।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: pandu, kunti, madri.
```

### Chapter 117 — Sages escort young Pandavas home

- **Filename:** `V01_P07_CH117_Sages_escort_young_Pandavas_home.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** শতশৃঙ্গের ঋষিরা কুন্তী ও পাঁচ পাণ্ডবকে হস্তিনাপুরে নিয়ে যান। কুরুবংশ ও নগরবাসীর সামনে পাণ্ডুর পাঁচ পুত্রের জন্মপরিচয় ও তাঁর মৃত্যুসংবাদ জানিয়ে তাঁরা অন্তর্ধান করেন।
- **Reference IDs:** pandu, kunti, yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH117: Sages escort young Pandavas home. Chapter context: শতশৃঙ্গের ঋষিরা কুন্তী ও পাঁচ পাণ্ডবকে হস্তিনাপুরে নিয়ে যান। কুরুবংশ ও নগরবাসীর সামনে পাণ্ডুর পাঁচ পুত্রের জন্মপরিচয় ও তাঁর মৃত্যুসংবাদ জানিয়ে তাঁরা অন্তর্ধান করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: pandu, kunti, yudhishthira, bhima, arjuna, nakula, sahadeva.
```

### Chapter 118 — Royal funeral at Ganga

- **Filename:** `V01_P07_CH118_Royal_funeral_at_Ganga.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** ধৃতরাষ্ট্রের নির্দেশে ভীষ্ম ও বিদুর পাণ্ডু–মাদ্রীর রাজকীয় অন্ত্যেষ্টি সম্পন্ন করেন। গঙ্গাতীরে শেষকৃত্য, জলাঞ্জলি, নগরবাসীর শোক এবং বারো রাতের শোকাচারের বিবরণ রয়েছে।
- **Reference IDs:** ganga, bhishma, dhritarashtra, pandu, vidura
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH118: Royal funeral at Ganga. Chapter context: ধৃতরাষ্ট্রের নির্দেশে ভীষ্ম ও বিদুর পাণ্ডু–মাদ্রীর রাজকীয় অন্ত্যেষ্টি সম্পন্ন করেন। গঙ্গাতীরে শেষকৃত্য, জলাঞ্জলি, নগরবাসীর শোক এবং বারো রাতের শোকাচারের বিবরণ রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: ganga, bhishma, dhritarashtra, pandu, vidura.
```

### Chapter 119 — Young Bhima survives river plot

- **Filename:** `V01_P07_CH119_Young_Bhima_survives_river_plot.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** পাণ্ডুর শ্রাদ্ধের পর সত্যবতী দুই পুত্রবধূকে নিয়ে বনবাসে যান। কিশোর ভীমের অসামান্য শক্তিতে ঈর্ষান্বিত দুর্যোধন তাঁকে জলে ফেলে, বিষাক্ত সাপের দংশন করিয়ে ও খাবারে বিষ মিশিয়ে হত্যার চেষ্টা করে।
- **Reference IDs:** satyavati, pandu, duryodhana, bhima
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH119: Young Bhima survives river plot. Chapter context: পাণ্ডুর শ্রাদ্ধের পর সত্যবতী দুই পুত্রবধূকে নিয়ে বনবাসে যান। কিশোর ভীমের অসামান্য শক্তিতে ঈর্ষান্বিত দুর্যোধন তাঁকে জলে ফেলে, বিষাক্ত সাপের দংশন করিয়ে ও খাবারে বিষ মিশিয়ে হত্যার চেষ্টা করে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: satyavati, pandu, duryodhana, bhima.
```

### Chapter 120 — Shantanu discovers Kripa and Kripi

- **Filename:** `V01_P07_CH120_Shantanu_discovers_Kripa_and_Kripi.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** রাজা জনমেজয়ের প্রশ্নের উত্তরে শরদ্বান, অপ্সরা জনপদী এবং নলখাগড়ার ঝোপে যমজ কৃপ-কৃপীর জন্মের কাহিনি আসে; শান্তনু তাঁদের লালনপালন করেন এবং কৃপ হন অস্ত্রবিদ্যার আচার্য।
- **Reference IDs:** janamejaya, shantanu, kripa, kripi
- **Pending New References:** kripi
- **Detailed Prompt:**

```text
V01 P07 CH120: Shantanu discovers Kripa and Kripi. Chapter context: রাজা জনমেজয়ের প্রশ্নের উত্তরে শরদ্বান, অপ্সরা জনপদী এবং নলখাগড়ার ঝোপে যমজ কৃপ-কৃপীর জন্মের কাহিনি আসে; শান্তনু তাঁদের লালনপালন করেন এবং কৃপ হন অস্ত্রবিদ্যার আচার্য।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: janamejaya, shantanu, kripa, kripi.
```

### Chapter 121 — Drona receives Parashurama weapons

- **Filename:** `V01_P07_CH121_Drona_receives_Parashurama_weapons.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** ভরদ্বাজ ও অপ্সরা ঘৃতাচীর সূত্রে দ্রোণের জন্ম, কৃপীর সঙ্গে তাঁর বিবাহ, অশ্বত্থামার জন্ম এবং পরশুরামের কাছ থেকে অস্ত্র ও ধনুর্বেদের গুপ্তবিদ্যা লাভের ঘটনা বর্ণিত হয়।
- **Reference IDs:** drona, kripa, ashwatthama, parashurama
- **Pending New References:** parashurama
- **Detailed Prompt:**

```text
V01 P07 CH121: Drona receives Parashurama weapons. Chapter context: ভরদ্বাজ ও অপ্সরা ঘৃতাচীর সূত্রে দ্রোণের জন্ম, কৃপীর সঙ্গে তাঁর বিবাহ, অশ্বত্থামার জন্ম এবং পরশুরামের কাছ থেকে অস্ত্র ও ধনুর্বেদের গুপ্তবিদ্যা লাভের ঘটনা বর্ণিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: drona, kripa, ashwatthama, parashurama.
```

### Chapter 122 — Drona retrieves ball from well

- **Filename:** `V01_P07_CH122_Drona_retrieves_ball_from_well.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** পুরোনো বন্ধু দ্রুপদের অপমানে ক্রুদ্ধ দ্রোণ কুরুরাজপুত্রদের সামনে অসাধারণ অস্ত্রকৌশল দেখান। ভীষ্ম তাঁকে আচার্য করেন; অর্জুন একটি বিশেষ গুরুদক্ষিণার অঙ্গীকার করেন এবং কর্ণসহ বহু রাজপুত্র তাঁর কাছে শিক্ষা নেন।
- **Reference IDs:** bhishma, karna, arjuna, drona, drupada
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH122: Drona retrieves ball from well. Chapter context: পুরোনো বন্ধু দ্রুপদের অপমানে ক্রুদ্ধ দ্রোণ কুরুরাজপুত্রদের সামনে অসাধারণ অস্ত্রকৌশল দেখান। ভীষ্ম তাঁকে আচার্য করেন; অর্জুন একটি বিশেষ গুরুদক্ষিণার অঙ্গীকার করেন এবং কর্ণসহ বহু রাজপুত্র তাঁর কাছে শিক্ষা নেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhishma, karna, arjuna, drona, drupada.
```

### Chapter 123 — Arjuna aims at wooden bird

- **Filename:** `V01_P07_CH123_Arjuna_aims_at_wooden_bird.webp`
- **Status:** Planned
- **Parva:** সম্ভব পর্ব
- **Bengali Context:** অর্জুনের নিশীথকালীন অনুশীলন, একলব্যের মাটির দ্রোণমূর্তির কাছে শিক্ষা ও গুরুদক্ষিণায় বুড়ো আঙুল দান, পাখির মাথায় লক্ষ্যভেদ এবং কুমিরের হাত থেকে দ্রোণকে রক্ষার পর ব্রহ্মশিরা অস্ত্রলাভ—এই অধ্যায়ে সম্ভব পর্বের সমাপ্তি।
- **Reference IDs:** arjuna, drona, ekalavya
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P07 CH123: Arjuna aims at wooden bird. Chapter context: অর্জুনের নিশীথকালীন অনুশীলন, একলব্যের মাটির দ্রোণমূর্তির কাছে শিক্ষা ও গুরুদক্ষিণায় বুড়ো আঙুল দান, পাখির মাথায় লক্ষ্যভেদ এবং কুমিরের হাত থেকে দ্রোণকে রক্ষার পর ব্রহ্মশিরা অস্ত্রলাভ—এই অধ্যায়ে সম্ভব পর্বের সমাপ্তি।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: arjuna, drona, ekalavya.
```


## Parva 08 — জতুগৃহদাহ পর্ব

**Chapters:** 124–138  
**Count:** 15

### Chapter 124 — Bhima and Duryodhana mace duel

- **Filename:** `V01_P08_CH124_Bhima_and_Duryodhana_mace_duel.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** অস্ত্রশিক্ষা সমাপ্ত হলে দ্রোণ কুরুরাজপুত্রদের জন্য জনসমক্ষে অস্ত্রপ্রদর্শনীর আয়োজন করেন। ধৃতরাষ্ট্র ও গান্ধারীকে রাজপুত্রদের কীর্তি বর্ণনা করে শোনানো হয়; ভীম ও দুর্যোধনের গদাযুদ্ধ শুরু হয়।
- **Reference IDs:** dhritarashtra, gandhari, duryodhana, bhima, drona
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH124: Bhima and Duryodhana mace duel. Chapter context: অস্ত্রশিক্ষা সমাপ্ত হলে দ্রোণ কুরুরাজপুত্রদের জন্য জনসমক্ষে অস্ত্রপ্রদর্শনীর আয়োজন করেন। ধৃতরাষ্ট্র ও গান্ধারীকে রাজপুত্রদের কীর্তি বর্ণনা করে শোনানো হয়; ভীম ও দুর্যোধনের গদাযুদ্ধ শুরু হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dhritarashtra, gandhari, duryodhana, bhima, drona.
```

### Chapter 125 — Arjuna displays divine weapons

- **Filename:** `V01_P08_CH125_Arjuna_displays_divine_weapons.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** ভীম–দুর্যোধনের দ্বন্দ্ব থামিয়ে দ্রোণ অর্জুনকে রঙ্গভূমিতে আহ্বান করেন। অর্জুন নানা দিব্যাস্ত্র ও লক্ষ্যভেদের দক্ষতা প্রদর্শন করলে দর্শকেরা অভিভূত হন। তখন প্রবেশদ্বারে বজ্রের মতো শব্দ শোনা যায়।
- **Reference IDs:** vyasa, duryodhana, bhima, arjuna, drona
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH125: Arjuna displays divine weapons. Chapter context: ভীম–দুর্যোধনের দ্বন্দ্ব থামিয়ে দ্রোণ অর্জুনকে রঙ্গভূমিতে আহ্বান করেন। অর্জুন নানা দিব্যাস্ত্র ও লক্ষ্যভেদের দক্ষতা প্রদর্শন করলে দর্শকেরা অভিভূত হন। তখন প্রবেশদ্বারে বজ্রের মতো শব্দ শোনা যায়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa, duryodhana, bhima, arjuna, drona.
```

### Chapter 126 — Duryodhana crowns Karna

- **Filename:** `V01_P08_CH126_Duryodhana_crowns_Karna.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** স্বাভাবিক কবচ-কুণ্ডলধারী কর্ণ রঙ্গভূমিতে এসে অর্জুনকে দ্বন্দ্বযুদ্ধের আহ্বান জানান। তাঁর বংশপরিচয় নিয়ে প্রশ্ন উঠলে দুর্যোধন তাঁকে অঙ্গরাজ্যে অভিষিক্ত করেন।
- **Reference IDs:** duryodhana, karna, arjuna
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH126: Duryodhana crowns Karna. Chapter context: স্বাভাবিক কবচ-কুণ্ডলধারী কর্ণ রঙ্গভূমিতে এসে অর্জুনকে দ্বন্দ্বযুদ্ধের আহ্বান জানান। তাঁর বংশপরিচয় নিয়ে প্রশ্ন উঠলে দুর্যোধন তাঁকে অঙ্গরাজ্যে অভিষিক্ত করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: duryodhana, karna, arjuna.
```

### Chapter 127 — Karna bows to Adhiratha

- **Filename:** `V01_P08_CH127_Karna_bows_to_Adhiratha.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** অধিরথকে পিতা বলে সম্মান জানান কর্ণ। ভীম তাঁকে সারথিপুত্র বলে বিদ্রূপ করলে দুর্যোধন বীরত্ব ও জন্মপরিচয়ের প্রশ্ন তুলে কর্ণের পক্ষে দাঁড়ান। সূর্যাস্তে প্রদর্শনী শেষ হয়।
- **Reference IDs:** duryodhana, karna, bhima, adhiratha
- **Pending New References:** adhiratha
- **Detailed Prompt:**

```text
V01 P08 CH127: Karna bows to Adhiratha. Chapter context: অধিরথকে পিতা বলে সম্মান জানান কর্ণ। ভীম তাঁকে সারথিপুত্র বলে বিদ্রূপ করলে দুর্যোধন বীরত্ব ও জন্মপরিচয়ের প্রশ্ন তুলে কর্ণের পক্ষে দাঁড়ান। সূর্যাস্তে প্রদর্শনী শেষ হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: duryodhana, karna, bhima, adhiratha.
```

### Chapter 128 — Arjuna brings Drupada to Drona

- **Filename:** `V01_P08_CH128_Arjuna_brings_Drupada_to_Drona.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** গুরুদক্ষিণা হিসেবে দ্রুপদকে বন্দি করতে বলেন দ্রোণ। পুরোনো অপমানের পরিপ্রেক্ষিতে তিনি পাঞ্চাল রাজ্য ভাগ করে দ্রুপদের কাছে পুনরায় বন্ধুত্ব চান; দ্রুপদ মনে মনে ক্ষোভ পুষে রাখেন।
- **Reference IDs:** arjuna, drona, drupada
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH128: Arjuna brings Drupada to Drona. Chapter context: গুরুদক্ষিণা হিসেবে দ্রুপদকে বন্দি করতে বলেন দ্রোণ। পুরোনো অপমানের পরিপ্রেক্ষিতে তিনি পাঞ্চাল রাজ্য ভাগ করে দ্রুপদের কাছে পুনরায় বন্ধুত্ব চান; দ্রুপদ মনে মনে ক্ষোভ পুষে রাখেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: arjuna, drona, drupada.
```

### Chapter 129 — Duryodhana complains to Dhritarashtra

- **Filename:** `V01_P08_CH129_Duryodhana_complains_to_Dhritarashtra.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** যুধিষ্ঠিরের রাজ্যলাভের পক্ষে নগরবাসীর সমর্থন বাড়তে থাকায় দুর্যোধন ঈর্ষান্বিত হয়। সে ধৃতরাষ্ট্রের কাছে নিজের বংশের উত্তরাধিকার হারানোর আশঙ্কা প্রকাশ করে।
- **Reference IDs:** dhritarashtra, duryodhana, yudhishthira
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH129: Duryodhana complains to Dhritarashtra. Chapter context: যুধিষ্ঠিরের রাজ্যলাভের পক্ষে নগরবাসীর সমর্থন বাড়তে থাকায় দুর্যোধন ঈর্ষান্বিত হয়। সে ধৃতরাষ্ট্রের কাছে নিজের বংশের উত্তরাধিকার হারানোর আশঙ্কা প্রকাশ করে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dhritarashtra, duryodhana, yudhishthira.
```

### Chapter 130 — Duryodhana proposes exile

- **Filename:** `V01_P08_CH130_Duryodhana_proposes_exile.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** যুধিষ্ঠিরের জনপ্রিয়তার কারণে তাঁকে নির্বাসন দিতে ধৃতরাষ্ট্রের দ্বিধা দেখা দেয়। দুর্যোধন প্রজাদের সমর্থন কেনা ও কুরুপ্রবীণদের অবস্থান নিয়ে পিতাকে বোঝায়।
- **Reference IDs:** dhritarashtra, duryodhana, yudhishthira
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH130: Duryodhana proposes exile. Chapter context: যুধিষ্ঠিরের জনপ্রিয়তার কারণে তাঁকে নির্বাসন দিতে ধৃতরাষ্ট্রের দ্বিধা দেখা দেয়। দুর্যোধন প্রজাদের সমর্থন কেনা ও কুরুপ্রবীণদের অবস্থান নিয়ে পিতাকে বোঝায়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dhritarashtra, duryodhana, yudhishthira.
```

### Chapter 131 — Pandavas receive elders blessings

- **Filename:** `V01_P08_CH131_Pandavas_receive_elders_blessings.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** ধৃতরাষ্ট্রের নির্দেশে মন্ত্রীরা বারণাবতের উৎসবের প্রশংসা করেন। যুধিষ্ঠির রাজার ইচ্ছা বুঝে ভ্রাতাদের নিয়ে সেখানে যাওয়ার সম্মতি দেন এবং গুরুজনদের আশীর্বাদ গ্রহণ করেন।
- **Reference IDs:** dhritarashtra, yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH131: Pandavas receive elders blessings. Chapter context: ধৃতরাষ্ট্রের নির্দেশে মন্ত্রীরা বারণাবতের উৎসবের প্রশংসা করেন। যুধিষ্ঠির রাজার ইচ্ছা বুঝে ভ্রাতাদের নিয়ে সেখানে যাওয়ার সম্মতি দেন এবং গুরুজনদের আশীর্বাদ গ্রহণ করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dhritarashtra, yudhishthira, bhima, arjuna, nakula, sahadeva.
```

### Chapter 132 — Duryodhana instructs Purochana

- **Filename:** `V01_P08_CH132_Duryodhana_instructs_Purochana.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** পাণ্ডবদের বারণাবতে পাঠানোর সিদ্ধান্তের পর দুর্যোধন গোপনে পুরোচনকে একটি দাহ্য গৃহ নির্মাণের নির্দেশ দেয়। এই অধ্যায়ে জতুগৃহের ষড়যন্ত্রের সূচনা হয়।
- **Reference IDs:** duryodhana, purochana
- **Pending New References:** purochana
- **Detailed Prompt:**

```text
V01 P08 CH132: Duryodhana instructs Purochana. Chapter context: পাণ্ডবদের বারণাবতে পাঠানোর সিদ্ধান্তের পর দুর্যোধন গোপনে পুরোচনকে একটি দাহ্য গৃহ নির্মাণের নির্দেশ দেয়। এই অধ্যায়ে জতুগৃহের ষড়যন্ত্রের সূচনা হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: duryodhana, purochana.
```

### Chapter 133 — Vidura warns Yudhishthira

- **Filename:** `V01_P08_CH133_Vidura_warns_Yudhishthira.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** পাণ্ডবদের বিদায়ে হস্তিনাপুরের প্রজাদের ক্ষোভ প্রকাশ পায়। বিদুর ধাঁধার মাধ্যমে যুধিষ্ঠিরকে আসন্ন বিপদের সতর্কবার্তা দেন; যুধিষ্ঠির পরে কুন্তীকে তার অর্থ জানান।
- **Reference IDs:** vidura, yudhishthira, kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH133: Vidura warns Yudhishthira. Chapter context: পাণ্ডবদের বিদায়ে হস্তিনাপুরের প্রজাদের ক্ষোভ প্রকাশ পায়। বিদুর ধাঁধার মাধ্যমে যুধিষ্ঠিরকে আসন্ন বিপদের সতর্কবার্তা দেন; যুধিষ্ঠির পরে কুন্তীকে তার অর্থ জানান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vidura, yudhishthira, kunti.
```

### Chapter 134 — Yudhishthira examines lac palace

- **Filename:** `V01_P08_CH134_Yudhishthira_examines_lac_palace.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** বারণাবতের নাগরিকেরা পাণ্ডবদের অভ্যর্থনা জানান। যুধিষ্ঠির নতুন গৃহের দাহ্য উপাদান শনাক্ত করে ভীমের সঙ্গে নিরাপদে পালাবার কৌশল স্থির করেন।
- **Reference IDs:** yudhishthira, bhima
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH134: Yudhishthira examines lac palace. Chapter context: বারণাবতের নাগরিকেরা পাণ্ডবদের অভ্যর্থনা জানান। যুধিষ্ঠির নতুন গৃহের দাহ্য উপাদান শনাক্ত করে ভীমের সঙ্গে নিরাপদে পালাবার কৌশল স্থির করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yudhishthira, bhima.
```

### Chapter 135 — Hidden escape tunnel

- **Filename:** `V01_P08_CH135_Hidden_escape_tunnel.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** বিদুরের বিশ্বস্ত খননকারী গোপনে পাণ্ডবদের কাছে এসে অগ্নিসংযোগের নির্দিষ্ট সময় জানান এবং জতুগৃহের নিচে পালাবার সুড়ঙ্গ তৈরি করেন।
- **Reference IDs:** vidura
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH135: Hidden escape tunnel. Chapter context: বিদুরের বিশ্বস্ত খননকারী গোপনে পাণ্ডবদের কাছে এসে অগ্নিসংযোগের নির্দিষ্ট সময় জানান এবং জতুগৃহের নিচে পালাবার সুড়ঙ্গ তৈরি করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vidura.
```

### Chapter 136 — Pandavas escape burning palace

- **Filename:** `V01_P08_CH136_Pandavas_escape_burning_palace.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** এক বছর পরে যুধিষ্ঠির পলায়নের সিদ্ধান্ত নেন। অগ্নিকাণ্ডে পুরোচন ও এক ব্যাধরমণীর পরিবার নিহত হয়; পাণ্ডবেরা মাতাসহ সুড়ঙ্গ দিয়ে বেরিয়ে যান।
- **Reference IDs:** yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH136: Pandavas escape burning palace. Chapter context: এক বছর পরে যুধিষ্ঠির পলায়নের সিদ্ধান্ত নেন। অগ্নিকাণ্ডে পুরোচন ও এক ব্যাধরমণীর পরিবার নিহত হয়; পাণ্ডবেরা মাতাসহ সুড়ঙ্গ দিয়ে বেরিয়ে যান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yudhishthira, bhima, arjuna, nakula, sahadeva.
```

### Chapter 137 — Citizens see burned palace

- **Filename:** `V01_P08_CH137_Citizens_see_burned_palace.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** দগ্ধ গৃহ দেখে বারণাবতের নাগরিকেরা ষড়যন্ত্রের নিন্দা করেন। হস্তিনাপুরে পাণ্ডবদের মৃত্যু বলে সংবাদ পৌঁছলেও তাঁরা দক্ষিণের অরণ্যে অগ্রসর হচ্ছেন।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH137: Citizens see burned palace. Chapter context: দগ্ধ গৃহ দেখে বারণাবতের নাগরিকেরা ষড়যন্ত্রের নিন্দা করেন। হস্তিনাপুরে পাণ্ডবদের মৃত্যু বলে সংবাদ পৌঁছলেও তাঁরা দক্ষিণের অরণ্যে অগ্রসর হচ্ছেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```

### Chapter 138 — Bhima guards sleeping family

- **Filename:** `V01_P08_CH138_Bhima_guards_sleeping_family.webp`
- **Status:** Planned
- **Parva:** জতুগৃহদাহ পর্ব
- **Bengali Context:** ভীম মাতাকে ও ভ্রাতাদের নিয়ে দুর্গম বন ও নদী পেরিয়ে যান। তাঁদের দুরবস্থা দেখে বিলাপ করেন এবং নিদ্রিত পরিবারের পাহারায় জেগে থাকেন।
- **Reference IDs:** bhima
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P08 CH138: Bhima guards sleeping family. Chapter context: ভীম মাতাকে ও ভ্রাতাদের নিয়ে দুর্গম বন ও নদী পেরিয়ে যান। তাঁদের দুরবস্থা দেখে বিলাপ করেন এবং নিদ্রিত পরিবারের পাহারায় জেগে থাকেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhima.
```


## Parva 09 — হিড়িম্ববধ পর্ব

**Chapters:** 139–144  
**Count:** 6

### Chapter 139 — Hidimbi sees Bhima

- **Filename:** `V01_P09_CH139_Hidimbi_sees_Bhima.webp`
- **Status:** Planned
- **Parva:** হিড়িম্ববধ পর্ব
- **Bengali Context:** অরণ্যে নরমাংসভোজী হিড়িম্ব পাণ্ডবদের দেখতে পায় এবং ভগিনীকে তাঁদের কাছে পাঠায়। ভীমের প্রতি আকৃষ্ট হয়ে হিড়িম্বা ভ্রাতার আদেশ অমান্য করে।
- **Reference IDs:** bhima, hidimbi
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P09 CH139: Hidimbi sees Bhima. Chapter context: অরণ্যে নরমাংসভোজী হিড়িম্ব পাণ্ডবদের দেখতে পায় এবং ভগিনীকে তাঁদের কাছে পাঠায়। ভীমের প্রতি আকৃষ্ট হয়ে হিড়িম্বা ভ্রাতার আদেশ অমান্য করে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhima, hidimbi.
```

### Chapter 140 — Hidimba confronts his sister

- **Filename:** `V01_P09_CH140_Hidimba_confronts_his_sister.webp`
- **Status:** Planned
- **Parva:** হিড়িম্ববধ পর্ব
- **Bengali Context:** ভগিনীর বিলম্বে হিড়িম্ব নিজে এসে তাকে হত্যা করতে উদ্যত হয়। হিড়িম্বা পাণ্ডবদের রক্ষার প্রস্তাব দেয়, কিন্তু ভীম নিজের শক্তিতে রাক্ষসের মোকাবিলা করতে চান।
- **Reference IDs:** bhima, hidimbi, hidimba
- **Pending New References:** hidimba
- **Detailed Prompt:**

```text
V01 P09 CH140: Hidimba confronts his sister. Chapter context: ভগিনীর বিলম্বে হিড়িম্ব নিজে এসে তাকে হত্যা করতে উদ্যত হয়। হিড়িম্বা পাণ্ডবদের রক্ষার প্রস্তাব দেয়, কিন্তু ভীম নিজের শক্তিতে রাক্ষসের মোকাবিলা করতে চান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhima, hidimbi, hidimba.
```

### Chapter 141 — Bhima wrestles Hidimba

- **Filename:** `V01_P09_CH141_Bhima_wrestles_Hidimba.webp`
- **Status:** Planned
- **Parva:** হিড়িম্ববধ পর্ব
- **Bengali Context:** ভীম নিরপরাধ হিড়িম্বাকে রক্ষা করতে হিড়িম্বকে দ্বন্দ্বযুদ্ধে আহ্বান করেন। তাঁদের প্রচণ্ড যুদ্ধের শব্দে কুন্তী ও অন্যান্য পাণ্ডব জেগে ওঠেন।
- **Reference IDs:** bhima, hidimbi, kunti, hidimba
- **Pending New References:** hidimba
- **Detailed Prompt:**

```text
V01 P09 CH141: Bhima wrestles Hidimba. Chapter context: ভীম নিরপরাধ হিড়িম্বাকে রক্ষা করতে হিড়িম্বকে দ্বন্দ্বযুদ্ধে আহ্বান করেন। তাঁদের প্রচণ্ড যুদ্ধের শব্দে কুন্তী ও অন্যান্য পাণ্ডব জেগে ওঠেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhima, hidimbi, kunti, hidimba.
```

### Chapter 142 — Bhima defeats Hidimba

- **Filename:** `V01_P09_CH142_Bhima_defeats_Hidimba.webp`
- **Status:** Planned
- **Parva:** হিড়িম্ববধ পর্ব
- **Bengali Context:** হিড়িম্বা কুন্তীর কাছে নিজের পরিচয় ও ভীমের প্রতি অনুরাগের কথা জানায়। অর্জুনের তাগিদে ভীম রাক্ষস হিড়িম্বকে বধ করেন।
- **Reference IDs:** bhima, arjuna, hidimbi, kunti, hidimba
- **Pending New References:** hidimba
- **Detailed Prompt:**

```text
V01 P09 CH142: Bhima defeats Hidimba. Chapter context: হিড়িম্বা কুন্তীর কাছে নিজের পরিচয় ও ভীমের প্রতি অনুরাগের কথা জানায়। অর্জুনের তাগিদে ভীম রাক্ষস হিড়িম্বকে বধ করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhima, arjuna, hidimbi, kunti, hidimba.
```

### Chapter 143 — Birth of Ghatotkacha

- **Filename:** `V01_P09_CH143_Birth_of_Ghatotkacha.webp`
- **Status:** Planned
- **Parva:** হিড়িম্ববধ পর্ব
- **Bengali Context:** যুধিষ্ঠিরের অনুমতিতে হিড়িম্বা ভীমের সঙ্গে মিলিত হয়। তাঁদের পুত্র ঘটোৎকচের জন্ম, তার অতিমানবীয় শক্তি ও পাণ্ডবদের প্রতি আনুগত্যের কথা বর্ণিত হয়েছে।
- **Reference IDs:** yudhishthira, bhima, hidimbi, ghatotkacha
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P09 CH143: Birth of Ghatotkacha. Chapter context: যুধিষ্ঠিরের অনুমতিতে হিড়িম্বা ভীমের সঙ্গে মিলিত হয়। তাঁদের পুত্র ঘটোৎকচের জন্ম, তার অতিমানবীয় শক্তি ও পাণ্ডবদের প্রতি আনুগত্যের কথা বর্ণিত হয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yudhishthira, bhima, hidimbi, ghatotkacha.
```

### Chapter 144 — Vyasa guides Pandavas to Ekachakra

- **Filename:** `V01_P09_CH144_Vyasa_guides_Pandavas_to_Ekachakra.webp`
- **Status:** Planned
- **Parva:** হিড়িম্ববধ পর্ব
- **Bengali Context:** পাণ্ডবেরা তপস্বীর ছদ্মবেশে বিভিন্ন রাজ্য অতিক্রম করেন। ব্যাস তাঁদের আশ্বাস দিয়ে নিরাপদ একচক্রা নগরের এক ব্রাহ্মণের গৃহে আশ্রয় নিতে বলেন।
- **Reference IDs:** vyasa, yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P09 CH144: Vyasa guides Pandavas to Ekachakra. Chapter context: পাণ্ডবেরা তপস্বীর ছদ্মবেশে বিভিন্ন রাজ্য অতিক্রম করেন। ব্যাস তাঁদের আশ্বাস দিয়ে নিরাপদ একচক্রা নগরের এক ব্রাহ্মণের গৃহে আশ্রয় নিতে বলেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa, yudhishthira, bhima, arjuna, nakula, sahadeva.
```


## Parva 10 — বকবধ পর্ব

**Chapters:** 145–152  
**Count:** 8

### Chapter 145 — Kunti hears lament

- **Filename:** `V01_P10_CH145_Kunti_hears_lament.webp`
- **Status:** Planned
- **Parva:** বকবধ পর্ব
- **Bengali Context:** একচক্রা নগরে ভিক্ষাজীবনে অভ্যস্ত পাণ্ডবেরা ব্রাহ্মণের গৃহে আশ্রয় নিয়েছেন। একদিন কুন্তী পরিবারের বিলাপ শুনে সাহায্য করতে চান; ব্রাহ্মণের কথায় আত্মীয়বিয়োগের আশঙ্কা প্রকাশ পায়।
- **Reference IDs:** kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P10 CH145: Kunti hears lament. Chapter context: একচক্রা নগরে ভিক্ষাজীবনে অভ্যস্ত পাণ্ডবেরা ব্রাহ্মণের গৃহে আশ্রয় নিয়েছেন। একদিন কুন্তী পরিবারের বিলাপ শুনে সাহায্য করতে চান; ব্রাহ্মণের কথায় আত্মীয়বিয়োগের আশঙ্কা প্রকাশ পায়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: kunti.
```

### Chapter 146 — Brahmin wife offers sacrifice

- **Filename:** `V01_P10_CH146_Brahmin_wife_offers_sacrifice.webp`
- **Status:** Planned
- **Parva:** বকবধ পর্ব
- **Bengali Context:** পরিবারের প্রাণরক্ষার জন্য ব্রাহ্মণী নিজেকে উৎসর্গ করার প্রস্তাব দেন। স্বামীহীন সংসারের নিরাপত্তা, সন্তানদের ভবিষ্যৎ এবং তৎকালীন সমাজের ধর্মবিধি নিয়ে তাঁর বিস্তারিত বক্তব্য রয়েছে।
- **Reference IDs:** —
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P10 CH146: Brahmin wife offers sacrifice. Chapter context: পরিবারের প্রাণরক্ষার জন্য ব্রাহ্মণী নিজেকে উৎসর্গ করার প্রস্তাব দেন। স্বামীহীন সংসারের নিরাপত্তা, সন্তানদের ভবিষ্যৎ এবং তৎকালীন সমাজের ধর্মবিধি নিয়ে তাঁর বিস্তারিত বক্তব্য রয়েছে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: confirm from chapter.
```

### Chapter 147 — Brahmin daughter and little son

- **Filename:** `V01_P10_CH147_Brahmin_daughter_and_little_son.webp`
- **Status:** Planned
- **Parva:** বকবধ পর্ব
- **Bengali Context:** ব্রাহ্মণের কন্যা নিজেকে উৎসর্গ করে পরিবারের সবাইকে রক্ষা করতে চায়। শিশুপুত্রের সরল সাহসিকতায় শোকাতুর পরিবার সাময়িক সান্ত্বনা পায়; কুন্তী তাঁদের কাছে আসেন।
- **Reference IDs:** kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P10 CH147: Brahmin daughter and little son. Chapter context: ব্রাহ্মণের কন্যা নিজেকে উৎসর্গ করে পরিবারের সবাইকে রক্ষা করতে চায়। শিশুপুত্রের সরল সাহসিকতায় শোকাতুর পরিবার সাময়িক সান্ত্বনা পায়; কুন্তী তাঁদের কাছে আসেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: kunti.
```

### Chapter 148 — Brahmin explains Baka tribute

- **Filename:** `V01_P10_CH148_Brahmin_explains_Baka_tribute.webp`
- **Status:** Planned
- **Parva:** বকবধ পর্ব
- **Bengali Context:** কুন্তীর প্রশ্নের উত্তরে ব্রাহ্মণ বক রাক্ষসের শাসন, খাদ্য ও নরবলির নির্ধারিত পালা এবং অযোগ্য রাজার নিষ্ক্রিয়তার কথা জানান।
- **Reference IDs:** kunti, baka
- **Pending New References:** baka
- **Detailed Prompt:**

```text
V01 P10 CH148: Brahmin explains Baka tribute. Chapter context: কুন্তীর প্রশ্নের উত্তরে ব্রাহ্মণ বক রাক্ষসের শাসন, খাদ্য ও নরবলির নির্ধারিত পালা এবং অযোগ্য রাজার নিষ্ক্রিয়তার কথা জানান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: kunti, baka.
```

### Chapter 149 — Kunti offers to send Bhima

- **Filename:** `V01_P10_CH149_Kunti_offers_to_send_Bhima.webp`
- **Status:** Planned
- **Parva:** বকবধ পর্ব
- **Bengali Context:** ব্রাহ্মণ পরিবারের বিপদ দূর করতে কুন্তী নিজের এক পুত্রকে পাঠানোর প্রস্তাব দেন। অতিথির নিরাপত্তা নিয়ে ব্রাহ্মণের আপত্তির জবাবে তিনি ভীমের অসাধারণ শক্তির আশ্বাস দেন।
- **Reference IDs:** bhima, kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P10 CH149: Kunti offers to send Bhima. Chapter context: ব্রাহ্মণ পরিবারের বিপদ দূর করতে কুন্তী নিজের এক পুত্রকে পাঠানোর প্রস্তাব দেন। অতিথির নিরাপত্তা নিয়ে ব্রাহ্মণের আপত্তির জবাবে তিনি ভীমের অসাধারণ শক্তির আশ্বাস দেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhima, kunti.
```

### Chapter 150 — Kunti explains plan to Yudhishthira

- **Filename:** `V01_P10_CH150_Kunti_explains_plan_to_Yudhishthira.webp`
- **Status:** Planned
- **Parva:** বকবধ পর্ব
- **Bengali Context:** ভীমকে পাঠানোর সিদ্ধান্ত নিয়ে যুধিষ্ঠির মায়ের কাছে আপত্তি জানান। কুন্তী প্রত্যুপকার, ধর্ম ও ভীমের শক্তির কথা বুঝিয়ে বললে তিনি সম্মত হন।
- **Reference IDs:** yudhishthira, bhima, kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P10 CH150: Kunti explains plan to Yudhishthira. Chapter context: ভীমকে পাঠানোর সিদ্ধান্ত নিয়ে যুধিষ্ঠির মায়ের কাছে আপত্তি জানান। কুন্তী প্রত্যুপকার, ধর্ম ও ভীমের শক্তির কথা বুঝিয়ে বললে তিনি সম্মত হন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yudhishthira, bhima, kunti.
```

### Chapter 151 — Bhima wrestles Baka

- **Filename:** `V01_P10_CH151_Bhima_wrestles_Baka.webp`
- **Status:** Planned
- **Parva:** বকবধ পর্ব
- **Bengali Context:** ভীম বকের নির্ধারিত খাদ্য নিজেই খেতে শুরু করেন। ক্ষুব্ধ রাক্ষসের সঙ্গে তাঁর বৃক্ষযুদ্ধ ও মল্লযুদ্ধ শেষে বক নিহত হয়।
- **Reference IDs:** bhima, baka
- **Pending New References:** baka
- **Detailed Prompt:**

```text
V01 P10 CH151: Bhima wrestles Baka. Chapter context: ভীম বকের নির্ধারিত খাদ্য নিজেই খেতে শুরু করেন। ক্ষুব্ধ রাক্ষসের সঙ্গে তাঁর বৃক্ষযুদ্ধ ও মল্লযুদ্ধ শেষে বক নিহত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhima, baka.
```

### Chapter 152 — Ekachakra rejoices

- **Filename:** `V01_P10_CH152_Ekachakra_rejoices.webp`
- **Status:** Planned
- **Parva:** বকবধ পর্ব
- **Bengali Context:** বকবধের পর ভীম অন্য রাক্ষসদের মানুষের অনিষ্ট না করার প্রতিজ্ঞা করান। একচক্রাবাসীরা মুক্তির খবর পায়, কিন্তু ব্রাহ্মণ পাণ্ডবদের পরিচয় গোপন রাখেন।
- **Reference IDs:** bhima
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P10 CH152: Ekachakra rejoices. Chapter context: বকবধের পর ভীম অন্য রাক্ষসদের মানুষের অনিষ্ট না করার প্রতিজ্ঞা করান। একচক্রাবাসীরা মুক্তির খবর পায়, কিন্তু ব্রাহ্মণ পাণ্ডবদের পরিচয় গোপন রাখেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhima.
```


## Parva 11 — চৈত্ররথ পর্ব

**Chapters:** 153–173  
**Count:** 21

### Chapter 153 — Brahmin tells of Draupadi

- **Filename:** `V01_P11_CH153_Brahmin_tells_of_Draupadi.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** একচক্রায় আগত এক ব্রাহ্মণ পাণ্ডবদের কাছে দ্রৌপদীর স্বয়ংবর এবং দ্রুপদের সন্তানদের অলৌকিক জন্মের কথা বর্ণনা করেন। তাঁরা বিস্তারিত বিবরণ শুনতে চান।
- **Reference IDs:** draupadi, drupada
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P11 CH153: Brahmin tells of Draupadi. Chapter context: একচক্রায় আগত এক ব্রাহ্মণ পাণ্ডবদের কাছে দ্রৌপদীর স্বয়ংবর এবং দ্রুপদের সন্তানদের অলৌকিক জন্মের কথা বর্ণনা করেন। তাঁরা বিস্তারিত বিবরণ শুনতে চান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: draupadi, drupada.
```

### Chapter 154 — Drona and Drupada broken friendship

- **Filename:** `V01_P11_CH154_Drona_and_Drupada_broken_friendship.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** আগন্তুক ব্রাহ্মণ দ্রোণের জন্ম, পরশুরামের কাছে অস্ত্রবিদ্যা লাভ, দ্রুপদের সঙ্গে ভাঙা বন্ধুত্ব ও গুরুদক্ষিণার মাধ্যমে পাঞ্চাল রাজ্য বিভাজনের ঘটনাগুলি বর্ণনা করেন।
- **Reference IDs:** drona, drupada
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P11 CH154: Drona and Drupada broken friendship. Chapter context: আগন্তুক ব্রাহ্মণ দ্রোণের জন্ম, পরশুরামের কাছে অস্ত্রবিদ্যা লাভ, দ্রুপদের সঙ্গে ভাঙা বন্ধুত্ব ও গুরুদক্ষিণার মাধ্যমে পাঞ্চাল রাজ্য বিভাজনের ঘটনাগুলি বর্ণনা করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: drona, drupada.
```

### Chapter 155 — Draupadi and Dhrishtadyumna emerge from fire

- **Filename:** `V01_P11_CH155_Draupadi_and_Dhrishtadyumna_emerge_from_fire.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** দ্রোণের কাছে অপমানিত দ্রুপদ যাজ ও উপযাজের সাহায্যে পুত্রেষ্টি যজ্ঞ করেন। যজ্ঞাগ্নি থেকে ধৃষ্টদ্যুম্ন ও কৃষ্ণা দ্রৌপদীর আবির্ভাব হয়।
- **Reference IDs:** draupadi, krishna, drona, drupada, dhrishtadyumna
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P11 CH155: Draupadi and Dhrishtadyumna emerge from fire. Chapter context: দ্রোণের কাছে অপমানিত দ্রুপদ যাজ ও উপযাজের সাহায্যে পুত্রেষ্টি যজ্ঞ করেন। যজ্ঞাগ্নি থেকে ধৃষ্টদ্যুম্ন ও কৃষ্ণা দ্রৌপদীর আবির্ভাব হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: draupadi, krishna, drona, drupada, dhrishtadyumna.
```

### Chapter 156 — Pandavas depart Ekachakra

- **Filename:** `V01_P11_CH156_Pandavas_depart_Ekachakra.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** দ্রৌপদীর জন্মকাহিনি শুনে পাণ্ডবদের মন অস্থির হয়। কুন্তীর প্রস্তাবে তাঁরা একচক্রা ছেড়ে পাঞ্চালের পথে যাত্রা করেন।
- **Reference IDs:** draupadi, kunti, yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P11 CH156: Pandavas depart Ekachakra. Chapter context: দ্রৌপদীর জন্মকাহিনি শুনে পাণ্ডবদের মন অস্থির হয়। কুন্তীর প্রস্তাবে তাঁরা একচক্রা ছেড়ে পাঞ্চালের পথে যাত্রা করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: draupadi, kunti, yudhishthira, bhima, arjuna, nakula, sahadeva.
```

### Chapter 157 — Maiden receives Shiva blessing

- **Filename:** `V01_P11_CH157_Maiden_receives_Shiva_blessing.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** ব্যাস পাণ্ডবদের কাছে দ্রৌপদীর পূর্বজন্মের তপস্যা ও শিবের পাঁচ স্বামীর বর সম্পর্কে জানান এবং পাঞ্চালে যাওয়ার পরামর্শ দেন।
- **Reference IDs:** vyasa, draupadi, shiva
- **Pending New References:** shiva
- **Detailed Prompt:**

```text
V01 P11 CH157: Maiden receives Shiva blessing. Chapter context: ব্যাস পাণ্ডবদের কাছে দ্রৌপদীর পূর্বজন্মের তপস্যা ও শিবের পাঁচ স্বামীর বর সম্পর্কে জানান এবং পাঞ্চালে যাওয়ার পরামর্শ দেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa, draupadi, shiva.
```

### Chapter 158 — Arjuna confronts Angaraparna

- **Filename:** `V01_P11_CH158_Arjuna_confronts_Angaraparna.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** গঙ্গাতীরে অঙ্গারপর্ণ গন্ধর্বের সঙ্গে অর্জুনের সংঘর্ষ হয়। যুদ্ধের পর চাক্ষুষী বিদ্যা, দিব্য অশ্ব ও আগ্নেয়াস্ত্রের আদানপ্রদানের প্রস্তাবে তাঁদের বন্ধুত্ব গড়ে ওঠে।
- **Reference IDs:** ganga, arjuna, angaraparna
- **Pending New References:** angaraparna
- **Detailed Prompt:**

```text
V01 P11 CH158: Arjuna confronts Angaraparna. Chapter context: গঙ্গাতীরে অঙ্গারপর্ণ গন্ধর্বের সঙ্গে অর্জুনের সংঘর্ষ হয়। যুদ্ধের পর চাক্ষুষী বিদ্যা, দিব্য অশ্ব ও আগ্নেয়াস্ত্রের আদানপ্রদানের প্রস্তাবে তাঁদের বন্ধুত্ব গড়ে ওঠে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: ganga, arjuna, angaraparna.
```

### Chapter 159 — Gandharva counsels Arjuna

- **Filename:** `V01_P11_CH159_Gandharva_counsels_Arjuna.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** গন্ধর্ব তাঁর ক্রোধ ও পরাজয়ের কারণ ব্যাখ্যা করেন। ব্রহ্মচর্যের শক্তি এবং রাজ্যের কল্যাণে জ্ঞানী পুরোহিত নিয়োগের গুরুত্ব নিয়ে আলোচনা হয়।
- **Reference IDs:** arjuna
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P11 CH159: Gandharva counsels Arjuna. Chapter context: গন্ধর্ব তাঁর ক্রোধ ও পরাজয়ের কারণ ব্যাখ্যা করেন। ব্রহ্মচর্যের শক্তি এবং রাজ্যের কল্যাণে জ্ঞানী পুরোহিত নিয়োগের গুরুত্ব নিয়ে আলোচনা হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: arjuna.
```

### Chapter 160 — Samvarana sees Tapati

- **Filename:** `V01_P11_CH160_Samvarana_sees_Tapati.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** অর্জুনের তাপত্য নামের উৎস ব্যাখ্যা করতে গন্ধর্ব সূর্যকন্যা তপতীর পরিচয় ও রাজা সংবরণের সঙ্গে তাঁর প্রথম সাক্ষাতের কাহিনি বলেন।
- **Reference IDs:** arjuna, samvarana, tapati
- **Pending New References:** samvarana, tapati
- **Detailed Prompt:**

```text
V01 P11 CH160: Samvarana sees Tapati. Chapter context: অর্জুনের তাপত্য নামের উৎস ব্যাখ্যা করতে গন্ধর্ব সূর্যকন্যা তপতীর পরিচয় ও রাজা সংবরণের সঙ্গে তাঁর প্রথম সাক্ষাতের কাহিনি বলেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: arjuna, samvarana, tapati.
```

### Chapter 161 — Tapati asks for Surya permission

- **Filename:** `V01_P11_CH161_Tapati_asks_for_Surya_permission.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** সংবরণ তপতীকে গান্ধর্ববিবাহের প্রস্তাব দেন। তপতী নিজের অনুরাগ প্রকাশ করলেও পিতা সূর্যের অনুমতি লাভ করতে বলেন।
- **Reference IDs:** tapati, surya
- **Pending New References:** tapati, surya
- **Detailed Prompt:**

```text
V01 P11 CH161: Tapati asks for Surya permission. Chapter context: সংবরণ তপতীকে গান্ধর্ববিবাহের প্রস্তাব দেন। তপতী নিজের অনুরাগ প্রকাশ করলেও পিতা সূর্যের অনুমতি লাভ করতে বলেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: tapati, surya.
```

### Chapter 162 — Vasishtha approaches Surya

- **Filename:** `V01_P11_CH162_Vasishtha_approaches_Surya.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** মন্ত্রী অচেতন সংবরণকে উদ্ধার করেন। রাজা সূর্যের আরাধনা ও বশিষ্ঠকে স্মরণ করলে ঋষি তাঁর অভিলাষ পূরণের জন্য সূর্যের কাছে যান।
- **Reference IDs:** vasishtha, surya
- **Pending New References:** vasishtha, surya
- **Detailed Prompt:**

```text
V01 P11 CH162: Vasishtha approaches Surya. Chapter context: মন্ত্রী অচেতন সংবরণকে উদ্ধার করেন। রাজা সূর্যের আরাধনা ও বশিষ্ঠকে স্মরণ করলে ঋষি তাঁর অভিলাষ পূরণের জন্য সূর্যের কাছে যান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vasishtha, surya.
```

### Chapter 163 — Tapati and Samvarana wedding

- **Filename:** `V01_P11_CH163_Tapati_and_Samvarana_wedding.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** বশিষ্ঠের মধ্যস্থতায় তপতী ও সংবরণের বিবাহ হয়। দীর্ঘ অনাবৃষ্টির পর তাঁরা রাজ্যে ফিরে আসেন; তাঁদের পুত্র কুরু থেকে বংশপরম্পরার ব্যাখ্যা পাওয়া যায়।
- **Reference IDs:** samvarana, tapati
- **Pending New References:** samvarana, tapati
- **Detailed Prompt:**

```text
V01 P11 CH163: Tapati and Samvarana wedding. Chapter context: বশিষ্ঠের মধ্যস্থতায় তপতী ও সংবরণের বিবাহ হয়। দীর্ঘ অনাবৃষ্টির পর তাঁরা রাজ্যে ফিরে আসেন; তাঁদের পুত্র কুরু থেকে বংশপরম্পরার ব্যাখ্যা পাওয়া যায়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: samvarana, tapati.
```

### Chapter 164 — Gandharva praises Vasishtha

- **Filename:** `V01_P11_CH164_Gandharva_praises_Vasishtha.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** অর্জুন বশিষ্ঠের পরিচয় জানতে চান। গন্ধর্ব ঋষির ক্ষমাশীলতা, আত্মসংযম এবং আদর্শ রাজপুরোহিতের ভূমিকা বর্ণনা করেন।
- **Reference IDs:** arjuna, vasishtha
- **Pending New References:** vasishtha
- **Detailed Prompt:**

```text
V01 P11 CH164: Gandharva praises Vasishtha. Chapter context: অর্জুন বশিষ্ঠের পরিচয় জানতে চান। গন্ধর্ব ঋষির ক্ষমাশীলতা, আত্মসংযম এবং আদর্শ রাজপুরোহিতের ভূমিকা বর্ণনা করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: arjuna, vasishtha.
```

### Chapter 165 — Nandini defends hermitage

- **Filename:** `V01_P11_CH165_Nandini_defends_hermitage.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** বশিষ্ঠের কামধেনু নন্দিনীকে বলপূর্বক নেওয়ার চেষ্টা করে বিশ্বামিত্র তপোবলের শক্তি উপলব্ধি করেন এবং রাজ্য ত্যাগ করেন।
- **Reference IDs:** nandini
- **Pending New References:** nandini
- **Detailed Prompt:**

```text
V01 P11 CH165: Nandini defends hermitage. Chapter context: বশিষ্ঠের কামধেনু নন্দিনীকে বলপূর্বক নেওয়ার চেষ্টা করে বিশ্বামিত্র তপোবলের শক্তি উপলব্ধি করেন এবং রাজ্য ত্যাগ করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: nandini.
```

### Chapter 166 — Shakti curses Kalmashapada

- **Filename:** `V01_P11_CH166_Shakti_curses_Kalmashapada.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** শক্তির সঙ্গে বিবাদে কল্মাষপাদ অভিশপ্ত হন। বিশ্বামিত্রের প্ররোচনায় রাক্ষসাবিষ্ট রাজা বশিষ্ঠের পুত্রদের হত্যা করেন।
- **Reference IDs:** shakti, kalmashapada
- **Pending New References:** shakti, kalmashapada
- **Detailed Prompt:**

```text
V01 P11 CH166: Shakti curses Kalmashapada. Chapter context: শক্তির সঙ্গে বিবাদে কল্মাষপাদ অভিশপ্ত হন। বিশ্বামিত্রের প্ররোচনায় রাক্ষসাবিষ্ট রাজা বশিষ্ঠের পুত্রদের হত্যা করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: shakti, kalmashapada.
```

### Chapter 167 — Vasishtha hears unborn Parashara

- **Filename:** `V01_P11_CH167_Vasishtha_hears_unborn_Parashara.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** পুত্রশোকে বশিষ্ঠের প্রাণত্যাগের চেষ্টা, বিপাশা ও শতদ্রুর নামকরণ এবং অদৃশ্যন্তীর গর্ভস্থ সন্তানের বেদপাঠের ঘটনা।
- **Reference IDs:** vasishtha, parashara
- **Pending New References:** vasishtha, parashara
- **Detailed Prompt:**

```text
V01 P11 CH167: Vasishtha hears unborn Parashara. Chapter context: পুত্রশোকে বশিষ্ঠের প্রাণত্যাগের চেষ্টা, বিপাশা ও শতদ্রুর নামকরণ এবং অদৃশ্যন্তীর গর্ভস্থ সন্তানের বেদপাঠের ঘটনা।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vasishtha, parashara.
```

### Chapter 168 — Vasishtha frees Kalmashapada

- **Filename:** `V01_P11_CH168_Vasishtha_frees_Kalmashapada.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** বশিষ্ঠ কল্মাষপাদকে রাক্ষসের কবল থেকে মুক্ত করেন; রাজার অনুরোধে মহিষীর গর্ভে অশ্মকের জন্ম হয়।
- **Reference IDs:** vasishtha, kalmashapada
- **Pending New References:** vasishtha, kalmashapada
- **Detailed Prompt:**

```text
V01 P11 CH168: Vasishtha frees Kalmashapada. Chapter context: বশিষ্ঠ কল্মাষপাদকে রাক্ষসের কবল থেকে মুক্ত করেন; রাজার অনুরোধে মহিষীর গর্ভে অশ্মকের জন্ম হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vasishtha, kalmashapada.
```

### Chapter 169 — Parashara hears Bhrigu history

- **Filename:** `V01_P11_CH169_Parashara_hears_Bhrigu_history.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** পরাশর নিজের পিতার মৃত্যুর কথা জেনে ক্রুদ্ধ হন। বশিষ্ঠ তাঁকে ভৃগুবংশীয়দের ওপর ক্ষত্রিয়দের অত্যাচার এবং ঔর্বের জন্মের কাহিনি বলেন।
- **Reference IDs:** bhrigu, parashara
- **Pending New References:** bhrigu, parashara
- **Detailed Prompt:**

```text
V01 P11 CH169: Parashara hears Bhrigu history. Chapter context: পরাশর নিজের পিতার মৃত্যুর কথা জেনে ক্রুদ্ধ হন। বশিষ্ঠ তাঁকে ভৃগুবংশীয়দের ওপর ক্ষত্রিয়দের অত্যাচার এবং ঔর্বের জন্মের কাহিনি বলেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhrigu, parashara.
```

### Chapter 170 — Aurva hears ancestors

- **Filename:** `V01_P11_CH170_Aurva_hears_ancestors.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** ঔর্ব ক্ষত্রিয়দের দৃষ্টিশক্তি ফেরান, কিন্তু জগৎ ধ্বংসের সংকল্প করেন। তাঁর পিতৃপুরুষেরা ক্রোধ সংযত করার উপদেশ দেন।
- **Reference IDs:** aurva
- **Pending New References:** aurva
- **Detailed Prompt:**

```text
V01 P11 CH170: Aurva hears ancestors. Chapter context: ঔর্ব ক্ষত্রিয়দের দৃষ্টিশক্তি ফেরান, কিন্তু জগৎ ধ্বংসের সংকল্প করেন। তাঁর পিতৃপুরুষেরা ক্রোধ সংযত করার উপদেশ দেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: aurva.
```

### Chapter 171 — Aurva releases fire into ocean

- **Filename:** `V01_P11_CH171_Aurva_releases_fire_into_ocean.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** ঔর্ব ন্যায়সংগত ক্রোধ ও দণ্ডবিধির পক্ষে যুক্তি দেন; পিতৃপুরুষদের নির্দেশে ক্রোধাগ্নি সমুদ্রে নিক্ষেপ করেন।
- **Reference IDs:** aurva
- **Pending New References:** aurva
- **Detailed Prompt:**

```text
V01 P11 CH171: Aurva releases fire into ocean. Chapter context: ঔর্ব ন্যায়সংগত ক্রোধ ও দণ্ডবিধির পক্ষে যুক্তি দেন; পিতৃপুরুষদের নির্দেশে ক্রোধাগ্নি সমুদ্রে নিক্ষেপ করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: aurva.
```

### Chapter 172 — Sages stop Parashara sacrifice

- **Filename:** `V01_P11_CH172_Sages_stop_Parashara_sacrifice.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** পরাশরের রাক্ষসযজ্ঞ এবং নিরপরাধ রাক্ষসদের রক্ষার জন্য অত্রি, পুলস্ত্য, পুলহ ও ক্রতুর আগমন।
- **Reference IDs:** parashara
- **Pending New References:** parashara
- **Detailed Prompt:**

```text
V01 P11 CH172: Sages stop Parashara sacrifice. Chapter context: পরাশরের রাক্ষসযজ্ঞ এবং নিরপরাধ রাক্ষসদের রক্ষার জন্য অত্রি, পুলস্ত্য, পুলহ ও ক্রতুর আগমন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: parashara.
```

### Chapter 173 — Brahmin wife curses Kalmashapada

- **Filename:** `V01_P11_CH173_Brahmin_wife_curses_Kalmashapada.webp`
- **Status:** Planned
- **Parva:** চৈত্ররথ পর্ব
- **Bengali Context:** কল্মাষপাদের হাতে ব্রাহ্মণের মৃত্যু, ব্রাহ্মণীর অভিশাপ এবং বশিষ্ঠের মাধ্যমে রাজার বংশরক্ষার কারণ।
- **Reference IDs:** kalmashapada
- **Pending New References:** kalmashapada
- **Detailed Prompt:**

```text
V01 P11 CH173: Brahmin wife curses Kalmashapada. Chapter context: কল্মাষপাদের হাতে ব্রাহ্মণের মৃত্যু, ব্রাহ্মণীর অভিশাপ এবং বশিষ্ঠের মাধ্যমে রাজার বংশরক্ষার কারণ।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: kalmashapada.
```


## Parva 12 — দ্রৌপদীস্বয়ংবর পর্ব

**Chapters:** 174–185  
**Count:** 12

### Chapter 174 — Dhaumya becomes priest

- **Filename:** `V01_P12_CH174_Dhaumya_becomes_priest.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** গন্ধর্বের পরামর্শে পাণ্ডবেরা ধৌম্যকে পুরোহিত নিযুক্ত করেন এবং তাঁর সঙ্গে পাঞ্চালের স্বয়ংবরে যাওয়ার সংকল্প করেন।
- **Reference IDs:** dhaumya
- **Pending New References:** dhaumya
- **Detailed Prompt:**

```text
V01 P12 CH174: Dhaumya becomes priest. Chapter context: গন্ধর্বের পরামর্শে পাণ্ডবেরা ধৌম্যকে পুরোহিত নিযুক্ত করেন এবং তাঁর সঙ্গে পাঞ্চালের স্বয়ংবরে যাওয়ার সংকল্প করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dhaumya.
```

### Chapter 175 — Brahmins describe svayamvara

- **Filename:** `V01_P12_CH175_Brahmins_describe_svayamvara.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** পথে ব্রাহ্মণদের সঙ্গে পাণ্ডবদের সাক্ষাৎ। তাঁদের মুখে দ্রৌপদীর রূপ, ধৃষ্টদ্যুম্নের জন্ম ও আসন্ন স্বয়ংবর উৎসবের বিবরণ শোনা যায়।
- **Reference IDs:** draupadi, dhrishtadyumna
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P12 CH175: Brahmins describe svayamvara. Chapter context: পথে ব্রাহ্মণদের সঙ্গে পাণ্ডবদের সাক্ষাৎ। তাঁদের মুখে দ্রৌপদীর রূপ, ধৃষ্টদ্যুম্নের জন্ম ও আসন্ন স্বয়ংবর উৎসবের বিবরণ শোনা যায়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: draupadi, dhrishtadyumna.
```

### Chapter 176 — Pandavas enter svayamvara arena

- **Filename:** `V01_P12_CH176_Pandavas_enter_svayamvara_arena.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** পাণ্ডবেরা ছদ্মবেশে পাঞ্চালে পৌঁছান। দ্রুপদের নির্মিত স্বয়ংবরমঞ্চ, দুরূহ ধনুক ও লক্ষ্যভেদের শর্ত বর্ণিত হয়।
- **Reference IDs:** drupada, yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P12 CH176: Pandavas enter svayamvara arena. Chapter context: পাণ্ডবেরা ছদ্মবেশে পাঞ্চালে পৌঁছান। দ্রুপদের নির্মিত স্বয়ংবরমঞ্চ, দুরূহ ধনুক ও লক্ষ্যভেদের শর্ত বর্ণিত হয়।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: drupada, yudhishthira, bhima, arjuna, nakula, sahadeva.
```

### Chapter 177 — Dhrishtadyumna introduces kings

- **Filename:** `V01_P12_CH177_Dhrishtadyumna_introduces_kings.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** ধৃষ্টদ্যুম্ন দ্রৌপদীর কাছে স্বয়ংবরসভায় সমবেত রাজা ও রাজপুত্রদের নাম এবং বংশপরিচয় তুলে ধরেন।
- **Reference IDs:** draupadi, dhrishtadyumna
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P12 CH177: Dhrishtadyumna introduces kings. Chapter context: ধৃষ্টদ্যুম্ন দ্রৌপদীর কাছে স্বয়ংবরসভায় সমবেত রাজা ও রাজপুত্রদের নাম এবং বংশপরিচয় তুলে ধরেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: draupadi, dhrishtadyumna.
```

### Chapter 178 — Krishna recognizes disguised Pandavas

- **Filename:** `V01_P12_CH178_Krishna_recognizes_disguised_Pandavas.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** দেবতা ও রাজাদের সমাবেশে কৃষ্ণ পাণ্ডবদের চিনতে পারেন। রাজারা ধনুকে জ্যা পরাতে ব্যর্থ হন এবং অর্জুন উঠে দাঁড়ান।
- **Reference IDs:** arjuna, krishna, yudhishthira, bhima, nakula, sahadeva
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P12 CH178: Krishna recognizes disguised Pandavas. Chapter context: দেবতা ও রাজাদের সমাবেশে কৃষ্ণ পাণ্ডবদের চিনতে পারেন। রাজারা ধনুকে জ্যা পরাতে ব্যর্থ হন এবং অর্জুন উঠে দাঁড়ান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: arjuna, krishna, yudhishthira, bhima, nakula, sahadeva.
```

### Chapter 179 — Arjuna wins Draupadi

- **Filename:** `V01_P12_CH179_Arjuna_wins_Draupadi.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** ব্রাহ্মণদের মতভেদের মধ্যেও অর্জুন ধনুকে জ্যা পরিয়ে লক্ষ্য বিদ্ধ করেন। দ্রৌপদী তাঁকে বরণ করেন।
- **Reference IDs:** arjuna, draupadi
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P12 CH179: Arjuna wins Draupadi. Chapter context: ব্রাহ্মণদের মতভেদের মধ্যেও অর্জুন ধনুকে জ্যা পরিয়ে লক্ষ্য বিদ্ধ করেন। দ্রৌপদী তাঁকে বরণ করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: arjuna, draupadi.
```

### Chapter 180 — Bhima and Arjuna defend Drupada

- **Filename:** `V01_P12_CH180_Bhima_and_Arjuna_defend_Drupada.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** দ্রৌপদীকে ব্রাহ্মণের হাতে দেওয়ার সিদ্ধান্তে রাজারা ক্ষুব্ধ হন। দ্রুপদকে রক্ষায় ভীম ও অর্জুন এগিয়ে আসেন; কৃষ্ণ ও বলরাম তাঁদের পরিচয় অনুমান করেন।
- **Reference IDs:** bhima, arjuna, draupadi, krishna, drupada
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P12 CH180: Bhima and Arjuna defend Drupada. Chapter context: দ্রৌপদীকে ব্রাহ্মণের হাতে দেওয়ার সিদ্ধান্তে রাজারা ক্ষুব্ধ হন। দ্রুপদকে রক্ষায় ভীম ও অর্জুন এগিয়ে আসেন; কৃষ্ণ ও বলরাম তাঁদের পরিচয় অনুমান করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhima, arjuna, draupadi, krishna, drupada.
```

### Chapter 181 — Arjuna duels Karna and Bhima confronts Shalya

- **Filename:** `V01_P12_CH181_Arjuna_duels_Karna_and_Bhima_confronts_Shalya.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** অর্জুনের সঙ্গে কর্ণের দ্বন্দ্ব, ভীমের হাতে শল্যের পরাজয় এবং কৃষ্ণের হস্তক্ষেপে যুদ্ধের অবসান।
- **Reference IDs:** karna, bhima, arjuna, krishna, shalya
- **Pending New References:** shalya
- **Detailed Prompt:**

```text
V01 P12 CH181: Arjuna duels Karna and Bhima confronts Shalya. Chapter context: অর্জুনের সঙ্গে কর্ণের দ্বন্দ্ব, ভীমের হাতে শল্যের পরাজয় এবং কৃষ্ণের হস্তক্ষেপে যুদ্ধের অবসান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: karna, bhima, arjuna, krishna, shalya.
```

### Chapter 182 — Kunti realizes her instruction

- **Filename:** `V01_P12_CH182_Kunti_realizes_her_instruction.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** ভিক্ষা ভাগ করে নেওয়ার অনিচ্ছাকৃত নির্দেশে কুন্তী উদ্বিগ্ন হন। ধর্ম ও ভ্রাতৃসম্প্রীতির কথা বিবেচনা করে যুধিষ্ঠির দ্রৌপদী সম্পর্কে সিদ্ধান্ত নেন।
- **Reference IDs:** yudhishthira, draupadi, kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P12 CH182: Kunti realizes her instruction. Chapter context: ভিক্ষা ভাগ করে নেওয়ার অনিচ্ছাকৃত নির্দেশে কুন্তী উদ্বিগ্ন হন। ধর্ম ও ভ্রাতৃসম্প্রীতির কথা বিবেচনা করে যুধিষ্ঠির দ্রৌপদী সম্পর্কে সিদ্ধান্ত নেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yudhishthira, draupadi, kunti.
```

### Chapter 183 — Krishna and Balarama visit Pandavas

- **Filename:** `V01_P12_CH183_Krishna_and_Balarama_visit_Pandavas.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** কৃষ্ণ ও বলরাম কুম্ভকারের গৃহে পাণ্ডবদের সাক্ষাৎ করেন এবং জতুগৃহ থেকে তাঁদের রক্ষা পাওয়ায় আনন্দ প্রকাশ করেন।
- **Reference IDs:** krishna, balarama, yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** balarama
- **Detailed Prompt:**

```text
V01 P12 CH183: Krishna and Balarama visit Pandavas. Chapter context: কৃষ্ণ ও বলরাম কুম্ভকারের গৃহে পাণ্ডবদের সাক্ষাৎ করেন এবং জতুগৃহ থেকে তাঁদের রক্ষা পাওয়ায় আনন্দ প্রকাশ করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: krishna, balarama, yudhishthira, bhima, arjuna, nakula, sahadeva.
```

### Chapter 184 — Dhrishtadyumna observes household

- **Filename:** `V01_P12_CH184_Dhrishtadyumna_observes_household.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** ধৃষ্টদ্যুম্ন গোপনে পাণ্ডবদের জীবনযাপন ও কথোপকথন পর্যবেক্ষণ করেন। দ্রুপদ কন্যার বিজয়ীর পরিচয় জানতে ব্যাকুল হন।
- **Reference IDs:** drupada, dhrishtadyumna
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P12 CH184: Dhrishtadyumna observes household. Chapter context: ধৃষ্টদ্যুম্ন গোপনে পাণ্ডবদের জীবনযাপন ও কথোপকথন পর্যবেক্ষণ করেন। দ্রুপদ কন্যার বিজয়ীর পরিচয় জানতে ব্যাকুল হন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: drupada, dhrishtadyumna.
```

### Chapter 185 — Drupada sends royal priest

- **Filename:** `V01_P12_CH185_Drupada_sends_royal_priest.webp`
- **Status:** Planned
- **Parva:** দ্রৌপদীস্বয়ংবর পর্ব
- **Bengali Context:** ধৃষ্টদ্যুম্নের বিবরণে দ্রুপদ আশান্বিত হন। তাঁর পুরোহিত পাণ্ডবদের কাছে পরিচয় জানতে গেলে যুধিষ্ঠির স্বয়ংবরের শর্তপূরণের কথা স্মরণ করিয়ে দেন।
- **Reference IDs:** yudhishthira, drupada, dhrishtadyumna
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P12 CH185: Drupada sends royal priest. Chapter context: ধৃষ্টদ্যুম্নের বিবরণে দ্রুপদ আশান্বিত হন। তাঁর পুরোহিত পাণ্ডবদের কাছে পরিচয় জানতে গেলে যুধিষ্ঠির স্বয়ংবরের শর্তপূরণের কথা স্মরণ করিয়ে দেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yudhishthira, drupada, dhrishtadyumna.
```


## Parva 13 — বৈবাহিক পর্ব

**Chapters:** 186–191  
**Count:** 6

### Chapter 186 — Pandavas choose weapons at palace

- **Filename:** `V01_P13_CH186_Pandavas_choose_weapons_at_palace.webp`
- **Status:** Planned
- **Parva:** বৈবাহিক পর্ব
- **Bengali Context:** দ্রুপদ পাণ্ডবদের রাজপ্রাসাদে আমন্ত্রণ জানান। ভোজের পরে বিভিন্ন পেশার উপকরণের মধ্যে তাঁদের অস্ত্রের প্রতি আকর্ষণ দেখে তিনি তাঁদের ক্ষত্রিয় পরিচয়ের আভাস পান।
- **Reference IDs:** drupada, yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P13 CH186: Pandavas choose weapons at palace. Chapter context: দ্রুপদ পাণ্ডবদের রাজপ্রাসাদে আমন্ত্রণ জানান। ভোজের পরে বিভিন্ন পেশার উপকরণের মধ্যে তাঁদের অস্ত্রের প্রতি আকর্ষণ দেখে তিনি তাঁদের ক্ষত্রিয় পরিচয়ের আভাস পান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: drupada, yudhishthira, bhima, arjuna, nakula, sahadeva.
```

### Chapter 187 — Yudhishthira reveals identities

- **Filename:** `V01_P13_CH187_Yudhishthira_reveals_identities.webp`
- **Status:** Planned
- **Parva:** বৈবাহিক পর্ব
- **Bengali Context:** যুধিষ্ঠির পাণ্ডবদের প্রকৃত পরিচয় প্রকাশ করেন। দ্রুপদ রাজ্য ফিরিয়ে দেওয়ার প্রতিশ্রুতি দেন; দ্রৌপদীর পাঁচ পাণ্ডবের সঙ্গে বিবাহের প্রস্তাব নিয়ে ধর্মীয় প্রশ্ন ওঠে।
- **Reference IDs:** yudhishthira, draupadi, drupada
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P13 CH187: Yudhishthira reveals identities. Chapter context: যুধিষ্ঠির পাণ্ডবদের প্রকৃত পরিচয় প্রকাশ করেন। দ্রুপদ রাজ্য ফিরিয়ে দেওয়ার প্রতিশ্রুতি দেন; দ্রৌপদীর পাঁচ পাণ্ডবের সঙ্গে বিবাহের প্রস্তাব নিয়ে ধর্মীয় প্রশ্ন ওঠে।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: yudhishthira, draupadi, drupada.
```

### Chapter 188 — Drupada debates marriage with Vyasa

- **Filename:** `V01_P13_CH188_Drupada_debates_marriage_with_Vyasa.webp`
- **Status:** Planned
- **Parva:** বৈবাহিক পর্ব
- **Bengali Context:** দ্রুপদ, ধৃষ্টদ্যুম্ন, যুধিষ্ঠির ও কুন্তী বহুপতি-বিবাহের ধর্মসংগততা নিয়ে নিজেদের মত দেন। ব্যাস তখন দ্রুপদকে একান্তে এর প্রাচীন কারণ বলার উদ্যোগ নেন।
- **Reference IDs:** vyasa, yudhishthira, drupada, dhrishtadyumna, kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P13 CH188: Drupada debates marriage with Vyasa. Chapter context: দ্রুপদ, ধৃষ্টদ্যুম্ন, যুধিষ্ঠির ও কুন্তী বহুপতি-বিবাহের ধর্মসংগততা নিয়ে নিজেদের মত দেন। ব্যাস তখন দ্রুপদকে একান্তে এর প্রাচীন কারণ বলার উদ্যোগ নেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa, yudhishthira, drupada, dhrishtadyumna, kunti.
```

### Chapter 189 — Vyasa recounts five Indras

- **Filename:** `V01_P13_CH189_Vyasa_recounts_five_Indras.webp`
- **Status:** Planned
- **Parva:** বৈবাহিক পর্ব
- **Bengali Context:** ব্যাস পাঁচ ইন্দ্রের মানবজন্ম, শিবের বিধান, দ্রৌপদীর শ্রীরূপ এবং তাঁর পূর্বজন্মের বরলাভের কাহিনি ব্যাখ্যা করেন। দ্রুপদ দিব্যদৃষ্টিতে পাণ্ডবদের পূর্বতন রূপ দেখেন।
- **Reference IDs:** vyasa, draupadi, drupada
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P13 CH189: Vyasa recounts five Indras. Chapter context: ব্যাস পাঁচ ইন্দ্রের মানবজন্ম, শিবের বিধান, দ্রৌপদীর শ্রীরূপ এবং তাঁর পূর্বজন্মের বরলাভের কাহিনি ব্যাখ্যা করেন। দ্রুপদ দিব্যদৃষ্টিতে পাণ্ডবদের পূর্বতন রূপ দেখেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa, draupadi, drupada.
```

### Chapter 190 — Draupadi marries five Pandavas

- **Filename:** `V01_P13_CH190_Draupadi_marries_five_Pandavas.webp`
- **Status:** Planned
- **Parva:** বৈবাহিক পর্ব
- **Bengali Context:** দ্রুপদ ব্যাসের ব্যাখ্যা মেনে নেন। ধৌম্যের পৌরোহিত্যে পরপর পাঁচ দিনে পাঁচ পাণ্ডবের সঙ্গে দ্রৌপদীর বিবাহ সম্পন্ন হয়; দ্রুপদ বিপুল উপহার প্রদান করেন।
- **Reference IDs:** vyasa, draupadi, drupada, yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P13 CH190: Draupadi marries five Pandavas. Chapter context: দ্রুপদ ব্যাসের ব্যাখ্যা মেনে নেন। ধৌম্যের পৌরোহিত্যে পরপর পাঁচ দিনে পাঁচ পাণ্ডবের সঙ্গে দ্রৌপদীর বিবাহ সম্পন্ন হয়; দ্রুপদ বিপুল উপহার প্রদান করেন।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vyasa, draupadi, drupada, yudhishthira, bhima, arjuna, nakula, sahadeva.
```

### Chapter 191 — Kunti blesses Draupadi

- **Filename:** `V01_P13_CH191_Kunti_blesses_Draupadi.webp`
- **Status:** Planned
- **Parva:** বৈবাহিক পর্ব
- **Bengali Context:** কুন্তী নববধূ দ্রৌপদীকে দীর্ঘায়ু, সৌভাগ্য ও সমৃদ্ধির আশীর্বাদ দেন। কৃষ্ণ পাণ্ডবদের বিবাহ উপলক্ষে ধনসম্পদ, রথ, অশ্ব ও অন্যান্য উপহার পাঠান।
- **Reference IDs:** draupadi, krishna, kunti
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P13 CH191: Kunti blesses Draupadi. Chapter context: কুন্তী নববধূ দ্রৌপদীকে দীর্ঘায়ু, সৌভাগ্য ও সমৃদ্ধির আশীর্বাদ দেন। কৃষ্ণ পাণ্ডবদের বিবাহ উপলক্ষে ধনসম্পদ, রথ, অশ্ব ও অন্যান্য উপহার পাঠান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: draupadi, krishna, kunti.
```


## Parva 14 — বিদুরাগমন পর্ব

**Chapters:** 192–198  
**Count:** 7

### Chapter 192 — Vidura hears Pandavas live

- **Filename:** `V01_P14_CH192_Vidura_hears_Pandavas_live.webp`
- **Status:** Planned
- **Parva:** বিদুরাগমন পর্ব
- **Bengali Context:** পাণ্ডবদের জীবিত থাকার সংবাদে রাজাদের বিস্ময়, বিদুরের আনন্দ এবং দুর্যোধন–কর্ণের গোপন পরামর্শের সূচনা।
- **Reference IDs:** vidura, duryodhana, karna, yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P14 CH192: Vidura hears Pandavas live. Chapter context: পাণ্ডবদের জীবিত থাকার সংবাদে রাজাদের বিস্ময়, বিদুরের আনন্দ এবং দুর্যোধন–কর্ণের গোপন পরামর্শের সূচনা।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: vidura, duryodhana, karna, yudhishthira, bhima, arjuna, nakula, sahadeva.
```

### Chapter 193 — Duryodhana proposes schemes

- **Filename:** `V01_P14_CH193_Duryodhana_proposes_schemes.webp`
- **Status:** Planned
- **Parva:** বিদুরাগমন পর্ব
- **Bengali Context:** ধৃতরাষ্ট্রের গোপন অভিপ্রায় এবং পাণ্ডবদের ঐক্য ভাঙা ও ভীমকে হত্যার জন্য দুর্যোধনের নানা কৌশল।
- **Reference IDs:** dhritarashtra, duryodhana, bhima
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P14 CH193: Duryodhana proposes schemes. Chapter context: ধৃতরাষ্ট্রের গোপন অভিপ্রায় এবং পাণ্ডবদের ঐক্য ভাঙা ও ভীমকে হত্যার জন্য দুর্যোধনের নানা কৌশল।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dhritarashtra, duryodhana, bhima.
```

### Chapter 194 — Karna advocates open war

- **Filename:** `V01_P14_CH194_Karna_advocates_open_war.webp`
- **Status:** Planned
- **Parva:** বিদুরাগমন পর্ব
- **Bengali Context:** দুর্যোধনের ছলনার পরিকল্পনা প্রত্যাখ্যান করে কর্ণের সরাসরি যুদ্ধের প্রস্তাব এবং রাজপরিষদের আহ্বান।
- **Reference IDs:** duryodhana, karna
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P14 CH194: Karna advocates open war. Chapter context: দুর্যোধনের ছলনার পরিকল্পনা প্রত্যাখ্যান করে কর্ণের সরাসরি যুদ্ধের প্রস্তাব এবং রাজপরিষদের আহ্বান।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: duryodhana, karna.
```

### Chapter 195 — Bhishma advises half kingdom

- **Filename:** `V01_P14_CH195_Bhishma_advises_half_kingdom.webp`
- **Status:** Planned
- **Parva:** বিদুরাগমন পর্ব
- **Bengali Context:** পাণ্ডবদের পৈতৃক অধিকার, কুরুবংশের সুনাম ও ধর্ম রক্ষার জন্য ভীষ্মের অর্ধেক রাজ্য দেওয়ার উপদেশ।
- **Reference IDs:** bhishma
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P14 CH195: Bhishma advises half kingdom. Chapter context: পাণ্ডবদের পৈতৃক অধিকার, কুরুবংশের সুনাম ও ধর্ম রক্ষার জন্য ভীষ্মের অর্ধেক রাজ্য দেওয়ার উপদেশ।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhishma.
```

### Chapter 196 — Drona advises reconciliation

- **Filename:** `V01_P14_CH196_Drona_advises_reconciliation.webp`
- **Status:** Planned
- **Parva:** বিদুরাগমন পর্ব
- **Bengali Context:** পাণ্ডবদের সম্মানসহ ফিরিয়ে আনার জন্য দ্রোণের পরামর্শ, কর্ণের দৈবতত্ত্ব ও অম্বুবিচের কাহিনি, এবং দ্রোণের প্রত্যুত্তর।
- **Reference IDs:** karna, drona
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P14 CH196: Drona advises reconciliation. Chapter context: পাণ্ডবদের সম্মানসহ ফিরিয়ে আনার জন্য দ্রোণের পরামর্শ, কর্ণের দৈবতত্ত্ব ও অম্বুবিচের কাহিনি, এবং দ্রোণের প্রত্যুত্তর।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: karna, drona.
```

### Chapter 197 — Vidura warns Dhritarashtra

- **Filename:** `V01_P14_CH197_Vidura_warns_Dhritarashtra.webp`
- **Status:** Planned
- **Parva:** বিদুরাগমন পর্ব
- **Bengali Context:** ভীষ্ম ও দ্রোণের পরামর্শের সমর্থনে বিদুরের যুক্তি, পাণ্ডবদের শক্তি ও মিত্রতা এবং দুর্যোধন সম্পর্কে সতর্কবাণী।
- **Reference IDs:** bhishma, dhritarashtra, vidura, duryodhana, drona
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P14 CH197: Vidura warns Dhritarashtra. Chapter context: ভীষ্ম ও দ্রোণের পরামর্শের সমর্থনে বিদুরের যুক্তি, পাণ্ডবদের শক্তি ও মিত্রতা এবং দুর্যোধন সম্পর্কে সতর্কবাণী।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: bhishma, dhritarashtra, vidura, duryodhana, drona.
```

### Chapter 198 — Vidura welcomes Pandavas at Panchala

- **Filename:** `V01_P14_CH198_Vidura_welcomes_Pandavas_at_Panchala.webp`
- **Status:** Planned
- **Parva:** বিদুরাগমন পর্ব
- **Bengali Context:** ধৃতরাষ্ট্রের সম্মতি, বিদুরের পাঞ্চালে আগমন, উপহার বিতরণ এবং পাণ্ডবদের হস্তিনাপুরে ফেরার আমন্ত্রণ।
- **Reference IDs:** dhritarashtra, vidura, yudhishthira, bhima, arjuna, nakula, sahadeva
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P14 CH198: Vidura welcomes Pandavas at Panchala. Chapter context: ধৃতরাষ্ট্রের সম্মতি, বিদুরের পাঞ্চালে আগমন, উপহার বিতরণ এবং পাণ্ডবদের হস্তিনাপুরে ফেরার আমন্ত্রণ।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: dhritarashtra, vidura, yudhishthira, bhima, arjuna, nakula, sahadeva.
```


## Parva 15 — রাজ্যলাভ পর্ব

**Chapters:** 199–199  
**Count:** 1

### Chapter 199 — Indraprastha established

- **Filename:** `V01_P15_CH199_Indraprastha_established.webp`
- **Status:** Planned
- **Parva:** রাজ্যলাভ পর্ব
- **Bengali Context:** পাণ্ডবদের হস্তিনাপুরে প্রত্যাবর্তন, অর্ধরাজ্য লাভ, খাণ্ডবপ্রস্থে ইন্দ্রপ্রস্থ নগর প্রতিষ্ঠা এবং কৃষ্ণের দ্বারাবতীতে যাত্রা।
- **Reference IDs:** krishna
- **Pending New References:** —
- **Detailed Prompt:**

```text
V01 P15 CH199: Indraprastha established. Chapter context: পাণ্ডবদের হস্তিনাপুরে প্রত্যাবর্তন, অর্ধরাজ্য লাভ, খাণ্ডবপ্রস্থে ইন্দ্রপ্রস্থ নগর প্রতিষ্ঠা এবং কৃষ্ণের দ্বারাবতীতে যাত্রা।. Cinematic painterly-realistic ancient Indian epic, 16:9 landscape, detailed textiles and natural lighting, no text, no modern objects. Maintain the approved character reference faces and body types; adapt age, costume and equipment to the chapter. Generate and review missing reference designs first. Verify the full chapter before rendering. Reference IDs: krishna.
```

---

## Final Notes

- This specification is designed for GitHub storage and project continuity.
- The **chapter plan is complete**, but the **image production itself is not complete**.
- Some entries mark **pending references**: those are proposed character IDs that still need final approved visual designs before their corresponding chapter images should be generated.
- Some existing generated images are overview drafts, not necessarily final publication-approved illustrations.
- OCR issues in the source text and later editorial verification may require prompt refinements before final image production.
- The guiding rule remains: **do not skip chapter content, do not break character continuity, and do not let visual style drift across the series.**
