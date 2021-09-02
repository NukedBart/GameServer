# 代码贡献
我们现在正在寻找有兴趣贡献此项目的人.  
我面现在需要以下领域的程序员:
* C#
* Python
* Electron
* Node.js
* Angular
* Socket.io

有关项目的更多信息请导航至 https://leaguesandbox.github.io/  
如有贡献想法，请加入 [Discord](https://discord.gg/0vmmZ6VAwXB05gB6) 或 QQ群 216683185.

# Pull requests

所有贡献者在 Pull request 被合并前必须签署 CLA (Contributor License Agreement, 贡献者许可协议). 这将会被 Pull request 的相关机器人接管, 以取保贡献的代码会合法使用 AGPL-3.0 协议.

# 代码提交

## 在提交前必须发表对应的 Issue

所有的提交必须有其对应的 issue. 以便于我们追踪该提交解决的问题与将会带来的问题.

## 代码提交模板:
```
解决 Issue 引用 -- 提交标题

提交简介

相关 Issue 引用
```
例如:
```
解决 #123 问题 -- 实现 foo

实现了 foo

相关 #123
```

你也可以使用 `进步` 而非 `解决` 一个 Issue, 以应对无法完全解决 Issue 的情况.

**上述向导是有关 _代码提交_ 信息的, 不是 _PULL REQUEST_ 请求！**
# 项目规则
* 每行的代码长度必须小于120个字符 (使用 Editor Guidelines 插件可以更好地帮助你追踪此问题)
* Pull requests 合并前必须先被审核
* Pull requests 在成功构建前不予合并
    * 如果遇到失败构建的 Pull request, 请联系该 Pull request 并告知其修改 Pull request
* 文件夹名称使用 `DaTuoFengMingMing` 大驼峰命名
* JSON 字典键使用 `DaTuoFengMingMing` 大驼峰命名
* 使代码清晰可读，便于理解
* 所有函数与公开变量必须有与项目规范一致的 Summary 内容.
* 不同功能需要在不同功能的分支(branch) 内完成
* 代码提交需要保持小批量逻辑性强的提交风格
* Pull requests 需要尽可能精简, 1个功能, 1个 pull request
    * 例如要提交一个实现了3个功能的 pull request, 你需要写一个功能提交一次, 分3次提交

# C# 开发指南
* 函数名使用 `DaTuoFengMingMing` 大驼峰命名
* 常量名使用 `QUAN_DA_XIE_MING_MING` 全大写命名
* 私有(private) 变量名使用 `_daiXiaHuaXianDeTuoFengMingMing` \_带下划线的驼峰命名
* 公开(public) 属性名 (public propertie { get; set; }) 使用 `DaTuoFengMingMing` 大驼峰命名
* 所有 `公开(public)` 变量的访问需要使用 get; 和 set;
* `代码折叠(#region)` 不允许使用, 代码量大时将代码分割成不同的类和文件
* 字典遍历使用 `switch` 与 长 `if/else` 判断语句
* 布尔值(boolean) 变量名需使用疑问驼峰命名 (is/can/should, canCastSpell/isCasting/shouldStopCasting)
* 所有 `if/else/while/for/foreach/try/catch/finally/lock` 语句必须使用大括号 (`{}`), 即使是一行.
* 尽量规避使用三目运算. `tiaojian ? xuanxiang1 : xuanxiang2`
    * 在适当的地方你是可以使用三目运算的，但还是要尽量避免使用
* 不允许使用带有条件判断的 内插字符串/格式字符串(Interpolated strings)

# 开发工作流及如何使用 git终端(git shell)
**强烈推荐使用 git终端(git shell) !!!**

1. 拉取最新的 indev 分支(branch)
    * `git fetch -p`
    * `git pull origin indev`
2. Checkout 一个新的 分支(branch)
    * `git checkout -b <fenzhi_ming>`
3. 更改代码, 提交代码
    * `git status` - 查看被修改的文件
    * `git add <filename>` - 将文件标记为将要提交
    * `git add -u` - 标记所有被更新的文件 (文件名匹配，内容不匹配)
    * `git add -A` - 标记所有未标记的文件
    * `git commit -m "<tijiao xinxi>"` - 提交代码更改
4. 推送(push) 到 github
    * `git push origin <fenzhi_ming>`
5. 创建 pull request
6. Checkout 到 indev
    * `git checkout indev`
7. 重复上述步骤

# 标签系统

使用了标签系统的 Issue 更方便辨认. 标签被分为几组, 命名为组名的第一个字母加上方便记忆的描述语. 同组标签颜色相同. 所有 Issue 均需要有相应的标签.

## 功能标签
代码功能相关的标签.

| 标签 | 简介 |
| -------------- | -------------- |
| A-ai | AI 人工智能功能相关 |
| A-collision | 碰撞\[体积/算法\]功能相关 |
| A-connection | 连接功能相关 |
| A-content-pipeline | 内容加载功能相关 |
| A-networking | 网络连接功能相关 |
| A-packets	| \[数据包/报文\]功能相关 | 
| A-script-engine | 脚本引擎功能相关 (物品脚本, 英雄脚本) |
| A-security | 安全功能相关 |
| A-tools | 工具相关 |
| A-vision | 视觉相关 |

## Blocker
Issue is blocking on something before it can be resolved

| Tag label | Description |
| -------------- | ----------- |
| B-reproduce | Blocked on a need to reproduce problem locally |
| B-needs-verification | Blocked due to missing verification |
程序水平不够深，无法翻译

## 难易度标签
解决 Issue 的难易度.
| 标签 | 简介 |
| -------------- | ----------- |
| E-easy | 修复不费吹灰之力 |
| E-good-first-issue | 帮助你了解项目的好 Issue |
| E-help-wanted | 有没有人来救救我啊 ? |

## 影响力标签
Issue 未被解决会导致的后果.

| 标签 | 简介 |
| -------------- | ----------- |
| I-cleanup | 不会影响项目; Issue 是为了项目代码整洁性提交的. |
| I-crash | 崩端了! |
| I-enhancement | 不会影响项目; Issue 提出了一些希望加入的功能或丢失的功能 |
| I-performance | 不必要的内存占用或性能损失 |
| I-wrong | 看到 bug 了 |

## 优先级标签
Issue 的优先级.

| 标签 | 简介 |
| -------------- | ----------- |
| P-high | 高优先级 |
| hacktoberfest | Hacktoberfest, no prefix cause it's a 特殊的 github 标签 iirc |

## 状态
Issue 的状态.

| 标签 | 简介 |
| -------------- | ----------- |
| S-clarifying | Issue 需要更多细节才可以解决 |
| S-has-open-pr | Issue 已经被人提过了 |
| S-testing-needed | 需要更多测试 |
| S-unverified | Issue 未被验证是否存在 |
| S-verified | Issue 确实存在诶 |
| S-wont-fix | 我就是不修 |
| invalid | 刷屏了啊 |

# P.S. 译者的话
buff列表在 [这里](https://github.com/NukedBart/GameServer/blob/indev/buff.md)
