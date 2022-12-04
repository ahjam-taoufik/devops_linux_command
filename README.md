### access server root a distance
  - /etc/ssh/sshd_config
  - assign yes to : PermitRootLogin
### add ssh-agent
  - show ssh agent :  ssh-add -l
  - add  ssh agent :  eval `ssh-agent`  (note : use backteck)
  - assign key to agent : ssh-add
  
  
  
### change hostname
 - show hostname : hostnamectl
 - change name in file : nano /etc/hostname
