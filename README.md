Custom Polybar Modules
======================

Dependencies: [ttf-font-awesome](http://fontawesome.io/)

mail
----
Checks the server for unread mails. If there is any, polybar shows the number of unread mails and the appropriate icon.
```
1. Download the script
2. Make it executable (chmod +x)
3. If you are using gmail, change the server to: imap.gmail.com (port is the same)
4. Add the next part to your polybar config
```
```ini
[module/mail]
type = custom/script
exec = /path/to/mail.py
interval = 30
label =  %output%
click-left = exec firefox hotmail.com &
```

caffeine
--------
Provides a menu to control [caffeine-ng](https://gitlab.com/hobarrera/caffeine-ng)
```
X:      close the menu
PLAY:   activate
PAUSE:  deactivate
STOP:   kill
```
```ini
[module/caffeine]
type = custom/menu

label-open = 
label-close = 
label-open-padding = 0
label-close-padding = 1
label-separator = " "

menu-0-0 = 
menu-0-0-exec = caffeine -a
menu-0-1 = 
menu-0-1-exec = caffeine -d
menu-0-2 = 
menu-0-2-exec = caffeine kill
```
