# 免密码登录 #

1. 检查远程服务器`/ect/ssh/sshd.config`下`PasswordAuthentication`状态是否为yes，可以关闭，则禁用密码登录
2. 删除远程服务器中原有的`.ssh`目录及其子文件，然后分别执行`mkdir ~/.ssh` 和 `touch ~/.ssh/authorized_keys`命令
3. 删除本地的.ssh目录及其子文件，利用`ssh-keygen -t rsa`生成密钥
4. 在本地利用`scp ~/.ssh/id_rsa.pub xx@xxxx:` 记得末尾加上`":"`
5. 远程服务器上将上传的公钥复制在`authorized_keys`中，`cat ~/id_rsa.pub >> ~/.ssh/authorized_keys`
6. 更改服务器`.ssh`文件权限，`chmod 700 ~/.ssh` , `chmod 600 ~/.ssh/authorized_keys`