# PCA History: content

The public content of [PCA History](https://pca.epixian.com): a timeline of dated,
sourced events in the history of the Presbyterian Church in America (PCA) and its
predecessors. Each event is a short note with a citation to a primary source and an
exact quote from the cited page. Events link to the earlier events they respond to.

This repository holds the content only. The site is built from a separate
repository, and this one is updated from it. To suggest a correction or a new
event, see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

The project's own work (schema, data, and the text written for it) is under the MIT
License. Quotations and source documents are copyright their original authors and
publishers. See [LICENSE](LICENSE).

## Layout

| Path | Contents |
|---|---|
| `content/events/` | One Markdown file per event |
| `content/actors/` | Bodies, churches, committees, people, publications |
| `content/issues/` | Topics; an issue can have a parent issue |
| `content/sources/` | Sources (minutes, studies, overtures, court records, news, opinion) |
| `content/glossary.yml` | Abbreviations that are not actors |
| `reports/` | Research notes for some topic passes |

## Event format

File name: `content/events/<id>.md`. The id is a short slug with no date, for
example `liberti-commissions-diaconate`. The id never changes, even when the date
changes.

```yaml
---
title: RPR cites PP for the Liberti commissioning
date: 2007-06              # EDTF: when the act happened (see below)
place: Memphis, TN         # optional: where it happened
actors: [rpr]              # who acted; these make the timeline lanes
subjects: [philadelphia-presbytery, liberti-church]   # optional: who it was about
issues: [women-deacons, rpr-review]
responds_to: [liberti-commissions-diaconate]          # earlier events; a list
kind: act                  # optional: act (default) | meeting (e.g. a General Assembly; issues optional)
series: general-assembly   # optional: a series of regular events (prev/next links); names in build.py SERIES
part_of: ga36              # optional: the meeting event this act belongs to; the meeting page lists its acts
status: draft              # draft | reviewed | needs-citation
visibility: public         # public | private (private events are not published)
citations:
  - source: m35ga          # id of a file in content/sources
    pages: "209"           # printed page or range "305-306"; omit if none
    quote: "exact words copied from the extracted page text"
---
One to three sentences in plain, neutral English, in the past tense. Say what
happened. Do not argue or conclude.
```

### Dates (EDTF)

| Value | Meaning |
|---|---|
| `2007` | some time in 2007 |
| `2007-06` | June 2007 |
| `2006-11-11` | an exact day |
| `2007?` | uncertain |
| `2007~` | approximate |
| `../2002` | on or before 2002 (open start) |
| `1992/2025-09-18` | a span from 1992 to 2025-09-18 |
| `../2025-09-18` | a span with an unknown start |

Use the date of the act, not the date of the minutes that record it. RPR reviews
presbytery minutes from earlier years, so the two dates often differ.

### Rules for citations

- Copy each quote from the extracted page text (`tools/show.py`), not from a
  secondary source. Keep quotes short: one phrase or sentence is enough.
- The build fails when a quote is not on the cited pages. The check ignores case,
  spaces, punctuation, and line-break hyphens.
- An event with no source yet has `status: needs-citation` and no `citations`.
- Events about living private people, or about local church matters that are not
  in public records, use `visibility: private`.

## Actor format

```yaml
---
name: Philadelphia Presbytery (PP)
kind: presbytery     # denomination | assembly | committee | presbytery | church | person | publication | organization
parent: pca          # optional: the body this actor belongs to
place: Philadelphia, PA   # optional
start: 1973          # optional EDTF
end: 1982            # optional EDTF
merged_into: pca     # optional
visibility: private  # optional
links:               # optional; organizations and public figures only; official accounts only
  website: https://example.org/
  x: https://x.com/handle    # also bluesky, threads, facebook, instagram, youtube, tiktok,
                             # linkedin, substack, podcast, wikipedia (full URLs; https where the site has it)
---
```

## Issue format

```yaml
---
title: Women and the diaconate
parent: women-in-ministry   # optional
---
One sentence that describes the issue.
```

## Source format

```yaml
---
short: M36GA
title: Minutes of the 36th General Assembly
date: 2008
kind: minutes        # minutes | study | statement | overture | court | book | news | opinion | article | website
# Three kinds of evidence:
#   record    (minutes, overture, court, news): what a body did - cited as fact
#             (court: complaints, reports and indictments in a church court case)
#   position  (statement; an adopted study): a stance a body formally adopted - cited for the
#             fact that it holds the stance, and its exact words
#   opinion   (opinion, most articles and books): what authors argued, with no body adopting it
url: https://pcahistory.org/pca/ga/36th_pcaga_2008.pdf
fetch: https://...    # optional: where tools/fetch.py downloads the text, if not from url (e.g. an X post mirror)
meeting: ga36        # optional: the meeting event these minutes record (links both ways)
origin: unknown      # optional: a copy posted online by a party we cannot identify (shown as a badge)
link: false          # optional: cite the source, but never link to it or show its pages
                     # (for a document that names private individuals)
---
```
