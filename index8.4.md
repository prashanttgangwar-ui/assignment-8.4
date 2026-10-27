## Aim
To create a responsive dashboard using CSS Grid for the outer page layout and Flexbox for arranging content inside statistic cards.

## Objectives
1. Create a dashboard with a header, sidebar and main content area.
2. Use CSS Grid to structure the overall page.
3. Create four statistic cards.
4. Use Flexbox to align icons, titles and numbers inside the cards.
5. Add a recent activity table.
6. Inspect the CSS Grid layout using browser DevTools.

## 1. Project Structure

Create a folder named `Assignment-8.4` with the following files:

```text
Assignment-8.4/
├── index.html
└── style.css
```

## 2. HTML Code — `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard | Admin Panel</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="dashboard">

        <!-- Header -->
        <header class="header">
            <div class="brand">
                <span class="brand-icon">▦</span>
                <h1>Admin Dashboard</h1>
            </div>

            <div class="header-right">
                <span class="welcome">Welcome, Admin</span>
                <div class="profile">A</div>
            </div>
        </header>

        <!-- Sidebar -->
        <aside class="sidebar">
            <h2>MENU</h2>

            <nav class="sidebar-nav">
                <a href="#overview" class="nav-link active">
                    <span>▦</span>
                    <span>Dashboard</span>
                </a>

                <a href="#statistics" class="nav-link">
                    <span>▤</span>
                    <span>Statistics</span>
                </a>

                <a href="#activity" class="nav-link">
                    <span>◷</span>
                    <span>Recent Activity</span>
                </a>

                <a href="#users" class="nav-link">
                    <span>♙</span>
                    <span>Users</span>
                </a>

                <a href="#settings" class="nav-link">
                    <span>⚙</span>
                    <span>Settings</span>
                </a>
            </nav>

            <div class="sidebar-bottom">
                <p>Dashboard Project</p>
                <small>Built with Grid and Flexbox</small>
            </div>
        </aside>

        <!-- Main Content -->
        <main class="main-content" id="overview">

            <section class="page-heading">
                <div>
                    <h2>Dashboard Overview</h2>
                    <p>Welcome back! Here is a summary of your website.</p>
                </div>

                <span class="date-badge">October 2026</span>
            </section>

            <!-- Four Statistic Cards -->
            <section class="stats-grid" id="statistics">

                <article class="stat-card users-card">
                    <div class="stat-top">
                        <div class="stat-icon">♙</div>
                        <span class="stat-label">Total Users</span>
                    </div>

                    <div class="stat-bottom">
                        <h3>2,450</h3>
                        <span class="stat-change">+12.5%</span>
                    </div>

                    <p class="stat-description">Compared to last month</p>
                </article>

                <article class="stat-card revenue-card">
                    <div class="stat-top">
                        <div class="stat-icon">₹</div>
                        <span class="stat-label">Total Revenue</span>
                    </div>

                    <div class="stat-bottom">
                        <h3>₹85,600</h3>
                        <span class="stat-change">+8.2%</span>
                    </div>

                    <p class="stat-description">Compared to last month</p>
                </article>

                <article class="stat-card orders-card">
                    <div class="stat-top">
                        <div class="stat-icon">▣</div>
                        <span class="stat-label">Total Orders</span>
                    </div>

                    <div class="stat-bottom">
                        <h3>1,280</h3>
                        <span class="stat-change">+6.4%</span>
                    </div>

                    <p class="stat-description">Compared to last month</p>
                </article>

                <article class="stat-card visitors-card">
                    <div class="stat-top">
                        <div class="stat-icon">◉</div>
                        <span class="stat-label">Total Visitors</span>
                    </div>

                    <div class="stat-bottom">
                        <h3>12,840</h3>
                        <span class="stat-change">+15.3%</span>
                    </div>

                    <p class="stat-description">Compared to last month</p>
                </article>

            </section>

            <!-- Recent Activity Table -->
            <section class="activity-section" id="activity">
                <div class="section-heading">
                    <div>
                        <h2>Recent Activity</h2>
                        <p>Latest updates from your dashboard</p>
                    </div>

                    <a href="#activity" class="view-all">View All</a>
                </div>

                <div class="table-wrapper">
                    <table>
                        <thead>
                            <tr>
                                <th>Activity</th>
                                <th>Date</th>
                                <th>Status</th>
                            </tr>
                        </thead>

                        <tbody>
                            <tr>
                                <td>
                                    <div class="activity-name">
                                        <span class="activity-icon blue">♙</span>
                                        <div>
                                            <strong>New user registered</strong>
                                            <small>Rahul Sharma</small>
                                        </div>
                                    </div>
                                </td>
                                <td>20 Oct 2026</td>
                                <td><span class="status completed">Completed</span></td>
                            </tr>

                            <tr>
                                <td>
                                    <div class="activity-name">
                                        <span class="activity-icon green">₹</span>
                                        <div>
                                            <strong>Payment received</strong>
                                            <small>Order #1024</small>
                                        </div>
                                    </div>
                                </td>
                                <td>19 Oct 2026</td>
                                <td><span class="status completed">Completed</span></td>
                            </tr>

                            <tr>
                                <td>
                                    <div class="activity-name">
                                        <span class="activity-icon orange">▣</span>
                                        <div>
                                            <strong>New order placed</strong>
                                            <small>Order #1025</small>
                                        </div>
                                    </div>
                                </td>
                                <td>19 Oct 2026</td>
                                <td><span class="status pending">Pending</span></td>
                            </tr>

                            <tr>
                                <td>
                                    <div class="activity-name">
                                        <span class="activity-icon purple">⚙</span>
                                        <div>
                                            <strong>Profile updated</strong>
                                            <small>Admin account</small>
                                        </div>
                                    </div>
                                </td>
                                <td>18 Oct 2026</td>
                                <td><span class="status completed">Completed</span></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </section>

            <!-- Additional Information -->
            <section class="bottom-panel" id="users">
                <div>
                    <h3>System Status</h3>
                    <p>All dashboard services are running normally.</p>
                </div>

                <span class="system-status">
                    <span class="status-dot"></span>
                    All Systems Operational
                </span>
            </section>

            <footer class="footer" id="settings">
                <p>&copy; 2026 Admin Dashboard. All rights reserved.</p>
            </footer>

        </main>

    </div>

