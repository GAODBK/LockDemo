> 这是我clone学习的第一个Android程序，描述的很繁杂
> <br>由于记不住github password，只能使用上传压缩包的形式而分享修改后的代码，见`Releases`
> <br>虽然这个clone仓库 根目录下LockDemo.zip也是修改后的源代码

1. 资料：[clone的是这个GitHub上开源的Android项目](https://github.com/still-soul/LockDemo.git)，
   [也可以看看 阿里 在 语雀app 上提供的一份讲解](https://www.yuque.com/antfe/featured/fc36a0ngy28g1982),
   <br>[由于图片加载不出，到gitee上看看`/chuanglang/lockdome-README`吧](https://gitee.com/chuanglang/lockdome#https://gitee.com/link?target=https%3A%2F%2Fwww.yuque.com%2Fantfe%2Ffeatured%2Ffc36a0ngy28g1982)

3. 效果描述：
   - 息屏后按下电源键 会先拉起 展示海报界面。用户手机息屏后 不用重新解锁进入到app页面，提升使用体验
   - 打开程序 有消息推送效果（大小通知效果都有，通知对黑色模式进行了适配
   - 但奇怪的是 miui13的手机 有锁屏通知效果，originos4没有锁屏通知效果）

4. 修改后效果图
   | 打开程序界面告诉你，需要提供权限，见`/img/873183982.jpg`        | 给予程序权限后，锁屏页面效果，见 `img/873183944.jpg` |
   | --------------------------------------- | ---------------------------- |
   | ![](img/873183982.jpg) | ![](img/873183944.jpg) |
   | ![](img/24.jpg) |  ![](img/36.jpg)|

5. **Android 项目导入**： 
   - 替换`APP`下的`build.gradlle`
   - `project`下的`build.gradle`
   - 将`setting.gradle`替换为本地的可执行语句

6. 通过设置为程序`提供`所需要的`权限` 

   - 设置权限需求见： `/img/spxs2.jpg`  和  `/img/httc2.jpg`
   - ![锁屏显示权限](img/spxs2.png)
   - ![后天弹出权限](img/httc2.png)
