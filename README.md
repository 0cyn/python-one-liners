Small ones will be placed in the README, large ones get their own file. 

### Exit with 0 in a shell if a user response contains 'y', else exit with 1

`python3 -c "exit(int('y' in input('> ').lower())^ 1)"`
