[README.md](https://github.com/GAODBK/LockDemo/files/15209159/README.md)

> 这是我clone学习的第一个Android程序，描述的很繁杂

1. 资料：[在GitHub上开源的Android项目](https://github.com/still-soul/LockDemo.git)，[阿里在语雀上提供的一份讲解](htt    ps://www.yuque.com/antfe/featured/fc36a0ngy28g1982)
  4
  5
  6
2. 展示锁屏组件在`息屏后重新唤起界面`的效果
  8
    - 息屏后按下电源键拉起展示的锁屏界面。用户手机息屏后不用重新解锁进入到页面，提升使用体验
 10
 11
 12
3. 修改后实现效果
 14
| 打开程序界面告诉你，需要提供权限![hello world页面](.\img\873183982.jpg) | 给予程序权限后，锁屏页面效果![](.\img\873183944.jpg) |
| ------------------------------------------------------------ | ------------------------------------------------    ---- |

 18
**Android 项目导入**： 在`img`文件夹中 使用 VScode 打开 `Android studio环境搭建.md` 简单来说：
 20
- 替换`APP`下的`build.gradlle```
- `project`下的`build.gradle`
- 将`setting.gradle`替换为本地的可执行语句

 25 通过设置 `提供`程序所需要的`权限`
![锁屏显示权限](.\img\spxs2.png)
![后天弹出权限](.\img\httc2.png)   
