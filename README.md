# Deeply app — web preview

Clickable Flutter web build of the Deeply app running on **mock data** (no backend).
Source lives in the private monorepo `YehorDesign/deeply` (`app/`). Rebuilt by hand:

```
flutter build web --release --dart-define=USE_MOCK=true --base-href /deeply-app-preview/
```

Live: https://yehordesign.github.io/deeply-app-preview/
Login: any email + any password of 4+ characters, or continue as guest.

Live build (real API on Railway, demo login demo@thedeeply.app / Deeply123!): https://yehordesign.github.io/deeply-app-preview/live/

## Live build against the real API

```
flutter build web --release   --dart-define=API_BASE_URL=https://api-production-64c30.up.railway.app   --base-href /deeply-app-preview/live/
```

Verified end to end on 2026-09-02 with the demo account: log in, Home
("today" card and its done state), Program (28 days across 4 weeks, the next
day marked "opens tomorrow"), a day and its practice, marking a step done,
Library, a course page with its chapter/domain grouping and age filters, a
lesson, Profile, and guest mode. Screenshots of that walk-through:
[`shots/live/`](shots/live/).

Content behind the API is still thin — two courses, twelve materials, one
printable, a challenge with no days yet, no cover images — so blocks that have
no data are hidden rather than padded.
