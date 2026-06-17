# 🎆 Celebrate Poland — Interactive Event Agenda

An interactive, mobile-friendly event agenda web app for **Celebrate Poland**, Poland, Ohio's annual 4th of July festival. Built with plain HTML, Bootstrap 5, and vanilla JavaScript — no build tools, no dependencies to install.

**Live Demo:** `https://YOUR_USERNAME.github.io/celebrate_poland_agenda/`

---

## 📋 Features

- **Day-by-day navigation** — switch between Friday and Saturday with a single click
- **Category filters** — filter events by Music, Food, Kids, Arts, Community, Parade, or Fireworks
- **Event cards** — each event displays its time, location, description, and color-coded category tags
- **Highlighted events** — featured events like the concert and fireworks are visually elevated
- **Free admission badges** — clearly marks which events are free to attend
- **Fully responsive** — works on desktop, tablet, and mobile
- **No backend required** — a single `index.html` file, hostable anywhere

---

## 🗂️ Project Structure

```
celebrate_poland_agenda/
├── index.html              # The entire app — HTML, CSS, and JS in one file
├── README.md               # You're reading it
└── .github/
    └── workflows/
        └── deploy.yml      # GitHub Actions workflow for auto-deploy to GitHub Pages
```

---

## 🚀 Deployment

This project uses **GitHub Pages** for free static hosting with automatic deployment via GitHub Actions.

### First-Time Setup

1. **Create a GitHub repository** at [github.com/new](https://github.com/new) — name it `celebrate_poland_agenda`, leave it empty (no README).

2. **Push your local code:**
   ```bash
   cd ~/Repos/celebrate_poland_agenda
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOUR_USERNAME/celebrate_poland_agenda.git
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to your repo on GitHub → **Settings → Pages**
   - Under **Source**, select **"GitHub Actions"**
   - Save

4. **Your site will be live at:**
   ```
   https://YOUR_USERNAME.github.io/celebrate_poland_agenda/
   ```
   The first deploy takes about 30–60 seconds after your push.

### Ongoing Deploys

Every push to `main` triggers the GitHub Action and automatically redeploys the site. No manual steps needed.

---

## ✏️ Updating the Schedule

All event data lives directly in `index.html` as HTML. To add, edit, or remove events:

1. Find the relevant day's section (`id="day-friday"` or `id="day-saturday"`)
2. Copy an existing `.event-card` block and update the content
3. Set the `data-cat` attribute to one or more categories (space-separated) so filters work correctly:

```html
<div class="event-card" data-cat="music community">
  ...
</div>
```

**Available categories:** `music` · `food` · `kids` · `arts` · `community` · `parade` · `fireworks` · `history`

### Adding a Highlighted/Featured Event

Add the `highlight` class to make an event card stand out with a gold border:

```html
<div class="event-card highlight" data-cat="fireworks">
```

---

## 📅 Schedule Source

The schedule is based on the **2025 Celebrate Poland event** (June 27–28, 2025), mapped to the confirmed **2026 dates of June 26–27**. Always verify times and details at the official site before the event:

**[celebratepolandohio.com](https://www.celebratepolandohio.com)**

> ⚠️ Event details (band names, exact times, new activities) are subject to change. Update `index.html` once the official 2026 schedule is released.

---

## 🛠️ Built With

| Technology | Purpose |
|---|---|
| HTML5 | Structure and content |
| CSS3 | Custom styling and theming |
| [Bootstrap 5.3](https://getbootstrap.com/) | Responsive layout utilities |
| [Font Awesome 6.5](https://fontawesome.com/) | Icons |
| Vanilla JavaScript | Day switching and category filtering |
| GitHub Pages | Free static hosting |
| GitHub Actions | Automatic CI/CD deployment |

---

## 📍 Event Info

| | |
|---|---|
| **Event** | Celebrate Poland |
| **Location** | Village Hall · 308 S. Main St · Poland, OH 44514 |
| **Dates** | June 26–27, 2026 |
| **Admission** | FREE |
| **Website** | [celebratepolandohio.com](https://www.celebratepolandohio.com) |
