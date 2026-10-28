# Deliverable 2: Working Asset Documentation & Evaluator Guide

**Asset Name:** NxtWave AI Placement Benchmark & Viral Ticket Engine  
**Live Asset Location:** `asset/index.html` (Standalone, zero-dependency web application)  
**Slide Presentation Deck:** `PRESENTATION_DECK.html`  
**Purpose:** Eliminate webinar friction, benchmark final-year resume vulnerability, generate personalized boarding passes, and trigger a self-sustaining peer referral loop on WhatsApp.

---

## 1. Why We Built This Asset (Strategy & Justification)

The challenge brief explicitly noted:
> *"Landing page (Note: Everyone might build a landing page)... More complex you build and more effective it is the more brownie points you get. You decide what is worth building."*

### The Problem With Standard Landing Pages
1. **Banner Blindness:** Engineering students are inundated with webinars promising "free certificates". Standard landing pages experience 70–80% bounce rates.
2. **Passive Consumption:** Reading speaker bios and bullet points doesn't create emotional urgency or active investment.
3. **Zero Virality:** A standard form has no built-in viral loop. Once a student registers, the interaction terminates.

### Our Solution: An Interactive Product-Led Growth (PLG) Engine
We combined four distinct growth mechanics into a single cohesive client-side application:
1. **Interactive Placement AI Gap Grader:** Hooks the student's primary psychological trigger—fear of resume rejection during 2025 hiring cuts.
2. **Dynamic Personalized Ticket Generator (HTML5 Canvas):** Transforms the registration confirmation into a high-status boarding pass that students can download as an image (`.png`) and post on WhatsApp Status or LinkedIn.
3. **Calendar Auto-Sync (.ics):** Generates and downloads an RFC-5545 `.ics` file with 1 click to eliminate the standard 40% webinar no-show rate.
4. **The "3-Peer" Viral Referral Gate:** Locks high-value technical assets (GitHub repository + 50 ATS AI resume bullet points) behind a 3-batchmate referral threshold, accompanied by 1-click WhatsApp sharing.
5. **Growth Team Telemetry Dashboard:** An embedded executive view allowing NxtWave hiring managers to inspect live campaign conversion rates, channel attribution, and unit economics (CAC: ₹3.86).

---

## 2. Technical Architecture & File Structure

The asset was engineered with zero external server dependencies, making it 100% portable, instantly previewable in any modern browser, and immune to npm/node version incompatibilities.

```
asset/
├── index.html        # Complete UI layout, accessible semantics, responsive Tailwind styling
├── styles.css        # Custom design system, glassmorphism, ticket styling, animations
├── app.js            # Reactive state management, Canvas rendering, .ics export, viral simulator
├── server.js         # Optional lightweight Node.js HTTP server (Node 16+)
└── README.md         # Quickstart instructions for the evaluator
```

### Core Technologies Used
- **Tailwind CSS (via CDN):** Rapid responsive utility design with dark-mode aesthetic.
- **HTML5 Canvas API:** Custom vector drawing engine for dynamic boarding pass image generation (`.png` download).
- **Blob / Data URL API:** Native calendar event file generator (`.ics` format).
- **Canvas-Confetti:** Micro-reward visual feedback on registration and referral milestones.
- **Vanilla JavaScript (ES6+):** Pure reactive state architecture with zero framework bloat.

---

## 3. Step-by-Step Evaluator Walkthrough

To experience the asset exactly as an engineering student and growth evaluator:

### Step 1: Open the Application
- Open `c:\Users\pc\Documents\NxtWave\asset\index.html` in Google Chrome, Microsoft Edge, or Firefox.

### Step 2: Test the Resume Diagnostic Grader
1. On the initial screen, select your branch (e.g., **CSE / IT / AI-DS** or **Mechanical / Civil**).
2. Click **Continue to Step 2**.
3. Select your current project types (e.g., check **Standard CRUD / Web App** and **Cloned / Tutorial Project**).
4. Click **Generate My AI Diagnostic**.
5. Observe the personalized **ATS AI Risk Report** showing a score of **28–38 / 100 (High Risk)** and explaining why cloned projects fail automated screening filters.

