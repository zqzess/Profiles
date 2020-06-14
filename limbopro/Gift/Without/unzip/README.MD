## 更新说明 
### 06.14.2020 
1. Quantumult X 最新版本（v.1.0.10）已重新支持远程脚本（不完全版），博主仍建议大家使用 WorkingCopy 本地脚本，会更方便；
### 04.13.2020 
想玩脚本签到的小伙伴可追踪 https://github.com/chavyleung/scripts ；
### 04.12.2020
0. 重复教程 **第一步**，下载仓库最新的 **zip文件** 或使用 使用 [WorkingCopy](https://limbopro.xyz/archives/workingcopy.html) 同步最新仓库文件到手机📱 ；（⚠️再次下载⬇️ **zip文件📃** 前请先删除 [Script]文件夹📁内 已经解压的文件，因为 iPhone 文件没有覆盖这一说...； ）
1. 然后进入 QuantumultX ，点击右下角 [三菱按钮] - [重写] - [引用] - 点击 [unzip适配版] 更新
2. ⚠️第一次使用 [WorkingCopy](https://limbopro.xyz/archives/workingcopy.html) 同步最新仓库文件 ，亦需要清空 [Script] 内的所有文件；

### 04.10.2020
0. 教程 **第一步** 中增加了使用 **workingcopy** 克隆GitHub仓库到手机📱本地的方法；
### 04.09.2020
1. 本次更新已精简 [Rewrite_local] 配置，并引用了 unzip适配版的 Js.conf
2. 请重复一次教程 **第二步** 的操作，并重新配置证书📄；
3. 然后进入 QuantumultX ，点击右下角 [三菱按钮] - [重写] - [引用] - 点击 [unzip Rewrite] 更新 
4. 未来只需执行 该操作以及 重复 **教程第一步** 即可（届时会有更新说明），无须再重新配置证书📄；

---

## 正文部分


![Quantumult x for limbopro][1]

## 毒奶预配置文件（unzip版）说明

0. 利用 Quantumult X 自带的 [配置文件] - [下载] 功能对 Quantumult X 各个模块即参数进行预配置；
1. 利用 NobyDa 贡献的脚本解锁🔓各项事务，VSCO，Termius，网易蜗牛读书会员等；
2. 另外默认配置的是 🔓 美区App Store下载的 Tiktok；届时自己进 [QuantumultX] - [配置文件] - [编辑] - 找到 Tiktok 修改参数即可 
3. Surge/Clash 用户可以使用由毒奶提供的 订阅转换 API，亦能获得相同的效果；https://limbopro.xyz/archives/subconverter.html

## 本预配置文件所引用到的仓库
0. 在此毒奶对大家的付出表示感谢
1. [NobyDa](https://github.com/NobyDa/Script/tree/master) 脚本仓库（*如删库可替换 NobyDa 为 limbopro，其他同理）
2. [ConnersHua](https://github.com/ConnersHua/Profiles/tree/master) 神机规则
3. [limbopro](https://github.com/limbopro/Profiles/tree/master/limbopro) 机场专线
4. [Qure](https://github.com/Koolson/Qure/tree/master/IconSet) 开源图标
5. [chavyleung](https://github.com/chavyleung/scripts) 签到脚本

## 关于策略及分流的说明
⚠️ 本预配置文件默认8个策略，如上方**预览图**中所示；按以下 **具体操作** 操作完毕后即可在 Quantumult X 主界面看见。

- **故障切换**：该策略组自动检测组内节点可用情况（surge 会切换选中最低延迟节点）；
- **机场专线**：主流机场域名分流规则，例如 N3RO ，你可使其请求走代理，直连等；
- **社交媒体**：国外社交媒体，如Twitter/Facebook/Instagram/Telegram 等，**流量消耗小，但需要稳定**；
- **苹果服务**：苹果服务相关分流规则；
- **Netflix**：鉴于大家喜欢看 Netflix；
- **其他国外流媒体**：如油管，P站等一切你可以想得到国外流媒体，**流量消耗大**；
- **广告拦截**：默认选择 `Reject`，广告拦截可能会造成某些错误🙅，届时 将 **广告拦截** 的 **策略偏好** 修改为 PROXY 或 Direct 即可；
- **Final**： 排除以上已知的分流规则的其他未知；

在 [配置] - [编辑] - [filter_remote] - 对应如下：（供参考）
```
https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/AdRule.list, tag=野比去广告（稳定版）, force-policy=🛑 广告拦截, enabled=true
https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/AdRuleTest.list, tag=野比去广告（测试版）, force-policy=🛑 广告拦截, enabled=false
https://raw.githubusercontent.com/limbopro/Profiles/master/limbopro/airports.list, tag=机场专线, force-policy=✈️ 机场专线, enabled=true
https://raw.githubusercontent.com/ConnersHua/Profiles/master/Quantumult/X/Filter/Media/Netflix.list, tag=Netflix, force-policy=🎥 Netflix, enabled=true
https://raw.githubusercontent.com/ConnersHua/Profiles/master/Quantumult/X/Filter/GlobalMedia.list, tag=其他国外流媒体, force-policy=🎥 其他国外流媒体, enabled=true
https://raw.githubusercontent.com/ConnersHua/Profiles/master/Quantumult/X/Filter/Global.list, tag=社交媒体, force-policy=📲 社交媒体, enabled=true
https://raw.githubusercontent.com/ConnersHua/Profiles/master/Quantumult/X/Filter/Apple.list, tag=苹果服务, force-policy=🍎 苹果服务, enabled=true
```

* GEOIP,CN,DIRECT，默认中国大陆网站均走直连；

## 特殊情况
⚠️ 如果你已经正在使用 QuantumultX，并且**只想通过JS脚本解锁🔓相应事务**，无需遵循以下完整**具体操作**，则仅需执行其中两步即可：
1. 按 **具体操作** 中第一步，将脚本仓库下载到手机📱；
2. 进入 QuantumultX ，点击右下角 [三菱按钮] - [重写] - [引用] ，
3. 右上角 [+]  https://raw.githubusercontent.com/limbopro/Profiles/master/limbopro/Gift/Without/unzip/Js.conf ，同步；
4. 按 **具体操作** 第三步（⚠️，如果你之前已经生成并信任📄证书，则这一步可以省略；务必开启相应开关）
5. 以上。

## 具体操作
💡 完整视频对照操作教程请参阅：https://t.me/limboprossr/1702 或参阅 YouTube https://www.youtube.com/watch?v=4Sy0HUcOvYk&loop=0 （该视频教程不包含生成证书与信任证书📚）

### 第一步 ⏬ 下载 脚本仓库压缩包
💡✅ **第一步  ⏬ 下载 脚本仓库**， 博主建议尽量使用 [WorkingCopy](https://limbopro.xyz/archives/workingcopy.html) 替代，以方便以后更新（后期脚本仓库更新只需在在 WorkingCopy 内下拉即可更新），**如不想使用 WorkingCopy ，请继续看下文**；

1. https://github.com/NobyDa/Script/archive/master.zip （*如删库可替换 NobyDa 为 limbopro，其他同理）
2. 复制上述并在 Safari 打开下载，打开下载的文件
3. 下载成功后，进入 [文件]App - [我的iPhone] - [下载项] 找到  Script-master.zip 并解压
4. 进入解压后的 文件夹 [Script-master]
5. 右上角 点击 [选择] - [全选]
6. 点击底部 中间类似 文件夹的按钮 📂 （移动）
7. 选择 [我的iPhone] - [Quantumult X] - [Scripts]
8. 点击 右上角 的 [移动] 按钮
9. 完成

### 第二步 ⏬ 下载 毒奶自用预配置文件（unzip版）

1. 复制 https://raw.githubusercontent.com/limbopro/Profiles/master/limbopro/Gift/Without/unzip/QuantumultX4limbopro.conf 预配置文件链接；
2. 进入 QuantumultX ，点击右下角 [三菱按钮]
3. 找到 [配置文件] 模块下的 [下载] 点击
4. 粘贴 刚刚复制的配置 [链接]，点击 右上角 [确定] 按钮
5. 确认，届时 QuantumultX 已添加 8个策略

### 第三步 生成并配置证书
1. 进入 QuantumultX ，点击右下角 [三菱按钮]
2. 找到 [MitM] 模块 - 生成并配置证书📄 

- 进入QuantumultX，点击页面右下角三菱`按钮`，找到`MinM`模块，点击`生成证书`，提示生成成功，点击`安装证书`此时会跳转至` Safari`，提示`此网站...下载一个配置描述文件。您要允许吗？`，点击`允许`，网页提示`已下载描述文件`；
- 进入 iOS 系统`设置`-` 通用`-`描述文件`-`已下载的描述文件`-选中，并安装，输入密码...完成描述文件安装；
- 进入 iOS 系统`设置`-` 通用`-`关于本机`-`证书信任设置`-`针对根证书启用完全信任`-选中刚刚安装的并启用即可；

3. 找到 [重写] 模块 - 开启按钮 🔘
4. 找到 [MitM] 模块 - 开启按钮 🔘

### 第四步 订阅并为各个策略添加或删除节点
1. 机场怎么订阅就不说了
2. 进入 QuantumultX 主界面，可长按各个 **策略图标** 以 为该策略添加/减少节点；
3. 有红色感叹号❕标注的节点务必删除；


## Faq 
在反馈问题前，请多看看 **网络活动日志模块**（QuantumultX 主界面 **橘红色** 的日记本标识，里面📝了你的各个网络请求）；多熟悉一下 QuantumultX 操作界面，可能帮助你解决很多常见问题。

### 备份你的机场订阅链接🔗
1. 进入 QuantumultX ，点击右下角 [三菱按钮]
2. 找到 [配置文件] 模块 - 点击 [编辑] - 找到 [server_remote] 
3. 复制 [server_remote] 下方的机场订阅链接🔗 存到某处备用
4. 届时 恢复时 重新再 [server_remote] 下方 粘贴即可

### 使用毒奶预配置文件后的一些检查
1. 如果出现错误提示，不要慌
2. 进入 QuantumultX 主界面 - 各个图标点一下 看一下
3. 熟悉一下

## 已知存在问题及解决办法
### 使用 unzip 版预配置文件后，微博开屏广告没有去掉
**A 两个方面**

1. 确保 Quantumult X 已安装证书📄并且信任
2. 进入 QuantumultX ，点击右下角 [三菱按钮] - 找到 [配置文件] 模块 - 点击 [编辑] - 找到 [rewrite_local] 下  `去微博应用内广告 (By yichahucha)` 被 # 号 注释的那行，删除 # 号即可；

```
#^https?://(sdk|wb)app\.uve\.weibo\.com(/interface/sdk/sdkad.php|/wbapplua/wbpullad.lua) url script-response-body QuantumultX/File/wb_launch.js
```

### Tiktok 如何换区
0. Tiktok 老是推荐美国🇺🇸用户上传的视频？换下国别代码即可；


1. 进入 QuantumultX ，点击右下角 [三菱按钮] - 找到 [配置文件] 模块 - 点击 [编辑] - 找到 [rewrite_local] 下 关于 Tiktok 部分，将 US 换成 其他国别代码即可； 国别代码参考：https://limbopro.xyz/usr/uploads/2019/10/3740990267.png

```
(?<=(carrier|sys)_region=)CN url 307 US
```

2. 换成 JP；看看日本🇯🇵妞；
2. 另外，不是换了就马上就切换到日区的，多刷几个视频就有日区用户推荐了；

### 野比去广告测试版引发的问题
1. 目前已知会导致 QQ 定位不能正常发起
2. 使用 [抖音去水印下载ios捷径](https://limbopro.xyz/archives/1560.html#h-44) 下载抖音视频时会出现断连；
3. 已默认禁用；可进入 Quantumult x，[分流] - [引用] 中 找到，并右滑开启/禁用；

### 及时更新
*保持更新。

1. [分流] - [引用] 更新
2. [重写] - [引用] 更新
3. unzip 版本更新；

## 最后 BTW
因为这个配置文件也是我自用的，会保持更新，但一般无太大问题不建议大家每次跟随更新。

### 进阶玩法
https://limbopro.xyz/archives/3846.html

### 关注频道
https://t.me/limboprossr

[1]: https://raw.githubusercontent.com/limbopro/Profiles/master/limbopro/Gift/Without/unzip/QuantumultX4limbopro.PNG
