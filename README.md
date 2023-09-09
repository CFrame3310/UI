# Untitled UI Library
This Documentation is for " Untitled UI " .<br>
P.S. This UI isn't my Original but i modified source code for more features.
- Getting Start.
```lua
local library = loadstring(game:HttpGet('https://raw.githubusercontent.com/CFrame3310/UI/main/Untitled_UI.lua'))()
 ```
- CreateWatermark
```lua
library:CreateWatermark(<string> text)
 ```
- CreateWindow.
 ```lua
local Window = library:CreateWindow(<string> text, <Enum> Hide/Show key)
 ```
- CreateTab
```lua
local Tab = Window:CreateTab(<string> text)
 ```
- CreateThemeSystem
```lua
Tab:CreateThemeSystem(<string> text) 
 ```
- CreateSector
```lua
local Sector = Tab:CreateTab(<string> text , <string> Sector Side Left/Right)
```
- AddLabel
```lua
local Label = Sector:AddLabel(<string> text)
 ```
- AddSeperator
```lua
local Seperator = Sector:AddLabel(<string> text)
```
- AddToggle
```lua
Sector:AddToggle(<string> text, <bool> default, <function> callback)
```
- AddButton
```lua
Sector:AddButton(<string> text, <function> callback)
```
- AddTextbox
```lua
Sector:AddTextbox(<string> text, <string> default, <function> callback)
```
- AddColorpicker
```lua
Sector:AddColorpicker(<string> text, <Color3> default, <function> callback)
```
- AddSlider
```lua
Sector:AddSlider(<string> text, <int> min, <int> default, <int> max, <int> decimals, <function> callback)
```
- AddDropdown
```lua
Sector:AddDropdown(<string> text, <table> items, <string> default, <bool> multichoice, <function> callback)
```
- Example
```lua
local library = loadstring(game:HttpGet('https://raw.githubusercontent.com/CFrame3310/UI/main/Untitled_UI.lua'))()
library:CreateWatermark('Modify by cframe | {game} | {fps} ') -- {game} will replace with Game name and {fps} will replace with your fps.
local Window = library:CreateWindow("Window",Enum.KeyCode.RightControl)
local Tab = Window:CreateTab("Tab")
local Tab2 = Window:CreateTab("Tab2")
Tab2:CreateThemeSystem('Theme System')
local Sector1 = Tab:CreateSector("Sector1","Left")
local Sector2 = Tab:CreateSector("Sector2","Right")

Items = {1,2,3,4,5,6}

Sector1:AddLabel("Label")

Sector1:AddToggle("Toggle",false,function(t)
    print(t)
end)

Sector1:AddButton("Button",function(t)
    print(t)
end)

Sector1:AddDropdown("Dropdown",Items,"None",false,function(t)
    print(t)
end)

Sector1:AddDropdown("Multi Dropdown",Items,'None',true,function(t)
    print(t)
end)

Sector1:AddSlider("Slider",1,50,100,1,function(t)
    print(t)
end)

Sector1:AddColorpicker('ColorPicker',Color3.fromRGB(255, 255, 255),function(t)
    print(t)
end)

Sector1:AddTextbox("Text Box",' ',function(t)
   print(t)
end)

Sector1:AddSeperator("Seperator")
```
