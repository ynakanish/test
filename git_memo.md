# git: how to use
## normal git
### edit on LOCAL
- git clone https://github.com/ynakanish/test.git

	copy from remote 

- git log

	view commit log

- <edit your file>

	** edit your files **

- git add <file>

	add to commit list

- git commit -m[a] "first commit"

	commit for LOCAL repository
	-a option is useful. all edited file is add to commit list.


### relation with REMOTE
- git push

	commit for REMOTE repository

- git pull

	apply from REMOTE repository

## git flow
- git flow init

	initialize for git-flow

- git branch

	view branch list

- git push origin develop

	push to REMOTE for develop branch

- git flow feature start <feature name>
- git flow <branch name> start <branch version>

	create new feature on LOCAL repository
		-> please check by "git branch" command

- git flow feature publish <feature name>

	push to REMOTE for feature branch

- git flow feature pull origin <feature name>

	pull from REMOTE repository

- git flow <branch type(develop|feature)> track <branch name>

	* other worker *

	get published feature.  
	ex) git flow feature track <feature name>

-- git flow feature pull

	update got published feature.
	and please use "git lofw featrue rebase"

-- git flow feature rebase

	clean got published feature

-- git push

	push to REMOTE repository

- git flow <merge target branch> pull origin
- git flow <merge target branch> rebase

	pull from REMOTE repository for merge target repository.
	this is important prepare for next 'finish feature'

- git flow <feature name> finish <feature name>

	finish the feature.
	and merge to origin 

	this command can use other branch.
	ex) git flow release finish v1.0
		release branch is merge to master branch by v1.0 tag.
	ex) git flow hotfix finish v1.0.1
		hotfix branch is merge to master branch by v1.0.1 tag.
		and merge to develop branch too.

# keywords

- origin

	original git repository

	ref: http://qiita.com/hshimo/items/99811144bf4a081319e5

# references

いまさら聞けない、成功するブランチモデルとgit-flowの基礎知識
http://www.atmarkit.co.jp/ait/articles/1311/18/news017.html

git-flowのインストールとブランチ運用前のリポジトリ準備
http://www.atmarkit.co.jp/ait/articles/1311/28/news042.html

図とコマンドで分かる！ git-flowによる開発の流れと使い方
http://www.atmarkit.co.jp/ait/articles/1401/06/news013.html

EOF
