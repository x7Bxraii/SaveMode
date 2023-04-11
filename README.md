_G.Auto_Farm = false -- true / false

function totarget(p)
    local Distance2 = (p.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    local tween_s = game:service"TweenService"
    local info = TweenInfo.new(Distance2/350, Enum.EasingStyle.Linear)
    local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = p})
    tween:Play()
    if Distance2 <= 80 then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p
    end
end

function checklevel()
    local lv = game:GetService("Players").LocalPlayer.Data.Level.Value
    if lv == 1 or lv <= 9 then
        Mon = "Bandit [Lv. 5]"
        Title = "Bandit"
        QuestName = "BanditQuest1"
        QuestNumber = 1
        CFrameQuest = CFrame.new(1061.15271, 16.7367725, 1548.93018, -0.836085379, -3.89774577e-08, 0.548599303, -1.17575967e-08, 1, 5.31300408e-08, -0.548599303, 3.79710414e-08, -0.836085379)
        CFrameMon = CFrame.new(1151.11829, 16.7761021, 1599.73499, -0.999999762, 0, -0.000701809535, 0, 1, 0, 0.000701809535, 0, -0.999999762)
        CFramePuk = CFrame.new(1101.75903, 67.6758957, 1617.50391, -0.399259984, -5.24373327e-08, -0.916837752, -1.74068084e-08, 1, -4.96134582e-08, 0.916837752, -3.84945009e-09, -0.399259984)
    elseif lv == 10 or lv <= 14 then
        Mon = "Monkey [Lv. 14]"
        Title = "Monkey"
        QuestName = "JungleQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-1599.23096, 37.8653831, 153.335953, -0.0493941903, 1.29583286e-08, 0.998779356, 3.21716165e-08, 1, -1.13831318e-08, -0.998779356, 3.15700852e-08, -0.0493941903)
        CFrameMon = CFrame.new(-1479.76099, 23.195364, 106.327942, 0.96289885, 5.22265786e-10, -0.269862473, 6.59528099e-10, 1, 4.28857172e-09, 0.269862473, -4.30744285e-09, 0.96289885)
        CFramePuk = CFrame.new(-1776.32959, 61.1782455, 66.8902054, -0.912609756, -2.38546143e-08, 0.408831745, -2.14773621e-08, 1, 1.04056577e-08, -0.408831745, 7.15677129e-10, -0.912609756)
        elseif lv == 15 or lv <= 29 then
        Mon = "Gorilla [Lv. 20]"
        Title = "Gorilla"
        QuestName = "JungleQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-1599.23096, 37.8653831, 153.335953, -0.0493941903, 1.29583286e-08, 0.998779356, 3.21716165e-08, 1, -1.13831318e-08, -0.998779356, 3.15700852e-08, -0.0493941903)
        CFrameMon = CFrame.new(-1242.46655, 6.62262297, -523.166382, -0.974416733, 9.23166681e-08, -0.224748924, 9.58993027e-08, 1, -5.02435071e-09, 0.224748924, -2.64490758e-08, -0.974416733)
        CFramePuk = CFrame.new(-1133.4574, 40.8067436, -526.086792, 0.647179008, -2.76535794e-10, 0.762338042, 3.26674865e-08, 1, -2.73699801e-08, -0.762338042, 4.26169464e-08, 0.647179008)
    elseif lv == 30 or lv <= 39 then
        Mon = "Pirate [Lv. 35]"
        Title = "Pirate"
        QuestName = "BuggyQuest1"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-1140.631591796875, 4.752050399780273, 3829.557373046875)
        CFrameMon = CFrame.new(-1214.6678466796875, 4.752050399780273, 3921.6865234375)
        CFramePuk = CFrame.new(-1200.720947265625, 40.65950393676758, 3857.213134765625)
        elseif lv == 40 or lv <= 59 then
        Mon = "Brute [Lv. 45]"
        Title = "Brute"
        QuestName = "BuggyQuest1"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-1140.631591796875, 4.752050399780273, 3829.557373046875)
        CFrameMon = CFrame.new(-1155.450439453125, 14.809873580932617, 4343.56103515625)
        CFramePuk = CFrame.new(-1152.588623046875, 65.20112609863281, 4171.59619140625)
    elseif lv == 60 or lv <= 74 then
        Mon = "Desert Bandit [Lv. 60]"
        Title = "Desert Bandit"
        QuestName = "DesertQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(895.375, 6.438462734222412, 4391.236328125)
        CFrameMon = CFrame.new(947.9159545898438, 6.4496684074401855, 4480.22802734375)
        CFramePuk = CFrame.new(1032.504150390625, 27.975067138671875, 4486.28857421875)
        elseif lv == 75 or lv <= 89 then
        Mon = "Desert Officer [Lv. 70]"
        Title = "Desert Officer"
        QuestName = "DesertQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(895.375, 6.438462734222412, 4391.236328125)
        CFrameMon = CFrame.new(1611.8514404296875, 1.6109551191329956, 4358.0693359375)
        CFramePuk = CFrame.new(1607.384033203125, 9.891866683959961, 4371.90673828125)
    elseif lv == 90 or lv <= 99 then
        Mon = "Snow Bandit [Lv. 90]"
        Title = "Snow Bandit"
        QuestName = "SnowQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(1387.3765869140625, 87.27276611328125, -1297.6300048828125)
        CFrameMon = CFrame.new(1336.7840576171875, 87.27276611328125, -1407.56201171875)
        CFramePuk = CFrame.new(1266.7135009765625, 105.77224731445312, -1403.9957275390625)
        elseif lv == 100 or lv <= 119 then
        Mon = "Snowman [Lv. 100]"
        Title = "Snowman"
        QuestName = "SnowQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(1387.3765869140625, 87.27276611328125, -1297.6300048828125)
        CFrameMon = CFrame.new(1180.2354736328125, 105.83464813232422, -1504.948974609375)
        CFramePuk = CFrame.new(1219.989990234375, 138.0117950439453, -1489.3658447265625)
    elseif lv == 120 or lv <= 149 then
        Mon = "Chief Petty Officer [Lv. 120]"
        Title = "Chief Petty Officer"
        QuestName = "MarineQuest2"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-5037.7451171875, 28.65203285217285, 4324.623046875)
        CFrameMon = CFrame.new(-4676.2490234375, 20.65203285217285, 4514.68505859375)
        CFramePuk = CFrame.new(-4714.13671875, 101.17584228515625, 4575.5244140625)
    elseif lv == 150 or lv <= 174 then
        Mon = "Sky Bandit [Lv. 150]"
        Title = "Sky Bandit"
        QuestName = "SkyQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-4840.43212890625, 717.66943359375, -2620.939697265625)
        CFrameMon = CFrame.new(-4982.35009765625, 278.06671142578125, -2850.903076171875)
        CFramePuk = CFrame.new(-4992.9755859375, 345.3492431640625, -2913.34765625)
        elseif lv == 175 or lv <= 189 then
        Mon = "Dark Master [Lv. 175]"
        Title = "Dark Master"
        QuestName = "SkyQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-4840.43212890625, 717.66943359375, -2620.939697265625)
        CFrameMon = CFrame.new(-5249.826171875, 388.6519470214844, -2257.554931640625)
        CFramePuk = CFrame.new(-5225.88818359375, 429.84625244140625, -2276.978759765625)
    elseif lv == 190 or lv <= 209 then
        Mon = "Prisoner [Lv. 190]"
        Title = "Prisoner"
        QuestName = "PrisonerQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(5308.90087890625, 1.6551395654678345, 474.7144775390625)
        CFrameMon = CFrame.new(5122.390625, 1.653416633605957, 472.34649658203125)
        CFramePuk = CFrame.new(5142.0546875, 88.65245819091797, 505.8910217285156)
        elseif lv == 210 or lv <= 249 then
        Mon = "Dangerous Prisoner [Lv. 210]"
        Title = "Dangerous Prisoner"
        QuestName = "PrisonerQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(5308.90087890625, 1.6551395654678345, 474.7144775390625)
        CFrameMon = CFrame.new(5573.677734375, 1.6514381170272827, 778.7866821289062)
        CFramePuk = CFrame.new(5669.908203125, 72.65213012695312, 822.338134765625)
    elseif lv == 250 or lv <= 274 then
        Mon = "Toga Warrior [Lv. 250]"
        Title = "Toga Warrior"
        QuestName = "ColosseumQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-1579.07958984375, 7.921878337860107, -2985.86328125)
        CFrameMon = CFrame.new(-1873.09765625, 7.289072513580322, -2754.8623046875)
        CFramePuk = CFrame.new(-1966.8994140625, 49.05440139770508, -2884.71240234375)
        elseif lv == 275 or lv <= 299 then
        Mon = "Gladiator [Lv. 275]"
        Title = "Gladiator"
        QuestName = "ColosseumQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-1579.07958984375, 7.921878337860107, -2985.86328125)
        CFrameMon = CFrame.new(-1278.5670166015625, 7.442545413970947, -3276.233642578125)
        CFramePuk = CFrame.new(-1271.096435546875, 59.69337844848633, -3178.59765625)
    elseif lv == 300 or lv <= 324 then
        Mon = "Military Soldier [Lv. 300]"
        Title = "Military Soldier"
        QuestName = "MagmaQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-5314.35595703125, 12.236553192138672, 8516.2724609375)
        CFrameMon = CFrame.new(-5411.53076171875, 11.06879711151123, 8455.30078125)
        CFramePuk = CFrame.new(-5514.03369140625, 62.79969787597656, 8577.8798828125)
        elseif lv == 325 or lv <= 374 then
        Mon = "Military Spy [Lv. 325]"
        Title = "Military Spy"
        QuestName = "MagmaQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-5314.35595703125, 12.236553192138672, 8516.2724609375)
        CFrameMon = CFrame.new(-5859.20703125, 77.23063659667969, 8807.896484375)
        CFramePuk = CFrame.new(-5803.71484375, 99.15316009521484, 8787.0556640625)
    elseif lv == 375 or lv <= 399 then
        Mon = "Fishman Warrior [Lv. 375]"
        Title = "Fishman Warrior"
        QuestName = "FishmanQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(61122.44921875, 18.471633911132812, 1566.513671875)
        CFrameMon = CFrame.new(60890.3046875, 18.482818603515625, 1526.8817138671875)
        CFramePuk = CFrame.new(60875.53515625, 95.671875, 1538.6331787109375)
        elseif lv == 400 or lv <= 449 then
        Mon = "Fishman Commando [Lv. 400]"
        Title = "Fishman Commando"
        QuestName = "FishmanQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(61122.44921875, 18.471633911132812, 1566.513671875)
        CFrameMon = CFrame.new(61906.62890625, 18.482818603515625, 1448.6910400390625)
        CFramePuk = CFrame.new(61889.1640625, 75.47234344482422, 1394.8994140625)
    elseif lv == 450 or lv <= 474 then
        Mon = "God's Guard [Lv. 450]"
        Title = "God's Guard"
        QuestName = "SkyExp1Quest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-4721.849609375, 845.2769775390625, -1952.407470703125)
        CFrameMon = CFrame.new(-4705.89892578125, 845.2769775390625, -1918.1612548828125)
        CFramePuk = CFrame.new(-4634.376953125, 866.9027709960938, -1940.004638671875)
        elseif lv == 475 or lv <= 524 then
        Mon = "Shanda [Lv. 475]"
        Title = "Shanda"
        QuestName = "SkyExp1Quest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-7860.11474609375, 5545.49169921875, -380.8464050292969)
        CFrameMon = CFrame.new(-7653.63623046875, 5545.49169921875, -519.7054443359375)
        CFramePuk = CFrame.new(-7687.20849609375, 5600.8671875, -440.41326904296875)
    elseif lv == 525 or lv <= 549 then
        Mon = "Royal Squad [Lv. 525]"
        Title = "Royal Squad"
        QuestName = "SkyExp2Quest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-7904.0625, 5635.96240234375, -1412.447998046875)
        CFrameMon = CFrame.new(-7683.056640625, 5606.876953125, -1446.4793701171875)
        CFramePuk = CFrame.new(-7642.0048828125, 5637.08056640625, -1408.032470703125)
        elseif lv == 550 or lv <= 624 then
        Mon = "Royal Soldier [Lv. 550]"
        Title = "Royal Soldier"
        QuestName = "SkyExp2Quest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-7904.0625, 5635.96240234375, -1412.447998046875)
        CFrameMon = CFrame.new(-7834.43701171875, 5606.876953125, -1733.3182373046875)
        CFramePuk = CFrame.new(-7836.80859375, 5681.28955078125, -1791.0555419921875)
    elseif lv == 625 or lv <= 649 then
        Mon = "Galley Pirate [Lv. 625]"
        Title = "Galley Pirate"
        QuestName = "FountainQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(5257.51318359375, 38.501129150390625, 4050.001953125)
        CFrameMon = CFrame.new(5530.72998046875, 38.53862762451172, 3978.4111328125)
        CFramePuk = CFrame.new(5560.244140625, 106.68080139160156, 4065.46826171875)
        elseif lv == 650 or lv <= 699 then
        Mon = "Galley Captain [Lv. 650]"
        Title = "Galley Captain"
        QuestName = "FountainQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(5257.51318359375, 38.501129150390625, 4050.001953125)
        CFrameMon = CFrame.new(5673.16357421875, 46.37102508544922, 4881.63916015625)
        CFramePuk = CFrame.new(5592.3447265625, 105.80111694335938, 4821.6162109375)
    elseif lv == 700 or lv <= 724 then
        Mon = "Raider [Lv. 700]"
        Title = "Raider"
        QuestName = "Area1Quest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-427.7587585449219, 72.97052001953125, 1836.075439453125)
        CFrameMon = CFrame.new(-740.317138671875, 39.13978576660156, 2378.76025390625)
        CFramePuk = CFrame.new(-477.94854736328125, 99.898193359375, 2318.80712890625)
        elseif lv == 725 or lv <= 774 then
        Mon = "Mercenary [Lv. 725]"
        Title = "Mercenary"
        QuestName = "Area1Quest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-427.7587585449219, 72.97052001953125, 1836.075439453125)
        CFrameMon = CFrame.new(-964.3770141601562, 72.9596939086914, 1670.4215087890625)
        CFramePuk = CFrame.new(-856.9752197265625, 135.4171600341797, 1407.5870361328125)
    elseif lv == 775 or lv <= 799 then
        Mon = "Swan Pirate [Lv. 775]"
        Title = "Swan Pirate"
        QuestName = "Area2Quest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(636.956787109375, 73.07052612304688, 918.2445678710938)
        CFrameMon = CFrame.new(904.6843872070312, 72.9596939086914, 1263.237060546875)
        CFramePuk = CFrame.new(919.4708862304688, 156.1327362060547, 1186.965576171875)
        elseif lv == 800 or lv <= 874 then
        Mon = "Factory Staff [Lv. 800]"
        Title = "Factory Staff"
        QuestName = "Area2Quest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(636.956787109375, 73.07052612304688, 918.2445678710938)
        CFrameMon = CFrame.new(455.5044250488281, 72.95975494384766, 84.6566162109375)
        CFramePuk = CFrame.new(532.2526245117188, 129.19515991210938, 352.215576171875)
    elseif lv == 875 or lv <= 899 then
        Mon = "Marine Lieutenant [Lv. 875]"
        Title = "Marine Lieutenant"
        QuestName = "MarineQuest3"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-2441.427490234375, 73.01608276367188, -3217.718017578125)
        CFrameMon = CFrame.new(-2820.90283203125, 72.96611785888672, -3033.86083984375)
        CFramePuk = CFrame.new(-2956.54296875, 153.86935424804688, -3100.923583984375)
        elseif lv == 900 or lv <= 949 then
        Mon = "Marine Captain [Lv. 900]"
        Title = "Marine Captain"
        QuestName = "MarineQuest3"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-2441.427490234375, 73.01608276367188, -3217.718017578125)
        CFrameMon = CFrame.new(-1888.3226318359375, 72.96611785888672, -3325.980224609375)
        CFramePuk = CFrame.new(-1796.655517578125, 95.15141296386719, -3224.689208984375)
    elseif lv == 950 or lv <= 974 then
        Mon = "Zombie [Lv. 950]"
        Title = "Zombie"
        QuestName = "ZombieQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-5494.44873046875, 48.48011779785156, -794.482177734375)
        CFrameMon = CFrame.new(-5743.5322265625, 48.48011779785156, -735.978271484375)
        CFramePuk = CFrame.new(-5714.35009765625, 126.03197479248047, -752.2390747070312)
        elseif lv == 975 or lv <= 999 then
        Mon = "Vimpire [Lv. 975]"
        Title = "Vimpire"
        QuestName = "ZombieQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-5494.44873046875, 48.48011779785156, -794.482177734375)
        CFrameMon = CFrame.new(-6074.79638671875, 6.402699947357178, -1287.52587890625)
        CFramePuk = CFrame.new(-5922.89306640625, 41.97527313232422, -1092.051025390625)
    end
end
spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
totarget(CFrameQuest)
wait(.3)
local args = {
    [1] = "StartQuest",
    [2] = QuestName,
    [3] = QuestNumber
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        for i,v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        if v.Name == Mon and v2.Name == Mon then
            totarget(v.HumanoidRootPart.CFrame * CFrame.new(0,1,15))
            v.HumanoidRootPart.Size = Vector3.new(60,2.5,60)
            v.HumanoidRootPart.CFrame = CFrameMon
            game:GetService'VirtualUser':CaptureController()
            game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
            v2.HumanoidRootPart.CanCollide = false
            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
        end
        end
    end
                end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
    if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, Title) then
local args = {
    [1] = "AbandonQuest"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
            if not game:GetService("Workspace").Enemies:FindFirstChild(Mon) then
                totarget(CFramePuk)
            end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        if v.Name == Mon then
            if v.Humanoid.Health == 0 then
            v:Destroy()
            end
            end
            end
            end
        end)
    end
end)

