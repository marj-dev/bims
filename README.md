# BIMS design preview (front-end only)

Static HTML, CSS and JavaScript for every screen of the Barangay Information Management System. No PHP, database or server is needed.

## Open it
Double-click `gallery.html`. It lists every page (public site, resident, admin, barangay officials and SK portals). Or open `index.html` for the landing page.

## Folders
- `*.html` in the root: public website (landing, about, services, officials chart, announcements, map, contact, register, log in)
- `resident/`, `admin/`, `officials/`, `sk/`: the four portals
- `assets/css/style.css`: design system (colors, buttons, forms, cards, tables, badges)
- `assets/css/public.css`, `landing.css`: public website and landing page
- `assets/css/admin.css`: portal layout (sidebar, topbar, cards, tables, timelines, steppers)
- `assets/css/resident.css`: resident extras (request form, notifications, dialog)
- `assets/css/preview.css`: placeholders used only in this preview (map/image boxes, toast, bars)
- `assets/js/ui.js`: preview behavior (menu, confirm pop-ups, toasts, search filters, mark as read)
- `assets/js/landing.js`: landing page effects and officials tabs
- `assets/js/request.js`: document request form behavior

## Design tokens (edit in `assets/css/style.css`, the `:root` block)
`--green-900/700/600/100/50` greens, `--navy` text, `--line` borders, `--warn/--danger/--info` status colors, `--radius`, `--font`.
The landing page also uses `--forest`, `--leaf`, `--gold` (in `landing.css`).

## Notes for the developer connecting the database
- All data on these pages is sample data. Buttons marked `data-demo` and forms only show a message.
- Keep class names so the CSS keeps working: `.badge-<status>` (pending, processing, ready, done, verified, rejected, ...), `.kpi`, `.panel`, `.filters`, `.kv`, `.timeline`, `.stepper`, `.table-wrap`, `.alert-*`.
- Status badges use `badge-` plus the database status value (for example `badge-needs_clarification`).
- `data-confirm="..."` on a button asks for confirmation before it proceeds.
