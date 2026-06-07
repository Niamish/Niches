# Niches — Type a Niche, Get a Verdict

**Niches** is a sleek, terminal-inspired landing page for a niche opportunity scoring tool.  
It lets users type any market or niche idea and receive a modeled opportunity verdict based on demand, competition, monetization, and momentum.

The project is built as a single standalone HTML file with embedded CSS and JavaScript, making it easy to open, customize, and deploy.

---

## ✨ Project Description

Niches is designed like an **opportunity terminal** for founders, creators, marketers, and researchers.

Instead of guessing whether a niche is worth entering, the interface gives users a quick market verdict:

- Is the niche worth building?
- Is it too crowded?
- Can it be monetized?
- Is momentum increasing?
- What is the best wedge to enter?

The product experience feels like a command-line research dashboard, but with a premium editorial interface.

---

## 🚀 Main Features

### Terminal-Style Search Interface

Users can type a niche directly into the input terminal and receive instant suggestions or run a new analysis.

Example niches included in the demo:

- AI tools for therapists
- Spreadsheet automation for accountants
- Sourdough starters for beginners
- Van life electrical systems
- Notion templates for freelancers
- Pilates for postpartum recovery
- Mechanical keyboards
- Personal finance for Gen Z
- Dog training for reactive dogs
- Faceless YouTube automation

---

## 📊 Opportunity Verdict System

Each niche is scored across four key signals:

1. **Demand**
   - Measures whether people are actively looking for this niche.

2. **Competition**
   - Measures how crowded the market is.
   - Lower competition is better.

3. **Monetization**
   - Measures whether the audience is willing to pay.

4. **Momentum**
   - Measures whether the niche is trending upward or cooling down.

The final score uses the formula:

```txt
score = 0.32 × demand
      + 0.30 × monetization
      + 0.22 × momentum
      + 0.16 × (100 − competition)
```

---

## 🟢 Verdict Types

The app classifies opportunities into three verdict bands:

### GREEN

A strong opportunity.  
The niche has enough demand, monetization potential, and momentum to justify action.

### AMBER

A possible opportunity.  
The niche may be worth entering, but only with a clear wedge or focused sub-audience.

### RED

A risky or overcrowded niche.  
The market may be too saturated, too weak, or too difficult to monetize without a strong edge.

---

## 🧠 The Wedge System

For each niche, the app generates a strategic wedge, such as:

- Pick a sharper sub-audience.
- Own a specific price point.
- Reframe a crowded B2C topic as a B2B offer.
- Choose a geographic or language wedge.
- Focus on one measurable outcome.
- Build around a workflow competitors ignore.

This makes the app feel less like a generic score calculator and more like a strategic market research assistant.

---

## 💻 Tech Stack

This project uses:

- **HTML5**
- **CSS3**
- **Vanilla JavaScript**
- **Google Fonts**

No React, Vite, build tools, or external JavaScript libraries are required.

---

## 🎨 Design Style

The visual identity is:

- Dark terminal aesthetic
- Neon green opportunity accent
- Editorial typography
- Grid background
- Soft glow effects
- Grain texture overlay
- Minimal command-line interface
- Responsive mobile layout

Fonts used:

- **Fraunces**
- **Bricolage Grotesque**
- **JetBrains Mono**

---

## 📁 File Structure

```bash
niches.html
README.md
```

The project is fully contained inside `niches.html`.

It includes:

- HTML layout
- CSS styling
- JavaScript scoring logic
- Demo niche database
- Pricing panel
- Methodology panel
- Signup/tracking form UI

---

## ▶️ How to Run Locally

### Option 1: Open Directly

Double-click the file:

```bash
niches.html
```

It will open in your browser.

### Option 2: Use VS Code Live Server

1. Open the project folder in VS Code.
2. Install the **Live Server** extension.
3. Right-click `niches.html`.
4. Select **Open with Live Server**.

---

## 🌐 Deploy on GitHub Pages

GitHub Pages works best when the main file is named `index.html`.

### Steps

1. Rename:

```bash
niches.html
```

to:

```bash
index.html
```

