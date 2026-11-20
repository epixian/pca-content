# Contributing

Corrections and new events are welcome. Open a pull request, or open an issue if
you only want to point out a problem.

## What a change needs

- **A source.** Every event cites a source, with the page and a short quote copied
  exactly from that page. Primary sources come first: General Assembly minutes,
  presbytery and session records, overtures, court records, and the documents
  themselves. News reports and opinion pieces are cited for what they report or
  argue, and the event text says whose claim it is.
- **Plain, factual text.** One to three sentences in the past tense. Say what
  happened, who did it, and when. Do not argue, characterize motives, or draw
  conclusions. Let the quotes speak.
- **The schema.** See the formats in [README.md](README.md). Use existing actor and
  issue ids where they fit.

## Sources the maintainer cannot download

The site checks every quote against the text of the cited page. For that, the
maintainer downloads and archives each source.

- If the source is online, put its URL in the source file (`url:`).
- If it is not online (a scan, a PDF from a presbytery clerk, a printed book), attach
  the file to the pull request description, or link to a copy, and say where it
  came from.
- If you do not know who first posted a document, say so. The source file then gets
  `origin: unknown`.

## Privacy

Do not add events about private individuals or internal matters of a local church
that are not in a public record. People named in a public document (signers,
witnesses) can appear in its text, but they do not get an actor record unless the
name comes up again and again.

## How a change reaches the site

The maintainer reviews the pull request, archives its sources, checks every quote,
and adopts the change in the site repository. This repository is then updated from
the site repository, and the pull request is closed with a link to the update. Your
name stays on the change as a co-author.
