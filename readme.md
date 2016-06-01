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
9. 把公钥和私钥复制出来到D: cp -R ~/.ssh/*  /d
10. 打开公钥id_rsa.pub,登录到对应的网站,输入密钥


11. 进入相应的本地仓库
12. git init
13. git add .
14. git commit -m "remark"
15. git remote add origin https://shumaojie@bitbucket.org/shumaojie/IssueSummary.git


###重点说明###
1. 每个仓库的local配置都保存在.git/config文件
2. 没有本地local没有配置,就找全局global，没有全局global没有配置就找系统system


##利用github git shell登录github##
###提示####
1. 如果仓库在github上，优先选择git shell 
2. 利用github UI登录后，可直接使用git shell来登录
3. 直接利用git add.   git commit -m "update" git push
4. 推荐先在github上建立仓库，然后利用git clone来实现


