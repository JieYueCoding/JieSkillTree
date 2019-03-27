# Git



## Git的诞生

自2002年开始，[林纳斯·托瓦兹](https://zh.wikipedia.org/wiki/%E6%9E%97%E7%BA%B3%E6%96%AF%C2%B7%E6%89%98%E7%93%A6%E5%85%B9)决定使用[BitKeeper](https://zh.wikipedia.org/wiki/BitKeeper)作为[Linux内核](https://zh.wikipedia.org/wiki/Linux%E5%85%A7%E6%A0%B8)主要的版本控制系统用以维护代码。因为BitKeeper为[专有软件](https://zh.wikipedia.org/wiki/%E4%B8%93%E6%9C%89%E8%BD%AF%E4%BB%B6)，这个决定在社群中长期遭受质疑。在Linux社群中，特别是[理查德·斯托曼](https://zh.wikipedia.org/wiki/%E7%90%86%E6%9F%A5%E5%BE%B7%C2%B7%E6%96%AF%E6%89%98%E6%9B%BC)与[自由软件基金会](https://zh.wikipedia.org/wiki/%E8%87%AA%E7%94%B1%E8%BB%9F%E9%AB%94%E5%9F%BA%E9%87%91%E6%9C%83)的成员，主张应该使用开放源代码的软件来作为Linux内核的版本控制系统。[林纳斯·托瓦兹](https://zh.wikipedia.org/wiki/%E6%9E%97%E7%BA%B3%E6%96%AF%C2%B7%E6%89%98%E7%93%A6%E5%85%B9)曾考虑过采用现成软件作为版本控制系统（例如[Monotone](https://zh.wikipedia.org/wiki/Monotone)），但这些软件都存在一些问题，特别是性能不佳。现成的方案，如[CVS](https://zh.wikipedia.org/wiki/%E5%8D%94%E4%BD%9C%E7%89%88%E6%9C%AC%E7%B3%BB%E7%B5%B1)的架构，受到林纳斯·托瓦兹的批评[[15\]](https://zh.wikipedia.org/wiki/Git#cite_note-15)。

2005年，[安德鲁·垂鸠](https://zh.wikipedia.org/wiki/%E5%AE%89%E5%BE%B7%E9%AD%AF%C2%B7%E5%9E%82%E9%B3%A9)写了一个简单程序，可以连接BitKeeper的存储库，BitKeeper著作权拥有者[拉里·麦沃伊](https://zh.wikipedia.org/wiki/%E6%8B%89%E9%87%8C%C2%B7%E9%BA%A5%E6%B2%83%E4%BC%8A)认为安德鲁·垂鸠对BitKeeper内部使用的[协议](https://zh.wikipedia.org/wiki/%E7%BD%91%E7%BB%9C%E4%BC%A0%E8%BE%93%E5%8D%8F%E8%AE%AE)进行[逆向工程](https://zh.wikipedia.org/wiki/%E9%80%86%E5%90%91%E5%B7%A5%E7%A8%8B)，决定收回无偿使用BitKeeper的许可。Linux内核开发团队与BitMover公司进行磋商，但无法解决他们之间的歧见。林纳斯·托瓦兹决定自行开发版本控制系统替代BitKeeper，以十天的时间编写出git第一个版本[[16\]](https://zh.wikipedia.org/wiki/Git#cite_note-16)[[17\]](https://zh.wikipedia.org/wiki/Git#cite_note-17)。



## Git的作用

**git**是用于Linux内核开发的版本控制工具。与[CVS](https://zh.wikipedia.org/wiki/%E5%8D%94%E4%BD%9C%E7%89%88%E6%9C%AC%E7%B3%BB%E7%B5%B1)、[Subversion](https://zh.wikipedia.org/wiki/Subversion)一类的集中式版本控制工具不同，它采用了分布式版本库的作法，不需要服务器端软件，就可以运作版本控制，使得源代码的发布和交流极其方便。git的速度很快，这对于诸如Linux内核这样的大项目来说自然很重要。git最为出色的是它的合并追踪（merge tracing）能力。



## Git的操作

### 通过 Git 克隆 GitHub上的代码

通过`clone`命令创建的本地仓库，其本身就是一个 Git 仓库，不用我们再进行`init`初始化操作，而且自动关联远程仓库。我们只需要在这个仓库进行修改或者添加等操作，然后`commit`即可。

**第一步**

输入`git clone git@github.com:JieYueCoding/JieSkillTree.git`命令，其中`clone`后面所接的链接为我们刚刚复制的远程仓库的地址.



### 通过 Git 将代码提交到 GitHub

我们需要先了解两个命令，也是我们在将来需要经常用到的两个命令，分别为push和pull.

- push：该单词直译过来就是“推”的意思，如果我们本地的代码有了更新，为了保持本地与远程的代码同步，我们就需要把本地的代码推到远程的仓库，代码示例：

```
git push origin master
```

- pull：该单词直译过来就是“拉”的意思，如果我们远程仓库的代码有了更新，同样为了保持本地与远程的代码同步，我们就需要把远程的代码拉到本地，代码示例：

```
git pull origin master
```

**第一步**

输入`git add`和`git commit -m "注释信息"`命令，将文件添加并提交到仓库

**第二步**

输入`git push origin master`命令，将本地仓库修改（或者添加）的内容提交到远程仓库



**注意**：**在我们向远程仓库提交代码的时候，一定要先进行pull操作，再进行push操作，防止本地仓库与远程仓库不同步导致冲突的问题，尤其是第二种提交代码的情况，很容易就出现问题。**