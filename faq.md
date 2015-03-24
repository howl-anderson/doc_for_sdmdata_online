# FAQ
## Q: It says species name csv must encoding in ASCII, What's this meaning?
A: Species name is latin character for species, there are no special character. If it have it means species name is wrong. Sometime user using other encoding to lead this error, in this suitation, user can use Windows (R) buildin notepad to translate, open the file and then save as text file, choose encoding in 'ANSI' before save it.

## Q: My task status was 'PENDDING', what's this meaning?
A: For support multi-user online, we using queue to manage task, something job worker (fetch data from GBIF, cross check point worker) are realy buniness. User's comming task have to wait in the queue, this status is called 'PENDDING'. When worker is ready, user's task will be executed in order.

## Q: My task failed with status 'FAIL', what's this meaning?
A: Collect data from GBIF need network, something network is not always working, user's task cannot connect to GBIF, this will lead it fall after cetain retry. User can put the task to queue again when it failed.

## Q: Cross check work are realy very slow?
A: Cross check is a hard job for computer (more harder for humam being, ofcourse). It take a lot of CPU and memory to runing a cross check worker. And cross check always have most workload than other worker. so this is why it works very slow.
