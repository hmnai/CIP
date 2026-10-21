# COAR Global Internal Portal — Interactive Concept

A self-contained, static HTML/CSS/JavaScript demonstration. **No live organisational data, credentials, database connections or working AppSheet links are included.** All KPI values, individual names, map markers and project milestones are synthetic.

## Launch on Windows

1. Extract the ZIP, then open the `coar_portal_demo` folder.
2. Double-click `index.html`. It works without a local server, build process or Internet connection.
3. If you prefer a local server, open a terminal in the folder and run `python -m http.server 8000`, then open `http://localhost:8000`.

## Try these interactions

- Change **Preview as** (upper-right) among Executive, Country Manager, IMU, RSU and Research.
- Navigate the sidebar and observe which modules are available for the selected demo role.
- Open any **Level of Effort** page; change month/project/person, click a project bar, or reset filters.
- Open CL Network Mapping or Partner Mapping and click a marker.
- Open Project Tracking and inspect the example milestone progress.
- Open AppSheet Applications: placeholders intentionally do **not** navigate to real applications.
- Search the sample Tools & Resources library.
- Switch to Executive and inspect the Access Matrix.

## File guide

- `index.html`: Portal shell, sidebar, top header, stylesheet and script links.
- `styles.css`: COAR-inspired colours, layout, responsive design, dashboard cards and charts.
- `app.js`: Demo navigation, synthetic data, interactive views and simulated role access.

## Security and production readiness

**Do not deploy this demo as a secure production portal.** The role switcher is purely client-side and does not prevent users from obtaining data. Production requires Firebase Authentication, server-side authorisation, Firestore Security Rules, and secured API endpoints checking per-user unit/country access. Never put private Sheets data or service-account credentials in front-end files. The live AppSheet applications must enforce their own sharing permissions.

The demo intentionally does not reuse real Power BI data or imply the charts reproduce PBIX calculations. For the production RSU dashboard, use the separately developed classification logic and validate measures against Power BI. The diagrams in the mapping views are illustrative and NOT geographic basemaps.

Suggested next stage: use this prototype as a visual and interaction baseline, then integrate with your existing Firebase portal in a staging project, adding a controlled resource registry and backend data access one module at a time.
