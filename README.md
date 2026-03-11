# BookMyShow Clone

A full-stack clone of [BookMyShow](https://www.bookmyshow.com/) — India's largest ticket booking platform for movies, plays, and live events. Browse movies, view details, and make payments with Razorpay integration.

**Live Demo:** [bookmyshow-clone-rust.vercel.app](https://bookmyshow-clone-rust.vercel.app)

---

## Features

- **Movie Discovery** — Browse popular, top-rated, and upcoming movies via TMDB API
- **Movie Details** — View synopsis, cast & crew, similar movies, and recommendations
- **Plays & Events** — Browse live events and plays with filters (date, language)
- **Razorpay Payments** — Secure payment flow for buying/renting movies (test mode)
- **Responsive UI** — Mobile-friendly design with Tailwind CSS
- **Hero Carousel** — Featured movies with slick carousel
- **Premiers Section** — New releases every Friday
- **Online Stream Events** — Discover streaming events

---

## Tech Stack

| Category | Technologies |
|----------|--------------|
| **Frontend** | React 19, React Router v7 |
| **Styling** | Tailwind CSS, Bootstrap |
| **UI Components** | Headless UI, React Slick |
| **HTTP** | Axios |
| **Payments** | Razorpay Checkout |
| **Data** | TMDB API (The Movie Database) |

---

## Project Structure

```
bookmyshow-clone/
├── public/
│   └── index.html          # Entry HTML, Razorpay script
├── src/
│   ├── components/         # Reusable components
│   │   ├── Cast/           # Cast & crew display
│   │   ├── Entertainment/  # Entertainment cards
│   │   ├── HeroCarousel/   # Hero slider with arrows
│   │   ├── MovieHero/      # Movie hero section
│   │   ├── Navbar/         # Navigation
│   │   ├── PaymentModal/   # Razorpay payment modal
│   │   ├── PlayFilter/     # Event filters
│   │   ├── Poster/         # Movie/event poster
│   │   └── PosterSlider/   # Poster carousel
│   ├── Context/
│   │   └── Movie.Context.jsx  # Global movie state
│   ├── layouts/
│   │   ├── Default.layout.jsx  # Default page layout
│   │   └── Movie.layout.jsx    # Movie page layout
│   ├── pages/
│   │   ├── Home.page.jsx       # Homepage
│   │   ├── Movie.page.jsx      # Movie detail page
│   │   └── Play.page.jsx       # Plays & events
│   ├── App.js
│   └── index.js
├── .env.example             # Environment variables template
├── tailwind.config.js
└── package.json
```

---

## Getting Started

### Prerequisites

- Node.js 18+ and npm

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/ritesh-1912/bookmyshow-clone.git
   cd bookmyshow-clone
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   Edit `.env` and add your keys:
   - `TMDB_REACT_API_KEY` — Get from [TMDB API](https://www.themoviedb.org/settings/api)
   - `REACT_APP_RAZORPAY_KEY_ID` — Get from [Razorpay Dashboard](https://dashboard.razorpay.com/app/keys)
   - `RAZORPAY_KEY_SECRET` — Razorpay secret (for server-side use)
   - `REACT_APP_API_URL` — (Optional) Backend API URL if using custom backend

4. **Start the development server**
   ```bash
   npm start
   ```
   Opens at [http://localhost:3000](http://localhost:3000)

---

## Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `TMDB_REACT_API_KEY` | TMDB API key for movie data | Yes |
| `REACT_APP_RAZORPAY_KEY_ID` | Razorpay Key ID (public, for checkout) | Yes |
| `RAZORPAY_KEY_SECRET` | Razorpay secret (server-side only) | For payment verification |
| `REACT_APP_API_URL` | Custom backend API base URL | No |

> ⚠️ **Security:** Never commit `.env` to version control. It contains secrets and is listed in `.gitignore`.

---

## Deployment

### Frontend (Vercel)
- **Dashboard:** [vercel.com/ritesh-gargs-projects/bookmyshow-clone](https://vercel.com/ritesh-gargs-projects/bookmyshow-clone)
- Add environment variables in Vercel project settings

### Backend (Render)
- **Dashboard:** [dashboard.render.com](https://dashboard.render.com/web/srv-cu6cgr56l47c73bvv2e0)

---

## Available Scripts

| Command | Description |
|---------|-------------|
| `npm start` | Run development server |
| `npm run build` | Create production build |
| `npm test` | Run tests |

---

## API References

- [TMDB API](https://developers.themoviedb.org/3) — Movie and TV data
- [Razorpay Docs](https://razorpay.com/docs/) — Payment integration

---

## License

This project is for educational purposes. BookMyShow is a trademark of Bigtree Entertainment Pvt. Ltd.
