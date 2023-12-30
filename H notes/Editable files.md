Group specific files
`find / type f -group $(id -ng | getent group $(id -g) | cut -d: -f1) 2>/dev/null`

User specific files
`find / type f -user $(whoami) 2>/dev/null`