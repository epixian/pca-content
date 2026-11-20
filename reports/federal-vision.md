# Federal Vision and the church courts: research pass

Written 2026-11-20. All new events have `status: draft` and `visibility: public`. The last `tools/build.py --strict` run (under the shared build lock) passed with no errors and no warnings. Every event in this pass rests on the General Assembly minutes (M33GA–M46GA). I made no new sources, fetched nothing, and changed nothing in the cache.

## Scope

This pass covers how the PCA dealt with the Federal Vision (FV), Auburn Avenue theology (AAT) and the New Perspective on Paul (NPP) from 2005 to 2017:

- **The Assembly's study.** Mississippi Valley's report (2005), the four overtures and the ad interim committee (2006), and the nine declarations and the 35th General Assembly's action (2007).
- **Louisiana Presbytery and TE Steve Wilkins (2005–2008).** The exoneration, the Central Carolina memorial, the Suncoast Florida overture, the Standing Judicial Commission (SJC) decisions, the guilty plea, the departure of Auburn Avenue to the CREC, and the admonition.
- **Pacific Northwest Presbytery and TE Peter Leithart (2007–2014).** The study committee, Case 2009-6, the 2011 trial and acquittal, Case 2012-05, the overtures for a rehearing and for original jurisdiction, and the SJC answer.
- **Siouxlands Presbytery and TEs Greg Lawrence and Joshua Moon (2007–2017).** The 2007 affirmations, Case 2008-14, the investigations, Case 2010-04 (Moon), the 2011 trial, Case 2012-08 (new trial), the 2015 retrial and Case 2016-16.
- **Missouri Presbytery and TE Jeffrey Meyers (2006–2013).** The 2006 report, the 2010 letter of concern, Case 2011-06, the 2012 trial and Case 2012-09.
- **Rules on higher-court review.** BCO 34-1 original jurisdiction, BCO 40-5, the SJC manual section on memorials, and BCO 43-10, where the minutes tie a change or a proposal to these cases.

The scope runs to 2017, beyond the planned end of about 2014, because the Lawrence case ended only with the SJC decision of October 19, 2017 (see "Decisions for the user").

## Issue tree (new)

- `federal-vision` (root): Federal Vision and the New Perspective on Paul. 42 of the 43 events have this issue. The exception is `ga37-amends-sjc-memorial-procedure`, because its overture does not name the Louisiana case.
- `original-jurisdiction`: original jurisdiction and higher-court review of presbyteries. Its parent is `judicial-process` only. The homosexuality/Revoice pass already uses it for five of its own events on the requests for original jurisdiction over TE Greg Johnson, so I did not put it under `federal-vision`.

I also put the existing `judicial-process` issue on 32 of the new events. I did not edit any existing event.

## Timeline

Kinds of evidence: **record** means what a body did, as the minutes show. **Court** means an SJC decision or a presbytery trial as the SJC decision summarizes it. **Position** means a statement the Assembly adopted. **Study** means a committee report. **Overture** means a request from a presbytery.

