# airGap.py
### version 0.9.1

By Patrick Riggs (github: sanpatricio)

airGap.py is a Python script that assists you with suggesting files that may be ready for copying between two air-gapped systems or networks.  It recursively looks through a directory for files modified within N days ago, then offers a couple ways to proceed with the results: display on screen, write to log file, or copy identified files to a directory

Example session:

```
me@handoftheking $ ./airGap.py 
In which directory do I begin my search: ./testing
How many days back am I looking: 1
Searching for files modified since 2016-09-29 21:04:48.908844
Found 1 modified files in the last 1 day(s).
Actions:
[1] Nothing, return to command line.
[2] Collect copies of hits in ./20160930-210448-nominatedForMigration/
[3] Write these results to ./20160930-210448-airGappy-Report.txt
[4] Write these results to the screen
What should I do with them [1]: 4
2016-09-30 19:30:./testing/file.txt
```

## Installation
Simply drop airGap.py into any directory to which you have write access, ensure it is executable, and verify the first line of the script points to your local copy of Python (/usr/bin/python).  Python 2.7 was used to write airGap.py.

## To-Do
1. Arrange for input gathered through the step-by-step to also be passed via command line argument for possible cron-ination.
