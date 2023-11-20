
`find / -perm -04000 2>/dev/null` will list files that have SUID or SGID bits set.

You can use GTFOBins ([https://gtfobins.github.io](https://gtfobins.github.io/)) and try to search for the programs you find in the list, if the program is listed with SUID you can use that to privilige escalation.