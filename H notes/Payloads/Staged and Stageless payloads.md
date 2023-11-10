Staged: 
1. Sends exploit shellcode all at once
2. Larger in size and won't always work
3. Have to be caught with multi/handler in msfconsole
Example: windows/x64/meterpreter/reverse_tcp

Stageless:
1. Sends payload in stages
2. Can be less stable
3. Can be caught with normal nc -lnvp
Example: windows/x64/meterpreter_reverse_tcp