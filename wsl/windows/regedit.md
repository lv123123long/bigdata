# 将应用注册到右键菜单

## 第一步

* 首先确认你安装了markdown文件的编写工具

* 比如Typora，MarkText等

## 第二步 regedit

* **win+R**，**输入**regedit打开注册表

* 查找 “**计算机\HKEY_CLASSES_ROOT\.md\ShellNew**”，找到 "**.md**"文件夹

* 在 “**.md**”文件夹下的 “**ShellNew**”文件夹中，(如果没有该文件夹，手动创建一个即可)创建“**字符串值**”；

* 将新建的字符串值 命名为“**NullFile**”

* 选中新建的“**NullFile**”，右键修改，在数值数据输入"**typora.md**",确定保存；

* 或Markdown.md

## 参考文档

* [参考1，我的实践]([win10如何鼠标右键新建Markdown文件？ - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/152310631#:~:text=win10%E5%A6%82%E4%BD%95%E9%BC%A0%E6%A0%87%E5%8F%B3%E9%94%AE%E6%96%B0%E5%BB%BAMarkdown%E6%96%87%E4%BB%B6%EF%BC%9F%201%20%E9%A6%96%E5%85%88%E7%A1%AE%E8%AE%A4%E4%BD%A0%E5%AE%89%E8%A3%85%E4%BA%86markdown%E6%96%87%E4%BB%B6%E7%9A%84%E7%BC%96%E5%86%99%E5%B7%A5%E5%85%B7--Typora%3B%202%20win%2BR%20%EF%BC%8C%20%E8%BE%93%E5%85%A5%20regedit,3%20%E6%9F%A5%E6%89%BE%20%E2%80%9C%20%E8%AE%A1%E7%AE%97%E6%9C%BA%5CHKEY_CLASSES_ROOT%5C.md%5CShellNew%20%E2%80%9D%EF%BC%8C%E6%89%BE%E5%88%B0%20%22%20.md%20%22%E6%96%87%E4%BB%B6%E5%A4%B9))

* [参考2，我觉得合理]([鼠标右键添加新建.md文档（亲测成功） - 简书 (jianshu.com)](https://www.jianshu.com/p/3f9aa45c1af1))
