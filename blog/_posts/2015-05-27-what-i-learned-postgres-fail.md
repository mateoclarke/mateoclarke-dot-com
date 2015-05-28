---
layout: post
title: What I Learned Yesterday - Postgres Fails
---

*Every day at AcademicWorks, the Engineering Team has a Dev Sync where we share something we learned from the day before. Often times we'll hear about some new movie, a cool Kickstarter project, or an interesting ruby gem. Our VP of Engineering has issued a challenge to our team. Whoever can teach something they learned from the day before that is technical in nature and directly related to our work for 20 consecutive days will win a prize. Here is what I learned yesterday...*

# PostgreSQL Fails, now what?

I was having issues starting up my environment. Our Rails scholarship app depends on a separate indexer app that runs a bunch of tasks with [foreman](http://theforeman.org/).

After digging in a bit and with much guidance from my primary mentor on the team, all signs pointed to my Postgres server having died.

## What I learned

- `$ ps aux | grep postgres` checks to see what programs are running postgres. If you don't get anything back, that points to your postgres server being MIA.
- The Unix `tail` command gets you the last 10 lines of a file. If you run this command on your server log, it can give you better details about what process failed and why. 
	- EX: `$ tail -n 50 /usr/local/var/postgres/server.log`
- Postmaster (`postmaster.pid`) is postegres' process- id file. If you already have a `postmaster.pid` file in your postgres folder, you might have issues.
	- To delete the redundant file: `rm -rf /usr/local/var/postgres/postmaster.pid`
- Now my `foreman start` works and I can start coding on the Rails app. Enough with the [yak shaving](http://en.wiktionary.org/wiki/yak_shaving). 


![Yak loop](http://media.giphy.com/media/11KL2DW3ddivK/giphy.gif)

