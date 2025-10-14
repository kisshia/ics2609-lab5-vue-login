# ICS2609 Lab 5 – Vue 3 + Pinia + Bootstrap: Progressive Login with Public API (DummyJSON), Token (localStorage), and Router Guards

A simple Vue 3 login application that demonstrates authentication using the [DummyJSON](https://dummyjson.com) API.
The app allows users to log in with demo credentials and redirects them to a dashboard upon successful login.

---

## 🚀 Features

* Vue 3 + Vite project structure
* Login form with validation and loading state
* Authentication handled via Axios interceptors
* Token stored in Pinia store (`useAuthStore`)
* Route protection (redirects unauthenticated users)

---

## 🧩 Tech Stack

* [Vue 3](https://vuejs.org/)
* [Pinia](https://pinia.vuejs.org/)
* [Vue Router](https://router.vuejs.org/)
* [Axios](https://axios-http.com/)
* [Bootstrap 5](https://getbootstrap.com/)

---

## 🧰 Project Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/kisshia/ics2609-lab5-vue-login.git
cd ics2609-lab5-vue-login
```

### 2️⃣ Install dependencies

```bash
npm install
```

### 3️⃣ Run the development server

```bash
npm run dev
```

Then open the link shown in your terminal (usually `http://localhost:5173/`).

---

## 🔐 Sample Credentials

You can log in using the following DummyJSON test user:

| Username | Password     |
| -------- | ------------ |
| `emilys` | `emilyspass` |

---

## 🗁 Folder Structure

```
ics2609-lab5-vue-login/
├── .vscode/
├── node_modules/
├── public/
├── src/
│   ├── api/
│   │   └── http.js              # Axios instance with interceptors
│   ├── assets/                  # Static assets (images, icons, etc.)
│   ├── components/              # Reusable components
│   ├── pages/
│   │   ├── DashboardPage.vue    # Protected page after login
│   │   ├── HomePage.vue         # Public home page
│   │   └── LoginPage.vue        # Login form
│   ├── router/
│   │   └── index.js             # Vue Router setup and guards
│   ├── stores/
│   │   └── auth.js              # Pinia authentication store
│   ├── App.vue                  # Root Vue component
│   ├── main.js                  # Application entry point
│   └── style.css                # Custom global styles
├── .gitignore
├── index.html
├── package-lock.json
├── package.json
├── README.md
└── vite.config.js
```

---

## 🧠 Notes

* API Base URL: `https://dummyjson.com`
* When login fails, an error message (“Invalid credentials”) will appear below the form.
* Logging out clears the stored token and user data from Pinia.
* You can verify successful login using **DevTools → Network → /auth/login** and check for the **Authorization header** when calling `/auth/me`.
