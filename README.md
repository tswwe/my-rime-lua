# Introduction

Thanks to [librime-lua](https://github.com/hchunhui/librime-lua), users can extend [RIME](https://rime.im) functions with Lua scripts.

This repository contains some (currently only one) Lua scripts that I wrote or modified for RIME and [RIME_JD](https://gitee.com/xkinput/Rime_JD):

## xnumber.lua

### Features

A yong-style number typing experience in RIME. Triggered via `=` by default.

![xnumber](img/xnumber.gif)

### Usage

1. Download and put the `xnumber.lua` script into `RIME_USER_DATA/lua/` folder.
2. Modify (or create if not existing) `RIME_USER_DATA/rime.lua` by adding one line: `number_translator = require("numberx")`.
3. Modify your schema (like `xkjd6.schema.yaml`) by adding an item like `- lua_translator@number_translator` under the `engine/translators` section. Attention: Since this script use `=` as default trigger key, you should check if it conflicts with your schema.
4. Re-deploy RIME and enjoy.