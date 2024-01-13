local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

local Window = OrionLib:MakeWindow({Name = "No hub", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})
                                                    
local MainTab = Window:MakeTab({
	Name = "Main",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = MainTab:AddSection({
	Name = "Main"
})

MainTab:AddButton({
	Name = "Speedhack",
	Min = 21,
	Max = 21,
	Default = 5,
	Color = Color3.fromRGB(255,255,255),
	Increment = 1,
	ValueName = "WS",
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
	end    
})

MainTab:AddButton({
	Name = "NoclipGui",
	Callback = function()
        loadstring(game:HttpGet("https://pastebin.com/raw/B5xRxTnk",true))()
  	end    
})

MainTab:AddButton({
	Name = "Pov 120",
	Callback = function()

loadstring(game:HttpGet("https://raw.githubusercontent.com/ha2ke3oer/Pov120/main/README.md"))()
  	end    
})

MainTab:AddButton({
	Name = "SpeedBypass",
	Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/finngameandglitch/bypass/main/bypass'))()
  	end    
})

MainTab:AddButton({
	Name = "Godmode",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/ha2ke3oer/Godmode/main/README.md"))()
  	end    
})

MainTab:AddButton({
	Name = "No e wait",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/ha2ke3oer/Istantpp/main/README.md"))()
  	end    
})

local GameTab = Window:MakeTab({
	Name = "Game",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = GameTab:AddSection({
	Name = "Game"
})

GameTab:AddButton({
	Name = "Bypass Screech",
	Callback = function()
		loadstring(game:HttpGet("https://pastebin.com/raw/rX4Fkmry"))()
  	end    
})

GameTab:AddButton({
	Name = "Old Seek Modle",
	Callback = function()
		loadstring(game:HttpGet("https://pastebin.com/raw/uXY1EAxZ"))()
  	end    
})

local ModeTab = Window:MakeTab({
	Name = "Mode",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = ModeTab:AddSection({
	Name = "Mode"
})

ModeTab:AddButton({
	Name = "Impossible mode",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/Ukazix/impossible-mode/main/Protected_79.lua.txt'))()
  	end    
})

ModeTab:AddButton({
	Name = "Haymen",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/HollowedOutMods/MayhemMode/main/loader.lua'))() 
  	end    
})

ModeTab:AddButton({
	Name = "Hardcore mode",
	Callback = function()
		loadstring(game:HttpGet('https://pastebin.com/raw/fT92NSzU'))() 
  	end    
})

ModeTab:AddButton({
	Name = "Fragmented mode",
	Callback = function()
		loadstring(game:HttpGet("https://glot.io/snippets/gpw1ypnl5o/raw/main.lua"))()
  	end
})

ModeTab:AddButton({
	Name = "extreme mode",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/huyhoanphuc/yfff/main/%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%26%2520%26404"))() 
  	end    
})

ModeTab:AddButton({
	Name = "room & door mode",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/huyhoanphuc/roomsanddoors-20-20-20-20-20-20/main/%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%26%2520%26404"))() 
  	end    
})

ModeTab:AddButton({
	Name = "Interminable room mode",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/huyhoanphuc/entity-spawn/main/%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%252620%2682662%26862%26862%2620%2620%2620%2620%2620%2620%2620%2620%2620%2620%26275%2638627%268275263%268376373%26302%2602%2620%2620%2620%26102%263%26082%26297%261752%267551%20%267522%26763%26763%26765273%26763637364%2637636646464%2644646466464646466%266363663636353%266535353'))() 
  	end    
})

ModeTab:AddButton({
	Name = "Forbidden mode",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/Check6969/Utilities/main/Mod/forbidden_mode.lua"))()
  	end    
})

local ScriptTab = Window:MakeTab({
	Name = "Script",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = ScriptTab:AddSection({
	Name = "Script"
})

ScriptTab:AddButton({
	Name = "Dex v3",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/Babyhamsta/RBLX_Scripts/main/Universal/BypassedDarkDexV3.lua"))() 
  	end    
})

ScriptTab:AddButton({
	Name = "Backdoor",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/iK4oS/backdoor.exe/master/source.lua"))()
  	end    
})

ScriptTab:AddButton({
	Name = "F3x",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/iimateiYT/Scripts/main/F3X.lua"))() 
  	end    
})

ScriptTab:AddButton({
	Name = "auto report",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/CF-Trail/Auto-Report/main/revamp.lua'))()
  	end    
})

ScriptTab:AddButton({
	Name = "Ghost hub",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/GhostPlayer352/Test4/main/GhostHub'))() 
  	end    
})

ScriptTab:AddButton({
	Name = "neoncat hub",
	Callback = function()
		loadstring(game:HttpGet("https://pastebin.com/raw/YdaJZKQY"))()
  	end    
})

ScriptTab:AddButton({
	Name = "Neon hub",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/Nivgab/Scripts/main/dh/Protected_7560656421504974.lua.txt'))()
  	end    
})

ScriptTab:AddButton({
	Name = "Awesome script",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/yieviro92creepy/Ak/main/Z'))() 
  	end    
})

ScriptTab:AddButton({
	Name = "Yieviro92creepy hub",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/yieviro92creepy/Bddtt/main/Taoao'))()
  	end    
})

ScriptTab:AddButton({
	Name = "Keyboard",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/advxzivhsjjdhxhsidifvsh/mobkeyboard/main/main.txt
  	end    
})

ScriptTab:AddButton({
	Name = "Blacking x bobhub",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/ZanoLeafVN/Blackking-x-BobHub/main/Bxb-obf.lua', true))()
  	end    
})

ScriptTab:AddButton({
	Name = "Fe fly",
	Callback = function()
		loadstring(game:HttpGet(('https://pastebin.com/raw/YvKv4AuY'),true))() 
  	end    
})

ScriptTab:AddButton({
	Name = "Night vision [press the letter t on the keybord",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/iCherryKardes/Doors/main/T%20to%20Night%20Vision"))()
  	end    
})

ScriptTab:AddButton({
	Name = "Bypass speed",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/finngameandglitch/bypass/main/bypass'))() 
  	end    
})

ScriptTab:AddButton({
	Name = "Doors hub",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/PVOwner/Doors/main/Doors2'))()
  	end    
})

ScriptTab:AddButton({
	Name = "Bruh hub",
	Callback = function()
		loadstring(game:HttpGet("https://raw.github.com/literallynotbruh/Doors-Hack/main/77_AJ84W5XNC4.lua"))() 
  	end    
})
ScriptTab:AddButton({
	Name = "Dxrk hub",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/CreepyPSC/dxrkhub/main/doors-scripts/hub-source"))() 
  	end    
})
ScriptTab:AddButton({
	Name = "Morph entity",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/ChronoAccelerator/Public-Scripts/main/Morphing/MorphScript.lua"))() 
  	end    
})

ScriptTab:AddButton({
	Name = "Exolution hub",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/ExolutionProject/Scripts/main/ExolutionPremiumHub.lua'))() 
  	end    
})

ScriptTab:AddButton({
	Name = "folder Gui",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/VaniaPerets/FolderGui-FolderHub/main/loader.lua", true))()
  	end    
})

ScriptTab:AddButton({
	Name = "depth hub",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/sirapobsriumang/Doors/main/Doors-scriptv2"))()
  	end    
})

ScriptTab:AddButton({
	Name = "Poop hub",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/zoophiliaphobic/POOPDOORS/main/script.lua'))()
  	end    
})

ScriptTab:AddButton({
	Name = "kinghub",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/KINGHUB01/KING-HUB-NO-1/main/kingshubno1"))()
  	end    
})

ScriptTab:AddButton({
	Name = "spawn entity hub",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/plamen6789/UtilitiesHub/main/UtilitiesGUI'))()
  	end    
})
local OtherScriptTab = Window:MakeTab({
	Name = "OtherScript",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

OtherScriptTab:AddButton({
	Name = "Remove door 50",
	Callback = function()
		game:GetService("Workspace").CurrentRooms:FindFirstChild("50").Door.Door:remove()
  	end    
})

OtherScriptTab:AddButton({
	Name = "Window on evry door",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/therealderkleinetiger/Doors-Public/main/Sally%20on%20every%20Window.lua"))()
  	end    
})

OtherScriptTab:AddButton({
	Name = "Tablet in shop",
	Callback = function()
		_G.UpdateStars = false -- stars disappear after picking up a book/breaker pole | false: a little lag
_G.OnShop = true -- can buy on pre run shop
_G.Price = 1 -- tablet price on shop
_G.Description = "FREE IPAD" -- tablet description on shop

loadstring(game:HttpGet('https://raw.githubusercontent.com/DeividComSono/Scripts/main/Scanner.lua'))()
  	end    
})

OtherScriptTab:AddButton({
	Name = "MCDonalds in door 0",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/K0t1n/Public/main/MCDonalds"))()
  	end    
})

OtherScriptTab:AddButton({
	Name = "Noclip + Bypass",
	Callback = function()
_G.Keybind = "R"
_G.ClipGui = true
_G.IncludeNoclip = true

local isEnabled = false

local UIS = game:GetService("UserInputService")

local Plr = game.Players.LocalPlayer
local Char = Plr.Character or Plr.CharacterAdded:Wait()

local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Parent = game.CoreGui
ScreenGui.Enabled = _G.ClipGui or false

local TextLabel = Instance.new("TextLabel")
TextLabel.Parent = ScreenGui

TextLabel.AnchorPoint = Vector2.new(1, 0)
TextLabel.Position = UDim2.new(1, -5, 0, 0)
TextLabel.Text = "Noclip + Bypasser: Off"
TextLabel.Size = UDim2.new(0,200,0,75)
TextLabel.TextScaled = true
TextLabel.TextStrokeColor3 = Color3.new(1,1,1)
TextLabel.TextStrokeTransparency = 0
TextLabel.BackgroundTransparency = 1

function getValue()
    local value
    if isEnabled then
        value = "On"
    else
        value = "Off"
    end
    return value
end

UIS.InputBegan:Connect(function(input, gp)
    if gp then return end

    if input.KeyCode == Enum.KeyCode[_G.Keybind] then
        isEnabled = not isEnabled
        task.wait()
        TextLabel.Text = "Noclip + Bypasser: " .. getValue()
    end
end)

game:GetService("RunService").RenderStepped:Connect(function()
    if not Char:FindFirstChild("HumanoidRootPart") then return end
    if _G.IncludeNoclip then
        Char.HumanoidRootPart.CanCollide = not isEnabled
        Char.Collision.CanCollide = not isEnabled
    end

    local HrpCFrame = Char.HumanoidRootPart.CFrame

    local ray = Ray.new(HrpCFrame.Position, HrpCFrame.LookVector * 0.5)
    local part = workspace:FindPartOnRay(ray)
    if part and part.CanCollide == true and isEnabled then
        Char.HumanoidRootPart.Anchored = true
        Char:PivotTo(Char.HumanoidRootPart.CFrame * CFrame.new(0, 1000, 0))
        task.wait()
        Char:PivotTo(Char.HumanoidRootPart.CFrame * CFrame.new(0, 0, -4))
        task.wait()
        Char:PivotTo(Char.HumanoidRootPart.CFrame * CFrame.new(0, -1000, 0))
        task.wait(0.1)
        Char.HumanoidRootPart.Anchored = false
    end
end)
  	end    
})

OtherScriotTab:AddButton({
	Name = "Figure Pov Door 100 script",
	Callback = function()
		loadstring(game:HttpGet("https://pastebin.com/raw/hViaKdbk"))()
  	end    
})

OtherScriptTab:AddButton({
	Name = "Figure Pov Door 50 script",
	Callback = function()
		loadstring(game:HttpGet("https://pastebin.com/raw/yAmUcY13"))()
  	end    
})

OtherScriptTab:AddButton({
	Name = "Seek Pov script",
	Callback = function()
		loadstring(game:HttpGet("https://pastebin.com/raw/QPsfr9P4"))()
  	end    
})

OtherScriptTab:AddButton({
	Name = "esp!",
	Callback = function()
		hrp.Parent.Humanoid.Changed:Connect(function(property) --//Triggers when any Property changed
hrp.total.total2.Frame.Size = UDim2.new(1,0,hrp.Parent.Humanoid.Health/100,0) --//Adjusts the size of the green Frame								
end)
end
-- -----------------------------------------------------------------------------------
function createESP(c) --//Checks and calls the proper function
bugfix = c:WaitForChild("Head") --// *Used so the children of the character arent nil.
for i,v in pairs(c:GetChildren()) do
if checkPart(v) then
actualESP(v)
end
end
if HEALTHBAR_ACTIVATED then --//If the user decided to
createHealthbar(c:WaitForChild("HumanoidRootPart")) --//Calls the function of the creation
end
end
-- -----------------------------------------------------------------------------------
for i,people in pairs(players:GetChildren())do
if people ~= players.LocalPlayer then
currentPlayer = people
								--//Used for Players already in the Game
createESP(people.Character)
people.CharacterAdded:Connect(function(character)
createESP(character)			
end)
end
end
-- -----------------------------------------------------------------------------------
end --//End of the entire function

createFlex() --// Does exactly that :)
  	end    
})

OtherScriptTab:AddButton({
	Name = "Fullbright",
	Callback = function()
		game:GetService ("Lighting").Brightness = 2 game:GetService ("Lighting").ClockTime = 14 game:GetService ("Lighting").FogEnd = 100000 game:GetService ("Lighting").GlobalShadows = false game:GetService ("Lighting").OutdoorAmbient = Color3.fromRGB (128, 128, 128)
  	end    
})

OtherScriptTab:AddButton({
	Name = "infiniteyield",
	Callback = function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
  	end    
})

local ItemTab = Window:MakeTab({
	Name = "Item",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = ItemTab:AddSection({
	Name = "Item"
})

ItemTab:AddButton({
	Name = "lazer gun",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/K0t1n/Public/main/Laser%20Gun.lua"))()
  	end    
})

ItemTab:AddButton({
	Name = "lucky block",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/K0t1n/Public/main/Lucky%20Block"))()
  	end    
})

ItemTab:AddButton({
	Name = "magic book",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/K0t1n/Public/main/Magic%20Book"))()
  	end    
})

ItemTab:AddButton({
	Name = "flamethrower",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/K0t1n/Public/main/Flamethrower"))()
  	end    
})

ItemTab:AddButton({
	Name = "chocolate bar",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/K0t1n/Public/main/Chocolate%20Bar.lua"))()
  	end    
})

ItemTab:AddButton({
	Name = "flashlight",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/K0t1n/Public/main/Flashlight.lua"))()
  	end    
})

ItemTab:AddButton({
	Name = "gummy flashlight",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/K0t1n/Public/main/Gummy%20Flashlight.lua"))()
end)
  	end    
})

ItemTab:AddButton({
	Name = "crucifix",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/huyhoanphuc/ygf/main/README.md", true))()
  	end    
})

ItemTab:AddButton({
	Name = "crucifix press q in keyboard",
	Callback = function()
_G.Uses = 9999
_G.Range = 999
_G.OnAnything = true
_G.Fail = false
loadstring(game:HttpGet('https://raw.githubusercontent.com/PenguinManiack/Crucifix/main/Crucifix.lua'))() 
  	end    
})

ItemTab:AddButton({
	Name = "magnet",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/MrNeRD0/Doors-Hack/main/MagnetByNerd.lua"))()
  	end    
})

ItemTab:AddButton({
	Name = "holy hand",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/MrNeRD0/Doors-Hack/main/HolyGrenadeByNerd.lua"))()
  	end    
})

ItemTab:AddButton({
	Name = "minecraft debug",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/K0t1n/Public/main/Debug%20Stick"))()
  	end    
})

ItemTab:AddButton({
	Name = "shears",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/MrNeRD0/Doors-Hack/main/shears_done.lua"))()
  	end    
})

local Spawn entityTab = Window:MakeTab({
	Name = "Spawn entity",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = SpawnentityTab:AddSection({
	Name = "Spawnentity"
})

SpawnentityTab:AddButton({
	Name = "blink",
	Callback = function()
		loadstring(game:HttpGet("https://pastebin.com/raw/8uvEapQw"))()
  	end    
})

SpawnentityTab:AddButton({
	Name = "rebound",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/ha2ke3oer/Rebound/main/README.md"))()
  	end    
})

SpawnentityTab:AddButton({
	Name = "c 60",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/ha2ke3oer/X-60/main/README.md"))()
  	end    
})

SpawnentityTab:AddButton({
	Name = "deer god",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/ha2ke3oer/Deer-god/main/README.md"))()
  	end    
})
