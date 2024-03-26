# df-mod3-sdm

Exercise 1: 
"Use Get-WinEvent to collect event logs from a remote or local computer. Redirect the output to a text file."
Get-WinEvent -ListLog * > logs.txt

"Use Get-Content and Select-String to search for specific text within the generated text file."
Get-Content logs.txt | Select-String -Pattern "error" | Out-File errors.txt

"Pipe Get-WinEvent to Where-Object to filter items in a pipeline."
Get-WinEvent -LogName "Security" | Where-Object {$_.Level -eq "Error"} | Out-File security_errors.txt

"Use Export-Csv command to export data to a CSV file."
Get-WinEvent -ListLog * | Export-Csv event_logs.csv -NoTypeInformation

Exercise 2:
"Use the mkdir command to create a new directory at the specified path."
mkdir C:\Different_Directory

"Use the copy command to copy a file from the source path to the destination path."
copy C:\Windows\System32\errors.txt C:\Different_Directory

Use the Get-Acl command to retrieve the access control list (ACL) for a file or directory.
Get-Acl C:\Different_Directory | Out-File acl.txt

Use the Export-Csv command to export data to a CSV file.
Get-Acl C:\Different_Directory | Export-Csv acl.csv -NoTypeInformation

Exercise 3:
Use the ConvertTo-SecureString command to encrypt sensitive data.












