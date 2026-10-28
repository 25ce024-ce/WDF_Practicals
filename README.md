# StudentHub — ITUE203 Web Development Frameworks Practicals (2026–27)

A single semester-long project that progressively covers Practical 1–15 from the supplied practical list. The project is intentionally organized so the same StudentHub portal is extended at each practical rather than creating fifteen unrelated projects.

## Requirements
- PHP 8.1+ with `mysqli` enabled
- MySQL 8+ or MariaDB
- XAMPP/WAMP/LAMP, VS Code, Git
- Modern browser

## Run locally with XAMPP
1. Copy the `StudentHub_WDF_Practicals` folder into `xampp/htdocs/`.
2. Start Apache and MySQL from the XAMPP control panel.
3. Open phpMyAdmin and import `database/studenthub.sql`.
4. Check `backend/config.php` and set your local database username/password if different.
5. Open `http://localhost/StudentHub_WDF_Practicals/`.
6. Demo admin account after importing the seed data: `admin@studenthub.local` / `Admin@12345`. Change this password for any real deployment. Seed hash is generated for the stated demo password.

## Static-only practicals
The first six practicals can be demonstrated without the PHP backend. Open the home page through Apache for consistent paths and for Fetch API requests. The external JSON datasets are in `data/` and contain 15+ sample records each.

## Practical-to-project map
1. `docs/requirements.md`, `docs/sitemap.md`, `docs/wireframe-notes.md`, Git setup
2. Ten semantic HTML pages, accessible labels/landmarks and shared navigation
3. `assets/css/style.css`: mobile-first Flexbox/Grid and breakpoints
4. `assets/js/main.js`: FAQ, modal, slider, banner, hamburger, theme/localStorage
5. `register.html` + `assets/js/validation.js`: front-end validation and error messages
6. `events.html`, `directory.html`, `assets/js/data-browser.js`, `data/*.json`: Fetch, search, filter, sort, pagination
7. `backend/process_form.php`: server-side validation and CSV/JSON storage
8. `database/studenthub.sql`, `backend/config.php`: relational schema and mysqli connection
9. `backend/register.php`: duplicate check, validation, `password_hash()`
10. `backend/login.php`, `backend/logout.php`, `backend/includes/auth.php`: sessions, role, timeout
11. `backend/students.php`: student CRUD/search/filter
12. `backend/events.php`: event CRUD and poster validation
13. `backend/api/students.php`, `backend/api/events.php`, `assets/js/api-crud.js`: JSON CRUD endpoints
14. `backend/admin.php`, `backend/includes/audit.php`: role-protected dashboard and audit log
15. Integration checklist and local deployment documentation

## Important security note
This is an educational local lab project, not a production-ready service. Keep PHP/MySQL running locally, use the included prepared statements, and do not deploy with demo credentials. The “remember me” feature is deliberately described as optional in the practical and is not enabled by default.
