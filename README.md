## copie past file from windows to linux
  
  scp -rv demo-site.zip timitar@192.168.1.106:/home/timitar/Desktop

## Regex
  - search in file file1.txt word 'taoufik' : grep taoufik file1.txt
  -  search in file file1.txt word 'taoufik' (ignore case): grep -i taoufik file1.txt
  -  search in file file1.txt word 'taoufik' (with line number): grep -n taoufik file1.txt
  - search in list word begin by 'Do' : ls -l | grep Do
  - search world begin by world 'hello' : grep -in ^"hello" file.txt
  - search world  end by world  'hello': grep -in "hello"$ file.txt
  - search world contains 'hello' : grep -in "hello." file.txt
  - search world contains 'hello' and at the end "m" in the seventh place  : grep -in "hello.m" file.txt
  - search world contains zero or multiple "o" in 'hello' : grep -in "hello*m" file.txt


## permission
   - chown user_name file_name
   - chgrp group_ame filename
   - chmod u+x (or u-x for remove) file_name (u=user)
   - chmod g+x (or g-x for remove) file_name (g=group)
   - chmod o+x (or o-x for remove) file_name  (o=other)
   - chmod u+rwx (or u=rwx) (or u=--- for remove) file_name
   - chmod g=x, o=r file_name
   - chmod u+x * (this command for all file)
   - chmod -R a+x folder_name (you can add permission in recursive : folder and file ) 
   - chmod -R a+X folder_name (you can add permission in recursive :only folder  ) 
   # octal method :
      user| group| other
     ----------------
      rwx | rwx  |  rwx
      421 | 421  |  421
      example : 
       - chmod 643 file_name (6=>4+2  4=>4   3=>2+1 )

## syntaxe command line :
  - command options arguments (ex : ls -l /etc)

## ssh
  ### 
    - yum install openssh-server
    - /sbin/service sshd status


## change password
  ### from your compte
    - passwd
  ### change password user from root
    - passwd user_name
## add user from root
   - useradd name_user
## groups commands
   - add group : groupadd group_name
   - show groups : cat /etc/group
   - add user in group : usermod -aG group_name user_name (a: append  G: second group)
   - add user in group : usermod  G group_name2 user_name ( G: second group , change group_name by group_name2)
   - add user in groups : usermod  G group_name1,group_name2,group_name3, user_name 
## some command
   - show all informations from specific user : getent passwd user_name
   - show all informations from specific user (privilege for root) : getent shadow user_name
   - show all id : id
   - show only id : id -u
   - show user name :id -un (or :  whoami)
   - show connect users in this moment : w (or : users)
   - add user in sudoers : in the root mod tape: sudo usermod -a -G sudo user_name (and restart machine)
   - whoami
   - w  : all user online in server
   


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

  
  
### info system
   - uname -a
### change hostname
 - show hostname : hostnamectl
 - change name in file : nano /etc/hostname
### show version 
 -  cat /etc/*ea*
### show memory
 - free -h
### disc space
 - df -h
###  stress server 
 - install : apt install stress
 - run for example : --cpu 1 --timeout 30
 - show result in terminal by : htop (install htop if don't you have it)
