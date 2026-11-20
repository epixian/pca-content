# The Aquila Report: archive survey

Written 2026-11-20. This is a survey only. I did not create or change events, sources, actors or issues. I did not edit `content/`, `tools/` or the site.

The Aquila Report (TAR) is mostly an aggregator. Most posts are excerpts of articles from other outlets, with a "Read More" link to the original. For each candidate below, the "Original" column gives that outlet when the post names it. The original is usually the better source to cite. TAR's own staff reports (2008–2012) and full reprints of overtures and presbytery resolutions are the exception: for those, TAR is the first publisher.

## 1. How I surveyed

**Requests.** I made 121 requests in total, from 14:41 to 15:07 (New York time) on 2026-11-20. The cap was 400.

| Kind | Requests | What |
|---|---|---|
| robots.txt and sitemaps | 30 | `robots.txt`, `wp-sitemap.xml`, 26 post sitemaps, the category sitemap and the tag sitemap |
| WordPress REST listings | 35 | the category list; the "PCA General Assembly" category (7 pages, 644 posts, plus 1 request that got the 429 and was sent again later); the "Documents" category (2 pages, 118 posts); 21 searches; 2 batch look-ups by slug; 1 meta test |
| Article pages (HTML) | 56 | the bylines and source links of 55 candidates, plus 1 test page |

**Rules I followed.**
- `robots.txt` disallows only `/wp-admin/`. I requested nothing under it.
- I sent one request at a time. The gap between requests was at least 3.5 s for the sitemaps. After the 429 (below), the gap was at least 10 s.
- The User-Agent was the `UA` string from `tools/fetch.py`.
- I requested no images or media. The script refuses media URLs.
- Every response is in `cache/survey/aquila/`. The file name comes from the URL plus a short hash, and `requests.jsonl` logs every request. A re-run reads the cache and sends no request for a URL that it already has. The scripts and the parsed URL list are in `cache/survey/aquila/scripts/` (`aq.py` fetches; `extract.py` reads bylines; `hot2.py` makes the counts in section 4).

**The REST API and one 429.** The sitemaps give URLs and `lastmod` dates only, not titles or categories. So I also used the WordPress REST API (`/wp-json/wp/v2/posts`) as a listing: 100 posts per request, with title, date and excerpt. `robots.txt` does not disallow it. Request 38 (the seventh REST listing in about 40 seconds) got HTTP 429. I stopped, waited, and raised the gap to 10 s. No other request failed. The REST API does not give the byline, so I read the bylines from the article pages.

**Date range.** The sitemaps list 50,469 posts, from May 2008 to November 2026. All titles come from the URL slugs.