| Date | What happened | Event | Source | Evidence |
|---|---|---|---|---|
| 2005-06 | 33rd GA answers Mississippi Valley's Overture 14 (distribute its NPP/FV report) "in the negative without prejudice" | `ga33-declines-npp-report-distribution` | M33GA pp. 203–204 | record |
| 2005-07 | Louisiana Presbytery declares TE Wilkins "faithful to the Confessional standards" | `louisiana-exonerates-wilkins` | M34GA p. 310; M36GA pp. 79, 82 | record (as later recited) |
| 2006-01-18 | Missouri Presbytery adopts its FV study report | `missouri-adopts-fv-report` | M41GA p. 552; M34GA pp. 210, 213 | record |
| 2006-01-28 | Central Carolina memorial on TE Wilkins and Louisiana Presbytery | `central-carolina-memorial-wilkins` | M36GA pp. 75–80 | record |
| 2006-04-04 | Suncoast Florida Overture 22: declare the Auburn Avenue session heterodox | `suncoast-overture-auburn-avenue` | M34GA pp. 83, 310 | overture |
| 2006-06-22 | 34th GA erects the ad interim committee (minority report on Overture 2 adopted) | `ga34-erects-fv-study-committee` | M34GA pp. 12, 190, 197, 210, 227–231; M35GA p. 509 | record |
| 2006-10-20 | SJC (Case 2006-02, Part I) directs Louisiana Presbytery to examine TE Wilkins; 17 concur | `sjc-directs-louisiana-reexamine-wilkins` | M36GA pp. 80–83 | court |
| 2007-01-20 | Louisiana Presbytery finds no strong presumption of guilt (13-8) | `louisiana-finds-no-presumption-wilkins` | M36GA pp. 87–89 | court (facts) |
| 2007-01-27 | Siouxlands adopts affirmations and denials on NPP and FV | `siouxlands-adopts-fv-affirmations` | M38GA pp. 135–136; M43GA p. 528 | record |
| 2007-06-13 | Study committee reports nine declarations | `fv-committee-nine-declarations` | M35GA pp. 509, 515, 566–567 | study |
| 2007-06-13 | 35th GA recommends the declarations "as a faithful exposition of the Westminster Standards" | `ga35-recommends-fv-declarations` | M35GA pp. 65, 68–69 | position |
| 2007-06-30 | Good Shepherd session (Minnetonka) protests the GA35 action | `good-shepherd-protests-ga35-fv-action` | M36GA pp. 51, 285 | record (communication) |
| 2007-10-19 | SJC Case 2007-8 sustains the Jones complaint (22-0) | `sjc-sustains-jones-complaint-wilkins` | M36GA pp. 117–118, 125 | court |
| 2007-10-19 | SJC Case 2006-02, Part II cites Louisiana Presbytery for trial (Case 2007-14) | `sjc-cites-louisiana-for-trial` | M36GA pp. 90–92 | court |
| 2008-01-19 | Louisiana Presbytery pleads guilty to Specification 2 (9-6-4) | `louisiana-pleads-guilty` | M36GA pp. 129–130 | court (facts) |
| 2008-01-27 | Auburn Avenue and TE Wilkins leave the PCA for the CREC | `auburn-avenue-leaves-pca` | M36GA pp. 130–131 | court (facts) |
| 2008-03-06/07 | SJC Case 2007-14: Specification 1 dismissed; admonition imposed (16-1) | `sjc-admonishes-louisiana` | M36GA pp. 73, 131–135 | court |
| 2006-06/2008-06-11 | SJC answers Overture 22 as "out of accord with the BCO" | `sjc-answers-suncoast-overture` | M36GA p. 140 | court |
| 2008-06-11 | 36th GA: the Moderator reads the admonition to Louisiana Presbytery | `ga36-admonition-louisiana-read` | M36GA pp. 62, 74, 136 | record |
| 2008-10-02/03 | Pacific Northwest finds TE Leithart's views not out of accord | `pacific-northwest-clears-leithart` | M38GA pp. 210–211 | court (facts) |
| 2009-06-17 | 37th GA rewrites SJC manual §16 (memorials); answers SE Louisiana Overture 7 | `ga37-amends-sjc-memorial-procedure` | M37GA pp. 76, 130, 200, 205; M36GA p. 85 | record |
| 2009-06-18 | 37th GA declines Central Carolina's BCO 34-1 amendment | `ga37-declines-original-jurisdiction-amendment` | M37GA pp. 213, 262–263, 266 | record |
| 2009-09 | Siouxlands rejects its committee's finding against TE Lawrence | `siouxlands-finds-no-presumption-lawrence` | M39GA pp. 578–579; M43GA p. 529 | court (facts) |
| 2009-10 | SJC Case 2008-14 orders a BCO 31-2 investigation of TE Lawrence (22-1) | `sjc-orders-lawrence-investigation` | M38GA pp. 136–144; M43GA p. 529 | court |
| 2009-10-15/2010-03-05 | SJC Case 2009-6 sustains the Bordwine complaint on TE Leithart (17-2) | `sjc-sustains-complaint-on-leithart` | M38GA pp. 128, 211–213 | court |
| 2010-06-29/2011-03 | SJC Case 2010-04 denies the complaint on TE Moon (19-1) | `sjc-denies-complaint-on-moon` | M39GA pp. 527, 579–583 | court |
| 2010-09-23/24 | Siouxlands finds a strong presumption of guilt against TE Lawrence | `siouxlands-indicts-lawrence` | M43GA pp. 530–531 | court (facts) |
| 2011-01-08 | Missouri Presbytery finds no strong presumption against TE Meyers | `missouri-declines-to-indict-meyers` | M41GA p. 553 | court (facts) |
| 2011-09-22 | Siouxlands acquits TE Lawrence (judicial commission 6-0; presbytery 24-6) | `siouxlands-acquits-lawrence` | M43GA pp. 532–533 | court (facts) |
| 2011-10-07 | Pacific Northwest acquits TE Leithart on five charges | `pacific-northwest-acquits-leithart` | M41GA pp. 583–585; M42GA p. 584 | court (facts) |
| 2012-04-13/14 | Missouri Presbytery tries TE Meyers | `missouri-tries-meyers` | M41GA pp. 494, 496, 554, 871 | court (facts); verdict only in a minority report |
| 2012-06-19 | SJC Case 2011-06: Missouri erred, but the complaint is moot (14-1) | `sjc-meyers-complaint-moot` | M41GA pp. 78, 551, 554 | court |
| 2013-03-06 | SJC Case 2012-09 (Bennett v. Missouri) administratively out of order | `sjc-bennett-complaint-out-of-order` | M41GA pp. 551, 870 | court |
| 2013-03-06/07 | SJC Case 2012-05 denies the complaint against the Leithart acquittal (15-2) | `sjc-upholds-leithart-acquittal` | M41GA pp. 585, 588–589, 591, 863 | court |
| 2013-04-25/05-07 | Gulf Coast, Calvary and Mississippi Valley ask for original jurisdiction over TE Leithart | `presbyteries-seek-original-jurisdiction-leithart` | M41GA pp. 76, 863–870 | overture |
| 2013-06-19/20 | 41st GA rules the records minority reports on the Leithart and Meyers trials out of order | `ga41-rpr-minority-reports-out-of-order` | M41GA pp. 22, 24, 497 | record |
| 2013-06-20 | 41st GA rules Overtures 19 and 23 (rehear SJC cases) out of order | `ga41-rules-sjc-rehearing-overtures-out-of-order` | M41GA pp. 36, 40–41, 69, 72 | record |
| 2013-06-20 | 41st GA adopts PNW Overture 15 (BCO 43-10) and declines Overture 16 (BCO 34-1) | `ga41-pacific-northwest-judicial-overtures` | M41GA pp. 50, 68, 848–849; M40GA p. 74 | record |
| 2013-10-17/2014-03-07 | SJC answers Overtures 20–22 in the negative (15-1-1) | `sjc-declines-original-jurisdiction-leithart` | M42GA pp. 499, 581–583 | court |
| 2014-06-17 | SJC Case 2012-08 orders a new trial of TE Lawrence (18-1) | `sjc-orders-lawrence-retrial` | M43GA pp. 528, 533–534, 538 | court |
| 2014-06-18 | 42nd GA enacts the BCO 43-10 amendment | `ga42-enacts-bco-43-10-reference-rule` | M42GA pp. 17, 94 | record |
| 2015-09-25 | Siouxlands retries TE Lawrence and finds him not guilty | `siouxlands-retrial-acquits-lawrence` | M46GA pp. 544–545 | court (facts) |
| 2017-10-19 | SJC Case 2016-16 denies the complaint against the second acquittal (22-1, my count of the roll) | `sjc-denies-complaint-lawrence-retrial` | M46GA pp. 536, 546–547 | court |

