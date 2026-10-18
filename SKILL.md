---
name: labs-practices
description: Verbatim knowledge base forked from the Labs Practices Site (labspractices.com, formerly the Tanzu Developer Center), covering agile/product practices and workshops (user stories, story mapping, retros, 2x2 prioritization, personas, event storming, premortems, etc.), technical and team guides (REST basics, microservice patterns, test doubles, architectural decision records, technical debt, remote work, hiring), and structured learning paths (Swift monolith modernization, cloud-native development, the Anchor leadership playbook, developer toil, secure software supply chain, and more). Use this skill whenever the user wants to run a specific agile/product/design workshop, needs step-by-step facilitation instructions for a team exercise, is writing user stories or retros, wants a technical guide on topics like microservices/REST/test doubles/technical debt, or is working through a multi-session learning path on application modernization or engineering leadership — even if they just name the activity (e.g. "run a retro", "do a story map", "set up a premortem") without saying "labs practices" or "skill."
---

# Labs Practices Site reference

This skill is a verbatim fork of the text content from the [Labs Practices Site](https://labspractices.com/) (`content/` directory of the `joemoore/labs-practices-site` GitHub repo, Apache-2.0 licensed). It does not reimplement or summarize the site's practices, guides, and learning paths — it carries the original Markdown files over unchanged so you can draw on the real instructions, facilitation notes, and explanations verbatim instead of reconstructing them from memory.

**What was forked, and what wasn't:** every Markdown file under `content/{practices,guides,learningpaths,topics,languages}/`, copied byte-for-byte into `references/` below, preserving the original directory layout and filenames (including Hugo's `index.md`/`_index.md` page-bundle convention). Korean translations (`*.kr.md`) and binary assets (images, PDFs, SVGs) were left out — only the English prose came over, since this is a text reference, not a working copy of the website. Site plumbing (Hugo layouts, theme, build scripts, CSS) was also left out; it has nothing to do with the knowledge itself.

**What's still original Hugo syntax inside the files:** you'll see YAML front matter (`title`, `description`, `tags`, and for practices specifically `why`, `when`, `what`, `length`, `participants`, `remote`) and Hugo shortcodes like `{{< callout >}}...{{< /callout >}}`. These are the real source formatting of the site, not instructions aimed at you — read a `{{< callout >}}` block as a highlighted tip/warning the same way a reader of the rendered page would.

## How to use this

This is reference content, not a canned workflow — so turn *consulting* it into one. Don't paraphrase from memory; open the file, and don't consider the answer finished until you can point at the evidence line called out in step 6.

1. **Classify the request, then find the exact file before answering.** Decide whether the user wants to run an exercise (→ `practices/`), get a technical explanation (→ `guides/`), work through a curriculum (→ `learningpaths/`), or get oriented (→ `topics/`/`languages/`). Search that category's `index.md`, then open the matching file. Answering from the title alone, or from general knowledge of "how retros usually work," is the exact failure mode this skill exists to prevent.
2. **Follow the file's actual steps; don't improvise around them.** Quote or closely follow the real "How to Use this Method" / step sections — timings, headcounts, and specific prompts included. If you want to add a tip the source doesn't have, say explicitly that it's your addition, not the site's.
3. **Surface the decision-relevant metadata up front.** For practices: `why`, `when`, `what`, `length`, `participants` from the front matter. These are the facts a facilitator checks before agreeing to run something — don't bury them below the agenda.
4. **Learning paths are ordered — respect it.** Check `references/learningpaths/index.md` for each path's lesson order (numeric file prefixes or a `weight` front matter field) before presenting lessons out of sequence.
5. **Resolve cross-references; don't fabricate when they miss.** Site-internal links are absolute paths like `/practices/ipm/` — translate `/category/slug/` to `references/category/slug.md` (or `.../slug/index.md`). If the slug isn't in that category's index, say so instead of inventing the linked content.
6. **Close with the file's own definition of done.** Most practices end in a "Success/Expected Outcomes" section — restate it as the exit criterion for the exercise, not just another paragraph to read past. For guides, the equivalent check is whether the answer actually grounded itself in that specific file or drifted into generic advice. For learning paths, name which lesson you're on and what comes next.
7. **Stay in scope.** If asked to run the Premortem, run the Premortem — don't substitute a "better" practice, merge two practices together, or pad the agenda with a step the source doesn't prescribe. If the user's situation genuinely doesn't fit the practice they asked for, say so instead of quietly reshaping the content to fit.

## Don't rationalize past the source

Specific ways this skill gets used wrong, and why each one defeats the point of forking verbatim content instead of just knowing this stuff already:

| If you're about to... | Don't — here's why |
|---|---|
| Answer "how to run a retro" from general knowledge because you already know retros | The fork exists to use *this* facilitation script, with its specific prompts and timings — look it up anyway. |
| Skip the front-matter `length`/`participants` because the user didn't ask for them | They're the first thing a real facilitator checks before committing a time slot — surface them unasked. |
| Summarize a practice's steps in your own words to save space | The agenda's specific wording is the content being forked; paraphrasing it defeats the fork. |
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
