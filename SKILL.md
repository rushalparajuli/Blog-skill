# Msty Blog Post Writer

## Scope
1. Work on Msty blog content under `content/blog`.
2. Match tone and structure in existing blog posts.
3. Return publish-ready markdown unless the user requests outline-only output.

## Before Writing
1. Identify post type: `product update`, `how-to/tutorial`, `thought leadership`, or `announcement`.
2. Read 2-3 similar posts in `content/blog` and mirror pacing, heading style, and depth.
3. Confirm required inputs: topic/title, author, publish date, audience, CTA.
4. If source material is provided (copy/paste, doc, pdf, transcript), extract key facts first and preserve factual claims.

## File and Slug Rules
1. New post path must be `content/blog/<slug>.md`.
2. Use lowercase kebab-case for `<slug>`.
3. Avoid spaces, uppercase, and numeric prefixes for new posts.
4. Keep slug stable unless the user explicitly asks to rename it.

## Frontmatter Standard
1. Use this key order:

```yaml
---
title: <Post Title

>
description: <One-sentence summary

>
date: YYYYMMDD
author: <Author Name

>
image: /blog/<asset-folder>/<hero-image-file

>
tags: [tag-one, tag-two]
# optional:
# ogImage: /blog/<asset-folder>/<og-image-file

>
---
```

2. `date` must be 8 digits in `YYYYMMDD`.
3. Include `author`.
4. Include `tags` as an array (`tags: []` if none).
5. Keep `description` concise and specific.
6. If hero image is not ready, keep `image:` present and list it in `Needed to publish`.
7. Use `ogImage` only when needed.

## Body Structure Standard
1. Do not add an H1 in the body; the title comes from frontmatter.
2. Start with 1-3 short paragraphs explaining scope and value.
3. Use clear H2 sections (`##`) with outcome-focused headings.
4. Keep paragraphs short and scannable.
5. End with a conclusion or next-step CTA.

## Tone Standard
1. Write in Msty voice: direct, practical, privacy-forward, technically credible.
2. Explain workflow impact before deep implementation detail.
3. Prefer concrete claims over hype.
4. Keep language clear for both technical and non-technical readers.

## Media Rules

### YouTube
1. If a YouTube URL is provided, add an embed near the top unless asked otherwise:

```md
## Video Guide

::youtube-player{videoId="VIDEO_ID"}
::
```

2. Extract `VIDEO_ID` from:
```text
https://www.youtube.com/watch?v=VIDEO_ID
https://youtu.be/VIDEO_ID
https://www.youtube.com/shorts/VIDEO_ID
```

3. Keep plain YouTube links only when needed in a resources section.

### Images
1. Prefer this component for in-post visuals:

```md
::blog_image
---
src: /blog/<asset-folder>/<file-name>.png
alt: <Accessible description

>
caption: <Optional caption

>
---
::
```

2. `alt` is required.
3. `caption` is optional but recommended for explanatory screenshots/charts.
4. Markdown image syntax is allowed when explicitly requested or when matching existing nearby style.

### Non-YouTube Video
1. For hosted MP4 video, use:

```md
::blog_video
---
src: https://...
alt: <Accessible description

>
caption: <Caption

>
---
::
```

## Asset Placement Rules
1. Store new assets in `public/blog/<asset-folder>/`.
2. Use a folder name based on the slug or a short readable variant.
3. Use lowercase kebab-case filenames.
4. Reference assets in posts as `/blog/<asset-folder>/<filename>`.
5. If the user supplies images, move/copy them into that folder before finalizing links.

## Source-to-Post Workflow
1. Extract facts, claims, and chronology from source material.
2. Rewrite for clarity and flow without changing factual meaning.
3. Remove redundancy and tighten structure.
4. Ask only blocking questions when critical publish inputs are missing.
5. Deliver a full publish-ready draft unless outline-only is requested.

## Drafting Workflow
1. If title is not final, propose 3 title options.
2. Produce full markdown with normalized frontmatter and structure.
3. Add embeds/components for provided media links/assets.
4. Match repository conventions.

## Final Validation Checklist
1. Path matches `content/blog/<slug>.md`.
2. Frontmatter has valid `title`, `description`, `date`, `author`, `image`, and `tags`.
3. `date` format is valid `YYYYMMDD`.
4. Body has no H1.
5. Any provided YouTube URL has a matching `::youtube-player` embed.
6. All `/blog/...` references resolve to files under `public/blog/...`.
7. Tone and structure align with current Msty blog posts.
8. Spelling, grammar, and links are clean.

## Output Contract
1. Return full markdown post content.
2. Return recommended file path: `content/blog/<slug>.md`.
3. Return required asset folder path: `public/blog/<asset-folder>/`.
4. If anything is missing, end with a short `Needed to publish` list.
