# 「少女前线」跨服手册（散爆版）（iOS 端 → 安卓官服）
 > By: [Mornwind](https://github.com/Mornwind)
 > 
 > Blog: [Mornwind’s Blog](https://blog.mornwind.cc)（博客中也有教程，使用的是国内备用仓库）
 > 
 > GitHub Repo: [Mornwind/GFCN_SwitchServer](https://github.com/Mornwind/GFCN_SwitchServer) 
 > 
 > Gitee Repo: [Mornwind/GFCN_SwitchServer](https://gitee.com/Mornwind/GFCN_SwitchServer) (国内备用仓库，配置中链接已全部替换成 gitee.com，防止国内无法访问 GitHub)
 > 
 > QQ Group：
 > > 【霞之丘 · 少前跨服】:[`915089623`](https://jq.qq.com/?_wv=1027&k=5rnvPAT)（本群已于 2021/8/12 10:59 被封，损失惨重，故新群拆分成两个，分别运作）
 > > 
 > > 【霞之丘⟡少前跨服答疑】：[`907757876`](https://jq.qq.com/?_wv=1027&k=wdMRfleu)（仅跨服答疑，勿水无关话题）（请先填写[【少前跨服情况统计】](https://docs.qq.com/form/page/DREpKbGVaQWtRcGhI)收集表，便于管理员有针对性地答疑及后期通知）
 > > 
 > > 【霞之丘⟡闲聊群】：[`908042781`](https://jq.qq.com/?_wv=1027&k=Ph1teaIm)（仅闲聊，不答疑）

## 致谢

- **参考&协助**
  - [霞ヶ丘詩羽x](https://space.bilibili.com/455501)：[B站专栏（cv3630717）](https://www.bilibili.com/read/cv3630717)
  - [MoonNarga](https://github.com/MoonNarga)：[Server_Switch_for_GirlsFrontline](https://github.com/MoonNarga/Server_Switch_for_GirlsFrontline)

---

## ⚠️ 注意事项 ⚠️

1. 本项目内所提到的所有客户端与服务器，均为**国服**。
2. 跨服脚本中**并未含有**用于修改游戏内数据以获得不正当收益的作弊内容，只是用来切换服务器，故理论上不会被封号。跨服脚本代码**公开透明**地存放于本项目中，欢迎随时进行检查。如若不放心，还请另寻他法。
3. **无法进行跨服充值，否则 1000% 会错充进客户端对应的原服务器，切记！**

---

## 跨服手册
 > 常见的游戏跨服方式分类，详见前言中的[附录3](/README.md#附录3ios-端常见跨服方式)。

### A-1 类型
 > A-1：通过**使用网络调试工具**，**在本地重写客户端请求**，**直接**实现跨服。

| 图标 | 跨服工具 | 别名 | 跨服教程<br/>与配置 |
| :-: | :-: | :-: | :-: |
| ![](/Icon/HTTP_Catcher_Icon.png) | HTTP Catcher | 网球 | [文字教程](#-http-catcher) |
| ![](/Icon/Thor_Icon.png) | Thor | 锤子 | [文字教程](#-thor) |
| ![](/Icon/Shadowrocket_Icon.png) | Shadowrocket | 小火箭 | [文字教程](#-shadowrocket) |
| ![](/Icon/Quantumult_X_Icon.png) | Quantumult X | 圈叉 | [文字教程](#-quantumult-x) |
| ![](/Icon/Surge_4_Icon.png) | Surge 4 | - | [文字教程](#-surge-4) |
| ![](/Icon/Loon_Icon.png) | Loon | 气球 | [文字教程](#-loon) |

<details>
<summary>点击查看：常用网络调试工具对比</summary>

| 跨服工具 | 国区商店<br/>购买与下载 | 正规渠道价格 | 跨服操作<br/>方便程度 | 设备上同时<br/>挂梯与跨服 | 备注 |
| :-: | :-: | :-: | :-: | :-: | :-: |
| HTTP Catcher<br/>（网球） | ✅ | ¥28.00（内购）<br/>\$3.99（内购） | ★★★★ | ❌ |  |
| Thor<br/>（锤子） | ✅ | ¥88.00<br/>\$12.99 | ★★★★ | ❌ |  |
| Shadowrocket<br/>（小火箭） | ❌ | \$2.99 | ★★★★ | ✅ |  |
| Quantumult X<br/>（圈叉） | ❌ | \$7.99 | ★★ | ✅ | TF 名额已满 |
| Surge 4 | ❌ | \$49.99（首次内购）<br/>+ \$14.99/y（订阅） | ★★ | ✅ | 是真的贵 |
| Loon<br/>（气球） | ❌ | \$2.99 | ★★ | ✅ | Bug 较多 |

</details>

#### ⑴ HTTP Catcher

<details>
<summary>点击查看：配置跨服</summary>

1. **下载并导入跨服配置文件**：下载下面的“.hcc”类型的跨服配置文件，通过“共享”或“在其他应用中打开”调出系统分享菜单，然后选择“拷贝到‘HTTP Catcher’”；在 HTTP Catcher 中弹出的“导入”对话框中选择“好的”，即可成功导入。

```
https://github.com/Mornwind/GFCN_SwitchServer/raw/master/HTTP_Catcher/gfcn_ios2gw.hcc
```

2. **启用跨服配置**：进入“更多”→“重写”，在弹出的“重写列表”界面中，点击下面的跨服配置使其前面出现“✓”。
3. **启用重写功能**：在“重写列表”界面中，打开上面的“重写列表”开关；然后回到“更多”界面。
4. **启用仅记录消息头**：进入“高级设置”，打开“仅记录消息头”开关；然后回到“历史”界面。
5. **启动 HTTP Catcher**：点击下方的开关按钮，然后在清除了游戏后台的情况下进入游戏，即可完成跨服。（如无其他使用需求，不玩游戏时别忘了停止 HTTP Catcher。）

</details>

#### ⑵ Thor

<details>
<summary>点击查看：配置跨服</summary>

1. **下载并导入跨服配置文件**：下载下面的“.f4thor”类型的跨服配置（过滤器）文件，通过“共享”或“在其他应用中打开”调出系统分享菜单，然后选择“拷贝到‘Thor’”；在弹出的跨服配置（过滤器）预览界面中，点击右上角导出图标，在弹出的菜单中选择“装载”，在弹出的“安全提醒”对话框中选择“继续”，即可成功导入；然后点击左上角的“✗”，回到主界面。

```
https://github.com/Mornwind/GFCN_SwitchServer/raw/master/Thor/gfcn_ios2gw.f4thor
```

2. **选中跨服过滤器**：点击闪电按钮上方显示的过滤器名称，在弹出的“过滤器”列表中，点击选中刚导入的跨服过滤器，然后会自动返回首页。
3. **启动 Thor**：在“过滤器”主界面中，点击闪电按钮启动 Thor，然后在清除了游戏后台的情况下进入游戏，即可完成跨服。（如无其他使用需求，不玩游戏时别忘了停止 Thor。）

</details>

#### ⑶ Shadowrocket
 > 需 Shadowrocket 为 2.1.62 (1118) 及以上的 TF 或商店版本，因为新版本中才有跨服所需的脚本功能。
 > 
 > 另外，因为 2.1.67 (1156) 版本修复了一个 Bug，使得跨服以此版本为界，分为新旧两种。强烈建议更新到 2.1.67 (1156) 版本以上。

<details>
<summary>点击查看：配置跨服（新，适用于 2.1.67 (1156) 及以上版本）</summary>

##### 方法一：直接订阅简易跨服配置

1. **新建本机节点**：在首页，点击右上角“+”，添加一个类型为“HTTP”（或“HTTPS”）、地址为“localhost”（或“127.0.0.1”）、端口为“1080”（或其他在 1-65535 之间的端口）的节点，然后在首页的“服务器节点”中选中该节点。
2. **设置路由模式**：将“全局路由”设置为“直连”（或“配置”）。
3. **设置远程订阅 URL**：在“配置文件”界面，点击右上角“+”，输入下面的远程订阅 URL，点击下载。

```
https://github.com/Mornwind/GFCN_SwitchServer/raw/master/Shadowrkt/gfcn_ios2gw.conf
```

4. **下载并应用简易跨服配置**：在“远程文件”中点击该 URL，选择“使用配置”，等待下载完毕后，即可看到“本地文件”中加载了本配置。
5. **启动 Shadowrocket**：返回 Shadowrocket 的首页，打开 Shadowrocket 的连接开关，然后在清除了游戏后台的情况下进入游戏，即可实现跨服。（如无其他使用需求，不玩游戏时别忘了停止 Shadowrocket。）

##### 方法二：手动写入当前使用中配置

1. **进入配置编辑界面**：在“配置文件”界面，从“本地文件”中找到当前正在使用的配置，点击它，在弹出的列表中选择“编辑纯文本”。
2. **添加跨服配置**：在弹出的编辑窗口中，将以下配置中 `[Script]` 下方的代码，在配置文件中找到对应位置复制进去，然后点击右上角的“保存”，返回 Shadowrocket 的首页。

```
[Script]
# 少女前线 跨安卓官服
## 切换服务器
gfcn_ios2gw = type=http-request,script-path=https://github.com/Mornwind/GFCN_SwitchServer/raw/master/Shadowrkt/gfcn_ios2gw.js,pattern=^http:\/\/gfcn-transit\.ios\.sunborngame\.com\/index\.php,max-size=1048576,requires-body=true,enable=true
```

3. **重启 Shadowrocket**：为确保修改生效，可以开关一次 Shadowrocket 的连接开关，然后在清除了游戏后台的情况下进入游戏，即可实现跨服。（如无其他使用需求，不玩游戏时别忘了停止 Shadowrocket。）

</details>

<details>
<summary>点击查看：配置跨服（旧，适用于 2.1.62 (1118) ～ 2.1.67 (1155) 版本）</summary>

##### 方法一：直接订阅简易跨服配置

1. **新建本机节点**：在首页，点击右上角“+”，添加一个类型为“HTTP”（或“HTTPS”）、地址为“localhost”（或“127.0.0.1”）、端口为“1080”（或其他在 1-65535 之间的端口）的节点，然后在首页的“服务器节点”中选中该节点。
2. **设置路由模式**：将“全局路由”设置为“直连”（或“配置”）。
3. **设置远程订阅 URL**：在“配置文件”页面，点击右上角“+”，输入下面的远程订阅 URL，点击下载。

```
https://github.com/Mornwind/GFCN_SwitchServer/raw/master/Shadowrkt/gfcn_ios2gw_old.conf
```

4. **下载并应用简易跨服配置**：在“远程文件”中点击该 URL，选择“使用配置”，等待下载完毕后，即可看到“本地文件”中加载了本配置。
5. **启动 Shadowrocket**：返回 Shadowrocket 的首页，打开 Shadowrocket 的连接开关，然后在清除了游戏后台的情况下进入游戏，即可实现跨服。（如无其他使用需求，不玩游戏时别忘了停止 Shadowrocket。）

##### 方法二：手动写入当前使用中配置

1. **进入配置编辑界面**：在“配置文件”页面，从“本地文件”中找到当前正在使用的配置，点击它，在弹出的列表中选择“编辑纯文本”。
2. **添加跨服配置**：在弹出的编辑窗口中，将以下配置中 `[Script]` 下方的代码，在配置文件中找到对应位置复制进去，然后点击右上角的“保存”，返回 Shadowrocket 的首页。

```
[Script]
# 少女前线 跨安卓官服
## 切换服务器
gfcn_ios2gw_old = type=http-request,script-path=https://github.com/Mornwind/GFCN_SwitchServer/raw/master/Shadowrkt/gfcn_ios2gw_old.js,pattern=^http:\/\/gfcn-transit\.ios\.sunborngame\.com\/index\.php,max-size=1048576,requires-body=true,enable=true
```

3. **重启 Shadowrocket**：为确保修改生效，可以开关一次 Shadowrocket 的连接开关，然后在清除了游戏后台的情况下进入游戏，即可实现跨服。（如无其他使用需求，不玩游戏时别忘了停止 Shadowrocket。）

</details>

#### ⑷ Quantumult X
 > Quantumult X 需先通过商店版应用内的收据验证，才可正常使用应用内的各种功能（包括重写功能、远程资源、远程脚本等）。

<details>
<summary>点击查看：配置跨服</summary>

##### 方法一：远程引用重写配置片段（推荐）

1. **添加重写引用远程资源**：在主界面中，点击右下角带有 Quantumult X 图标（类似三片风扇扇页）的圆形按钮进入设置界面；在弹出的设置界面中，找到“重写”部分，点击“重写”下的“引用”；在弹出的“资源列表（重写）”界面中，点击右上角的“新建远程资源”按钮（图标为铁链⛓️带个加号⨁）；在弹出的“资源”窗口中，在“标签”中填入“少女前线 跨安卓官服”，“自动更新”间隔默认设置为“48 小时”，在“资源路径”中填入下面的远程资源 URL；然后点击右上角“保存”按钮，在弹出的成功提示中点击“确定”，返回设置界面。

```
https://github.com/Mornwind/GFCN_SwitchServer/raw/master/Quan_X/gfcn_ios2gw.snippet
```

2. **启用“重写”功能**：在设置界面中，找到刚才的“重写”部分，打开其右侧的开关启用功能；然后点击左上角的箭头返回主界面。
3. **启动 QuanX**：打开主界面右上角开关启动 Quantumult X，即可在 iOS 端跨服登录安卓国服。（如无其他使用需求，不玩游戏时别忘了停止 Quantumult X。）

##### 方法二：手动写入当前使用中配置

1. **进入配置编辑界面**：在主界面中，点击右下角带有 Quantumult X 图标（类似三片风扇扇页）的圆形按钮进入设置界面；在弹出的设置界面中，找到“配置文件”部分，点击“配置文件”下的“编辑”。
2. **添加跨服配置**：在弹出的编辑窗口中，将以下配置中 `[rewrite_local]` 下方的代码，在配置文件中找到对应位置复制进去，然后点击右上角的“保存”，返回 Quantumult X 的首页。

```
[rewrite_local]
# 少女前线 跨安卓官服
## 切换服务器
^http:\/\/gfcn-transit\.ios\.sunborngame\.com\/index\.php url script-request-body https://github.com/Mornwind/GFCN_SwitchServer/raw/master/Quan_X/gfcn_ios2gw.js
```

3. **重启 Quantumult X**：为确保修改生效，可以开关一次 Quantumult X 的连接开关，然后在清除了游戏后台的情况下进入游戏，即可实现跨服。（如无其他使用需求，不玩游戏时别忘了停止 Quantumult X。）

</details>

#### ⑸ Surge 4

<details>
<summary>点击查看：配置跨服</summary>

##### 方法一：订阅模块化配置（推荐）

1. **安装并启用跨服配置模块**：在“首页”中找到“模块”卡片（若未找到，则去“更多”→“外观”→“卡片”中将该卡片设为可见），点击“模块”，在弹出的“模块”界面中，找到“安装的模块”部分，点击“安装新模块...”，然后在弹出的“安装模块”对话框中输入下面的 URL 地址，点“好的”下载模块文件。然后在弹出的配置预览窗口中，**检查有无恶意内容并仔细阅读最下方的“警告”**，在确认无误后，点击最下方的“安装”。回到“模块”界面，即可看到跨服配置模块已成功安装，左侧有“✓”表示该模块已启用。

```
https://github.com/Mornwind/GFCN_SwitchServer/raw/master/Surge_4/gfcn_ios2gw.sgmodule
```

2. **启用“脚本”功能**：回到“首页”中，将“脚本”卡片的开关打开（若未找到，则去“更多”→“外观”→“卡片”中将该卡片设为可见）。
3. **启用“始终开启”功能**：在“更多”→“设置”→“始终开启”中，打开“自动启动 Surge”的开关，即可保持 Surge 4 一直后台开启。
4. **启动 Surge 4**：点击“首页”右上角“启动”按钮启动 Surge 4，即可在 iOS 端跨服登录安卓国服。（如无其他使用需求，不玩游戏时别忘了停止 Surge 4。）

##### 方法二：手动编辑配置

1. **手动添加跨服配置**：点击“首页”左上角配置名，在弹出的“配置列表”窗口中，点击“在文本模式中编辑”（或是使用任一款编辑器打开你的 Surge 配置文件（.conf）直接进行编辑）。在编辑窗口中，将以下配置中 `[Script]` 下方的代码，在配置文件中找到对应位置复制进去，然后点击右上角“完成”保存修改。

```
[Script]
# 少女前线 跨安卓官服
## 切换服务器
gfcn_ios2gw = type=http-request,pattern=^http:\/\/gfcn-transit\.ios\.sunborngame\.com\/index\.php,script-path=https://github.com/Mornwind/GFCN_SwitchServer/raw/master/Surge_4/gfcn_ios2gw.js,requires-body=1
```

2. **启用“脚本”功能**：回到“首页”中，将“脚本”卡片的开关打开（若未找到，则去“更多”→“外观”→“卡片”中将该卡片设为可见）。
3. **启用“始终开启”功能**：在“更多”→“设置”→“始终开启”中，打开“自动启动 Surge”的开关，即可保持 Surge 4 一直后台开启。
4. **启动 Surge 4**：点击“首页”右上角“启动”按钮启动 Surge 4，即可完成跨服。（如无其他使用需求，不玩游戏时别忘了停止 Surge 4。）

</details>

#### ⑹ Loon

<details>
<summary>点击查看：配置跨服</summary>

##### 方法一：直接使用插件功能（推荐）

1. **进入“插件”页面**：点击进入底栏中的“配置”界面，找到“插件”部分，点击进入。
2. **添加跨服插件**：在弹出的“插件”界面中，点击最上方的“添加”按钮（图标为加号⨁），进入“添加插件”界面；在“URL”中填入下方的 URL，在“别名”中填入“少女前线 跨安卓官服”，“PROXY”默认为空白不选（或选内置的“DIRECT”），然后点击右上角“保存”；然后返回至“配置”界面。

```
https://github.com/Mornwind/GFCN_SwitchServer/raw/master/Loon/gfcn_ios2gw.plugin
```

3. **启用“脚本”功能**：在“配置”界面中，找到“脚本”部分，打开右侧的开关启用功能；然后返回“仪表”界面 。
4. **启动 Loon**：点击”仪表“界面右上角的“启动“开关，然后在清除了游戏后台的情况下进入游戏，即可实现跨服。（如无其他使用需求，不玩游戏时别忘了停止 Loon。）

##### 方法二：手动写入当前使用中配置

1. **进入配置编辑界面**：点击下方的“配置”，然后翻到最下面“编辑”部分，点击“文本编辑”。
2. **添加跨服配置**：在弹出的编辑窗口中，将以下配置中 `[Script]` 下方的代码，在配置文件中找到对应位置复制进去，然后点击右上角的“完成”，然后返回“仪表”界面。

```
[Script]
# 少女前线 跨安卓官服
## 切换服务器
http-request ^http:\/\/gfcn-transit\.ios\.sunborngame\.com\/index\.php script-path=https://github.com/Mornwind/GFCN_SwitchServer/raw/master/Loon/gfcn_ios2gw.js, requires-body=true, tag=gfcn_ios2gw
```

3. **启用“脚本”功能**：在“仪表”界面中，找到“脚本”卡片，打开“脚本”功能的开关。（若未找到，点击功能卡片下方的“快捷方式”，将“脚本”卡片设置为可见即可）
4. **重启 Loon**：为确保修改生效，可以开关一次“仪表”界面右上角的“启动”开关，然后在清除了游戏后台的情况下进入游戏，即可实现跨服。（如无其他使用需求，不玩游戏时别忘了停止 Loon。）

</details>

### A-2 类型（未提供）
 > A-2：通过**使用他人提供的代理服务器**，**在远端重写客户端请求**，**直接**实现跨服。

暂不提供此方式为「少女前线」进行跨服，因为使用代理服务器会受多种因素影响，造成跨服不稳定。

### B 类型（未提供）
 > B-1：通过**对游戏客户端修改后重新打包**，**由他人统一签名后在线下载安装**，**直接**实现跨服。
 > 
 > B-2：通过**对游戏客户端修改后重新打包**，**自行签名然后越狱安装或侧载**，**直接**实现跨服。

不提供此方式为「少女前线」进行跨服，因为修改客户端容易被封号。

### C-1 类型
 > C-1：通过**使用云游戏平台**，**将游戏画面实时传输至移动设备**，**间接**实现跨服。

| 图标 | 跨服工具 | 别名 | 跨服教程<br/>与配置 |
| :-: | :-: | :-: | :-: |
| - | 网易云游戏 | - | 见网易云游戏官网 |

| 跨服工具 | 国区商店<br/>购买与下载 | 正规渠道价格 | 跨服操作<br/>方便程度 | 设备上同时<br/>挂梯与跨服 | 备注 |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 网易云游戏 | - | ¥15.9/月<br/>¥70/季<br/>¥240/年 | ★★★★★ | ✅ | 部分渠道服平台未提供 |

 > 注：
 > 
 > 网易云游戏 - 官网：<https://cg.163.com>

### C-2 类型
 > C-2：通过**使用云主机**，**将游戏画面实时传输至移动设备**，**间接**实现跨服。

此方法需自行摸索。

---

[返回前言](/README.md)
