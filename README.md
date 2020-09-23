<div align="center">

## Read / Write information to the Windows XP / 2000 / NT \(?\) Event Log \(Admin Tools item \> Event Log\)


</div>

### Description

This simple code will write to the windows Event Logger, which can be read by going into Control Panel > Admin Tools > Event Logger. Useful for diagnostics after compile time, when you have no debug window.

YOU NEED TO ADD THE 'EVENT LOG' CONTROL FROM THE 'COMPONENTS' MENU TO YOUR FORM!
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Jon Barker](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/jon-barker.md)
**Level**          |Beginner
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |VB\.NET
**Category**       |[System Services/ Functions](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/system-services-functions__10-23.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/jon-barker-read-write-information-to-the-windows-xp-2000-nt-event-log-admin-tools-item-eve__10-66/archive/master.zip)





### Source Code

```
'ADD AN EVENTLOG TO YOUR FORM!
Dim Log As New EventLog()
'======== Adds an entry ========
Log.WriteEntry("Program Name", "Text you wish to add to the log, write here", EventLogEntryType.Error, "1", "1")
'======== Deletes entry ===
log.Delete("Program Name")
'===== Search for entry ===
Dim r as boolean
r = log.Exists("Name of program")
'r will return true, or false
'==== Get all entries ==
Dim r As Array
r = log.GetEventLogs()
'r is now an array containing all the entries of the log.
tHe_cLeanER
```

