# HTTP Requests

## Authentication

These examples use [httpie](https://httpie.io/).

```bash
# Log in as admin
http --session=./session.json localhost:8000/api/login email==admin password==admin
```

- Return Options
  - **200:** `{"message": "Logged in successfully!"}`
  - **401:** `{"detail": "You're already logged in as admin. Please log out first."}`

```bash
# Reset authentication database (if logged in as admin)
http --session=./session.json localhost:8000/api/reset_auth
```

- Return Options
  - **200:** `{"message": "Database reset successfully!"}`
  - **401:** `{"detail": "Please log in to perform this action"}`

```bash
# Logout
http --session=./session.json -f GET localhost:8000/api/logout
```

- Return Options
  - **200:** `{"message": "Logged out successfully!"}`
  - **401:** `{"detail": "You're not currently logged in"}`

# API

- Meta
  - **List all API endpoints:** http://localhost:8000/api
- Applications
  - **List all applications:** http://localhost:8000/api/applications/
  - **List application for specific user:** http://localhost:8000/api/applications/10049182
- Users
  - **List all users:** http://localhost:8000/api/users/
  - **List specific user:** http://localhost:8000/api/users/10049182