# Question:
Split-piping
## Solution
Got really stuck trying to use | in this manner :/challenge/hack 2> | /challenge/the 1> | /challenge/planet.  
Didn't work at all.  
Found out that >() is equivalent to | so i changed it to /challenge/hack 2> >(/challenge/the) > >(/challenge/planet)  
So basically sent stderr to challenge/the and standard output to challenge/planet  
Flag:pwn.college{QJcziLYRO3Y73sWBqBrR0eMnL4U.dFDNwYDLzAzMykzW}
