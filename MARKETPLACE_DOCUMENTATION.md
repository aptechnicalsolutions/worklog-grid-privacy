# WorkLog Grid for Jira — Documentation

WorkLog Grid is a Jira Cloud dashboard gadget that displays your worklogs in a timesheet-style grid: issues as rows, dates as columns, with hours per cell and row/column totals. Use it to see where time was logged at a glance, without leaving your dashboard.

---

## Table of contents

- [What you get](#what-you-get)
- [Installing the app](#installing-the-app)
- [Adding the gadget to a dashboard](#adding-the-gadget-to-a-dashboard)
- [Using the gadget](#using-the-gadget)
- [Free vs Pro](#free-vs-pro)
- [Exporting to CSV (Pro)](#exporting-to-csv-pro)
- [Tips](#tips)
- [Support](#support)

---

## What you get

- **Grid view** — Rows = Jira issues (key + summary). Columns = dates in your selected range. Cells = hours logged that day on that issue. Row totals, column totals, and a grand total are shown.
- **Date ranges** — Current week (Sun–Sat), last week, current month. On Pro: any custom date range (e.g. up to 5 years).
- **Project filter** — Limit the grid to a single project.
- **Me vs Other** — View your own worklogs by default. On Pro: search and select another user to view their timesheet.
- **Export (Pro)** — Export the grid to CSV (current view or a custom date range).

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

The gadget loads with the current week by default. Use the controls to change the date range, project, and (on Pro) the user.

---

## Using the gadget

### Date range

- **Week** — Current week (Sunday–Saturday).
- **Last Week** — Previous week (Sunday–Saturday).
- **Month** — Current calendar month.
- **Custom (Pro)** — Pick any start and end date (e.g. for audits or long-range reporting). Free tier can use Week, Last Week, or Month only.

### Show: Me or Other

- **Me** — Your worklogs only (default).
- **Other (Pro)** — Search for a user by name and select them to view their timesheet. Handy for team leads or viewing a contractor’s time.

### Project

Use the **Project** dropdown to limit the grid to one project. **All** shows every project you have worklogs in for the selected range.

### Refresh and Save

- **Refresh** — Reload the grid with the current filters and date range.
- **Save Settings** — Store your current choices (date range, project, selected user) so they’re restored next time you open the dashboard.

---

## Free vs Pro

| Feature | Free | Pro |
|--------|------|-----|
| Date presets | Week, Last Week, Month | Week, Last Week, Month, **Custom** (up to 5 years) |
| User | **Me** only | Me or **Other** (any user) |
| CSV export | — | Yes (current view or custom range, up to 5 years) |

Pro features show a **PRO** badge. Clicking them opens a short message; to upgrade, contact your Jira administrator. Only site administrators can purchase or start a trial.

---

## Exporting to CSV (Pro)

1. Set the date range and filters you want (or leave as-is for the current view).
2. Click **Export CSV**.
3. Choose **Export current view** (use the range already shown) or **Custom date range** (enter start and end).
4. Click **Export**. A CSV file downloads with columns: Issue, Summary, one column per date, and Total. A totals row is included.

The CSV is generated from the same worklog data as the grid and is suitable for payroll, billing, or external tools.

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
- **Email:** aptechnicalsolutionsllc@gmail.com

For licensing and upgrades, contact your Jira administrator.
