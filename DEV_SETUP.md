# 🚀 Development Setup

## Quick Start

```bash
# Install all dependencies (root, backend, frontend, library)
npm run install:all

# Run frontend + backend concurrently
npm run dev
```

The app will be available at:
- **Frontend**: http://localhost:5173
- **Backend**: http://localhost:3001

## Individual Commands

```bash
# Run only backend
npm run dev:backend

# Run only frontend  
npm run dev:frontend

# Run tests
npm run test

# Run tests with UI
npm run test:ui

# Build frontend for production
npm run build
```

## Manual Setup (if needed)

```bash
# Backend
cd backend
npm install
npm start

# Frontend (in another terminal)
cd frontend
npm install
npm run dev
```

## Environment Variables

### Backend (.env)
```
PORT=3001
```

### Frontend
No environment variables required. Configuration is in `frontend/src/config.ts`:
- Arkiv Mendoza Testnet (Chain ID: 60138453056)
- Backend URL: http://localhost:3001

## Troubleshooting

**Port already in use:**
```bash
# Kill process on port 3001 (backend)
lsof -ti:3001 | xargs kill -9

# Kill process on port 5173 (frontend)
lsof -ti:5173 | xargs kill -9
```

**Dependencies not installed:**
```bash
npm run install:all
```

**Crypto errors in browser:**
- Vite is configured with crypto polyfills (crypto-browserify)
- Check `frontend/vite.config.ts`

**MetaMask not detected:**
- Install MetaMask browser extension
- Connect to Arkiv Mendoza testnet
- Request test tokens from faucet
