## COMMANDS

### ADD TAG
	git tag -a <tag> -m 'Initial release'
	git push --tag

### DELETE TAG
	git tag -d <tag>
	git push origin :refs/tags/<tag>

### MOVE A TAG
	git tag -a <tag> <commit> -f
	git push -f origin <tag>
	
### SHOW DIFFERENCES WITH STAGE
	git diff --staged

### SHOW FILES MODIFIED IN PREVIOUS COMMIT
	git show <commit> --name-only

### UNCOMMIT AN UNPUSHED FILE PRESERVING CHANGES
        git reset <commit> --soft
        git reset HEAD~1 --soft #last commit

### REVERT A COMMITED FILE PRESERVING CHANGES AS UNESTAGED
	git reset <commit>

### CHANGE REMOTE ORIGIN
	git remote -v
	git remote set-url origin <origin_url>

## CONFIGURATION

### DISABLE SSL CERTIFICATE
	git config http.sslVerify "false"

### ALIASES
	git config --global user.name "Manel Pérez"
	git config --global user.email dummy@test.com
	git config --global alias.co checkout
	git config --global alias.ci commit
	git config --global alias.st status
	git config --global alias.br branch
	git config --global alias.hist 'log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short'
	
### SET GLOBAL CONFIG
	git config --global core.excludesfile '~/.gitignore'
