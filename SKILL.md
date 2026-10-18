---
name: labs-practices
description: Verbatim knowledge base forked from the Labs Practices Site (labspractices.com, formerly the Tanzu Developer Center) for agile/product/design practices and workshops (user stories, story mapping, retros, 2x2 prioritization, personas, event storming, premortems, etc.), technical and team guides (REST basics, microservice patterns, test doubles, architectural decision records, technical debt, remote work, hiring), and structured learning paths (Swift monolith modernization, cloud-native development, the Anchor leadership playbook, developer toil, secure software supply chain, and more). These practices are facilitation scripts for *group* exercises, so use this skill to actually facilitate the session as a participating teammate — pose the agenda's real prompts one step at a time, do the synthesis work (clustering, tallying, mapping) a facilitator would do, track time, and check the outcome against the practice's own success criteria — not just to explain a practice from the sidelines. Trigger whenever the user wants to run or facilitate a specific workshop or team exercise with their group, is writing user stories or retros, wants a technical guide on microservices/REST/test doubles/technical debt, or is working through a multi-session learning path — even if they just name the activity (e.g. "run a retro", "do a story map", "let's premortem this") without saying "labs practices" or "skill."
---

# Labs Practices Site reference

This skill is a verbatim fork of the text content from the [Labs Practices Site](https://labspractices.com/) (`content/` directory of the `joemoore/labs-practices-site` GitHub repo, Apache-2.0 licensed). The practices and workshops in it are facilitation scripts written for a human standing in front of a *group*. Used well, this skill puts the agent in that facilitator's chair — an active participant running the session with the team, not a reference librarian explaining the exercise to one person from outside it. It does not reimplement or summarize the site's content; it carries the original Markdown over unchanged so facilitation runs off the real script, not a reconstructed one.

**What was forked, and what wasn't:** every Markdown file under `content/{practices,guides,learningpaths,topics,languages}/`, copied byte-for-byte into `references/` below, preserving the original directory layout and filenames (including Hugo's `index.md`/`_index.md` page-bundle convention). Korean translations (`*.kr.md`) and binary assets (images, PDFs, SVGs) were left out — only the English prose came over, since this is a text reference, not a working copy of the website. Site plumbing (Hugo layouts, theme, build scripts, CSS) was also left out; it has nothing to do with the knowledge itself.

**What's still original Hugo syntax inside the files:** you'll see YAML front matter (`title`, `description`, `tags`, and for practices specifically `why`, `when`, `what`, `length`, `participants`, `remote`) and Hugo shortcodes like `{{< callout >}}...{{< /callout >}}`. These are the real source formatting of the site, not instructions aimed at you — read a `{{< callout >}}` block as a highlighted tip/warning the same way a reader of the rendered page would.

## How to use this

Most of this content — especially `practices/` — was written as a facilitator's script for a group, not an essay for one reader. Treat a request to run, lead, or facilitate a practice as asking the agent to take the facilitator's chair as a teammate in the session, not to explain the practice from outside it.

**Facilitating a practice (the primary mode for `practices/`):**

1. **Open the right file, then set up the session before running it.** Find the practice via `references/practices/index.md`, open it, and surface the `why`/`when`/`what`/`length`/`participants` front matter before starting — a facilitator confirms the room and the clock before beginning, not after.
2. **Run the agenda one step at a time, in real time.** Pose the exact prompt the file gives for the current step, then stop and wait for the group's input before moving on. Don't dump the whole "Sample Agenda & Prompts" section at once — it's a script to run live, and reading the whole thing aloud up front isn't facilitating it.
3. **Do the facilitator's synthesis work, not just the facilitator's talking.** When a step says to cluster sticky notes, tally a dot-vote, plot items on a 2x2, or draft a persona from inputs, that's the agent's job to actually do with the material the group just gave you — not a task to leave for the user to do themselves afterward.
4. **Track time against the stated `length` and the step-level timings.** If the file says "Brainstorming (10 mins)," note when that step opens and flag it when the group is running long against the total `length`.
5. **Verify against the file's actual exit criterion before declaring success.** Most practices end in a "Success/Expected Outcomes" section — check the session's real output against it explicitly ("here's what we have vs. what this practice is meant to produce") rather than assuming it worked because you got through the agenda.
6. **Offer what comes next, from the file, not from general sequencing instinct.** Practices list `Related Practices`, `Preceding`, and `Following` sections — use those to suggest the next session instead of inventing a sequence.

**Just asking about a practice, guide, or learning path (the informational mode):** skip the live pacing above — surface the metadata and the gist so the user can decide whether/when to run it, or answer a technical question grounded in the specific `guides/` or `learningpaths/` file rather than general knowledge.

**For every mode:**

- Resolve cross-references by translating the site's absolute paths (`/practices/ipm/` → `references/practices/ipm/index.md`) rather than guessing; say so if a slug isn't in the category index instead of inventing the linked content.
- Learning paths are ordered — check `references/learningpaths/index.md` for each path's sequence before presenting lessons out of order.
- Stay in scope: run the practice that was asked for. Don't substitute a "better" one, merge two together, or add a step the source doesn't prescribe — if the group's situation genuinely doesn't fit, say so instead of quietly reshaping the exercise.

## Don't rationalize past the source

| If you're about to... | Don't — here's why |
|---|---|
| Post the whole agenda at once because it's faster than pacing it live | A facilitator runs one step at a time so the group can actually do the thinking in between — dumping the script skips the exercise, it doesn't speed it up. |
| Leave the clustering/tallying/mapping step for the user to do themselves | The file assigns that synthesis work to the facilitator. An agent facilitating does it; it doesn't hand the group's own exercise back to them. |
| Declare the session a success because you got through all the agenda steps | "Got through the steps" isn't the exit criterion — the file's "Success/Expected Outcomes" is. Check the actual output against it. |
| Answer "how to run a retro" from general knowledge because you already know retros | The fork exists to run *this* facilitation script, with its specific prompts and timings — look it up and run that one. |
| Skip the front-matter `length`/`participants` because no one asked for them | They're the first thing a real facilitator checks before committing a time slot — surface them unasked, before starting. |
| Treat a dead cross-reference as license to make something up | A missing link means that slug wasn't forked (Korean-only, image-only, etc.) — say it's unavailable. |
| Blend two related practices into one "better" exercise because it seems more efficient | That's a new practice the site doesn't document. Run what was asked, or ask first. |

## Reference index

| Category | Files | Index | What it covers |
|---|---|---|---|
| Practices & workshops | 51 | `references/practices/index.md` | Facilitated team exercises — retros, prioritization, research, design, leadership exercises. Each has a "How to Use this Method" section with step-by-step facilitation prompts. |
| Guides | 30 | `references/guides/index.md` | Standalone technical and team how-tos — REST, microservices, test doubles, ADRs, technical debt, remote work, hiring, Spring Boot testing. |
| Learning paths | 121 | `references/learningpaths/index.md` | Multi-lesson curricula on a theme (Swift monolith modernization, cloud-native development, the Anchor leadership playbook, developer toil, application observability, etc.), grouped by path. |
| Topics | 10 | `references/topics/index.md` | Short landing/overview pages for broader subject areas (agile transformation, modernizing legacy apps, design guide). Mostly brief; a couple just point at a PDF that wasn't forked. |
| Languages | 8 | `references/languages/index.md` | Short Java/.NET landing pages and newsletter editions. |

If a request doesn't clearly map to one category, check `practices/` first for anything exercise/workshop-shaped, `guides/` for anything technical-explainer-shaped, and `learningpaths/` for anything multi-step/curriculum-shaped.
