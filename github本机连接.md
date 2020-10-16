# github本机连接 

1. ## 在github上新建一个ssh

2. ## 在本机上生成一个ssh

3. [github 生成配置ssh 秘钥方法详解](https://www.cnblogs.com/sharfir/p/8342298.html)

   如果安装github成功后，当从本地提交文件到github的时候，提交不成功，报错，可能问题就是你还没有生成ssh秘钥

   1.当你提交文件到github，不成功，出现如下的情况，就代表着github上面没有设置秘钥

   ![img](https://images2017.cnblogs.com/blog/1119637/201801/1119637-20180124155652100-1326537884.png)

    

    

   设置秘钥的步骤：

   1.找到本地环境：C:\Users\admin\.ssh  这个路径下的用户/名称/.ssh

   2.在这路径下，打开gitbub的命令控制台

   （1） git init //初始化一下，看看路径对不对

   （2） ssh-keygen -t rsa -C "邮箱"

   　　![img](https://images2017.cnblogs.com/blog/1119637/201801/1119637-20180124160514365-1357055717.png)

    （3）到本地环境.ssh路径下查看，是否生成id_rsa,id_rsa.pub这个两个文件

   　　![img](https://images2017.cnblogs.com/blog/1119637/201801/1119637-20180124160651928-1477527912.png)

    （4）生成后，现在把id_rsa.pub里面的内容复制到githubd 的add github key 的key里面

   　　![img](https://images2017.cnblogs.com/blog/1119637/201801/1119637-20180124161029506-1888974039.png)

   　　![img](https://images2017.cnblogs.com/blog/1119637/201801/1119637-20180124161153740-37132601.png)

    

   　　（5）第一次提交，配置密钥，需要输入github的密码，如下就是添加秘钥成功

   　　![img](https://images2017.cnblogs.com/blog/1119637/201801/1119637-20180124161353256-1539950160.png)

   　　　　

   　　（6）密钥配置成功后，要验证一下是否配置成功

   　　ssh -T git@github.com  

   　　出现： You've successfully authenticated, but GitHub does not provide shell access.就是说明配置成功
   　　

   　　![img](https://images2017.cnblogs.com/blog/1119637/201801/1119637-20180124162658475-1715282616.png)

    

    

    