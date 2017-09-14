# git
测试git的相关操作

  之前出现的本地master无法提交到远程master，并提示本地master和远程master版本不一致问题，是因为在创建远程master时添加了一个README.md文件，而这是本地master所没有的，也就造成了push失败的现象。 
  
  解决方法：1、远程master不创建这个文件 2、远程master继续创建这个文件，本地master在push之前先执行git pull --rebase origin master（注：pull=fetch+merge）操作，将远程的README.md文件合并到本地master中，确保本地、远程master版本一致，然后再将本地master PUSH到远程master中。
