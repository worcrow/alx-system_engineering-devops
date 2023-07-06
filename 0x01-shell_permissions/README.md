This dir containing the correction of project 0x01. Shell, permissions

/****
switch from the current user to another user named another_user:
su another_user
****/

/****
print the username of the current user : whoami
****/

/**** 
print the groups of the current user : groups
****/

/**** 
change the owner of a file named fl to the other owner named oth_owner: chown oth_owner fl
****/

/****
to create an empty file you can use touch followed by the name of the file ex: touch my_file
****/

/****
chmod used to change the permission of a file or directory followed by mode/octal_mode and file name or dir
there are 3 mode user->u ,group->g , and other->o
you can give permession read-> r , write-> w , execute->x, and no_permission->-
exapmle: -add execute permission to the owner of a file fl -----> chmod u+x fl
	 -adds execute permission to the owner and the group owner, and read permission to other users, to the file ------> chmod ug+x, o+r fl
	 -add execution permission to the owner, the group owner and the other users, to the file --------> chmod a+x fl or chmod +x fl
													          a mean all mode	
or you can give permission by octal_mode, each mode represented by a number r->4 , w->2, x->1a , and no_permission->0
example :-Write a script that sets the permission to the file as follows: Owner: no permission at all,Group: no permission at all,Other users: all the permissions --------> chmod 007 fl 7 stand for :rwx {make sum the the number that represent the mode 4+2+1=7}
or you can give permession with reference , example: Write a script that sets the mode of the file hello the same as olleh’s mode -------> chmod --reference=olleh hello (use man chmod to learn more about chmod)  						
****/

/****
adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users: chmod -R a+x */
let break it down: chmod -R --> change files and directories recursively 
		   a+x ---> give all mode execution right
		   */ ---> mean all directory in the current directory 
****/

/****
to create a dir and change it permission: mkdir -m {mode right} file , m --> stand for change mode when you use as option with mkdir (chmod mkdir to learn more) example: Create a script that creates a directory called my_dir with permissions 751 in the working directory -----> mkdir -m 751 my_dir 
****/

/****
chgrp : change the group of a file or directory , example : Write a script that changes the group owner to school for the file hello ---> chgrp school hello 
****/

/****
chown : change the ownership/group of a file or directory , if only the owner is given it change only the owner , if the owner followed by colon and group it change the the owner and the group of a file/dir , if the colon and group name are given it work as chgrp.
example : Write a script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory ------> chown -R vincent:staff * (man chown to learn more about chown) let break it down : 
	     chown -R vinvent:staff ----> change the owner and group files and directories recursively to vinvent(owner):staff(group)
	     *: stand for all the file and directory in the current folder
	-Write a script that changes the owner and the group owner of _hello to vincent and staff respectively : The file _hello is a symbolic link -----> chown -h vincent:staff _hello {-h -> affect symbolic links instead of any referenced file (useful only on systems that can change the ownership of a symlink)} 
	-Write a script that changes the owner of the file hello to betty only if it is owned by the user guillaume ----> chown --from=guillaume betty hello {  --from=CURRENT_OWNER:CURRENT_GROUP
              change the owner and/or group of each file only if its current owner and/or group match those specified here.  Either may be
              omitted, in which case a match is not required for the omitted attribute }    
****/

/****
Write a script that will play the StarWars IV episode in the terminal: telnet towel.blinkenlights.nl
let break it down : telnet: This is the command that starts the telnet client
		    towel.blinkenlights.nl: This is the hostname of the remote server that streams the movie in ASCII art. When you run the telnet command with this hostname, your computer connects to the remote server over the internet.
****/
