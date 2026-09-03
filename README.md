<div align="center">

# 🎭 CampusMeet

### Anonymous Meetup Matching for SRM Students

*Not a dating app — a privacy-first way to meet someone new, in person, on campus.*

![Status](https://img.shields.io/badge/status-planning-yellow)
![License](https://img.shields.io/badge/license-MIT-blue)
![Made for](https://img.shields.io/badge/made%20for-SRM%20Students-orange)

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [How It Works](#-how-it-works)
- [Rating System](#-rating-system)
- [Pre-Scripted Messages](#-pre-scripted-messages)
- [Privacy & Safety](#-privacy--safety)
- [Authentication](#-authentication)
- [Reporting & Moderation](#-reporting--moderation)
- [Liability Disclaimer](#️-liability-disclaimer)
- [Tech Stack](#-tech-stack)
- [Roadmap](#️-roadmap)
- [Getting Started](#-getting-started)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🧭 Overview

CampusMeet anonymously pairs verified SRM students to meet up in person — based on shared interests, weighted randomness, and rating compatibility. There are no profiles, no photos, no swiping, and no chat.

| | |
|---|---|
| 🚫 | **Not** gender-based matching — open to anyone |
| 🚫 | **Not** a dating app — just meeting someone new |
| 🔒 | Only verified SRM students (College ID required) |
| 💸 | Completely free to use |
| 🎲 | Matches use interests **+** randomness **+** rating |

---

## 🔄 How It Works

```
1. Fill out interest profile        →  no gender used in matching
2. Get proposed a match             →  you see ONLY their rating
3. Accept or reject the match       →  based on rating alone
4. Platform assigns venue + time    →  a public, campus-area spot
5. Both get a shared code phrase    →  e.g. "I love cats"
6. Show up and find each other      →  identified by the phrase only
```

No names. No photos. No open chat — ever.

---

## ⭐ Rating System

- Every user carries a **rating**, built from feedback after past meetups.
- When a match is proposed, each user sees **only the other person's rating** — nothing else.
- Users can **reject a match based on rating alone**, before any venue or time is revealed.
- This is the *one* deliberate exception to "nothing is shared" — enough for an informed choice, without breaking anonymity.

---

## 💬 Pre-Scripted Messages

To avoid open chat entirely, matched users can only send from a **fixed set of short messages**:

| Message | Meaning |
|---|---|
| 🏃 "I'm running late" | Delay notice |
| 🙅 "I'm not interested, cancelling" | Cancels the match |
| ✅ "I've arrived" | Confirms presence at venue |
| 🔁 "Can we reschedule?" | Requests a new time |

No custom text, images, links, or contact info can ever be sent.

---

## 🔐 Privacy & Safety

> Privacy is the foundation of this platform — not an add-on.

- **Zero identity exposure** — no name, photo, roll number, department, or gender shown at any stage.
- **No open communication** — only the fixed pre-scripted messages above.
- **No public profiles or directory** — users can't browse or search for anyone.
- **Code-phrase identification** — recognition at the venue happens through a random shared phrase only.
- **ID data is retained (not deleted)** — kept solely so reported accounts can be identified and actioned. Never used for matching or shown to anyone.
- **Data minimization** — beyond ID verification, interests, and rating history, nothing else is collected.

---

## 🎓 Authentication

- Sign-up requires verification with a valid **SRM College ID card**.
- One account per student — prevents duplicate/fake accounts.
- ID records are stored securely, used only for eligibility checks and misconduct investigations — never shown to other users or used in matching.

---

## 🎯 Matching Algorithm *(Planned)*

1. Build an interest profile (hobbies, music, personality, what kind of meetup you want).
2. Compute a **similarity score** between eligible users.
3. Blend in a **randomness factor** so matches aren't just "clones of you."
4. Show both users each other's **rating only** — accept/reject here.
5. On mutual accept, assign a **public venue + time** and generate a **code phrase**.
6. Only pre-scripted messages available until the meetup.
7. Matches drop periodically (e.g. weekly) — intentional, not addictive.

---

## 🚨 Reporting & Moderation

- Either user can **report** the other after a meetup.
- Reports use retained ID data to identify the reported account.
- Confirmed bad-faith behavior results in a **temporary ban**, with escalating duration for repeat reports and impact on rating.
- The reporting user's identity is never revealed to the reported user.

---

## ⚖️ Liability Disclaimer

> **This section should also appear in your in-app Terms of Service.**

CampusMeet is solely a **matching service**. We connect verified students based on interests, rating, and randomness, and suggest a time/place to meet.

- ❌ We do **not** vet, background-check, or take responsibility for any matched user's conduct or safety.
- ❌ We are **not responsible** for any incident, harm, dispute, or outcome from a meetup arranged through the app.
- ✅ Reporting may result in a ban — but this is a moderation action, not a safety guarantee.
- ✅ Users are encouraged to meet only at suggested public venues and use their own judgment.

> ⚠️ *Have this reviewed by someone familiar with Indian IT/consumer-protection law before public launch — retaining ID data and facilitating in-person meetups both carry real legal exposure.*

---

## 🧱 Tech Stack

| Layer | Suggestion |
|---|---|
| Frontend | React / Next.js |
| Backend | Node.js (Express) or Django |
| Database | PostgreSQL |
| Auth | Custom college-ID verification + JWT |
| Venue/scheduling | Curated list of campus-approved public venues + time slots |
| Code-phrase generator | Random phrase generator, shared to matched pair only |
| Hosting | Vercel / Render / Railway |
| ID image storage | Encrypted object storage, moderation-access only |

---

## 🗺️ Roadmap

- [ ] College ID verification flow
- [ ] Interest-based onboarding (no gender in matching logic)
- [ ] Rating system (post-meetup feedback)
- [ ] Matching engine (similarity + randomness + rating visibility)
- [ ] Accept/reject screen (rating-only view)
- [ ] Venue/time suggestion engine
- [ ] Code-phrase generator
- [ ] Pre-scripted message system
- [ ] Post-meetup reporting flow
- [ ] Ban/moderation dashboard
- [ ] Weekly match cycle scheduler
- [ ] Mobile-responsive UI

---

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/<your-username>/campusmeet.git
cd campusmeet

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env

# Run the development server
npm run dev
```

---

## 🤝 Contributing

This is a student-led project for SRM. Contributions, feedback, and design ideas are welcome — open an issue or a pull request.

---

## 📄 License

Specify a license (MIT recommended for open-source student projects) — add a `LICENSE` file to the repo.

---

<div align="center">

*Not officially affiliated with or endorsed by SRM University. Misuse, harassment, or impersonation results in account termination.*

</div>
