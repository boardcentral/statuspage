---
title: Database Maintenance
date: 2020-05-17 9:45:00
resolved: true
resolvedWhen: 2020-05-17 11:40:00
# Possible severity levels: down, disrupted, notice
severity: notice
affected:
  - Application
section: issue
---

Just a heads up that we're starting some maintenance on the
servers.  Access may go down from time to time but only last
a minute or so at a time.

I'll update my progress here as I go.  I expect it to all take
less than an hour.

Update: 10am  Issue with new configs... deploying a fix should
        be up momentarily.

Update 10:24 Wow... rolled back to previous version and app
       is running again.  Continuing maintenance

Update: 11:39 Maintenance complete (but if anything could go
        wrong it did!

We've moved from sqlite3 to postgres and are now using B2
for file upload storage.  This will help us scale in the
future.

Post mortem.  A number of things went wrong and here's what
we're going to change to reduce the chances of it happening
again:

* Tag and run a known good image (instead of latest)
* Run a quick shell with latest and make sure it loads before updating
  the 'current' tag. (and/or use a staging environment and canary deploys
  in the future).
* Only change one piece of infrastructure at a time!


Vince
