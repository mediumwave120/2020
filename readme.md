### github 使用
#### 1.第一步：创建SSH Key。把邮件地址换成你自己的邮件地址，然后一路回车，使用默认值即可
`$ ssh-keygen -t rsa -C "youremail@xxx.com"`
#### 2.这个文件在当前系统用户下面
#### 3.直接赋值粘贴 .ssh的文件会破坏格式 输入命令
`clip < ~/.ssh/id_rsa.pub`
#### 4.配置用户和邮箱
`$ git config --global user.name "your name"`
`$ git config --global user.email "your_email@youremail.com"`