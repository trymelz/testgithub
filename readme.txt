Step 1: setup git account
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get/testgithub$ git config --global user.email "trymelz@yahoo.com"
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get/testgithub$ git config --global user.name "trymelz"

Step 2: create git workspace
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get$ mkdir testgithub
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get$ cd testgithub/
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get/testgithub$ git init
	Initialized empty Git repository in /mnt/c/Users/LinfaWork/Python/DataScrapy/you-get/testgithub/.git/

Step 3: change and commit
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get/testgithub$ git add readme.txt
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get/testgithub$ git commit -m '1st and second steps'
	[master (root-commit) a6d953d] 1st and second steps
 	 1 file changed, 10 insertions(+)
 	 create mode 100644 readme.txt

Step 4: creating new branch
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get/testgithub$ git checkout -b first_release
	Switched to a new branch 'first_release'
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get/testgithub$ git branch
	* first_release
	  master
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get/testgithub$ git checkout master
	Switched to branch 'master'

Step 5: create a new repository in github
	login your github account and create a new repository, it shows the following
	Instructions from github

	…or create a new repository on the command line
	echo "# testgithub" >> README.md
	git init
	git add README.md
	git commit -m "first commit"
	git remote add origin git@github.com:trymelz/testgithub.git
	git push -u origin master

	…or push an existing repository from the command line
	git remote add origin git@github.com:trymelz/testgithub.git
	git push -u origin master

	…or import code from another repository
	You can initialize this repository with code from a Subversion, Mercurial, or TFS project.

Step 6: setup ssh key and add it in your github account
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ ssh-keygen -t rsa -b 4096 -C "trymelz@yahoo.com"
	Generating public/private rsa key pair.
	Enter file in which to save the key (/home/linfa/.ssh/id_rsa):
	Created directory '/home/linfa/.ssh'.
	Enter passphrase (empty for no passphrase):
	Enter same passphrase again:
	Your identification has been saved in /home/linfa/.ssh/id_rsa.
	Your public key has been saved in /home/linfa/.ssh/id_rsa.pub.
	The key fingerprint is:
	SHA256:XwfkuorSDmu6Ms3SJFPyZnfY5GzvdprD1OKz53orEz0 trymelz@yahoo.com
	The key's randomart image is:
	+---[RSA 4096]----+
	|            .    |
	|           o     |
	|            o    |
	|. .   .    . .   |
	| +   *  So. . .  |
	|o = o * +.Eo .   |
	| X ..+ = oo.     |
	|+ + oo..Xo+      |
	| +o+.oooB&o.     |
	+----[SHA256]-----+
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ eval $(ssh-agent -s)
	Agent pid 185
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ ssh-add ~/.ssh/id_rsa
	Identity added: /home/linfa/.ssh/id_rsa (/home/linfa/.ssh/id_rsa)
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ cat ~/.ssh/id_rsa.pub
	ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQC/mse1F7/JKymd4a7t77wVl0+sSqAgwj0aYALHoqd7f6Mb2xZGzfZH20vbJOC94EAQ2B5Cf1F5g2hnV7G8pmUsVXNDwXp2fBlz0hmkAQEw+vFM23T/NkSnyPAbtoDsvWjzf+LVUfHcPhR4OsG++3vrbMRjM4Vc4z9zCmmuPeoegJRG6z7A/CipLF82OVyQ5FzBBio5k5FfzIoTAtd8HgSkoHnFBVSsrnGK6XbvXFVhIC62vDJyjwAHlM7dO+8U3Pa34g2+tajtVoAsUIJxELf93vjwppxMv4u9XgdSJNQ91coWK9aCe7ik3+8HNUlEC/ujd8N/BAcVPc1HfR2jdrfBjQ1WrIZTzu9P2hsmzOAK5/L4tRQOEuMXRxnKzH+MSJnE7o9jFF8BOXejdzs2NUETfOImx4nEm/vuyTgltkF08mMGd+YolAi8DVUOVJeiMhwvRzxAlf+oqnmh6RyAGcXifrGYrAWB4n7LnIUJbUiQHYJgz1OhMO5FHRbkqsvA3GL2wuK0VY+2PMazbtwWLGZU/wmnDHelsfvTwNgGlCN17RhhniJNAqXz3NTItmVqm5oR8H1Yiq4eXTPmipFJ97pxgtaG6H9ysSYNVFwKiYwyu1vr21KfY4a3cTWWVOAQ0gpbjmslRIlDGwoiLPOfIo/4Ma01gxIoJ5WLGTwJO29GEQ== trymelz@yahoo.com

	login your github account->click your photo at top right corner->setting->SSH and CPG Keys
	add the above keys into SSH key

Step 7: push master branch to github repository
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git remote add origin git@github.com:trymelz/testgithub.git
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git push -u origin master
	The authenticity of host 'github.com (192.30.253.112)' can't be established.
	RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
	Are you sure you want to continue connecting (yes/no)? yes
	Warning: Permanently added 'github.com,192.30.253.112' (RSA) to the list of known hosts.
	Counting objects: 9, done.
	Delta compression using up to 4 threads.
	Compressing objects: 100% (6/6), done.
	Writing objects: 100% (9/9), 1.07 KiB | 122.00 KiB/s, done.
	Total 9 (delta 2), reused 0 (delta 0)
	remote: Resolving deltas: 100% (2/2), done.
	To github.com:trymelz/testgithub.git
	 * [new branch]      master -> master
	Branch 'master' set up to track remote branch 'master' from 'origin'.

