CONTEXT: Expert full-stack blockchain developer building educational dApp. Existing: Solidity tx contracts, React visualization, Node.js backend. ADD: AI assistant chatbot, multi-page SPA (Dashboard/Explorer/Academy/Profile), Tailwind/Figma UI/UX, PostgreSQL database, 100% automated workflows via WebSockets + SQL triggers.

GOAL: Production-ready blockchain visualizer with AI assistant, dynamic multi-page UI, SQL persistence. Users: Connect wallet → Navigate pages → AI guides → Auto-updating chain/explorer → Zero manual intervention.

REQUIREMENTS:
**Tech Stack Upgrades:**
- Frontend: Next.js 15 (App Router), Tailwind CSS + shadcn/ui, Lucide React icons, react-chatbot-kit, react-flow, D3.js
- Backend: Node.js + Express + Socket.io + Prisma ORM (PostgreSQL)
- Database: PostgreSQL (Docker/supabase), tables: users/blocks/transactions/sessions
- AI Assistant: OpenAI API (GPT-4o-mini) OR Vercel AI SDK, RAG context from SQL data
- Navigation: Next.js sidebar + responsive mobile drawer

**Page Structure:**
1. /dashboard: Wallet connect, tx form, live chain visualization, mining animation
2. /explorer: Block/tx search, charts (tx volume over time), recent blocks table
3. /academy: Interactive tutorials, AI chatbot (persistent across pages), glossary
4. /profile: User tx history, favorite blocks, settings (difficulty, theme)

**AI Assistant Features:**
- Floating chat bubble (bottom-right)
- Context-aware: "You sent 0.1 ETH to 0x123..." → "Great! Watch the mining animation below"
- Educational: Explains "Nonce: 45678 found valid hash 0000abc..." 
- SQL-powered: "Your total tx volume: 2.5 ETH across 15 blocks"
- Auto-dismiss after 5s inactivity

**Automated Workflows:**
1. User tx → Smart contract event → WebSocket → SQL insert → All pages auto-refresh
2. Block mined → Backend mining sim → SQL block insert → Push notification + UI update
3. Page change → SQL session log → Analytics dashboard auto-updates

**Database Integration (Prisma):**
- Auto-migrate on startup: npx prisma db push
- Real-time queries via Prisma + Socket.io
- Backup/restore via Prisma Studio

**UI/UX Design System:**
- Modern dark/light theme toggle
- Glassmorphism cards, smooth animations (Framer Motion)
- Loading skeletons, error boundaries
- Mobile-first responsive (Tailwind breakpoints)

**RESPONSE FORMAT:**
1. Complete monorepo structure: /contracts /frontend /backend /prisma
2. Docker-compose.yml for local dev (Postgres + backend)
3. Next.js 15 full source code (app/ directory with all 4 pages)
4. Prisma schema.prisma + migrations
5. AI assistant component with 20+ educational prompts
6. Deployment: Vercel (frontend), Railway (backend+DB), Sepolia contracts
7. 5 screenshots: Dashboard+chat, Explorer charts, Mobile view, Block modal, Profile

SECURITY/AUTOMATION:
- Rate limiting, SQL injection prevention (Prisma)
- Testnet tokens only, wallet signature verification
- CI/CD GitHub Actions (lint/test/deploy)
- 95% test coverage (Vitest + Playwright E2E)

PERFORMANCE: Server-Sent Events for real-time, React Query caching, optimized images
# blockchain-decentralized-transaction-platform