2. Push the file to your GitHub repository.

3. Open your repository on GitHub.

4. Go to:

```bash
Settings → Pages
```

5. Under **Build and deployment**, select:

```bash
Deploy from a branch
```

6. Choose:

```bash
main / root
```

7. Save.

Your site will be available at:

```bash
https://your-username.github.io/your-repository-name/
```

---

## ⚠️ GitHub Pages Note

If GitHub Pages opens the README instead of the website, it usually means the repository does not have an `index.html` file in the root folder.

To fix this:

```bash
Rename niches.html to index.html
```

Then commit and push the change.

---

## ⚙️ Customization Guide

### Change the Brand Name

Search for:

```html
niches
```

Replace it with your own product name.

---

### Change the Main Heading

Search for:

```html
Stop guessing.
```

You can replace the hero text with your own positioning.

---

### Change the Accent Color

Inside the CSS `:root` block, edit:

```css
--accent: #cdf24a;
--go: #aef05a;
--watch: #ffc24b;
--hot: #ff6a52;
```

---

### Add More Demo Niches

Find the `SEEDS` array in the JavaScript:

```js
var SEEDS = [
  {
    t: "AI tools for therapists",
    m: [78, 64, 82, 88],
    w: "Win on compliance + clinical workflow...",
    s: ["~14k/mo", "$6.20", "Low", "6–9 mo"]
  }
];
```

Add new objects with:

- `t` — niche title
- `m` — metrics array
- `w` — wedge insight
- `s` — supporting stats

Metric format:

```js
[demand, competition, monetization, momentum]
```

---

### Edit Pricing Plans

Search for:

```js
showPricing()
```

Inside this function, you can change the plan names, pricing, and feature lists.

Current plans:

- Scout — Free
- Operator — $29/month
- Studio — $99/month

---

### Edit Methodology

Search for:

```js
showMethod()
```

This controls the scoring explanation and methodology panel.

---

### Edit Signup Form

Search for:

```js
showBrief()
```

This controls the free tracking/signup form.

Currently, the form is front-end only.  
To collect real emails, connect it to a backend, database, form service, or email marketing tool.

---

## 📱 Responsive Design

The page is responsive and includes mobile-friendly behavior:

- Scrollable body on smaller screens
- Mobile command chips
- Adjusted terminal height
- Responsive data strips
- Mobile-friendly pricing cards
- Simplified topbar

---

## ⌨️ Keyboard Shortcuts

The interface includes keyboard-style interactions:

```txt
↑ / ↓    Navigate options
Enter    Run selected option
Esc      Go back or clear search
Cmd/Ctrl + K    Return to search
Cmd/Ctrl + P    Open pricing
Cmd/Ctrl + M    Open methodology
Cmd/Ctrl + .    Surprise niche
Cmd/Ctrl + Enter    Start free tracking
```

---

## 🧪 Demo Disclaimer

The current version uses modeled demo data generated inside the browser.  
It does not yet connect to live search volume, CPC, competition, trend, or market research APIs.

For a production version, connect the scoring engine to real data sources such as:

- Search volume APIs
- Google Trends
- Keyword research tools
- Ad CPC data
- Social trend data
- Creator/content density analysis
- Revenue or affiliate market data

---

## 🔮 Future Improvements

Possible upgrades:

- Real backend
- User accounts
- Saved niche dashboard
- Live trend tracking
- Email alerts
- PDF report export
- CSV export
- Real-time keyword API integration
- AI-generated niche reports
- Competitor analysis
- Stripe payment integration
- Admin dashboard
- Authentication
- SEO landing pages for niche categories

---

## 🧾 License

This project can be used for personal, educational, or portfolio purposes.

For commercial use, customize the brand name, content, pricing, and data sources before launching publicly.

---

## 👤 Author

Created as a premium terminal-style market research concept.

---

## ⭐ Final Note

Niches is built around a simple but powerful promise:

> Stop guessing. Type a niche. Get a verdict.

It is ideal for anyone building a product around market research, creator tools, startup ideation, niche discovery, or opportunity analysis.
