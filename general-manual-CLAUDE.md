# CLAUDE.md — Raredon Lab General Manual

## Project overview

A general lab manual for the Raredon Lab (PI: Dr. Micha Sam Brickman Raredon, Yale School of Medicine, Dept. of Anesthesiology) that applies to **all lab members** regardless of role. It covers authorship, mentorship, career development, general expectations, lab culture, and administrative policies.

The deliverable is a linked set of standalone HTML files — same design system as the Computational and Wet Lab manuals — hosted on GitHub Pages.

This is one of three sibling manuals. The other two are the **Computational Lab Manual** and the **Wet Lab Manual**. Cross-links between them will use absolute GitHub Pages URLs once all three are live.

**Status: New project. No documents drafted yet. Content must be elicited from the PI before writing begins.**

---

## Document plan (draft — confirm with PI before building)

The following topics are expected based on cross-references in the Computational Manual. The exact document list and section structure must be established through PI elicitation.

| Expected file | Expected title | Notes |
|---------------|----------------|-------|
| `index.html` | Overview & index | Landing page |
| `01-lab-mission.html` | Lab mission and identity | Who we are, what we are trying to accomplish, broadly |
| `02-joining-the-lab.html` | Joining the lab | Expectations, onboarding, mentorship structure |
| `03-authorship.html` | Authorship principles | CRediT taxonomy, authorship conversations, disputes. **Referenced from Computational Manual 07.** |
| `04-first-author.html` | Responsibilities of first authors | The full first author standard. **Referenced from Computational Manual 07 and 08.** |
| `05-mentorship.html` | Mentorship and career development | PI's role, mentorship expectations, career planning |
| `06-communication.html` | Communication and conduct | Lab culture, meetings, responsiveness, conflict |
| `07-safety.html` | General safety | Lab-wide safety expectations (non-wet-lab-specific) |
| `08-leaving-the-lab.html` | Leaving the lab | Exit expectations, letters of recommendation, alumni relationships |

---

## Design system

**Identical to the Computational Manual.** Copy all CSS exactly.

**Fonts (Google Fonts):** IBM Plex Serif (headings), IBM Plex Sans (body), IBM Plex Mono (code/labels)

**CSS variables:**
```css
:root {
  --sidebar-w: 256px; --header-h: 54px;
  --bg: #FFFFFF; --sidebar-bg: #F6F5F1; --border: #E3E1DC;
  --text-p: #1A1917; --text-s: #5C5A56; --text-t: #9C9A96;
  --accent: #1D4ED8; --accent-lt: #EFF6FF; --accent-bd: #BFDBFE;
  --code-bg: #F6F5F1; --code-bd: #D8D6D0;
  --note-bg: #F0FDF4; --note-bd: #16A34A;
  --warn-bg: #FFFBEB; --warn-bd: #D97706;
  --rule-bg: #FFF1F2; --rule-bd: #E11D48;
  --font: 'IBM Plex Sans', sans-serif;
  --font-serif: 'IBM Plex Serif', serif;
  --font-mono: 'IBM Plex Mono', monospace;
}
```

**Layout:** Fixed dark header (`#141210`, 54px). Fixed left sidebar (256px). Content: `margin-left: 256px`, `max-width: calc(256px + 800px)`, `padding: 52px 60px 100px`. Sections use `scroll-margin-top: calc(var(--header-h) + 20px)`.

**Component classes:** `.call.note`, `.call.warn`, `.call.rule`, `.call.info`, `.cb-wrap` + `.cb-label` + `<pre>`, `.steps` + `.snum`, `.dodont`, `h2` with `.sn` span.

---

## Writing principles

**Identical to the Computational Manual.** Apply to every sentence of prose.

1. **Limit em-dashes.** Only where a comma or colon would genuinely be weaker. Always grep for `—` before finalizing.
2. **No self-negation / auto-negation.** Speak directly to what is true.
3. **No rhetorical triplets.** Unless each element is informationally distinct.
4. **Never use "genuine" or "genuinely."**
5. **Frame as guidance, not group mandate.** Use second person ("you"). Give reasons for requirements.
6. **Nurturing tone.** Readers are learners. Frame standards in terms of their payoff.
7. **Assume an intelligent reader.** Do not over-explain.

---

## Hard rules on content

- **No specific lab member names** anywhere. Use role descriptions.
- **No "we" framing** in instructional prose except in mission/identity context.
- **Reading and writing scientific papers** is reserved for human authors. AI may assist with grant text only.

---

## Process for drafting documents

1. Elicit content from the PI with targeted questions before writing anything.
2. Draft as complete, browser-ready HTML using the design system above.
3. Present with `present_files`.
4. Iterate with `str_replace` for targeted edits.
5. Before finalizing: grep for `—`, scan for self-negation and "genuine/genuinely."

---

## Cross-linking

Once the General Lab Manual is live on GitHub Pages, update the following placeholder references in the **Computational Manual**:
- `07-ethics-teamwork.html` §1: "General Lab Manual — Authorship Principles"
- `07-ethics-teamwork.html` §2: "General Lab Manual — Responsibilities of First Authors"
- `08-publication.html` §5: "General Lab Manual — Responsibilities of First Authors"

The Computational Manual GitHub Pages URL should also be linked from the General Lab Manual index.

---

## PI context and sensibility

- Audience: all Raredon Lab members (computational, wet lab, clinical, rotation students, undergrads, postdocs, staff scientists).
- This manual should feel welcoming to non-computational readers. Avoid technical computing language unless the context requires it.
- Tone: same as Computational Manual — rigorous, direct, academic, written by a thoughtful scientist.
- The PI has strong opinions on authorship, credit, mentorship, and lab culture. Much of Document 07 of the Computational Manual contains relevant source material to draw from and expand here.
- The General Lab Manual should not duplicate the Computational Manual — it should cross-link to it for computational-specific content and cover what is universal to all lab members.
