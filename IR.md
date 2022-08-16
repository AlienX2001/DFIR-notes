# These are all windows event logs (evtx format)
![image](https://user-images.githubusercontent.com/64488123/184599765-14af2eb6-8deb-48af-842f-eb8bdc94c6df.png)

EID: 4688 means a new process has been created
EID: 4625 gets generated when there is a logon failure, and 4624 is when a logon is sucessful

![image](https://user-images.githubusercontent.com/64488123/184603555-65435c91-6d24-4f79-9412-84d6da33a90a.png)

![image](https://user-images.githubusercontent.com/64488123/184603863-b81f19b8-c43e-439b-9a1b-02c2d1686139.png)

For persistnece

![image](https://user-images.githubusercontent.com/64488123/184604851-775872f4-fa3b-4159-9320-8faf93b7f36c.png)


### A typical network logon - 4624
![image](https://user-images.githubusercontent.com/64488123/184600414-6269fbb2-d122-4bed-99b9-024880306782.png)

LogonType: 3 is classical network logon (more on this here https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventID=4624)

### A typical admin logon - 4672
![image](https://user-images.githubusercontent.com/64488123/184600831-27b684b4-a545-4e0a-83c6-834a79145564.png)

### Mounting of network share - 5140
![image](https://user-images.githubusercontent.com/64488123/184601045-3c54ecc3-d287-4a70-b90d-b59ad6217fcd.png)

### Scheduling a task - 106
![image](https://user-images.githubusercontent.com/64488123/184601381-593f165b-6015-4fc6-8d64-81a20ea5a683.png)

### Running a sched task - 200
![image](https://user-images.githubusercontent.com/64488123/184601777-3bae5910-2b82-4f0f-85c4-b13780319a9c.png)

### Completion of a sched task - 201
![image](https://user-images.githubusercontent.com/64488123/184602693-a18d89c3-986e-402f-a882-5bf8da28e745.png)

The ActionName could be a bit different from the actual process (.bat files may give cmd.exe because batch scripts are nothing but bunch of cmd.exe stuff)

### New process creation - 4688
![image](https://user-images.githubusercontent.com/64488123/184602351-c7df76cd-c8b0-4af0-a497-e9ae3a3ecc94.png)

TokenElevationType: 1936 means full token with no dropped privs(more on that here https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventID=4688)

### Sched Process cleaning up - 141
![image](https://user-images.githubusercontent.com/64488123/184602909-f4d86e37-d50f-410c-8131-b756c0033261.png)

### Logoff Event - 4634
![image](https://user-images.githubusercontent.com/64488123/184602970-af30e3a1-9850-47b0-86fb-984be0c426ed.png)

The logontype should be same as logon type during logon

### Service Installation - 7045
![image](https://user-images.githubusercontent.com/64488123/184604970-7e8bc294-2e2e-4756-a473-5685994e8da3.png)

This can be used as a persistance mechanism as malware can be installed as a windows service
Standard is System32, if not then its suspicious
