# WorkLog Grid for Jira — Version History

This document describes what’s new and changed in each release.

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
