# Deliverable 4: AI Worklog (3 Meaningful Iterations)

## Example 1 — Funnel Architecture & Lead Capture Hook
- **Prompt:** *"Build a landing page to get 500 engineering students for an AI workshop with a ₹2,000 budget."*
- **AI Output:** Generated a standard, one-page static registration form with basic text fields and a generic "Submit" button.
- **What I Changed/Rejected:** Rejected the static form because cold traffic drop-off on generic forms exceeds 90%. I pivoted the architecture into a 3-Step Interactive Placement Diagnostic that calculates a personalized ATS gap score (34/100) first, establishing urgency before asking for contact info.
- **Final Output:** A 3-step high-intent diagnostic funnel with personalized ATS risk cards and instant pass generation.

---

## Example 2 — Viral Loop Simulation & Behavioral Distribution
- **Prompt:** *"Create a referral system where students invite 3 friends to unlock a bonus vault."*
- **AI Output:** Implemented a naive script where every single student automatically reached 3 referrals within 2 seconds.
- **What I Changed/Rejected:** Rejected 100% uniform completion as mathematically unrealistic. Real viral dynamics follow a behavioral distribution. I rebuilt the engine with persona-weighted probabilities (~30% reach 3/3, ~35% stall at 2/3, ~20% reach 1/3, ~15% get 0) and slowed event delivery to a realistic human cadence (~28s).
- **Final Output:** A realistic viral simulation with progress tracking and gated starter vault unlocking.

---

## Example 3 — RBAC Security & Form Session State
- **Prompt:** *"Implement authentication and sign-in for students and admins with password support."*
- **AI Output:** Suggested hard-gating the entire landing page on load with login popups and placing redundant password fields on the pass claim form.
- **What I Changed/Rejected:** Rejected gating the landing page on initial load (destroys top-of-funnel reach). Removed the duplicate password field from the landing page. Moved account creation strictly inside the New Registration modal, built a dedicated input isolation handler (`resetAuthFormInputs`) to eliminate stale credentials, and created a dual-role RBAC toggle allowing admins to test unlimited registrations from Step 1.
- **Final Output:** Zero-friction progressive disclosure for visitors, seamless student pass access, and a Level-4 Growth Ops Admin preview mode.
