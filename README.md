#Github
github网站：www.github.com
注册后可以new一个repository
![image.png](https://upload-images.jianshu.io/upload_images/14451551-751bf104022c9ec0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
create完后会有以下页面，页面会提供几种本地Git远程管理的方法，比如:
![image.png](https://upload-images.jianshu.io/upload_images/14451551-04baaf199dec9cd6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
先复制到txt记事本，下面会用到。


#Git
- Git的安装
Git官网下载地址;https://www.git-scm.com/download/win(建议迅雷下载)
- Git的初始化
在桌面右击，然后点击Git Bash here。
输入以下指令完成初始化
```
git config --global user.name '你的Github用户名'
git config --global user.email '你注册Github时用的邮箱'
```
至此Git完成初始化，可以输入```git config --list```查看初始化信息
![image.png](https://upload-images.jianshu.io/upload_images/14451551-80e7e49b20220cad.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
一般只需要第一次使用时初始化Git，后面的使用不需要；而每新建一个Git文件夹都需要初始化一次Git仓库。
- 初始化一个新的Git仓库
输入以下命令创建Git文件夹并且初始化Git仓库
```
mkdir Test01
cd Test01/
git init
```
- 在介绍Git基本操作之前先看一下结构图
![image.png](https://upload-images.jianshu.io/upload_images/14451551-39e3163ffff5858a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- Git把工作区的文件添加至暂存区
输入以下命令在工作区创建文件并且添加至Git暂存区
```
touch hello01.c
touch hello02.c
git add hello01.c
git add hello02.c
```
至此，hello01.c和hello02.c两个文件已经添加至Git暂存区，我们可以输入```git status```查看Git暂存区的状态信息，如:
![image.png](https://upload-images.jianshu.io/upload_images/14451551-5ce1ecbe28bd4507.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 删除Git暂存区中的文件
输入以下命令删除Git暂存区中的hello01.c文件
```
git rm --cached hello01.c
```

![image.png](https://upload-images.jianshu.io/upload_images/14451551-9422eae5330af7af.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
至此，hello01.c文件已经从Git仓库中移除了。
也可以使用```git rm -f +文件名```命令把Git工作区中的文件和Git暂存区中的文件一起删除(慎用)。
- Git把暂存区的文件提交至Git仓库
```git commit -m'加上简述'```
![image.png](https://upload-images.jianshu.io/upload_images/14451551-b365fadcc58c607a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 把本地Git仓库上传至远程仓库
用到一开始新建远程仓库时提供的命令
```
git remote add origin https://github.com/XXX(用户名)/XXX(远程仓库名).git
git push -u origin master
```
![image.png](https://upload-images.jianshu.io/upload_images/14451551-f997b788e73ec8b7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
这时我们回到Github刷新一下
![image.png](https://upload-images.jianshu.io/upload_images/14451551-f053dcd29c926bed.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
至此，完成从Git至Github的工作流程了。
#用Git从Github上克隆项目
```git clone + 项目地址```
![image.png](https://upload-images.jianshu.io/upload_images/14451551-c7049e83ab7485cf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
克隆下来之后 提交到Git仓库后直接``` git push ```即可
# 用Github创建静态网页  
就是说可以挂一个html网页上去，但是要遵循以下规则:
- repository名必须为:用户名.github.io
- 仓库中必须要有一个index.html文件
- 访问域名为:用户名.github.io
![image.png](https://upload-images.jianshu.io/upload_images/14451551-126631fcba35f615.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/14451551-85ec332d2c6fdbf1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
# 创建Github pages
可以用现有的一些样式主题快速搭建一个项目主页或者个人博客
仓库名称随意，如果购买了域名甚至可以自定义域名。
在仓库里点击setting后,拉到最下面。
![image.png](https://upload-images.jianshu.io/upload_images/14451551-77d239b065730967.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
最后页面的内容用markdown在README.MD里修改。
最后效果图:
![image.png](https://upload-images.jianshu.io/upload_images/14451551-d53cf2c8efb9c764.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

