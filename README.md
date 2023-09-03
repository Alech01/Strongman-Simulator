local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

-- Main window
local Window = OrionLib:MakeWindow({
  Name = "BOXING FRIENDS",
  HidePremium = false,
  SaveConfig = true,
  ConfigFolder = "BOXING FRIENDS"
})

-- Tabs
local MainTab = Window:MakeTab({
  Name = "Main", 
  Icon = "rbxassetid://4483345998"
})
local EggTab = Window:MakeTab({
    Name = "Main", 
    Icon = "rbxassetid://4483345998"
})

-- Elements
MainTab:AddParagraph("Created By:", "SOULY")

-- Main
local autoPunchEnabled = false

MainTab:AddToggle({
    Name = "Kill",
    Default = false,
    Callback = function(Value)
        _G.skipfight = Value
        while _G.skipfight and task.wait() do
            local args = {
                [1] = "Kill",
                [2] = "Level 20"
            }

            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("NPC"):FireServer(unpack(args))
        end
    end
})
MainTab:AddToggle({
    Name = "Beach Egg",
    Default = false,
    Callback = function(Value)
        _G.skipfight = Value
        while _G.skipfight and task.wait() do
            local args = {
                [1] = "Beach",
                [2] = 1
            }

            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("HatchEgg"):InvokeServer(unpack(args))
        end
    end
})
MainTab:AddToggle({
    Name = "Crystal Egg",
    Default = false,
    Callback = function(Value)
        _G.skipfight = Value
        while _G.skipfight and task.wait() do
            local args = {
                [1] = "Crystal",
                [2] = 1
            }

            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("HatchEgg"):InvokeServer(unpack(args))
        end
    end
})
MainTab:AddToggle({
    Name = "Forest Egg",
    Default = false,
    Callback = function(Value)
        _G.skipfight = Value
        while _G.skipfight and task.wait() do
            local args = {
                [1] = "Forest",
                [2] = 1
            }

            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("HatchEgg"):InvokeServer(unpack(args))
        end
    end
})
MainTab:AddToggle({
    Name = "Dessert Egg",
    Default = false,
    Callback = function(Value)
        _G.skipfight = Value
        while _G.skipfight and task.wait() do
            local args = {
                [1] = "Desert",
                [2] = 1
            }

            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("HatchEgg"):InvokeServer(unpack(args))
        end
    end
})
MainTab:AddToggle({
    Name = "Hell Egg",
    Default = false,
    Callback = function(Value)
        _G.skipfight = Value
        while _G.skipfight and task.wait() do
            local args = {
                [1] = "Hell",
                [2] = 1
            }

            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("HatchEgg"):InvokeServer(unpack(args))
        end
    end
})
