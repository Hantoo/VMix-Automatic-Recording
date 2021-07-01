# VMix-Automatic-Recording
Automatic recording for VMIX based on day of the week and time of day

Copy the contents and paste it into a new script file within VMix. Settings > Scripting > New.
Within the script there are instructions on how to use it.

Change the line that matches below (line 16) to suit your need. The syntax is as follows: {DAY, START HOUR, START MIN, END HOUR, END MIN}  
Dim recordingSchedule(,) As Integer = {{0,11,00,13,00},{0,13,36,13,37},{0,13,40,13,43},{0,18,40,19,30},{1,01,40,02,00},{1,09,30,10,30}}

If I only wanted to record the 6:30PM service on a Sunday the line would look as follows:

Dim recordingSchedule(,) As Integer = {{0,18,30,20,00}}

If I also wanted to record Alpha on Tuesdays at 19:00 until 21:00 it would look like:

Dim recordingSchedule(,) As Integer = {{0,18,30,20,00},{2,19,00,21,00}}

Save the script with a name.

Create a webbroswer input with the URL provided in the script - Line 6. Replace "[ScriptName]" with the name of the script. Ensuring to remove the square brackets. This will automatically run the script when loading the input - which is upon load of the file / start up.

Recordings can not pass from one day to another, so must be stopped at 23:59 and start at 00:00
