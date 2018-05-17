## 环境
- 请确保你安装了最新的VS Code.http://code.visualstudio.com/
- 请确保安装了最新版的Git。https://git-scm.com/download。git安装到环境变量里， 确保任意路径可以访问。
- 参考链接：https://code.visualstudio.com/Docs/editor/versioncontrol

## 初始化
- 创建一个文件夹，我这里命名为gittest(随便起的)

- 用VS Code 打开这个文件夹，单击左侧的git图标
![](https://github.com/xuanhun/vscode/raw/master/3.jpg)

- 单击“初始化GIT存储库”的按钮

- 再回到我们的文件中，刚才的操作创建了一个.git文件夹，放置了当前仓库的所有 配置文件，如下图。
![](https://github.com/xuanhun/vscode/raw/master/6.jpg)

- 到目前为止我们在本地创建了一个代码仓库，下面来看一下VS Code的git功能。

## git 输出

## 提交保存
- 提交保存的第一步是暂存文件。
- 第二步是输入提交信息。
- 第三步然后使用状态栏的提交按钮提交全部更改。


## git命令列表
- ctrl+shift+P，输入git，会看到VS CODE支持的所有git命令。
![](https://github.com/xuanhun/vscode/raw/master/9.jpg)

- 撤销操作
输入 Undo Last Commit，撤销上次操作。输入Unstage,撤销暂存。
![](https://github.com/xuanhun/vscode/raw/master/10.jpg)

- 分支
输入Branch可以创建当前内容的分支。创建分支时需要输入分支名称。
![](https://github.com/xuanhun/vscode/raw/master/12.jpg)

- checkout
创建分支后，使用checkout命令可以拉取特定的分支内容。
![](https://github.com/xuanhun/vscode/raw/master/13.png)

- 冲突合并
VS Code 会检测文件冲突，并以<<<<<,>>>>,====和颜色区分出来。

## 连接远程代码仓库
说了这么多，现在问题来了，在本机初始化一个代码库，一般没什么卵用。 我们大多数情况是要连接远程的代码服务器的。

下面我们在github上创建一个Repository，复制地址备用。
```
git remote add origin +github项目地址，例如：
git remote add origin git@github.com:JayMoPlus/helloworld.git
```

现在我们查看一下.git文件夹下的config文件，可以看到添加了远程Reps地址。

![](https://github.com/xuanhun/vscode/raw/master/18.jpg)

接下来我们从下拉菜单中执行发布命令。
![](https://github.com/xuanhun/vscode/raw/master/19.jpg)

之后，会把本地提交的文件同步到github。同步之后再打开git的隐藏菜单，可以看到 同步等命令可以直接使用了。

## 正式使用
- vs code打开git工作区就会看到所有代码显示在这里 

![](http://upload-images.jianshu.io/upload_images/2065390-a262f07bfbd6248a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

-  点击+号，把所有文件提交到暂存区。 然后打开菜单选择–提交已暂存的 相当于`add .`
- 然后按提示随便在消息框里输入一个消息，再按ctrl+enter提交 相当于`·`commit -m`
- 然后把所有暂存的代码push云端，相当于`git push -u origin master`

# 团队协作
## 加入组织并建立分支
- 创建组织并添加成员：在用户首页左下角有一个组织选项，点击添加组织。界面如下：
-  创建项目组并添加分支:进入之后，点击添加项目，就可以添加项目了
-  每个成员都建立一个分支(并用成员名字命名，这个适合小团队)

## 开始团队协作

- 同步远端内容到本地
> 这里的master是你开发的项目主分支，开发前先将远端内容同步下来，因为别人可能合并了新的内容到主分支，为了保证开发进度的一致，需要先pull下主分支内容。
- 将改动推送到远端分支
```
 git checkout 你的开发分支名 //切换到你的开发分支
```
> 现在你可以进行开发，开发完成并确认无误后你可以将改动推送到远程开发分支。

> 这一步时，很多人会碰到没有分支的情况，这里说明一下。如果你clone的时候，远端项目的分支还没有建立，你clone下来的项目是没有分支结构的，需要你自己新建分支并推送到远端仓库或者· 在远端仓库分支建立后再次clone，就会将仓库的分支结构也clone下来。`git checkout -b jaymo666 master    # 新建jaymo666分支，并切换到该分支

```
$ git add * //t添加所有改动文件到暂存区
$ git commit -m "开发说明"  //添加提交说明
$ git push origin 你的开发分支名
```
- 这里只是将改动推送到属于你自己的开发分支，所以这里的分支名是为你建立的开发分支的名字。
## 将远端分支合并到主分支
现在你已经在本地进行了一些开发了，并且确认这些开发可以使用，想要推送到主分支，让大家在这个基础上继续开发，所以你需要合并到主分支
```
$ git branch -a  //查看本地和远程所有分支，带*号是当前所在分支。
$ git checkout master //切换到主分支
$ git merge 你的开发分支名 //将你的开发分支合并到主分支
git push origin master    # 推送master分支代码到远端
git push origin --tags    # 推送tag到远端
```
> 合并到主分支后，所有的成员拉取的内容都会改变，所以合并到主分支一定要谨慎。

###【参考来源】
- https://ovenzeze.github.io/git-team-wrok/