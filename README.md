# ChoreChart

A simple family webapp for managing chores.

STACK
- Backend: ASP.NET Core (C#), Swagger for API docs
- Frontend: HTML / CSS / JS (basic pages)
- Database: MySQL
- Testing: Postman (API collections)

ROLES
- Parent
  • Create chores, assign to child or mark as open
  • Set due date, reward (points/$), penalty (optional)
  • Approve/reject completed chores
  • View child summaries
- Child
  • See "My Chores" and "Open Chores"
  • Claim open chores (if allowed)
  • Mark chores as done (optional note/photo)
  • View earned rewards

CHORE STATES
OPEN → ASSIGNED → SUBMITTED → APPROVED/REJECTED → (optional) EXPIRED

PAGES
- Login / Signup
- Parent Dashboard (family overview, create chore, approvals)
- Child Dashboard (my chores, open chores, rewards)

MVP API (simplified)
- POST /auth/signup
- POST /auth/login
- POST /families (create), POST /families/join
- POST /chores (create chore)
- GET /families/{id}/chores (list chores)
- POST /chores/{id}/claim (child claims)
- POST /chores/{id}/submit (child submits)
- POST /submissions/{id}/approve or /reject
- GET /users/{id}/rewards (view balance)

BUILD ORDER
1. Auth + Family create/join
2. Parent: create & assign chores
3. Child: view & claim chores
4. Submit + approve/reject flow
5. Rewards page
6. Add Swagger + Postman collection

FUTURE IDEAS
- Recurring chores
- Notifications
- Gamification / streaks
- Allowance payouts

# to make changes in repo:
git add .
git commit -m "describe what changed"
git push