# STEAM-SEL Lesson Designer

**An open AI skill that helps educators weave doodling, music and drama into any subject, so learners build Empathy, Mindfulness, Critical Inquiry and Compassion while they learn.**

Created by NMG under the mentorship of EO as part of the OE4BW 2026 programme · Based on *Keep Calm and STEAM Ahead! Handbook for Educators*, Edition 2 (2026) · Licensed [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) · Version 1.8

---

## What it does

The STEAM-SEL Lesson Designer turns an AI assistant into a planning partner for educators. It:

- **asks about your lesson one question at a time**, mostly multiple choice, so you can answer with a letter: topic, learners, setting, time, goals, support needs, resources;
- **speaks your language**: it replies in the language you write in, and asks which language you want the lesson plan in: the same language, your learners' language, a bilingual version, or teacher notes in one language with learner materials in another;
- **recommends an art form** (doodling, music and sound, or drama) that fits your topic, or uses the one you choose;
- **creates ready-to-use materials**: lesson plans, learner worksheets, **doodles** (drawn as images where your AI tool can make them, always with a drawing guide), **original songs and chants** with simple sargam or doh-re-mi melodies and body-percussion rhythms, **soundscape and drama scripts**, quizzes with answer keys, learner rubrics, levelled texts and multi-session units;
- **links lessons to real-world issues** such as climate, water, gender equality, waste and peace, through the handbook's SDG Lens;
- **builds in good practice**: "I can" success criteria, three levels of differentiation, Universal Design for Learning, inclusion and emotional safety, and clear guidance for child-protection concerns;
- **proposes open resources first**: it recommends openly licensed (OER) resources first, reuses public-domain material only after asking you to verify its status and authenticity, and mentions copyrighted material only as a clearly labelled suggestion for you to check for legal access and accessibility. With web search on, it cites the sources it consulted;
- **works for low-resource settings**: every plan works with paper, pen, voice and bodies, and can be exported as plain text for WhatsApp or SMS;
- **helps you reflect** after you've taught the lesson, and plans the next one.

**See it in action:** three [example lesson plans](examples/), covering germination through doodling (Grade 5), supply and demand through drama (first-year university), and a Monsoon Memories climate unit (Grades 6–8, SDG 13).

**Who it's for:** schoolteachers, university lecturers, counsellors, NGO and community facilitators, youth workers, mentors and parents. In the handbook's words: whether you're 13 or 103, if you guide learning, you are an educator.

**Sustainable Development Goals:** like the handbook, the skill supports **SDG 4** (Quality Education), **SDG 3** (Good Health and Well-Being), **SDG 10** (Reduced Inequalities) and **SDG 16** (Peace, Justice and Strong Institutions) through the way SEL is taught. Through the SDG Lens, learners can also explore real-world issues as content, such as **SDG 13** (Climate Action), **SDG 5** (Gender Equality), **SDG 6** (Clean Water and Sanitation) and **SDG 12** (Responsible Consumption and Production), in line with SDG Target 4.7 on education for sustainable development and global citizenship.

## What's in this repository

```
steam-sel-lesson-designer/
├── README.md                    ← this file
├── LICENSE.md                   ← CC BY-NC-SA 4.0
├── CHANGELOG.md                 ← version history
├── TESTING.md                   ← test conversations to check it works
├── CITATION.cff                 ← how to cite the skill
├── build-single-file.ps1        ← rebuilds the single-file version after edits
├── examples/                    ← sample lesson plans made with the skill
├── steam-sel-lesson-designer/   ← the skill itself (Agent Skills format)
│   ├── SKILL.md                 ← main instructions
│   └── references/              ← details the AI reads when needed
│       ├── intake-questions.md
│       ├── handbook-knowledge.md
│       ├── sdg-lens.md
│       ├── assessment-and-inclusion.md
│       ├── research-and-licensing.md
│       ├── output-templates.md
│       └── creating-doodles-music-scripts.md
└── chatbots/                    ← versions for chatbots that can't load skill folders
    ├── compact-instructions.md  ← short version (under 8,000 characters)
    └── full-knowledge-file.md   ← everything in one file
```

## How to use it

Choose the option that matches your AI tool. Menu names change from time to time, so check your tool's help pages if a step looks different.

### Option 1: AI tools that support skills (SKILL.md folders)

The `steam-sel-lesson-designer/` folder follows the open Agent Skills format: a folder with a `SKILL.md` file and supporting files. Several AI assistants and agents can load skills in this format.

