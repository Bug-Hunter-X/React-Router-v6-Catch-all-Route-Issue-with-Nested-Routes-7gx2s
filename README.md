# React Router v6 Catch-all Route Issue

This repository demonstrates a subtle bug in React Router v6 related to the usage of catch-all routes ("/*") when nested within other routes.  The catch-all route unexpectedly matches even when other, more specific, routes should take precedence.

The problem is clearly shown in `App.js`, where the `/*` route interferes with the other routes.  `AppSolution.js` offers a solution to this issue.

## How to reproduce:
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe that navigating to `/` or `/about` still shows the NotFound component.

## Solution:
The solution involves carefully considering route placement and the order in which they're defined within the `Routes` component. See `AppSolution.js` for a corrected implementation.