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

- List active connections and the number using NETSTAT - Linux only

##### example:
```
netstat -ntu |  awk '{print $5}' |  cut -d: -f1 |  sort |  uniq -c |  sort -n
```

- Remove all but a certain file (in a directory)

##### example:
```
rm -f !(dontremove_filename.txt)
```

- List apps that are connected to the intenet at the moment

##### example:
```
 lsof -P -i -n |  cut -f 1 -d " "|  uniq |  tail -n +2
```

- Convert uppercase files to lowercase files - bulk

##### example:
```
 rename 'y/A-Z/a-z/' *
```

- Quick and live ssh network throughput test. Might need to install PV

##### example:
```
 pv /dev/zero|ssh $host 'cat > /dev/null'
```

- All IPS connected to the current machine

##### example:
```
 netstat -lantp |  grep ESTABLISHED | awk '{print $5}' |  awk -F: '{print $1}' |  sort -u
```
 