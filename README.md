# command-linux

** SSH **
ssh [_remote_user_]@[_remote_ip_]

** TUNNEL **

ssh -p [_port_number_] -L [_server_port_]:[_server_ip_]:[_server_port_] [_remote_user_]@[_remote_ip_]

** SCP **  

scp -P [ _port_ ] [ _file_ ] user@[ IP ]:[remote path]  
  
** update-alternatives **

  update-alternatives --install /usr/bin/[_command_name_] [_command_name_] [_path_]/bin/[some command] 100
  
  update-alternatives --display [_command_name_]
