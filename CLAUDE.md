# CLAUDE.md — editing conventions for this course site

This is the live syllabus for a graduate seminar in Research Methods in Construction Engineering and Management (SNU, Dept. of Architecture and Architectural Engineering). Students read the rendered site; ETL links to it. Treat every edit as something ~16 students will see within the hour.

## Non-negotiables

**Never invent a citation.** Do not guess an author list, year, volume, or DOI. If a reference cannot be verified, either leave it out or add it with an explicit `<!-- VERIFY -->` comment and tell the user in your reply. A fabricated citation in a research methods syllabus is worse than a missing one.

**Exemplar vs. methods reading.** These are different things and the distinction is load-bearing:

- An **exemplar** is an empirical study that *used* the method. Students reverse-engineer its design (RQ → design → data → analysis → claim → limits). Label: `[X exemplar]`.
- A **CEM methods reading** is an essay, review, position paper, or how-to *about* the method. Label: `*CEM methods reading (discussion, not an exemplar):*`.

Most papers in the ASCE *Second Special Collection on Research Methodologies in CEM* (JCEM 2022–23) and the 2010 JCEM special issue (Vol. 136 No. 1) are methods readings, **not** exemplars. Spearing et al. (2022) is the notable exception — it is genuinely empirical. Never file a methods reading under exemplars; the Exemplar Analyst role becomes impossible to perform.

**Every method week needs at least two exemplars.** Weeks 4–14. If a good second exemplar genuinely does not exist for a method (as with mixed methods in Week 6), say so honestly in the text and treat the absence as information about the field. Do not pad with a weak paper.

**Every Methods readings list ends with a recommendation line:**

```
→ **If you only have time for one:** [reading]. [One sentence on why — tie it to
that week's lab or discussion, not just to length.]
```

## Renumbering discipline

Week numbers appear in many places. If a week is added, removed, or moved, update **all** of these in the same edit:

1. `calendar.qmd` — the master table
2. `schedule.qmd` — week headings and any cross-references between weeks
3. `methods.qmd` — the "Week" column in all five inventory tables (A–E), plus the cross-cutting concerns paragraph
4. `syllabus.qmd` — which weeks run roles (§ Weekly roles), the roles-per-student arithmetic, Lab numbers in the assessment table, and week references in the rubrics
5. Lab numbering in `schedule.qmd` — labs are numbered sequentially across the semester, and six of them are graded
6. `handouts/` — any handout that names a week or date
7. Fischer's four test methods table in Week 3 — it maps each test method to the weeks that teach it

Getting this wrong has happened before. Check all seven.

## The horseshoe is the spine

Fischer's CIFE horseshoe is introduced in Week 3 and closed in Week 14. Preserve these threads:

- Every **Method Card** ends by naming which horseshoe box the method serves.
- Week 3 flags honestly that the horseshoe fits artifact-producing research better than interpretive research; Week 6 supplies the contrast (Eisenhardt's inductive process model); Week 14 supplies the rival (Hevner's DSR). Do not quietly drop any of these three beats.
- The **Horseshoe Wall** is revised weekly and graded twice (W3, W11).
- The Yoon, Kim, Park & Ahn (2023) deictic-gesture line of work is the worked local example, introduced in Week 3 and returning as an exemplar in Week 11.

## Voice

Written for students, second person, direct. Not administrative boilerplate and not a lecture.

Instructor-facing rationale ("we changed this because the 2025 version was lecture-forward…") does **not** belong on the public site — it goes in `instructor/notes.md`, which is excluded from rendering and gitignored, so it never leaves your machine. Prep burden, staffing, elective swaps under consideration, and the dataset to-do list all live there too. Back it up yourself; GitHub is not holding a copy.

Keep the honest caveats. Where the field lacks a clean exemplar, where a framework has limits, where a statistic is often reported as ritual — say so plainly. That candor is the pedagogical point, not a rough edge to smooth.

## Every substantive edit

1. Update `last-updated:` in `_quarto.yml`.
2. Add an entry to the top of `changelog.qmd` under a new dated `##` heading. Log readings, deadlines, restructuring. Do not log typos or formatting.
3. If a **date or deadline** moved, say so in your reply so the user remembers to post an ETL announcement. The site alone is not sufficient notice for a schedule change.
4. Run `quarto render` and confirm the build is clean before committing.

## Committing

Commit messages: short imperative subject, one line of why if it is not obvious.

```
Add Week 9 SEM exemplar from Doloi (2013)

Week 9 had only one exemplar; the regression half of the lab had no model paper.
```

Do not commit `_site/` or `.quarto/` — both are gitignored.

## Things not to do

- Do not host reading PDFs in this repo. DOI links only; licensed copies go in ETL.
- Do not add an `instructor/` file to the `render:` list in `_quarto.yml`, and do not `git add -f` it — the repo is public.
- Do not convert the honest "no clean exemplar exists" passages into confident recommendations.
- Do not expand the reading lists without checking the load. Roughly three items per week for everyone, with role-holders reading two or three more. The lists are already deliberately over-supplied; adding is usually worse than substituting.
