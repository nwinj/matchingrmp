CampusMeet — Anonymous Meetup Matching for SRM Students

A free, privacy-first platform that anonymously matches SRM students to meet up in person — not a dating app. Two people are paired based on shared interests, weighted randomness, and rating compatibility, then the platform suggests a public time and venue. Neither person knows who the other is until they physically find each other at the venue, identified only by a fun code phrase.

⚠️ Status: Early development / planning stage. This README describes the intended design and will evolve as the project is built.

✨ Core Idea

This is not a dating app — it's an anonymous meetup / new-friend matcher, open to anyone regardless of gender. There's no romantic framing, no gender-based matching, and no swiping.

Matching is not based on gender — anyone can be matched with anyone. It's about meeting a new person, not dating.
You never see who you're matched with beforehand — no name, no photo, no ID, no social handles, no free-form chat.
The only piece of information shared during matching is the other person's rating (see below) — nothing else about them.
The platform suggests a public time and venue (e.g. a campus cafe) for both matched users to independently show up to.
At the venue, people identify each other using a fun, randomly assigned code phrase shown to both users (e.g. "I love cats") — said or shown to recognize one another, with no name or photo involved.
A small set of pre-scripted, limited messages are available before the meetup (e.g. "Running late", "Not interested", "On my way") — never a free-text chat.
Completely free to use.
⭐ Rating System
Every user has a rating, built from feedback after past meetups (e.g. did they show up, were they respectful, etc.).
When a match is proposed, each user can see the other's rating only — no name, photo, or other detail.
Users have the right to reject a match based solely on the rating shown, before a venue/time is even finalized.
Ratings are the one deliberate exception to "nothing is shared" — because they give users a basis to make an informed choice without compromising anonymity.
💬 Limited Pre-Scripted Messages

To avoid any open chat (and the harassment/privacy risks that come with it), matched users can only send from a fixed set of short, pre-written messages, such as:

"I'm running late"
"I'm not interested, cancelling this match"
"I've arrived"
"Can we reschedule?"

No custom text, images, links, or contact info can ever be sent through the app.

🔐 Privacy & Safety Principles

Privacy is the foundation of the entire system, not an add-on.

Zero identity exposure before or during matching. Matched users see only the other's rating and, later, a code phrase — never a name, photo, roll number, department, or gender.
No open-ended communication. Only the fixed pre-scripted messages above are possible. No chat, no images, no contact exchange at any stage.
No public profiles, no directory. Users cannot browse, search for, or select a specific person.
Code-phrase identification. Recognition at the venue happens purely through a shared, randomly generated phrase — never a photo or name.
ID data is retained, not deleted. Unlike a typical anonymous app, we deliberately keep each user's college ID verification record on file. This isn't used for matching or shown to anyone — it exists solely so that if a report is filed after a meetup, the platform can identify and act against the reported account.
Data minimization otherwise. Beyond ID verification (for eligibility + accountability), interest tags (for matching), and rating history, no other personal data is collected.
🎓 Authentication
Sign-up is restricted to users who verify themselves with a valid SRM College ID card.
One account per student — verification prevents duplicate/fake accounts.
ID verification records are stored securely and used only for (a) confirming eligibility and (b) identifying an account if it's reported for misconduct. They are never shown to other users or used in the matching process itself.
🎯 Matching Algorithm (Planned)
Each user fills out an interest profile (hobbies, music, movies, personality traits, what kind of meetup they're looking for, etc.) — no gender field used for matching.
A similarity score is computed between eligible users based on overlapping/weighted interests.
A randomness factor is blended in so matches aren't purely "clone of you" — encourages meeting genuinely new people.
Both users see each other's rating only and can accept or reject the proposed match at this stage.
Once both accept, the platform selects a public meetup time and venue and generates a shared code phrase for identification.
Only the pre-scripted messages above are available before the meetup — no further interaction happens through the app.
Matches are revealed periodically (e.g. a weekly drop) rather than a swipe feed, to keep the experience intentional and infrequent rather than addictive.
🚨 Reporting & Moderation
After a meetup, either user can report the other directly from the app.
A report flags the reported account for review using the retained ID verification data (see Privacy above).
Users found to have engaged in bad-faith or harmful behavior are temporarily banned from the platform for a set period; repeated reports can escalate the ban duration and affect their rating.
Reporting does not reveal the reporting user's identity to the reported user.
⚖️ Liability Disclaimer

Please read this carefully — it should also appear in your in-app Terms of Service.

CampusMeet is solely a matching service. We connect two verified students based on interest similarity, rating, and randomness, and suggest a time/place to meet. We do not vet, background-check, or take responsibility for the conduct, safety, or behavior of any matched user, before, during, or after a meetup.

Users meet entirely at their own discretion and own risk.
The platform is not responsible for any incident, harm, dispute, or outcome arising from a meetup arranged through the app.
Reporting a bad actor may result in a ban from the platform, but this is a moderation action, not a guarantee of safety, and not an admission of liability.
Users are strongly encouraged to meet only in the public venues suggested by the app, inform a friend of their plans, and use their own judgment.

(You should have this reviewed by someone knowledgeable about Indian consumer-protection/IT law before launching publicly — a disclaimer in a README/ToS reduces but does not eliminate legal exposure, especially since you're retaining ID data and facilitating in-person meetups between strangers.)

🧱 Suggested Tech Stack

(Adjust based on your comfort level — this is a reasonable starting point for a solo/small-team student project.)

Layer	Suggestion
Frontend	React / Next.js
Backend	Node.js (Express) or Django
Database	PostgreSQL (relational — good for structured interest/rating/matching data)
Auth	Custom college-ID verification + JWT sessions
Venue/scheduling logic	Backend service picking from a curated list of campus-approved public venues + time slots
Code-phrase generator	Simple random phrase generator, shared to both matched users only
Hosting	Vercel / Render / Railway (student-friendly free tiers)
Image storage (ID verification)	Encrypted object storage (e.g. S3-compatible), access-restricted to moderation use only
🗺️ Roadmap
 College ID verification flow
 Interest-based onboarding form (no gender field in matching logic)
 Rating system (post-meetup feedback → rating score)
 Matching engine (similarity + randomness + rating visibility)
 Accept/reject match screen (rating-only view)
 Venue/time suggestion engine (curated public campus-area spots)
 Code-phrase generator for venue identification
 Pre-scripted message system (fixed message set only)
 Post-meetup reporting flow
 Ban/moderation dashboard for reported accounts
 Weekly match cycle scheduler
 Mobile-responsive UI
🚀 Getting Started
bash
# Clone the repo
git clone https://github.com/<your-username>/campusmeet.git
cd campusmeet

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env

# Run the development server
npm run dev
🤝 Contributing

This is currently a student-led project for SRM. Contributions, feedback, and design ideas are welcome — open an issue or a pull request.

⚖️ Disclaimer

This platform is an independent student project and is not officially affiliated with or endorsed by SRM University. It is intended solely for enrolled students for the purpose of anonymous, respectful, in-person meetups with new people. Misuse, harassment, or impersonation will result in account termination.

📄 License

Specify a license (MIT recommended for open-source student projects) — add a LICENSE file to the repo.
