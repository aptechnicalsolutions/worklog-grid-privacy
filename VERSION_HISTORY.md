# WorkLog Grid for Jira — What’s New

A simple overview of what changed in each release.

---

## Version 3.3.0

**Improvements**

- **Refresh shows the latest data** — When you click **Refresh**, the grid now loads the most up-to-date worklogs from Jira. Time you log on an issue elsewhere will appear after you refresh.
- **Trial and paid licenses work correctly** — If you’re on a trial, paid plan, or promo (e.g. 10% off), the app now correctly gives you extended date ranges and unlimited exports instead of the free-tier limits.
- **Clearer upgrade message** — When you hit free-tier limits (31-day range, 5 exports per month), the message now clearly explains the limit and tells you to contact support to upgrade.
- **Faster loading** — The grid loads more quickly when you have many issues with logged time.

---

## Version 3.2.0

**Improvements**

- **Custom date range** — When you pick custom dates, the grid only updates after you click **Apply**. You can change the dates or click away without triggering a reload.
- **Log work modal on small gadgets** — On short dashboards, the Log work popup no longer gets cut off. The form scrolls and the **Cancel** and **Log work** buttons stay visible.
- **Smoother refresh** — While the grid is refreshing, it stays on screen with a short “Loading…” overlay instead of disappearing.

**Removed**

- The **Today** button was removed (it didn’t behave reliably in the dashboard). The grid still highlights today’s column.

---

## Version 3.0.0

**New**

- **Log work from the grid** — When viewing **Me**, click any hour cell to open a **Log work** window. Enter the date, time started, time spent, and an optional description, then save. The worklog is added or updated in Jira and the grid updates. Same as logging work on the issue, without leaving the dashboard. When viewing **Other**, the grid is read-only.

---

## Version 2.3.0

**Improvements**

- **Simpler pricing** — Free for 1–10 users; paid for 11+. Free users can use custom date range (up to 31 days), project filter, and **Other** user (view one other person’s timesheet). No paywalls for normal viewing or filtering.
- **Export for everyone** — Everyone can export to CSV. Free: up to 31 days per export and 5 exports per month. Paid/trial: unlimited exports and longer date ranges. When free users hit the limit, a short message explains and points to support.
- **Cleaner interface** — Removed **PRO** badges and the **Pro Trial** badge. Upgrade messaging only appears when you hit export or range limits.

---

## Version 2.2.0

**Improvements**

- **Upgrade message (free users)** — When a free user tries a paid feature, the message is simpler: one **Close** button and a clear note to contact your Jira administrator to upgrade.
- **Stability** — Security and dependency updates for better compatibility.

---

## Version 2.0.0 — Initial release

**What you get**

- **Grid** — Issues as rows, dates as columns, hours per cell. Row, column, and grand totals. Sticky Issue column; today’s column highlighted.
- **Date ranges** — Week (current Sun–Sat), Last week, Month. Paid: custom date range.
- **Filters** — Project filter; **Me** or **Other** (search and select one user to view their timesheet). Paid plans included custom range, Other user, and CSV export.
- **Export** — Export the grid to CSV (paid).
- **Settings** — Your choices (date range, project, selected user) are saved and restored when you open the dashboard.

---

## Support

**AP Technical Solutions LLC** — support@aptechnicalsolutions.com

For licensing and upgrades, contact your Jira administrator.
