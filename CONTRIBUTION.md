# Team Contribution

## Bao Dang
- Designed the logo, UI, and ERDs for the project.
- Worked on the majority of frontend, including the most of the game features such as custom code editor and room menu, as well as integrating with the backend's API and websocket.
- Designed unit tests for components with Testing Library and E2E Playwright tests for the frontend.
- Reviewed PRs for other teammates and fixed bugs.

## Minh Vu
- Worked on backend's OAuth authentication flow (user login and register). Created user login session management and ensure robust password encryption for each user profile.
- Set up PostgreSQL database to manange each user creation, user register/login session, and construct initial (based) endpoints using FastAPI for further developement.
- Leveraging E2E tests using PlayWright and JavaScript. Built the testing pipeline from register and login page to main, and to player duel battle wait room. Focused on each front-end details (Error logs, appearance of crucial components of webpage, etc) for smooth user interaction

## Donald Winkelman
- Setup Svelte's styling and implemented frontend's authentication (register and log in) and profile pages.
- Implemented input error validation using Zod and Superform.
- Reviewed and merged PRs for teammates.

## Huy Ngo
- Implemented a scraper for retrieving 50+ LeetCode problems
- Utilized OpenAI API for generating test cases for the LeetCode problems and runtime analysis for users' solutions
- Built a code execution pipeline with robust error notification
- Designed the majority of backend's game mechanics with WebSocket, including queuing for ranked and unranked matches, lobby and room creation, room settings, ability uses, etc.