43 events in all.

## Record vs opinion

**Record and court.** All events rest on the GA minutes. The presbytery acts (Louisiana, Siouxlands, Pacific Northwest, Missouri) come from the "Summary of the Facts" in SJC decisions or from overtures, because no presbytery minutes are sources. The event text says so where it matters.

**Position.** Only one event is a position: the GA35 action. The Assembly "recommend[ed] the declarations in this report as a faithful exposition of the Westminster Standards" and "commend[ed]" the report "for careful consideration and study." It did not amend the Constitution, and it did not itself declare any person's views out of accord.

**Study.** The committee report and its nine declarations (`fv-committee-nine-declarations`).

**Opinion.** This pass has no opinion sources. The only voices that argue against the Assembly's line are the Good Shepherd session's protest (a record of a session's act) and the arguments in presbytery overtures. The other side appears through the SJC opinions and the overtures. See the balance note under "Decisions for the user".

### Points where the record and later accounts differ

These are noted, not resolved:

1. **The date and place of the GA35 action.** The journal puts 35-20 in the Wednesday afternoon session of June 13, 2007 (M35GA pp. 65, 68), and the Good Shepherd protest says "June 13, 2007". Later SJC summaries give "06-14-07" (M38GA p. 208; M46GA p. 537). M46GA p. 537 calls it "the 2007 Chattanooga GA", and M43GA p. 528 says Memphis. The `ga35` meeting event says Memphis. The events follow the journal.
2. **"Officially opposed."** The minority reports at GA41 say the Assembly "has officially opposed the Federal Vision, declaring it to be out of accord with our Standards" (M41GA pp. 72, 77). The GA35 action recommended the declarations as a faithful exposition. It did not use these words. The SJC decisions in the Leithart, Moon and Lawrence cases all decided on the record of the case and said that they did not judge the man's views in general.
3. **The Central Carolina memorial date.** The SJC summary says January 26, 2006 (M36GA p. 75). The attestation says January 28, 2006 (p. 80). The event uses the attestation and gives both.
4. **The 2009 Siouxlands vote on TE Lawrence.** Case 2010-04 gives "20 to 13 with one abstention" (M39GA p. 579). Case 2012-08 gives "20-17 (with one abstaining)" (M43GA p. 529), and Case 2016-16 repeats 20-17 (M46GA p. 539). The event gives both.
5. **The September 2008 Siouxlands vote on the White complaint.** Case 2008-14 gives "12 yeas, 18 nay" (M38GA p. 136). Case 2012-08 gives "18-12" (M43GA p. 529). These agree in substance. I quote neither.
6. **The Leithart acquittal margin.** The Overtures Committee's grounds at GA41 say the SJC upheld the acquittal "by an 88% majority" (M41GA p. 71). The roll call was 15 concurring and 2 dissenting (M41GA p. 589), which is 88% of those voting. These agree.
7. **The GA42 session heading.** M42GA p. 16 prints "Second Session - Wednesday Morning June 18, 2013" and p. 31 prints "June 20, 2013". These are misprints for 2014. The BCO 43-10 event uses 2014-06-18 and quotes neither heading.
8. **The SJC meeting dates in M39GA.** The report to GA39 says the commission met on June 29, 2010, October 21, 2010, and "March 3, 2010" (M39GA p. 527). The last date is probably a misprint for 2011. The Moon event uses the span 2010-06-29/2011-03.
9. **The length of the Leithart trial.** Case 2012-05 calls it "A two day, 15-hour trial" (M41GA p. 583). The Overtures Committee's grounds at GA41 speak of "an 18-hour trial" (M41GA p. 71). M42GA p. 584 gives June 3–4, 2011. The event says only "June 3–4".
10. **The struck text in Overture 2 (M34GA p. 230).** The extracted text runs the struck words and the added words together. The `ga34-erects-fv-study-committee` event quotes only the bullet instruction at the bottom of the page and Fowler's quotation of the adopted mandate (M35GA p. 509).

## Gaps and open questions

- **Decision dates the minutes do not print.** These have spans bounded by the SJC meeting dates: Case 2009-6 (Bordwine), Case 2010-04 (Moon), Case 2007-14 (March 6–7, 2008), and the answer to Overtures 20–22. The answer to Suncoast Florida's Overture 22 has the span June 2006 to June 11, 2008. Its words "not one elder in the presbytery filed a complaint" suggest a date before February 15, 2007, when TE Jones complained. That is an inference, so the event keeps the wide span. The Case 2008-14 date is "October, 2009" from a later decision (M43GA p. 529). The Case 2012-05 span uses the hearing date (March 6, 2013) and the date of the proposed decision (March 7, 2013, M41GA p. 863). The survey's dates are publication dates of Aquila Report posts, so I did not use them.
- **The Meyers verdict.** The minutes say only that Missouri Presbytery "conducted a trial" (M41GA p. 554). The not-guilty result appears only in the records minority report (M41GA p. 496) and indirectly in Overture 23. The event says this. The RPR recommendation that the Assembly adopted approved the Missouri minutes of April 13–14 and July 17, 2012 without exception (M41GA p. 447), but it does not state the verdict.
- **Where the ministers went.** The record shows that TE Wilkins and Auburn Avenue joined the CREC (2008). I found no record of a later move by TE Leithart, TE Meyers or TE Lawrence, and the events assert none.
- **Louisiana Presbytery dissolved.** An editor's note in M41GA p. 487 says Louisiana Presbytery "has been dissolved." I did not find when or why, and I wrote no event.
- **Records review.** I searched the RPR recommendations for Louisiana, Siouxlands, Pacific Northwest and Missouri in M36GA–M42GA. I searched for "31-2", "Federal", "judicial", the ministers' names, "vitals", "hostile" and "out of accord". I then opened the hits. They show only routine exceptions and the paedocommunion exceptions below. None is about Federal Vision. For example, GA38 approved the Siouxlands minutes of September 24–25 and October 20, 2009 without exception (M38GA p. 112). RPR exceptions on paedocommunion exceptions in Pacific Northwest (M39GA p. 474; M40GA p. 458; M41GA pp. 487–493) are near this topic, but I left them out. At GA41 the 458-481 vote on Recommendation 54 was about a paedocommunion exception, not about TE Leithart.
- **Presbytery records.** No presbytery minutes or reports are sources: not the Mississippi Valley report (2005), the Louisiana ad hoc committee report (2005), the Missouri report (2006), the Siouxlands report (2007) or the Pacific Northwest study committee reports (2008). The text of the Missouri report is in M34GA pp. 210–226 (Overture 26), and the Mississippi Valley report is in M33GA pp. 204 ff. Neither is cited beyond the overture.
- **Archived SJC PDFs.** cache/archive has the separate decisions for Cases 2006-02, 2007-08, 2007-14, 2008-14, 2009-06, 2010-04 and 2012-05. I compared some of them with the minutes text and used only the minutes, so they are not sources. The archive also has Case 2016-16 (`2016-16_Sartorius_v_Siouxlands.pdf`), which I did not open. No archived decision exists for Cases 2011-06, 2012-08 or 2012-09.
- **Other bodies.** The OPC Communication 2 to GA33 (its justification report, M33GA p. 54) and the RCUS Communication 1 to GA34 (M34GA p. 60) are in the minutes. I wrote no events for them. The 2007 "Joint Federal Vision Profession", which several ministers signed, is named in M41GA pp. 72, 77, 552. It is not a source.
- **The SJC manual change (2009).** Southeast Louisiana's Overture 7 does not name the Louisiana case in the text I read (M37GA pp. 205–207). The link between that overture and the Wilkins case is my inference, so the event has no `federal-vision` issue and no `responds_to`.
- **Vote counts.** The "22-1" for Case 2016-16 is my count of the roll call (M46GA p. 547). The other vote counts are printed in the minutes.
- **2002–2004.** I found nothing on the topic in M30GA–M32GA. Case 2002-16 (Delhi v. Louisiana, M32GA pp. 78–83) involves Auburn Avenue, but it concerns a dispute between members and the League of the South. It names a private family, and I left it out.

## Suggested follow-ups

1. Add the Missouri Presbytery minutes of April 13–14, 2012, or another record of the Meyers verdict, and replace the minority-report citation.
2. Look for SJC minutes or the archived decisions to date Cases 2009-6 and 2010-04 and the answer to Overtures 20–22.
3. Find the date of and reason for the dissolution of Louisiana Presbytery (M40GA–M41GA RPR or the Stated Clerk's reports).
4. Consider one event each for the Mississippi Valley (2005) and Louisiana (2005) presbytery reports, with the presbytery documents as sources.
5. Consider a short follow-on pass on paedocommunion exceptions in RPR (2010–2014). It is the nearest unrecorded topic.
6. If wanted, add a few opinion sources from both sides (for example published responses by the ministers involved, or reviews of the 2007 report) as `kind: opinion`, so that the responses are not only from presbyteries.
