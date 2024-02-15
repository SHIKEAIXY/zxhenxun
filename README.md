</div>
<div align="center">
<br>
    <img src="图片/真寻.png" width="80%">

</div>

## [点击此处查看真寻bot安装时报错的解决问题](https://gitee.com/SHIKEAIXY/zhenxun/blob/master/Installation%20issues.md)

还未完善...

# 前言

大家都知道一键脚本这个东西吧
- 没错真寻也有
- 但是不建议使用脚本，很容易出问题，出了还不好修
- 所以还是建议手动安装
- 你要是非用脚本也拦不住你对吧 [官方传送门](https://github.com/zhenxun-org/zhenxun_bot-deploy) [TRSS脚本传送门](https://trss.me/Install/Windows.html)

### 来下载2000张真寻图片吧~

既然是喜欢真寻的肯定也喜欢真寻的表情包/头像/壁纸吧

[点击此处获取高达2000张的超级可爱的真寻表情包吧！！！](https://gitee.com/SHIKEAIXY/zhenxun-wallpaper-picture)

## 聊天群QQ：778502891

## 部署问题找我（可能没时间看，但一定会回）QQ：1991682159

## 与真寻相关  

1. 有什么问题可以在本库提Issues或者加上方聊群询问

2. linux系统的教程请查看[linux分支](https://gitee.com/SHIKEAIXY/zhenxun/tree/linux)

3. [点击查看zhenxun_bot的介绍](https://github.com/HibiKier/zhenxun_bot/blob/main/README.md)

4. [点击查看zhenxun_bot的更新内容](https://github.com/HibiKier/zhenxun_bot/releases)

5. [点击查看zhenxun_bot使用说明](https://hibikier.github.io/zhenxun_bot/ )

## 介绍

1. 一个win系统的[zhenxun_bot](https://github.com/HibiKier/zhenxun_bot)安装教程

2. 需要有一定的基础 如果没有一些基础的话可会困难重重哒 为了自己喜欢的真寻加油鸭！

3. 真寻bot非常可爱 嗯 非常可爱！！！非常可爱！！！非常可爱！！！

4. 真寻bot是一个基于 [Nonebot2](https://github.com/nonebot/nonebot2) 和 [~~go-cqhttp~~](https://github.com/Mrs4s/go-cqhttp) 的开发，以 [postgresql](https://www.postgresql.org/) 作为数据库，非常可爱的绪山真寻bot

<a href='https://gitee.com/SHIKEAIXY/zhenxun/stargazers'><img src='https://gitee.com/SHIKEAIXY/zhenxun/badge/star.svg?theme=dark' alt='star的人'></img></a>
<a href='https://gitee.com/SHIKEAIXY/zhenxun/members'><img src='https://gitee.com/SHIKEAIXY/zhenxun/badge/fork.svg?theme=dark' alt='fork的人'></img></a>
[![](https://img.shields.io/badge/python-v3.8+-DeepSkyBlue)](https://www.python.org)
[![](https://img.shields.io/badge/poetry-brightgreen.svg)](https://python-poetry.org)
[![](https://img.shields.io/badge/nonebot-2.0.0-yellow)](https://nb2.baka.icu)
[![](https://img.shields.io/badge/go--cqhttp-1.0.0-red)](https://docs.go-cqhttp.org/)
[![](https://img.shields.io/badge/TRSS--Yunzai/Miao--Yunzai-ws--plugin-red)](https://gitee.com/xiaoye12123/ws-plugin)
[![](https://img.shields.io/badge/Gensokyo-QQAPI-red)](https://github.com/Hoshinonyaruko/Gensokyo)

# 正文啦！
# 一 准备工作

## 安装 版本大于3.8且小于3.11的python 与 poetry

### ①安装python

这里我推荐安装python3.10

[点击下载py3.10](https://yshs.lanzouy.com/iFMpG0gdwt9a)

下面两个对钩点上 然后点击Install Now等待安装完成
<br>
    <img src="图片/py安装.png" width="50%">

安装完成打开cmd输入py 查看是否有py版本输出

### ②安装poetry

1. 打开Powershell（需要管理员权限）运行

不会打开？不要慌 点击此处 [如何在Windows 10/11中打开PowerShell](https://www.51cto.com/article/696873.html)

打开后输入下面内容并回车（安装时间较长）

```
(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | python -
```

1.1 使用pip安装（此步骤无需进行2的变量环节）
```
python -m pip install -U pip
```
```
pip install poetry
```

2. 然后将`%APPDATA%\Python\Scripts`添加到PATH环境变量(位置在右键此电脑→属性→高级系统设置→环境变量)
<br>
    <img src="图片/变量.png" width="50%">

3. 打开cmd发送poetry查看是否有版本输出

如果没有请重启电脑 重新打开cmd输入 poetry

还不行？[点击此处解决](https://www.baidu.com)

# 二 安装postgresql

## ①下载postgresql数据库
[点击此处将下载Postgresql-15.1-1版本安装包](https://get.enterprisedb.com/postgresql/postgresql-15.1-1-windows-x64.exe)

不想要15.1版本的可以自行下载别的版本（目前只要是9.0以上的版本都可以）

## ②安装postgresql数据库

1.双击安装程序，点击Next（打不开报错？不要找我 我也不会）
<br>
    <img src="图片/安装数据库.png" width="50%">

2.选择安装路径（对路径没有要求不用改 默认c盘），继续Next

安装路径中不要出现中文！（防止报错）
<br>
    <img src="图片/数据库安装路径.png" width="50%">

3.去掉即可，不影响使用，Stack BuilderNext
<br>
    <img src="图片/取消Stack Builder安装.png" width="50%">

4.数据存储路径（对路径没有要求不用改 默认c盘），Next
<br>
    <img src="图片/数据存储路径.png" width="50%">

5.输入postgres用户的密码，例如：zhenxun（防止后期问题请按照本教程的密码输入 上下全部输入zhenxun）
<br>
    <img src="图片/数据库密码.png" width="50%">

6.默认端口，Next
<br>
    <img src="图片/数据库端口.png" width="50%">

7.接下来一路点Next直到进入安装
<br>
    <img src="图片/一路下一步.png" width="50%">

8.显示下面的图 代表你安装完成
<br>
    <img src="图片/数据库安装完成.png" width="50%">

## ③配置连接

1.找到安装的pgAdmin启动数据库 并启动

打开方法一： 在应用中搜索 pgAdmin 点击展开 找到下面图片显示的打开即可
<br>
    <img src="图片/启动数据库.png" width="80%">

[是英文怎么办？点击此处解决](https://blog.csdn.net/weixin_46329056/article/details/125929563?ydreferer=aHR0cHM6Ly93d3cuYmFpZHUuY29tL2xpbms%2FdXJsPUwzNmhIRml6RjMwd2QzWnFEanFpY0NLYzFGbmlGUktRTXhCU21UTmFObjZNM0NxLUY5YzJzYV9IY2kzekV5bEVlTTctNzZnWjVmNC15aTI3ZjE3V3JJVDRnUzMtejdlTHp6aFJPY1Y2Tm9XJndkPSZlcWlkPTgyNjY3OTdjMDAwZTA0NGEwMDAwMDAwMjY0M2FiNDZj)

2.新建连接

左侧栏右键点击后选择，在点击ServersRegister服务器
<br>
    <img src="图片/添加数据库.png" width="50%">

随便给它起一个响亮的名字（
<br>
    <img src="图片/真寻名字.png" width="50%">

填写配置，如果是连接远程服务器的话对应的服务器IP，本地的话可以直接填写 就是安装时配置的端口，没有修改的话默认

就是安装时配置
的密码主机名称/地址127.0.0.1端口5432 密码就是你安装是输入的密码（本教程前面用的是zhenxun）
<br>
    <img src="图片/编辑数据库1.png" width="50%">

 3.点击保存
左侧栏会出现一个可爱真寻
<br>
    <img src="图片/编辑数据库2.png" width="50%">

## ④新建数据库

1.点击展开

2.右击，选择后点击数据库创建数据库
<br>
    <img src="图片/新建数据库.png" width="50%">

3.直接创建

设置数据库名称后点击保存 
<br>
    <img src="图片/保存数据库.png" width="50%">

ok火速下一步

# 三 开始安装真寻本体

请安装Git，已有可跳过

[点击我进行下载Git](https://registry.npmmirror.com/-/binary/git-for-windows/v2.43.0-rc0.windows.1/Git-2.43.0-rc0-64-bit.exe)

1.github下载真寻本体

```
git clone --depth 1 https://github.com/HibiKier/zhenxun_bot
```

2.执行下面内容

```
poetry install
poetry shell
playwright install chromium
```

3.设置超级用户，打开 .env.dev 文件（在真寻根目录），在中添加自己大号（主人）的QQ号，123456789为QQ号

    SUPERUSERS=["123456789"]

4.打开 configs/config.py 填写数据库数据

```
-----------------------------------------------------------
-----------------------------------------------------------
 如果你听我的话了 密码和名字与我填的一样 且数据库也在该服务器上 
 可以直接复制以下配置 替换掉 configs/config.py 中的数据库数据
-----------------------------------------------------------
-----------------------------------------------------------

bind: str = ""  # 数据库连接链接
sql_name: str = "postgres"
user: str = "postgres"
password: str = "zhenxun"
address: str = "127.0.0.1"
port: str = "5432"
database: str = "zhenxun"

---------------------------------------------------------------
---------------------------------------------------------------
  -------------------如果没有听我的怎么办呢--------------------
  -----------------按照下面的格式进行修改即可------------------
---------------------------------------------------------------
---------------------------------------------------------------

# 数据库（必要）
# 如果填写了bind就不需要再填写后面的字段了
# 示例："bind": "postgres://user:password@127.0.0.1:5432/database"
bind: str = ""       #数据库连接链接
sql_name: str = "postgres"
user: str = ""       #数据用户名
password: str = ""   #数据库密码
address: str = ""    #数据库地址
port: str = ""       #数据库端口
database: str = ""   #数据库名称

```

5.启动真寻，会在 configs 和 data/configs 目录下生成各种配置文件

```
python bot.py
```

（如果你没有这些需求可以忽略这步，毕竟默认配置了）

6.打开 configs/config.yaml，里面包含的是各种插件的配置项，填写完毕后重启真寻Bot

# 四 连接zhenxun_bot

<details>
  <summary>使用go-cqhttp连接真寻bot（不建议）</summary>

## ①下载go-cqhttp 

### gitee下载

请安装Git，已有可跳过

[点击我进行下载Git](https://registry.npmmirror.com/-/binary/git-for-windows/v2.43.0-rc0.windows.1/Git-2.43.0-rc0-64-bit.exe)

```
git clone --depth 1 https://gitee.com/SHIKEAIXYY/1.1.9unidbg_and_gocq.git
```
### zip下载 (不建议!)

[点击此处下载签名和go-cqhttp](https://gitee.com/SHIKEAIXYY/1.1.9unidbg_and_gocq/repository/archive/master.zip)

下载后请配置`windows_amd64`而`unidbg-fetch-qsign-1.1.9`一会要用

## ②配置go-cqhttp

1.打开config.yml文件，修改`QQ账号和密码`保存即可（先不要重新启动！！！）
<br>
    <img src="图片/账号.png" width="70%">

# 部署签名api

### ①下载java 

1.[点击此处下载jdk](https://mirrors.tuna.tsinghua.edu.cn/Adoptium/17/jdk/x64/windows/OpenJDK17U-jdk_x64_windows_hotspot_17.0.9_9.msi)

2.安装完成后打开cmd运行`java`查看是否有输出

[如果没有输出点击此处查看如何配置变量，如果你看不懂那就没办法了](https://blog.csdn.net/qq_41436122/article/details/82620080)

配置完成后重新启动服务器后再打开cmd运行`java`查看是否有输出

### ②使用

1.打开`1.1.9unidbg_and_gocq\unidbg-fetch-qsign-1.1.9`双击运行`一键启动.bat` (就[下载go-cqhttp](https://gitee.com/SHIKEAIXY/zhenxun/blob/master/README.md#%E4%B8%8B%E8%BD%BDgo-cqhttp)下载的那个文件里面)

没有闪退即可使用（默认使用8.9.78版本）

2.签名启动成功后再重新启动 go-cqhttp.bat 登录即可

3.切记api不要关闭！！！

### ③配置

1.端口默认是`520`

2.key默认为`1314`

3.如需修改可打开`unidbg-fetch-qsign-1.1.9\txlib`找到你要修改的版本打开这个文件如修改`8.9.71`则打开`8.9.71\config.json`进行修改并修改gocq的配置文件
<br>
    <img src="图片/签名配置端口key.png" width="50%">

### ④启动 go-cqhttp

1.返回上一目录打开`windows_amd64`文件

2.双击 `go-cqhttp.bat` 进行验证即可
<br>
    <img src="图片/gocq_bat.png" width="50%">

3.如果出现以下内容则不用管它，不影响登录和使用 **（如果你看着变扭请看下一条）** 

```
[WARNING]: Callback error: Packet timed out, Or response data is empty
[ERROR]: Protocol -> parse incoming packet error: return code unsuccessful: -10005
```

4.在gocq运行的页面中使用`ctrl+c`后输入下方内容回车重新启动即可
```
go-cqhttp
```

5.自动提交滑块ticket无反应
- 这个不知道有没有解决办法
- 如果没反应请使用`2. 手动抓取提交`
- [使用安卓手机点击此处下载](https://maupdate.rainchan.win/txcaptcha.apk)

### ⑤关于其他签名协议登录

1.现在个个版本都不稳定，看你63版本到最新版本哪个能登了

2.换登录版本教程在`go-cqhttp_windows_amd64\data\versions\修改版本.md`中

### 如果你使用了gocq还登录上就别~~作~~让他好好run

</details>

---

<details>
  <summary>使用[云崽]的[ws插件]跳过gocq使用icqq连接真寻bot（在2024年2月5号的晚上7点ICQQ删库...建议各位早日使用Gensokyo）</summary>

## 安装云崽

### ①安装前置

1. 请安装Git，已有可跳过

[点击我进行下载Git](https://registry.npmmirror.com/-/binary/git-for-windows/v2.43.0-rc0.windows.1/Git-2.43.0-rc0-64-bit.exe)

2. 下载node.js

[点击此处下载node.js](https://npmmirror.com/mirrors/node/v18.18.0/node-v18.18.0-x64.msi)

3. 右键鼠标打开`Open Git Bash here`

win11需先点击显示更多选项后才显示`Open Git Bash here`
<br>
    <img src="图片/win11打开git.png" width="40%">
<br>
    <img src="图片/win打开git2.png" width="40%">
 
然后运行下方命令
```
bash <(curl -L https://gitee.com/SHIKEAIXY/zhenxun/raw/master/Yunzai.sh)
```

<details>
  <summary>如果不想使用sh一键下载可点击此处手动下载</summary>

&nbsp;2.1. 在cmd依次输入以下内容并回车 

```
git clone --depth=1 https://gitee.com/yoimiya-kokomi/Miao-Yunzai.git ./Yunzai/Miao-Yunzai/
```
```
cd Yunzai/Miao-Yunzai
```
```
git clone --depth=1 https://gitee.com/yoimiya-kokomi/miao-plugin.git ./plugins/miao-plugin/
```
```
npm --registry=https://registry.npmmirror.com install pnpm -g
```
```
//可选
pnpm config set registry https://registry.npmmirror.com
```
```
pnpm install -P
```
```
git clone --depth=1 https://gitee.com/xiaoye12123/ws-plugin.git ./plugins/ws-plugin/
```
```
pnpm install --filter=ws-plugin
```
```
cd ..
```
```
git clone --depth 1 -b redis https://gitee.com/SHIKEAIXYY/Trss-ComWeChat-Yunzai.git ./redis
```
```
git clone --depth 1 https://gitee.com/touchscale/Qsign.git ./Qsign
```
</details>
&nbsp;

4. 下载jdk

[点击此处下载jdk](https://mirrors.tuna.tsinghua.edu.cn/Adoptium/17/jdk/x64/windows/OpenJDK17U-jdk_x64_windows_hotspot_17.0.9_9.msi)

#### ②说明

1. 安装完的`云崽`和`数据库`在你bat运行的同级目录`Yunzai`的文件夹中

2. `redis`为数据库

3. `Miao-Yunzai`为机器人本体

4. `Qsign`为签名api

### ③启动云崽

1. 请打开`Yunzai`文件夹

2. 运行`redis`数据库（运行`redis/双击我启动redis.bat`即可）

3. 运行`Qsign`（运行`Qsign/一键startAPI.bat`即可）默认是80的签名，端口为801，秘钥为114514

4. 启动机器人并配置

在`Miao-Yunzai`目录下cmd输入`node app`即可

#### ④机器人配置

1. 请输入机器人QQ号(建议用小号)：`这里输入机器人的QQ号即可`

2. 请输入登录密码(为空则扫码登录)：`这里输入机器人的QQ密码即可`

3. 请选择登录端口：`这里请通过方向键选择aPad！！！`（下面的图片选错了别跟着图片走！！！）

4. 请输入主人QQ号：`这里输入用来管理机器人的QQ号即可`

5. 请输入签名API地址（可留空）：`这里输入下方内容即可`

```
http://127.0.0.1:801/sign?key=114514
```
<br>
    <img src="图片/机器人配置.png" width="50%">

5. 触发滑动验证，需要获取ticket通过验证，请选择获取方式:`这里选择 0.自动获取ticket 进行扫码即可`

6. 查看云崽bot是否正常运行，如运行成功请关掉云崽重新输入`node app`并回车启动机器人

7. 连接本地bot(给云崽机器人QQ发送)

```
#ws添加连接
``` 
```
zhenxun_bot,1
``` 
```
ws://127.0.0.1:8080/onebot/v11/ws/
``` 
8. 发送`#ws查看连接`来查看是否连接成功

出现带以下内容的图片，则代表连接成功
```
连接名字: zhenxun_bot
连接类型: 1
当前状态: 已连接
```
### 注意不要关闭云崽和真寻本体

如果连接失败大概率就是你关了真寻或者真寻启动失败了

</details>

---

<details>
  <summary>使用Gensokyo(QQBot)连接真寻bot</summary>

# 没必要评价第三方好还是官方好，各有各的好处和弊端，能接受就用，接受不了就别用，别一天天的骂来骂去，~~你就算骂也别骂到人家开发者上去，咱能不能有点良心？~~ 
# 别拿着建议的理由去骂开发者，人家更不更新跟你什么关系，没强迫你更新吧？你要是认为Gensokyo更新太快就别用，把开发者气跑了你就开心高兴了？

### ①说明：

1. 新框架`Gensokyo` 视频：https://www.bilibili.com/video/BV1Aw411K7Z5

2. `Gensokyo`仓库：https://github.com/Hoshinonyaruko/Gensokyo

3. `Gensokyo`gitee镜像：https://gitee.com/sanaefox/Gensokyo

4. `Gensokyo`教程 https://www.bilibili.com/read/cv27523883

5. `Gensokyo`的`web端`用户名和密码已全部修改为`zhenxun`

6. `Gensokyo` QQ群：196173384

### ②注册企业账号

1. 随随便便注册一个企业qq开放平台账号：https://q.qq.com
<br>
    <img src="图片/企业注册.png" width="50%">

2. 登录企业qq开放平台账号并创建机器人
<br>
    <img src="图片/创建机器人.png" width="50%">

3. 填好信息后点击下一步

4. 打开后点击`基础信息-信息`
<br>
    <img src="图片/资质认证.png" width="50%">

5. 点击`详情`
<br>
    <img src="图片/资质认证2.png" width="50%">

6. 点击`进入认证`后填写相关信息并点击提交审核进行认证（目前不认证无法上线机器人，可沙箱使用）
<br>
    <img src="图片/资质认证3.png" width="50%">

### ④下载配置Gensokyo

1.下载gensokyo-windows-amd64（取用v325，更新时间2024.2.14）若发现教程的Gensokyo版本更新，可以选择无视更新
```
git clone --depth 1 -b gensokyo-windows-amd64 https://gitee.com/SHIKEAIXY/zhenxun.git ./Gensokyo
```

2. 打开下载的`Gensokyo`后并双击打开`config.yml`

3. 打开之前的网站`q.qq.com`点击`开发-开发设置`并复制`QQ号 ID 令牌 秘钥`填写到`config.yml配置文件`的7~9行
<br>
    <img src="图片/配置Gensokyo2.png" width="50%">
<br>
    <img src="图片/配置Gensokyo.png" width="50%">

4. 将自己服务器的公网ip填入`server_dir`
<br>
    <img src="图片/配置Gensokyo3.png" width="50%">

5. 并开放端口号`15630`（不配置将无法发送图片）

打开防火墙(不会可以`按住win键+R键`输入`Firewall.cpl`并点击确定)
<br>
    <img src="图片/防火墙.png" width="50%">

打开防火墙后点击`高级设置`
<br>
    <img src="图片/防火墙2.png" width="50%">

然后点击`入站规则`并`新建规则`
<br>
    <img src="图片/防火墙3.png" width="50%">

选择端口后下一页
<br>
    <img src="图片/防火墙4.png" width="50%">

然后填写端口`15630`并下一页
<br>
    <img src="图片/防火墙5.png" width="50%">

然后一直下一页即可，名字随便起

6. 如果你没有公网ip可使用早苗的图床

将`server_dir`和`port`修改为下方内容

```
server_dir: "sanae.online"
port: "443" 
``` 
然后将`lotus`的`false`设置为`true`后保存即可使用
<br>
    <img src="图片/gsk图床.png" width="50%">

7. 以上完成后双击运行`gensokyo.bat`不出意外就可以运行了

### ⑤配置沙箱使用机器人

1. 打开QQ点击新创建聊群（不超过20人的群）

2. 再次回到网站`q.qq.com`

3. 点击`开发-沙箱配置`后找到`在QQ群配置`将聊群修改为刚刚创建的聊群（如果失败就几秒后再试试）
<br>
    <img src="图片/机器人沙箱.png" width="50%">

4. 接下来回到QQ打开刚刚创建的聊群，点击右上角的`三个横杠`，点击`管理群-群机器人`，找到你的机器人点击添加

5. 接下来@机器人并发送真寻帮助查看是否可以发图  如：@冰祈 真寻帮助
6. 如果不行自己查看上文中让填写的ip是否为公网ip并且开放了端口号，如都设置了还不行那就找作者去，我不到啊

**注意！！！**
 
 `zhenxun_bot`与`Gensokyo`需全部运行，不可关闭

</details>

---

# 五 重新启动真寻

关机/页面关上了该怎么重新启动真寻？

1. 打开真寻根目录cmd运行

```
poetry shell
```
```
python bot.py
```
#### 启动命令说明
- poetry shell 这个是进入虚拟环境
- python bot.py 这个是用python来运行bot.py这个文件

# 六 真寻插件下载
 
[插件安装问题](https://github.com/zhenxun-org/nonebot_plugins_zhenxun_bot/issues/27)

[真寻索引库](https://github.com/zhenxun-org/nonebot_plugins_zhenxun_bot)

[nb商店（不是全部都谦融）](https://nonebot.dev/store/plugins)

---

## 插件的下载方法

1. 方法一：手动拉取

在zhenxun_bot/plugins中cmd运行

简单说明：git clone为拉取，--depth 1为最近一次提交，使用该命令可加快下载速度
```
git clone --depth 1 + 仓库地址
```

---

2. 方法二：指令下载

请给你的真寻机器人发送`查看插件仓库`查看

发送完成后可发送`安装插件+序号`如：安装插件2 进行下载即可

如需卸载发送`卸载插件+序号`即可

---

下载时长会和你的网络与仓库大小有关系 