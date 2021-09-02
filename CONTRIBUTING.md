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

**下面的向导是有关 _代码提交_ 信息的, 不是 _PULL REQUEST_ 信息！**
# 项目规则
* 每行的代码长度必须小于120个字符 (使用 Editor Guidelines 插件可以更好地帮助你追踪此问题)
* Pull requests must be approved before they can be merged
* Pull requests should not be merged before the build has passed
    * If the build fails, ping the pull request creator and tell him to fix it
* Files and folders in `PascalCase`
* JSON dictionary keys in `PascalCase`
* Keep the code as simple and clear to read as possible
* All functions and public variables should have summary comments which follow the standard found throughout the project already.
* Each separate feature should be developed in their own branch
* Commits should be in logical small pieces
* Pull requests should be kept as small as possible, generally one feature per pull requests
    * Instead of submitting one huge pull request with 3 features, submit each feature individually

# C# guidelines
* Function names in `PascalCase`
* Constants in `ALL_CAPS`
* Private variables in `_camelCaseWithUnderscore`
* Public properties as getters / setters in `PascalCase`
* All `public` variable access should happen through getters / setters
* `#region`s shouldn't be used, instead split code into classes/files when needed
* Dictionaries preferred over `switch`es and long `if/else` statements
* Boolean variable names should be prefixed with a question (is/can/should)
* All `if/else/while/for/foreach/try/catch/finally/lock` clauses should be wrapped inside brackets (`{}`), even if they are only one line.
* Conditional operator should be avoided. `condition ? option1 : option2`
    * This is fine to use in some niche cases where you can't avoid using it
* Interpolated strings with embedded logic should not be used

# Development flow and how to use git shell
**Using git shell is strongly encouraged**

1. Pull latest version of indev
    * `git fetch -p`
    * `git pull origin indev`
2. Checkout to a new branch
    * `git checkout -b <branch_name>`
3. Make changes, do commits
    * `git status` - List of changed files
    * `git add <filename>` - Stage file for commit
    * `git add -u` - Stage all updated files for commit
    * `git add -A` - Stage all unstaged files for commit
    * `git commit -m "<commit message>"` - Create commit
4. Push to github
    * `git push origin <branch_name>`
5. Create pull request
6. Checkout back to indev
    * `git checkout indev`
7. Repeat

# Tag system

Issues uses tag system that make them easier to identify. Tags are grouped into several groups named with first letter of the group name followed by a short-hand descriptive word or phrase. Tags in group are in same color. Every issue should have relevant tags.

## Area
To-what part of the code is relevant?

| Tag label | Description |
| -------------- | -------------- |
| A-ai | Content releated to Artificial Intelligence |
| A-collision | Content releated to collision |
| A-connection | Content releated to connection |
| A-content-pipeline | Content related to loading |
| A-networking | Content related to networking |
| A-packets	| Content related to packets | 
| A-script-engine | Content related to script engine (items, champion's scripts) |
| A-security | Content related to security |
| A-tools | Content related to tools |
| A-vision | Content related to vision |

## Blocker
Issue is blocking on something before it can be resolved

| Tag label | Description |
| -------------- | ----------- |
| B-reproduce | Blocked on a need to reproduce problem locally |
| B-needs-verification | Blocked due to missing verification |

## Effort
The expected complexity of fixing the issue.

| Tag label | Description |
| -------------- | ----------- |
| E-easy | Can be easily resolved |
| E-good-first-issue | Issue which will help you get into the project |
| E-help-wanted | Assignee/Issue creator requests help? |

## Impact
The effect of the issue remaining unresolved.

| Tag label | Description |
| -------------- | ----------- |
| I-cleanup | No impact; the issue is one of maintainability or tidiness. |
| I-crash | Application crash |
| I-enhancement | No impact; the issue is a missing or proposed feature |
| I-performance | Unnecessary memory usage/Performance degradation |
| I-wrong | An incorrect behaviour is observed (bug) |

## Priority
Priority of the issues.

| Tag label | Description |
| -------------- | ----------- |
| P-high | High priority |
| hacktoberfest | Hacktoberfest, no prefix cause it's a special github label iirc |

## Status
Status of the issues.

| Tag label | Description |
| -------------- | ----------- |
| S-clarifying | This issue needs clarification |
| S-has-open-pr | There is a PR open that resolves the issue |
| S-testing-needed | Needs testing |
| S-unverified | This issue needs verification |
| S-verified | This issue has been verified |
| S-wont-fix | The issue will not be fixed |
| invalid | Used for mark spam hacktoberfest PR's as invalid (they will not count) |
