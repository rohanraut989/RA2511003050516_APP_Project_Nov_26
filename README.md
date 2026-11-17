# BloodBeacon

**Blood, found faster.**

BloodBeacon is an AI-powered emergency blood donor activation system. When a patient needs blood, it automatically finds eligible, compatible donors near the hospital, ranks them with a machine-learning model that predicts who is most likely to respond, and activates them one by one through a sequential WhatsApp cascade — no app install, no manual phone calls. A donor's phone number stays private until the donor confirms.

**Live system:** https://bloodbeacon.onrender.com

---

## Course Details

| | |
|---|---|
| **Course ID** | 21CSC203P |
| **Course Name** | Advanced Programming Practice |

## Team Members — Batch 14

| Full Name | Register Number | Department | Section | Academic Year |
|---|---|---|---|---|
| Maniraj Sharma | RA2511003050513 | Computer Science and Engineering | C | 2026–27 (Second Year) |
| Rohan Kumar Raut | RA2511003050516 | Computer Science and Engineering | C | 2026–27 (Second Year) |
| Navnit Singh | RA2511003050517 | Computer Science and Engineering | C | 2026–27 (Second Year) |
| Bikesh Kumar Kushwaha | RA2511003050536 | Computer Science and Engineering | C | 2026–27 (Second Year) |

## Mentor Details

| | |
|---|---|
| **Mentor's Full Name** | Dr. D. Deena Rose |
| **Designation** | Assistant Professor, Department of Computer Science and Engineering |

---

## How It Works

1. A patient's family submits a blood request (group, hospital, city) on the web app.
2. The **NBTC eligibility engine** filters donors by medical rules — age 18–65, weight, haemoglobin, and the mandatory donation gap.
3. The **compatibility engine** matches blood groups using the red-cell (and plasma) compatibility matrix.
4. The **ML Donor-Response Predictor** (Logistic Regression, scikit-learn) ranks the matched donors by predicted likelihood of responding.
5. The **sequential cascade** asks donors one at a time on WhatsApp with a two-step consent conversation; the first confirmed donor's contact is shared with the receiver, who is also notified on WhatsApp on confirmation and fulfilment.

## Key Features

- Rule-based medical eligibility (AI never touches a medical rule)
- Blood-group compatibility with tiered matching — same city first, then nearby cities, with cross-group disclosure
- ML ranking of donors inside each tier
- WhatsApp-first: works on any phone, no app install
- Privacy-first: donor number revealed only after the donor confirms
- Donor protection: monthly alert caps and donation-gap cooldowns prevent donor fatigue
- Fully automatic public flow; staff console is passcode-gated and separate

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python, Flask, Gunicorn |
| Database | PostgreSQL (Supabase) |
| Machine Learning | scikit-learn (Logistic Regression) |
| Messaging | WhatsApp via a Node.js (Baileys) bridge |
| Frontend | HTML, CSS, Jinja2 |
| Hosting | Render |

## Project Report

The full project report is included in this repository: `BATCH_14_APP_PROJECT_REPORT.pdf`
