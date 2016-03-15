# commandline2Repo
## Version Control System
###Question
###1. Compare distributed and centralized version control systems. What advantages does a distributed version control system have over a centralized versioncontrol system.

##### Distributed Version Control System
In a DVCS (such as Git, Mercurial, Bazaar or Darcs), clients don’t just check out the latest snapshot of the files: they fully mirror the repository. Thus if any server dies, and these systems were collaborating via it, any of the client repositories can be copied back up to the server to restore it. Every clone is really a full backup of all the data.
<br>
<br>
Furthermore, many of these systems deal pretty well with having several remote repositories they can work with, so you can collaborate with different groups of people in different ways simultaneously within the same project. This allows you to set up several types of workflows that aren’t possible in centralized systems, such as hierarchical models.
<br>
<br>
In a distributed VCS, when a developer makes changes on a local machine to a copy of a repository, the developer can then optionallypush these changes back into the other copies. This can prove challenging if there are many developers working on a project, as it would entail pushing code to every developer’s copy of the repository each time.
<br>
<br>
As a result, though a distributed VCS does not prescribe a centralized repository, in practice, most development teams “bless” a single copy of the repository as the primary, or central, copy. They then push changes to this central copy, and other developers later pull these changes down to their own copies.

##### Centralized Version Control System
The major issue that people encounter is that they need to collaborate with developers on other systems. To deal with this problem, Centralized Version Control Systems (CVCSs) were developed. These systems, such as CVS, Subversion, and Perforce, have a single server that contains all the versioned files, and a number of clients that check out files from that central place. For many years, this has been the standard for version control.
<br>
<br>
This setup offers many advantages, especially over local VCSs. For example, everyone knows to a certain degree what everyone else on the project is doing. Administrators have fine-grained control over who can do what; and it’s far easier to administer a CVCS than it is to deal with local databases on every client.
<br>
<br>
However, this setup also has some serious downsides. The most obvious is the single point of failure that the centralized server represents. If that server goes down for an hour, then during that hour nobody can collaborate at all or save versioned changes to anything they’re working on.
<br>
<br>
If the hard disk the central database is on becomes corrupted, and proper backups haven’t been kept, you lose absolutely everything – the entire history of the project except whatever single snapshots people happen to have on their local machines. Local VCS systems suffer from this same problem – whenever you have the entire history of the project in a single place, you risk losing everything.
##### Advantages Over Centralized Version Control
The act of cloning an entire repository gives distributed version control tools several advantages over centralized systems:
<br>
<br>
1.Performing actions other than pushing and pulling changesets is extremely fast because the tool only needs to access the hard drive, not a remote server.
<br>
2.Committing new changesets can be done locally without anyone else seeing them. Once you have a group of changesets ready, you can push all of them at once.
<br>
3. Everything but pushing and pulling can be done without an internet connection. So you can work on a plane, and you won’t be forced to commit several bugfixes as one big changeset.
<br>
4. Since each programmer has a full copy of the project repository, they can share changes with one or two other people at a time if they want to get some feedback before showing the changes to everyone.



###Question
###2. Explain what a GitHub repository fork is and its purpose and use.

##### GitHub repository fork

A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project.
<br>
Most commonly, forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for your own idea.
<br>
Propose changes to someone else's project
<br>
A great example of using forks to propose changes is for bug fixes. Rather than logging an issue for a bug you've found, you can:
<br>
Fork the repository.
Make the fix.
Submit a pull request to the project owner.
If the project owner likes your work, they might pull your fix into the original repository!
<br>
##### Use someone else's project as a starting point for your own idea.
At the heart of open source is the idea that by sharing code, we can make better, more reliable software.
In fact, when you create a repository on GitHub, you have a choice of automatically including a license file, which determines how you want your project to be shared with others.

