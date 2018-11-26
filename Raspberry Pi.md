### Raspberry Pi Sheet

#### SSH Server

1. Install: `sudo apt-get install ssh`.
2. Start|stop|status: `sudo /etc/init.d/ssh {start|stop|reload|force-reload|restart|try-restart|status}`.
3. Enable/disable auto startup: `sudo update-rc.d ssh {disable|enable}`.

### Possible Issues

1. Locale problems like:

   ```
   perl: warning: Setting locale failed.
   ```

   - Solutions
     - If you are using ssh, make sure that the server you are connecting has the locale language files for the current selected locale on host machine you are using to connect to the server.[3]

#### References

1. https://www.thomas-krenn.com/en/wiki/Configure_Locales_in_Ubuntu
2. https://daker.me/2014/10/how-to-fix-perl-warning-setting-locale-failed-in-raspbian.html
3. https://www.linuxquestions.org/questions/linux-general-1/locale-cannot-set-lc_all-to-default-locale-no-such-file-or-directory-218622/