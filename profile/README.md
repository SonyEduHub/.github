## Sony Vansha Education Hub

<hr>

![wallhaven-6d3v17](https://github.com/user-attachments/assets/c7b8e1c1-9b80-4943-b673-49420d1b90dc)

## Struktur Next.js Full Stack (Professional)

```sh
my-nextjs-app/
│
├── public/                     # Static assets
│   ├── images/
│   └── icons/
│
├── src/
│   │
│   ├── app/                    # App Router (Next.js 13+)
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── loading.tsx
│   │   ├── error.tsx
│   │   │
│   │   ├── api/                # Backend API routes
│   │   │   ├── auth/
│   │   │   │   └── route.ts
│   │   │   ├── users/
│   │   │   │   └── route.ts
│   │   │   └── posts/
│   │   │       └── route.ts
│   │   │
│   │   ├── dashboard/
│   │   │   ├── page.tsx
│   │   │   ├── layout.tsx
│   │   │   └── components/
│   │   │
│   │   └── auth/
│   │       ├── login/
│   │       │   └── page.tsx
│   │       └── register/
│   │           └── page.tsx
│   │
│   │
│   ├── components/             # Reusable UI Components
│   │   ├── ui/
│   │   │   ├── button.tsx
│   │   │   ├── modal.tsx
│   │   │   └── input.tsx
│   │   │
│   │   ├── layout/
│   │   │   ├── navbar.tsx
│   │   │   ├── sidebar.tsx
│   │   │   └── footer.tsx
│   │   │
│   │   └── common/
│   │       ├── loader.tsx
│   │       └── empty-state.tsx
│   │
│   │
│   ├── lib/                    # Core utilities
│   │   ├── db.ts               # Database connection
│   │   ├── logger.ts
│   │   └── utils.ts
│   │
│   │
│   ├── services/               # Business logic layer
│   │   ├── auth.service.ts
│   │   ├── user.service.ts
│   │   └── post.service.ts
│   │
│   │
│   ├── repositories/           # Database queries
│   │   ├── user.repository.ts
│   │   └── post.repository.ts
│   │
│   │
│   ├── hooks/                  # Custom React hooks
│   │   ├── useAuth.ts
│   │   └── useDebounce.ts
│   │
│   │
│   ├── store/                  # Global state
│   │   ├── auth.store.ts
│   │   └── app.store.ts
│   │
│   │
│   ├── types/                  # TypeScript types
│   │   ├── user.ts
│   │   └── post.ts
│   │
│   │
│   ├── middleware/             # Middleware logic
│   │   └── auth.middleware.ts
│   │
│   │
│   ├── config/                 # Configuration
│   │   ├── env.ts
│   │   └── constants.ts
│   │
│   │
│   └── styles/                 # Global styling
│       ├── globals.css
│       └── tailwind.css
│
│
├── prisma/                     # ORM (optional)
│   ├── schema.prisma
│   └── migrations/
│
│
├── tests/                      # Testing
│   ├── unit/
│   └── integration/
│
│
├── .env
├── .env.example
├── next.config.js
├── tsconfig.json
├── package.json
└── README.md
```

### Arsitektur Layer (Best Practice)

```sh
UI (React Components)
        │
        ▼
API Route (Controller)
        │
        ▼
Service Layer (Business Logic)
        │
        ▼
Repository Layer (Database Query)
        │
        ▼
Database
```

Contoh flow:

```sh
app/api/users/route.ts
        ↓
user.service.ts
        ↓
user.repository.ts
        ↓
PostgreSQL
```

### Tools yang Biasanya Dipakai

- Next.js (App Router)
- TypeScript
- PostgreSQL
- Prisma / Drizzle ORM
- Zod (validation)
- React Query / SWR
- TailwindCSS
- Docker

---

## Keuntungan Struktur Ini

- ✅ Scalable untuk project besar
- ✅ Separation of concern jelas
- ✅ Mudah testing
- ✅ Mudah replace database / service
- ✅ Tim besar bisa kerja paralel
