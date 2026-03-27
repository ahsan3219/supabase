# Expo React Native Social Auth Quickstart

This example shows how to use `supabase-js` with Expo for social login flows across:

- Apple Sign In (iOS + Android + Web)
- Google Sign In (iOS + Android + Web)

## Why this example exists

It demonstrates a practical mobile + web setup with:

- platform-specific social login buttons
- `signInWithIdToken` for OAuth providers
- secure local session persistence on native platforms

## Prerequisites

- Node.js 20+
- npm
- Expo CLI (`npx expo`)
- A Supabase project with Apple and/or Google providers configured

## Environment variables

Create an `.env` file in this directory and set:

```bash
EXPO_PUBLIC_SUPABASE_URL=...
EXPO_PUBLIC_SUPABASE_PUBLISHABLE_KEY=...

# Apple
EXPO_PUBLIC_APPLE_AUTH_SERVICE_ID=...
EXPO_PUBLIC_APPLE_AUTH_REDIRECT_URI=...

# Google (web)
EXPO_PUBLIC_GOOGLE_AUTH_WEB_CLIENT_ID=...
```

## Run the example

```bash
npm install
npx expo start
```

Then choose one of:

- `i` for iOS simulator
- `a` for Android emulator
- `w` for web

## Notes and troubleshooting

- Apple auth on Android requires `serviceId` and `redirectUri` configured in Apple Developer settings.
- Web social login requires valid OAuth redirect URLs in both the provider console and Supabase Auth settings.
- If login succeeds at the provider but fails in app, inspect the browser/device logs for token and nonce errors.
