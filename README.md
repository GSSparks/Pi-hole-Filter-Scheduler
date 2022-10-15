# Pi-Hole Filter Scheduler

I use these two sytemd timers and services to turn on and off Pi-Hole filters at certain times. I use this to deny all access to DNS after a certain time depending on the day of the week, and then turn access back on at 7:00am every morning.

The service executes a sqlite3 command on Pi-Hole's database setting enable to 1 or 0. 1 = filter on, and 0 = filter off.

<h2>How to use:</h2>
<ul>
  <li>Create a new group called 'internet-access-scheduler'</li>
  <li>Add clients that you want to schedule to this group</li>
  <li>Create a Pi-Hole regex filter to block all access [:alnum:].[:alnum:]</li>
  <li>Add the internet-access-scheduler group to this filter</li>
  <li>Edit the internet-access-schedule-off.service and internet-access-schedule-on.service files to reflect the filter you created. Put your newly created filter id where it says <b><i>id</b></i>. <b>HINT: </b>You can find the filter id by hovering your mouse over the regex on the Pi-Hole web interface.</li>
  <li>Finally, change the times in the internet-access schedule-off(on).timer to suit your needs.</li>
  <li>Sit back and smile while your children kick and scream because their internet all of the sudden was blocked at 7:00 pm.</li>
</ul>
Visit my post about this scheduler <a href="https://garysparks.info/scheduling-a-pi-hole-internet-access-filter/" >here</a> for step by step instructions.
