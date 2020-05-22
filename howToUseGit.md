### Gitの初期設定からadd, commit, pushする流れ

参考

<https://techacademy.jp/magazine/6235>

<https://prog-8.com/docs/git-env-win>

<https://blog.csdn.net/liuweixiao520/article/details/78971221>

1.GitHubでリポジトリを作成する
GitHubにログインした状態で、「New Repository」ボタンを押下します。

2.<https://gitforwindows.org/>からgitのインストーラをDL

3.インストーラを起動。gitのコマンドラインはvisual studio codeを選択する以外は、デフォルト設定でOK

4.以下はVSCodeかGit bushで操作。

5.はじめに、ローカルのPC上にローカルリポジトリを作成します。
mkdir file_folder_name
cd file_folder_name
「mkdir」は新しくディレクトリを作成するコマンドで、「cd」はディレクトリを移動するコマンドになります。
(pwd 当前路径)

6.`git init`

7.リモートリポジトリを登録する前にユーザー名とメールアドレスを設定しておく。以下のコマンドを実行して登録するか、設定ファイル(.git/config)を直接編集する。

 git config --global user.name "ユーザー名"`

 git config --global user.email "メールアドレス"`

8.`git remote add origin <リモートリポジトリのURL>`

9.テストファイルを作る。ここではtest.htmlとする

10.`git add *`

 (作業ディレクトリ上のすべてのものをインデックスにadd)

11.`git commit -m "コメント"`

 (コメントは必須)

12.`git push origin master`

13.githubのリモートリポジトリに反映されているか確認


(補足) .gitconfigのいじりかた

参考 

<https://qiita.com/KTakata/items/470da16b9e53799dcb65>

設定の確認

`git config --list`


設定をエディタで編集
`git config -e`

エディタの操作法はvimと同様

### ブランチの作成、マージ

总结：其实只需要进行下面几步就能把本地项目上传到Github

     1、在本地创建一个版本库（即文件夹），通过git init把它变成Git仓库；（只有第一次需要）

     2、把项目复制到这个文件夹里面，再通过git add .把项目添加到仓库；

     3、再通过git commit -m "注释内容"把项目提交到仓库；

     4、由于新建的远程仓库里面的README文件不在本地仓库目录中，通过以下命令先将内容合并以下：

$ git pull --rebase origin master 

     5、最后通过git push -u origin master把本地仓库的项目推送到远程仓库（也就是Github）上；
