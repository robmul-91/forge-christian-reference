

## Reading Companion Days 106–130 (Nov 1, 2026)
<!-- === SECTION: Companion weeks 16-19 (Days 106-130) === -->
- The 📘 Companion now appears on Days 1–130 (through 2 Samuel 16, with 1 Chronicles 1–20 and the Psalms placed in the plan), approved by Robert as drafted (`notes/companion_days106_130_draft.md`).
- Memory verses (KJV, from `data/kjv.json`): week 16 Psalm 142:5 (Days 106–112, review on Day 112), week 17 Psalm 19:14 (Days 113–119, review on Day 119), week 18 Psalm 100:4 (Days 120–126, review on Day 126), week 19 Psalm 51:10 (Days 127–133, review on Day 133, still to be written).
- Source: `notes/companion_src/days106_130.py` (WEEK16–19, DAYS, SOURCES9), merged by `companion_gen.py`. Test: `node verify_companion.js` (Days 1–130, Day 131 absent). Backups: `*.bak_pre_companion106130_20261101`.

## Reading Companion Days 91–105 (Nov 1, 2026)
<!-- === SECTION: Companion weeks 13-15 (Days 91-105) === -->
- The 📘 Companion now appears on Days 1–105 (Genesis 1 – 1 Samuel 21, with Ruth and Psalms 1, 2, 23, 34, 56, 59), approved by Robert as drafted (`notes/companion_days91_105_draft.md`).
- Memory verses (KJV, from `data/kjv.json`): week 13 Joshua 24:15 (review on Day 91), week 14 Ruth 1:16 (Days 92–98, review on Day 98), week 15 1 Samuel 16:7 (Days 99–105, review on Day 105).
- Source: `notes/companion_src/days91_105.py` (WEEK13_REVIEW, WEEK14–15, DAYS, SOURCES8), merged by `companion_gen.py`. Test: `node verify_companion.js` (Days 1–105). Backups: `*.bak_pre_companion91105_20261101`.

