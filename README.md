# 脚本制作教程
> [前言](#前言)
>
> [脚本如何制作](#脚本制作教程)
> [脚本如何加密](#加密)


### 前言
* 1.在你的设备上安装lua 编辑器 为了方便更好的了解lua这门语言 只观看不实践 永远没效果
* 2.学习lua 确保绝对会语法
* 3.做脚本可能会遇到开户等行为我们要抵止这种行为

### 脚本制作教程
* 制作脚本需要有一个UI 如:WareUI
* WareUI模板:
'''lua
local library = library:new("脚本名字")
local Tab = library:Tab("标签")
local section = Tab:section("分区",true)

section:Textbox("文本框", "", "请输入", function(s)
    print(s)
end)

section:Button("开关", function(s)
    print("Button")
end)

section:Toggle("开关", "", false, function(s)
    print(s)
end)

section:Dropdown("下拉条", '', {"0","1","2","3","4","5","6","7","8","9"}, function(s)
    print(s)
end)

section:Keybind("键位绑定", Enum.KeyCode.LeftControl, function(s)
    OpenMain()
end)

section:Slider("拉条", "", 1, 1, 100, false, function(s)
    print(s)
end)

section:Label("标签")

'''
