# commandline2Repo
## Version Control System
###Question
###1. Compare distributed and centralized version control systems. What advantages does a distributed version control system have over a centralized versioncontrol system.

##### Distributed Version Control System
In the past few years, distributed VCSs have slowly started to supplant centralized VCSs in many software
development organizations as well as in the world of opensource software development. The model for distributed VCS is peertopeer;there is no central server. Instead, developers copy, or clone, the entire source code repository from one another, placing the entire history of a project on their local hard drives. 
<br>
<br>
In doing so, distributed VCS avoids the primary pitfall of centralized systems, allowing developers to work freely, anywhere, any time, with the confidence that they have everything they need to get their jobs done right.
<br>
<br>
In a distributed VCS, when a developer makes changes on a local machine to a copy of a repository, the developer can then optionallypush these changes back into the other copies. This can prove challenging if there are many developers working on a project, as it would entail pushing code to every developer’s copy of the repository each time.
<br>
<br>
As a result, though a distributed VCS does not prescribe a centralized repository, in practice, most development teams “bless” a single copy of the repository as the primary, or central, copy. They then push changes to this central copy, and other developers later pull these changes down to their own copies.

##### Centralized Version Control System
Most versioncontrol systems, such as Subversion, CVS, Perforce, and Microsoft’s Visual Source Safe, have historically employed a centralized architecture. In a centralized VCS, a single server acts as the primaryrepository for all of the code, images, and other assets in a project. Developers working on the project “check out” the files they need from the server, similar to checking out books from a library. Upon checkout, the system copies the latest version of the requested files to the developer’s computer, also known as
the client, and he or she begins working.
<br>
<br>
Depending on the system, other developers may or may not be able to check out the same files. Centralized VCSs that employ “file locking” prevent concurrent access to files, allowing only one copy of any file in the repository to be checked out at any given time. Such locking mechanisms prevent the types of conflict Becky and Greg faced, blocking both developers from attempting to make changes to the same file at the same time.
<br>
<br>
Unfortunately, while it seems to be a simple and effective solution, file locking turns out to be a nuisance and
hinderance to team productivity. If any given file can only be edited by a single developer at any given time,
other developers may find themselves waiting for hours or even days before they are able to work. For instance,
if Becky has the file checked out, Greg would not be able to do the work he needs to do to it.
<br>
<br>
As a result, most modern centralized VCSs do not lock files on checkout, but instead ask developers to resolve
conflicts when a file is checked back in to the repository. If no one else has changed the file in question, then
checkin is rather straightforward. However, if someone has changed the file, the developer must complete a file
merge, reconciling the differences between the two copies before checking in the newly merged copy.

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
#####a 'user' can belong to a group
