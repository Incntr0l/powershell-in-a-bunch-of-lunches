# Chapter 5 Lab Exercises

1. In the registry, go to ***HKEY_CURRENT_USER\software\microsoft\Windows\-currentversion\explorer***. Locate the *Advanced* key, and set it's *Don't Pretty Path* property to *1*.
    - Use *cd hkcu:* to get into the **HKEY** directory, then *cd .\software\microsoft\windows\currentversion\explorer*. After you cd to the above folder, use the command ***set-itemproperty -path advanced -PSPropert DontPrettyPath -value 1***.
2. Create a new directory called C:\Labs
    - ***mkdir -path C:\Labs***
3. Create a zero-length file named *C:\Labs\Text.txt* **(use New-Item)**
    - ***New-item -path C:\Labs\Test.txt***
4. Is it possible to use *Set-Item* to change the contents of **C:\Labs\Test.txt** tp *-TESTING*? Or do you get an error? if you get an error, why?
    - You get an error because it is not a supported operation.
5. Using the *Environmemt* provider, display the value of the system environment variable *%TEST%*.
    - 