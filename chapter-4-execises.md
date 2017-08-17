# Chapter 4 Execises

1. Display a list of running processes
    - ***Get-Process***
2. Display the 100 most recent entries from the **Application event log**.
    - ***Get-Eventlog -LogName Application -Newest 100***
3. Display a list of all commands that are of the **cmdlet** type.
    - ***Get-Command -CommandType Cmdlet***
4. Display a list of all aliases
    - ***Alias***
5. Make a new alias, so you can run *np* to launch **Notepad** from a PowerShell promt.
    - ***New-Alias -Name np -Value Notepad.exe***
6. Display a list of services that begin with the letter *"M"*.
    - There are two commands that can get services that start with the letter *"M"*, those are: ***Get-Service M(wildcard)*** and ***Get-Service -Name M(wildcard)***
7. Display a list of all *Windows Firewall* Rules.
    - ***Get-NetFirewallRule***
8. Display a list of only *inbound Windoes Firewall* rules.
    - ***Get-NetFirewallRule -Direction Inbound***