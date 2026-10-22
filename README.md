<a href="https://scoresist.com"><img src="https://raw.githubusercontent.com/OUTATlME/OUTATlME/main/assets/banner.png" alt="SCORESIST — live scores with the story of every match" width="100%"></a>

I build **[SCORESIST](https://scoresist.com)**, a live sports app for football, basketball, the NBA, volleyball and Formula 1. I run the product end to end: what we build, how it looks and how it holds up on match day.

## What it does

- **Live scores that keep up.** Every live match on one screen, refreshed every 15 seconds, with goals, cards and substitutions as they happen.
- **A full match centre.** Stadium photo, scorers, statistics, player ratings, head-to-head, absences and official highlight videos where available.
- **Lineups on the pitch.** Formations, player photos, ratings and match events in one view.
- **Standings with context.** Qualification zones, recent form, home and away tables, and live league positions next to each score.
- **Built for fans.** Google sign-in, favourites synced across devices, live match chat, fan ratings and themes in your club's colours.

<img src="https://raw.githubusercontent.com/OUTATlME/OUTATlME/main/assets/screens.png" alt="SCORESIST on a phone: live matches, a match centre, a lineup and a league table" width="100%">

<img src="https://raw.githubusercontent.com/OUTATlME/OUTATlME/main/assets/desktop.png" alt="SCORESIST on desktop: sport tabs, a date strip and league-grouped results" width="100%">

## Under the hood

- **App:** Flutter, Riverpod and GoRouter. Live on the web; Android build in testing.
- **API:** NestJS and TypeScript on PostgreSQL with Prisma.
- **Data:** commercial sports data feeds, synced by background jobs that share a fixed request budget.
- **Accounts:** Supabase Auth with Google sign-in, and row-level security on every table.
- **Delivery:** GitHub Actions checks every change; the web app ships to Firebase Hosting and the API to Railway.

Since August 2026: **375 merged pull requests** and **5,000+ automated tests** running on every change.

## How I work

- **Product:** I decide what gets built and in what order, and define how every feature should behave.
- **Design:** I direct every screen, from layout and colour to match-day details, and approve the renders before release.
- **Testing:** I test each change on real matches and real phones, from live scores to push alerts.
- **Operations:** I run releases and the production side: hosting, database, sign-in, app-store accounts and costs.
- **Data quality:** I track data across leagues and decide how the app handles gaps and provider errors.

The code is written with AI coding assistants under my direction, and nothing ships without my sign-off.

<sub>The application source code is private. Club names, logos, photos and match data belong to their respective owners and data providers.</sub>
