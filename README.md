* 感谢本地温迪 QQ 2378518248

脚本教程看完变大牛

此文章为中文

请不要使用翻译

翻译会导致文章的符号变为中文!!!

有问题请发邮箱397510573@qq.com
#

# 脚本制作教程
> [前言](#前言)
>
> 脚本如何制作
> > [打开控制台](#脚本制作教程打开控制台)
> > 
> > [脚本制作教程(基础)](#脚本制作教程基础)
> >
> > [脚本制作教程(中等)](#脚本制作教程中等)
> > 
> > [脚本制作教程(UI)](#脚本制作教程UI)
> 
> [脚本如何加密](#脚本如何加密)

#

### 前言
* 1.在你的设备上安装lua 编辑器 为了方便更好的了解lua这门语言 只观看不实践 永远没效果
* 2.学习lua需确保语法正确
* 3.做脚本可能会遇到开户等行为我们要抵止这种行为
* 4.此文章只供交流使用
#

### 脚本制作教程(打开控制台)
> 打开控制台
> > 手机版
> > > 在聊天框输入"/console"
> > > 
> > > 执行此代码
> > > game:GetService("VirtualInputManager"):SendKeyEvent(true, "F9", false, game)
> > 
> > 电脑版
> >
> > > 按键盘的"F9"
> > >
> > > 如上面的无效，请按键盘的"Shift + F9"

#

### 脚本制作教程(基础)
> [基础](#基础)
>
> [函数](#函数)

#### 基础
* 此区块中大部分()里的""(双引号)可以换成''(单引号)
```lua
loadstring()
-- loadstring的作用是"加载脚本"

game:HttpGet("URL")
-- game:HttpGet的作用是"从("URL")中请求内容"
-- URL为需请求的链接

loadstring(game:HttpGet("URL"))
-- 上面两个的结合体
-- 最常用的
-- loadstring(game:HttpGet("URL"))的作用是"加载脚本(从("URL")中请求内容)"

print("输出")
-- print的作用是"输出"("")中的内容在控制台

warn("警告")
-- warn的作用是"警告"("")中的内容在控制台
-- 但字体是黄色的
-- 不影响脚本运行

error("错误")
-- error的作用是"提出错误"("")中的内容在控制台
-- 但字体是红色的
-- 影响脚本运行

setclipboard("设置剪切板")
-- setclipboard的作用是"设置剪切板"("")中的内容在剪切板里
-- 可以把任意内容设置于剪切板
```
> > > 基础函数
> > 
> > game后面可以使用两种方式链接
> > 
> > 1.使用"game."
> > 
> > 2.使用"game:GetService("")"
> > 
> > 我更推荐第2种
> 
> > > 传送功能
> > 
> > game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0, 0, 0)
> > 
> > 似乎看起来,特别混乱,让我们来拆分一下
> > 
> > game是游戏
> > 
> > players是玩家
> > 
> > LocalPlayer是本地玩家,就是使用脚本的人
> > 
> > Character如果你用翻译器翻译,会翻译出来字符
> > 
> > HumanoidRootPart是玩家的身体
> > 
> > CFrame是位置(坐标)
> > 
> > =是设置变量为右边的
> > 
> > CFrame.new是一个类型，对应的就是CFrame
> > 
> > 后面的(0, 0, 0)就是位置
> > 
> > 可以用以下代码复制玩家当前位置到剪切板
> > setclipboard(tostring(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame))
> >
> > 但是上面不是唯一的传送方式
> >
> > 传送方式第二种
> >
> > Position是第二种传送方式
> >
> > 精度没有CFrame高
> >  
> > game:GetService("Players").LocalPlayer.Character:MoveTo(Vector3.new(0, 0, 0))
> >
> > game是游戏
> > 
> > players是玩家
> > 
> > LocalPlayer是本地玩家,就是使用脚本的人
> >
> > Character如果你用翻译器翻译,会翻译出来字符
> >
> > MoveTo移动到...
> >
> > Vector3.new是一个类型,很常用，修改size也是这个类型
> >
> > 后面的(0, 0, 0)就是位置
> >
> > 可以用以下代码复制玩家当前位置到剪切板
> > setclipboard('game:GetService("Players").LocalPlayer.Character:MoveTo(Vector3.new('..tostring(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position)..'))')

#### 函数

```lua
game:GetService("Players").LocalPlayer.AccountAge
-- 账号注册时间(天)
idenifyexecutor()
-- 你的注入器名字
game:GetService("Players").LocalPlayer.Character.Name
game:GetService("Players").LocalPlayer.Name
-- 注册时的名称
game:GetService("Players").LocalPlayer.DisplayName
-- 昵称可以变的
game.PlaceId
-- 服务器ID
game:GetService("MarketplaceService"):GetProductInfo(game.PlaceId).Name
-- 服务器名字
game:GetService("Players").LocalPlayer.UserId
game:GetService("Players").LocalPlayer.CharacterAppearanceId
-- 用户ID，注册时分配的，不可变
game:GetService("RbxAnalyticsService"):GetClientd()
-- 客户端ID，删除再下载游戏就会变
game:GetService("HttpService"):GetUserAgent()
-- UA,Roblox请求外部网站时用的
game:GetService("HttpService"):JSONDecode()
-- 转json为lua表
game:GetService("HttpService"):JSONEncode()
-- 转lua表为json

```
* 感谢本地温迪
* QQ 2378518248
```lua
打印 Code = "print"
局部:设", replace = "local "
为 Code = "="
局部:方法", replace = "local function "
方法 Code = "function"
方法执行", replace = "function()"
返回 Code = "return "
结束}", replace = "end "
加", replace = "+"
减", replace = "-"
真的", replace = "true"
假的", replace = "false"
乘", replace = "*"
除", replace = "/"
等于", replace = "=="
不等于", replace = "~="
大于", replace = ">"
小于", replace = "<"
大于等于", replace = ">="
小于等于", replace = "<="
且", replace = "and "
或", replace = "or "
不是", replace = "not "
如果", replace = "if "
那么", replace = " then "
其他 Code = "else "
别的如果", replace = "elseif "
停止", replace = "break "
对于", replace = "for "
在 Code = "in "
当", replace = "while "
就执行{", replace = "do "
等待", replace = "task.wait() "
继续", replace = "continue "
转化数字 Code = "tonumber"
转换字符 Code = "tostring"
类型 Code = "type"
抛出错误 Code = "error"
判断是否抛出错误 Code = "assert"
远程事件 Code = "game:GetService('ReplicatedStorage')."
获取子级 Code = "GetChildren()"
列表:插入 Code = "table.insert"
列表:移除 Code = "table.remove"
列表:元素连接 Code = "table.concat"
列表:制成表 Code = "table.pack"
列表:分解表 Code = "table.unpack"
字符:子字符串 Code = "string.sub"
字符:长度 Code = "string.len"
字符:全改小写 Code = "string.lower"
字符:全改大写 Code = "string.upper"
字符:格式字符 Code = "string.format"
字符寻找字符 Code = "string.match"
字符:更替字符 Code = "string.gsub"
数学:绝对值 Code = "math.abs"
数学:大数取整 Code = "math.ceil"
数学:小数取整 Code = "math.floor"
数学:取最大返回 Code = "math.max"
数学:取最小返回 Code = "math.min"
数学:随机数 Code = "math.random"
数学:平方根 Code = "math.sqrt"
创建协程 Code = "coroutine.create"
恢复协程 Code = "coroutine.resume"
挂起协程 Code = "coroutine.yield"
当前时间 Code = "os.time"
当前日期 Code = "os.date"
重复 Code = "repeat "
直到 Code = "until "
全局 Code = ""
模块 Code = "require"
定义类 Code = "class '"
类结束", replace = "' end"
继承 Code = ":extend"
初始化 Code = "__init"
静态 Code = "static"
只读 Code = "readonly"
属性 Code = "property"
方法 Code = "method"
调用", replace = "()"
构造器 Code = "__newindex"
元表 Code = "metatable"
设置元表 Code = "setmetatable"
获取元表 Code = "getmetatable"
索引 Code = "__index"
新索引 Code = "__newindex"
连接 Code = ".."
长度", replace = "#"
文件打开 Code = "io.open"
文件关闭 Code = "io.close"
文件读取 Code = "io.read"
文件写入 Code = "io.write"    
环境 Code = "_G"
加载 Code = "load"
加载字符串 Code = "loadstring"
执行 Code = "pcall"
断言 Code = "assert"
错误处理 Code = "xpcall"
延迟调用 Code = "defer"
线程 Code = "thread"
新建线程 Code = "coroutine.create"
启动线程 Code = "coroutine.resume"
挂起线程 Code = "coroutine.yield"
克隆 Code = "clone"
销毁 Code = "destroy"
父对象 Code = ".Parent"
子对象 Code = ".Children"
实例 Code = "Instance"
新建实例 Code = "Instance.new"
游戏服务 Code = "game:GetService"
工作空间 Code = "workspace"
玩家 Code = "Players"
服务器 Code = "ServerScriptService"
客户端 Code = "StarterPlayer"
资源存储 Code = "ReplicatedStorage"
光照 Code = "Lighting"
声音 Code = "SoundService"
网络 Code = "NetworkServer"
聊天 Code = "Chat"
物理 Code = "PhysicsService"
数据存储 Code = "DataStoreService"
市场 Code = "MarketplaceService"
用户输入 Code = "UserInputService"
分析 Code = "AnalyticsService"
数据 Code = "game"
等待 Code = "wait"
任务等待 Code = "task.wait"
服务 Code = "Service"
事件 Code = "Event"
信号 Code = "Signal"
连接 Code = "Connect"
触发 Code = "Fire"
断开 Code = "Disconnect"
等待完成 Code = "Wait"
绑定到渲染步 Code = "BindToRenderStep"
取消绑定 Code = "UnbindFromRenderStep"
绑定到帧 Code = "BindToFrame"
取消帧绑定 Code = "UnbindFromFrame"
绑定到输入 Code = "BindToInput"
取消输入绑定 Code = "UnbindFromInput"
绑定到用户动作 Code = "BindToUserAction"
取消用户动作绑定 Code = "UnbindFromUserAction"
绑定到远程事件 Code = "OnClientEvent"
触发远程事件 Code = "FireServer"
绑定到远程过程调用 Code = "OnClientInvoke"
触发远程过程调用 Code = "InvokeServer"
绑定到属性改变 Code = "Changed"
绑定到销毁 Code = "Destroying"
绑定到子对象添加 Code = "ChildAdded"
绑定到子对象移除 Code = "ChildRemoved"
绑定到父对象改变 Code = "ParentChanged"
绑定到点击 Code = "MouseButton1Click"
绑定到拖动开始 Code = "DragBegin"
绑定到拖动结束 Code = "DragEnd"
绑定到鼠标进入 Code = "MouseEnter"
绑定到鼠标离开 Code = "MouseLeave"
绑定到鼠标移动 Code = "MouseMove"
绑定到触摸开始 Code = "TouchStarted"
绑定到触摸结束 Code = "TouchEnded"
绑定到触摸移动 Code = "TouchMoved"
绑定到输入开始 Code = "InputBegan"
绑定到输入结束 Code = "InputEnded"
绑定到键盘按下 Code = "KeyPress"
绑定到键盘释放 Code = "KeyRelease"
绑定到文本输入 Code = "TextInput"
绑定到文本更改 Code = "TextChanged"
绑定到滑动开始 Code = "ScrollBegin"
绑定到滑动结束 Code = "ScrollEnd"
绑定到滑动移动 Code = "ScrollMove"
绑定到游戏加载 Code = "GameLoaded"
绑定到游戏保存 Code = "GameSaving"
绑定到游戏关闭 Code = "GameClosing"
绑定到玩家加入 Code = "PlayerAdded"
绑定到玩家移除 Code = "PlayerRemoving"
绑定到玩家重生 Code = "PlayerRespawning"
绑定到玩家重生完成 Code = "PlayerRespawned"
绑定到角色添加 Code = "CharacterAdded"
绑定到角色移除 Code = "CharacterRemoving"
绑定到角色重生 Code = "CharacterRespawning"
绑定到角色重生完成 Code = "CharacterRespawned"
绑定到角色身体部分添加 Code = "BodyPartAdded"
绑定到角色身体部分移除 Code = "BodyPartRemoved"
绑定到角色身体部分改变 Code = "BodyPartChanged"
绑定到角色身体部分碰撞 Code = "BodyPartTouched"
绑定到角色身体部分不再碰撞 Code = "BodyPartUntouched"
绑定到角色身体部分接触 Code = "BodyPartContact"
绑定到角色身体部分接触结束 Code = "BodyPartContactEnd"
绑定到角色身体部分接触开始 Code = "BodyPartContactStart"
绑定到角色身体部分接触移动 Code = "BodyPartContactMove"
绑定到角色身体部分接触更新 Code = "BodyPartContactUpdate"
绑定到角色身体部分接触状态改变 Code = "BodyPartContactStateChanged"
绑定到角色身体部分接触状态开始 Code = "BodyPartContactStateStart"
绑定到角色身体部分接触状态结束 Code = "BodyPartContactStateEnd"
绑定到角色身体部分接触状态更新 Code = "BodyPartContactStateUpdate"
绑定到远程事件 Code = "OnClientEvent"
触发远程事件 Code = "FireServer"
绑定到远程过程调用 Code = "OnClientInvoke"
触发远程过程调用 Code = "InvokeServer"
绑定到属性改变 Code = "Changed"
绑定到销毁 Code = "Destroying"
绑定到子对象添加 Code = "ChildAdded"
绑定到子对象移除 Code = "ChildRemoved"
绑定到父对象改变 Code = "ParentChanged"
绑定到点击 Code = "MouseButton1Click"
绑定到拖动开始 Code = "DragBegin"
绑定到拖动结束 Code = "DragEnd"
绑定到鼠标进入 Code = "MouseEnter"
绑定到鼠标离开 Code = "MouseLeave"
绑定到鼠标移动 Code = "MouseMove"
绑定到触摸开始 Code = "TouchStarted"
绑定到触摸结束 Code = "TouchEnded"
绑定到触摸移动 Code = "TouchMoved"
绑定到输入开始 Code = "InputBegan"
绑定到输入结束 Code = "InputEnded"
绑定到键盘按下 Code = "KeyPress"
绑定到键盘释放 Code = "KeyRelease"
绑定到文本输入 Code = "TextInput"
绑定到文本更改 Code = "TextChanged"
绑定到滑动开始 Code = "ScrollBegin"
绑定到滑动结束 Code = "ScrollEnd"
绑定到滑动移动 Code = "ScrollMove"
绑定到游戏加载 Code = "GameLoaded"
绑定到游戏保存 Code = "GameSaving"
绑定到游戏关闭 Code = "GameClosing"
绑定到玩家加入 Code = "PlayerAdded"
绑定到玩家移除 Code = "PlayerRemoving"
绑定到玩家重生 Code = "PlayerRespawning"
绑定到玩家重生完成 Code = "PlayerRespawned"
绑定到角色添加 Code = "CharacterAdded"
绑定到角色移除 Code = "CharacterRemoving"
绑定到角色重生 Code = "CharacterRespawning"
绑定到角色重生完成 Code = "CharacterRespawned"
绑定到角色身体部分添加 Code = "BodyPartAdded"
绑定到角色身体部分移除 Code = "BodyPartRemoved"
绑定到角色身体部分改变 Code = "BodyPartChanged"
绑定到角色身体部分碰撞 Code = "BodyPartTouched"
绑定到角色身体部分不再碰撞 Code = "BodyPartUntouched"
绑定到角色身体部分接触 Code = "BodyPartContact"
绑定到角色身体部分接触结束 Code = "BodyPartContactEnd"
绑定到角色身体部分接触开始 Code = "BodyPartContactStart"
绑定到角色身体部分接触移动 Code = "BodyPartContactMove"
绑定到角色身体部分接触更新 Code = "BodyPartContactUpdate"
绑定到角色身体部分接触状态改变 Code = "BodyPartContactStateChanged"
绑定到角色身体部分接触状态开始 Code = "BodyPartContactStateStart"
绑定到角色身体部分接触状态结束 Code = "BodyPartContactStateEnd"
绑定到角色身体部分接触状态更新 Code = "BodyPartContactStateUpdate"
```

#

### 脚本制作教程(中等)
> [上传图片ID](#上传图片ID)
> 
> [文件操作](#文件操作)
>
> [Spy教程](#Spy)
>
> [Dex教程](#Dex)


#### 上传图片ID
* [Roblox创作中心 贴花](https://create.roblox.com/dashboard/creations?activeTab=Decal)
* https://create.roblox.com/dashboard/creations?activeTab=Decal
* 点击这个上传图片 ![图片](https://raw.githubusercontent.com/renlua/Script-Tutorial/refs/heads/main/QQ20250119-191659.png)


#### 文件操作
* 修改文件代码
* 此分区的所有操作为在"Workspace"文件夹中，无法读取个人信息
```lua
readfile("文件路径")
-- readfile的做用是"读取文件"("")中的内容为文件路径
-- 没文件夹的直接加文件名字
-- 有文件夹的加"./文件夹名"
-- 如readfile("文件名.txt")
-- 如readfile("./文件夹名/文件名.txt")

-- syn文档:
-- <string> readfile(<string> path)
-- Reads the contents of the file located at and returns it. If the file does not exist, it errors.path

writefile("文件路径", "文件内容")
-- 不可使用的扩展名：.exe、.scr、.bat、.com、.csh、.msi、.vb、.vbs、.vbe、.ws、.wsf、.wsh、.ps1、.psy
-- writefile的做用是"写入文件"("", "")中的第一项为文件路径，第二项为需写入文件的内容
-- 文件不存在自动创建
-- 没文件夹的直接加文件名字
-- 有文件夹的加"./文件夹名"
-- 如writefile("文件名.txt", "test")
-- 如writefile("./文件夹名/文件名.txt", "test")

-- syn文档:
-- <void> writefile(<string> filepath, <string> contents)
-- Writes to the supplied .contentsfilepath
-- Extensions that are not allowed: .exe, .scr, .bat, .com, .csh, .msi, .vb, .vbs, .vbe, .ws, .wsf, .wsh, .ps1, .psy.

appendfile("文件路径", "文件内容")
-- appendfile的做用是"追加写入文件"("", "")中的第一项为文件路径，第二项为需追加写入文件的内容
-- 没文件夹的直接加文件名字
-- 有文件夹的加"./文件夹名"
-- 如appendfile("文件名.txt", "test")
-- 如appendfile("./文件夹名/文件名.txt", "test")

-- syn文档:
-- <void> writefile(<string> filepath, <string> contents)
-- Appends to the file contents at . If the file does not exist, it errors.content path

loadfile("文件路径")
-- loadfile的做用是"加载文件中的脚本"("")中的第一项为文件路径
-- 没文件夹的直接加文件名字
-- 有文件夹的加"./文件夹名"
-- 如loadfile("文件名.txt")
-- 如loadfile("./文件夹名/文件名.txt")

-- syn文档:
-- <function> loadfile(<string> path)
-- Loads in the contents of a file as a chunk and returns it if compilation is successful. Otherwise, if an error has occured during compilation, nil followed by the error message will be returned.

listfiles("路径")
-- listfiles的做用是"列出路径中的所有文件"("")中的第一项为路径
-- 没文件夹的直接加"./"
-- 有文件夹的加"./文件夹名"
-- 如loadfile("./")
-- 如loadfile("./文件夹名/文件名.txt")

-- syn文档:
-- <table> listfiles(<string> folder)
-- Returns a table of files in .folder

isfile("文件路径")
-- isfile的做用是"判断路径是否为文件"("")中的第一项为文件路径
-- 是文件返回true,不是文件返回false
-- 没文件夹的直接加文件名
-- 有文件夹的加"./文件夹名"
-- 如isfile("文件名.txt")
-- 如isfile("./文件夹名/文件名.txt")

-- syn文档:
-- <bool> isfile(<string> path)
-- Returns if is a file or not.path

isfolder("文件夹路径")
-- isfolder的做用是"判断路径是否为文件夹"("")中的第一项为文件夹路径
-- 是文件夹返回true,不是文件夹返回false
-- 没文件夹的直接加文件夹名
-- 有文件夹的加"./文件夹名"
-- 如isfolder("文件夹名")
-- 如isfolder("./文件夹名/文件夹名")

-- syn文档:
-- <bool> isfolder(<string> path)
-- Returns if is a folder or not.path

makefolder("文件夹路径")
-- makefolder的做用是"新建文件夹"("")中的第一项为文件夹路径
-- 没文件夹的直接加文件夹名
-- 有文件夹的加"./文件夹名"
-- 如makefolder("文件夹名")
-- 如makefolder("./文件夹名/文件夹名")

-- syn文档:
-- <void> makefolder(<string> filepath)
-- Creates a new folder at .filepath

delfolder("文件夹路径")
-- delfolder的做用是"删除文件夹"("")中的第一项为文件夹路径
-- 没文件夹的直接加文件夹名
-- 有文件夹的加"./文件夹名"
-- 如delfolder("文件夹名")
-- 如delfolder("./文件夹名/文件夹名")

-- syn文档:
-- <void> delfolder(<string> path)
-- Deletes the folder in the supplied , if no folder exist errors.path

delfile("文件路径")
-- delfile的做用是"删除文件"("")中的第一项为文件路径
-- 没文件夹的直接加文件夹名
-- 有文件夹的加"./文件夹名"
-- 如delfile("文件名")
-- 如delfile("./文件夹名/文件名")

-- syn文档:
-- <void> delfile(<string> path)
-- Deletes the file in the supplied , if no file exist errors.path

```

#### Spy
* 这是Spy代码，可以用来做脚本
```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/renlua/Script-Tutorial/refs/heads/main/Spy.lua"))
```

#

### 脚本制作教程(UI)
* 制作脚本需要有一个UI 如:WareUI
* WareUI模板:
```lua
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/renlua/Script-Tutorial/refs/heads/main/WareUI.lua"))()
-- 脚本的UI(WareUI)

local window = library:new("脚本名字")
-- 你的脚本名字

local Tab = window:Tab("标签")
-- 左边的标签

local section = Tab:section("分区",true)
 -- true为默认打开，false为默认关闭

section:Textbox("文本框", "", "请输入", function(Value)
    print(Value)
end)
-- 输入文本 Value为输入的内容

section:Button("按钮", function()
    print("Button")
end)
-- 一个按钮点击执行里面的内容

section:Toggle("开关", "", false, function(Value)
    print(Value)
end)
-- 一个开关false为默认关闭，true默认打开，Value为返回值

section:Dropdown("下拉条", '', {"0","1","2","3","4","5","6","7","8","9"}, function(s)
    print(s)
end)
-- 一个下拉条，'{"0","1","2","3","4","5","6","7","8","9"}'为下拉的内容
-- Value为返回值为选择了什么

section:Keybind("键位绑定", Enum.KeyCode.LeftControl, function()
    OpenMain()
end)
-- 一个快捷键，用于电脑，作用为打开或关闭UI

section:Slider("拉条", "", 1, 1, 100, false, function(Value)
    print(Value)
end)
-- 一个能拉动的拉条，Value为数值

section:Label("标签")
-- 一个标签类似于留言
```

### 脚本如何加密
* 首先你要有一个邮箱
* 若没有邮箱用 QQ号@qq.com 也可以
* 下载一个Discord
* 电脑建议用电脑版，电脑更新太慢了
* 手机Discord安装包 ↓ ↓ ↓ ↓ ↓
* [https://share.weiyun.com/9EH1KEIU 密码：666666](https://share.weiyun.com/9EH1KEIU)
* 加入[Moonsec的频道](https://discord.gg/DxpvZzuJ6m)
* https://discord.gg/DxpvZzuJ6m
* 成员列表里面有个叫Moonsec V3的机器人 ![图片](https://raw.githubusercontent.com/renlua/Script-Tutorial/refs/heads/main/QQ20250119-122234.png)
* 给他发你要加密的脚本
* 他会返回一个东西 ![图片](https://raw.githubusercontent.com/renlua/Script-Tutorial/refs/heads/main/QQ20250118-163439.png)
* 点击那个蓝色的"here"
* 进去会跳转人机验证
* 过完后给那个机器人发"done"
* 他会返回一个东西 ![图片](https://raw.githubusercontent.com/renlua/Script-Tutorial/refs/heads/main/QQ20250119-123705.png)
* 下拉条选择Roblox ![图片](https://raw.githubusercontent.com/renlua/Script-Tutorial/refs/heads/main/QQ20250119-123903.png)
* 然后三个红色全部点满
* 一会儿，他会发一个东西 ![图片](https://raw.githubusercontent.com/renlua/Script-Tutorial/refs/heads/main/QQ20250118-164510.png)
* 点击那个蓝色的"[Click Here]"
* 他就会自动下载加密后的脚本到本地

  

