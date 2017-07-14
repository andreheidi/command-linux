# command-linux

**ssh**

  ssh [_remote_user_]@[_remote_ip_]

**tunnel**

  ssh -p [_port_number_] -L [_server_port_]:[_server_ip_]:[_server_port_] [_remote_user_]@[_remote_ip_]

  *with more connection*
  
  ssh -p [_port_number_] -L [_server_port_]:[_server_ip_]:[_server_port_] -L [_server_port_]:[_server_ip_]:[_server_port_] [_remote_user_]@[_remote_ip_]
  

**scp**

  scp -P [ _port_ ] [_file_name_] [_user_]@[ _IP_ ]:[_remote path_]
  
**update-alternatives**

  update-alternatives --install /usr/bin/[_command_name_] [_command_name_] [_path_]/bin/[some command] 100
  
  update-alternatives --display [_command_name_]
