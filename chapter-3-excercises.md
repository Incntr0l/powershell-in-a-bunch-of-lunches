# Chapter 3 Lab Questions

1. Run Update-Help and ensure it completes without errors.
    - Update-Help
2. Can you find any cmdlets capable of converting other cmdlets' output into *html*?
    - Convert-ToHTML
3. Are there any cmdlets that can redirect output into a *file*, or to a *printer*?
    - Yes, the commands are *Out-File* for file output, and *Out-Printer* for printer output.
4. How many cmdlets are available for working with *processes*?
    - There are five, ***debug***, ***get***, ***start***, ***stop***, and ***wait***
5. What cmdlet might you use to *write* to get an event *log*?
    - ***Write-EventLog***
6. You've learned that aliases are nicknames for cmdlets; what cmdlets are available to *create, modify, export, or import* ***aliases***?
    - The commands in that order are as follows: ***New-Alias, Set-Alias, Export-Alias, and Import-Alias***
6. Is there a way to keep a *transcript* of everything you type in the shell, and save that transcript to a text file?
    - There is a way, the command is ***Start-Transcript -Path (path.txt)***
7. It can take a long time to retrieve all of the entries from the *Security Event Log*.How can you get only the 100 *most recent* entries?
    - Use the ***Get-EventLog -LogName Security -newest 100*** command.
8. Is there a way to retrieve all of the *services* that are installed on a remote computer?
    - Use the command ***Get-Service -computername (computername)***
9. Is there a way to see what *processes* are running on a remote computer?
    - Use the command ***Get-Process -computername (computername)***
10. Examine the help file for the **Out-File** cmdlet. The file created by this cmdlet default to a width of how many characters? Is there a parameter that would enable you to change that width?
    - The default width is ***80px***,  but it can be changed by using the ***-Width X*** parameter.
11. By default, **Out-File** will overwrite and existing file that has the same filename as what you specify. Is there a parameter that would prevent the cmdlet from overwriting and existing file?
    - There is a parameter, and that parameter is named ***-Append***
12. How could you see a list of all *aliases* defined in PowerShell?
    - Use the ***Alias*** command.
13. Using both an alias and abbreviated parameter names, what is the chortest command line that you could type to retrieve a list of running processes from a computer named **Server1**?
    - The shortest that I can think of is ***ps -computer Server1***
14. How many cmdlets are available that can deal with **generic objects**?
    - Type the command ***Get-Command -noun object*** to find out but I believe it is 14.
15. This chapter briefly mentioned *arrays*. What help topic could tell you more about them?
    - The command ***Get-Help about_Arrays*** will give you information about Arrays.

These are all the questions and answers for this chapter. Chapter 4 will be put into another **Markdown** file later.