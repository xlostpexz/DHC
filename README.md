    local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/naypramx/Ui__Project/Script/XeNonUi", true))()
    local CenterHubNo1 = library:CreateWindow("Winnable Hub | DHC -- Right Control",Enum.KeyCode.RightControl)
    local Tab = CenterHubNo1:CreateTab("Main")
    local Sector1 = Tab:CreateSector("Drop Cash","left")
    Sector1:AddLabel("Credit : Winnable Hub")
        Sector1:AddButton("Copy Discord",function(t)
      setclipboard("https://discord.gg/t97DRzvVgN")
        end)

    Sector1:AddSlider("FPS CAP",1,60,160,1,function(x)
        setfpscap(x)
    end)

    Sector1:AddToggle("Drop Cash [Bank]",false,function(t)
       _G.Bank = t
       _G.DropCash = t
       _G.Freeze = t
    end)
    
    Sector1:AddToggle("Drop Cash [Cub]",false,function(t)
       _G.Cub = t
       _G.DropCash = t
       _G.Freeze = t
    end)
    
    Sector1:AddToggle("Drop Cash [Cub]",false,function(t)
       _G.ADMINBASE = t
       _G.DropCash = t
       _G.Freeze = t
    end)
    
    Sector1:AddToggle("White Screen",false,function(t)
        _G.WSCR = t
    end)

    spawn(function()
       game:GetService("RunService").RenderStepped:Connect(function()
        pcall(function()
            if _G.Bank then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-378.162689, 28.1529045, -283.689117, 0.987646401, 7.94339883e-08, -0.156699002, -9.65024753e-08, 1, -1.01317404e-07, 0.156699002, 1.15187611e-07, 0.987646401)
            end
        end)
       end)
    end)
    
    spawn(function()
       game:GetService("RunService").RenderStepped:Connect(function()
        pcall(function()
            if _G.Cub then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-263.700104, 0.881493032, -372.321228, -0.999921203, 3.95413835e-08, 0.0125545431, 4.06696934e-08, 1, 8.96172097e-08, -0.0125545431, 9.01207358e-08, -0.999921203)
            end
        end)
       end)
    end)
    
    spawn(function()
       game:GetService("RunService").RenderStepped:Connect(function()
        pcall(function()
            if _G.ADMINBASE then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-868.93634, -31.2300167, -589.579468, 0.98762691, 3.08274366e-08, -0.156821907, -5.46884174e-08, 1, -1.4783852e-07, 0.156821907, 1.54585635e-07, 0.98762691)
            end
        end)
       end)
    end)
    
    spawn(function()
       game:GetService("RunService").RenderStepped:Connect(function()
        pcall(function()
            if _G.DropCash then
                wait(1)
local args = {
    [1] = "DropMoney",
    [2] = "10000"
}

game:GetService("ReplicatedStorage").MainEvent:FireServer(unpack(args))

            end
        end)
       end)
    end)
    
        spawn(function()
       game:GetService("RunService").RenderStepped:Connect(function()
        pcall(function()
            if _G.Freeze then
                wait(0.5)
                game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true
            elseif _G.Freeze == false   then
                game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
            end
        end)
       end)
        end)
        
        spawn(function()
       game:GetService("RunService").RenderStepped:Connect(function()
        pcall(function()
            if _G.WSCR then
    game.RunService:Set3dRenderingEnabled(false)
elseif _G.WSCR == false then
   game.RunService:Set3dRenderingEnabled(true)
        end
        end)
       end)
        end)
