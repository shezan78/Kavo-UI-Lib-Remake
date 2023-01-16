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

## Update section
```lua
Section:UpdateSection("Section New Title")
```

## Creating Labels
```lua
Section:NewLabel("LabelText")
```

## Update Label
```lua
label:UpdateLabel("New Text")
```

## Creating Buttons
```lua
Section:NewButton("ButtonText", "ButtonInfo", function()
    print("Clicked") -- You can also put a loadstring here
end)
```

## Update Button
Make sure your button is local when updating it.
```lua
button:UpdateButton("New Text")
```

## Creating Toggles
```lua
Section:NewToggle("ToggleText", "ToggleInfo", function(state)
    if state then
        print("Toggle On") -- You can put a loadstring or script here
    else
        print("Toggle Off") -- You can put a loadstring or script here
    end
end)
```

## Updating Toggles
```lua
getgenv().Toggled = false

local toggle = Section:NewToggle("Toggle", "Info", (state)
    getgenv().Toggled = state
end)

game:GetService("RunService").RenderStepped:Connect(function()
	if getgenv().Toggled then
		toggle:UpdateToggle("Toggle On")
	else
		toggle:UpdateToggle("Toggle Off")
	end
end)
```

## Creating Sliders
```lua
Section:NewSlider("SliderText", "SliderInfo", 500, 0, function(s) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)
```

## Creating Textboxes
```lua
Section:NewTextBox("TextboxText", "TextboxInfo", function(txt)
	print(txt)
end)
```

## Creating Keybinds
```lua
Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.F, function()
	print("You just clicked the bind")
end)

```

## Toggling UI with Keybinds
```lua
Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.F, function()
	Library:ToggleUI()
end)
```
