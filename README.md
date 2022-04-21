# Short Scripts and one-liners
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

#### Mound folder with sshfs
 
- Mount a folder or filesystem using SSH

##### example:
```
sshfs name@server:/path/to/folder /path/to/mount/point
```

- Add a prifix in to filenames bulk

##### example:
```
rename 's/^/prefix/' *
```

- Set an audible alarm when a IP comes online - realy works

##### example:
```
ping -i 60 -a IP_address
```

- List active connections and the number using NETSTAT

##### example:
```
netstat -ntu |  awk '{print $5}' |  cut -d: -f1 |  sort |  uniq -c |  sort -n
```

