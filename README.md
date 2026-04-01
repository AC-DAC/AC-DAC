# Hey, I'm Alex 👋
Digital Producer with 14+ years in multimedia and design, transitioning into DevOps engineering. I bring systems thinking from a production background, understanding how things are built, delivered, and maintained, and I'm applying that to infrastructure, automation, and deployment pipelines.
 
---
 
## What I'm Working On
- Building a DevOps learning path hands-on: Linux → Git → Docker → CI/CD → Cloud → IaC → Observability
- Deploying and maintaining real infrastructure on a self-hosted Raspberry Pi 4B lab environment
- Automating Android app delivery for FitForge via GitHub Actions → EAS Build → Google Play Store
 
---
 
## Projects
 
### FitForge
Privacy-first workout tracking app for Android. No ads, no account required, all data stored on-device. Features custom workout creation, guided session mode, stats and insights, reminders, and QR code workout sharing. Built in React Native / Expo with a custom Material Design-inspired design system. Currently in closed testing on the Google Play Store.
 
CI/CD pipeline: GitHub Actions `test → build → submit` on version tag push. Jest unit test suite. EAS Build produces AAB artifact; EAS Submit delivers to Play Store internal track via Google Service Account (least-privilege permissions). Actions pinned to immutable commit SHAs with `permissions: contents: read` at workflow level. Lefthook + gitleaks for pre-commit secret scanning.
 
<table>
  <tr>
    <td><img src="assets/screenshots/fitforge-phone-screenshots-01.png" width="220"/></td>
    <td><img src="assets/screenshots/fitforge-phone-screenshots-02.png" width="220"/></td>
    <td><img src="assets/screenshots/fitforge-phone-screenshots-03.png" width="220"/></td>
  </tr>
</table>
 
<table>
  <tr>
    <td><img src="assets/screenshots/fitforge-tablet-screenshots_7-4.png" width="340"/></td>
    <td><img src="assets/screenshots/fitforge-tablet-screenshots_7-5.png" width="340"/></td>
  </tr>
  <tr>
    <td><img src="assets/screenshots/fitforge-tablet-screenshots_10-6.png" width="340"/></td>
    <td><img src="assets/screenshots/fitforge-tablet-screenshots_10-7.png" width="340"/></td>
  </tr>
</table>
 
`React Native` `Expo` `GitHub Actions` `EAS Build` `Jest` `Android`

---
 
### Mothership — Centralised WordPress Management Infrastructure
Self-hosted centralised management dashboard for over 15 production WordPress client sites, built on MainWP and deployed to a dedicated subdomain. Replaces a manual, site-by-site update workflow with a single control plane covering bulk updates, uptime monitoring, and security visibility across all managed sites.
 
Key implementation decisions: real server-level cron over WP-Cron (unreliable on a low-traffic dashboard-only subdomain); per-site OpenSSL key pairs with Unique Security IDs replacing password authentication; maintenance mode for frontend obscurity after directory password protection was evaluated and rejected (intercepts WordPress core HTTP requests). Backup strategy layered across UpdraftPlus per-site (weekly) and VentraIP server-level hourly snapshots.
 
![Mothership Dashboard](assets/screenshots/mothership-dashboard.jpg)
 
`MainWP` `WordPress` `Apache` `MariaDB` `Linux` `Cron`
