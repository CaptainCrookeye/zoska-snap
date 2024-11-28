Dominik Netri 4.C 2. sk.

Inštalácia Next.js

npx create-next-app@latest

Settings:
What is your project named? *názov projektu*
Would you like to use TypeScript? No / Yes - Yes
Would you like to use ESLint? No / Yes - Yes
Would you like to use Tailwind CSS? No / Yes - No
Would you like your code inside a `src/` directory? No / Yes - Yes
Would you like to use App Router? (recommended) No / Yes - Yes
Would you like to customize the import alias (`@/*` by default)? No / Yes - No

Inštalácia Material UI:
npm install @mui/material @emotion/react @emotion/styled
npm install @mui/icons-material @mui/material @emotion/styled @emotion/react

Spustenie servera na development:
npm run dev
npm run build //optimalizovany kod na production

VSCode extensions:
GitLens
GitHub Pull Requests
Prettier

File system:
app – core stránky, router
priečinky v app – jednotlivé stránky

Vyhradené súbory v app:
page.tsx – hlavná stránka
layout.tsx
not-found.tsx

Version control:
ukladanie lokálnych súborov na cloud cez .git
production server – hostovanie stránky na internete
github – ukladá len poslednú zálohu
git – ukladá všetky predchádzajúce verzie

Setup:
git init
git branch -m main
založiť repository na github stránke
git config –global user.name „GITHUB_MENO“
git config –global user.email „GITHUB_EMAIL“
git remote add origin REPOSITORY_URL
git remote -v //kontrola či to funguje

Príkazy:
git add . //uloží celý projekt
Source Control záložka – commitne zmeny na github, treba dať hore meno

Production server:
vercel - služba na hosting

Prisma:
1. Vercel -> Storage:
    Neon -> Create -> Accept -> Region -> Frankfurt, Germany-(fra1) -> Connect
    in snap-zoska-4h-postgres:
    .env.local -> Show secret -> Copy snippet into your src/.env 

2. VsCode:
    npm install @prisma/client @auth/prisma-adapter
    npm install prisma --save-dev
    npx prisma init

3. VsCode:
    In .env replace value of DATABASE_URL
    .env
    create app/api/prisma.ts
    package.json:   "build": "prisma generate && next build",
                    "postinstall": "prisma generate",


4. VsCode terminal:
    npx prisma format
    npx prisma migrate dev --name NAZOV_COMMITU  //podobne ako github commit, 
    npx prisma generate                          //podobne ako github sync
    npx prisma studio                            //editor DB
