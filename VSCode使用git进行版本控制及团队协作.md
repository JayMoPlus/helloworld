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