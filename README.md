# AuthSystem — Bootstrap 5 Authentication POC

## Project Description

A complete, fully responsive authentication system proof of concept built with **Bootstrap 5**, **Bootstrap Icons**, and custom CSS. No frameworks, no templates — original styling only.

---

## Tech Stack

| Layer      | Technology                          |
|------------|-------------------------------------|
| Markup     | Semantic HTML5                      |
| Styling    | Bootstrap 5.3 (CDN) + Custom CSS    |
| Icons      | Bootstrap Icons 1.11 (CDN)          |
| Fonts      | Google Fonts — Inter + Poppins      |
| Scripting  | Vanilla JavaScript (ES6+)           |

---

## Pages

| File                   | Purpose                              |
|------------------------|--------------------------------------|
| `index.html`           | Login page                           |
| `register.html`        | New user registration                |
| `forgot-password.html` | Password recovery request            |
| `reset-password.html`  | Set a new password                   |
| `dashboard.html`       | Authenticated user dashboard         |
| `styles.css`           | All custom styles + CSS variables    |

---

## Redirection Flow

```
Login (index.html)
  ├── Submit form          → dashboard.html
  ├── "Create one" link    → register.html
  └── "Forgot password?"  → forgot-password.html

Register (register.html)
  ├── Submit form          → index.html (login)
  └── "Sign in" link       → index.html

Forgot Password (forgot-password.html)
  ├── Submit email         → reset-password.html (via success CTA)
  └── "Back to Login"      → index.html

Reset Password (reset-password.html)
  ├── Submit new password  → index.html (login)
  └── "Back to Login"      → index.html

Dashboard (dashboard.html)
  └── Logout button        → index.html
```

---

## Features

### All Pages
- Bootstrap 5 via CDN
- Bootstrap Icons via CDN
- Custom `styles.css` linked
- Fully responsive: 320px → 768px → 1366px → 1920px+
- Dark mode toggle (persisted via `localStorage`)
- Smooth transitions (0.3s ease) on all interactive elements

### Login (`index.html`)
- Centered Bootstrap-styled card
- Email + password inputs with labels
- Show / hide password toggle
- Remember me checkbox
- Client-side validation with custom error messages
- Loading spinner on submit → redirects to dashboard

### Register (`register.html`)
- Full Name, Email, Password, Confirm Password fields
- Real-time **password strength indicator** (Weak / Fair / Good / Strong)
- **Password requirements checklist** (length, uppercase, number, special char)
- Bootstrap validation states (is-valid / is-invalid)
- Terms & conditions checkbox
- Loading spinner on submit → redirects to login

### Forgot Password (`forgot-password.html`)
- Email input with validation
- Loading spinner on submit
- Animated **success state** replaces form after submission
- "Continue to Reset" CTA → reset-password.html

### Reset Password (`reset-password.html`)
- New Password + Confirm Password fields
- **Show / hide toggle** on both fields (Bootstrap Icons)
- Real-time password strength bar + requirements checklist
- Validation with custom error messages
- Loading spinner on submit → redirects to login

### Dashboard (`dashboard.html`)
- Sticky navbar with brand logo, user pill, dark mode toggle, logout button
- Welcome banner with gradient background
- 4 stat cards (Users, Sessions, Uptime, Alerts) with trend indicators
- Recent activity feed with colour-coded dots
- Quick action grid (Edit Profile, Change Password, Security, Notifications)
- Profile completion progress bar
- Security score progress bar

---

## Custom CSS Highlights (`styles.css`)

- CSS custom properties (variables) for light and dark themes
- Google Fonts: `Inter` (body) + `Poppins` (headings)
- Gradient background on auth pages
- Box shadows with hover elevation effect on all cards
- Gradient primary button with hover lift + glow
- Password strength segments with colour transitions
- Requirements checklist with animated check/cross icons
- Fully dark-mode aware (all colours switch via `[data-theme="dark"]`)

---

## GitHub Repository

```
https://github.com/YOURUSERNAME/html-authentication-poc
```

> Replace `YOURUSERNAME` with your actual GitHub username after pushing.

---

## Important Notes

- This is a **front-end only** authentication POC — no backend or real auth logic
- No CSS frameworks other than Bootstrap 5 are used
- No JavaScript frameworks or libraries are used
- Repository should be set to **public**
- All page redirections work via HTML form actions and anchor tags
- Dark mode preference is saved in `localStorage` and persists across pages
