# Pi-Hole Filter Scheduler

I use these two sytemd timers and services to turn on and off Pi-Hole filters at certain times. I use this to deny all access to DNS after a certain time depending on the day of the week, and then turn access back on at 7:00am every morning.

The service executes a sqlite3 command on Pi-Hole's database setting enable to 1 or 0. 1 = filter on, and 0 = filter off.

<ul>
<li>The Pi-Hole Filter to block all access is [:alnum:].[:alnum:]</li>
</ul>
