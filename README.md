# linux command

* [SSH](#ssh)
* [TUNNELS](#tunnels)
* [SSH-KEYGEN](#ssh-keygen)
* [DU](#du)
* [SCP](#scp)
* [UPDATE-ALTERNATIVES](#update-alternatives)
* [LS](#ls)
* [Clear RAM Memory Cache, Buffer and Swap Space](#clear-ram-memory-cache-buffer-and-swap-space)
* [CRONTAB](#crontab)


## ssh

  ssh [_remote_user_]@[_remote_ip_]

## tunnels

  ssh -p [_port_number_] -L [_local_server_port_]:[_local_server_ip_]:[_local_server_port_] [_remote_user_]@[_remote_ip_]

  *with more connection*
  
  ssh -p [_port_number_] -L [_local_server_port_]:[_local_server_ip_]:[_local_server_port_] -L [_local_server_port_]:[_local_server_ip_]:[_local_server_port_] [_remote_user_]@[_remote_ip_]
  
## ssh-keygen

*Remove the RSA KEY. When display the message: "WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!", execute the command*

  ssh-keygen -R [_IP_]
  
## du

*Show the file/folder size*

  du -s -h _*_
  
  du -s -h /[_folder_]
  
  du -s -h [_file_]

## scp

  scp -P [ _port_ ] [_file_name_] [_user_]@[ _IP_ ]:[_remote path_]
  
## update-alternatives

  update-alternatives --install /usr/bin/[_command_name_] [_command_name_] [_path_]/bin/[some command] 100
  
  update-alternatives --display [_command_name_]
  
  update-alternatives --config [_comand_name_]

## ls

ls -la |grep [PARAM]\ [PARAM]

ex.: _ls -la |grep Feb\ 21_

## Clear RAM Memory Cache Buffer and Swap Space

https://www.tecmint.com/clear-ram-memory-cache-buffer-and-swap-space-on-linux/

1. Clear PageCache only.

  **#echo 1 > /proc/sys/vm/drop_caches && swapoff -a && swapon -a**
  
2. Clear dentries and inodes.

  **#echo 2 > /proc/sys/vm/drop_caches && swapoff -a && swapon -a**
  
3. Clear PageCache, dentries and inodes.

  **#echo 3 > /proc/sys/vm/drop_caches && swapoff -a && swapon -a**
  
## Crontab

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