</body>
</html>
```

## 3. CSS Code — `style.css`

```css
/* Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* General styling */
body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #f1f5f9;
    color: #1e293b;
    line-height: 1.5;
}

/* OUTER LAYOUT: CSS GRID */
.dashboard {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 240px minmax(0, 1fr);
    grid-template-rows: 75px minmax(0, 1fr);
    grid-template-areas:
        "header header"
        "sidebar main";
}

/* Header */
.header {
    grid-area: header;
    background-color: #ffffff;
    border-bottom: 1px solid #e2e8f0;
    padding: 0 30px;

    /* INNER LAYOUT: FLEXBOX */
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
}

.brand {
    display: flex;
    align-items: center;
    gap: 12px;
}

.brand-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 42px;
    height: 42px;
    border-radius: 10px;
    background-color: #2563eb;
    color: white;
    font-size: 25px;
}

.brand h1 {
    font-size: 1.35rem;
    color: #0f172a;
}

.header-right {
    display: flex;
    align-items: center;
    gap: 14px;
}

.welcome {
    color: #475569;
    font-size: 0.95rem;
}

.profile {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-color: #dbeafe;
    color: #1d4ed8;
    font-weight: bold;
    font-size: 1.1rem;
}

/* Sidebar */
.sidebar {
    grid-area: sidebar;
    background-color: #0f172a;
    color: white;
    padding: 28px 16px;

    display: flex;
    flex-direction: column;
}

.sidebar h2 {
    color: #94a3b8;
    font-size: 0.75rem;
    letter-spacing: 1.5px;
    padding: 0 14px;
    margin-bottom: 20px;
}

.sidebar-nav {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.nav-link {
    display: flex;
    align-items: center;
    gap: 13px;
    padding: 13px 14px;
    border-radius: 8px;
    color: #cbd5e1;
    text-decoration: none;
    transition: background-color 0.3s, color 0.3s;
}

.nav-link span:first-child {
    width: 22px;
    text-align: center;
    font-size: 1.2rem;
}

.nav-link:hover,
.nav-link.active {
    background-color: #2563eb;
    color: white;
}

.sidebar-bottom {
    margin-top: auto;
    padding: 20px 12px 0;
    color: #cbd5e1;
    border-top: 1px solid #334155;
}

.sidebar-bottom p {
    font-size: 0.9rem;
    margin-bottom: 5px;
}

.sidebar-bottom small {
    color: #94a3b8;
    font-size: 0.75rem;
}

/* Main content */
.main-content {
    grid-area: main;
    min-width: 0;
    padding: 30px;
}

.page-heading {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 15px;
    margin-bottom: 28px;
}

.page-heading h2 {
    font-size: 1.8rem;
    color: #0f172a;
    margin-bottom: 5px;
}

.page-heading p,
.section-heading p {
    color: #64748b;
    font-size: 0.95rem;
}

.date-badge {
    background-color: white;
    border: 1px solid #e2e8f0;
    color: #475569;
    padding: 10px 14px;
    border-radius: 8px;
    font-size: 0.9rem;
}

/* Four statistic cards using CSS Grid */
.stats-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 20px;
    margin-bottom: 30px;
}

