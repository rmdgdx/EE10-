# EE10 — Electrical Engineering Research Project

**Rizal Technological University · Cities of Mandaluyong and Pasig**
College of Engineering and Industrial Technology
Course Professor: **Dr. Ryan Manuel D. Guido**
3 units · 4th year · First Semester, A.Y. 2026–2027

> A fifteen-week outcomes-based course that carries a research project from the
> first spark of an idea to a defended, publication-ready body of work — two
> linked studies executed back to back.

**Live site:** https://rmdgdx.github.io/EE10-/

---

## The two-phase model

| | Weeks | Produces |
|---|---|---|
| **Phase 1** | 1–8 | A design-thinking and ideation sprint, a defended **research project proposal**, and a **review or scientometric paper** in IEEE format submitted to an IEEE conference or journal indexed in IEEE Xplore. |
| **Phase 2** | 9–15 | The research gap Phase 1 quantified, answered by **building, calibrating, validating, and demonstrating a working prototype**, reported as a **full IEEE article** and defended before a panel. |

The connection is structural, not decorative: the Phase 1 paper's closing gap
statement becomes the Phase 2 article's opening paragraph, and its comparison
tables become the related-work section.

**The standard:** *simple to build, hard to argue with, and demonstrably useful.*
The innovation is expected to live in sensing strategy, signal processing,
embedded intelligence, and validation rigor — not in elaborate hardware.

---

## Repository contents

```
.
├── index.html                  Course home — start here
├── syllabus.html               The full syllabus (self-contained, prints cleanly)
├── assets/
│   └── css/
│       └── rtu-course.css      Shared theme for index.html and units/*.html
├── units/
│   ├── index.html              Unit index — the twelve teaching weeks
│   ├── _TEMPLATE.html          Blank themed unit page — duplicate this
│   ├── unit-01-…html           WORKED EXAMPLE — written out in full
│   └── unit-02…unit-12         Themed stubs awaiting content
├── templates/
│   ├── index.html              Template index
│   ├── proposal.md             …and ten more course forms
│   └── README.md
├── LICENSE                     All rights reserved
├── CITATION.cff                Machine-readable citation metadata
├── .nojekyll                   Serves files beginning with “_” on GitHub Pages
└── .gitignore                  Keeps corpus exports and personal data out
```

### Where things live

| I want to… | Go to |
|---|---|
| Read the course design | [`syllabus.html`](syllabus.html) |
| See the ideation guidelines and idea bank | [`syllabus.html#ideation`](syllabus.html#ideation) |
| See the rubrics | [`syllabus.html#rubrics`](syllabus.html#rubrics) |
| Find the readings (all free to access) | [`syllabus.html#readings`](syllabus.html#readings) |
| Read a unit lecture | [`units/index.html`](units/index.html) |
| Grab a form to fill in | [`templates/index.html`](templates/index.html) |

---

## Publishing to GitHub Pages

1. Push this repository to `https://github.com/rmdgdx/EE10-`.
2. **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
3. Branch `main`, folder `/ (root)`. Save.
4. The site appears at `https://rmdgdx.github.io/EE10-/` within a minute or two.

`.nojekyll` is present so GitHub Pages serves `units/_TEMPLATE.html` — files
beginning with an underscore are otherwise skipped by Jekyll.

### Renaming the repository

The repository name appears in exactly three places. Change it in all three and
nothing else needs touching:

- `README.md` (this file — the live-site link and the push instruction)
- `CITATION.cff` (`repository-code` and `url`)
- nowhere in the HTML — every internal link is relative, so the site works from
  any repository name, any subdirectory, and from a local folder with no server.

---

## Authoring a new unit page

1. Duplicate `units/_TEMPLATE.html`.
2. Rename it `unit-NN-short-title.html`.
3. Fill in each section, replacing every `TODO` block.
4. **Keep the section IDs unchanged** — `glance`, `objectives`, `lecture`,
   `worked`, `studio`, `selfcheck`, `hots`, `assignment`, `futures`,
   `resources`. The in-page navigation, the print layout, and the previous/next
   links all depend on them.
5. Add a card for the page in `units/index.html`.
6. Link the unit's readings directly to their sources, and keep every reading
   free to access.

`units/unit-01-the-ee-research-landscape.html` is written out in full as the
pattern to follow.

### House rules for unit content

| Section | What belongs there |
|---|---|
| Unit at a Glance | Week, phase, course outcomes, contact time, the graded deliverable |
| Learning Objectives | Five or six observable actions tied to the course outcomes |
| Lecture Discussion | Numbered subsections, narrative prose, tables for comparisons |
| Worked Example | One case carried end to end with the reasoning shown |
| Studio Activity | The in-class work that produces the unit's deliverable |
| Self-Check Quiz | Five short items with a collapsible answer key |
| HOTS Test | Twenty higher-order items — analysis, evaluation, creation |
| Reinforcement Assignment | Take-home work applied to the team's own project |
| Futures Essay | Three prompts, roughly 300 words each |
| Unit Resources | Free-to-access readings, each linked to its source |

---

## Styling

`assets/css/rtu-course.css` is the single source of truth for `index.html`,
`units/*.html`, and `templates/index.html`.

`syllabus.html` deliberately carries its own inline copy of the base theme so it
renders correctly when emailed, downloaded, or printed on its own — which is how
a syllabus is usually consumed. **If you change a colour or type rule in the
shared stylesheet, mirror it in `syllabus.html`.**

Useful classes: `.callout` (`.gold` `.green` `.red`), `.badge` (`.new`
`.updated` `.mandated` `.p1` `.p2` `.free` `.lib`), `.period-banner`,
`.timeline`, `.steps`, `.cardgrid` + `.card`, `.qlist` + `.opts`,
`details.key`, `.todo`, `.info-grid`, `.unit-row`, `.week-col`.

Every page prints cleanly: navigation is hidden, sections avoid page breaks,
answer keys collapse away, `TODO` notices disappear, and external links print
their full URL in small grey type.

---

## Readings policy

Every reading prescribed in this course is **free to access** — open-access
articles, open textbooks, government and standards-body publications, and
official vendor documentation. No paid textbook is required.

Three resources genuinely cannot be free and are marked separately in the
syllabus: IEEE Xplore full text, Scopus and Web of Science, and the Philippine
Electrical Code 2017. These are reached through University library credentials
or the College reference collection.

Where a team needs a paywalled source for the Phase 1 corpus, check the
publisher's own repository, the author's institutional repository, or the
journal's open archive before requesting library assistance. Cite the version of
record regardless of which copy was read, and never use pirated repositories.

---

## Academic integrity

Fabricated or beautified measurement data is the most serious offence in this
course — the entire value of Phase 2 rests on the claim that the reported
numbers came from the reported instrument on the reported day.

Generative AI may be used for language editing, code scaffolding, and literature
triage. Every such use is disclosed in the manuscript's AI-use statement, and AI
systems are never listed as authors. AI-generated citations that do not exist
are treated as academic dishonesty.

Full policy: [`syllabus.html#policies`](syllabus.html#policies).

---

## Licence

**All rights reserved.** See [`LICENSE`](LICENSE). Students enrolled in EE10 may
view, download, and print these materials for their own coursework. All other
use requires written permission from the Course Professor.

Third-party materials linked from these pages remain the property of their
respective copyright holders. Linking is not redistribution — no third-party
text is reproduced here.

---

*Last updated: 14 August 2026*
