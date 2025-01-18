脚本教程看完变大牛

此文章为中文

请不要使用翻译

翻译会导致文章的符号变为中文!!!

#

# 脚本制作教程
> [前言](#前言)
>
> 脚本如何制作
> > [打开控制台](#脚本制作教程(打开控制台))
> > 
> > [脚本制作教程(基础)](#脚本制作教程(基础))
> >
> > [脚本制作教程(中等)](#脚本制作教程(中等))
> > 
> > [脚本制作教程(UI)](#脚本制作教程(UI))
> 
> [脚本如何加密](#加密)

#

### 前言
* 1.在你的设备上安装lua 编辑器 为了方便更好的了解lua这门语言 只观看不实践 永远没效果
* 2.学习lua 确保绝对会语法
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
* 基础代码
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
#

### 脚本制作教程(中等)
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
