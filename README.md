# SMU XCPC Wiki

本项目的作用是

- 发布训练信息
- 个人、队伍的训练 Wiki ，可以用来记录训练过程、心得体会、感悟等
- Blog，虽然本项目也可以作为博客使用，但是使用前请联系管理员

参加本项目的先决要求

- SMU XCPC 集训队正式队员
- 有 git 一点基础，不会的可以参考[Git教程 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/896043488029600)、[git入门笔记](https://www.cnblogs.com/PHarr/p/16416136.html)
- 会使用Markdown
- 本地有python环境，有GitHub账户

注意事项

- 禁止修改根目录下除`docs`外任何文件
- 在`docs/队员`、`docs/队伍`目录下禁止修改除本人及其所属队伍以外的任何文件
- 修改`docs`目录下其他文件之前要与项目的负责人联系

符合以上条件，并且想参与本项目的可以通过各种方式联系`PHarr`

# 使用教程

首先确保本地`Python`、`Python package manager pip`，要求`Python3`，且版本不要太老。

安装MkDocs

```sh
pip install mkdocs
```

安装成功后可以尝试在命令行中执行`mkdocs -V`如果可以看到版本号就说明安装成功。

MkDocs 的使用方法可以通过`mkdocs -h`查看，也可以[ MkDocs 文档开发教程](https://mkdocs-like-code.readthedocs.io/zh_CN/latest/)。但是本项目不需要过于复杂的功能只看本教程也可以学会

这里我们使用了一款主题，所以要安装这个主题
```sh
pip install mkdocs mkdocs-material
```

如果安装不上或者安装速度慢可以尝试更换安装源
```sh
pip install --trusted-host pypi.douban.com -i http://pypi.douban.com/simple/ mkdocs mkdocs-material

```

---

克隆项目之前要先加入组织，加入组织请私信管理员

克隆项目，在本地找到合适的位置，打开命令行输入

```sh
git clone https://github.com/SMU-XCPC/wiki
```

然后你可以在本地看到一个文件夹`wiki`，以下简称`wiki`为根目录

---

再除第一次克隆项目外，每一次要修改之前都要先在根目录下执行，从云端更新本地文件

```sh
git pull
```

新建页面，在`Member`目录下新建一个以自己名字命名的Markdown文件即可，例如`PHarr.md`

注意本项目你的Markdown只能有一个一级标题，并且是自己的名字，可以有多个二级标题或三级标题。格式如下例如

```markdown
# PHarr

## 获奖记录

## 训练情况

## To Do List
```

因为你的一级标题会直接在侧边栏显示，其他标题则会在点开对应页面后显示

新建好文件后你就可以自由发挥创作了，再次提醒**不要修改其他人的界面**

队伍类似，直接在`队伍`目录下创建就好

---

你在记录过程中可以直接在本地预览你的markdown文件

同时你也可以在根目录下打开终端，输入

```sh
mkdocs serve
```

然后打开浏览器输入`http://127.0.0.1:8000/`实时预览最终效果，注意在浏览器中预览必须要在本地文件保存后才会更新

如果想要关闭本地预览只需要关闭终端窗口即可

---

当你写完之后，你要将你文件上传

首先你应该进入到根目录下

```sh
git add .
```

修改加入到缓存区中

```sh
git commit
```

更新版本，注意此时会让弹出文本编辑器让你填写更新哪些内容，请不要直接关闭，而是填写这些内容，可以简略，如果不知道写什么，就写上你的ID。

```sh
git push
```

将本地文件修改推送到Github。

```sh
mkdocs gh-deploy
```

最后执行，更新网页，因为pages是静态服务，所以更新会有一些延迟

Github国内访问不太稳定，这是正确推送的截图

![image-20230210184931515](https://s2.loli.net/2023/02/10/USh4DtkCJfEQ72w.png)

![image-20230210185013636](https://s2.loli.net/2023/02/10/qBhoztaWDAvTVdu.png)

