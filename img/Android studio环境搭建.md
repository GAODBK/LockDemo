<a name="j7epA"></a>
# jdk，gradle 下载
1. 在`Oracle `官网，注册账号，下载`jdk8`or`jdk11`
> 不用下太高级的版本，因为需要注意  Gradle版本与Java版本的对应关系

![image.png](https://cdn.nlark.com/yuque/0/2024/png/35479677/1709268847963-36252499-e52d-4328-92cf-7639e71296de.png#averageHue=%23f9f9f9&clientId=ua86d579d-4a8c-4&from=paste&height=430&id=u6040750e&originHeight=538&originWidth=534&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=18159&status=done&style=none&taskId=u5c59d4c9-d563-4ea9-8e9a-66329e41329&title=&width=427.2)

2. 去`gradle 官网`下载，由于我看不懂别人的解释，直接跟着他们的版本号 进行操作 下载，故下载的`gradle6.1.1`
3. 配置`GRADLE_USER_HOME`环境
```java
GRADLE_USER_HOME
D:\environment\gradle-6.1.1
```
<a name="wJfvh"></a>
# 下载 as 与SDK
Android studio 在官网 下载 不难，

- 不过 接着就要下载 AndroidSDK 了，这玩意 要连接 Google 的（故：启动clash，准备 20个G 的国外流量 和 一个小时的时间（网速越好，下载越快））；
- 若能正确的下载完SDK，通过`设置`>`SDK Manager`查看SDK的下载内容，
   - 这个AndroidSDK在电脑D盘占了9.8G，C盘也是差不多 这么大的内存消耗
   - 但大概率 在 `SDK Tools` 页面缺少了 `Command-line Tools` 这个工具，等待下载一下（这个是为了 flutter 的开发做准备，flutter 需要这个东西）

![image.png](https://cdn.nlark.com/yuque/0/2024/png/35479677/1709303842955-9cb548a9-e9ae-425b-877b-03f1224310f5.png#averageHue=%232c2f35&clientId=uba5ae9a3-ce84-4&from=paste&height=350&id=dHVXN&originHeight=437&originWidth=465&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=40800&status=done&style=none&taskId=u6c8013c5-7443-4dcd-97aa-1c265b60f30&title=&width=372)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/35479677/1709269701296-405fd25a-e59b-4806-803c-8451f6b13051.png#averageHue=%232d3135&clientId=ua86d579d-4a8c-4&from=paste&height=365&id=UkHtM&originHeight=456&originWidth=1133&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=87256&status=done&style=none&taskId=ub15ea155-42e1-4b34-83ae-771c43a4c83&title=&width=906.4)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/35479677/1709269726167-e722a2c7-5c85-4ef9-9f82-3d6724c2b29b.png#averageHue=%232e3135&clientId=ua86d579d-4a8c-4&from=paste&height=454&id=uc9ebbb3e&originHeight=568&originWidth=1128&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=100338&status=done&style=none&taskId=u304da80e-4909-4dc1-a1c7-a2b3994ffa7&title=&width=902.4)
<a name="LYlsZ"></a>
# 打开一个安卓项目
![image.png](https://cdn.nlark.com/yuque/0/2024/png/35479677/1709270196028-9ace049d-e160-4540-8321-ffde4ed97b6d.png#averageHue=%232e3135&clientId=ua86d579d-4a8c-4&from=paste&height=498&id=u9a6c944c&originHeight=622&originWidth=512&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=54384&status=done&style=none&taskId=u92edfecd-2221-46fa-8d2b-f9b0fc81993&title=&width=409.6)
<a name="aAiuR"></a>
### 先用较快的手速，关闭底部的自动下载
在2024年，下载Android studio 新建一个项目  程序设计为默认下载 gradle8.3.0，而且还TM不好找 下方的两个文件

> 安卓开发克隆github上的项目到本地后
> 替换APP下的build.gradlle
> 和project下的build.gradle
> 将setting.gradle替换


<a name="EHAU1"></a>
## 打开`build.gradle`文件
修改版本号，项目刚下载下来时，版本号是：.build:gradle:3.5.1'，修改为.build:gradle:4.0.1'
```java
// Top-level build file where you can add configuration options common to all sub-projects/modules.

buildscript {
repositories {
    google()
    jcenter()

}
dependencies {
classpath 'com.android.tools.build:gradle:4.0.1'
//        classpath 'com.android.tools.build:gradle:6.1.1'
}
// NOTE: Do not place your application dependencies here; they belong
// in the individual module build.gradle files

}

allprojects {
    repositories {
        google()
        jcenter()

    }
}

task clean(type: Delete) {
    delete rootProject.buildDir
}
```
这是我看的 对于 gradle 版本号 在 as 的解释在后续的操作中，我会解释我对这个的设置（偏转的解释）<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/35479677/1709269393691-4662630c-53f4-4595-b472-8e1ee11583b2.png#averageHue=%23fbfbfb&clientId=ua86d579d-4a8c-4&from=paste&height=599&id=ud14e1005&originHeight=749&originWidth=679&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=75587&status=done&style=none&taskId=ucd3b1cbb-5afd-4226-bc38-635f221fd14&title=&width=543.2)<br />[Just a moment...](https://stackoverflow.com/questions/56016265/could-not-find-com-android-tools-buildgradle5-1-1)
<a name="FB7Tr"></a>
## 打开`gradle-wrapper.properties`文件

1. 配置 `GRADLE_USER_HOME`环境
2. 注释掉 下载 网址链接，如果是在第一步没有下gradle，那在这一步需要下载
```java
#Fri Mar 01 10:58:54 CST 2024
distributionBase=GRADLE_USER_HOME
distributionPath=wrapper/dists
# distributionUrl=https\://services.gradle.org/distributions/gradle-6.1.1-bin.zip
zipStoreBase=GRADLE_USER_HOME
zipStorePath=wrapper/dists
```
gradle 询问大佬 给的解释![205642ca2c6d7a772f1f099b00720f8272972966.jpg@!web-comment-note.webp](https://cdn.nlark.com/yuque/0/2024/webp/35479677/1709302859513-f6fe855e-9855-40f9-a09a-54207a66a4e2.webp#averageHue=%233b3f34&clientId=uba5ae9a3-ce84-4&from=drop&id=u488ea4e8&originHeight=682&originWidth=2250&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=48692&status=done&style=none&taskId=u9f98b9fc-ec93-46ac-990b-99340009e49&title=)<br />指定`gradle wrapper`的版本号（的下载版本）

指定`gradle插件`的版本号。如果你使用外置的gradle，只需要更新外置gradle的版本号就可以了<br />![0f8ebad0ae9cb4f59d9c3c4c74450c3b72972966.png@!web-comment-note.webp](https://cdn.nlark.com/yuque/0/2024/webp/35479677/1709302896058-9a9534c6-d603-4d17-9a0f-c3ab81c71c37.webp#averageHue=%23484b3b&clientId=uba5ae9a3-ce84-4&from=drop&id=ud571c399&originHeight=796&originWidth=2172&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=43510&status=done&style=none&taskId=u2a4c70b3-59a8-4d95-838e-c5ac280f104&title=)
<a name="tEbgy"></a>
## 调用下载到本地的Java与gradle
使用自己下载好 的`gradle`与`Java`进行环境配置，省一点翻墙流量，<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/35479677/1709271368825-64c28e76-321a-458d-96ba-3de9d40a29c2.png#averageHue=%232e3339&clientId=ua86d579d-4a8c-4&from=paste&height=326&id=ud5794008&originHeight=266&originWidth=681&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=37748&status=done&style=none&taskId=u62969485-9588-4efe-a3a9-877d5f4ecb6&title=&width=834.7999877929688)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/35479677/1709271736684-2cd27bd9-73e4-4caf-bd22-8ba672c3c563.png#averageHue=%232d3339&clientId=ua86d579d-4a8c-4&from=paste&height=267&id=ua83ec5f8&originHeight=504&originWidth=1475&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=132159&status=done&style=none&taskId=u4769f5b8-4715-4054-81e7-ed3d9c79aa8&title=&width=781)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/35479677/1709272039413-7cf4dbef-f09f-49e2-a117-37d9a22fe53f.png#averageHue=%23272a2e&clientId=ua86d579d-4a8c-4&from=paste&height=552&id=u58230535&originHeight=690&originWidth=1244&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=127128&status=done&style=none&taskId=u698e5b20-e2cc-4e2b-87fa-9d79e0b4b63&title=&width=995.2)
<a name="IxZMs"></a>
## 可以使用命令行与as 启动项目了
下载了模拟器，会看到模拟器的名字，已经出现，先启动模拟器，在启动项目，构建程序，出现在模拟器里<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/35479677/1709272149383-8a53b600-f17c-490e-8a83-d6801b99ce83.png#averageHue=%23388a28&clientId=ua86d579d-4a8c-4&from=paste&height=121&id=u4c7488ee&originHeight=151&originWidth=700&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=23823&status=done&style=none&taskId=ucd6ee14b-0fa9-45ed-9ae7-cf402c832fc&title=&width=560)

