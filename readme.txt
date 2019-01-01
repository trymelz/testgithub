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

	linfa@ThinkCenter1:~/LinfaWork/Python/DataScrapy/you-get/testgithub$ git checkout first_release
	Switched to branch 'first_release'

	note: after you switch to first_release, the file in the workspace will replaced by those in the first_release

	

