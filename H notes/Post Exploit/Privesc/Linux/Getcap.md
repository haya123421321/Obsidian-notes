
We can use the `getcap` tool to list enabled capabilities.

`getcap -r / 2>/dev/null`

If one of the programs has cap_setuid on it use the [[Suid]] method