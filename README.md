### access server root a distance
  - /etc/ssh/sshd_config
  - assign yes to : PermitRootLogin
### generate ssh key
  - execute command : ssh-keygen
  - go to /root/.ssh/
  - copy key public and past in server distant by command : ssh-copy-id -i ~/.ssh/mykey user@host
  - use this key for access server : ssh -i ./private_key root@host_IP

### add ssh-agent
  - show ssh agent :  ssh-add -l
  - add  ssh agent :  eval `ssh-agent`  (note : use backteck)
  - assign key to agent : ssh-add

  
  
  
### change hostname
 - show hostname : hostnamectl
 - change name in file : nano /etc/hostname
### show version 
 -  cat /etc/*ea*
