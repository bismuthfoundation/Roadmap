# Bootstrap automation

Proposal

## API endpoint

(static file updated after upload/test)

http://api.bismuth.live/bootstrap/pow.json

> Option: have a secondary api endpoint for redundancy

returns a list of dict with {url, height, (opt) timestamp, (opt) signature}

- url is the url of thhe ledger.tar.gz
- height the latest height of that archive
- timestamp the time of collection
- signature an optionnal sha signature of the file for integrity check (signed with a fixed trusted address to define)

oldest archives are auto deleted. Some old checkpoint may be kept.
(like 1 per month for the last 4 months, 1 per week for 4 last weeks, 1 per day for 4 last days)

## Node mods

Very light weight mod.  
Instead of having a single hardcoded url, hardcode the api endpoint(s).

- call the api
- order the urls by height and timestamp
- try to fetch the first one
- move to the next if not available (or, option, if too slow)

## Bootstrap manager

- Dedicated node (can be one or 2 for redundancy)
- crontab
- stop the node clean via "stop" command
- copy the db
- restart the node
- test the copy (TODO: dup the node start check for integrity)
- tar gz the data if test ok
- sign
- upload to one or several hosts (ex: S3, scaleway objects)
- update the api(s) json with new download urls
