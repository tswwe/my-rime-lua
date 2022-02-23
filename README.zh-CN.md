# 仓库介绍

得益于 [librime-lua](https://github.com/hchunhui/librime-lua)，用户能够使用 Lua 脚本来扩展 [RIME](https://rime.im) 的功能。

本仓库存放一些（目前只有一个）我为 RIME and [RIME_JD](https://gitee.com/xkinput/Rime_JD) 编写的 Lua 脚本：

## xnumber.lua

### 功能

实现仿小小输入法的特殊输入模式。用 `=` 触发。

![xnumber](img/xnumber.gif)

### 用法

1. 下载 `xnumber.lua` 脚本并放到 `用户资料夹/lua/` 目录下。
2. 修改（若不存在则新建）`用户资料夹/rime.lua` ，在合适的位置添加一行：`number_translator = require("numberx")`。
3. 修改你的方案文件（如 `xkjd6.schema.yaml`），在 `engine/translators` 下添加一项： `- lua_translator@number_translator`。注意：本脚本使用 `=` 作为触发键，请检查是否与你的方案存在冲突。
4. 重新部署 RIME 即可。