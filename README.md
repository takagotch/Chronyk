### chronyk
---
https://github.com/KoffeinFlummi/Chronyk

```py
from chronyk import Chronyk
t = Chronyk(1410531179.0)
t = Chronyk("May 2nd, 2016 12:51 am")
t = Chronyk("yesterday")
t = Chronyk("21. 8. 1976 23:18")
t = Chronyk("2 days and 30 hours ago")
t.ctime()
t.timestamp()
t.timestring()
t.timestring("%Y-%m-%d")
t.relativestring()
t.date()
t.datetime()


import sys
import chronyk

timestr = input("Please enter the date your were born: ")
try:
  date = chronyk.Chronyk(timestr, allowfuture=False)
except chronyk.DateRangeError:
  print("Yeah, right.")
  sys.exit(1)
except ValueError:
  print("Failed to parse birthdate.")
  sys.exit(1)
else:
  print("You ware born {}".format(date.relativestring()))

t = Chronyk("4 hours ago", timezone=0)
t.ctime()
t.timezone = -3600
t.relativeTime()
t.ctime()

t = Chronyk("4 hours ago")
t.relativestring(timezone=0)

t = Chronyk(1410524713.69, timezone=0
t.relativestring(timezone=chronyk.LOCALTZ))
```

```sh
pip install chronyk
```

```
```


