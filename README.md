# Fe O Faki Handicrafts — Web Application
*Internship Project · 2025*

A Laravel web application built for Fe O Faki Handicrafts,
a small business selling traditional Pacific handicrafts.

> **Note:** This project was built as part of a team internship.
> My scope was the backend — authentication system and server-side
> routing. The frontend UI (Blade templates, CSS) was designed and
> built by a teammate.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Laravel 11 (PHP MVC) |
| Database | SQLite (default) / MySQL (configurable) |
| Auth | Session-based — manual implementation, no Sanctum/Passport |
| Frontend | Blade templates, CSS, JavaScript (teammate-authored) |

---

## What I Built

### Dual Authentication System
Two separate auth flows with session management:

**Admin**
- Login / logout with email + password
- Password verification via `Hash::check()`
- Session keys: `admin_logged_in`, `admin_id`
- Protected dashboard route after login

**User**
- Registration with input validation
- Login / logout
- Session-based access control

### Routing
Full route structure covering:
- Public pages (home, about, contact, products)
- User auth (login, register, logout)
- Admin auth (separate login, dashboard)
- Scoped views (POS, inventory, layby, cart, checkout)

---

## What Was Scoped But Not Completed
- Product CRUD (create, edit, delete) — `ProductsController` 
  returns view only; backend logic not implemented within 
  the internship timeline
- Cart and checkout — routes and views exist, no backend logic

---

## Getting Started

```bash
git clone https://github.com/Patrickpaul155/fe-o-faki-api-Internship-2025.git
cd fe-o-faki-api-Internship-2025

composer install
cp .env.example .env
php artisan key:generate

# For MySQL: uncomment and configure DB_ lines in .env
# Default runs on SQLite — no extra config needed

php artisan migrate
php artisan serve
```

---

## Environment

Key `.env` values to configure for MySQL:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=fe_o_faki
DB_USERNAME=root
DB_PASSWORD=
```
