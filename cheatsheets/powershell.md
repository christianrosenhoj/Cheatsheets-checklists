Powershell Cheatsheet
===========

# Handy Commands
| Command							| Meaning
| :---								| :---
| `gsv | clip`						| Clips output of `gsv` to the clipboard
| `get-help | gm`					| Check what object `get-help` is
| `ls | get-object name`			| Take only one column (in this case name)
| `-Whatif`							| Whatif I do something? Check without running

# Some examples
| Command							| Meaning
| :---								| :---
| `get-process | export-csv c:\proc.csv` | creates a file with all the processes
| `get-process | out-gridview`		| nice gridview
| `get-service | convertto-html -Property Displayname, status | out-file c:\info.html` | html page
| `get-pssnapin -registered` 		| find registered snappins
| `add-pssnapin sql*`				| example of adding sql* snapin (use get-command -module sql* to check contents)






# Get some help 
| Command								| Meaning
| :---									| :---
| `Update-Help -Force`					| Update the help
| `Save-Help`							| Save the help to a local file
| `man`									| Scrollable
| `help`								| Alias
| `Get-Help "*keyword*"` 				| Get help
| `Get-Help Get-*` 						| Get all commands which start with "Get-"
| `Get-Help`							| `-ShowWindow`
| 										| `-Detailed`
|										| `-Examples`
| 										| `-Full`
| 										| `-Online`
| 										| `-ShowCommand`
| `Get-Help -Category Provider`			|
| `Get-verb`							| Get the verbs used in PowerShell
| `Get-Alias -Definition get-process` 	| Get all aliases for `Get-Process`
| `Get-Help About_*`					| Get all the about topics
| `Get-Process | Get-Member`			| Get all the methods, properties,... of the object
| `Get-Command -Module AD*`				| Get all commands from modules which start with AD

# Export
| Command			| Meaning
| :---				| :---
| `Export-csv`		|
| `Export-Clixml`	|
| `Out-File`		|
| `Out-Printer`		|
| `Out-GridView`	|
| `Out-File`		|
|					|
| `ConvertTo-Csv`	|
| `ConvertTo-Html`	|

# Create new property

| Command																| Meaning
| :---																	| :---
| `Select -Property @{n(ame)='ComputerName';e(xpression)={$_.name}}`	| Creates a new property called `ComputerName` from the existing property `Name`
| `Select -ExpandProperty name`											| Return the property in a array

# WmiObject & CimInstance

# Remoting
| Command																| Meaning
| :---																	| :---
|`Invoke-Command -ComputerName dc {Restart-Computer}`					| Execute the command on specific computers
| `icm dc {Restart-Computer}`											| Short version

# Execution Policy

| Command			| Meaning
| :---				| :---
| `Restricted`		|
| `Unrestricted`	| Run any script **(not recommended)**
| `AllSigned`		|
| `RemoteSigned`	| Only run scripts that are remote signed
| `Bypass`			|
| `Undefined`		|

# Powershell Remote Session

| Command										| Meaning
| :---											| :---
| `Get-PSSession`								| Get open sessions
| `$sessions = New PSSession -ComputerName dc`	| Open session
| `icm -Session $sessions {...}`				| Execute command in script block to all sessions





Special thx to JurgenVM (in particular), Fabien Dibot, SteveX and various others!