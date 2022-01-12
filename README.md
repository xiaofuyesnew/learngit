# 标题

## 12.27

> flex

1. 不知道什么时候用flex来布局
  什么时候用其他的
2. 没有构建布局的思路
3. css的掌握还不熟悉

> 1. 在任何的地方都可以使用flex布局，你可以这样理解，flex布局可以应用在任何父子容器关系，需要规则排序的地方，此外，少部分定位需要用到 `position` 。在布局方面，这两者可以应用在所有的场景。
> 2. 试着重现自己看到的 app 布局，有思考，多练习，对于布局就有一个直观的概念。出一个题：淘宝首页这个布局怎么处理。
> 3. 这个没有捷径可以走，除了了解基础知识还要多练习，参考上一个问题出的题目

## 12.28

> git

1. git暂存区，是必须要把文件从工作区提交到暂存区才能上传到分支吗？如果不提交到暂存区能上传到分支吗？
2. 为什么有时候合并的时候出先merge: dve - not something we can merge不能合并的东西（文件名可能出现错误，用git branch查看当前分支）
3. 合并冲突只能手动修改吗？

> 1. 你要建立一个关联：`git add .` 将已修改的文件放置在暂存区； `git commit -m 'xxx'` 提交更改； 这两步发生在你本地，也就是在你工程文件的一个 `.git` 隐藏文件夹里面的操作。只有在你本地文件有`提交`的状态下，你才能向远程 `push` 你的更改。当然，在 vs code 的 git 功能中，直接填入 `message` 点击提交，其实是将`add` 和 `commit` 操作合并了。另外，如果要获知当前的 git 状态，可以用 `git status` 来查看。
> 2. `merge` 的时候你要注意，因为多人协作的时候多人可能会编辑同一个文件，这个文件在 git 进行分支合并的时候会被认为是冲突 `conflict` , 你需要先把冲突的地方编辑好，然后，对冲突编辑完成后的更改进行提交，才可以进行 `merge` 。
> 3. 只能手动修改，自动不存在的，因为多人修改同一个文件，git 无法判断哪一部分是需要的，而哪一部分需要删除。因此，在正式的 `git-flow` 工作流中有专门的 `registry administrator` 才有权限去合并分支。

## 12.29

> grid

1. grid-column 和 grid-row 两个属性没懂（column代表行/列  grid-row在第几行）

> 1. grid 布局只了解即可，它用于比较标准的工业设计和规范化 UI 中，平时直接使用的比较少。如果想快速了解这个概念范畴，可以去看看一些知名的 UI 库当中的 `layout` 组件。

## 12.30

>弹性布局

1. 响应式布局和弹性布局的区别，什么时候用哪一个会更好一些？

> 1. 两者不在同一个概念级别，响应式布局指的是当设备或浏览器在尺寸改变时，对应的布局方式会随着尺寸的改变而改变，它是一个综合的结果，可以通过 `html` 、 `CSS` 、`js` 来实现，比如通过媒体查询在宽度变化时，显示不同的 PC 端和移动端布局，通过 `window.resize` 来控制页面变化时的行为，等等；弹性布局，仅指代在 `CSS` 范畴中使用了 `display: flex;` 的布局方式。

## 1.5

> 回答问题

1. 用div把页面分为三部分：导航栏  内容部分 版权部分

把导航栏分成四部分：上层导航栏 右边内容 中间轮播图 左边内容 一个大div套着其他小div加上class容易调用，在用ul li a input 来填充内容
在用css：margin padding width height float慢慢调试

## 1.10

> JavaScript

1. 声明变量 let const var 有什么区别，尽量少用var来声明变量吗?

> [参考教程](https://es6.ruanyifeng.com/#docs/let)
>
> 直接说结论：不要用 `var`
>
> 原因：因为 `var` 可以重复定义，是顶级作用域，并且存在变量提升

> `let` `const` 和 `var` 的区别：
>
> 块级作用域，不存在变量提升，不可重复定义
>
> `let` 和 `const` 的异同：
>
> 不同点：`let` 定义的变量（基本类型和引用类型）可以重复赋值，`const` 不能，但引用类型的属性或方法可以赋值
>
> 相同点：块级作用域（{}），先声明后调用，不能重复声明

---

***要求：***

1. 使用 `playground` 来做淘宝的页面，工具不只是学习的，还需要用；
2. 淘宝的页面使用 `@media` 来实现在同一个页面上的响应式布局，`F12` 移动模式来开发一套移动端的样式；
3. 移动端样式自己尝试写，不要抄样式，写好注释；
4. 移动端思考用纯的 `flex` 布局来完成移动端的样式。
5. 持续提问题。

---
