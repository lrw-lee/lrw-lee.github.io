---
title: tmux
date: 2020-05-08 11:14:19
tags:
- tmux
categories:
- 工具
---
一款优秀的终端复用软件。当关闭终端后,再次打开时原终端里面的任务不会中断 ;处于异地的两人可以对同一会话进行操作，一方的操作另一方可以实时看到 ;单个屏幕的灵活布局；

<!-- more -->

### Session

1. 新建会话
``` bash
$ tmux new -s session1
```

2. 退出会话
> ctrl+b d

3. 退出会话
> ctrl+b d

4. 终端环境查看会话列表
```bash
$ tmux ls
```

5. 会话环境中查看会话列表
> ctrl+b s 

6. 从终端环境进入会话
```bash
$ tmux a(attach) -t session1
```

7. 终端销毁会话
```bash
$ tmux kill-session -t session1
```

8. 会话环境销毁会话
> ctrl+b : 状态栏变黄色输入kill- session -t session1 回车

9. 终端重命名会话
```bash
$ tmux rename -t old_session_name new_session_name
```

10. 会话环境重命名当前会话
> ctrl+b $ 	输入new_session_name

### Window:

1. 修改当前窗口名
> ctrl_b ,

2. 创建window
> ctrl+b c

3. 关闭window：ctrl+b &
4. 切换window

  - ctrl+b p(previous) 切换到上一个window

  - ctrl+b n(next) 切换到下一个window

  - ctrl+b 0 切换到0号window

  - ctrl+b w 列出当前session所有window，通过上下键切换

  - ctrl+b l(L) 相邻的window切换

### Pane:

1. 垂直分屏
> ctrl+b % 

2. 水平分屏
> ctrl+b " 

3. 关闭pane ctrl+b x 关闭当前使用中的pane
4. 切换pane

  - ctrl+b o 依次切换当前窗口下的各个pane

  - ctrl+b Up|Down|Left|Right 根据箭头方向切换到某一个pane

  - ctrl+b Space(空格) 对当前窗口下的所有pane重新排列

  - ctrl+b z 最大化当前pane，再按一次恢复
