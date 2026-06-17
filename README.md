*This project has been created as part of the 42 curriculum by ahbey, manbengh, wlarbi-a, cumoncoq, nabboud.*

# ft_transcendence

A full-stack social network with real-time chat, posts, friends system, and notifications.

---

## Quick Start

### Prerequisites

- Docker & Docker Compose

### First run (SSL init)

```bash
make init up
```

### All subsequent runs

```bash
make up
```

### Access

| URL | Description |
|-----|-------------|
| `https://localhost:4433/` | Application |
| `https://localhost:4433/api-docs/` | API documentation |

### Useful commands

```bash
make init      # Generate SSL certificates (first run only)
make up        # Start all services
make down      # Stop containers
make logs      # View logs
make ps        # List running containers
make restart   # Restart services
make re        # Clean and restart
make fclean    # Full cleanup (containers, images, volumes)
```

---

## Features

| Feature | Description |
|---------|-------------|
| OAuth | Login with 42 Intra or GitHub |
| 2FA | Two-factor authentication |
| Profiles | Update profile, password, bio, username |
| Posts | Create and delete posts with images |
| Likes & comments | Social interactions |
| Friends system | Add, accept, and delete friends |
| Real-time chat | WebSocket-based messaging |
| Notifications | Real-time user alerts |
| Advanced search | Search users and posts |
| Dashboard | Personal analytics |
| i18n + RTL | Multi-language with right-to-left support |
| Content moderation AI | Automatic comment moderation |
| Public API | External access to platform data |

---

## Technical Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Next.js, React, TypeScript, TailwindCSS |
| Backend | Node.js, Express |
| ORM | Prisma |
| Database | PostgreSQL |
| Real-time | WebSockets |
| Reverse proxy | Nginx |
| Containerization | Docker |

---

## Browser Compatibility

| Browser | Status |
|---------|--------|
| Google Chrome 147+ | Validated (required baseline) |
| Safari 26.1 | Validated |
| Firefox / Edge | To be tested |

---

---

## Team

| Login | Role | Responsibilities |
|-------|------|-----------------|
| manbengh | PO, Developer | Public API, notifications |
| nabboud | PO, Developer | Image upload, dashboard, posts |
| ahbey | PM, Developer | ORM (Prisma), 2FA, content moderation AI |
| wlarbi-a | PM, Developer | i18n, RTL, browser compatibility |
| cumoncoq | Tech Lead, Developer | WebSockets, chat, OAuth, design system |

---

## Modules

### Major (2 pts each)

- Framework frontend + backend (all team)
- User interaction — cumoncoq
- Real-time features (WebSockets) — cumoncoq
- User Management — manbengh, ahbey, cumoncoq, nabboud
- Public API — manbengh

### Minor (1 pt each)

- Prisma ORM — ahbey
- Notifications — manbengh, cumoncoq
- OAuth — cumoncoq
- 2FA — ahbey
- Dashboard analytics — nabboud
- i18n — wlarbi-a
- RTL — wlarbi-a
- Multi-browser support — wlarbi-a
- Design system — cumoncoq
- Content moderation AI — ahbey
- Advanced search — nabboud, wlarbi-a
- File upload — nabboud

**Total: 22 points** (minimum required: 14)

---

## Database Relationships

- User → Post (1:N)
- Post → Comment (1:N)
- User → Comment (1:N)
- User / Post → Like, Favorite, Repost (1:N)
- Comment → CommentLike, CommentFavorite (1:N)
- User → Friends (N:N via sender/receiver)
- User → Notification (1:N via recipient + actor)
- Conversation → ConversationMember → Message (1:N)

---

## Project Management

The team held 2–3 meetings per week via Discord. Tasks were distributed weekly on GitHub based on modules and individual strengths.

**Tools:** GitHub, Docker, Prisma Studio, Discord

---

## Resources

- [Prisma](https://www.prisma.io/docs)
- [Express](https://expressjs.com/)
- [Next.js](https://nextjs.org/docs)
- [React](https://react.dev/)
- [TypeScript](https://www.typescriptlang.org/docs/)
- [Tailwind CSS](https://tailwindcss.com/docs)
- [PostgreSQL](https://www.postgresql.org/docs/)

---

## AI Usage

AI tools were used to assist with documentation writing and organizing project features. All generated content was reviewed and validated by the team.
