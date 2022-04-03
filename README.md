# Short Scripts Collection
 
## Collection of quick and short scripts


## Rename multiple folders using powershell
 
'''
$i = 1
Get-ChildItem *.jpg | %{Rename-Item $_ -NewName ('1000100_{0:D4}.jpg' -f $i++)}
'''
