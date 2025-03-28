* 感谢本地温迪 QQ 2378518248
* 感谢小云 QQ 168777105
* 感谢https://?¿¿X0℃¹² QQ 2173548297

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
    { pattern = "打印:", replace = "print" },
    { pattern = "局部:设", replace = "local " },
    { pattern = "为:", replace = "=" },
    { pattern = "局部:方法", replace = "local function " },
    { pattern = "方法:", replace = "function" },
    { pattern = "方法执行", replace = "function()" },
    { pattern = "返回:", replace = "return " },
    { pattern = "结束}", replace = "end " },
    { pattern = "加", replace = "+" },
    { pattern = "减", replace = "-" },
    { pattern = "真的", replace = "true" },
    { pattern = "假的", replace = "false" },
    { pattern = "乘", replace = "*" },
    { pattern = "除", replace = "/" },
    { pattern = "等于", replace = "==" },
    { pattern = "不等于", replace = "~=" },
    { pattern = "大于", replace = ">" },
    { pattern = "小于", replace = "<" },
    { pattern = "大于等于", replace = ">=" },
    { pattern = "小于等于", replace = "<=" },
    { pattern = "且", replace = "and " },
    { pattern = "或", replace = "or " },
    { pattern = "不是", replace = "not " },
    { pattern = "如果", replace = "if " },
    { pattern = "那么", replace = " then " },
    { pattern = "其他:", replace = "else " },
    { pattern = "别的如果", replace = "elseif " },
    { pattern = "停止", replace = "break " },
    { pattern = "对于", replace = "for " },
    { pattern = "在:", replace = "in " },
    { pattern = "当", replace = "while " },
    { pattern = "就执行{", replace = "do " },
    { pattern = "等待", replace = "task.wait() " },
    { pattern = "继续", replace = "continue " },
    { pattern = "转化数字:", replace = "tonumber" },
    { pattern = "转换字符:", replace = "tostring" },
    { pattern = "类型:", replace = "type" },
    { pattern = "抛出错误:", replace = "error" },
    { pattern = "判断是否抛出错误:", replace = "assert" },
    { pattern = "远程事件:", replace = "game:GetService('ReplicatedStorage')." },
    { pattern = "获取子级:", replace = "GetChildren()" },
    { pattern = "列表:插入:", replace = "table.insert" },
    { pattern = "列表:移除:", replace = "table.remove" },
    { pattern = "列表:元素连接:", replace = "table.concat" },
    { pattern = "列表:制成表:", replace = "table.pack" },
    { pattern = "列表:分解表:", replace = "table.unpack" },
    { pattern = "字符:子字符串:", replace = "string.sub" },
    { pattern = "字符:长度:", replace = "string.len" },
    { pattern = "字符:全改小写:", replace = "string.lower" },
    { pattern = "字符:全改大写:", replace = "string.upper" },
    { pattern = "字符:格式字符:", replace = "string.format" },
    { pattern = "字符寻找字符:", replace = "string.match" },
    { pattern = "字符:更替字符:", replace = "string.gsub" },
    { pattern = "数学:绝对值:", replace = "math.abs" },
    { pattern = "数学:大数取整:", replace = "math.ceil" },
    { pattern = "数学:小数取整:", replace = "math.floor" },
    { pattern = "数学:取最大返回:", replace = "math.max" },
    { pattern = "数学:取最小返回:", replace = "math.min" },
    { pattern = "数学:随机数:", replace = "math.random" },
    { pattern = "数学:平方根:", replace = "math.sqrt" },
    { pattern = "创建协程:", replace = "coroutine.create" },
    { pattern = "恢复协程:", replace = "coroutine.resume" },
    { pattern = "挂起协程:", replace = "coroutine.yield" },
    { pattern = "当前时间:", replace = "os.time" },
    { pattern = "当前日期:", replace = "os.date" },
    { pattern = "重复:", replace = "repeat " },
    { pattern = "直到:", replace = "until " },
    { pattern = "全局:", replace = "" },
    { pattern = "模块:", replace = "require" },
    { pattern = "定义类:", replace = "class '" },
    { pattern = "类结束", replace = "' end" },
    { pattern = "继承:", replace = ":extend" },
    { pattern = "初始化:", replace = "__init" },
    { pattern = "静态:", replace = "static" },
    { pattern = "只读:", replace = "readonly" },
    { pattern = "属性:", replace = "property" },
    { pattern = "方法:", replace = "method" },
    { pattern = "调用", replace = "()" },
    { pattern = "构造器:", replace = "__newindex" },
    { pattern = "元表:", replace = "metatable" },
    { pattern = "设置元表:", replace = "setmetatable" },
    { pattern = "获取元表:", replace = "getmetatable" },
    { pattern = "索引:", replace = "__index" },
    { pattern = "新索引:", replace = "__newindex" },
    { pattern = "连接:", replace = ".." },
    { pattern = "长度", replace = "#" },
    { pattern = "文件打开:", replace = "io.open" },
    { pattern = "文件关闭:", replace = "io.close" },
    { pattern = "文件读取:", replace = "io.read" },
    { pattern = "文件写入:", replace = "io.write" },    
    { pattern = "环境:", replace = "_G" },
    { pattern = "加载:", replace = "load" },
    { pattern = "加载字符串:", replace = "loadstring" },
    { pattern = "执行:", replace = "pcall" },
    { pattern = "断言:", replace = "assert" },
    { pattern = "错误处理:", replace = "xpcall" },
    { pattern = "延迟调用:", replace = "defer" },
    { pattern = "线程:", replace = "thread" },
    { pattern = "新建线程:", replace = "coroutine.create" },
    { pattern = "启动线程:", replace = "coroutine.resume" },
    { pattern = "挂起线程:", replace = "coroutine.yield" },
    { pattern = "克隆:", replace = "clone" },
    { pattern = "销毁:", replace = "destroy" },
    { pattern = "父对象:", replace = ".Parent" },
    { pattern = "子对象:", replace = ".Children" },
    { pattern = "实例:", replace = "Instance" },
    { pattern = "新建实例:", replace = "Instance.new" },
    { pattern = "游戏服务:", replace = "game:GetService" },
    { pattern = "工作空间:", replace = "workspace" },
    { pattern = "玩家:", replace = "Players" },
    { pattern = "服务器:", replace = "ServerScriptService" },
    { pattern = "客户端:", replace = "StarterPlayer" },
    { pattern = "资源存储:", replace = "ReplicatedStorage" },
    { pattern = "光照:", replace = "Lighting" },
    { pattern = "声音:", replace = "SoundService" },
    { pattern = "网络:", replace = "NetworkServer" },
    { pattern = "聊天:", replace = "Chat" },
    { pattern = "物理:", replace = "PhysicsService" },
    { pattern = "数据存储:", replace = "DataStoreService" },
    { pattern = "市场:", replace = "MarketplaceService" },
    { pattern = "用户输入:", replace = "UserInputService" },
    { pattern = "分析:", replace = "AnalyticsService" },
    { pattern = "数据:", replace = "game" },
    { pattern = "等待:", replace = "wait" },
    { pattern = "任务等待:", replace = "task.wait" },
    { pattern = "服务:", replace = "Service" },
    { pattern = "事件:", replace = "Event" },
    { pattern = "信号:", replace = "Signal" },
    { pattern = "连接:", replace = "Connect" },
    { pattern = "触发:", replace = "Fire" },
    { pattern = "断开:", replace = "Disconnect" },
    { pattern = "等待完成:", replace = "Wait" },
    { pattern = "绑定到渲染步:", replace = "BindToRenderStep" },
    { pattern = "取消绑定:", replace = "UnbindFromRenderStep" },
    { pattern = "绑定到帧:", replace = "BindToFrame" },
    { pattern = "取消帧绑定:", replace = "UnbindFromFrame" },
    { pattern = "绑定到输入:", replace = "BindToInput" },
    { pattern = "取消输入绑定:", replace = "UnbindFromInput" },
    { pattern = "绑定到用户动作:", replace = "BindToUserAction" },
    { pattern = "取消用户动作绑定:", replace = "UnbindFromUserAction" },
    { pattern = "绑定到远程事件:", replace = "OnClientEvent" },
    { pattern = "触发远程事件:", replace = "FireServer" },
    { pattern = "绑定到远程过程调用:", replace = "OnClientInvoke" },
    { pattern = "触发远程过程调用:", replace = "InvokeServer" },
    { pattern = "绑定到属性改变:", replace = "Changed" },
    { pattern = "绑定到销毁:", replace = "Destroying" },
    { pattern = "绑定到子对象添加:", replace = "ChildAdded" },
    { pattern = "绑定到子对象移除:", replace = "ChildRemoved" },
    { pattern = "绑定到父对象改变:", replace = "ParentChanged" },
    { pattern = "绑定到点击:", replace = "MouseButton1Click" },
    { pattern = "绑定到拖动开始:", replace = "DragBegin" },
    { pattern = "绑定到拖动结束:", replace = "DragEnd" },
    { pattern = "绑定到鼠标进入:", replace = "MouseEnter" },
    { pattern = "绑定到鼠标离开:", replace = "MouseLeave" },
    { pattern = "绑定到鼠标移动:", replace = "MouseMove" },
    { pattern = "绑定到触摸开始:", replace = "TouchStarted" },
    { pattern = "绑定到触摸结束:", replace = "TouchEnded" },
    { pattern = "绑定到触摸移动:", replace = "TouchMoved" },
    { pattern = "绑定到输入开始:", replace = "InputBegan" },
    { pattern = "绑定到输入结束:", replace = "InputEnded" },
    { pattern = "绑定到键盘按下:", replace = "KeyPress" },
    { pattern = "绑定到键盘释放:", replace = "KeyRelease" },
    { pattern = "绑定到文本输入:", replace = "TextInput" },
    { pattern = "绑定到文本更改:", replace = "TextChanged" },
    { pattern = "绑定到滑动开始:", replace = "ScrollBegin" },
    { pattern = "绑定到滑动结束:", replace = "ScrollEnd" },
    { pattern = "绑定到滑动移动:", replace = "ScrollMove" },
    { pattern = "绑定到游戏加载:", replace = "GameLoaded" },
    { pattern = "绑定到游戏保存:", replace = "GameSaving" },
    { pattern = "绑定到游戏关闭:", replace = "GameClosing" },
    { pattern = "绑定到玩家加入:", replace = "PlayerAdded" },
    { pattern = "绑定到玩家移除:", replace = "PlayerRemoving" },
    { pattern = "绑定到玩家重生:", replace = "PlayerRespawning" },
    { pattern = "绑定到玩家重生完成:", replace = "PlayerRespawned" },
    { pattern = "绑定到角色添加:", replace = "CharacterAdded" },
    { pattern = "绑定到角色移除:", replace = "CharacterRemoving" },
    { pattern = "绑定到角色重生:", replace = "CharacterRespawning" },
    { pattern = "绑定到角色重生完成:", replace = "CharacterRespawned" },
    { pattern = "绑定到角色身体部分添加:", replace = "BodyPartAdded" },
    { pattern = "绑定到角色身体部分移除:", replace = "BodyPartRemoved" },
    { pattern = "绑定到角色身体部分改变:", replace = "BodyPartChanged" },
    { pattern = "绑定到角色身体部分碰撞:", replace = "BodyPartTouched" },
    { pattern = "绑定到角色身体部分不再碰撞:", replace = "BodyPartUntouched" },
    { pattern = "绑定到角色身体部分接触:", replace = "BodyPartContact" },
    { pattern = "绑定到角色身体部分接触结束:", replace = "BodyPartContactEnd" },
    { pattern = "绑定到角色身体部分接触开始:", replace = "BodyPartContactStart" },
    { pattern = "绑定到角色身体部分接触移动:", replace = "BodyPartContactMove" },
    { pattern = "绑定到角色身体部分接触更新:", replace = "BodyPartContactUpdate" },
    { pattern = "绑定到角色身体部分接触状态改变:", replace = "BodyPartContactStateChanged" },
    { pattern = "绑定到角色身体部分接触状态开始:", replace = "BodyPartContactStateStart" },
    { pattern = "绑定到角色身体部分接触状态结束:", replace = "BodyPartContactStateEnd" },
    { pattern = "绑定到角色身体部分接触状态更新:", replace = "BodyPartContactStateUpdate" },
    { pattern = "绑定到远程事件:", replace = "OnClientEvent" },
    { pattern = "触发远程事件:", replace = "FireServer" },
    { pattern = "绑定到远程过程调用:", replace = "OnClientInvoke" },
    { pattern = "触发远程过程调用:", replace = "InvokeServer" },
    { pattern = "绑定到属性改变:", replace = "Changed" },
    { pattern = "绑定到销毁:", replace = "Destroying" },
    { pattern = "绑定到子对象添加:", replace = "ChildAdded" },
    { pattern = "绑定到子对象移除:", replace = "ChildRemoved" },
    { pattern = "绑定到父对象改变:", replace = "ParentChanged" },
    { pattern = "绑定到点击:", replace = "MouseButton1Click" },
    { pattern = "绑定到拖动开始:", replace = "DragBegin" },
    { pattern = "绑定到拖动结束:", replace = "DragEnd" },
    { pattern = "绑定到鼠标进入:", replace = "MouseEnter" },
    { pattern = "绑定到鼠标离开:", replace = "MouseLeave" },
    { pattern = "绑定到鼠标移动:", replace = "MouseMove" },
    { pattern = "绑定到触摸开始:", replace = "TouchStarted" },
    { pattern = "绑定到触摸结束:", replace = "TouchEnded" },
    { pattern = "绑定到触摸移动:", replace = "TouchMoved" },
    { pattern = "绑定到输入开始:", replace = "InputBegan" },
    { pattern = "绑定到输入结束:", replace = "InputEnded" },
    { pattern = "绑定到键盘按下:", replace = "KeyPress" },
    { pattern = "绑定到键盘释放:", replace = "KeyRelease" },
    { pattern = "绑定到文本输入:", replace = "TextInput" },
    { pattern = "绑定到文本更改:", replace = "TextChanged" },
    { pattern = "绑定到滑动开始:", replace = "ScrollBegin" },
    { pattern = "绑定到滑动结束:", replace = "ScrollEnd" },
    { pattern = "绑定到滑动移动:", replace = "ScrollMove" },
    { pattern = "绑定到游戏加载:", replace = "GameLoaded" },
    { pattern = "绑定到游戏保存:", replace = "GameSaving" },
    { pattern = "绑定到游戏关闭:", replace = "GameClosing" },
    { pattern = "绑定到玩家加入:", replace = "PlayerAdded" },
    { pattern = "绑定到玩家移除:", replace = "PlayerRemoving" },
    { pattern = "绑定到玩家重生:", replace = "PlayerRespawning" },
    { pattern = "绑定到玩家重生完成:", replace = "PlayerRespawned" },
    { pattern = "绑定到角色添加:", replace = "CharacterAdded" },
    { pattern = "绑定到角色移除:", replace = "CharacterRemoving" },
    { pattern = "绑定到角色重生:", replace = "CharacterRespawning" },
    { pattern = "绑定到角色重生完成:", replace = "CharacterRespawned" },
    { pattern = "绑定到角色身体部分添加:", replace = "BodyPartAdded" },
    { pattern = "绑定到角色身体部分移除:", replace = "BodyPartRemoved" },
    { pattern = "绑定到角色身体部分改变:", replace = "BodyPartChanged" },
    { pattern = "绑定到角色身体部分碰撞:", replace = "BodyPartTouched" },
    { pattern = "绑定到角色身体部分不再碰撞:", replace = "BodyPartUntouched" },
    { pattern = "绑定到角色身体部分接触:", replace = "BodyPartContact" },
    { pattern = "绑定到角色身体部分接触结束:", replace = "BodyPartContactEnd" },
    { pattern = "绑定到角色身体部分接触开始:", replace = "BodyPartContactStart" },
    { pattern = "绑定到角色身体部分接触移动:", replace = "BodyPartContactMove" },
    { pattern = "绑定到角色身体部分接触更新:", replace = "BodyPartContactUpdate" },
    { pattern = "绑定到角色身体部分接触状态改变:", replace = "BodyPartContactStateChanged" },
    { pattern = "绑定到角色身体部分接触状态开始:", replace = "BodyPartContactStateStart" },
    { pattern = "绑定到角色身体部分接触状态结束:", replace = "BodyPartContactStateEnd" },
    { pattern = "绑定到角色身体部分接触状态更新:", replace = "BodyPartContactStateUpdate" },
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
> 
> [Hook](#Hook)


#### 上传图片ID
* [Roblox创作中心 贴花](https://create.roblox.com/dashboard/creations?activeTab=Decal)
* https://create.roblox.com/dashboard/creations?activeTab=Decal
* 点击这个上传图片 ![图片](https://raw.githubusercontent.com/renlua/Script-Tutorial/refs/heads/main/QQ20250119-191659.png)
* 然后点击贴花右边的图像
* 或进此链接
* https://create.roblox.com/dashboard/creations?activeTab=Image
* 选择刚刚的图片
* 点击图片右上角三个点
* 然后点击复制资源ID
* 他会复制到剪切板
* 这个就是你的图片资源ID
* 但是还要在前面加rbxassetid://


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
-- listfiles("./")
-- listfiles("./文件夹名/")

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
loadstring(game:HttpGet("https://raw.githubusercontent.com/renlua/Script-Tutorial/refs/heads/main/Spy.lua"))()
```
* 这个不知道怎么说
* 上视频
* [https://share.weiyun.com/nbyqFvXG 密码：666666](https://share.weiyun.com/nbyqFvXG)

#### Dex
* 这是Dex代码，可以用来做脚本，功能比Spy多
* 也比Spy难
```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/renlua/Script-Tutorial/refs/heads/main/dex.lua"))()
```
* 这个不知道怎么说
* 上视频
* 教学1 [https://share.weiyun.com/l5l1wyHk 密码：666666](https://share.weiyun.com/l5l1wyHk)
* 教学2 [https://share.weiyun.com/WECQih4F 密码：666666](https://share.weiyun.com/WECQih4F)
* 教学3 [https://share.weiyun.com/kL40zxsx 密码：666666](https://share.weiyun.com/kL40zxsx)
#### Hook
```lua
hookfunction
这个的用法是修改这个函数
例如
hookfunction有两个写法

1.
local function hello()
    print("Hello")
end
hookfunction(print, hello)

2.
local old
old = hookfunction(print, function(self,...)
    self = "Hello"
    return old(self,...)
end)

两个的作用都是一样的
最常用是第二种

附抓包脚本
```
```lua


-- Gui to Lua
-- Version: 3.2

-- Instances:

local HttpSpy = Instance.new("ScreenGui")
local Background = Instance.new("Frame")
local Topbar = Instance.new("Frame")
local Icon = Instance.new("ImageLabel")
local Exit = Instance.new("TextButton")
local ImageLabel = Instance.new("ImageLabel")
local Minimize = Instance.new("TextButton")
local ImageLabel_2 = Instance.new("ImageLabel")
local TopBar = Instance.new("Frame")
local ImageLabel_3 = Instance.new("ImageLabel")
local ImageLabel_4 = Instance.new("ImageLabel")
local Title = Instance.new("TextLabel")
local UICorner = Instance.new("UICorner")
local MainContainer = Instance.new("ScrollingFrame")
local UIListLayout = Instance.new("UIListLayout")
local UICorner_2 = Instance.new("UICorner")
local TemplateText = Instance.new("TextButton")

--Properties:

HttpSpy.Name = "sb"
HttpSpy.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
HttpSpy.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
HttpSpy.ResetOnSpawn = false

Background.Name = "Background"
Background.Parent = HttpSpy
Background.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Background.BackgroundTransparency = 0.140
Background.BorderColor3 = Color3.fromRGB(139, 139, 139)
Background.BorderSizePixel = 0
Background.Position = UDim2.new(0.506695807, 0, 0.56610918, 0)
Background.Size = UDim2.new(0, 402, 0, 262)
Background.Active = true
Background.Draggable = true

Topbar.Name = "Topbar"
Topbar.Parent = Background
Topbar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Topbar.BackgroundTransparency = 1.000
Topbar.Size = UDim2.new(1, 0, 0, 25)

Icon.Name = "Icon"
Icon.Parent = Topbar
Icon.AnchorPoint = Vector2.new(0, 0.5)
Icon.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Icon.BackgroundTransparency = 1.000
Icon.Position = UDim2.new(0, 10, 0.5, 0)
Icon.Size = UDim2.new(0, 13, 0, 13)
Icon.Image = "rbxgameasset://Images/menuIcon"

Exit.Name = "Exit"
Exit.Parent = Topbar
Exit.BackgroundColor3 = Color3.fromRGB(12, 4, 20)
Exit.BackgroundTransparency = 0.180
Exit.BorderSizePixel = 0
Exit.Position = UDim2.new(0.870000005, 0, 0, 0)
Exit.Size = UDim2.new(-0.00899999961, 40, 1.04299998, -10)
Exit.Font = Enum.Font.Gotham
Exit.Text = "X"
Exit.TextColor3 = Color3.fromRGB(255, 255, 255)
Exit.TextSize = 13.000
Exit.MouseButton1Click:Connect(function()
HttpSpy:Destroy()
end)

ImageLabel.Parent = Exit
ImageLabel.BackgroundColor3 = Color3.fromRGB(36, 36, 36)
ImageLabel.BackgroundTransparency = 1.000
ImageLabel.Position = UDim2.new(0.999998331, 0, 0, 0)
ImageLabel.Size = UDim2.new(0, 9, 0, 16)
ImageLabel.Image = "http://www.roblox.com/asset/?id=8650484523"
ImageLabel.ImageColor3 = Color3.fromRGB(12, 4, 20)
ImageLabel.ImageTransparency = 0.180

Minimize.Name = "Minimize"
Minimize.Parent = Topbar
Minimize.BackgroundColor3 = Color3.fromRGB(12, 4, 20)
Minimize.BackgroundTransparency = 0.180
Minimize.BorderSizePixel = 0
Minimize.Position = UDim2.new(0.804174006, 0, 0, 0)
Minimize.Size = UDim2.new(0.00100000005, 27, 1.04299998, -10)
Minimize.Font = Enum.Font.Gotham
Minimize.Text = "-"
Minimize.TextColor3 = Color3.fromRGB(255, 255, 255)
Minimize.TextSize = 18.000

ImageLabel_2.Parent = Minimize
ImageLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel_2.BackgroundTransparency = 1.000
ImageLabel_2.Position = UDim2.new(-0.455000013, 1, 0, 0)
ImageLabel_2.Size = UDim2.new(0, 12, 0, 16)
ImageLabel_2.Image = "http://www.roblox.com/asset/?id=10555881849"
ImageLabel_2.ImageColor3 = Color3.fromRGB(12, 4, 20)
ImageLabel_2.ImageTransparency = 0.180

TopBar.Name = "TopBar"
TopBar.Parent = Topbar
TopBar.BackgroundColor3 = Color3.fromRGB(12, 4, 20)
TopBar.BackgroundTransparency = 0.180
TopBar.BorderSizePixel = 0
TopBar.Position = UDim2.new(0.268202901, 0, -0.00052294743, 0)
TopBar.Size = UDim2.new(0, 186, 0, 16)

ImageLabel_3.Parent = TopBar
ImageLabel_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel_3.BackgroundTransparency = 1.000
ImageLabel_3.Position = UDim2.new(0.999999642, 0, -0.00046946716, 0)
ImageLabel_3.Size = UDim2.new(0, 14, 0, 16)
ImageLabel_3.Image = "http://www.roblox.com/asset/?id=8650484523"
ImageLabel_3.ImageColor3 = Color3.fromRGB(12, 4, 20)
ImageLabel_3.ImageTransparency = 0.180

ImageLabel_4.Parent = TopBar
ImageLabel_4.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel_4.BackgroundTransparency = 1.000
ImageLabel_4.Position = UDim2.new(-0.0817726701, 0, 0, 0)
ImageLabel_4.Size = UDim2.new(0, 16, 0, 16)
ImageLabel_4.Image = "http://www.roblox.com/asset/?id=10555881849"
ImageLabel_4.ImageColor3 = Color3.fromRGB(12, 4, 20)
ImageLabel_4.ImageTransparency = 0.180

Title.Name = "Title"
Title.Parent = TopBar
Title.AnchorPoint = Vector2.new(0, 0.5)
Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Title.BackgroundTransparency = 1.000
Title.BorderSizePixel = 0
Title.Position = UDim2.new(-0.150533721, 32, 0.415876389, 0)
Title.Size = UDim2.new(0.522161067, 80, 1.11675644, -7)
Title.Font = Enum.Font.SourceSansLight
Title.Text = "Http Spy"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.TextSize = 17.000
Title.TextWrapped = true

UICorner.CornerRadius = UDim.new(0, 9)
UICorner.Parent = Background

MainContainer.Name = "MainContainer"
MainContainer.Parent = Background
MainContainer.AnchorPoint = Vector2.new(0.5, 0.5)
MainContainer.BackgroundColor3 = Color3.fromRGB(12, 4, 20)
MainContainer.BackgroundTransparency = 0.180
MainContainer.BorderColor3 = Color3.fromRGB(16, 16, 16)
MainContainer.BorderSizePixel = 0
MainContainer.Position = UDim2.new(0.5, 0, 0.540076315, 0)
MainContainer.Size = UDim2.new(1, -10, 0.91984731, -10)
MainContainer.BottomImage = "rbxgameasset://Images/scrollBottom (1)"
MainContainer.MidImage = "rbxgameasset://Images/scrollMid"
MainContainer.ScrollBarThickness = 4
MainContainer.TopImage = "rbxgameasset://Images/scrollTop"
MainContainer.AutomaticCanvasSize = "XY"

UIListLayout.Parent = MainContainer
UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
UIListLayout.Padding = UDim.new(0, 3)

UICorner_2.Parent = MainContainer


local script = Instance.new('LocalScript', MainContainer)

TemplateText.Name = "TemplateText"
TemplateText.Parent = HttpSpy.Background.MainContainer.LocalScript
TemplateText.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
TemplateText.BackgroundTransparency = 0.7
TemplateText.BorderSizePixel = 0
TemplateText.Position = UDim2.new(3.75832236e-08, 0, 0, 0)
TemplateText.Size = UDim2.new(1.00000012, 0, 0, 20)
TemplateText.Font = Enum.Font.SourceSansSemibold
TemplateText.Text = "ur mom"
TemplateText.TextColor3 = Color3.fromRGB(255, 255, 255)
TemplateText.TextScaled = true
TemplateText.TextSize = 14.000
TemplateText.TextWrapped = true
TemplateText.TextXAlignment = Enum.TextXAlignment.Center
TemplateText.TextYAlignment = Enum.TextYAlignment.Center

local Template = script.TemplateText

local function registerDynamicScrollingFrame(frame)
local layout = frame:FindFirstChildWhichIsA("UIListLayout")
local absoluteContentSize = layout.AbsoluteContentSize
frame.CanvasSize = UDim2.new(0, 0, 0, absoluteContentSize.Y)
layout:GetPropertyChangedSignal("AbsoluteContentSize"):Connect(function()
local absoluteContentSize = layout.AbsoluteContentSize
frame.CanvasSize = UDim2.new(0, 0, 0, absoluteContentSize.Y)
end)
end

appendfile("http.txt","RUN\n")
local function Log(text,headers)
print(text)
appendfile("http.txt",text.."\n")
local Label = Template:Clone()
if headers and type(headers) == "table" then 
text = text .. " (HEADERS:"
for Index, Value in next, headers do 
text = text.. tostring(Index).. ": "..tostring(Value)

end
text = text .. ")"
end
Label.Text = text 
Label.Parent = script.Parent
Label.MouseButton1Click:Connect(function()
setclipboard(text)
end)
end
registerDynamicScrollingFrame(MainContainer)
local HttpGet

HttpGet = hookfunction(game.HttpGet, function(self, url, ...)
Log("Http Get Request from: "..url)

return HttpGet(self, url, ...)
end)

local HttpPost

HttpPost = hookfunction(game.HttpPost, function(self, url, ...)
Log("Http Post Request from: "..url)

return HttpPost(self, url, ...)
end)


local RequestLog

local rbxreq = http_request or request or HttpPost or syn.request or fluxus.request
RequestLog = hookfunction(rbxreq, function(data)
Log(data.Url)

return RequestLog(data)
end)


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

  

