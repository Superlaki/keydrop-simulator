# KeyDrop Simulator - Public Deployment

## Wdrożenie produkcyjne

### Opcja 1: Vercel (zalecane)
1. Zainstaluj Vercel CLI: `npm i -g vercel`
2. Zaloguj się: `vercel login`
3. Wdróż: `vercel --prod`
4. Skonfiguruj bazę danych PostgreSQL w Vercel

### Opcja 2: Railway
1. Stwórz konto na [railway.app](https://railway.app)
2. Podłącz repozytorium GitHub
3. Skonfiguruj zmienne środowiskowe:
   - `DATABASE_URL` (PostgreSQL)
   - `NODE_ENV=production`
4. Railway automatycznie zbuduje i wdroży aplikację

### Opcja 3: DigitalOcean App Platform
1. Stwórz konto DigitalOcean
2. Podłącz repozytorium GitHub
3. Skonfiguruj:
   - Build command: `yarn build`
   - Run command: `yarn start`
   - Environment variables: `DATABASE_URL`, `NODE_ENV=production`

### Konfiguracja bazy danych
- Użyj PostgreSQL (Railway, Supabase, ElephantSQL)
- Importuj schema: `npx prisma db push`
- Wygeneruj client: `npx prisma generate`

### Domena
- Każda platforma udostępnia subdomenę
- Można podłączyć własną domenę w ustawieniach

### Monitorowanie
- Sprawdzaj logi w panelu platformy
- Monitoruj użycie bazy danych
- Ustaw alerty wydajności

Aplikacja będzie dostępna 24/7 bez potrzeby uruchamiania lokalnego komputera.
