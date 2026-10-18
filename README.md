# labs-practices-skill

An [Agent Skill](https://www.anthropic.com/news/skills) packaging of the text content from the [Labs Practices Site](https://labspractices.com/) — agile/product practices and workshops, technical and team guides, and structured learning paths.

This repository is a GitHub fork of [joemoore/labs-practices-site](https://github.com/joemoore/labs-practices-site). Instead of the Hugo site itself (layouts, theme, build scripts, assets), it carries over only the site's Markdown content under `content/{practices,guides,learningpaths,topics,languages}/`, copied verbatim, reorganized as a skill:

```
SKILL.md              - what the skill does, when to use it, how to navigate it
references/
  practices/           - 51 files: facilitated team exercises (retros, prioritization, research, design)
  guides/               - 30 files: technical/team how-tos (REST, microservices, test doubles, ADRs, remote work)
  learningpaths/        - 121 files: multi-lesson curricula (Swift modernization, cloud-native dev, leadership)
  topics/               - 10 files: short subject-area overview pages
  languages/            - 8 files: Java/.NET landing pages and newsletters
```

Each `references/<category>/index.md` is a generated table of contents (not part of the original site); every other file is byte-for-byte identical to its counterpart in the upstream repo's `content/` tree. Korean translations (`*.kr.md`) and binary assets (images, PDFs) were not carried over — this is a text reference, not a working copy of the site.

See `SKILL.md` for how an agent should use this content (navigation, resolving the site's internal `/category/slug/` links to local files, and pulling facilitation metadata like `why`/`when`/`what`/`participants` out of each practice's front matter).

## License

Apache License 2.0, inherited from the upstream [Labs Practices Site](https://github.com/joemoore/labs-practices-site) — see [LICENSE](LICENSE).
