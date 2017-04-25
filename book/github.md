# github配置

#### 检查本机的ssh密钥
* $ cd ~/. ssh

#### 清理本机密匙
* $ mkdir key_backup
* $ cp id_rsa* key_backup
* $ rm id_rsa*

#### 生成新的密匙
* $ Ssh-keygen –t rsa –C "你的邮件地址"

#### 认证连接
* $ ssh -T git@github.com

#### 配置用户
 * $ git config --global user.name "John Doe"
 * $ git config --global user.email "johndoe@example.com"

# 错误
#### 1. On branch master nothing to commit, working directory clean

* 1）rm -rf .git/
* 2）git init
* 3）git remote add &lt;namn&gt;&nbsp;&lt;url&gt;
* 4）git add .
* 5）git commit -m"提交描述"
* 6）git push -f &lt;name&gt; master
