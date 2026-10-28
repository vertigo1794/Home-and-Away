# Home & Away

**One helps you find a home. One takes you away.**

An Apple-style landing page that introduces two mobile apps built for the Mobile Application Development course (Semester 4): **Renly** and **Sky Saver**.

**Live site:** https://vertigo1794.github.io/Home-and-Away/

---

## The apps

### Renly
*Find your buyer. Faster.*

A property app for real-estate agents. Post listings, browse a co-broking marketplace, and chat with leads to book viewings, all in one place.

- Built by **Fakhrullah Bin Rassul**
- Flutter + Supabase
- Download: [latest Android APK](https://github.com/vertigo1794/renly/releases/latest/download/Renly.apk)
- Source: [vertigo1794/renly](https://github.com/vertigo1794/renly)

### Sky Saver
*The sky, in your pocket.*

A flight booking app. Search a route, pick a seat from a live seat map, and keep the boarding pass ready.

- Built by **Mohamad Hairi Bin Abdul Ahmad**
- React Native (Expo) + Supabase
- Download: [latest Android APK](https://github.com/Hairi19/skysaver/releases/latest/download/SkySaver.apk)
- Source: [Hairi19/skysaver](https://github.com/Hairi19/skysaver)

---

## What's on the page

| Section | What it does |
|---|---|
| **Intro** | 3D "clay" app icon that flips between the Renly and Sky Saver logos over a grid of icons, then zooms away as you scroll |
| **Get the highlights.** | Film gallery with each app's promo video. Press play to watch (with sound); when one film ends it slides to the next. Swipe, dots or arrows to switch |
| **About & stats** | Short story of the project with words that light up as you scroll, plus flip-board numbers |
| **Built to move.** | The Renly film plays inside the letters, then the camera dives through the "o" |
| **Team** | One card per developer with photo, short bio, a hover preview film and a direct APK link |
| **Renly / Sky Saver** | Per-app showcase: a real 3D iPhone (Emerald / Deep Blue Titanium) whose screen changes with each feature, a horizontal gallery, a bento "Highlights" grid and tech specs |
| **Explore** | Tap through each app's features, switch apps, drag to turn the 3D phone and change its finish (Emerald Titanium, Deep Blue Titanium, Graphite, Silver) |
| **Privacy** | How each app handles your data |
| **Compare** | Drag-to-compare slider and a side-by-side summary of both apps |
| **Scan. Install. Go.** | QR codes to download each APK straight to a phone |
| **FAQ** | Installing the APK, Android "unknown apps" warning, and more |

The page switches its colour theme as you scroll (dark, light, Renly, Sky Saver), works on phones, and respects the *reduce motion* accessibility setting.

---

## Built with

- Plain **HTML, CSS and JavaScript**, no build step or framework
- [GSAP](https://gsap.com/) + ScrollTrigger (from CDN) for scroll animations
- [Lenis](https://lenis.darkroom.engineering/) for smooth scrolling
- [Three.js](https://threejs.org/) for the 3D iPhone (desktop only; model: "iPhone 17 Pro" by Ranguel, CC BY 4.0)
- [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) for the download QR codes
- System font (SF Pro on Apple devices) with [Inter](https://fonts.google.com/specimen/Inter) as fallback
- Hosted on **GitHub Pages**

## Run it locally

```bash
git clone https://github.com/vertigo1794/Home-and-Away.git
cd Home-and-Away
python3 -m http.server 5173
```

Then open http://localhost:5173. Use a local server rather than opening `index.html` directly, so the 3D phone and films can load.
In Safari, films need a server that supports HTTP range requests (for example `npx serve`); Chrome is fine with the command above.

## Project structure

```
index.html   page content and sections
style.css    layout, themes and phone mockups
effects.css  styles for the scroll and pointer effects
main.js      film gallery, explorer, theme switching, smooth scroll
effects.js   scroll effects (masked text, zoom, galleries, flip numbers, QR)
phone3d.js   real 3D iPhone (three.js)
assets/      app screenshots, logos, films, team photos, 3D model
```

## Team

| Name | App |
|---|---|
| Fakhrullah Bin Rassul | Renly |
| Mohamad Hairi Bin Abdul Ahmad | Sky Saver |

---

Made for Mobile Application Development, Semester 4.
