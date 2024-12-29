# Prune script 
Prune Script for the unifi database. Stolen off of the old unifi forum. 

This script works for me continuously, but i'm ultimately not responsible for any damage that this may cause

## How to use
Download the script to your unifi console client.

Run the following command. 

```
mongo --port=27117 < prune.js
```

Once you've confirmed the output. set dryrun=false on line 6. 

Then run the command again. If you set the days=0 it will remove all of your passed stats, and old devices pruning your database. Otherwise set the length in days accordingly. 
