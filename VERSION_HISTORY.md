# WorkLog Grid for Jira — Version History

This document describes what’s new and changed in each release.

---

## Version 3.0.0

**Release summary:** Log work directly from the grid. Click a cell to open a Jira-style modal (date, time started, time spent, description); save updates Jira and refreshes the grid. *(Published to production as 3.0.)*

### Changes

- **Log work from the grid**
  - When viewing **Me**, click any hour cell to open a **Log work** modal.
  - Set **date**, **time started**, **time spent** (hours), and optional **description** (stored as worklog comment in Jira).
  - Save adds or updates the worklog via Jira REST API; grid cache is invalidated so the next refresh shows the new value immediately.
  - Same workflow as logging work on the issue page, without leaving the dashboard. **Other** user view remains read-only.
- **Backend**
  - New scope: **write:jira-work** for creating and updating worklogs.
  - **saveWorklog** resolver accepts optional **started** (ISO date/time) and **comment** (plain text, sent as ADF to Jira).
  - After a successful save, the timesheet cache for the current view is invalidated so the grid refetches fresh data.
- **Technical**
  - Permissions: `storage:app`, `read:jira-work`, **`write:jira-work`**, `read:jira-user`.

---

## Version 2.3.0

**Release summary:** Simplified pricing and access model aligned with Atlassian Marketplace (1–10 users free, 11+ paid). Free users get a full in-app experience with soft export limits; trial badges removed.

### Changes

- **Pricing & access**
  - **Trial users** (`license.isEvaluation`): full access, unlimited exports; no gating.
  - **Paid users** (`license.isActive`): full access, unlimited exports.
  - **Free users**: full viewing and filtering; custom date range (up to 31 days), project filter, and **Other user** (single user) are now available to everyone. No Pro-only paywalls for normal usage.
- **Export model**
  - **Free**: CSV export allowed with soft limits — max 31 days per export, 5 exports per user per month, up to 1000 rows. Limits enforced server-side; export count stored per site/user/month.
  - **Paid/Trial**: Unlimited exports; up to 365 days per export and higher row cap.
  - Export button visible to all users; when free users hit limits, a friendly “Export limits” modal explains the policy and offers a support link for small teams that want unlimited exports.
- **Small-team upgrade path**
  - Modal copy emphasizes unlimited exports and extended ranges for paid plans; directs small teams to contact support for manual upgrade options (Marketplace billing is site-based, so 1–10 user sites cannot pay via tier).
- **UI/UX**
  - Removed all **PRO** badges (Custom dates, Other user, Export CSV).
  - Removed **Pro Trial** pill/badge.
  - No “Free Tier” badge. Upgrade messaging only when export limits are exceeded or export range exceeds free max.
- **Backend**
  - Centralized plan config (`PLAN_CONFIG`); helpers: `getPlanState()`, `getExportLimits()`, `canExport()`, `getUpgradeMessageContext()`.
  - `getLicenseInfo` now returns export limits and optional `supportUrl` (set via `WORKLOGGRID_SUPPORT_URL` for “Contact support” link).
- **Manifest**
  - Gadget description updated: view yours or one other user’s timesheet; export to CSV with soft limits on free plans.

---

## Version 2.2.0

**Release summary:** Security and dependency updates. No change to app behavior or features.

### Changes

- Security and dependency updates for stability and compatibility with current Forge and Jira. No new features or user-facing changes.

---

## Version 2.1.0

**Release summary:** Upgrade modal improvements for Free-tier users.

### Changes

- **Upgrade modal (Free tier)**  
  When a Free user taps a Pro feature (Custom dates, Other user, or Export CSV), the upgrade modal is simplified: clearer message, single “Close” button, and improved spacing. Users are directed to contact their Jira administrator to upgrade; the in-app upgrade button was removed.

---

## Initial release (2.0.0)

**Release summary:** Initial release with grid view, filters, and CSV export.

### Features

- **Grid view**
  - Timesheet-style grid: issues as rows, dates as columns, hours per cell.
  - Row, column, and grand totals.
  - Sticky Issue column; today’s column highlighted and scrolls into view.
- **Date ranges**
  - Week (current Sun–Sat), Last week, Month.
  - Pro: Custom date range (e.g. up to 5 years).
- **Filters**
  - Project dropdown to limit to one project.
  - Me vs Other (Pro): search and select another user to view their timesheet.
- **Export (Pro)**
  - Export to CSV: current view or custom date range (up to 5 years).
- **Licensing**
  - Free tier: Week, Last week, Month; Me only; project filter.
  - Pro tier: Custom range, Other user, CSV export.
  - “Pro Trial” pill when on trial; PRO badges and upgrade modal for Free users.
- **Persistence**
  - User preferences (date range, project, selected user) saved and restored per gadget.
  - Short-lived cache for grid data to reduce API load.
- **Technical**
  - Built on Atlassian Forge; Jira REST APIs only; no external services. Permissions: `storage:app`, `read:jira-work`, `read:jira-user`.

---

## Support

For questions or issues: **AP Technical Solutions LLC** — aptechnicalsolutionsllc@gmail.com.

For licensing and upgrades, contact your Jira administrator.
