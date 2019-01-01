Step 1: setup git account
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get/testgithub$ git config --global user.email "linfa.zhu@gmail.com"
	linfa@ThinkCenter1:~/Python/DataScrapy/you-get/testgithub$ git config --global user.name "Linfa Zhu"

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
