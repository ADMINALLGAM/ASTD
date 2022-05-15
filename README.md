local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/naypramx/Ui__Project/Script/XeNonUi", true))()
library:CreateWatermark("Clown HUB No.1")
local CenterHubNo1 = library:CreateWindow("Clown HUB",Enum.KeyCode.RightControl)
    local Tab = CenterHubNo1:CreateTab("Main")
    local Sector1 = Tab:CreateSector("Farming","left")
    Sector1:AddLabel("Farm")
    
    
    Sector1:AddToggle("Auto Farm",false,function(state)
        
        _G.Auto = state
while _G.Auto do wait()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-102.98844146728516, 1387.056884765625, 842.9007568359375)
        wait(2)
        
        CFrameQuest = CFrame.new(-91.49962615966797, 1388.0064697265625, 847.6353149414062) ------ ใส CFrame ตรงw(-90.15608215332031, 1388.0064697265625, 848.3006591796875)
         
         
         function TP(P)
           local Distance = (P.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude -- จุดที่จะไป Position Only
           local Speed = 50 -- ความเร็วของมึง
           tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear)
           tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = P})
           tween:Play()
         end
         
        
        
        
        TP(CFrameQuest)
        if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
        wait(.1)
    end



--เลือกด่าน
local args = {
    [1] = "InfLevel",
    [2] = "-1.7",
    [3] = false
}

game:GetService("ReplicatedStorage").Remotes.Input:FireServer(unpack(args))
--------------------

-- Auto start

local args = {
    [1] = "Start"
}

game:GetService("ReplicatedStorage").Remotes.Input:FireServer(unpack(args))


repeat wait() until game:IsLoaded()
-----เลือกโหมด
local args = {
    [1] = "VoteGameMode",
    [2] = "Normal" ----- Normal,Extreme
}

game:GetService("ReplicatedStorage").Remotes.Input:FireServer(unpack(args))
wait(1)

------EXP IV

local args = {
    [1] = "Summon",
    [2] = {
        ["Rotation"] = 0,
        ["cframe"] = CFrame.new(-261.7045593261719, 35.54701232910156, -217.45498657226562) * CFrame.Angles(-0, 0, -0),
        ["Unit"] = "EXP IV"
    }
}

game:GetService("ReplicatedStorage").Remotes.Input:FireServer(unpack(args))

wait(1)
--------------------------------------------
end
end)


Sector1:AddLabel("Misc")
Sector1:AddButton("Turn on/off auto skip",function()
    local args = {
    [1] = "AutoSkipWaves_CHANGE"
}

game:GetService("ReplicatedStorage").Remotes.Input:FireServer(unpack(args))
end)
