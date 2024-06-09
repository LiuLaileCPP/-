# GitHub
## GitHub三要素:
**Repository仓库**<br>
项目管理存储基本单位
一个仓库中存储一个项目，一个用户可以拥有多个仓
库，仓库属性分为public 和 private<br>
**commit提交：**<br>
git commit -m "提交说明" #提交到本地仓库<br>
**Branch分支**<br>
在仓库中可以包含多个分支，分支才是代码文件的第
一存储单位，默认的仓库主分支为master/main<br>
## 仓库内容
* Code，资源存储，
代码资源，
二进制，项目管理脚
本，许可证<br>
* issues，使用时遇到的bug 或 进行提交，等待反馈
* README，使用markdown语言编写，工程自述说明<br>
* LICENSE 许可证:GPL2.0,3.0.Apahce 2.0，Mit，这
些许可证，给使用者最大使用权限以及最少的限制<br>
## 设备认证
进入到仓库文件夹下执行<br>
git init // 创建本地仓库
*后续对仓库的操
作，都要在仓库位置(master)*<br>
git config -list //查看git的配置文件<br>
**账号验证：**git config --global "注册的用户名" git config --global "注册的email"<br>
**生成本机设备密文**
ssh-keygen -t rsa -c“注册邮箱’
创建本地密文 *去对应的目录下查找密文文件*<br>
rsa.pub 复制密文，粘贴到 settings -> ssH key and
GPG -> new ssh key ->粘贴<br>
**测试是否关联**ssh -T git@github.com #SSH远程登入<br>
## 为云端仓库起别名 方便上传
git remote add 别名 SSH地址(云端仓库地址)
<br>git remote remove 别名 #删除起的别名
## 代码上传步骤
1. git add code.c #代码写入git缓冲区
2. git commit -m "提交说明" #代码提交到本地仓库文件夹
3. git push 仓库别名 master #代码上传到云端仓库的master分支
git rm #删除本地文件及仓库数据<br>
git restore #本地仓库中存在时恢复被删除的文件<br>
git status #查看状态<br>
## 代码更新的依赖关系被破坏
*本地内容要比云端新,完成更新替换， 但是如果直接
修改云端内容,导致,本地内容无法再次提交*
**解决办法：**先拉取 git pul 云端内容 与本地内容合井或操作,
而后再次推即可
<br>**拉取**git pull --release 别名 master<br>
**更新**
* git rebase --abort #忽略新版，此时还不能上传
* git rebase --skip #忽略旧版本，更新本地代码后可上传
* git rebase --continue #版本合并，解决冲突后直接上传
## 下载代码
git clone "https仓库地址" 
## MarkDown语法
\*斜体\* *斜体* \*\*粗体\*\* **粗体**  \*\*\*粗斜体\*\*\* ***斜粗体***
\~\~删除线\~\~ ~~删除线~~
<br>分割线：---
---
<br>引用：<br>
^一级引用
^^二级引用
**表格语法：**<br>居左 局右 居中：\-\-|:\-\-|:\-\-:<br>
名称|技能|排行
--|:--|:--:|
篮球|唱跳rap|1
**代码段**<br>
三个\`代码语言<br>
 	代码正文<br>
三个\`<br>
```c
	#include<stdio.h>
	int main()
	{
		printf("姬霓太美！)";
		return 0;
	}
```
**超链接**<br>
\[GitHub](https://www.github.com "点击跳转")
<br>**插入图片**
\!\[别名](c:/users//Desktop//蔡徐坤.jpg)





















































