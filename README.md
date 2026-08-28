# Hi there, I'm Bharath Reddy 👋

**Systems & Full-Stack Software Engineer** - I write low-level C (epoll, mmap, seccomp, WAL) and ship production
TypeScript/React applications on top of it. M.S. Cyber Operations, Webster University.

📍 Florence, KY (Greater Cincinnati) | 🌐 [bharathdev.com](https://bharathdev.com) | 💼 [LinkedIn](https://linkedin.com/in/nagireddybharathreddy) | ✉️ [hello@bharathdev.com](mailto:hello@bharathdev.com)

Open to Software Engineer roles in the US (F-1 OPT, eligible for the 24-month STEM extension - no sponsorship required near-term).

---

## 🚀 Featured Projects

### ⚙️ Systems & Databases

**[server_1500](https://github.com/kx3ez1/server_1500)** - *Express-style HTTP server in pure C11*
A hot-reloadable HTTP server on an `epoll` event loop with a trie-based router, middleware pipeline (CORS, IP filtering,
payload limits), and gzip/brotli/zstd encoding.
- **1.59M req/sec per core at 627 ns average latency** - MTU-aligned responses fit a single 1500-byte Ethernet frame
- Slab allocation (zero heap allocs on the request path) and zero-copy static assets via `mmap` + `writev`
- `seccomp` syscall sandboxing, per-IP rate limiting, master-worker `fork` isolation, `SIGHUP` zero-downtime reload
- 57 unit, integration, and E2E tests

**[ZetaDB](https://github.com/kx3ez1/zeta_db)** - *Crash-safe in-memory key-value database in C*
An in-memory engine with sequential Write-Ahead Logging and a coroutine HTTP REST API (API-key/bearer auth, JSON).
- **4.5M reads/sec** on 16 B values, **3.0M** on 4 KB values (500K queries over 10K keys)
- `engine_exists()` fast path reaches **5.9M ops/sec** - 1.97x faster on 4 KB records by skipping payload copies
- Fine-grained sharding + Optimistic Concurrency Control for parallel access
- 34/34 CTest suites: ACID durability, hard-kill WAL recovery, corrupt-WAL boundaries, HTTP auth/overflow

### 🌐 Full-Stack

**[Easy Com](https://github.com/kx3ez1/easy_com)** - *Full-stack e-commerce platform*
Storefront plus a role-gated admin dashboard (products, orders, users, checkouts).
- **Frontend:** Next.js 16 App Router, React 19, Redux Toolkit, Tailwind CSS v4, Firebase Auth
- **Backend:** Express 5 in TypeScript behind an Nginx proxy - Bearer-token auth middleware, request sanitization,
  centralized error handling, Stripe *and* PayPal checkout flows
- **Storage:** persisted through **ZetaDB** (my own engine, above) via an interface-driven repository layer that keeps
  the datastore swappable
- 105 Jest tests across 10 suites covering repositories, controllers, and middleware

**[Portfolio](https://github.com/kx3ez1/Portfolio)** - *Personal site*
Next.js 16 / React 19 on Cloudflare Workers, with the resume built from LaTeX source in-repo.

**[Spotify Clone](https://github.com/kx3ez1/spotify-clone)** - *Music streaming app*
React 18 + Vite + Tailwind CSS with Redux Toolkit state, the JioSaavn API for search, and the Web Audio API for custom
playback controls and queue management.

### 🤖 Tools & Automation

**[LLM Wrapper Telegram Bot](https://github.com/kx3ez1/llm_wrapper_telegram_bot)** - *Python Telegram bot*
OpenAI SDK pointed at an Azure OpenAI endpoint, with markdown responses, reply-with-context threading, response
auto-splitting past Telegram's 4096-char limit, optional password gating, rotating logs, concurrent handling via
`ThreadPoolExecutor`, and Docker Compose deployment.

**[Custom Clock GNOME Extension](https://github.com/kx3ez1/custom_clock_gnome_extension)** - *GNOME Shell extension*
Adds a secondary clock beside the system clock for a chosen timezone or synchronized internet time, with a GSettings
schema and a preferences UI.

---

## 🛠️ Tech Stack

**Languages**
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)

**Frontend**
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-764ABC?style=for-the-badge&logo=redux&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)

**Backend & Data**
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![Django](https://img.shields.io/badge/Django_REST-092E20?style=for-the-badge&logo=django&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-DD2C00?style=for-the-badge&logo=firebase&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=for-the-badge&logo=stripe&logoColor=white)

**Systems, Infra & Testing**
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=for-the-badge&logo=cmake&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare_Workers-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white)

---

## 📊 GitHub Activity

<p align="center">
  <img src="https://streak-stats.demolab.com?user=kx3ez1&theme=dark&hide_border=true" alt="kx3ez1 GitHub streak" />
</p>
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=kx3ez1&layout=compact&theme=dark&hide_border=true&langs_count=8" alt="kx3ez1 top languages" />
</p>
