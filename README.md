local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("ZETTO HUB", "BloodTheme")
local Tab = Window:NewTab("Mian")
local Section = Tab:NewSection("Auto fram")

Section:NewToggle("Auto Fram", "ZETTO HUB", function(state)
    loadstring(game:HttpGet("https://raw.githubusercontent.com/x7Bxraii/SaveMode/main/README.md"))()
end)

local Weaponlist = {}
local Weapon = nil

for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
    table.insert(Weaponlist,v.Name)
end

Section:NewToggle("Auto Equip", "ZETTO HUB NO.1", function(a)
    AutoEquiped = a
    end)
    
    spawn(function()
    while wait() do
    if AutoEquiped then
    pcall(function()
    game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Weapon))
    end)
    end
    end    
end)

Section:NewDropdown("select weapon", "Enjoy:)", Weaponlist, function(currentOption)
    Weapon = currentOption
end)


local Tab = Window:NewTab("Status")
local Section = Tab:NewSection("Status player")

Section:NewToggle("Auto stats", "menu stats", function(state)
    _G.AddPoint = state;
    while _G.AddPoint do wait()
    local args = {
        [1] = "AddPoint",
        [2] = "Melee",
        [3] = 1,
    }
    
    game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer(unpack(args))
    end
end)
Section:NewDropdown("Stats", "BRUH", {"melee"}, function(currentOption)

end)

local Tab = Window:NewTab("Raid")
local Section = Tab:NewSection("Raid Fram")
Section:NewToggle("Auto Buy Chip", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)

Section:NewDropdown("select Raid", "DropdownInf", {"Flame", "Ice", "Light", "Quake", "Dark", "Spider", "Rumble", "Magma", "Human:Buddha", "Sand", "Brid:Phonix", "Dough"}, function(currentOption)
    print(currentOption)
end)

Section:NewToggle("Auto Fram Raid", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
Section:NewToggle("Kill Aura", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
Section:NewToggle("Next Island", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
Section:NewToggle("Auto Awekening", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
--- รอไอเกมมันสร้างโอโต้ดัน

local Tab = Window:NewTab("Auto Item")
local Section = Tab:NewSection("Fine Item")

Section:NewToggle("Auto Saber", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
Section:NewToggle("Auto Yama", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)

Section:NewToggle("Auto Tushita", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)

Section:NewToggle("Auto Rengoku", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)

Section:NewToggle("Auto Canvender", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)

Section:NewToggle("Auto Dark Dagger", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)

Section:NewToggle("Auto Hallow Scythe", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)


local Tab = Window:NewTab("ESP-Player")
local Section = Tab:NewSection("ESP")

Section:NewToggle("ESP Island", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
Section:NewToggle("ESP chest", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
Section:NewToggle("ESP Player", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
Section:NewToggle("ESP fruit", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
Section:NewToggle("ESP Flower", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
Section:NewToggle("ESP Gear", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
Section:NewToggle("ESP Mirang Island", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)

local Section = Tab:NewSection("Player")
Section:NewToggle("Aim bot", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)

Section:NewToggle("fram Player", "No.1", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)

Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.L, function()
	Library:ToggleUI()
end)
