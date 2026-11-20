# Overture texts as sources

Date: 2026-11-20

Goal: each event about an overture cites the overture's own text (its title line,
"Whereas" clauses, "be it resolved" clause or adoption line), not only the minutes'
summary or the committee's action. All quotes were checked with `tools/find.py` on
the cited printed page. `uv run -q tools/build.py --strict` passes.

## Sources added

| Id | Title | Notes |
|---|---|---|
| m156gs | Minutes of the 156th General Synod (RPCES), 1978 | https://www.pcahistory.org/rgo/rpces/minutes/RPCES_1978_Synod.pdf (11 MB). Overture N is on pp. 133-134. |

No new `o<n>-<N>ga` files were needed. The existing o14-53ga, o37-53ga, o61-53ga,
o72-53ga, o1-54ga and o2-54ga were reused.

## Overture events

"Already" = the event cited the overture's own text before this work. "Added" = new
citation(s) added in this work.

| Event | Overture | Overture text: source, page | Status |
|---|---|---|---|
| rpces-156gs-denies-local-option | Overture N, Michigan-Northern Indiana Presbytery (156th GS, 1978) | m156gs 133-134; m38ga 384 (reprint in Evangel O7 attachment); rpces-reconsideration-women-deacons (docsynod) | Added m156gs 133, 134 and m38ga 384 |
| ga17-women-not-on-ga-committees | Overture 24, Tennessee Valley (17th GA) | m17ga 183 | Added |
| ga21-adopts-louisiana-crc-overture | Overture 35, Louisiana (21st GA) | m21ga 63-64 | Already (p. 64) |
| ga22-message-to-crc-synod-1994 | none (IRC report action) | - | Not an overture event |
| ga24-concern-women-in-combat | Overture 20, Philadelphia (24th GA) | m24ga 282 | Already |
| ga25-declines-women-in-combat-overture | Overture 13, Philadelphia (25th GA) | m25ga 184-185 | Already (p. 185); added title line p. 184 |
| ga25-declines-women-role-study | Overture 15, South Coast (25th GA) | m25ga 173-174 | Already |
| ga26-forms-women-military-committee | Overture 26, Philadelphia (26th GA, 1998) | not found | M26GA (https://pcahistory.org/pca/ga/26th_pcaga_1998.pdf) is 268 MB, over the 120 MB limit. The 1998 "Significant Actions" PDFs (pcahistory.org/pca/ga/actions/26thGA_1998_Actions_LRT.pdf, _PRG.pdf) and the AISCWIM pages have no overture text. |
| rpr-cites-pp-liberti | (none; RPR action) | m36ga 205 is in Overture 9's text | No change |
| liberti-overtures-pp-women-deacons | Liberti Church overture to PP (2007/08) | not found | Overture 9 lists it as "Exhibit C", but M36GA does not print the exhibits. Searched all cached minutes for "liberti" and "Exhibit C". The event cites Overture 9's summary of it (m36ga 205-206). |
| presbyteries-overture-36ga-study | Overtures 9 (PP), 15 (Western Canada), 17 (Rocky Mountain), NCP concurrence (36th GA) | m36ga 205-206, 210-212, 214 | Already |
| oc-recommends-no-study-36ga | Overtures 9 and 19 (Central Georgia) (36th GA) | m36ga 206, 212 | Added |
| oc-minority-report-study-36ga | Overture 9 | m36ga 206 | Added |
| ga36-acts-on-study-overtures | Overture 9 | m36ga 206 | Added |
| ccc-overtures-pp-reaffirm | Crossroads overture to PP (Aug. 11, 2008) | m37ga 257-260 (printed in Overture 15) | Already (p. 257); added resolved clause p. 259 and adoption line p. 260 |
| pp-denies-ccc-overture | Crossroads overture to PP | m37ga 259 | Added |
| pp-churches-forgo-diaconate | City Church alternative overture to PP (Mar. 31, 2009) | not found in full | Only summarized in the SJC record, m42ga 529 (already cited). |
| ccc-overture-15-37ga | Overture 15, Crossroads (37th GA) | m37ga 256-257 | Already (p. 257); added title p. 256 |
| ga37-rules-overture-15-out-of-order | Overture 15 | m37ga 256 | Added |
| grace-overture-danvers | Overture 13, Grace (37th GA) | m37ga 279-282 | Already |
| ga37-declines-danvers | Overture 13, Grace | m37ga 279 | Added |
| overtures-38ga-amend-bco-9-7 | Overtures 7 (Evangel), 2 (Central Carolina), 9 (Eastern Carolina), 13 (Westminster) (38th GA) | m38ga 380-383, 386-390 | Already (pp. 383, 386); added pp. 383 (resolved), 387, 388, 390 (adoption lines) |
| ncp-overture-unordained-diaconal-38ga | Overture 10, Northern California | m38ga 394 | Already |
| tennessee-valley-overture-deaconesses-38ga | Overture 16, Tennessee Valley | m38ga 390-391 | Already |
| ga38-proposes-bco-9-7 | Overtures 7, 2, 9, 13, 16, 10 | m38ga 383, 387 | Added (Evangel resolved clause; Central Carolina text) |
| ga45-women-roles-recommendations | none (study committee report) | - | Not an overture event |
| overture-amend-bco-9-7-fails | Overture 9, Grace (46th GA) | m46ga 684-686 | Already |
| srp-overture-25-diaconate-2018 | Overture 25, Savannah River (46th GA) | m46ga 721 | Already |
| ga46-declines-women-on-boards | Overtures 13 (Nashville) and 26 (Tennessee Valley) (46th GA) | m46ga 692, 702 (O13); 722, 726 (O26) | Already for O13; added O26 pp. 722, 726 |
| bryce-avenue-overture-women-worship | Bryce Avenue session overture (50th GA) | m50ga 1002-1003 | Already |
| nwgp-overture-titles | Overture 26, Northwest Georgia (50th GA) | m50ga 1029 | Already |
| presbyteries-approve-bco-7-3 | (presbytery vote on the amendment from O26) | m50ga 1029 (cited in nwgp-overture-titles) | No change |
| lee-carr-deaconess-survey | none (article) | - | Not an overture event |
| srp-overture-34-diaconate | Overture 34, Savannah River (52nd GA) | m52ga 1270-1271 | Already |
| stp-ffo-report-published | none (website report) | - | Not an overture event |
| swfl-overture-14-titles | Overture 14, Southwest Florida (53rd GA) | o14-53ga 1-7 | Already |
| ga53-answers-overture-37 | Overture 37, Pacific (53rd GA) | o37-53ga 1, 5 | Already (p. 5); added title p. 1 |
| ga53-declares-danvers | Overture 61, Calvary (53rd GA) | o61-53ga 1, 4 | Already (p. 4); added title p. 1 |
| ga53-sends-down-bco-12-8 | Overture 72, Ascension (53rd GA) | o72-53ga 2 | Already |
| swfl-overture-1-titles | Overture 1, Southwest Florida (54th GA) | o1-54ga 1-3 | Already |
| swfl-overture-2-diaconal-titles | Overture 2, Southwest Florida (54th GA) | o2-54ga 1-4 | Already |

## Facts and discrepancies

No event fact needed a correction. Notes:

- Overture 26 from Tennessee Valley (46th GA) was adopted "at a called meeting,
  April 7, 2018" (m46ga 726). The event does not give this date, so no change.
- The original 1978 synod minutes (m156gs 133-134) read "RECONSIDERATION ON WOMEN
  DEACONS" and "affirm the prerogative" (singular). The docsynod transcription
  (rpces-reconsideration-women-deacons) and the M38GA reprint read "RECONSIDERATION
  OF" and "prerogatives". The existing event quote matches the docsynod text, so it
  still verifies.
- m17ga 129 refers to "Overture 4" in the Bills and Overtures action that went to
  the Judicial Business Committee. Pages 38, 176 and 183 show that this is
  Overture 24 from Tennessee Valley. The event body gives no overture number.
- Central Georgia's Overture 19 (36th GA) has the title "Decline to Elect Study
  Committee on Deaconesses" on m36ga 212; the recommendation on the same page says
  "Decline to Erect".
- Evangel Presbytery's Overture 7 (38th GA) has no adoption line in M38GA, so its
  adoption date is not known from the minutes.

## Update 2026-11-20

Overture 26 (1998) found: M26GA (268 MB scan, downloaded by streaming to disk). The overture text begins on p. 210; the Assembly's action on 1998-07-02 is on p. 209 (Bills and Overtures Committee recommended the negative; the Assembly adopted a substitute in the affirmative). Cited in `ga26-forms-women-military-committee`. Now 28 of 30 overture events cite the overture text.
