# Seagrass Monitoring System

An AI-powered system that lets volunteers photograph seagrass meadows with a mobile app, and automatically estimates the seagrass species and how much of the area they cover. Results are reviewed by administrators and shown on a public bilingual (Thai/English) web dashboard.

**Live website:** https://sgm-seagrass.vercel.app

<!-- After uploading screenshots, remove the "<!--" and "-->" markers around the lines below -->
<!--
![Web dashboard](images/web-map.png)
![Mobile app](images/mobile-app.png)
-->

## How it works

1. **Mobile app (Flutter):** volunteers take a photo with a 4x4 grid guide. The app records GPS location and works offline, then uploads photos once the phone has internet.
2. **Database and accounts (Supabase):** stores photos, locations, and user accounts, with access rules so each user only sees what they should.
3. **AI analysis:** a scheduled job triggers a Python worker on GitHub Actions. It splits each photo into a 4x4 grid and uses a deep learning model (EfficientNet-B0) to estimate the species in each cell and the overall seagrass coverage.
4. **Admin review:** administrators log in, review the results, and approve data before it is published.
5. **Web dashboard (React):** shows published survey results on an interactive map, in Thai and English.

## Tech stack

- **Web:** React, Vite, Leaflet
- **Mobile:** Flutter (offline queue with SQLite)
- **Backend:** Supabase (PostgreSQL, Auth, Row Level Security, Storage, Edge Functions)
- **AI pipeline:** Python, PyTorch, GitHub Actions
- **Hosting:** Vercel

## My role

Designed and built the whole system: the mobile app, the web dashboard and admin panel, the database, and the automated analysis pipeline. Trained and compared 5 deep learning models and connected the best one to the pipeline.

## Source code

The source code is kept in private repositories because it contains project infrastructure. Access is available on request, so please contact me.

**Nonpawit Chonchit** — Computer Science student, Prince of Songkla University, Phuket Campus
nonpawit.chonchit@gmail.com
