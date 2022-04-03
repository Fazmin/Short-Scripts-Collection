# Short Scripts Collection
 
## Collection of useful short scripts


#### Rename multiple folders using powershell
 
- Inumarate though the file type you want to rename
- Pipe the result to **Rename-Item** Rename the files with a suffix () and add a 4 digit tag

##### example:
```
$i = 1
Get-ChildItem *.jpg | %{Rename-Item $_ -NewName ('1000100_{0:D4}.jpg' -f $i++)}
```
