# DevOps Bootcamp (# for H1, ## H2, ### H3, - for bullet points, **for bold**, for single line of code/command, ```for block of code```)


## Introduction to DevOps and why DevOps/benefits

- Work together, automation, share responsibilities and deploy infrastructure as code
-
-
-
-


### Linux commands that also work on Bash
- Create a Dir `mkdir name_of_the_dr`
- Go inside the Dir `cd name of the dir`
- Come out of the Dir `cd ..` or `'cd'`
- Who am I `uname -a`
- Where am I `pwd`
- Create a file `touch name_of_the_file` or `nano file_name` you land inside the file
- Exit from nano `CTRL + X` then `Y` then `ENTER`
- List all `ls -a` or `ls`
- To see the content of the file on the terminal `cat file_name`
- Clear your screen `clear`
- Delete a folder `rm -rf name_of_the_folder`
- Delete a file `rm name_of_the_file`
-Delete multiple files `rm name_of_the_file1 name_of_the_file2`


## Vagrant
- To initialise vagrant -> vagrant init
- To start vagrant -> vagrant up
- To destroy vagrant -> vagrant destroy
- To SSH into vagrant -> vagrant ssh
- To reload vagrant -> vagrant reload



## Permissions



Linux permissions dictate 3 things you may do with a file, read, write and execute. They are referred to in Linux by a single letter each.



__r__ (read) - you may view the contents of the file.
__w__ (write) - you may change the contents of the file.
__x__ (execute) - you may execute or run the file if it is a program or script.



For every file we define 3 sets of people for whom we may specify permissions.



#### Owner



The user who owns the file. Typically the person who created the file but ownership can be changed.



#### Group



Every file belongs to a single group. Groups can have many users in it so you can give access to multiple people.



#### Others



Everyone else who is not in the group or the owner.




Three persmissions and three groups of people. That's about all there is to permissions really. Now let's see how we can view and change them.



### View Permissions



To view permissions for a file we use the long listing option for the command ls.



ls -l [path]



### Change Permissions



To change permissions on a file or directory we use a command called "chmod" It stands for change file mode bits which is a bit of a mouthfull but think of the mode bits as the permission indicators.



```
chmod [permissions] [path]
```



chmod has permission arguments that are made up of 3 components



There are two ways you can use chmod and you will see both used. One is shorter and one is more descriptive.




## Environment Variables
- How can we check the existing env var in our system 'printenv var'
- How can we create an Env variable 'export name_of_the_var=value'
- ~/.bashrc, ~/.profile, ~/.bash_profile


## How to setup persistent environment variables

- 1st step - do echo $SHELL to see what kind of shell you are using
- 2nd step - set variables in /home/.bashrc ( nano /home/.bashrc or nano .bashrc )
- 3rd step - At the end of the file append the following line: export FIRST_NAME="yourName" and save
- 4th step - do source /home/.bashrc or source .bashrc
- 5th step - in the terminal do the following: sudo nano /etc/profile
- 6th step - Append the variable at the end of the file
- 7th step - Save and exit
- 8th step - Verify if it is working: printenv VARIABLE_NAME
- 9th step - exit from your VM
- 10th step - ssh back into your VM and do again printenv VARIABLE_NAME
