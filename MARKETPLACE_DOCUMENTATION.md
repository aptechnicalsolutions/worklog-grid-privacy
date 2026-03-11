# WorkLog Grid for Jira — Documentation

WorkLog Grid is a Jira Cloud dashboard gadget that displays your worklogs in a timesheet-style grid: issues as rows, dates as columns, with hours per cell and row/column totals. Use it to see where time was logged at a glance, without leaving your dashboard.

---

## Table of contents

- [What you get](#what-you-get)
- [Installing the app](#installing-the-app)
- [Adding the gadget to a dashboard](#adding-the-gadget-to-a-dashboard)
- [Using the gadget](#using-the-gadget)
- [Logging work from the grid](#logging-work-from-the-grid)
- [Free vs Paid](#free-vs-paid)
- [Exporting to CSV](#exporting-to-csv)
- [Tips](#tips)
- [Support](#support)
- [Version history](#version-history)

---

## What you get

- **Grid view** — Rows = Jira issues (key + summary). Columns = dates in your selected range. Cells = hours logged that day on that issue. Row totals, column totals, and a grand total are shown.
- **Date ranges** — Current week (Sun–Sat), last week, current month, or custom (free: up to 31 days; paid: up to 1 year).
- **Project filter** — Limit the grid to a single project.
- **Me vs Other** — View your own worklogs or search and select one other user to view their timesheet. Available to all users.
- **Log work from the grid** — When viewing **Me**, click any hour cell to open a Log work modal. Enter the date, time started, time spent (hours), and an optional description, then save. The worklog is added or updated in Jira and the grid refreshes. You can log or edit time without opening the issue.
- **Export** — Export the grid to CSV (current view or custom date range). Free: soft limits (31 days per export, 5 per month); paid/trial: unlimited.

All data comes from Jira worklogs and respects your Jira permissions. Nothing is sent to external systems.

---

## Installing the app

1. In Jira, go to **Apps** → **Find new apps** (or **Manage apps** → **Find new apps**).
2. Search for **WorkLog Grid**.
3. Click **Install** (or **Get it free** / **Start free trial** for Pro).
4. Complete the installation for your site.

Only Jira administrators can install apps. If you don’t see the option, ask your admin to install WorkLog Grid.

---

## Adding the gadget to a dashboard

1. Open **Dashboards** and open (or create) a dashboard.
2. Click **Add gadget** (or **Add** → **Gadget**).
3. Find **WorkLog Grid** and click **Add**.
4. Click **Save** on the dashboard.

The gadget loads with the current week by default. Use the controls to change the date range, project, and user (Me or Other).

---

## Using the gadget

### Date range

- **Week** — Current week (Sunday–Saturday).
- **Last Week** — Previous week (Sunday–Saturday).
- **Month** — Current calendar month.
- **Custom** — Pick any start and end date (free: up to 31 days; paid/trial: up to 1 year). After choosing start and end dates, click **Apply** to load the grid for that range; the grid does not refresh when you simply click away from the date fields.

### Show: Me or Other

- **Me** — Your worklogs only (default).
- **Other** — Search for a user by name and select them to view their timesheet. Available to all users. Handy for team leads or viewing a contractor’s time.

### Project

Use the **Project** dropdown to limit the grid to one project. **All** shows every project you have worklogs in for the selected range.

### Refresh and Save

- **Refresh** — Reload the grid with the current filters and date range.
- **Save Settings** — Store your current choices (date range, project, selected user) so they’re restored next time you open the dashboard.

### Logging work from the grid

When you’re viewing **Me** (your own worklogs), you can log or edit time directly from the grid:

1. Click any hour cell (or a cell with **0** to add new time).
2. A **Log work** modal opens with the issue and date. You can change:
   - **Date** — The day the work was done (defaults to the cell’s date).
   - **Time started** — When you started (defaults to 9:00 AM).
   - **Time spent (hours)** — How many hours (e.g. `2.5`). Prefilled with the current value if the cell already has time.
   - **Description (optional)** — What you worked on; stored as the worklog comment in Jira.
3. Click **Log work** to save. The grid refreshes with the new value. Click **Cancel** to close without saving.

This uses the same Jira worklog API as logging work on the issue page. You can only log work for yourself (when **Me** is selected); the **Other** view is read-only.

---

## Free vs Paid

Marketplace pricing: sites with 1–10 users are free; 11+ users are paid. All users get the full in-app experience (date presets including Custom, Me/Other user, project filter, CSV export). The main difference is export limits.

| Feature | Free | Paid / Trial |
|--------|------|------------------|
| Date presets | Week, Last Week, Month, **Custom** (up to 31 days) | Week, Last Week, Month, **Custom** (up to 1 year) |
| User | **Me** or **Other** (one user) | Me or **Other** (one user) |
| CSV export | Yes, with limits: 31 days per export, 5 per month | Unlimited; up to 365 days per export |

When free users hit export limits, a friendly modal explains the limits and offers a link to contact support (e.g. for small teams that want unlimited exports). Only site administrators can purchase or start a trial.

---

## Exporting to CSV

1. Set the date range and filters you want (or leave as-is for the current view).
2. Click **Export CSV**.
3. Choose **Export current view** (use the range already shown) or **Custom date range** (enter start and end).
4. Click **Export**. A CSV file downloads with columns: Issue, Summary, one column per date, and Total. A totals row is included.

The CSV is generated from the same worklog data as the grid and is suitable for payroll, billing, or external tools. **Free users**: up to 31 days per export, 5 exports per month; if you hit the limit, the app shows a short message with a support link. **Paid/trial**: unlimited exports and longer date ranges.

---

## Tips

- **Wider grid** — Use a 2-column (or 1-column) dashboard layout so the gadget has more horizontal space and less scrolling.
- **Sticky Issue column** — The Issue column stays visible when you scroll the grid horizontally.
- **Today** — The column for today’s date is highlighted so you can spot it quickly.
- **Empty grid** — If you see no data, try **Month** or a **Custom** range, or confirm you have worklogs in the selected range and project.

---

## Support

For questions, issues, or feature requests:

- **Vendor:** AP Technical Solutions LLC  
- **Email:** support@aptechnicalsolutions.com

For licensing and upgrades, contact your Jira administrator.

---

## Version history

For a list of changes in each release, see [VERSION_HISTORY.md](./VERSION_HISTORY.md). Current public versions: **3.0.0**, **2.2.0**, and **2.0.0**. The next planned release is **3.1.0** (minor improvements and security updates).
