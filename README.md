# Crestron-IFTTT-Module
Crestron programming module that provides bi-directional communications with IFTTT
IFTTT Example Program Instructions

For the example program to operate properly it requires that you create a few IFTTT Applets.  In addition, please forward port 9691 from your router to your Crestron processor.  If you want to use a different port you will just need to change this in the IFTTT Applet below and in the parameter field of the IFTTT Crestron module. 

The IFTTT Applets required for the example program are as follows

Alexa trigger test - respond to a command from an Amazon Echo
Applet Title
If You say "Alexa trigger test", then make a web request

Trigger
Say a specific phrase
What phrase? - test
Action
Make a web request
URL - http://your_name.mycrestron.com:9691
Method - Post
Content Type - text/plain
Body - test|{{TriggeredAt}}|one|two

test - send an email without any data values sent from the Crestron system
Applet Title
If Maker Event "test", then send me an email at your_id@gmail.com

Trigger
Event Name - test3
Action
Send me an email
Subject - The event named "{{EventName}}" occurred on the Maker Channel
Body -
What: {{EventName}}<br>
When: {{OccurredAt}}<br>

test1 - send an email with 1 data value sent from the Crestron System
Applet Title
If Maker Event "test1", then send me an email at your_id@gmail.com

Trigger
Event Name - test1
Action
Send me an email
Subject - The event named "{{EventName}}" occurred on the Maker Channel
Body -
What: {{EventName}}<br>
When: {{OccurredAt}}<br>
Extra Data1: {{Value1}}<br>

test2 - send an email with 2 data values sent from the Crestron System
Applet Title
If Maker Event "test2", then send me an email at your_id@gmail.com

Trigger
Event Name - test2
Action
Send me an email
Subject - The event named "{{EventName}}" occurred on the Maker Channel
Body -
What: {{EventName}}<br>
When: {{OccurredAt}}<br>
Extra Data1: {{Value1}}<br>
Extra Data2: {{Value2}}<br>

test3 - send an email with 3 data values sent from the Crestron System
Applet Title
If Maker Event "test3", then send me an email at your_id@gmail.com

Trigger
Event Name - test3
Action
Send me an email
Subject - The event named "{{EventName}}" occurred on the Maker Channel
Body -
What: {{EventName}}<br>
When: {{OccurredAt}}<br>
Extra Data1: {{Value1}}<br>
Extra Data2: {{Value2}}<br>
Extra Data3: {{Value3}}<br>
