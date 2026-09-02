# Deeply app — web preview

Clickable Flutter web build of the Deeply app running on **mock data** (no backend).
Source lives in the private monorepo `YehorDesign/deeply` (`app/`). Rebuilt by hand:

```
flutter build web --release --dart-define=USE_MOCK=true --base-href /deeply-app-preview/
```

Live: https://yehordesign.github.io/deeply-app-preview/
Login: any email + any password of 4+ characters, or continue as guest.

Live build (real API on Railway, demo login demo@thedeeply.app / Deeply123!): https://yehordesign.github.io/deeply-app-preview/live/
