Highland CPU Monitoring Script - Command reference guide.

This document provides a reference for managing the do\\\_cpu\\\_monitor.py script, which monitors CPU usage and restarts MySQL if CPU usage exceeds 95% threshold.

Start the Script in the Background

ohup /usr/bin/python3 /usr/local/bin/do\\\_cpu\\\_monitor.py > /var/log/do\\\_cpu\\\_monitor.log 2>&1 &

Check if the Script is Running

ps aux | grep do\\\_cpu\\\_monitor.py

Stop the Script

pkill -f do\\\_cpu\\\_monitor.py

Monitor Log

stail -f /var/log/do\\\_cpu\\\_monitor.log

View the Last 100 Log Entriestail -n 100 /var/log/do\\\_cpu\\\_monitor.log

If changes are made to the current script save them in the the file then Stop the script (pkill -f do\\\_cpu\\\_monitor.py) make sure it isn’t running (ps aux | grep do\\\_cpu\\\_monitor.py) then with the script stopped, run the new script so it will run in the background (nohup /usr/bin/python3 /usr/local/bin/do\\\_cpu\\\_monitor.py > /var/log/do\\\_cpu\\\_monitor.log 2>&1 &)Script Locationusr>local>bin>do\\\_cpu\\\_monitor.py