Small ones will be placed in the README, large ones get their own file. 

All of these assume they're running in a shell context

### Exit with 0 in a shell if a user response contains 'y', else exit with 1

`python3 -c "exit(int('y' in input('> ').lower())^ 1)"`

### Check if an IP/port is up on the network, Exit 0 if so, 1 if it hits the timeout.

`python3 -c "check = lambda x,y,z: (lambda s: (s.settimeout(z), s.connect((x, int(y))), s.close(), True))(__import__(\"socket\").socket(__import__(\"socket\").AF_INET,__import__(\"socket\").SOCK_STREAM));check(__import__(\"socket\").gethostbyname('$IP'),$PORT,$TIMEOUT)"
