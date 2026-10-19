# routines

Routine checklists, and the instructions that Claude scheduled tasks fetch and follow on every run.

## Checklists

| File | When |
|---|---|
| [daily.md](daily.md) | Every day |
| [weekly.md](weekly.md) | Saturday morning |
| [monthly.md](monthly.md) | Every month |
| [yearly.md](yearly.md) | December 31 and January 1 |

## Scheduled task instructions

Each scheduled task holds only a short bootstrap prompt: it fetches its file below from the main branch and follows it. The schedule and private values (name, email, home area) stay in the scheduled task, and the files refer to them by placeholder name (`USER_NAME`, `HOME_AREA`, `BOOKING_NAME`, `BOOKING_EMAIL`).

| Scheduled task | Schedule (JST) | Instructions |
|---|---|---|
| Weekly routine 🗓️ | Saturday 6:59 | [tasks/weekly-routine.md](tasks/weekly-routine.md) |
| Hair Salon | Saturday 8:50 | [tasks/hair-salon.md](tasks/hair-salon.md) |
| Hospital Visit 🏥 | Saturdays in March and September, 8:52 | [tasks/hospital-visit.md](tasks/hospital-visit.md) |
| Quit Smoking 🚭️ | Every day 23:00 | [tasks/quit-smoking.md](tasks/quit-smoking.md) |
| Uncomplete Tasks 🗒️ | Every hour at :50 | [tasks/uncomplete-tasks.md](tasks/uncomplete-tasks.md) |
