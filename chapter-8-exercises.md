# Chapter 8 Lab Exercises

Below is the answers to the lab exercises in the Powershell in a Month of Lunches book on Safari Books online.

1. Identify a cmdlet that will produce *a random number*
    - ***Get-Random*** will give you a random command.
2. Identify a cmdlet that will display the *current date and time*.
    - ***Get-Date***
3. What type of object does the cmdlet from task #2 produce? (What is the *tpye name* of the object object produced by the cmdlet?)
    - System.DateTime
4. Using the cmdlet from task #2 and **Select-Object**, display only the current day of the week in a table.
    - ***Get-Date | Select DayOfWeek***
5. Identify a cmdlet that will display information about installed *hotfixes*
    - ***Get-HotFix***
6. Using the cmdlet from task #5, display a list of installed hotfixes. Sort the list by the installation date, and display only the installation date, the user who installed the hotfix, and the hotfix ID. Remember that the column headers shown in a command's default output aren't necessarily the real property names - you'll need to look up the real property names to be sure.
    - ***Get-Hotfix | Sort InstalledOn | Select InstallationDate,InstalledBy,HotFixID***
7. Repeat Task #6, but this time sort the results by the HotFix description, and include the description, the hotfix ID, and the installation date. Put the results into a HTML file.
    - ***Get-HotFix | Sort Description | Select Description,HotFixID,InstalledOn | OUt-File HotFix.html***
8. Display a list o the 50 newest entries in the Security event log (you can use a different log, such as System or Application, if your Security log is empty). Sort the list with the oldest entries appearing first, and with entries made at the same time sorted by their index. Display the index, time and source for each entry. Put this information into a text file. 
    - ***Get-EventLog Security -newest 50 | Sort TimeGenerated,Index | Select Index,TimeGenerated,Source | Out-File Security.txt***