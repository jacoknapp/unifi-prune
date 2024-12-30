# Unifi Console Prune script 
Prune Script for the unifi database. Stolen off of the old unifi forum. This will remove all data from before X days, and any devices before X days as configured in the file. It will not remove any device that has custom information saved in its fields (i.e. static ips, notes, or a rename). 

This script works for me continuously, but i'm ultimately not responsible for any damage that this may cause

## How to use

SSH onto your unifi conosle (settings -> control plane -> console, turn on ssh and set a password.)

SSH into your console. The username is root

Run the following commands. 

```
wget https://raw.githubusercontent.com/jacoknapp/unifi-prune/refs/heads/main/prune.js
mongo --port=27117 < prune.js
```

Once you've confirmed the output. set dryrun=false on line 6. 

You also can configure the number of days of info to keep by changing the variable days on line 2. Setting the days = 0 will prune all data from today, including old devices that don't have a static IP address, or a set name. 

If everything looks the way it should the run the command again
