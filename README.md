### access server root a distance
  - /etc/ssh/sshd_config
  - assign yes to : PermitRootLogin
### add ssh-agent
  - show ssh agent :  ssh-add -l
  - add  ssh agent :  eval `ssh-agent`  (note : use backteck)
  - assign key to agent : ssh-add
### install ansible (good method)
  - apt install python3-pip
  - pip3 install ansible==2.9.9  (install specific version )
  
  
  
### change hostname
 - show hostname : hostnamectl
 - change name in file : nano /etc/hostname
### show version 
 -  cat /etc/*ea*
