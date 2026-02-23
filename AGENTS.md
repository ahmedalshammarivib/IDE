# React Native / Expo Project Rules

## Tech Stack
- React Native + Expo SDK 52+ (latest stable)
- TypeScript strict mode — no `any` types
- Expo Router v3 (file-based navigation)
- Zustand (state management)
- TanStack Query (data fetching & caching)
- NativeWind v4 (styling)
- Zod (validation)
- EAS Build (production builds)

## Folder Structure
```
app/           → Expo Router screens (file-based)
components/ui/ → base design system components
features/      → feature modules
hooks/         → shared custom hooks
store/         → Zustand stores
api/           → ALL data fetching
utils/         → helper functions
constants/     → app-wide constants
types/         → shared TypeScript interfaces
```

## Hard Rules
- Functional components ONLY
- expo-image instead of Image
- FlashList for ALL lists — never ScrollView with map
- No inline styles — NativeWind classes only
- Named exports for all components
- No `any` types
- All API calls ONLY in api/ folder
- Zod validation for ALL external data
- Use `npx expo install` — never npm/yarn directly for Expo packages

## Build Commands
- npx expo start -c    → dev server (clean cache)
- npx expo run:android → Android build
- npx expo run:ios     → iOS build
- eas build            → production build
