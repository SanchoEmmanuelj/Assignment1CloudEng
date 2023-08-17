#ASSIGNMENT 1

...
Student Name | EMMANUEL JONGWO SANCHO
...

###Task 1 - Create A User.

To create a user on a Linux system, you can use the useradd command. Here's how you can do it:

Open a terminal on your Linux system.
Use the useradd command to create a new user. 
![user was created](<Screenshot 2023-08-17 at 08.59.26.png>)

###Task 2 - Set an expiry date of 2 weeks on the new userm.

To set an expiration date for a user account on Linux, we can use the usermod command along with the -e option. The -e option allows you to specify the account's expiration date. The date format is YYYY-MM-DD format.

Here's how you can set an expiration date of 2 weeks from the current date for a user:
![expiration date was set](<Screenshot 2023-08-17 at 09.13.38.png>)

To verify that the expiration date has been set, you can use the chage command with the -l option:
![verify that expiration was set](<Screenshot 2023-08-17 at 09.21.42.png>)

###Task 3 - Prompt the user to change there password on login.

To do this we Use the -chage command to set an expiration date for the user's password. This will force the user to change their password upon their first login. also the (-d 0) option sets the password's expiration date to the current day, forcing the user to change their password immediately upon login.
![PassWord Change Is Required](<Screenshot 2023-08-17 at 09.32.55.png>)

###Task 4 - attach or append the user to a group called altschool.

To add or append an existing user to an existing group on Linux, we can use the (-usermod) command.we also put -aG options then the <groupname> followed by <username>

-a: Append the user to the group's list of supplementary groups. Without this option, the user will be removed from all other groups and added only to the specified group.
-G: Specify the supplementary groups to which the user should belongs
![User has been addded to the altschool group](<Screenshot 2023-08-17 at 09.53.53.png>)

we added the user sanchoemmanuel to the existing group altschool. The -aG options append (-a) the user to the specified group(s), and -G specifies the group(s) to which the user should belong.

After running this command, the user sanchoemmanuel became a member of the altschool group as seen on screenshot.


###Task 5 - Allow altschool group to be able to run only cat command on /etc/.

To allow a specific group to run only the cat command on files within the /etc/ directory in Linux

First we Create a New Command Alias in sudoers Configuration:
Open the sudoers configuration file using the (visudo) command

Then we Add the line to allow members of the altschool group to run the cat command.
![command line to allow altschool group to perform cat on /etc/ file](<Screenshot 2023-08-17 at 10.50.34.png>)

###Task 6 - Create another user. make sure that this user doesn't have a home directory.

To create a user without a home directory, we can use the (useradd) command with the (--no-create-home) option. This option prevents the creation of a home directory for the user.
![created the user Mary without a home directory](<Screenshot 2023-08-17 at 11.21.21.png>)


#THE END