###Question
###3.Files in UNIX systems have 'owners', and there are 'groups' that can have access to a file. In addition a 'user' can belong to a group. Explain what all these terms mean and the relationship between them.
#####Title: File Users, Owners, and Groups
#####Category: Working with Files and Directories through The Command Line
#####Users and Groups
Although every UNIX user has a username of up to eight characters long, inside the computer UNIX represents each user by a single number: the user identifier ( UID ). Usually, the UNIX system administrator gives every user on the computer a different UID .
<br>
UNIX also uses special usernames for a variety of system functions. As with usernames associated with human users, system usernames usually have their own UIDS as well. Here are some common "users" on various versions of UNIX : 
<br>
<br>
root , the superuser, which performs accounting and low-level system functions.
<br>
<br>
daemon or sys , which handles some aspects of the network. This username is also associated with other utility systems, such as the print spoolers, on some versions of UNIX .
<br>
<br>
agent , which handles aspects of electronic mail. On many systems, agent has the same UID as daemon .
<br>
<br>
guest , which is used for site visitors to access the system.
<br>
<br>
ftp , which is used for anonymous FTP access.
<br>
<br>
uucp , which manages the UUCP system.
<br>
<br>
news , which is used for Usenet news.
<br>
<br>
lp , which is used for the printer system.
<br>
<br>
nobody , which is a user that owns no files and is sometimes used as a default user for unprivileged operations.

###Question
###4. There are operators that can be used to test files, strings, and integers. List at least four operators that can be used to test files, four that can be used to test strings, and four that can be used to test integers and describe how these operators work with at least one example usage of each.
#####Title: Test Operators
#####Category: Conditionals on The Command Line

#####File Test Operators
-e : Returns true if a file exists
<br>
-f : Returns true if a file is a regular file, not a directory
<br>
-d : Returns true if a file is a directory
<br>
-w : Returns true if you can write to a given file
<br>
-r : Returns true if you can read a given file

##### example of file test operator
"#"!/bin/sh
<br>
file="/var/www/cmd/unix/test.sh"
<br>
if [ -r $file ]
<br>
then
<br>
echo "File has read access"
<br>
else
<br>
echo "File does not have read access"
<br>
fi
<br>
This would produce following result −
<br>
File has read access

##### String Test Operators
= : Returns true if two strings are identical
<br>
!= : Returns true if two strings are not identical
<br>
< : Returns true if the first string is alphabetically less than the second string (in sorting order)
<br>
">" : Returns true if the first string is alphabetically greater than the second string

##### example of string test operator
'#'!/bin/sh
<br>
a="abc"
<br>
b="efg"
<br>
if [ $a = $b ]
<br>
if [ $a != $b ]
<br>
then
<br>
   echo "$a != $b : a is not equal to b"
  <br> 
else
<br>
   echo "$a != $b: a is equal to b"
   <br>
fi
<br>
This would produce following result −
<br>
abc = efg: a is not equal to b
<br>
abc != efg : a is not equal to b

#####Integer Test Operators
-eq : Returns true if two integers are equal
<br>
-ne : Returns true if two integers are not equal
<br>
-gt : Returns true if the number on the left is greater than the number on the right
<br>
-ge : Returns true if the number on the left is greater than or equal to the number on the right
<br>
-lt : Returns true if the number on the left is less than the number on the right
<br>
-le : Returns true if the number on the left is less than or equal to the number on the right

##### example of integer test operator
'#'!/bin/sh
<br>
a=10
<br>
b=20
<br>
if [ $a -eq $b ]
<br>
then
<br>
   echo "$a -eq $b : a is equal to b"
   <br>
else
<br>
   echo "$a -eq $b: a is not equal to b"
   <br>
fi
<br>
if [ $a -ne $b ]
<br>
then
<br>
   echo "$a -ne $b: a is not equal to b"
   <br>
else
<br>
   echo "$a -ne $b : a is equal to b"
   <br>
fi
<br>
if [ $a -gt $b ]
<br>
then
<br>
   echo "$a -gt $b: a is greater than b"
   <br>
else
<br>
   echo "$a -gt $b: a is not greater than b"
   <br>
fi
<br>
This would produce following result −
<br>
10 -eq 20: a is not equal to b
<br>
10 -ne 20: a is not equal to b
<br>
10 -gt 20: a is not greater than b

###Question
###5. Describe UNIX processes for a beginner. Then, discuss function of the ps command, and include an example of the syntax an usage of the ps command.
#####Title: Introduction to UNIX Processes
#####Category: UNIX Processes on the Command Line


