# Short Scripts and One line commands collection
 
## Collection of useful short scripts


#### Rename multiple folders using powershell
 
- Innumerate though the file type you want to rename
- Pipe the result to **Rename-Item** Rename the files with a suffix () and add a 4 digit tag

##### example:
```
$i = 1
Get-ChildItem *.jpg | %{Rename-Item $_ -NewName ('1000100_{0:D4}.jpg' -f $i++)}
```


#### Alternative way to schedule command
 
- An alternative to using cron. This method allows a one-off task to be scheduled for a certain time.

##### example:
```
echo "ls -l" | at midnight
```