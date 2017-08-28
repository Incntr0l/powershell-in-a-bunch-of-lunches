# Chapter 6 Questions and Answers

Below is the questions and answers for the Chapter 6 lab in the "Powershell in a Month of Lunches" book on Safari Books Online.

1. Create two similar, but different, text files. Try comparing them by using *diff*. Run something like this: ***Diff -reference (Get-Content filename.txt) -difference (Get-Content filename2.txt).*** If the files have only one line of text that's different, the command should work.
    - Type in quotation marks one line, for example "I am a daemon", and pipe that to ***Out-File filename1.txt***, so the command should look like this: ***"I am a daemon | Out-File filename1.txt***. Do the same for the second file but name it something different. Then run the command that is stated in the question, and you should see a InputObject with what you have written in the two files and the SideIndicator chart.
2. What happens if you run *Get-Service | Export-CSV services.csv | Out-File* from the console? Why does that happen?
    - An error appears because there is no ***-Path*** paramater for the ***Out-File*** command.
3. Apart from getting one or more services and piping them to *Stop-Service*, what other means does *Stop-Service* provide for you to specify the service or services you want to stop? Is it possible to stop a service without using *Get-Service* at all?
    - There is a way, you can stop **Performance Logs** and **Alerts** by using the command ***stop-service sysmonlog***.
4. What if you want to create a pipe-delimited file instead of a comma-separated (CSV) file? You would still use the *Export-CSV* command, but what parameters would you specify?
    - After piping to ***Export-CSV*** and putting in the file name, use the ***Delimiter*** command followed by whatever you want it delimited by, so for piping you would use the pipeline symbol ( | ).
5. Is there a way to eliminate the *#* comment line from the top of an exported CSV file? That line normally contains type of information, but what if you want to omit that from a particular file?
    - There is a way, you can use the piped commend ***export-csv X.csv (X being the csv file name) -NoTypeInformation*** for removing the *#* comment line.
6. *Export-CliXML* and *Export-CSV* both modify the system because they can create and overwrite files. What parameter would prevent the from overwriting an existing file? What parameter would ask you if you were sure before proceeding to write the output file?
    - You can use the ***-Append*** parameter to prevent the overwrite of the file, while the ***-Confirm*** parameter would ask you to be sure if you wanted to proceed.
7. Windows maintains several regional settings, which include a default list separator. On the U.S. systems, that separator is a comma. How can you tell *Export-CSV* to use the system's default separator, rather than a comma?
    - You can use the ***Set-Culture*** command to change it to the System Default.