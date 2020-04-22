# 公主连结 国服 刷初始脚本 fork of [bbpp222006](https://github.com/bbpp222006/Princess-connection)

### TODO：
1. 自动识别验证码  https://github.com/Dawnnnnnn/bilibili-captcha
2. 自动复制 `/data/data/com.bilibili.priconne/shared_prefs/*` 以保存游客号信息 **注意：游客号在线时常只有15分钟**
3. 到达10级结束刷本而不是用光体力
4. 多线程
5. nogui虚拟机运行

## 简介
此项目为公主连接脚本. 使用opencv图像识别进行按钮分析.

目前的功能只有刷初始号. 以后可能增加新功能. 敬请期待.


## 环境
python包:
```
pip install opencv-python==3.* -i https://pypi.tuna.tsinghua.edu.cn/simple/
pip install matplotlib -i https://pypi.tuna.tsinghua.edu.cn/simple/
pip install uiautomator2 
```

windows端需要adb工具.
`adb devices`

若使用模拟器,则需要将模拟器设置为桥接模式.  具体参考这个项目(https://github.com/Jiahonzheng/JGM-Automator)

设置好后命令行运行
`python -m uiautomator2 init`
对模拟器进行初始化  

接着在手机(模拟器)上打开 ATX(小黄车) ，点击 启动 UIAutomator 选项，确保 UIAutomator 是运行的。

**模拟器分辨率要求540*960,手机版本.**

## 刷初始号功能
本项目下zhanghao.txt为待刷账号与密码. 
每一行用tab作为账密的分割(其实你可以在源码中修改读取方式)

jieguo.txt是账号上最后三星的结果.

**当前不支持游客号刷初始,各位使用的时候请一定修改zhanghao.txt里的内容**

## 使用

`python main.py`
