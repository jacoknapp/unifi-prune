# Prune script 
Prune Script for the unifi database. Stolen off of the old unifi forum. 

This script works for me continuously, but i'm ultimately not responsible for any damage that this may cause

## How to use

SSH onto your unifi conosle (in the control center, turn on ssh and set a password.)

Run the following commands. 

```
wget https://raw.githubusercontent.com/jacoknapp/unifi-prune/refs/heads/main/prune.js
mongo --port=27117 < prune.js
```

Once you've confirmed the output. set dryrun=false on line 6. 

Then run the command again. If you set the days=0 it will remove all of your passed stats, and old devices pruning your database. Otherwise set the length in days accordingly. 
