Steps after getting shell
```bash
python3 -c 'import pty;pty.spawn("/bin/bash")'
export TERM=xterm
```

`ctrl + z`

```bash
stty raw -echo; fg
stty rows 38 columns 116
```
