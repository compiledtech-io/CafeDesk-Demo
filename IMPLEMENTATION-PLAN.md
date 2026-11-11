# CafeDesk Demo — Steps and Phases

## Phase 1 — Create the workspace
1. Use the existing `CafeDesk` folder as the project root.
2. Add `CafeDesk.code-workspace` so the folder opens directly in VS Code.
3. Keep the demo self-contained: no server, package installation, or external data service.

## Phase 2 — Build the mobile-first foundation
1. Create the shared browser app in `index.html` using semantic HTML, CSS, and JavaScript.
2. Apply the cafe color palette, Inter-first typography, rounded cards, and a centered 430px mobile layout.
3. Add a role-selection landing screen that opens separate `client.html` and `admin.html` sites.
4. Show portal-specific bottom navigation and a consistent brand/title header.
5. Make dialogs, buttons, and inputs touch-friendly and responsive.

## Phase 3 — Seed and persist demo data
1. Seed 12 sample customers, 12 menu items, 30 orders across the last 14 days, and three past campaigns.
2. Seed representative stamp/reward data and calculate dates relative to the current date.
3. Store app state in localStorage; restore it on load and provide a reset action.
4. Keep all totals and dashboard metrics derived from the current state.

## Phase 4 — Implement staff workflows
1. Build the table-order menu, demo table selection/scan, cart sheet, customer lookup, validation, and order confirmation.
2. Update customer visits and coffee stamps when orders are placed.
3. Show customer-facing stamp and reward progress in the Customer portal; keep stamp awards and reward redemption in Admin.
4. Build lapsed-customer offers, WhatsApp link sequencing, campaign logging, and automation toggles in Admin.

## Phase 5 — Implement owner reporting and feedback
1. Add live KPIs, seven-day order bars, top-item counts, offer history, and review metrics.
2. Add empty states, accessible labels, and a toast for each user action.
3. Keep WhatsApp and Google Review URLs clearly editable demo constants.

## Phase 6 — Verify the deliverable
1. Open `client.html` and `admin.html` in a modern browser; no build step is required.
2. Check that the Customer site contains only order, My Stamps, and Rewards tabs.
3. Check that the Admin site contains only Stamps, Rewards, Come Back, and Dashboard tabs.
4. Refresh each site to verify localStorage persistence.
5. Use **Reset demo data** in Admin to restore the original sample state.

## Current implementation
- `index.html` contains the complete front-end demo and sample data.
- `client.html` opens the customer site with ordering, personal stamp progress, and rewards/reviews.
- `admin.html` opens staff stamp management, reward redemption, come-back campaigns, and the dashboard.
- Both sites share localStorage demo data; each site removes unrelated screens and navigation from its loaded app.
- The Customer site looks up one demo customer at a time; the Admin site can browse all customers.
- Admin access is a demo UI separation, not authentication or a production security boundary.
- `CafeDesk.code-workspace` opens this folder as the CafeDesk workspace.
- No real payments, customer messaging, backend, or external API calls are configured.
