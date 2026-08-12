# Django Assignment 1

Welcome to the Django Assignment Repository for the Enterprise Python Backend Development class.

## Objective

This assignment is designed to assess your understanding of:

- Django Project Setup
- Django Apps
- Models
- Views
- URLs
- Templates
- Admin Panel
- Git & GitHub Workflow

---

## Instructions

1. Clone this repository.

```bash
git clone <repository-url>
```

2. Create and activate a virtual environment.

Windows

```bash
python -m venv venv
venv\Scripts\activate
```

Linux/macOS

```bash
python3 -m venv venv
source venv/bin/activate
```


3. Apply migrations.

```bash
python manage.py migrate
```

4. Start the development server.

```bash
python manage.py runserver
```

---

## Assignment Requirements

Complete all the tasks given during class.

Your project should:

- Follow Django best practices
- Have clean and readable code
- Use meaningful variable names
- Handle errors appropriately
- Include comments where necessary

---

## Git Requirements

You are expected to:

- Initialize Git (if required)
- Make **at least 5 meaningful commits**
- Use descriptive commit messages
- Push your project to GitHub before the deadline

Examples of good commit messages:

```
Created Django project
Added blog app
Implemented models
Configured URLs
Completed templates
```

---

## Submission

Submit only your GitHub repository link before the deadline.

---

## Marking Scheme

| Criteria | Marks |
|-----------|------:|
| Project setup | 10 |
| Django functionality | 35 |
| Code quality | 15 |
| Git commits | 15 |
| README | 10 |
| Project structure | 10 |
| Timely submission | 5 |
| **Total** | **100** |

---

## Important

Do **not** upload:

- venv/
- __pycache__/
- *.pyc
- .env

Ensure your `.gitignore` file excludes these files.

---

Good luck, and happy coding!

## Author

Sunday Chinonso Solomon

**Enterprise Python Backend Development**
# Akax Portfolio

A Django portfolio site — Homepage, Skills, Blog (full CRUD), and Contact.

## Stack
- Django 6.0 (works fine on Django 5.x too — see `requirements.txt`)
- SQLite (default dev database)
- Vanilla JS + hand-rolled CSS (no frontend framework)
- Google Fonts: Inter, Playfair Display, IBM Plex Mono

## Pages
| URL | Page | Auth |
|-----|------|------|
| `/` | Homepage — hero, featured skills, latest posts | Public |
| `/skills/` | Skills & tools, grouped, with progress bars | Public |
| `/blog/` | Blog list with category tab filtering (no reload) | Public |
| `/blog/new/` | Create post | Login required |
| `/blog/<slug>/` | Post detail (Edit/Delete buttons show if logged in) | Public to view |
| `/blog/<slug>/edit/` | Edit post | Login required |
| `/blog/<slug>/delete/` | Delete confirmation | Login required |
| `/contact/` | Contact form → saves to DB | Public |
| `/login/`, `/logout/` | Admin auth | Public |
| `/admin/` | Django admin — manage all content | Superuser |

## Design system
Near-black background (`#0a0a0b`) with a warm gold accent (`#d4a857`), glassmorphism
cards (`backdrop-filter: blur`), Playfair Display for headings, Inter for body text,
IBM Plex Mono for eyebrow labels and category tags. Tokens live in
`static/css/base.css` as CSS custom properties — full dark/light theme swap via
`data-theme` attribute + `localStorage`.

Dark/light theme toggle, mobile hamburger nav, scroll-reveal animations, and blog
category tab filtering (JS, no page reload) **are** implemented.
