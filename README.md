# -Monkey

# Android 暴力测试 Monkey

基于adb 自动暴力测试 Monkey

# 第一、安装方法


1、Android Studio自带，在SDK目录下找到ADB的存放路径。先Win+R键，进入cmd 控制界面检查ADB是否可能用

![2781551-7b4d22f66d81e611](https://user-images.githubusercontent.com/13359093/211736603-ac473a7b-6d5e-4947-91db-33d49fafbd5c.png)


2、找到ADB的存放路径。AS安装完成以后adb如果没更改路劲基本存在SDK的platform-tools文件下面

![2781551-e7ee7f31a4efb654](https://user-images.githubusercontent.com/13359093/211736650-aa8ed066-46c4-4fa4-a6d4-12de6ec1f45f.png)

3、在电脑的高级设置Path 路径 配置下环境变量 ，环境变量配置应该挺简单都会的吧。下面的配置方法。在弹出编辑环境变量空白出 按新建按钮输入自己的adb所在路劲，最后按确定 >确定就O了。

![2781551-70fca983f9f84d4c](https://user-images.githubusercontent.com/13359093/211736708-e9c88fb4-0383-4c50-a1e0-c43d884799a5.png)

4、就是检查ADB 配置的环境变量能不能用
Win键+R打开命令cmd再输入adb
如果输入adb按回车弹出这些信息，那就恭喜配置adb环境成功了。

![2781551-49c0a83a469966b3](https://user-images.githubusercontent.com/13359093/211736762-4ff6a832-d8d9-40fc-be85-2c1d44562fd6.png)

# 第二、查看ADB安装成功后就是连接手机进行暴力测试玩玩了。

1、手机连接电脑Studio表示能进行调试

![2781551-f8a788741ca4a344](https://user-images.githubusercontent.com/13359093/211736849-30b9bd59-d490-47ae-afe1-53a8c69a14ed.png)

2、也就是关键的一步，也就一句命令符，Win键+R打开命令cmd，然后输入

```
adb shell monkey -p xxx.xx.x--throttle 300 --ignore-crashes --ignore-timeouts --ignore-security-exceptions --monitor-native-crashes -v -v -v 1000 >F:/Logcat.txt >F:/error.txt
```

路径说明； adb shell monkey -p 自己应用包名 --throttle 300 --ignore-crashes --ignore-timeouts --ignore-security-exceptions --monitor-native-crashes -v -v -v 设置的自动点击次数>日志为输出详细日志存放路径以及输出文件名 >为测试的log输出日志及文件名称

3、输入正确的命令符 就可以了 ，让它自己跑完 点击设置的次数

![2781551-ac5d698e240aea54](https://user-images.githubusercontent.com/13359093/211737002-72a54bab-9b85-4973-a01c-691fb84cd07d.png)


4、就看到 你设置的路径下有两个 txt 设定的文件 F:/error.txt



![2781551-703f21460ca8c88f](https://user-images.githubusercontent.com/13359093/211737052-4b65097e-6056-4fc7-a4e7-88b8536c1d88.png)

到此就算已经走了一个自动化暴力Monkey测试了，有兴趣可以玩一玩！！！

