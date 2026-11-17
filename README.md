# ourhoa.info

A searchable reference for the governing documents of Fossil Lake Homeowners Association, Inc.
Every section has its own link, and a complaint page builds the written complaint the
Enforcement Policy requires.

It is a static site with no build step.

| File | What it is |
| --- | --- |
| `index.html` | The whole site: layout, search, section links, complaint page |
| `data.json` | The text of every document, one document per line |
| `pdf/` | The source PDFs each section links back to |
| `netlify.toml` | Tells Netlify to serve the repository root |

## Settings

The `SITE` block near the top of the script in `index.html` holds everything that changes if
this becomes the Association's official site:

- `official`: `false` shows "Unofficial resident reference"; `true` switches the label and disclaimer
- `complaint.recipientEmail` and `complaint.recipientAddress`: where complaints are sent
- `publicUrl`: leave empty to use whatever address the site is served from

## About the text

Six documents were transcribed from scans (Covenants, Bylaws, Articles of Incorporation,
Enforcement Policy, the delegation resolution and the Disputes Policy). They were proofread and
their figures checked against the page images, but small errors may remain. The recorded and
adopted documents control.

The Covenants PDF here is pages 1 to 41 of the recorded document. Exhibit A (property
description) and Exhibit B (owner approvals) are not included.

## Run locally

    python3 -m http.server

Then open http://localhost:8000.