- **Claude (claude.ai):** download **[steam-sel-lesson-designer.zip](https://github.com/nmg-002/steam-sel-lesson-designer/releases/latest/download/steam-sel-lesson-designer.zip)** from the [latest release](https://github.com/nmg-002/steam-sel-lesson-designer/releases/latest), then upload it in **Settings › Capabilities › Skills**. (Or download this repository and compress the inner `steam-sel-lesson-designer` folder into a ZIP yourself.)
- **Claude Code:** copy the inner `steam-sel-lesson-designer` folder into `~/.claude/skills/` (for you) or `.claude/skills/` inside a project (for everyone working on it).
- **Other agents:** check your tool's documentation for where it reads skill folders, and copy the inner folder there.

Then just ask for a lesson, for example: *"Help me plan a 40-minute Grade 6 lesson on photosynthesis."*

### Option 2: ChatGPT (Custom GPT)

1. In ChatGPT, go to **GPTs › Create › Configure**.
2. Paste the contents of `chatbots/compact-instructions.md` into **Instructions**.
3. Upload `chatbots/full-knowledge-file.md` under **Knowledge**.
4. Under **Capabilities**, turn on **Web Search**.
5. Save, and share the GPT with your colleagues if you like.

### Option 3: Gemini (Gem) and other chatbots with custom instructions

Create a custom assistant (in Gemini, a **Gem**). Paste `chatbots/compact-instructions.md` into its instructions and add `chatbots/full-knowledge-file.md` as a knowledge file. If your tool has no file upload but allows long instructions, paste `full-knowledge-file.md` instead.

### Option 4: Any chatbot, no setup

Open a new chat, paste the whole of `chatbots/full-knowledge-file.md` as your first message, then type **Start**.

### Turn on web search

With web search on, the assistant can check current facts, find openly licensed resources and give you links to its sources. Without it, it still works, but it will mark uncertain facts "(please verify)" and won't give new links.

## Important notes

- **AI can make mistakes.** Every output reminds you to check facts, figures, links and licences, and to adapt the plan to your learners. You remain the decision-maker.
- **Privacy:** the assistant never needs learners' names or personal details. Please don't enter them.
- **Child protection:** the assistant is not a safeguarding service. If a learner discloses harm or is at risk, follow your organisation's child-protection procedure and contact your designated safeguarding lead.

## Checking that it works

[TESTING.md](TESTING.md) has 21 short test conversations (for example "Hi", "Who made you?" and a child-protection scenario) with what the assistant should do. Run a few of them whenever you set the skill up in a new AI tool or edit it.

## Updating the skill

1. Edit `steam-sel-lesson-designer/SKILL.md` or the files in `references/`.
2. Run `build-single-file.ps1` to rebuild `chatbots/full-knowledge-file.md`.
3. If the change affects the conversation or the rules, update `chatbots/compact-instructions.md` to match, and keep it under 8,000 characters.
4. Raise the version number in `SKILL.md` (`metadata: version`) and add an entry to `CHANGELOG.md`.
5. Run the scenarios in [TESTING.md](TESTING.md).
6. Upload the changes, then publish a new release: add a version tag (for example `v1.3`) under **Releases › Draft a new release**, paste the changelog entry as the notes, and attach a fresh `steam-sel-lesson-designer.zip` of the skill folder.

## Credits and attribution

**This skill:** STEAM-SEL Lesson Designer, by NMG, created under the mentorship of EO as part of the OE4BW 2026 programme. Licensed CC BY-NC-SA 4.0. Drafted with the help of AI (Claude, by Anthropic) and reviewed by the creator.

**Adapted from:** *Keep Calm and STEAM Ahead! Handbook for Educators*, **Edition 2 (2026)**, by NMG (Goa University), licensed [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). Handbook: [gomesnatasha.in](https://gomesnatasha.in/2025/09/28/keep-calm-and-steam-ahead/).
- **Chapters 1–4** (first published as Edition 1, 2025) were developed under the mentorship of GBC, with the support of Hub-Coordinator AD, as part of the OE4BW 2025 programme.
- **Chapter 5, on the Sustainable Development Goals** (new in Edition 2, 2026), was developed under the mentorship of EO, as part of the OE4BW 2026 programme.
- The handbook was itself adapted from the course *Keep Calm and eXpress yourself!* by AD, NMG, DW and IK (2022), CC BY-NC-SA 4.0.

**Changes made:** the handbook's frameworks (EMC², the three art forms, the 6-Step Approaches, the Single-Point Rubric and the SDG Lens), examples and templates were summarised and restructured as instructions for an AI assistant. New material was added, including the question-by-question intake, research and citation rules, licensing guidance, success criteria and learner rubrics, three-tier differentiation, a UDL 3.0 check, an optional CASEL crosswalk, safety and child-protection guidance, export formats, a sharing pack and an after-lesson reflection.

**Suggested credit when you share or adapt this skill:**
> *STEAM-SEL Lesson Designer* AI skill by NMG (2026), created under the mentorship of EO as part of the OE4BW 2026 programme, based on *Keep Calm and STEAM Ahead! Handbook for Educators*, Edition 2 (2026) by NMG et al. Licensed CC BY-NC-SA 4.0.

**Citing in academic work:** use the **"Cite this repository"** button in the right-hand sidebar on GitHub for a ready-made APA or BibTeX reference (from [CITATION.cff](CITATION.cff)).

Other works mentioned in the skill (UNESCO MGIEP's EMC² framework, CAST's UDL Guidelines, CASEL's SEL framework, the Kennedy Center's definition of arts integration, Ed Hawkins' warming stripes, NOAA data) belong to their respective owners and are referred to, not reproduced.

## Licence

This work is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). You may share and adapt it for **non-commercial** purposes, as long as you **give credit**, **indicate any changes**, and **share your adaptations under the same licence**. See [LICENSE.md](LICENSE.md).

## Contributing

Suggestions, corrections and new examples are welcome. Please open an issue describing the change, or submit a pull request. Contributions are accepted under the same CC BY-NC-SA 4.0 licence.
