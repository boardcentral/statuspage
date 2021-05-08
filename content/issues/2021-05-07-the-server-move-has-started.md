---
title: Moving Servers
date: 2021-05-07 20:00:00
resolved: false
resolvedWhen: 
# Possible severity levels: down, disrupted, notice
severity: disrupted
affected:
  - Application
section: issue
---

The move to the new hosting provider has started.

## Please note:

While the move itself is expected to take less than two hours,
because the IP address will change for the server, DNS will
be have to be updated and that takes some time to propogate 
across the  Internet (anywhere from a few minutes to as much 
as a day or two) and is out of our control.

The application will remain available during the move in a
read only state.  Write access will automatically be restored 
once DNS has updated for you.

Update: 20:00 - App is readonly, moving the database

Update: 20:11 - Database move is complete. Deploying the application...

Update: 20:52 - Application is Deployed.  Updating DNS and SSL Certificate...

