# Linux Clock-In/Out App with Admin Panel

## Objective
Build a Linux application for employees to clock in, clock out, and take lunch breaks, with an admin panel for user management. All data stored locally.

## Requirements
- [ ] Employee clock in / clock out
- [ ] Lunch break tracking (start lunch / end lunch)
- [ ] Admin panel: add users, remove users, view all users
- [ ] All data stored locally (no cloud)

## Decisions
1. **UI Technology**: Web UI (Flask, runs in browser)
2. **Storage**: SQLite (local, relational, zero-config)
3. **Employee Auth**: PIN code entry
4. **Admin Auth**: Dedicated admin user account (username + password)

## Tech Stack
- **Backend**: Python + Flask
- **Database**: SQLite (local file)
- **Frontend**: HTML + CSS + vanilla JS (lightweight, no build step)
- **Auth**: Session-based login; employees use PIN on clock screen

## Data Model
- `users`: id, name, pin, role (admin/employee), active, created_at
- `time_entries`: id, user_id, entry_type (clock_in, clock_out, lunch_start, lunch_end), timestamp

## UI Flow
1. **Login**: Choose Admin Login (username/password) or Employee PIN entry
2. **Employee Dashboard**: Clock In / Clock Out / Start Lunch / End Lunch buttons, current status, today's hours
3. **Admin Panel**: Add/remove employees, view all users, view/export time entries

## Implementation Steps
1. Set up project structure and virtual environment
2. Initialize SQLite database and models
3. Build Flask backend (routes, auth, CRUD)
4. Build frontend templates (login, employee dashboard, admin panel)
5. Add clock-in/out and lunch logic
6. Testing and verification
7. Create start script
