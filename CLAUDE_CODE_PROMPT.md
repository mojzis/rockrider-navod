# Claude Code Prompt — Grandma's E-Bike Guide (GitHub Pages)

## Project Goal

Build a **single-page static web app** (pure HTML + CSS + JS, no build tools needed) that can be deployed as a **GitHub Page**. The app is a friendly, interactive guide for an elderly woman who just got her first electric bike — the **Rockrider E-ACTV 500**. She forgets how to operate it and needs an always-available, easy-to-use reference she can open on her phone or tablet.

---

## Audience & Design Principles

- **Primary user**: An elderly grandmother, possibly unfamiliar with technology
- **Device**: Smartphone or tablet, likely held in portrait orientation
- **Tone**: Warm, patient, encouraging — like a kind grandchild explaining step by step
- **Design**: Large text, big touch targets (min 48px), high contrast, no clutter
- **Language**: Simple plain English. No jargon. Short sentences. Active voice.
- **Aesthetic**: Friendly and clear — think large icons, soft greens/teals (matching the bike's color), clean white cards, rounded corners. Inspired by a "how-to recipe card" style — big steps, clear numbers.

---

## Technical Requirements

- **Single file**: Everything in one `index.html` file (inline CSS + JS). Must work offline after first load.
- **No frameworks, no npm, no build step** — just plain HTML/CSS/JS that GitHub Pages serves directly.
- **Responsive**: Works on 375px (iPhone SE) up to 768px (iPad). On desktop, content centers with max-width ~600px.
- **Accessible**: Good contrast ratios, readable font sizes (body text ≥ 18px, headings ≥ 24px).

---

## App Structure

### Navigation
A sticky bottom navigation bar with large icon+label tabs for each section:
1. 🔋 **Battery** 
2. 💡 **Lights**
3. ⚡ **Assistance**
4. 🚶 **Walk Mode**
5. 🔌 **Charging**
6. ⚠️ **Troubleshooting**

Only one section is visible at a time. Active tab is highlighted.

### Each Section
Each section is a set of **step cards**. Each card has:
- A big number circle (1, 2, 3…)
- An emoji icon relevant to the action
- A short **bold title** (≤ 6 words)
- 1–2 sentences of plain explanation
- Optional: a "⚠️ Remember:" callout in a soft yellow box for important warnings

---

## Content Per Section

Use the content below verbatim as the source of truth. Write it in the friendliest, simplest way possible for each card.

---

### 1. 🔋 Battery — "Turning the bike on and off"

**Turning ON:**
1. Make sure the battery is inserted (it clicks in)
2. Press and hold the **ON/OFF button** on the screen until it lights up
3. The screen will show your speed, battery level, and assistance mode — you're ready!

**Turning OFF:**
1. Press and hold the **ON/OFF button** until the screen goes dark
2. ⚠️ Remember: Always remove the key from the battery lock before riding

**Inserting the battery:**
1. Before inserting, check nothing is already in the battery slot
2. Slide the battery into its housing until it clicks
3. Always remove the key from the lock before you ride

**Removing the battery:**
1. Turn the key — the battery will move slightly so you can grip it
2. Pull the pull tab if it does not move on its own

---

### 2. 💡 Lights — "Turning lights on and off"

**To turn lights ON or OFF:**
1. Find the **Display «−» button** (the down arrow on the screen unit)
2. Press and **hold it for 3 seconds**
3. The screen will show **"LIGHTS ON"** or **"LIGHTS OFF"**

⚠️ Remember: In rain, fog, or at night always turn the lights on and slow down.

---

### 3. ⚡ Assistance — "Choosing how much help you get"

**What is assistance?**
The bike has a motor that helps you pedal. You can choose how much help you want:
- **Mode 0** — No motor help (just your own legs)
- **Mode 1** — A little help (+70%) — good for flat roads ✅ *starts here*
- **Mode 2** — More help (+150%) — good for gentle hills
- **Mode 3** — A lot of help (+220%) — good for steeper hills
- **Mode 4** — Maximum help (+280%) — use when tired or on big hills

**Tip:** The motor only helps when you are pedalling. It stops automatically above 25 km/h.

**To increase assistance (go up):**
1. Press the **«+» button** on the handlebar remote (the up arrow)
2. Each press moves up one mode (1 → 2 → 3 → 4)

**To decrease assistance (go down):**
1. Press the **«−» button** on the handlebar remote (the down arrow)
2. Each press moves down one mode (4 → 3 → 2 → 1 → 0)

⚠️ Remember: When the battery is getting low, switch to a **lower mode** (1 or 2) to save energy.

---

### 4. 🚶 Walk Mode — "Push the bike uphill without effort"

**What is Walk Mode?**
Walk Mode makes the motor gently push the bike forward while you walk beside it — perfect for pushing it up a ramp or steep path without tiring yourself.

**To activate Walk Mode:**
1. Make sure the bike is ON
2. Press and **hold the «+» button** on the handlebar remote for 3 seconds
3. The screen will show **"WALK MODE"**
4. The bike will move forward slowly (max 6 km/h) — walk alongside it

⚠️ Remember: Only use Walk Mode when you are **walking beside the bike**, not sitting on it.

---

### 5. 🔌 Charging — "How to charge the battery"

**How to charge:**
1. Remove the battery from the bike (or charge it while still on the bike)
2. Open the charging port cover on the battery
3. Plug in **only the charger that came with the bike**
4. A **red LED** means it is charging
5. A **green LED** means it is fully charged — unplug it

**How long does it take?**
A full charge from 0% to 100% takes about **7 hours**.

**Charging tips:**
- Charge indoors only, in a dry place
- Charge at temperatures between 10°C and 40°C
- Never charge near water or flammable materials
- Charge the battery at least once every **6 months** even if you haven't ridden

⚠️ Remember: Never use a different charger. Using the wrong charger can cause a fire.

**Battery storage tips:**
- Store the battery between 30% and 60% charge
- Keep it in a cool, dry place (10°C–25°C), away from direct sunlight
- If storing for a long time, check the charge every 3 months

---

### 6. ⚠️ Troubleshooting — "Something seems wrong?"

Present these as expandable accordion cards (tap to expand).

**The motor isn't helping me**
Possible reasons:
- You are going faster than 25 km/h — the motor stops automatically at that speed
- You are not pedalling — the motor only works when you pedal
- The battery is very low — charge the battery
- Assistance mode is set to 0 — press «+» to choose mode 1, 2, 3 or 4
- The screen is off — press ON/OFF to turn it back on

**The battery seems to drain quickly**
- Cold weather reduces battery life — this is normal in winter
- Using high assistance modes (3 or 4) uses more battery
- Going uphill uses more battery
- Switch to mode 1 or 2 on flat ground to save battery
- Make sure tyres are inflated to 2–5 bar

**I see an error on the screen (e.g. ERROR ENGINE 042)**
- Error 10 or 12: Battery is low or empty — charge the battery
- Error 44: Motor is too hot — stop and rest, pedal gently with low assistance
- Any other error: Turn the bike off and on again. If it persists, contact a Decathlon workshop.

**The brakes feel weak**
- New brake pads need "bedding in" — apply each brake gently about 10 times, slowing from ~25 km/h to 5 km/h
- In wet weather, braking distances are always longer — slow down earlier

**I need help**
Visit: [Decathlon Support](https://www.support.decathlon.com) or go to your nearest Decathlon store.

---

## Additional UX Details

- Add a friendly **welcome screen / hero** at the top (before the tabs) with the bike name, a greeting like *"Hello! 👋 Tap a topic below to get started."*
- The **active section** smoothly scrolls into view
- Each step card has a subtle entrance animation (fade + slide up) when the section appears
- On the Troubleshooting section, items are **accordion-style** (collapsed by default, tap to expand)
- Add a small **"Back to top ↑"** button that appears after scrolling down
- Footer: *"Made with ❤️ for Grandma · Based on the official Rockrider E-ACTV 500 manual"*

---

## File Output

Produce a single file: `index.html`

It must be deployable to GitHub Pages by:
1. Creating a new GitHub repository
2. Putting `index.html` in the root
3. Enabling GitHub Pages (Settings → Pages → Deploy from branch: main / root)

No other files needed.
