# Mova Landing Page Builder - Frontend

## Requirements
- Node.js 18+
- npm atau yarn

## Setup

1. Install dependencies:
```bash
npm install
# atau
yarn install
```

2. Create `.env` file:
```env
EXPO_PUBLIC_BACKEND_URL=https://api.movacuan.online
```

3. Run development:
```bash
npx expo start --web
```

## Build untuk Production

### Build Web (untuk Vercel/Netlify):
```bash
npx expo export --platform web
```
Output akan di folder `dist/`

### Build APK (untuk Android):
```bash
# Install EAS CLI
npm install -g eas-cli

# Login ke Expo
eas login

# Build APK
eas build --platform android --profile preview
```

## Deploy ke Vercel

1. Push code ke GitHub
2. Connect repository ke Vercel
3. Set build command: `npx expo export --platform web`
4. Set output directory: `dist`
5. Add environment variable: `EXPO_PUBLIC_BACKEND_URL`
6. Deploy!

## Deploy ke Netlify

1. Push code ke GitHub
2. Connect repository ke Netlify
3. Set build command: `npx expo export --platform web`
4. Set publish directory: `dist`
5. Add environment variable: `EXPO_PUBLIC_BACKEND_URL`
6. Deploy!

## Struktur Folder

```
frontend/
├── app/                    # Halaman (file-based routing)
│   ├── _layout.tsx        # Root layout
│   ├── index.tsx          # Home/Welcome page
│   ├── login.tsx          # Login page
│   ├── register.tsx       # Register page (with serial number)
│   ├── dashboard.tsx      # User dashboard
│   ├── editor.tsx         # Landing page editor
│   └── view/
│       └── [slug].tsx     # Public landing page viewer
├── src/
│   ├── api/
│   │   └── client.ts      # API client
│   └── context/
│       └── AuthContext.tsx # Auth context
├── assets/                 # Images, fonts
├── app.json               # Expo config
└── package.json           # Dependencies
```