/* Individual statistic card */
.stat-card {
    background-color: white;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    padding: 22px;
    box-shadow: 0 4px 12px rgba(15, 23, 42, 0.04);
    min-width: 0;
}

/* FLEXBOX aligns the icon and title */
.stat-top {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 22px;
}

.stat-icon {
    width: 45px;
    height: 45px;
    flex-shrink: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 10px;
    font-size: 1.5rem;
    font-weight: bold;
}

.users-card .stat-icon {
    background-color: #dbeafe;
    color: #2563eb;
}

.revenue-card .stat-icon {
    background-color: #dcfce7;
    color: #15803d;
}

.orders-card .stat-icon {
    background-color: #ffedd5;
    color: #c2410c;
}

.visitors-card .stat-icon {
    background-color: #f3e8ff;
    color: #7e22ce;
}

.stat-label {
    color: #64748b;
    font-size: 0.9rem;
}

/* FLEXBOX aligns the number and percentage */
.stat-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 10px;
}

.stat-bottom h3 {
    color: #0f172a;
    font-size: 1.7rem;
    overflow-wrap: anywhere;
}

.stat-change {
    color: #15803d;
    background-color: #dcfce7;
    padding: 4px 7px;
    border-radius: 5px;
    font-size: 0.75rem;
    font-weight: bold;
}

.stat-description {
    color: #94a3b8;
    font-size: 0.8rem;
}

/* Recent activity section */
.activity-section {
    background-color: white;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    padding: 24px;
    margin-bottom: 24px;
    box-shadow: 0 4px 12px rgba(15, 23, 42, 0.04);
}

.section-heading {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 15px;
    margin-bottom: 22px;
}

.section-heading h2 {
    color: #0f172a;
    font-size: 1.3rem;
    margin-bottom: 4px;
}

.view-all {
    color: #2563eb;
    font-size: 0.9rem;
    font-weight: bold;
    text-decoration: none;
}

.view-all:hover {
    text-decoration: underline;
}

/* Responsive table wrapper */
.table-wrapper {
    width: 100%;
    overflow-x: auto;
}

table {
    width: 100%;
    border-collapse: collapse;
    text-align: left;
    white-space: nowrap;
}

thead {
    background-color: #f8fafc;
}

th {
    color: #64748b;
    font-size: 0.8rem;
    font-weight: bold;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

th,
td {
    padding: 16px 12px;
    border-bottom: 1px solid #e2e8f0;
}

tbody tr:last-child td {
    border-bottom: none;
}

td {
    color: #475569;
    font-size: 0.9rem;
}

/* FLEXBOX aligns activity icons and text */
.activity-name {
    display: flex;
    align-items: center;
    gap: 12px;
}

.activity-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    width: 38px;
    height: 38px;
    border-radius: 8px;
    font-size: 1.2rem;
}

.activity-icon.blue {
    background-color: #dbeafe;
    color: #2563eb;
}

.activity-icon.green {
    background-color: #dcfce7;
    color: #15803d;
}

.activity-icon.orange {
    background-color: #ffedd5;
    color: #c2410c;
}

.activity-icon.purple {
    background-color: #f3e8ff;
    color: #7e22ce;
}

.activity-name strong,
.activity-name small {
    display: block;
}

.activity-name strong {
    color: #1e293b;
    font-size: 0.9rem;
}

.activity-name small {
    color: #94a3b8;
    font-size: 0.8rem;
    margin-top: 3px;
}

.status {
    display: inline-block;
    padding: 5px 10px;
    border-radius: 20px;
    font-size: 0.8rem;
    font-weight: bold;
}

.status.completed {
    color: #15803d;
    background-color: #dcfce7;
}

.status.pending {
    color: #b45309;
    background-color: #fef3c7;
}

/* Bottom information panel */
.bottom-panel {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 15px;
    background-color: white;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    padding: 20px 24px;
    margin-bottom: 24px;
}

.bottom-panel h3 {
    font-size: 1rem;
    color: #0f172a;
    margin-bottom: 4px;
}

.bottom-panel p {
    color: #64748b;
    font-size: 0.9rem;
}

.system-status {
    display: flex;
    align-items: center;
    gap: 8px;
    color: #15803d;
    font-size: 0.85rem;
    font-weight: bold;
}

.status-dot {
    width: 9px;
    height: 9px;
    border-radius: 50%;
    background-color: #22c55e;
}

/* Footer */
.footer {
    text-align: center;
    color: #94a3b8;
    font-size: 0.85rem;
    padding: 10px 0;
}

/* Tablet responsiveness */
@media (max-width: 1100px) {
    .stats-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .main-content {
        padding: 24px;
    }

    .stat-card {
        padding: 18px;
    }
}

