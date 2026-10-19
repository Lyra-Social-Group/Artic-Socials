# ArtcDragon - Official Social Links

A high-performance, single-page custom link-in-bio web application built for **ArtcDragon**. Engineered with **Vue 3** and **Vite**, featuring modern glassmorphism aesthetic accents, smooth micro-interactions, dark mode styling, and zero external CSS runtime dependencies.

---

## 🌐 Live Site & Service Status

If the service is operational, the official live deployment is hosted at:
**[https://artic.lyrafoxwood.net/](https://artic.lyrafoxwood.net/)**

[![Better Stack Badge](https://incidents.betterstack.com/status-badges/v1/monitor/3153h.svg)](https://incidents.betterstack.com/?utm_source=status_badge)

### 🚨 Service Outage & Downtime Protocol

If `artic.lyrafoxwood.net` is unreachable or offline:

1. **Check Live Status Badge**: Click the Better Stack status badge above to check real-time system health and active incident reports.
2. **Direct Social Fallbacks**: Access core creator channels directly during web routing disruptions:
   * **Twitch**: [twitch.tv/artcdragon](https://twitch.tv/artcdragon/home)
   * **YouTube**: [youtube.com/@Artcdrgn](https://www.youtube.com/@Artcdrgn)
   * **Discord**: [The Artc Palace](https://discord.com/invite/sSW7C82aGv)
3. **Report Infrastructure Incidents**: Notify system administration at **Lyra Social Group LLC** via `Contactme@lyrafoxwood.app` or through `status.lyrasocialgroup.tech`.

---

## Key Features & Architecture

* **Pure Scoped CSS Engine**: Built entirely without external CSS frameworks or heavy utility toolchains to ensure minimal bundle size, zero build-step styling conflicts, and instant first-contentful-paint (FCP).
* **Glassmorphism Design System**: Dynamic background ambient glows with high-performance CSS blur filters, optimized for both high-DPI desktop screens and mobile viewports.
* **Interactive Link Cards**: Brand-specific accent hovers, live status badges, and external destination indicators.
* **Dynamic Year Generation**: Automatically updates copyright year strings using Vue reactive getters without manual maintenance.
* **Cloudflare Edge Deployment**: Pre-configured for automated continuous integration and static edge distribution via Cloudflare Pages.

---

## Technical Stack

* **Framework**: [Vue 3](https://vuejs.org/) (Composition API via `<script setup>`)
* **Build Engine**: [Vite](https://vitejs.dev/)
* **Style Engine**: Pure CSS3 (Scoped Variables & Flexbox Layouts)
* **Hosting Infrastructure**: Cloudflare Pages / Edge Network

---

## Project Structure

Artic-Socials/
├── dist/                   # Production build artifact
├── src/
│   ├── App.vue             # Core component & link configurations
│   ├── main.js             # Vue application initialization
│   └── style.css           # Global resets and CSS variables
├── index.html              # HTML5 entrypoint & meta tags
├── package.json            # Project manifest & build scripts
├── vite.config.js          # Vite build configuration
└── README.md               # Documentation

---

## Deployment Configuration

This repository is configured for automated edge deployment:

| Parameter | Configuration |
| :--- | :--- |
| **Framework Preset** | `Vue.js` / `Vite` |
| **Build Command** | `npm run build` |
| **Build Output Directory** | `dist` |
| **Production Domain** | `artic.lyrafoxwood.net` |
| **Node.js Environment** | `18.x` or higher |

---

## License & Ownership

Software built, maintained, and licensed by **Lyra Social Group LLC**.  
Designed with ❤️ by [Lyra Foxwood](https://lyrafoxwood.com).

&copy; 2026 ArtcDragon & Lyra Social Group LLC. All rights reserved.
