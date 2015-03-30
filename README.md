# server_side_event
A repo to test the use of server_side events to implement a queueing system


###The general work-flow should be as follows
1. When a user requests robotsfor.me/CarlDemoInterface a request is sent to the server at CarlDemoInterfaceController.php

2. CarlDemoInterfaceController.php makes a request to the queue table, which contains user name in order of qeue. If the queue is empty, it directs the user to the /View/CarlDemoInterface/View.ctp with the buttons enabled. If the queue is not empty, it adds the user to the queue and directs the user to the /View/CarlDemoInterface/View.ctp with the buttons disabled and information abou the waitlist position and wait time

3. CarlDemoInterfaceController.php is then responsible for updating the clients every second with the new wait time, as well is their possibly new waitlist position, and whether or not they are not the active user. If they are the active user, the buttons should be enabled and they should be notivied
