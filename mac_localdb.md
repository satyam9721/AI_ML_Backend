satyam_007@Satyams-MacBook-Air ~ % brew services start postgresql@17
==> Successfully started `postgresql@17` (label: sh.brew.postgresql@17)
satyam_007@Satyams-MacBook-Air ~ %
satyam_007@Satyams-MacBook-Air ~ % brew services start postgresql@17
Service `postgresql@17` already started, use `brew services restart postgresql@17` to restart.

> brew services list
> Name Status User File
> postgresql@17 started satyam_007 ~/Library/LaunchAgents/sh.brew.postgresql@17.plist
> postgresql@18 none satyam_007
> redis none

Test database connection - psql -h localhost -U ai_admin -d ai_ml_db
