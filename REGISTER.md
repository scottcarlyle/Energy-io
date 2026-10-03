# App register - Energy-io

| App | Folder | Hosting | Database | Status | Notes |
|---|---|---|---|---|---|
| Master Console | apps/master-console | SharePoint | HQ Supabase | In design (UI-1 owed) | Admin only |
| Project Console | apps/project-console | SharePoint, one per project | Per-project Supabase | In design | Re-scoped Site Console |
| Field apps | apps/field | Netlify, one site per project | Per-project Supabase | In design | One generic bundle + per-project config.json |
| Final File Console Builder | apps/master-console | SharePoint | HQ Supabase | In design | Part of Master Console |
| PO System | apps/po-system | SharePoint: Procurement - General/Apps/PO System | None (Excel macro + config.json; lightyear_po_sync.py adds invoices) | Live, moving to Procurement site | PO Viewer.html + PO Master Console.xlsm |
| SharePoint File Management Console | apps/sfmc | SharePoint (HTML console, Graph via Entra app "File Management Console") | HH Inspections Supabase (for now) | In build (screens Rev A approved) | One-way Projects to Construction copy, on request |
