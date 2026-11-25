# Requirements: Urban Air Quality Assistant

## 1. Problem Statement
Urban residents often see an AQI number without knowing what it means for them. They need a fast, clear, trustworthy way to turn an AQI reading into a category and practical health actions, especially for children, older adults, and people with respiratory or heart conditions.

## 2. Goals
- Convert any AQI value (0-500) into a standard category in under one second.
- Give actionable, group-specific health advice.
- Work offline, on any device, with no sign-up or API key.
- Be accessible to all users (WCAG 2.1 AA aligned).

## 3. Target Users
| User | Need |
|------|------|
| Citizens | Know if it is safe to go out |
| Parents | Protect children's outdoor time |
| Elderly / patients | Avoid triggering conditions |
| Outdoor workers / athletes | Plan exertion safely |

## 4. Functional Requirements
| ID | Requirement | Priority |
|----|-------------|----------|
| FR-1 | User enters an AQI value (0-500) | Must |
| FR-2 | Input is validated (whole number, in range) with a clear error message | Must |
| FR-3 | App shows category, description, colour, and a gauge marker | Must |
| FR-4 | App shows recommended actions per category | Must |
| FR-5 | User selects an audience (general, children, elderly, respiratory, outdoor) and advice adapts | Must |
| FR-6 | Optional place label shown with the result | Should |
| FR-7 | Last 10 checks saved locally with a table and bar chart | Should |
| FR-8 | User can clear history | Should |
| FR-9 | "Try a sample value" button for quick demo | Could |
| FR-10 | Reference AQI scale table and everyday tips | Should |

## 5. Non-Functional Requirements
| Area | Requirement |
|------|-------------|
| Accessibility | Semantic HTML, labels, ARIA live region, skip link, visible focus, keyboard-only use, colour is never the only signal, reduced-motion support |
| Responsiveness | Works from 320px phones to desktops; tables scroll horizontally if needed |
| Performance | Single file, no external requests, no frameworks; loads instantly |
| Security | No `innerHTML` with user input (uses `textContent`), input length limits, no third-party scripts |
| Privacy | No tracking, no server; history stays in browser `localStorage` and is optional |
| Reliability | App works even if `localStorage` is blocked |
| Compatibility | Latest Chrome, Edge, Firefox, Safari; light and dark mode |
| Maintainability | Clean, commented, data-driven code (categories and advice defined as data) |

## 6. AQI Categories (Reference)
| AQI | Category |
|-----|----------|
| 0-50 | Good |
| 51-100 | Moderate |
| 101-150 | Unhealthy for Sensitive Groups |
| 151-200 | Unhealthy |
| 201-300 | Very Unhealthy |
| 301-500 | Hazardous |

## 7. Constraints and Assumptions
- AQI is entered manually; live sensor/API data is a future enhancement.
- Advice is general guidance, not medical advice (disclaimer shown in app).
- Uses the standard US EPA AQI breakpoints.

## 8. Acceptance Criteria
1. Entering 42, 87, 135, 178, 245, 340 shows Good, Moderate, Sensitive, Unhealthy, Very Unhealthy, Hazardous respectively.
2. Entering -5, 600, 12.5, or blank shows an error and no result.
3. Selecting "Children" at AQI 135 adds a child-specific tip.
4. The app is fully usable with keyboard only and a screen reader announces results.
5. Opens correctly by double-clicking `index.html` and on GitHub Pages.
6. No console errors; no network requests.

## 9. Out of Scope (Current Version)
Live AQI feeds, user accounts, push alerts, maps.
