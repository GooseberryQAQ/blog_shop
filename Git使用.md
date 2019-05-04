# Git主要使用操作（个人总结，仅供参考）
## 提交项目至远程仓库
### 一、设置用户名和邮箱
* 用户名：`$ git config --global user.name "..."`
* 密码：`$ git config --global user.email "email@example.com"`

### 二、将文件夹初始化成git仓库
* `$git init`

### 三、生成ssh密钥以及后续过程
* 省略

### 四、在本地仓库提交文件
* 添加文件(*不用加方括号*)：`$ git add <filename>`
* 添加说明：`$ git commit -m "message"`

### 五、提交到Github
* 1、远程仓库关联本地：`$ git remote add origin git@github.com:username/reponame.git`</br>
其中 **`username`** 是github的用户名<font color=#00ffff size=3>reponame</font>是仓库名
* 2、提交：`$ git push -u origin master`(远程仓库中项目为空，且为第一次提交);</br>
若项目不为空(**如添加了README文件**)则先用，`$ git pull --rebase origin master`,然后再使用上面的命令提交。
* 3、后续使用：</br>
推送本地的更新到远程库 `$git push origin master`（与`git push`有区别）</br>
将远程更新到本地 `$git pull origin master`

## 将远程仓库克隆到本地
### 从Github拉取项目
* `$ git clone url`(填入具体的url，会覆盖本地内容)
* `$ git pull git@github.com:username/reponame.git master`(把当前分支内容上传到远程master分支上)