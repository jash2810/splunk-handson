<h1>Splunk Hands-on by Jash</h1>
<p>This repository demonstrate some basics of splunk hands-on log analysis performed by me on splunk web tool. I used some log file from my windows computer and performed analysis on it.</p>

<h3>Total Events in the log file</h3>
<b>Query: Index = “main”</b>
<p>Count: 1385 Events</p>
<img src="https://github.com/jash2810/splunk-handson/blob/master/public/images/indexmain.png?raw=true" />

<p>Here, when we expand any log, we can have a detailed look as follow.</p>
<img src="https://github.com/jash2810/splunk-handson/blob/master/public/images/individualeventexpand.png?raw=true" alt="" srcset="">

<h3>Filter Task Category</h3>
<p>Task Category to filter: <b>Windows Update Agent</b></p>
<b>Query: index="main" "Task Category"="Windows Update Agent"</b>
<p>Count: 51 Events</p>
<img src="https://github.com/jash2810/splunk-handson/blob/master/public/images/filterwindowsupdateagent.png?raw=true" alt="" srcset="">

<h3>Task Category Statistics</h3>
<b>Query: index="main" "Task Category"="Windows Update Agent" | stats count by date_hour</b>
<p>Stats Found: 7</p>
<img src="https://github.com/jash2810/splunk-handson/blob/master/public/images/countbydatehourstats.png?raw=true" alt="" srcset="">
<p>For having deeper visualization in graphics, we can click on the visualization tab and have the following picture</p>
<img src="https://github.com/jash2810/splunk-handson/blob/master/public/images/countbydatehourvisual.png?raw=true" alt="" srcset="">

<h3>Created Demo Report</h3>
<p>The demo report was created of all the above observations for future reviews.</p>
<img src="https://github.com/jash2810/splunk-handson/blob/master/public/images/demoreport1.png?raw=true" alt="" srcset="">

<h3>Searching by Task Categories using OR query</h3>
<b>Query: index="main" "Task Category"="Service State Event" OR "Task Category"="Windows Update Agent"</b>
<img src="https://github.com/jash2810/splunk-handson/blob/master/public/images/orquery.png?raw=true" alt="" srcset="">

<h3>Task Categories Statistics for Windows Update Agent & Service State Event</h3>
<b>Query: index="main" "Task Category"="Service State Event" OR "Task Category"="Windows Update Agent" | stats count by "Task Category"</b>
<p>Statistics:</p>
<img src="https://github.com/jash2810/splunk-handson/blob/master/public/images/countbytaskcatstats.png?raw=true" alt="" srcset="">

<p>Pie chart view of Windows Update Agent & Service State Event</p>
<p>Windows Update Agent shares 37.078% off two events mentioned above while Service State Event shares 62.922%.</p>
<p>This shares are shown in the pie charts below</p>
<img src="https://github.com/jash2810/splunk-handson/blob/master/public/images/countbytaskcatvisual.png?raw=true" alt="" srcset="">
<img src="https://github.com/jash2810/splunk-handson/blob/master/public/images/countbytaskcatvisual1.png?raw=true" alt="" srcset="">

<h3>Created Dashboard</h3>
<p>Demo Dashboard holds two search reports we did in the above hands-on for further analysis.</p>
<img src="https://github.com/jash2810/splunk-handson/blob/master/public/images/dashboard.png?raw=true" alt="" srcset="">

<hr>