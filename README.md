# NxtWave Growth Intern Challenge – Working Asset & Telemetry Engine

[![Production Status](https://img.shields.io/badge/Vercel-Live_Deployment-success?style=for-the-badge&logo=vercel)](https://nxtwave-growth-intern-xi.vercel.app/)
[![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github)](https://github.com/jashwanth15/NxtWave-Growth-Intern)
[![Challenge](https://img.shields.io/badge/Challenge-NxtWave_Growth_Intern-0b66c2?style=for-the-badge)](https://github.com/jashwanth15/NxtWave-Growth-Intern)

A high-converting, product-led registration and peer-referral web application engineered for NxtWave's free live workshop: **“Build Your First AI Project in 60 Minutes”**.

👉 **Live Production URL:** [https://nxtwave-growth-intern-xi.vercel.app/](https://nxtwave-growth-intern-xi.vercel.app/)  
👉 **GitHub Repository:** [https://github.com/jashwanth15/NxtWave-Growth-Intern](https://github.com/jashwanth15/NxtWave-Growth-Intern)

---

## 🌟 Overview

This working asset replaces low-converting static registration forms with an interactive, multi-stage enrollment and viral referral engine. It guides final-year engineering students through a 45-second placement readiness diagnostic, dynamically generates an authentic high-resolution ticket pass via client-side HTML5 Canvas, and powers a gamified peer-referral loop to unlock a curated starter vault.

The application also includes a built-in Growth Operations Telemetry dashboard allowing administrators to monitor registrations, channel distribution, and campaign velocity in real time.

---

## 🚀 Key Features

### 1. 45-Second Placement Diagnostic
- Interactive assessment capturing student branch (CSE/IT, ECE, Mechanical, Civil, etc.) and current project experience.
- Provides an objective resume audit benchmarked against 2025 tech hiring and automated ATS filter standards.

### 2. Personalized ATS AI Gap Report
- Dynamic visual scoring that exposes candidate resume vulnerability (e.g. lack of deployed GenAI experience).
- Positions the live 60-minute hands-on workshop as the direct solution to build and deploy a verifiable project.

### 3. Client-Side Canvas Ticket Engine
- Instant client-side generation of an authentic VIP workshop pass featuring attendee name, college, branch, QR code, and ticket ID (`#NW-AI-XXXX`).
- One-click high-resolution PNG download rendered directly in the browser (zero external image API dependencies).
- One-click `.ics` calendar file export compatible with Google Calendar, Apple Calendar, and Outlook.

### 4. Viral Peer Referral Gate ($K = 1.35$)
- Gamified referral milestone system where students invite classmates to unlock the **VIP AI Project Starter Vault** (code boilerplates, resume bullet points, and mentor review).
- Dynamic 1-click WhatsApp sharing pre-filled with the student's personalized referral tracking link.

### 5. Growth Ops Admin Command Center
- Role-Based Access Control (RBAC) allowing instant toggling between Student Experience and Admin Telemetry mode.
- Real-time campaign tracking: total registrations, channel cohorts (Campus Ambassadors, WhatsApp, Tech Communities, Viral Loop), and live activity stream.
- Built-in simulation tools to test incoming referral webhooks, batch ambassador uploads, and daily progress.

---

## 🎮 How to Demo & Test

### Student Experience (Default)
1. Open [https://nxtwave-growth-intern-xi.vercel.app/](https://nxtwave-growth-intern-xi.vercel.app/).
2. Select your branch and complete the 2-click diagnostic to view your resume audit score.
3. Enter student details to generate your personalized workshop ticket pass.
4. Test downloading the pass as a PNG and exporting the `.ics` calendar invite.
5. Click **"Copy Link"** or **"Share on WhatsApp"** to generate the active peer referral link.

### Growth Ops Admin Dashboard
1. Click **"🛡️ Growth Ops Admin Preview"** in the top navigation bar or footer.
2. Enter the admin passcode: `admin123` (or click the quick demo login).
3. Inspect the live telemetry dashboard, conversion metrics, channel distribution, and event stream.
4. Use the **Simulator Controls** at the bottom of the dashboard to trigger test referral webhooks or ambassador batch injections.
5. To test another student registration as an admin, click **"🧪 Test Another Registration"** in the ticket header to cleanly return to Step 1 without clearing admin credentials.

---

## 💻 Tech Stack & Architecture

- **Frontend:** Vanilla HTML5, ES6+ JavaScript, Tailwind CSS (via CDN)
- **Graphics & Export:** Native HTML5 Canvas 2D API (client-side image generation)
- **Styling & Design System:** Tailwind CSS with NxtWave brand palette (Plus Jakarta Sans, dark navy `#0f172a`, signature brand blue `#0b66c2`)
- **State & Storage:** Client-side event-driven state store with `localStorage` and `sessionStorage` fallback
- **Backend / Server:** Node.js static server (`asset/server.js`) for local development; configured for zero-config Vercel static deployment (`vercel.json`)
- **Performance:** 99+ Google Lighthouse score, zero external framework overhead, sub-300ms page load times on mobile 3G/4G connections

> 📖 **Full Architectural Documentation:** For comprehensive component interaction diagrams, data flow models, and technical trade-offs, see [`ARCHITECTURE.md`](./ARCHITECTURE.md).

---

## 📁 Repository Structure

```
├── ARCHITECTURE.md       # Comprehensive system architecture & data flow diagrams
├── index.html            # Main application entry point (Student View + Admin Telemetry)
├── app.js                # Core logic, Canvas ticket generator, referral engine, telemetry
├── styles.css            # Custom animations, ticket styling, shimmer effects
├── vercel.json           # Production deployment routing configuration
├── asset/
│   ├── index.html        # Modular asset source
│   ├── app.js            # Modular application logic
│   ├── styles.css        # Modular stylesheets
│   └── server.js         # Lightweight local Node.js development server
└── README.md             # Project documentation
```

---

## ⚙️ Local Development Setup

### Prerequisites
- Node.js (v16 or higher) installed on your machine.

### Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/jashwanth15/NxtWave-Growth-Intern.git
   cd NxtWave-Growth-Intern
   ```

2. **Start the local server:**
   ```bash
   node asset/server.js
   ```

3. **Open in your browser:**
   ```
   http://localhost:3000
   ```

*(Alternatively, you can open `index.html` directly in any modern web browser without running a server).*

---

## 🌐 Deployment

This project is configured for continuous static deployment via **Vercel**. Every push to the `main` branch automatically triggers a production build.

- **Production URL:** [https://nxtwave-growth-intern-xi.vercel.app/](https://nxtwave-growth-intern-xi.vercel.app/)