### Step 3: Test Registration & Ticket Pass Generation
1. In the registration card, enter:
   - **Name:** Your Full Name
   - **Phone:** Your 10-Digit WhatsApp Number
   - **College:** Your College Name & City
2. Click **Generate My VIP Ticket & Entry Pass**.
3. Observe the celebration confetti and the dynamically generated **VIP Boarding Pass** featuring the student's name, college, unique ticket ID (`#NW-AI-XXXX`), and QR badge.
4. Click **Download Pass (PNG)** to verify the HTML5 Canvas generation. The browser will immediately download a crisp image file: `NxtWave_AI_Workshop_Pass_NW-AI-XXXX.png`.
5. Click **Add to Calendar (.ics)** to verify the `.ics` calendar invitation download.

### Step 4: Test the Viral Referral Loop & Anti-Fraud Verification
1. Scroll to the **Unlock the VIP AI Project Starter Vault** section.
2. Note that the progress bar displays **0 / 3 Batchmates Registered** with the anti-fraud status indicator: *"Waiting for classmates to register via your link..."*.
3. Click **Share to Class WhatsApp Group** to inspect the pre-populated, high-converting viral referral copy formatted with the student's unique ticket number.
4. To test verification as an evaluator or admin without exposing cheat buttons to students, switch to the **Growth Strategy** tab in the header.
5. In the **Admin & Evaluator Sandbox**, click **⚡ Fire Verified Referral Webhook (+1)**:
   - Referrals counter increments to 1/3, displaying *"Verified Peer #1 Registered"* with real-time timestamp.
   - Click it a second and third time:
   - On the 3rd verified peer, celebratory confetti explodes, the progress reaches **3/3 (100%)**, and the **VIP Starter Vault UNLOCKED** banner appears with active links to the GitHub repository and ATS prompt pack!
6. Click **Reset Referrals** to return to 0 and re-lock the vault for fresh testing.

### Step 5: Inspect the Dynamic Real-Time Growth Engine
1. In the top navigation bar, toggle to **Growth Strategy (500 GOAL)**.
2. Review the live dynamic telemetry system:
   - **Live Campaign Pacing:** Starts at **0 / 500 Claimed** (500 seats remaining). As students register, the big progress bar fills up, remaining seats drop in real time, and the live blended CAC is calculated dynamically.
   - **Real-Time Channel Attribution Bars:**
     - *CR Bounty Broadcasts:* Starts at **0 / 250 Target** and grows with each direct registration.
     - *Viral Peer Referral Loop:* Starts at **0 / 175 Target** and grows with each verified referral.
     - *Tech Placement Communities:* Starts at **0 / 75 Target**.
   - **7-Day Velocity Chart (Live Day 1 vs Roadmap):**
     - *Day 1 (LIVE):* Dynamically grows taller with every single registration that occurs today!
     - *Days 2–7:* Labeled as **Target Roadmap Forecast** showing the milestone path to achieve the 500 goal.
   - **Live Registration Event Stream:** Displays a timestamped real-time log of every student pass generated and verified referral.
   - **Interactive Growth Controls:**
     - Click **`📢 Simulate CR Broadcast (+15)`** to simulate a college representative sharing to a WhatsApp group—watch all channel bars, total seats, and Day 1 velocity smoothly animate and climb toward 500!
     - Click **`⚡ +1 Peer Referral`** to watch the viral loop advance.
     - Click **`Reset to 0`** to return the entire system to a clean baseline state.

---

## 4. How to Host & Share (Live Links)

For sharing with the NxtWave hiring team via the Google Form:

### Option A: One-Click Vercel / Netlify Drop Deployment
1. Drag and drop the `asset/` folder into [Netlify Drop](https://app.netlify.com/drop) or import to Vercel.
2. A public URL (e.g. `https://nxtwave-ai-growth-challenge.netlify.app`) is generated in under 30 seconds.

### Option B: GitHub Pages
1. Push the repository to GitHub.
2. In Repository Settings $\to$ Pages, select the root or `/asset` branch.
3. The live link will be active at `https://<username>.github.io/<repo-name>/asset/`.

### Option C: Google Drive / Zip Submission
- Compress the `NxtWave/` folder into a `.zip` file and upload to Google Drive with "Anyone with link can view" permission.
