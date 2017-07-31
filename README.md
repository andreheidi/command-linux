# linux command

**ssh**

  ssh [_remote_user_]@[_remote_ip_]

**tunnel**

  ssh -p [_port_number_] -L [_server_port_]:[_server_ip_]:[_server_port_] [_remote_user_]@[_remote_ip_]

  *with more connection*
  
  ssh -p [_port_number_] -L [_server_port_]:[_server_ip_]:[_server_port_] -L [_server_port_]:[_server_ip_]:[_server_port_] [_remote_user_]@[_remote_ip_]
  
**ssh-keygen**

*Remove the RSA KEY. When display the message: "WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!", execute the command*

  ssh-keygen -R [_IP_]
  
**du**

*Show the file/folder size*

  du -s -h _*_
  
  du -s -h /[_folder_]
  
  du -s -h [_file_]

**scp**

  scp -P [ _port_ ] [_file_name_] [_user_]@[ _IP_ ]:[_remote path_]
  
**update-alternatives**

  update-alternatives --install /usr/bin/[_command_name_] [_command_name_] [_path_]/bin/[some command] 100
  
  update-alternatives --display [_command_name_]

**List file with filter**

ls -la |grep [PARAM]\ [PARAM]

ex.: _ls -la |grep Feb\ 21_

**Clear RAM Memory Cache, Buffer and Swap Space**

https://www.tecmint.com/clear-ram-memory-cache-buffer-and-swap-space-on-linux/

1. Clear PageCache only.

  **# sync; echo 1 > /proc/sys/vm/drop_caches**
  
2. Clear dentries and inodes.

  **# sync; echo 2 > /proc/sys/vm/drop_caches**
  
3. Clear PageCache, dentries and inodes.

  **# sync; echo 3 > /proc/sys/vm/drop_caches**
  
**Crontab**

Edit crontab

  _crontab -e_
  
  _*_ _*_ _*_ _*_ _*_ /path/file.sh
  
  **Descriptions of the crontab date/time fields**
  
    field     meaning        allowed values
    __________________________________________________________
      1       minute          0-59
      2       hour            0-23
      3       day of month    1-31
      4       month           1-12 (or names, see below)
      5       day of week     0-7 (0 or 7 is Sun, or use names)
