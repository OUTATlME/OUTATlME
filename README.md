[![Building SCORESIST — Eren Deniz Karaman](https://raw.githubusercontent.com/OUTATlME/OUTATlME/main/assets/profile-banner.png)](https://scoresist.com)

# Hi, I'm Eren Deniz Karaman.

I'm building **SCORESIST**, a sports platform that connects scores with the story of a match: events, lineups, standings, teams and players.

I lead the product direction, define requirements and test the experience, from the daily match feed to the details on the pitch.

**[Explore the live app →](https://scoresist.com)** · **[Engineering notes](https://github.com/OUTATlME/OUTATlME/blob/main/ENGINEERING.md)**

## SCORESIST — Signature of Sports

**Scores are the starting point. The match is the story.**

Football, basketball, volleyball and Formula 1 sections share a consistent interface, with feature depth shaped by each sport and its available data.

- **Follow the schedule:** browse fixtures and results by date, sport, league and country.
- **Understand the action:** explore football goals, cards, substitutions and match statistics.
- **Read the lineup:** see formations, player portraits and event markers on a dedicated pitch.
- **Explore the context:** move between matches, leagues, teams and player profiles.
- **Make it yours:** use favorites and choose light, dark or team-inspired themes.

## Inside the app

### The match feed

Sports navigation, league grouping and country context make the daily schedule easy to explore.

[![SCORESIST English match feed with sports navigation and league-grouped results](https://raw.githubusercontent.com/OUTATlME/OUTATlME/main/assets/match-feed.jpg)](https://scoresist.com)

### Lineups and match context

Provider-supplied formations, player identities and event indicators come together on the pitch. This view shows the upper section of the scrollable two-team lineup.

[![SCORESIST English lineup view with formations, player portraits and event indicators](https://raw.githubusercontent.com/OUTATlME/OUTATlME/main/assets/lineups.jpg)](https://scoresist.com)

*Screenshots from the public web app, captured on 14 September 2026.*

## Behind the product

| Area | Technologies and purpose |
| --- | --- |
| Interface | Flutter, Dart, Riverpod and GoRouter |
| Backend | NestJS, TypeScript and REST APIs |
| Data | PostgreSQL, Supabase and provider integrations |
| Synchronization | Background jobs, request budgets and event reconciliation |
| Delivery | GitHub Actions, Firebase Hosting and Railway |

Three engineering priorities guide the work:

1. **Keep scores moving.** Separate fast score checks from heavier event collection and follow up on late events.
2. **Use the request budget carefully.** Prioritize live and upcoming matches while retaining capacity for historical data and enrichment.
3. **Verify what reaches users.** Combine automated checks, visual review and deployed web artifact verification.

[Read the engineering decisions and verification notes →](https://github.com/OUTATlME/OUTATlME/blob/main/ENGINEERING.md)

## How I work

I combine product direction and hands-on testing with AI-assisted development. I evaluate implementation choices, review outcomes and refine the details through real use.

## Current status

**The web app is live and actively evolving.** Data coverage varies by sport and competition. Formula 1 currently covers schedules and results. Account activation, Android store publication and broader release-language coverage remain future work.

This profile is the public SCORESIST showcase. Application source code is maintained privately.

**[Try SCORESIST →](https://scoresist.com)**

[Asset and data credits](https://github.com/OUTATlME/OUTATlME/blob/main/NOTICE.md)
