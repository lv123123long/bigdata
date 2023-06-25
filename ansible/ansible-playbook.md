# ansible-playbook

* 每个play和task  名称具有唯一性

## 模块参数传递

* **copy: src=/etc/passwd dest=/tmp**     也可以换行写

* 使用args参数声明接下来的是参数

## 模块参数里面的变量

* inventory_hostname   该变量表示的是当前正在执行任务的目标节点在inventory中定义的主机名

# 模块（不满足幂等性的四个模块）

## command

* 执行简单shell命令，不支持特殊符号

## shell

* 和command一样，但是支持特殊符号

## raw

* 执行底层shell命令，command和shell都是执行上层python代码启动/bin/sh

* 如果目标主机没有安装python，就只能使用raw模块了

## script

* 在远程主机执行该脚本文件

* 不要求目标主机安装好了python

## 指定其他解释器

* 比如expect执行expedct脚本，perl执行perl脚本

* 在args参数里面添加：参数executeable: 解释器

# 参数

## 外部参数

* -v   显示详细信息
* --start-at-task   指定执行哪个任务 ，ansible-playbookassert.yml --start-at-task="print origin fail msg"
* --step参数，以交互的方式一步一步执行，每步任务的执行都需要输入三个选项中的一个：**N（跳过）Y（执行）C（继续执行后面所有步骤）**
* -c 或者 --connection  选项来指定连接方式，，，也可以在play和task级别上指定连接方式

## 内部参数

* creates参数：当指定的文件或目录存在时，则不执行命令

* removes参数：当指定的文件或目录不存在时，则不执行命令

## 连接

* 默认情况下，ansible是使用ssh连接，连接方式是smart

* smart是智能选择ssh和paramiko，当ansible支持安装的ControlPersist（即持久连接时）选择使用ssh，否则使用paramiko

* local和docker是非基于ssh连接的方式

* winrm是连接windows的方式

* inventory中也可以通过连接的行为变量ansible_connection指定连接类型
  
  ```
  192.168.200.29 ansible_connection="smart"
  ```
  
  
