# Kavo-UI-Lib-Remake
Just remaking Kavo UI Lib as asked by Stefan.

## Getting Loadstring
```lua
local Library = loadstring(game:HttpGet("https://github.com/shezan78/Kavo-UI-Lib-Remake/blob/main/Kavo%20UI%20Library%20main%20source.lua"))()
```

## Creating UI Library Window
```lua
local Window = Library.CreateLib("TITLE", "DarkTheme")
--[[
  Themes:
    LightTheme
    DarkTheme
    GrapeTheme
    BloodTheme
    Ocean
    Midnight
    Sentinel
    Synapse
]]
```

## Creating Tabs
```lua
local Tab = Window:NewTab("TabName")
```

## Creating Section
```lua
local Section = Tab:NewSection("Section Name")
```
