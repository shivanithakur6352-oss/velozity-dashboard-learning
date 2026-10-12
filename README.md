# Velozity Dashboard — Learning Starter

This is a learning scaffold for a role-based project dashboard. The hiring assessment shown in the supplied brief says AI tools are strictly prohibited, so this package is intentionally **not a completed submission**. Implement and understand the TODOs yourself before using any work in an assessment.

## Stack
- Frontend: React + TypeScript + Vite
- Backend: Node.js + Express + TypeScript
- Database: PostgreSQL + Prisma
- Real-time: Socket.IO
- Validation: Zod

## Suggested setup
1. Install Node.js LTS and PostgreSQL.
2. Copy `server/.env.example` to `server/.env` and set your local database URL and secrets.
3. From `server/`: `npm install`
4. From `server/`: `npx prisma generate`
5. From `server/`: `npx prisma migrate dev --name init`
6. From `server/`: `npm run dev`
7. From `client/`: `npm install`, then `npm run dev`

The scaffold includes the main schema and a few starting files. It does not yet implement production-ready auth, permissions, WebSocket event filtering, notifications, scheduled overdue processing, or the complete UI.

## Implementation checklist
- [ ] Access-token verification middleware
- [ ] Refresh-token rotation with HttpOnly cookie; hash stored refresh tokens
- [ ] API-level role checks for every protected route
- [ ] Project-manager ownership checks on project and task endpoints
- [ ] Developer task-assignment checks
- [ ] Persist task status changes and activity events in one transaction
- [ ] Socket.IO room authorization and role-filtered activity feed
- [ ] Catch-up query for the latest 20 missed events
- [ ] Notifications and read/unread endpoints
- [ ] Scheduled overdue-task job
- [ ] Dashboard aggregates and query-parameter filters
- [ ] Seed data: 1 admin, 2 project managers, 4 developers, 3+ projects and tasks
- [ ] Tests for cross-role access and WebSocket authorization
- [ ] Deploy and document limitations

Never commit `.env` or real credentials.
