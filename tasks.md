# Tasks: Urban Air Quality Assistant

Legend: ✅ done · ⬜ future

## Phase 1: Planning
- ✅ T1. Define problem, users, and goals (see `requirements.md`)
- ✅ T2. List functional and non-functional requirements
- ✅ T3. Choose a single-file, zero-dependency architecture (avoids preview/iframe failures)

## Phase 2: Design
- ✅ T4. Define the six AQI categories, colours, and messages as data
- ✅ T5. Write category-based and audience-based advice
- ✅ T6. Design a responsive layout with light and dark themes

## Phase 3: Build (`index.html`)
- ✅ T7. Semantic page structure with landmarks, skip link, and section navigation
- ✅ T8. AQI input with validation and accessible error handling
- ✅ T9. Category result card with colour, description, and gauge marker
- ✅ T10. Audience selector that adapts advice
- ✅ T11. History (last 10) with table and bar chart using safe `localStorage`
- ✅ T12. Clear-history and sample-value buttons
- ✅ T13. AQI scale table and everyday tips
- ✅ T14. About section and health disclaimer

## Phase 4: Quality
- ✅ T15. Accessibility pass (labels, ARIA live, focus, contrast, reduced motion)
- ✅ T16. Security pass (`textContent` only, input limits, no external calls)
- ✅ T17. Responsive pass (320px to desktop)
- ✅ T18. Code cleanup (strict mode, data-driven logic, comments)

## Phase 5: Test Checklist
| # | Input / Action | Expected |
|---|----------------|----------|
| 1 | 42 | Good |
| 2 | 87 | Moderate |
| 3 | 135 | Unhealthy for Sensitive Groups |
| 4 | 178 | Unhealthy |
| 5 | 245 | Very Unhealthy |
| 6 | 340 | Hazardous |
| 7 | 0 and 500 | Good and Hazardous (boundaries) |
| 8 | -5, 600, 12.5, blank | Error shown, no result |
| 9 | 135 + Children | Child-specific tip added at top |
| 10 | 40 + Children | No extra tip (risk too low) |
| 11 | 11 checks in a row | History keeps only latest 10 |
| 12 | Clear history | Table and chart hidden |
| 13 | Tab key only | All controls reachable, focus visible |
| 14 | Browser storage blocked | App still works |
| 15 | Phone width (320px) | No horizontal page scroll |

## Phase 6: Release
- ✅ T19. Write `readme.md` with run and deploy steps
- ⬜ T20. Create public GitHub repo `Urban-Air-Quality-Assistant` and upload 4 files
- ⬜ T21. Enable GitHub Pages (Settings → Pages → main / root)
- ⬜ T22. Open the live link and run the test checklist
- ⬜ T23. Add 2-3 screenshots and the live link to `readme.md`
- ⬜ T24. Share the link with Hack2skill

## Phase 7: Future Enhancements
- ⬜ Live AQI data from public APIs
- ⬜ City search and map view
- ⬜ Multilingual support (Telugu, Hindi, English)
- ⬜ PWA install and offline caching
- ⬜ Pollution alert notifications