/* Mobile responsiveness */
@media (max-width: 700px) {
    .dashboard {
        grid-template-columns: 1fr;
        grid-template-rows: auto auto minmax(0, 1fr);
        grid-template-areas:
            "header"
            "sidebar"
            "main";
    }

    .header {
        min-height: 75px;
        padding: 14px 18px;
    }

    .brand h1 {
        font-size: 1.05rem;
    }

    .brand-icon {
        width: 36px;
        height: 36px;
    }

    .welcome {
        display: none;
    }

    .sidebar {
        padding: 12px;
    }

    .sidebar h2,
    .sidebar-bottom {
        display: none;
    }

    .sidebar-nav {
        flex-direction: row;
        flex-wrap: wrap;
        gap: 8px;
    }

    .nav-link {
        flex: 1 1 130px;
        justify-content: center;
        padding: 10px;
        font-size: 0.85rem;
    }

    .main-content {
        padding: 18px 12px;
    }

    .page-heading h2 {
        font-size: 1.45rem;
    }

    .stats-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 12px;
    }

    .stat-card {
        padding: 14px;
    }

    .stat-top {
        align-items: flex-start;
        flex-direction: column;
        gap: 8px;
        margin-bottom: 16px;
    }

    .stat-bottom h3 {
        font-size: 1.35rem;
    }

    .activity-section {
        padding: 15px;
    }

    .bottom-panel {
        padding: 16px;
    }
}

/* Small mobile screens */
@media (max-width: 400px) {
    .stats-grid {
        grid-template-columns: 1fr;
    }

    .stat-top {
        flex-direction: row;
        align-items: center;
    }

    .stat-bottom {
        justify-content: flex-start;
        gap: 12px;
    }

    .date-badge {
        font-size: 0.8rem;
    }
}
```

## 4. Explanation of CSS Grid and Flexbox

### A. CSS Grid for the Outer Dashboard

The dashboard uses CSS Grid to divide the page into a header, sidebar and main content area.

```css
.dashboard {
    display: grid;
    grid-template-columns: 240px minmax(0, 1fr);
    grid-template-rows: 75px minmax(0, 1fr);
    grid-template-areas:
        "header header"
        "sidebar main";
}
```

- `display: grid` creates the outer grid layout.
- `grid-template-columns` defines a 240px sidebar and a flexible main content column.
- `grid-template-rows` defines the header row and the remaining page area.
- `grid-template-areas` assigns the positions of the header, sidebar and main content.

### B. Flexbox for Statistic Cards

Flexbox arranges the icon and title horizontally and aligns the statistic number with its percentage change.

```css
.stat-top {
    display: flex;
    align-items: center;
    gap: 12px;
}

.stat-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 8px;
}
```

- `display: flex` arranges child elements in a flexible row by default.
- `align-items: center` aligns items along the cross-axis.
- `justify-content: space-between` places available space between items.
- `gap` adds spacing between the elements.
- `flex-wrap: wrap` allows items to move to another line when necessary.

### C. Grid for Four Statistic Cards

```css
.stats-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 20px;
}
```

This creates four equal-width columns on wide screens. Media queries reduce the number of columns on smaller screens.

## 5. How to Test the Dashboard

1. Create `index.html` and `style.css` inside the `Assignment-8.4` folder.
2. Paste the respective code into each file and save them.
3. Open `index.html` in Chrome, or use the Live Server extension in VS Code.
4. Check the header, sidebar, four statistic cards and recent activity table.
5. Resize the browser to test the tablet and mobile layouts.
6. Verify that the table can scroll horizontally on narrow screens.

## 6. Inspect CSS Grid Using DevTools

1. Open the dashboard in Google Chrome.
2. Right-click the page and select **Inspect**, or press `F12`.
3. Open the **Elements** panel.
4. Select the element with the class `dashboard`.
5. In the Styles panel, locate `display: grid`.
6. Click the **grid badge** beside the CSS Grid declaration if Chrome displays one.
7. Use the Grid overlay to inspect the columns, rows and layout areas.
8. Select `.stats-grid` to inspect the grid containing the four statistic cards.

The exact position of the Grid controls can vary between Chrome versions.

## 7. Expected Output

The completed dashboard contains:

- A top header with the dashboard title and admin profile.
- A dark sidebar with navigation links.
- Four statistic cards showing users, revenue, orders and visitors.
- A recent activity table with dates and status labels.
- A system-status panel and footer.
- A responsive design that adapts to desktop, tablet and mobile screens.

## 8. Result

A responsive admin dashboard was created successfully using HTML5 and CSS. CSS Grid was used for the outer page layout and the statistic-card arrangement, while Flexbox was used to align icons, labels, numbers and other elements inside the cards. The layout can be inspected using the browser's DevTools Grid inspector.

