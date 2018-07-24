# npm-install-ends-with-Killed

this commands changed configuration for swap


  sudo /bin/dd if=/dev/zero of=/var/swap.1 bs=1M count=1024
  
  sudo /sbin/mkswap /var/swap.1
  
  sudo /sbin/swapon /var/swap.1
  
  


Clear PageCache, dentries and inodes.


# sync; echo 3 > /proc/sys/vm/drop_caches 


Now we will be combining both above commands into one single command to make a proper script to clear RAM Cache and Swap Space.

# echo 3 > /proc/sys/vm/drop_caches && swapoff -a && swapon -a && printf '\n%s\n' 'Ram-cache and Swap Cleared'

OR

$ su -c "echo 3 >'/proc/sys/vm/drop_caches' && swapoff -a && swapon -a && printf '\n%s\n' 'Ram-cache and Swap Cleared'" root
