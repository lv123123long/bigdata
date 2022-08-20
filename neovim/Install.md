# Install

## 安装篇

* 先下载，再解压安装

## 配置篇

* 我们采用的是lua配置
* neovim的配置文件放在~/.config/nvim/init.lua 文件中

### 目录划分

* ftplugin：存放不同文件类型的缩进规则文件
* lint：存放各种语言的代码检查规范配置文件
* baseic：存放基本配置文件
* conf：存放插件相关配置文件
* dap：存放DAp相关配置文件
* lsp：存放lsp相关配置文件
* snippet：存放代码片段相关文件

### 文件说明

* init.lua：配置文件入口
* config.lua：存放用户自定义配置文件
* keybinds.lua： 存放键位绑定的文件
* plugins.lua：存放依赖插件的文件
* settings.lua：存放neovim基本配置项的文件

## 操作提示

```
mkdir -p ~/.config/nvim/{ftplugin,lint,lua,snippet}
mkdir -p ~/.config/nvim/lua/{basic,conf,dap,lsp}
touch ~/.config/nvim/init.lua
touch ~/.config/nvim/lua/basic/config.lua
touch ~/.config/nvim/lua/basic/keybinds.lua
touch ~/.config/nvim/lua/basic/plugins.lua
touch ~/.config/nvim/lua/basic/settings.lua

```