**Dates.** The sitemap `lastmod` is the last edit, not the publication date. For the counts, I estimated each publication date as the earliest `lastmod` of that post and all later posts (the post IDs increase with time). This estimate is good from 2010. It is poor for 2008–2009, because many old posts were edited on the same day (2009-06-24). Every date in the candidate tables in section 3 is the real TAR publication date, from the REST API or from the article page. A repost often comes days after the original (for example, Tooley's original is dated 2026-06-16 and the TAR repost 2026-06-25). So for an original with no date of its own, read the TAR date as "on or before".

**What I skipped.**
- I did not read any article beyond the 55 candidates.
- I did not follow any "Read More" link to the original outlet.
- I did not use the tag pages. TAR stopped using tags in about 2014.
- The "Documents" category (118 posts) has almost no PCA records. It holds doctrinal essays.
- WordPress search matches body text and returns the newest results first. Searches with more than 100 hits show only the newest 100. So I found candidates for the earlier years from the sitemap slugs, not from the searches.

**Negative findings.**
- **Appleton case.** TAR has no post on TE Rick Appleton or on the Pittsburgh Presbytery case. A search for "Appleton" found only a 2013 obituary of a different man.
- **Garris case.** TAR has two opinion posts on it (see 3.3). It has no news report and no court document.
- **Save the PCA.** TAR has no post with "Save the PCA" in its title. Related posts are the Matthew Lee piece already in the graph (`aquila-lee-2025`), the 2025 commentaries on "shepherdesses" (see 3.1), and "Semantic Range" (2026-04-13), which mentions "the Save the PCA data" from church websites.
- **CRC and NAPARC, 1990–2002.** TAR started in 2008, so it has no news from that period. I listed all 76 slugs with "crc", "christian-reformed" or "naparc". They report CRC synods from 2010 to 2026 (Belhar, women in office, sexuality, the 2024–2025 departures). None is about PCA–CRC relations. TAR has one retrospective on the 1995 GA, and NAPARC items from 2017 and 2025 (see 3.6).
- **Women in the military.** TAR has no post on a PCA GA action after 2002. It has one session statement (2014) and some opinion pieces (see 3.5).

## 2. Existing Aquila sources (excluded below)

`aquila-cn-52ga`, `aquila-cn-call-for-clarity`, `aquila-cn-problem-middle`, `aquila-lee-2025` and `aquila-lee-carr-2023` are already sources. They are not in the candidate lists.

## 3. Candidate sources for existing topics

"Byline" is the name that TAR prints. "Original" is the outlet that the "Read More" link or the closing note names. "Staff" means a TAR staff report. Items marked **(record)** reprint or report what a court did, and they point to a primary record.

### 3.1 Women in office, deaconesses, complementarianism

The graph already has the GA36–GA39 acts, the Liberti and RPR events, and the GA53 events. The TAR items below add presbytery actions, an SJC case and the reprinted texts of overtures from 2008–2012. Most of these presbytery actions are not in the graph yet.

| Date | Title | Byline | Original | URL | Could support |
|---|---|---|---|---|---|
| 2008-05-31 | Study on Women as Deacons Requested of PCA GA | Staff | TAR | https://theaquilareport.com/study-on-women-as-deacons-requested-of-pca-ga/ | **(record)** Lists GA36 Overtures 9 (Philadelphia), 15 (Western Canada), 17 (Rocky Mountain) and 19 (Central Georgia, against). Cross-check M36GA. |
| 2008-06-15 | General Assembly Rejects Study Committee on Women Deacons | Staff | TAR | https://theaquilareport.com/general-assembly-rejects-study-committee-on-women-deacons/ | **(record)** GA36, 2008-06-12: Overture 9 answered in the negative after 5.5 hours in the Overtures Committee; a minority report. Supports `ga36-acts-on-study-overtures`. |
| 2008-06-17 | PCA GA: Deaconesses Cannot Serve on Diaconates | Staff | TAR | https://theaquilareport.com/pca-ga-deaconesses-cannot-serve-on-diaconates/ | **(record)** GA36 finds the responses of Northern California and Philadelphia presbyteries "unsatisfactory" (RPR, BCO 9-3). Quotes the presbytery responses. |
| 2008-06-17 | Ohio Valley Presbytery Committee on Women Serving as Deacons | Staff | TAR | https://theaquilareport.com/ohio-valley-presbytery-committee-on-women-serving-as-deacons/ | **(record)** Full text of the Ohio Valley Presbytery committee report (adopted January 2008) on the diaconate of Redeemer PC, Indianapolis. A new presbytery-level event. |
| 2009-04-24 | Resolution Adopted by Rocky Mountain Presbytery on Women Serving as Deacons | Staff | TAR | https://theaquilareport.com/resolution-adopted-by-rocky-mountain-presbytery-on-women-serving-as-deacons/ | **(record)** Text of the resolution of 2009-04-23 (and of the April 2008 action). A new event. |
| 2009-10-28 | Proposed Overture on Deaconess to the 38th PCA General Assembly | Staff | TAR | https://theaquilareport.com/proposed-overture-on-deaconess-to-the-38th-pca-general-assembly/ | **(record)** Text of the Central Carolina Presbytery overture to amend BCO 9-7 (adopted 2009-10-27). It became GA38 Overture 2. |
| 2010-01-25 | Women May Be Deacons in Proposed BCO Amendment | Staff | TAR (cites the Bayly blog) | https://theaquilareport.com/women-may-be-deacons-in-proposed-bco-amendment/ | **(record)** The Westminster PC (Atlanta) session overture to Metro Atlanta Presbytery: "may be commissioned, but not ordained." MAP deferred it on 2010-01-23. |
| 2010-03-24 | Overture from Northern California to Clarify the Practice in the Ministry of Deacons in the PCA | Staff | TAR | https://theaquilareport.com/overture-from-northern-california-to-clarify-the-practice-in-the-ministry-of-deacons-in-the-pca/ | **(record)** Text of the NCP overture to GA38 (March 2010), with a proposed BCO 9-8. |
| 2010-04-19 | Tennessee Valley Presbytery Overtures PCA GA to Affirm Unordained Deaconesses | Staff | TAR | https://theaquilareport.com/tennessee-valley-presbytery-overtures-pca-ga-to-affirm-unordained-deaconesses/ | **(record)** Text of the overture (2010-04-17, from New City Fellowship). A second source for `tennessee-valley-overture-deaconesses-38ga`. |
| 2010-06-23 | PCA Committee on Constitutional Business Finds 3 Overtures on Deaconesses Contrary to Constitution | Don K. Clements | TAR | https://theaquilareport.com/pca-committee-on-constitutional-business-finds-3-overtures-on-deaconesses-contrary-to-constitution/ | **(record)** The CCB opinions on the six GA38 overtures, with votes (for example 8-0-0 on Overture 2). Cross-check M38GA. |
| 2010-11-08 | PCA Standing Judicial Commission Overturns Northern California Position Statement on Role of Women in Diaconal Functions | Don K. Clements | TAR | https://theaquilareport.com/pca-standing-judicial-commission-overturns-northern-california-position-statement-on-role-of-women-in-diaconal-functions/ | **(record)** SJC Case 2009-25 (Brown and Session of Grace PC v. Northern California Presbytery). The SJC annulled the presbytery's six-view statement and did not rule on the views. Primary record: the SJC report in M39GA. |
| 2011-05-19 | Metro Atlanta Presbytery (PCA) Rules Challenge to Its Deaconess Policy Out of Order | Wes White | weswhite.net (dead) | https://theaquilareport.com/metro-atlanta-presbytery-pca-rules-challenge-to-its-deaconess-policy-out-of-order/ | Says that MAP, Metro New York, NCP and Philadelphia each adopted the six-view resolution in 2009. Has a comment by an RPR member. |
| 2011-09-22 | PCA's Metro Atlanta Presbytery Rescinds Resolution Allowing for the Possibility of Women as Deacons | Staff | TAR | https://theaquilareport.com/metro-atlanta-presbytery-rescinds-resolution-allowing-for-the-possibility-of-women-as-deacons/ | **(record)** MAP rescinded its April 2009 six-point resolution on 2011-09-20. Links to `map-elects-women-diaconal` and the `rpr-cites-map-*` events. |
| 2012-03-07 | A Review of General Assembly Actions on the Issue of Deaconesses in the PCA (2007–2011) | Wes White | weswhite.net (dead) | https://theaquilareport.com/a-review-of-general-assembly-actions-on-the-issue-of-deaconesses-in-the-pca-20072011/ | A year-by-year list of GA35–GA39 actions with minutes page numbers (for example M38GA p. 270). Use it as a finding aid. |
| 2012-06-25 | PCA's Northern California Presbytery Submits to GA on Deaconess Issue | Wes White | his blog (dead) | https://theaquilareport.com/pcas-northern-california-presbytery-submits-to-ga-on-deaconess-issue/ | NCP's response to the RPR exception in 2012. It may close `rpr-cites-ncp-deaconesses`. |
| 2016-06-22 | PCA GA: AC Committee of Commissioners Recommends Not Erecting Study Committee on Women in Ministry | Staff | TAR | https://theaquilareport.com/pca-ga-ac-committee-of-commissioners-recommends-not-erecting-study-committee-on-women-in-ministry/ | **(record)** The CMC proposal and the 31-7 vote of the committee of commissioners. The GA44 floor then erected the committee (`ga44-forms-women-study-committee`). |
| 2016-12-27 | Westminster Presbytery Overtures PCA 45th GA Not to Receive Ad Interim Committee Report on Role of Women | Staff | TAR | https://theaquilareport.com/westminster-presbytery-overtures-pca-45th-ga-not-receive-ad-interim-committee-report-role-women/ | **(record)** Overture text (2016-11-12): "the 44th General Assembly erred." The answer is in M45GA. |
| 2017-04-21 | Report of the PCA Committee on Women Serving in the Ministry of the Church | Staff | pcaac.org | https://theaquilareport.com/report-pca-committee-women-serving-ministry-church/ | Excerpt and list of members of the 2017 report. The graph cites the minutes; no new event. |
| 2018-05-17 | Reservations about PCA Overture 13: Women and the Boards of the PCA | Daniel Schrock | TAR | https://theaquilareport.com/reservations-about-pca-overture-13-women-and-the-boards-of-the-pca/ | Opinion before `ga46-declines-women-on-boards` (Nashville Overture 13). |
| 2019-03-14 | Metro New York Presbytery Overtures 47th PCA GA to Allow Women to Be Ordained as Deacons | Staff | TAR | https://theaquilareport.com/metro-new-york-presbytery-overtures-47th-pca-ga-to-allow-women-to-be-ordained-as-deacons/ | **(record)** Full text of the MNY overture of 2019-03-13 (amend BCO 7-2, 9-3, 17-3, 24; add ch. 25). The answer is in M47GA. A new event. |
| 2019-06-11 | Women Serving on PCA Committees and Agencies? One More Time with Feeling | Daniel Schrock | TAR | https://theaquilareport.com/women-serving-on-pca-committees-and-agencies-one-more-time-with-feeling/ | Says that the PCA declined this "on three separate occasions." Cites M17GA and M46GA. Opinion. |
| 2023-05-01 | An Overture on Titles & Ordination | Brad Isbell | PCA Polity | https://theaquilareport.com/an-overture-on-titles-ordination/ | Background to GA50 Overture 26 (Northwest Georgia, BCO 7-3). Links to the pcaga.org PDF. Supports `nwgp-overture-titles`. |
| 2025-05-07 | The Problem with Commissioning Deaconesses | Zachary Garris | PCA Polity | https://theaquilareport.com/the-problem-with-commissioning-deaconesses/ | Opinion. Links to the byFaith piece "The Case for Commissioning, Not Ordaining, Deaconesses" and to a Protestia "investigation" (2025-02). |
| 2025-10-14 | The PCA's "Essgate" | Brad Isbell | Presbycast (Substack) | https://theaquilareport.com/the-pcas-essgate/ | Opinion on the "deaconess" and "shepherdess" titles after the Save the PCA report. |
| 2025-10-16 | Shepherdesses in the PCA? | Zachary Garris | American Reformer | https://theaquilareport.com/shepherdesses-in-the-pca/ | Repost of `amreformer-garris-2025` (event `garris-shepherdesses`). Cite the original. Links to X posts by Michael Foster. |
| 2025-11-24 | SJC and Study Report | Thomas Rickard | Medium (one part of a series; the first part, on PCA Polity, is already a source) | https://theaquilareport.com/sjc-and-study-report/ | Opinion. Part 6 of a series on commissioned deaconesses. Discusses SJC precedent. |
| 2026-01-07 | A Presbyterian Call to Prayer & Lament | Zachary Groff | PCA Polity | https://theaquilareport.com/a-presbyterian-call-to-prayer-lament/ | Introduces the "Call to Prayer & Lament" statement (pcaprayerandlament.com). A reply followed on 2026-02-19. Check the signers' text before you use it. |
| 2026-02-10 | The Last Gasp of a Progressive Feminist Agenda in the PCA? | Ryan Biese | Substack (rfbwcf) | https://theaquilareport.com/the-last-gasp-of-a-progressive-feminist-agenda-in-the-pca/ | Opinion before GA53 on deaconess and shepherdess titles. Biese also appears in the Garris case. |
| 2026-04-13 | Semantic Range | Thomas Rickard | PCA Polity | https://theaquilareport.com/semantic-range/ | Opinion: commissioning versus ordination. Issue `commissioning-vs-ordination`. |
| 2026-07-11 | PCA Adopts Danvers Statement Endorsing Complementarianism | Scott Barkley | Baptist Press | https://theaquilareport.com/pca-adopts-danvers-statement-endorsing-complementarianism/ | **(record, news)** GA53 Overture 61 (Calvary), 934-841-34; Overtures Committee 66-64-3. A second news source for `ga53-declares-danvers`. Cite Baptist Press. Discrepancy: Baptist Press says the vote was "on June 27", but the TAR daily GA updates run from June 22 to June 25, and a GA report is dated June 26. Check the day in the minutes. |
| 2026-09-15 | General Assembly Responds to Dissent Regarding Overture 37 | byFaith Staff | byFaith | https://theaquilareport.com/general-assembly-responds-to-dissent-regarding-overture-37/ | **(record)** The GA53 answer to the dissent on Overture 37 (Overtures Committee 115-14-1). Already a source: the byFaith original is `byfaith-ga53-dissent`. The two linked PDFs (the dissent and the answer) are not yet sources. |

Lower priority (title only, not read): "PCA Goes Back to Where It Started: Women's Ordination" (2016-06-29); "Didn't We Just Do This?" parts 1–3 (2016-06-08/10); "Why I Voted Against the Ad Interim Women in Ministry Study Committee Report" (2017-06-26); "The Crux of the Matter in the PCA Deaconess Debate" (2022-08-29); "Did the RPCES have Deaconesses? Yes and No." (2021-12-03, issue `rpces-heritage`); "Calvin's Deaconesses" (2026-02-04); "Women's Ordination Brings Tyranny" (2026-05-21); "The Deaconess & the Household of God" (2026-09-11).

### 3.2 Christian nationalism, theonomy, civil magistrate

| Date | Title | Byline | Original | URL | Could support |
|---|---|---|---|---|---|
| 2018-06-08 | The Westminster Confession of Faith, BCO 59, and the Civil Magistrate (Part 2) | Nathaniel Sheetz | TAR | https://theaquilareport.com/the-westminster-confession-of-faith-bco-59-and-the-civil-magistrate-part-2/ | Opinion on the overtures to make BCO 59 constitutional (marriage and the magistrate). |
| 2022-04-27 | Overture 26 to PCA General Assembly: A Statement on Political Violence | Scott Seaton | TAR | https://theaquilareport.com/overture-26-to-pca-general-assembly-a-statement-on-political-violence/ | **(record)** GA49 Overture 26 (Potomac), by its author. Links to the pcaga.org PDF. The GA49 answer is in M49GA. Issue `spirituality-of-the-church`. |
| 2024-04-10 | Thoughts on Overture 12 From the 2023 PCA General Assembly: Sending the Overture to the Civil Magistrate | T. David Gordon | TAR | https://theaquilareport.com/thoughts-on-overture-12-from-the-2023-pca-general-assembly-sending-the-overture-to-the-civil-magistrate/ | Opinion on WCF 31.4 and GA50 Overture 12. Gordon says that he sent a protest to Ascension Presbytery. Links to `ga51-commends-commission-letter`. |
| 2024-07-30 | 'Of the Civil Magistrate': How Presbyterians Shifted on Church-State Relations | Kevin DeYoung | The Gospel Coalition | https://theaquilareport.com/of-the-civil-magistrate-how-presbyterians-shifted-on-church-state-relations/ | Opinion and history of the 1788 revision of WCF 23, by the later GA52 moderator. |
| 2024-08-07 | No, the American Revision of the Westminster Standards Does Not Undermine Westminster's Civil Ethics | Ron DiGiacomo | philosophical-theology.com | https://theaquilareport.com/no-the-american-revision-of-the-westminster-standards-does-not-undermine-westminsters-civil-ethics/ | A reply to DeYoung (WCF 19.4, WLC 108). Pair it with the item above. |
| 2025-06-30 | Have I Been Condemned to Hell by the 52nd PCA General Assembly? | Larry Ball | TAR | https://theaquilareport.com/have-i-been-condemned-to-hell-by-the-52nd-pca-general-assembly/ | Opinion on `ga52-condemns-racial-superiority-teaching`. The actor `larry-ball` exists. |
| 2025-07-29 | PCA Christian Nationalism Study Committee Members Announced | Megan Fowler | byFaith | https://theaquilareport.com/pca-christian-nationalism-study-committee-members-announced/ | Repost of `byfaith-cn-committee-members`. Cite byFaith. |
| 2025-08-04 | On the PCA's Committee on Christian Nationalism | Philip D. Bunn | Providence Magazine | https://theaquilareport.com/on-the-pcas-committee-on-christian-nationalism/ | Opinion on the new committee and on Overture 47. |
| 2026-05-25 | The American Revision: Church, State, and Religious Liberty | Tony Arsenal | Reformed Arsenal | https://theaquilareport.com/the-american-revision-church-state-and-religious-liberty/ | Opinion on WCF 23 (1788). |
| 2026-06-15 | A Response to PCA's CN Study Committee | Miles Smith | Ad Fontes | https://theaquilareport.com/a-response-to-pcas-cn-study-committee/ | Repost of `adfontes-smith-cn-2026`. The graph has only the year. The original is dated on or before 2026-06-15. |
| 2026-06-25 | Presbyterians & Christian Nationalism | Mark Tooley | Juicy Ecumenism (2026-06-16) | https://theaquilareport.com/presbyterians-christian-nationalism/ | Repost of `ird-presbyterians-cn-2026`. |
| 2026-06-26 | The PCA's 2026 Louisville Assembly: Revival of the Right | David W. Hall | Reformed Politics (Substack) | https://theaquilareport.com/the-pcas-2026-louisville-assembly-revival-of-the-right/ | GA53 report with election vote counts (for example SJC and MNA board seats) and the stated clerk election. A news-type source for GA53, by an author who takes a side. |

Lower priority (2022–2023 titles from the sitemap; the months are estimates): "The Case for Christian Nationalism: Preliminary Considerations" (2022-11); "Christian Nationalism: Dump the Term While We Still Can" (2022-09); "The Shadowy Nature of Theonomy? A Reply to Batzig" (2022-11); "Am I a Kinist?" (2023-08); "Why I Am Not a Christian Nationalist" (2023-09). Lower priority (2024–2026): "The Institutional Church, Spirituality and Christian Nationalism" (2024-02-29); "A Political Primer on Reformed Confessions" (2024-02-05); "Thoughts on Theonomy" (2024-08-14); "A Few Clarifications and Elaborations Concerning the Christian Nationalism Controversy" (2025-08-13); "Today's 'Christian Nationalists' Were Yesterday's Sabbath-Contenders" (2026-06-17); "Principled Polytheism and the PCA" (2026-07-03); the 2016 series "Theonomy, Greg Bahnsen, and the Federal Vision" (2016-07-05 to 2016-08-28).

### 3.3 The Garris case

| Date | Title | Byline | Original | URL | Could support |
|---|---|---|---|---|---|
| 2026-06-08 | A Slippery Slope: Rio Grande Presbytery's Suspension of a Serving Pastor | Forrest L. Marion (RE, First PC Crossville) | TAR | https://theaquilareport.com/a-slippery-slope-rio-grande-presbyterys-suspension-of-a-serving-pastor/ | Opinion. It quotes "indefinitely suspend" and cites the Christian Post (2026-06-01). |
| 2026-08-31 | The Question with TE Garris's Suspension: Justice Delayed, Justice Denied? | Forrest Marion | TAR | https://theaquilareport.com/the-question-with-te-garriss-suspension-justice-delayed-justice-denied/ | Opinion. It says "Pastor Garris has appealed the presbytery's decision" to the SJC, and "because of his appeal, Pastor Garris is permitted to continue preaching." It dates the ruling "May 2026." The Garris report says that no source confirmed an appeal. This is a first source for one, but it is opinion. Confirm it from the SJC docket or the M54GA SJC report. |

### 3.4 The Appleton case

None found (see section 1).

### 3.5 Women in the military

| Date | Title | Byline | Original | URL | Could support |
|---|---|---|---|---|---|
| 2014-05-01 | A Session's Statement of Opposition to Women Serving in the Military | Staff (text from TE Charles A. Hickey) | TAR | https://theaquilareport.com/a-sessions-statement-of-opposition-to-women-serving-in-the-military/ | The statement of the Trinity PC session (Ludlow, KY). It cites *Rostker v. Goldberg* and a letter of the PRJC. A local act; probably `visibility: private` or not used. |
| 2024-12-20 | Revisiting the PCA Report: "Man's Duty to Protect Woman" | Forrest L. Marion | TAR | https://theaquilareport.com/revisiting-the-pca-report-mans-duty-to-protect-woman/ | Opinion on the 2001 majority report (`ga29-women-military-consensus`). It cites Marion's earlier TAR piece of 2016-08-14. |

Lower priority: "Top Generals: Women Should Register For the Draft" (2016-02-11); "Conscripted for Life, Not War: Why the Draft is Wrong for Women" (2016-02-20); "Women Face The Draft After Lawmaker's Protest Amendment Backfires" (2016-07-23); "Don't Force Young Women to Fight the Nation's Wars" (2021-07-27); "Should We Prepare Our Daughters to Register for the Military Draft?" (2022-01-29). None of them reports a PCA GA action. This agrees with the lead in `complementarianism-pca.md`: I found no 2016 PCA statement on women and the draft.

### 3.6 CRC and NAPARC history; NAE

| Date | Title | Byline | Original | URL | Could support |
|---|---|---|---|---|---|
| 2012-06-19 | At the PCA GA: Less than 2/3 vote to recommend an amended proposal to stay in the NAE | (not read) | TAR | https://theaquilareport.com/at-the-pca-ga-less-than-23-vote-to-recommend-an-amended-proposal-to-stay-in-the-nae/ | **(record)** GA40 vote on NAE membership. Primary record: M40GA. |
| 2022-06-28 | Presbyterian Church in America Votes to Leave National Association of Evangelicals | Emily McFarlan Miller | Religion News Service (2022-06-23) | https://theaquilareport.com/presbyterian-church-in-america-votes-to-leave-national-association-of-evangelicals/ | **(record, news)** GA49, 2022-06-22: the PCA left the NAE. This was "the third time in the past decade" that the PCA considered it. Overture 3 (Pee Dee) PDF linked. Follows `ga47-remains-in-nae`. Cite RNS. |
| 2025-06-23 | The 1995 (23rd) PCA General Assembly | David W. Hall | Reformed Politics (Substack); excerpt from Hall, *Irony and the Presbyterian Church in America* | https://theaquilareport.com/the-1995-23rd-pca-general-assembly/ | A secondary account of GA23. It calls the CRC action "the strongest action toward any NAPARC church in our history" and mentions the admission of the RCUS to NAPARC. Use it as a guide to M23GA; `ga23-crc-remove-from-naparc` already cites the minutes. |
| 2025-11-13 | Council of Reformed and Presbyterian Churches Celebrates 50 Years | Liz Lykins | WORLD (Sift) | https://theaquilareport.com/council-of-reformed-and-presbyterian-churches-celebrates-50-years/ | NAPARC at 50, with its 13 members. Links to "A Brief History of NAPARC" (naparc.org PDF, 2025-10). That PDF is a better source for the NAPARC actor and for the CRC suspension (1997–2002). |

Lower priority: "Central Carolina Overture Asks PCA GA to Withdraw Its Membership from the National Association of Evangelicals" (2011-04-29, record); "Connecting the Dots: The NAE, the PCA and BioLogos" (2012-09); "'Gender Apartheid' and 'Toxic Masculinity' in NAPARC?" parts 1–2 (2017-07-14/18); "The Christian Reformed Church Corrects Course" (2022-08-03) and "The Curious Case of the Christian Reformed Church" (2024-08-20), which are on later CRC synods.

### 3.7 Judicial cases (judicial-process issue)

| Date | Title | Byline | Original | URL | Could support |
|---|---|---|---|---|---|
| 2023-11-02 | PCA's Judicial Commission Vindicates the "Jonesboro 7," Cites Abuse by Session | Ryan Biese | Substack (rfbwcf) | https://theaquilareport.com/pcas-judicial-commission-vindicates-the-jonesboro-7-cites-abuse-by-session/ | An account of an SJC hearing (Covenant Presbytery), from court filings and observers. The author writes in support of the complainants. Primary record: the SJC decision. Follow-up: "Covenant Presbytery Apologizes, Bringing Closure to Jonesboro 7 Ordeal" (2024-06-13). |
| 2025-05-28 | PCA Leader's "Scandalizers" List Triggers Ethics Probe, Fraternal Rift | Zoe Miller | WORLD | https://theaquilareport.com/pca-leaders-scandalizers-list-triggers-ethics-probe-fraternal-rift/ | **(news)** Requests for investigation of Stated Clerk Bryan Chapell after a TGC podcast. It links to a byFaith "Statement from officers." Check the names before use (living people). |
| 2026-06-15 | Grace Presbytery Deposes and Excommunicates Minister | Andy Jones | byFaith | https://theaquilareport.com/grace-presbytery-deposes-and-excommunicates-minister/ | **(record, news)** A criminal case. It is not a doctrinal case. Probably out of scope. |
| 2026-08-04 | Complaint Against Missouri Presbytery Concerning Ordination of SSA Pastor Appealed to PCA Standing Judicial Commission | Presbyterian Plumb Line | Presbyterian Plumb Line | https://theaquilareport.com/complaint-against-missouri-presbytery-concerning-ordination-of-ssa-pastor-appealed-to-pca-standing-judicial-commission/ | **(record)** Missouri Presbytery ordained a same-sex-attracted candidate on 2025-04-22; a complaint went to the SJC. For the sexuality pass (section 5). |
| 2026-09-21 | SJC Issues Decision in TE Burk Parsons' Appeal | byFaith Staff | byFaith | https://theaquilareport.com/sjc-issues-decision-in-te-burk-parsons-appeal/ | **(record)** SJC Case 2025-15, Parsons v. Central Florida Presbytery. The decision PDF is on byFaith. |

### 3.8 Save the PCA

No new TAR item. The nearest items are "The PCA's 'Essgate'" (3.1), "Shepherdesses in the PCA?" (3.1), "PCA Threat Assessment" (Justen Ellis, PCA Polity, 2025-10-16; on worship, not on Save the PCA), and the WORLD piece on the "scandalizers" list (3.7).

## 4. Hot-button issues

**Method.** I counted titles (URL slugs) on a PCA-only base. The base is 1,639 posts: the 644 posts in the "PCA General Assembly" category, plus every post whose slug names the PCA, a presbytery, the General Assembly, the SJC, the BCO, an overture, byFaith, MTW, MNA or Covenant Seminary. I removed slugs that name another body (PCUSA, EPC, OPC, ARP, RPCNA, CRC, RCA and others) and do not also name the PCA. Each issue has a list of whole words (see `scripts/hot2.py`). A post can count for more than one issue. Treat the counts as rough lower bounds:
- Many posts on these issues do not name the PCA in the slug.
- From 2017, the slugs drop small words, so phrases like "role of women" do not match.
- 2008–2009 are left out, because those dates are poor.

| Issue | '10 | '11 | '12 | '13 | '14 | '15 | '16 | '17 | '18 | '19 | '20 | '21 | '22 | '23 | '24 | '25 | '26 | Total |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Polity: BCO amendments, AC funding, strategic plan, GA structure, SJC reform | 61 | 49 | 7 | 4 | 7 |  | 3 | 11 | 12 | 6 | 7 | 11 | 15 | 8 | 10 | 4 | 7 | 222 |
| Homosexuality, Revoice, Side B, Overtures 23/37, Missouri Presbytery/Johnson | 3 | 3 | 1 | 1 |  |  | 1 | 1 | 11 | 23 | 16 | 33 | 29 | 11 | 5 | 1 | 2 | 141 |
| Judicial cases (SJC, presbytery trials, original jurisdiction) | 11 | 15 | 2 | 10 | 3 | 1 | 2 | 1 | 1 |  | 2 | 7 | 10 | 4 | 2 | 2 | 6 | 79 |
| Women in office: deaconesses, women deacons, commissioning, shepherdesses | 16 | 8 | 4 | 1 |  | 1 | 11 | 11 | 1 | 3 |  | 1 | 3 | 2 | 1 | 3 | 4 | 70 |
| Worship and sacraments: intinction, paedocommunion, worship directory, Jesus Calling, images | 3 | 4 | 9 | 5 | 3 |  |  | 4 | 1 |  | 1 | 1 | 1 | 4 | 6 | 4 |  | 46 |
| Departures and new bodies: Vanguard, Veritas, churches leaving | 4 | 7 | 5 | 2 | 5 | 2 | 1 |  | 2 | 2 | 3 |  | 5 | 2 | 2 | 2 |  | 44 |
| Federal Vision (Leithart, Meyers, Lawrence, Wilkins) | 6 | 19 | 1 | 10 | 2 |  |  |  |  |  |  |  |  |  |  |  |  | 38 |
| Race: racial reconciliation (2016 Ov. 43), CRT, white supremacy, kinism | 3 | 3 |  |  | 1 | 8 | 10 | 1 |  | 1 | 2 | 5 |  |  |  |  |  | 34 |
| Insider movements (MTW, Bible translation) |  | 5 | 4 | 5 | 13 |  |  |  |  |  |  |  |  |  |  |  |  | 27 |
| Creation days, historical Adam, theistic evolution | 1 | 4 | 13 | 2 | 1 | 1 |  |  |  | 1 |  | 1 |  |  | 1 |  |  | 25 |
| Ecumenical: NAE, NAPARC, EPC, CREC, OPC/ARP relations | 3 | 3 | 3 | 1 | 2 | 1 |  | 1 |  | 2 |  |  | 1 |  | 1 | 1 |  | 19 |
| Abuse and child protection |  |  |  |  | 3 |  |  | 1 |  | 1 |  |  | 3 | 4 | 3 |  |  | 15 |
| Subscription and exceptions (good faith subscription) |  | 2 | 4 |  |  |  |  | 1 | 1 |  |  | 3 | 1 | 1 | 1 | 1 |  | 15 |
| Christian nationalism, theonomy, civil magistrate |  |  |  |  |  |  |  |  | 1 |  |  |  | 1 |  | 1 | 3 | 4 | 10 |
| Gender identity, transgender |  |  |  |  |  |  |  | 1 |  |  |  | 1 |  | 3 | 2 |  |  | 7 |
| (all PCA-named posts) | 233 | 186 | 125 | 102 | 86 | 57 | 56 | 64 | 54 | 73 | 60 | 105 | 105 | 97 | 60 | 64 | 56 | 1583 |

Site-wide counts (all 50,469 slugs, not only PCA) show the same peaks for two issues: race-related titles reach 64 in 2020 and 102 in 2021, and Christian nationalism and theonomy titles reach 14 a year in 2024–2026.

**Ranked list.** I ranked by the PCA counts, by how long the debate lasted, and by how many GA, SJC or presbytery records it produced. Dates are publication dates of the TAR items named.

1. **Homosexuality and ordination standards (2018–2026).** The peak is 2019–2022. Bodies: GA46–GA53; Missouri Presbytery; the SJC (complaint against Missouri Presbytery denied, 2021-10-22; *Speck v. Missouri Presbytery*, opinions 2022-02-07; new appeal 2026-08-04); the Ad Interim Committee on Human Sexuality (report 2020-05-28). Overtures: Nashville Statement (GA47, 2019-06-28); Overtures 23 and 37 (GA48; presbytery tally 2021-11-22; failed 2022-02); Overture 15 (GA49; failed 2023-02-06; final tally 2023-05-29); the 2023 items (vote update 2023-11-30). Requests for original jurisdiction over TE Greg Johnson came from Central Georgia, Savannah River, Southeast Alabama and Grace presbyteries (2020–2022). Primary records: M46GA–M51GA; the 2020 committee report; SJC decisions; the Stated Clerk's presbytery vote tallies; Missouri Presbytery's BCO 31-2 report (TAR reprint 2020-08-12).
2. **Polity and connectionalism (2010–2011, and later).** AC funding by BCO 14 amendments (defeated by the presbyteries, 2011-01-22); the 2010 Strategic Plan; the CMC; ruling elder attendance; a delegated assembly; reform of the SJC (2013–2014); BCO 34-1 (2026). Primary records: M38GA–M40GA; presbytery votes; AC and CMC reports.
3. **Federal Vision and the church courts (2007–2014).** Louisiana Presbytery admonished (GA36, 2008-06-12); Siouxlands (Moon 2010-10-29; Lawrence 2011 trial; SJC sustained a complaint 2014-06-19); Pacific Northwest (Leithart; SJC panel 2009-12-10; trial 2011; final SJC decision 2013-04-04; original jurisdiction declined 2013-11-05); Missouri (Meyers; SJC proposed decision 2011-11-30; found not guilty 2012-04). Primary records: the 2007 FV study report (confirm in the minutes); SJC decisions in M38GA–M42GA; presbytery trial records.
4. **Race and racial reconciliation (2002–2025).** The GA30 racial reconciliation action of 2002 (TAR reprint 2015-06-18); the 2015 personal resolution debate (2015-06-15); Overture 43, approved 861-123 (2016-06-24); the 2018 race report (already in the graph); Chesapeake Overture 36 on white supremacy (2021-04-22); the GA52 condemnation (already in the graph). Primary records: M30GA, M43GA, M44GA, M46GA, M48GA, M52GA.
5. **Women in office.** Already covered. TAR adds the 2008–2012 presbytery actions (section 3.1).
6. **Worship and sacraments.** Paedocommunion in RPR (2011–2012); intinction (Ohio and Savannah River 2012, Heartland 2013-11-04, BCO 58-5 amendment 2012); the GA52 worship directory committee (2025-07-30). Primary records: M39GA–M41GA RPR reports; M52GA.
7. **Departures and new bodies.** Seven Metro New York ministers to the EPC (2012-11-22); RCA churches into the PCA (2014–2015); Vanguard Presbytery (2019-12-02; first GA called 2024-10; second GA 2026-08-13); Veritas Presbytery (2024-09-12); Saint Andrew's Chapel joined and then left (2025-12-15). Primary records: presbytery minutes; the GA statistics; the new bodies' own documents.
8. **Ecumenical relations: NAE and NAPARC.** NAE: 2011 overture; 2012 vote; 2019 (in the graph); exit 2022-06-22. NAPARC: 50 years (2025). Primary records: M39GA, M40GA, M47GA, M49GA; NAPARC minutes.
9. **Insider movements (2011–2014).** GA39 Overture 9 (2011-04-05); the ad interim committee; the report endorsed (2014-07-15). Primary records: M39GA–M42GA; the committee's partial and final reports.
10. **Creation and the historical Adam (2010–2012).** A 2011 TAR piece on the PCA creation study report (2011-05-19; the report itself is from 2000); the Rocky Mountain and Savannah River overtures on Adam (2012-01/02); the GA40 seminar debate; the Waltke resignation at RTS (2010-04). Primary records: M28GA; M40GA overtures.
11. **Abuse and protections in church courts (2014–2024).** Child protection overture (2014-01-26); the ad interim committee on domestic abuse and sexual assault (check the minutes for the GA that formed it and the GA that received its report); witness, counsel and background-check overtures (2023–2024); the Jonesboro 7 case. Primary records: M42GA; the committee report; M50GA–M51GA.
12. **Christian nationalism and theonomy.** Already covered. TAR adds opinion only.
13. **Subscription and exceptions; gender identity; IVF (2026-11-05).** These are smaller and more recent.

## 5. Top 5 suggested topic passes

1. **Homosexuality, Revoice and ordination standards (2018–2026).** Scope: Revoice 2018 and the presbytery responses; the GA47 Nashville Statement vote; the Ad Interim Committee on Human Sexuality (formed 2019, report 2020, GA48 action 2021); Overtures 23 and 37 (sent down 2021, failed 2022) and Overture 15 (sent down 2022, failed 2023); the 2023 amendments that went to the presbyteries (TAR reports strong support in November 2023; confirm the GA51 enactment in the minutes); Missouri Presbytery's BCO 31-2 investigation of TE Greg Johnson; the requests for original jurisdiction; the SJC cases (including *Speck v. Missouri*, 2021–2022); and the 2025 ordination complaint now before the SJC. Why it matters: TAR has more PCA posts on this than on any doctrinal issue after 2017. It led to several proposed BCO amendments on officer qualifications, and it moved the courts, the presbyteries and the GA at the same time. The records are rich: GA minutes, the study report, vote tallies and SJC decisions. The issue also links to the existing `ordination-exceptions` and `judicial-process` issues.
2. **Federal Vision and the church courts (2006–2014).** Scope: the Federal Vision study committee and its report (2006–2007; confirm the GA numbers in the minutes); RPR and judicial actions on Louisiana Presbytery (Wilkins) and on Siouxlands (Moon, Lawrence), Pacific Northwest (Leithart) and Missouri (Meyers); the SJC decisions; and the overtures for original jurisdiction (2013). Why it matters: it was one of the largest series of doctrinal cases in 2007–2014 (38 PCA-named TAR titles). It tested how far a GA study report binds presbyteries, and how the SJC reviews a presbytery's judgment on doctrine. It is mostly a court record, so it fits the graph's citation rules well.
3. **Race and racial reconciliation (1973–2025).** Scope: the GA30 racial reconciliation action (2002); the 2015 personal resolution and its referral; Overture 43 and the GA44 confession (2016); the 2018 study report (already partly in the graph); the 2021 Chesapeake overture on white supremacy and the GA48 answer; and the link to the existing kinism and GA52 events. Why it matters: it reaches back to the founding (`rpces-heritage`, the "Southern" origin debate in several TAR history pieces). It ties the existing ethno-nationalism branch to the PCA's own acts of repentance, and it frames the Garris and Appleton cases.
4. **Abuse, church-court protections and accountability (2014–2026).** TAR has only about 15 PCA-named titles on this, but the issue has many court records. Scope: the 2014 child protection overture; the Ad Interim Committee on Domestic Abuse and Sexual Assault (check the minutes for its dates); the 2023–2024 overtures on witnesses, counsel for the accused and background checks; and the SJC cases on how courts treat members and officers (the Jonesboro 7, Parsons, Metro New York). Why it matters: it shows how the PCA changed its BCO procedure in response to cases. It gives the existing `judicial-process` issue its rule changes, not only its cases. Keep criminal cases and named private persons private, as the project rules require.
5. **Polity and connectionalism (2010–2026).** Scope: the 2010 Strategic Plan; the BCO 14 amendments to fund the Administrative Committee (sent down by GA38, defeated by the presbyteries in 2011) and the alternative funding plans; the Cooperative Ministries Committee; byFaith funding overtures (2011); ruling elder attendance and proposals for a delegated assembly; proposals to reform the SJC and the GA nominating process (2013–2014); and later changes such as BCO 34-1 (2026). Why it matters: this is the largest group of PCA-named TAR titles (222), with a sharp peak in 2010–2011. It is about how the PCA governs itself: how far the GA and its committees can bind or tax churches and presbyteries. That question lies under most other debates in this list. The records are GA minutes, presbytery votes, and AC and CMC reports.

Other passes that the records would support: ecumenical relations and realignment (the NAE votes of 2011, 2012, 2019 and 2022; NAPARC after the CRC; the CREC; Vanguard, Veritas and other new bodies; the 2026 EPC split); insider movements (2011–2014); creation and the historical Adam; and worship and sacraments (intinction, paedocommunion, the 2025 worship directory committee).