## My Journey to Faith: Graduate School paragraph (Nov 2, 2026)
<!-- === SECTION: Journey graduate-school paragraph === -->
Approved by Robert: a new last paragraph in the "Graduate School & the Limits of Science" section of My Journey to Faith (Home → #home/journey-science), added verbatim in `apologetics_content.js` (APO_DATA.journey, section `science`) and in `notes/my_journey_to_faith.md`. `verify_apologetics.js` checks that it is present verbatim, is the section's last paragraph and appears once. Backups: `*.bak_pre_journeygrad_20261102`.

## Map: Powers legend collapse and scroll (Nov 2, 2026)
<!-- === SECTION: Powers legend collapse/scroll === -->
Approved by Robert. On phones and tablets the Map tab's inset "Powers" legend covered up to half the map, its toggles were cut off, and its header could not be reached with the keyboard. Changes in `template.html`:
- The header is now a real button, `#legend-tg` (with `aria-expanded` and `aria-controls="legend-body"`). Enter or Space toggles the legend, and Escape inside an open legend collapses it.
- The power toggles, the tribal-territory toggle (`drawOverlay`) and the boundary note sit in `#legend-body`, which scrolls under the pinned header.
- Collapsed, the legend shrinks to a small "Powers ▸" pill (about 90×46).
- Size limits: at most 260px wide up to 900px screens, max-height min(60%, 50vh) on small screens and 45% on iPad portrait.
- The state is saved in localStorage as `forge.legendCollapsed` and reapplied after every `drawEra` rebuild. With nothing saved, small screens start collapsed.
- Toggling re-places the labels (`scheduleLabels`) and refits the map if you haven't zoomed (`refit`). Forge Dark Mode has matching rules (dark pill, focus ring, note colour).

Test: `node verify_mobile.js` checks the new section at 390 and 768 wide (every toggle reachable, pinned header, pill size, aria, keyboard, persistence, dark mode). Screenshots: `/workspace/shots_legend/*_legend_after_*`. Backups: `*.bak_pre_legendfix_20261102`.

## Reading Companion Days 321–365: the companion is now complete (Days 1–365)
<!-- === SECTION: Companion weeks 47-52 (Days 321-365); companion complete === -->
Added Nov 2, 2026 from `notes/companion_src/days321_365.py`, approved by Robert as drafted (`notes/companion_days321_365_draft.md`): companion notes for Days 321–365 (Acts 13–28, Paul's letters, Hebrews, the general letters and Revelation). **The 📘 Companion now covers every day of the 365-day plan (Days 1–365); there is no Day 366.** Week 46's review (James 1:22) shows on Day 322. New memory verses: week 47 Galatians 2:20 (Days 323–329), week 48 2 Corinthians 5:17 (Days 330–336), week 49 Romans 8:28 (Days 337–343), week 50 Ephesians 2:8–9 (Days 344–350), week 51 2 Timothy 3:16–17 (Days 351–357), week 52 Revelation 21:4 (Days 358–365, eight days so the plan's last day carries the review and a whole-year look back). Reviews on Days 329, 336, 343, 350, 357 and 365. Sources are in SOURCES15. **Sardis place added (approved by Robert):** Sardis (Rev 1:11; 3:1–6; Sart, Manisa Province, Turkey, 38.488 N, 28.040 E, confirmed against Wikipedia, BIAA and UNESCO) was already in the gazetteer (`gen_general.py`), but it shares a map point with Lud (Gen 10, 'Lydia?'), so `gen_places.py` used to merge its events into the `lud` place. A new `=== SECTION: points kept as their own place ===` in `gen_places.py` keeps Sardis separate, so `places.json` has 551 places, including `#places/sardis` (secure, Asia Minor, like the other six churches). Day 361 now lists all seven churches on the map. Extra backups: `gen_places.py` and `places.json` (`*.bak_pre_companion321365_20261102`). `verify_companion.js` now checks all Days 1–365 (and no Day 366), weeks 1–52, the Day 322 review, and the new reviews and memory boxes. Backups: `*.bak_pre_companion321365_20261102`.

## Reading Companion Days 281–320
<!-- === SECTION: Companion weeks 41-46 (Days 281-320) === -->
Added Nov 2, 2026 from `notes/companion_src/days281_320.py`, approved by Robert as drafted except one sentence removed from Day 311 (`notes/companion_days281_320_draft.md`): companion notes for Days 281–320 (the Gospels from the Sermon on the Mount through the passion and resurrection, John 21, Acts 1–12 and James). New memory verses: week 41 Matthew 6:33 (Days 281–287), week 42 John 6:35 (Days 288–294), week 43 John 11:25 (Days 295–301), week 44 John 14:6 (Days 302–308), week 45 Acts 1:8 (Days 309–315), week 46 James 1:22 (Days 316–322; review on Day 322, still to be written). Reviews on Days 287, 294, 301, 308 and 315. Sources are in SOURCES14. `verify_companion.js` now checks Days 1–320 (Day 321 has no companion), weeks 41–46, and the reviews and memory boxes. Backups: `*.bak_pre_companion281320_20261102`.

## Reading Companion Days 241–280
<!-- === SECTION: Companion week 35 review, weeks 36-40 (Days 241-280) === -->
Added Nov 2, 2026 from `notes/companion_src/days241_280.py`, approved by Robert as drafted (`notes/companion_days241_280_draft.md`): companion notes for Days 241–280 (Ezekiel 33–48, Daniel 3–12, Ezra, Haggai, Zechariah, Esther, Nehemiah, Psalms 85, 107, 111–134, 146–150 and 119, Malachi, then Matthew 1–12, Mark 1–2, Luke 1–6 and John 1–5). Week 35's review (Ezekiel 36:26) shows on Day 245. New memory verses: week 36 Psalm 121:1–2 (Days 246–252), week 37 Zechariah 4:6, the full verse (Days 253–259), week 38 Psalm 119:105 (Days 260–266), week 39 John 1:14 (Days 267–273), week 40 John 3:16 (Days 274–280). Reviews on Days 252, 259, 266, 273 and 280. Sources are in SOURCES13. `verify_companion.js` now checks Days 1–280 (Day 281 has no companion), weeks 36–40, and the reviews and memory boxes. Backups: `*.bak_pre_companion241280_20261102`.

## Reading Companion Days 201–240
<!-- === SECTION: Companion week 29 review, weeks 30-35 (Days 201-240) === -->
Added Nov 1, 2026 from `notes/companion_src/days201_240.py`, approved by Robert as drafted (`notes/companion_days201_240_draft.md` in forge): companion notes for Days 201–240 (Isaiah 46–66, 2 Kings 21–25, 2 Chronicles 33–36, Nahum, Zephaniah, Habakkuk, Jeremiah, Daniel 1–2, Ezekiel 1–32, Lamentations, Psalms 74, 79, 94, 102, 137, 44, Obadiah). Week 29's review (Isaiah 40:31) shows on Day 203. New memory verses: week 30 Zephaniah 3:17 (Days 204–210), week 31 Habakkuk 3:17–18 (Days 211–217), week 32 Jeremiah 29:13 (Days 218–224), week 33 Jeremiah 31:33 (Days 225–231), week 34 Lamentations 3:22–23 (Days 232–238), week 35 Ezekiel 36:26 (Days 239–245; review on Day 245, still to be written). Reviews on Days 210, 217, 224, 231 and 238. Sources are in SOURCES12. `verify_companion.js` now checks Days 1–240 (Day 241 has no companion), weeks 30–35, and the reviews and memory boxes. Backups: `*.bak_pre_companion201240_20261101`.

## Reading Companion Days 161–200
<!-- === SECTION: Companion week 23 review, weeks 24-29 (Days 161-200) === -->
Added Nov 1, 2026 from `notes/companion_src/days161_200.py`, approved by Robert as drafted (`notes/companion_days161_200_draft.md` in forge): companion notes for Days 161–200 (Psalms, 1 Kings 9 – 2 Kings 20, 2 Chronicles 8–32, Ecclesiastes, Joel, Jonah, Amos, Hosea, Micah, Isaiah 1–45). Week 23's review (2 Chronicles 7:14) shows on Day 161. New memory verses: week 24 Ecclesiastes 12:13 (Days 162–168), week 25 1 Kings 18:21 (Days 169–175), week 26 Joel 2:13 (Days 176–182), week 27 Micah 6:8 (Days 183–189), week 28 Isaiah 26:3 (Days 190–196), week 29 Isaiah 40:31 (Days 197–203; review on Day 203, still to be written). Reviews on Days 168, 175, 182, 189 and 196. Sources are in SOURCES11. `verify_companion.js` now checks Days 1–200 (Day 201 has no companion), weeks 24–29, and the reviews and memory boxes. Backups: `*.bak_pre_companion161200_20261101`.

## Reading Companion Days 131–160
<!-- === SECTION: Companion weeks 19 review, 20-23 (Days 131-160) === -->
Added Nov 1, 2026 from `notes/companion_src/days131_160.py`: companion notes for Days 131–160 (2 Samuel 17–24, 1 Chronicles 21–29, many Psalms, 1 Kings 1–8, 2 Chronicles 1–7, Song of Songs, Proverbs). Week 19's review (Psalm 51:10) shows on Day 133. New memory verses: week 20 Psalm 18:2 (Days 134–140, review Day 140), week 21 Psalm 139:23–24 (Days 141–147, review Day 147), week 22 Proverbs 3:5–6 (Days 148–154, review Day 154), week 23 2 Chronicles 7:14 (Days 155–161; review on Day 161, still to be written). Sources are in SOURCES10. `verify_companion.js` now checks Days 1–160 (Day 161 has no companion), weeks 20–23, and the reviews and memory boxes.
