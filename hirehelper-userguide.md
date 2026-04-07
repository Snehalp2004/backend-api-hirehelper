# HireHelper - Backend User Guide

## What is HireHelper?
HireHelper is a full-stack web application designed to connect users who need help with tasks (hirers) and those willing to offer services (helpers). Key features include:
- User authentication (login/register/forgot password/OTP verification)
- Profile management with photo uploads
- Dashboard for overview
- Posting and managing tasks/requests
- Viewing feeds, my tasks, my requests, offers
- Notifications
- Help section

Built with Node.js/Express backend, postgresql database.

## User Guide (Backend/Admin)
1. **Setup**:
   - Install dependencies: `npm install`
   - Configure database in config/db.js and run SQL scripts in sql/ folder (e.g., create_tasks_table.sql).
   - Initialize DB: `node config/initDb.js`
   - Start server: `node server.js` (runs on port 3000).

2. **API Endpoints**:
   - Auth: POST /api/auth/login, /api/auth/register
   - Users: /api/users/
   - Profiles: /api/profiles/
   - Tasks: /api/tasks/
   - Requests: /api/requests/
   - Notifications: /api/notifications/

3. **Key Files**:
   - controllers/: Business logic
   - routes/: API routes
   - middleware/: Auth checks
   - utils/taskStatus.js: Task statuses
   - uploads/profile-photos/: Profile images

4. **Database**:
   - Tables: users, tasks, requests, notifications, profiles
   - Use MySQL client to query/manage data.

For integration: Frontend connects via services like auth.service.ts to backend APIs.

For developers: Run `npm start` in backend-api to start the backend.