Step 8: push other branch to github repository
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git branch
	  first_release
	* master
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git push origin first_release
	Total 0 (delta 0), reused 0 (delta 0)
	remote:
	remote: Create a pull request for 'first_release' on GitHub by visiting:
	remote:      https://github.com/trymelz/testgithub/pull/new/first_release
	remote:
	To github.com:trymelz/testgithub.git
	 * [new branch]      first_release -> first_release	
	

	You might be wondering what that "origin" word means in the command above. What happens is that when you clone a remote repository to your local machine, git creates an alias for you. In nearly all cases this alias is called "origin." It's essentially shorthand for the remote repository's URL.

Step 9: submit pull request
	now you default branch in github is master. When you click "2 branches", "new pull request" button showes on "first_release" branch
	when you click it, the errow message appear: "master is up to date with all commits from first_release. Try switching the base for your comparison."

	<note> when submit pull request, if base=master and compare=first_relase, it means try to merge commits from first_release to master
	

	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git checkout first_release
	Switched to branch 'first_release'

	note: after you switch to first_release, the file in the workspace will replaced by those in the first_release
	change readme.txt file and commit and push to github first_release branch

	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git add readme.txt
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git commit -m 'adding pull step in first_release branch'
	[first_release b3e067e] adding pull step in first_release branch
	 1 file changed, 107 insertions(+), 2 deletions(-)
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git push origin first_release
	Counting objects: 3, done.
	Delta compression using up to 4 threads.
	Compressing objects: 100% (2/2), done.
	Writing objects: 100% (3/3), 2.83 KiB | 580.00 KiB/s, done.
	Total 3 (delta 0), reused 0 (delta 0)
	To github.com:trymelz/testgithub.git
	   25c8f9f..b3e067e  first_release -> first_release

	note: now you can click "new pull request" button showes on "first_release" branch

	now click merge request, after solving conflict, we have the following message

	@trymelz adding pull step in first_release branch
 	@trymelz Merge branch 'master' into first_release


Step 10: resolving conflict (assume the github has new stuff from other peoples in first_release branch)
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git pull origin first_release
	remote: Enumerating objects: 7, done.
	remote: Counting objects: 100% (7/7), done.
	remote: Compressing objects: 100% (2/2), done.
	remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
	Unpacking objects: 100% (3/3), done.
	From github.com:trymelz/testgithub
	 * branch            first_release -> FETCH_HEAD
	   b3e067e..d46c5f1  first_release -> origin/first_release
	Auto-merging readme.txt
	CONFLICT (content): Merge conflict in readme.txt
	Automatic merge failed; fix conflicts and then commit the result.
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git status
	On branch first_release
	You have unmerged paths.
	  (fix conflicts and run "git commit")
	  (use "git merge --abort" to abort the merge)

	Unmerged paths:
	  (use "git add <file>..." to mark resolution)

	        both modified:   readme.txt

	no changes added to commit (use "git add" and/or "git commit -a")
	
	fix the conflict by editing readme.txt
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git add readme.txt
	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git commit -m 'fix confilict'
	[first_release dd5c951] fix confilict


Step 11: Contribute to someone else's repository
	Say you want to contribute changes to someone else’s repository (eg, this one).
	Say it’s by myfriend, and is called the_repo, then you’ll find it at https://github.com/myfriend/the_repo.
	Click the “Fork” button at the top right.You’ll now have your own copy of that repository in your github account.
	
	Open a terminal/shell on your local computer.Type
	$ git clone git@github.com:username/the_repo
	where username is your username.

	You’ll now have a local copy of your version of that repository.
	Change into that project directory (the_repo):
	$ cd the_repo

	Add a connection to the original owner’s repository.
	$ git remote add myfriend git://github.com/myfriend/the_repo

	note the first myfriend does not need to be the same as the username of myfriend. You could very well choose:
	$ git remote add repo_nickname git://github.com/myfriend/the_repo

	To check this remote add set up:
	$ git remote -v

	Make changes to files.
	git add and git commit those changes
	git push them back to github. These will go to your version of the repository.

	Go to your version of the repository on github.
	Click the “Pull Request” button at the top.

	Note that your friend’s repository will be on the left and your repository will be on the right.

	Click the green button “Create pull request”. Give a succinct and informative title, in the comment field give a short explanation of the changes and click the green button “Create pull request” again.

	Pulling others’ changes
	Before you make further changes to the repository, you should check that your version is up to date relative to your friend’s version.
	Go into the directory for the project and type:
	$ git pull myfriend master
	This will pull down and merge all of the changes that your friend has made.

	Now push them back to your github repository.
	$ git push

	Handling pull requests (at your friend's side)
	Say your friend has suggested some changes to your code.
	Ask them to get a github account and follow the instructions above: fork your repository, make the changes, and submit a pull request.
	Once they do that, you’ll get an email about it. How to handle it?

	Using the github website:
	Go to your version of the repository.
	Click on “Pull Requests” at the top.
	Click on the particular request.
	You’ll see their comments on the pull request, and can click to see the exact changes.
	If you want them to make further changes before you merge the changes into your repository, add a comment.
	If you hate the whole idea, just click the “Close” button.
	If you want to merge the changes into your repository, click the “Merge pull request” button.
	Your github repository will now be fixed, but you’ll want to get them into your local repository, too.
	Open a terminal/shell, and type
	$ git pull

	Using the command line
	You don’t have to use the github website for this.
	Open a terminal/shell.
	Go into the directory for your project.
	Add a connection to your friend’s version of the github repository, if you haven’t already.
	$ git remote add myfriend git://github.com/myfriend/the_repo
	Pull his/her changes.
	$ git pull myfriend master
	Push them back to your github repository.
	$ git push
	The pull request on github will be automatically closed.