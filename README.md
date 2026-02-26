# 🎉 Local Events App

[![Node.js](https://img.shields.io/badge/Node.js-5FA04E?logo=nodedotjs&logoColor=fff)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-000?logo=express&logoColor=fff)](https://expressjs.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=fff)](https://www.postgresql.org/)
[![Prisma](https://img.shields.io/badge/Prisma-2D3748?logo=prisma&logoColor=fff)](https://www.prisma.io/)

O aplicație web modernă pentru gestionarea evenimentelor locale, construită cu Node.js, Express și PostgreSQL.

## 🎯 Descriere

Platformă web care facilitează organizarea și descoperirea evenimentelor locale. Utilizatorii pot crea conturi, publica evenimente, vizualiza detalii și gestiona propriile evenimente într-o interfață intuitivă și modernă, cu accent pe securitate și performanță.

---

## ✨ Funcționalități

- 🔐 **Autentificare securizată** - Înregistrare, login cu JWT, hashare parole
- 📅 **CRUD Evenimente** - Creare, editare, ștergere și vizualizare evenimente
- 🖼️ **Upload imagini** - Suport pentru imagini evenimente
- 👤 **Profile utilizator** - Gestionare cont și schimbare parolă
- 🎨 **Design responsive** - Interfață modernă pentru mobile și desktop
- 🔒 **Securitate** - Rate limiting, Helmet.js, validare input cu Zod

---

## 🛠️ Tehnologii

### Backend
- **[Node.js](https://nodejs.org/)** - Runtime JavaScript
- **[Express.js](https://expressjs.com/)** ^5.1.0 - Web framework
- **[Prisma ORM](https://www.prisma.io/)** ^5.22.0 - Database ORM
- **[PostgreSQL](https://www.postgresql.org/)** - Bază de date
- **[JWT](https://jwt.io/)** - Autentificare cu token-uri
- **[bcrypt](https://www.npmjs.com/package/bcrypt)** - Hashare parole

### Frontend
- **[EJS](https://ejs.co/)** - Template engine
- **HTML5 / CSS3** - Markup și styling
- **JavaScript** - Interactivitate client-side

### Securitate & Validare
- **[Helmet.js](https://helmetjs.github.io/)** - Securitate HTTP headers
- **[CORS](https://www.npmjs.com/package/cors)** - Cross-Origin Resource Sharing
- **[express-rate-limit](https://www.npmjs.com/package/express-rate-limit)** - Rate limiting
- **[Zod](https://zod.dev/)** - Schema validation

### Tools & Utilities
- **[Multer](https://www.npmjs.com/package/multer)** - File upload handling
- **[cookie-parser](https://www.npmjs.com/package/cookie-parser)** - Cookie parsing
- **[dotenv](https://www.npmjs.com/package/dotenv)** - Environment variables
- **[method-override](https://www.npmjs.com/package/method-override)** - HTTP method override
- **[nodemon](https://nodemon.io/)** - Development auto-reload

---

## 🚀 Instalare Locală

### Prerequisite
- **Node.js** >= 18.x
- **npm** >= 9.x
- **PostgreSQL** database (local sau cloud - Neon recomandat)

### 1. Clonează repository-ul

```bash
git clone https://github.com/USERNAME/local-events-app.git
cd local-events-app
```

### 2. Instalează dependențele

```bash
npm install
```

### 3. Configurează variabilele de mediu

Creează un fișier `.env` bazat pe `.env.example` și completează cu datele tale.

### 4. Configurează baza de date

```bash
# Creează/actualizează schema în database
npx prisma db push

# SAU creează migration (recomandat pentru producție)
npx prisma migrate dev --name init
```

### 5. Generează Prisma Client

```bash
npm run generate
```

### 6. Pornește serverul

```bash
# Development mode (cu nodemon)
npm run dev

# Production mode
npm start
```

## 🛣️ Rute Principale

- `/` - Pagina principală (redirect la `/events`)
- `/login`, `/signup`, `/logout` - Autentificare
- `/events` - Lista evenimente
- `/events/:id` - Detalii eveniment
- `/events/new` - Creare eveniment nou (autentificat)
- `/profile` - Profil utilizator (autentificat)

---

Poți vizualiza un demo [aici](https://local-events.vercel.app/)
