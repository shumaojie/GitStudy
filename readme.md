#git 学习心得#

##使用git bash设置ssh登录##
###步骤###
1. 设置用户名:git config --global user.name "shumaojie"
2. 设置用户邮箱:git config --global user.email "yanjie.jw@163.com"
3. Staubli电脑设置代理: git config --global http.proxy http://gateway.zscaler.net:80
4. 使用ssh登录:git config --global http.sslVerify false

5. 启动ssh服务器:ssh-agent  bash
6. 生产私钥和公钥:$ ssh-keygen -t rsa -C "yanjie.jw@163.com"
7. 添加私钥到本地:ssh-add ～/.ssh/id_rsa
8. 添加私钥是否已经添加:ssh-add -l
9. 把公钥和私钥复制出来到当前目录下: cp -R ~/.ssh/*  .
10. 打开公钥id_rsa.pub,登录到对应的网站,输入公钥


11. 进入相应的本地仓库
12. git init
13. git add .
14. git commit -m "remark"
15. git remote add origin https://bitbucket.org/shumaojie/IssueSummary.git


###重点说明###
1. 每个仓库的local配置都保存在.git/config文件
2. 没有本地local没有配置,就找全局global，没有全局global没有配置就找系统system


##安装github for windows##
1. 国内请安装免费翻墙软件：PsiPon3, 下载安装并运行
2. 打开chrome浏览器 [github for windows](https://desktop.github.com/)
3. 下载github for windows安装包（670K左右）
4. 运行安装包，在线安装**必须翻墙,因为程序是托管在亚马逊云上**
5. 进行用github用户名和密码登录配置


##利用github git shell登录github##
###提示####
1. 如果仓库在github上，优先选择git shell 
2. 利用github UI登录后，可直接使用git shell来登录
3. 直接利用git add.   git commit -m "update" git push
4. 推荐先在github上建立仓库，然后利用git clone来实现



##利用git 返回到某个版本##
***可以根据日期来返回到某个版本***  
1. git log 获取所有commit版本
2. git reset --hard  commitno (获取前面6位)


##FAQ##
1. 配置密钥后,还是需要输入用户名问题
2. 网站上一个公钥，是否所有电脑还共用一个私钥
3. git和http的网址是否相同
4. http.sslverify配置具体含义  

5. fatal:The remote end  hung up unexpectedly
6. error: fatal: WRPC failed: HTTP 400 curl 22 The requested URL returned error:400 Bad Request
7. error: RPC failed; curl 56 SSL read: err三种方式 or
8. ssh: connect to host bitbucket.org port 22: Connection timed out
9. fatal:Could not read from remote repository
10. bitbucket.org/coding.net  push不上去大的项目,但是github可以
11. fatal: unable to access '':the requested URL returned error:500  解决：生成密钥并部署密钥


11. 访问有三种方式1.ssh 2.https 3.http 
12. 在github shell中可以通过一个 ./ 来执行脚本
13. 在git log时可以通过q来退出这个命令行
14. 在修改后的文件中，只能执行下git add.;git  commit ,git push后通过git reset  --hard  commit号来执行返回
15. 当说两个文件冲突时，可以先开一个branch 
16. git config --global  --list 里面global的设置都保存在C:\Documents and settings\用户名\.gitconfig文件夹下（windows）
17. git remote show  origin  查看远程origin
18. 修改远程目录名称  git  remote  rename  origin   oldname  newname
19. Recv failture: Connnection was reset  （原因：没有连上网络）
20. rsa routines:RSA_padding_check_PKCS1_type_1:block type is not 01  进行配置git config --global http.sslVerify false
21. fatal: The remote end hung up unexpectedly
22. coding.net不允许上传超过20M的单个文件




