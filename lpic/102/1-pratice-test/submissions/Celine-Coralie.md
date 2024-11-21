1. ```journalctl```

2. /etc/resolv.conf

3. Password

4. ServerName:Allow

5. ::1 

6. -R

7. LD_LIBRARY_PATH

8. ```systemctl stop ssh```

9. ```route```

10. /var/cron/tabs

11. B

12. C

13. C

14. B

15. C

16. B

17. B

18. A

19. B

20. B

21. Open the ```crontab -e``` and add 0 2 * * 5 /path/to/backup.sh

22. -Hard links point directly to the data(inode) on the disk while soft links point to the path of a file.
    
    -With hard links, if the original file is deleted the data is not lost as far as there is still at least one hard link pointing to it while with soft links, if the original file id deleted the soft link becomes a broken link because it points to a path that no longer exists.
    
    -Hard links do not work across different filesystems while soft links can point to files or directories in another filesystem.
    
    -To create a hard link you input the command ```ln file.txt hardlink.txt```
    
    -To create a soft link you input the command ```ln -s file.txt softlink.txt```

23. auto eth0
 
    iface eth0 inet static
    
    address 192.168.0.155
    
    netmask 255.255.255.0
    
    gateway 192.168.0.1

    dns-nameservers 127.0.0.53

24. ```chmod -R u=rw,g=r,o=r /home/user``` for files.

    ```chmod -R u=rwx,g=rx,o=rx /home/user``` for directories.

25. Since programs that resolve names to numbers mostly use functions provided by the standard C library, these functions now read the /etc/nsswitch.conf file for instructions on how to resolve these names to their various numbers and this file also supports plugins.

    An example of a line in the file is "hosts:          files mdns4_minimal [NOTFOUND=return] dns"

26. ```groupadd sshusers
    
     sudo nano /etc/ssh/sshd_config
    
     AllowGroups sshusers
    
     sudo systemctl restart ssh
    
27. -iptables support ipv6 through ip6 tables while ufw supports ipv6 out of the box

    -iptables log to /var/log/syslog while ufw logs to /var/log/ufw.log

    -iptables have no graphical interface while ufw haas graphical interfaces like Gufw

    -iptables allow traffic by default while ufw denies all incoming traffic by default

    -iptables are low-level, complex and require manual rule configuration while ufw are high-level, simplified and user friendly  
