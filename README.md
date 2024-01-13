local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

local Window = OrionLib:MakeWindow({Name = "No hub v2", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})
                                                    

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

local BypassTab = Window:MakeTab({
	Name = "Bypass",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = BypassTab:AddSection({
	Name = "Bypass"
})

BypassTab:AddButton({
	Name = "Bypass Screech",
	Callback = function()
		loadstring(game:HttpGet("https://pastebin.com/raw/rX4Fkmry"))()
  	end    
})
local GameTab = Window:MakeTab({
	Name = "Game",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

GameTab:AddButton({
	Name = "Notify entity",
	Callback = function()
        local addconnect
        addconnect = workspace.ChildAdded:Connect(function(v)
            if table.find(entitynames,v.Name) then
                repeat task.wait() until plr:DistanceFromCharacter(v:GetPivot().Position) < 1000 or not v:IsDescendantOf(workspace)
                
                if v:IsDescendantOf(workspace) then
                    message(v.Name:gsub("Moving",""):lower().." is coming go hide")
                end
            end
        end) 
        
        repeat task.wait() until not flags.hintrush
        addconnect:Disconnect()
    end
end)
  	end    
})

GameTab:AddButton({
	Name = "Old Seek Modle",
	Callback = function()
		loadstring(game:HttpGet("https://pastebin.com/raw/uXY1EAxZ"))()
  	end    
})

GameTab:AddButton({
	Name = "Skeleton no lock",
	Callback = function()
		local addconnect
        addconnect = workspace.CurrentRooms.ChildAdded:Connect(function(room)
            local door = room:WaitForChild("Wax_Door",2)
            
            if door then
                door:Destroy() 
            end
        end)
        
        repeat task.wait() until not flags.noskeledoors
        addconnect:Disconnect()
    end
end)
        local function deciphercode()
        local paper = char:FindFirstChild("LibraryHintPaper")
        local hints = plr.PlayerGui:WaitForChild("PermUI"):WaitForChild("Hints")
        
        local code = {[1]="_",[2]="_",[3]="_",[4]="_",[5]="_"}
            
            if paper then
                for i,v in pairs(paper:WaitForChild("UI"):GetChildren()) do
                    if v:IsA("ImageLabel") and v.Name ~= "Image" then
                        for i,img in pairs(hints:GetChildren()) do
                            if img:IsA("ImageLabel") and img.Visible and v.ImageRectOffset == img.ImageRectOffset then
                                local num = img:FindFirstChild("TextLabel").Text
                                
                                code[tonumber(v.Name)] = num 
                            end
                        end
                    end
                end 
            end
            
            return code
        end
        
        local addconnect
        addconnect = char.ChildAdded:Connect(function(v)
            if v:IsA("Tool") and v.Name == "LibraryHintPaper" then
                task.wait()
                
                local code = table.concat(deciphercode())
                
                if code:find("_") then
                    message("get all hints first")
                else
                    message("the code is ".. code)
                end
            end
        end)
        
        repeat task.wait() until not flags.getcode
        addconnect:Disconnect()
    end
end)
  	end    
})

GameTab:AddButton({
	Name = "A 000 no lock",
	Callback = function()
		local function check(room)
            local door = room:WaitForChild("RoomsDoor_Entrance",2)
            
            if door then
                local prompt = door:WaitForChild("Door"):WaitForChild("EnterPrompt")
                prompt.Enabled = true
            end 
        end
        
        local addconnect
        addconnect = workspace.CurrentRooms.ChildAdded:Connect(function(room)
            check(room)
        end)
        
        for i,v in pairs(workspace.CurrentRooms:GetChildren()) do
            check(room)
        end
        
        repeat task.wait() until not flags.roomsnolock
        addconnect:Disconnect()
    end
end)
  	end    
})

OtherTab:AddButton({
	Name = "Auto loot",
	Callback = function()
		local function setup(room)
            local function check(v)
                if v:IsA("Model") then
                    if v.Name == "DrawerContainer" then
                        local knob = v:WaitForChild("Knobs")
                        
                        if knob then
                            local prompt = knob:WaitForChild("ActivateEventPrompt")
                            local interactions = prompt:GetAttribute("Interactions")
                            
                            if not interactions then
                                task.spawn(function()
                                    repeat task.wait(0.1)
                                        if plr:DistanceFromCharacter(knob.Position) <= 12 then
                                            fireproximityprompt(prompt)
                                        end
                                    until prompt:GetAttribute("Interactions") or not flags.draweraura
                                end)
                            end
                        end
                    elseif v.Name == "GoldPile" then
                        local prompt = v:WaitForChild("LootPrompt")
                        local interactions = prompt:GetAttribute("Interactions")
                            
                        if not interactions then
                            task.spawn(function()
                                repeat task.wait(0.1)
                                    if plr:DistanceFromCharacter(v.PrimaryPart.Position) <= 12 then
                                        fireproximityprompt(prompt) 
                                    end
                                until prompt:GetAttribute("Interactions") or not flags.draweraura
                            end)
                        end
                    elseif v.Name:sub(1,8) == "ChestBox" then
                        local prompt = v:WaitForChild("ActivateEventPrompt")
                        local interactions = prompt:GetAttribute("Interactions")
                        
                        if not interactions then
                            task.spawn(function()
                                repeat task.wait(0.1)
                                    if plr:DistanceFromCharacter(v.PrimaryPart.Position) <= 12 then
                                        fireproximityprompt(prompt)
                                    end
                                until prompt:GetAttribute("Interactions") or not flags.draweraura
                            end)
                        end
                    elseif v.Name == "RolltopContainer" then
                        local prompt = v:WaitForChild("ActivateEventPrompt")
                        local interactions = prompt:GetAttribute("Interactions")
                        
                        if not interactions then
                            task.spawn(function()
                                repeat task.wait(0.1)
                                    if plr:DistanceFromCharacter(v.PrimaryPart.Position) <= 12 then
                                        fireproximityprompt(prompt)
                                    end
                                until prompt:GetAttribute("Interactions") or not flags.draweraura
                            end)
                        end
                    end 
                end
            end
    
            local subaddcon
            subaddcon = room.DescendantAdded:Connect(function(v)
                check(v) 
            end)
            
            for i,v in pairs(room:GetDescendants()) do
                check(v)
            end
            
            task.spawn(function()
                repeat task.wait() until not flags.draweraura
                subaddcon:Disconnect() 
            end)
        end
        
        local addconnect
        addconnect = workspace.CurrentRooms.ChildAdded:Connect(function(room)
            setup(room)
        end)
        
        for i,room in pairs(workspace.CurrentRooms:GetChildren()) do
            if room:FindFirstChild("Assets") then
                setup(room) 
            end
        end
        
        repeat task.wait() until not flags.draweraura
        addconnect:Disconnect()
    end
end)
  	end    
})
local ModeTab = Window:MakeTab({
	Name = "Mode",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
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
