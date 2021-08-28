# <img src="https://github.com/Aetopia/Lunar-Client-Lite-Launcher/blob/main/Logo.png" alt="image.png" width="30" height="30">  Lunar Client Lite 启动器
<b>:注意: 这是原仓库的简体中文汉化版本，除了修改翻译之外，背景图片改为洛谷图床获取。</b>  
<b>:注意: 项目状态: 维护模式 （仅修复 Bug。）</b>  

Lunar Client Lite 是一款简单的轻量级和 unlocked 启动器，具有以下特点：
1. 快速版本切换
2. 自定义 JVM 参数支持
3. 多启动目录支持
4. 一个简单易用的界面

## 使用条件
在开始使用 LC Lite 之前，请确保已安装 Lunar Client 端，并确保已安装你喜欢的的 LC 版本。
（如果你没有安装LC，则 LC Lite 将下载最新的 Lunar Client 安装程序。）

<b>LC Lite 只有在购买 Minecraft 后才可以使用</b>
## 如何使用 & 启动？
<b>如果 `LCL.exe` 被杀毒软件误报，请加其到杀毒软件白名单。</b>
1. 在这里下载最新构建
原版：https://github.com/Aetopia/Lunar-Client-Lite-Launcher/releases  
简体中文汉化版：https://github.com/Dian-Jiao/Lunar-Client-Lite-Launcher/releases  

2. 启动 `LCL.exe`.

3. 当 LC Lite 启动时，应该长这样： 

[![image.png](https://i.postimg.cc/L85jVd5R/image.png)](https://postimg.cc/v4R1QN5S)

~~图片懒得改了，下同~~

4. 设置你的 LCL 设置。  
点击 `选项` 页面。    

[![image.png](https://i.postimg.cc/bvFCRHpV/image.png)](https://postimg.cc/VSnWftSX)     

在 `JVM 额外参数` 处设置你的 JVM 额外参数。
该参数默认设置为 `-Xms3G -Xmx3G -XX:+DisableAttachMechanism`.。

在这个页面，你可以自定义通过点击 `✎` LC 1.7-1.17 的启动路径。   

取消勾选 `Cosmetics` 复选框可以减少 LC's 启动时间并且修复 `"标题画面未响应"` 或者 `"启动时未响应"` 的问题。    
取消勾选该选项会禁用 Lunar Client 的 cosmetics。此更改仅限于该程序启动的客户端。  

点击 `保存` 按钮保存你的设置，

5. 点击 `关于` 页面查看 Lunar Client Lite 相关信息和访问额外选项。 
 
[![image.png](https://i.postimg.cc/T2r8TFRR/image.png)](https://postimg.cc/3WJfBL46)   

在 `About` 页面，可以单击给定的链接查看我的 GitHub 个人资料、查看 LC Lite 的 GitHub 存储库以及加入 Couleur Tweak Tips Discord Server 的邀请链接。

如果单击 `重置`按钮，您可以重置 LC Lite 的设置并重新下载 LC Lite 的 ~~GitHub 存储库~~ 从洛谷图床放的资源文件。

如果您单击 `打开` 按钮，您可以打开 LC Lite 的日志文件夹。

6. 通过 `版本` 下拉框选择任何版本。


[![image.png](https://i.postimg.cc/NFT2nYT2/image.png)](https://postimg.cc/64WQ7kMB)   

7. 最后点击启动按钮启动游戏。  
<i>无法通过 LC Lite 启动 LC？ 确保通过官方 LC 启动器下载了所需版本！</i>  
<b>注意：要更新 Lunar Client 及其依赖项，必须使用官方 LC 启动器来更新。</b>

# 下面的我不想翻译了 爆炸了 反正没什么用

### Which JVM Arguments are good for LC?  

LC uses OpenJDK 16 so they aren't many "optimal" JVM arguments which you can find online.  
Here is a list of arguments you can use for LC via LC Lite which I consider optimal.  

1. Using this argument can be useful if you are low on RAM since using this argument will force LC to use only 1.5 GB of RAM.  

```
-Xmx700m  
```

2. This is a slightly modified version of MC's default arguments for OpenJDK 16. From what I have seen using these arguments will make LC use 4 GB (5 and above will cause memory leaks) RAM and should provide optimal performance.  

 ```
-Xms4G -Xmx4G -XX:+UnlockExperimentalVMOptions -XX:+UseG1GC -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=32M
```  
3. This is a slightly modified version of MC's default arguments for OpenJDK 16. Here MC clears out RAM more slowly as compared to any other arguments listed here. This should also provide optimal performance alongside the other arguments listed here.

```
-XX:+UseG1GC -Xmx4G -Xms4G -Dsun.rmi.dgc.server.gcInterval=2147483646 -XX:+UnlockExperimentalVMOptions -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=32M
```

# Extras
## Information on `wrapper.cmd`
Via `wrapper.cmd` its possible to specify arguments to launch a specific version of Lunar Client.    

To use this functionality of the script, use the following format:  
`wrapper.cmd "Version" "Asset Index of the Version" "JVM Arguments" "Directory" "Lunar Client Cosmetic Textures Directory"`  
i.e  
```
wrapper.cmd "1.8" "1.8" "-Xms3072m -Xmx3072m" "%APPDATA%\.minecraft" "%USERPROFILE%\.lunarclient\textures" 
```
This will launch `LC 1.8` and will allocate 3 GB to LC and will have cosmetic textures enabled.    

<b>OR</b>  
```
wrapper.cmd "1.8" "1.8" "-Xms3072m -Xmx3072m" "%APPDATA%\.minecraft" 
```
This will launch `LC 1.8` and will allocate 3 GB to LC and will have cosmetic textures disabled. 

## Logs
LC Lite also generates a `logs` folder.  
[![image.png](https://i.postimg.cc/5yJkDYfn/image.png)](https://postimg.cc/TLk9DPLD)  
Here, you can view the latest log for the latest Lunar Client instance or view any log for a previous Lunar Client instance.

## Credits
<b>Original launch command made by [`lemons#2555`](https://github.com/respecting)  
LCLI Settings Patcher made by [CTT](https://dsc.gg/CTT) (Original Optifine Patcher made by `temp`)  
This Project is based off [LCLI](https://github.com/couleur-tweak-tips/utils/blob/main/LCLI.bat) made by [Couleur](https://github.com/couleurm)</b>

