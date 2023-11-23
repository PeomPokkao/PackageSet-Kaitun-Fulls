game.StarterGui:SetCore("SendNotification", {
    Icon = "rbxassetid://11915607895"; -- ใส่หน้าพ่อมึงมึง
    Title = "Upper Cut Hub", 
    Text = "loading",
})

_G.Team = "Pirate"


if game:GetService("Players").LocalPlayer.PlayerGui.Main:FindFirstChild("ChooseTeam") then
	repeat wait()
		if game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("Main").ChooseTeam.Visible == true then
			if _G.Team == "Pirate" then
				for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.Activated)) do                                                                                                
					v.Function()
				end
			elseif _G.Team == "Marine" then
				for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Marines.Frame.ViewportFrame.TextButton.Activated)) do                                                                                                
					v.Function()
				end
			else
				for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.Activated)) do                                                                                                
					v.Function()
				end
			end
		end
	until game.Players.LocalPlayer.Team ~= nil and game:IsLoaded()
end

local SimpleUi = loadstring(game:HttpGet("https://raw.githubusercontent.com/naypramx/Ui__Project/Script/SimpleUi"))()
local Main = SimpleUi:create('Ents Hub')
local Menu = Main:Menu('Ents hub')
local Page = Menu:Page()
local Page2 = Menu:Page()

-- Logo Change --
game:GetService("CoreGui").Simlib.Mainsceen.Topbar.ImageLabel.Image = "http://www.roblox.com/asset/?id=7040391851"
-- Logo Change --

-- Head Name -- \\ Bit
for __,head in pairs(game:GetService("CoreGui").Simlib.Mainsceen.Topbar:GetDescendants()) do
    if head:IsA"TextLabel" then
        if head.Text == "Ents" then
            head.Text = "Ents"
        end
    end
end
--Head Name \\ EiEi

Page:Label('Ents Hub')
Page:Button('Part Neon',false,function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/PeomPokkao/Partneon/main/README.md"))()
end)
Page:Toggle('Open is Buy Legendarysword until false',false,false,false,function(value)
    _G.Buy = value

spawn(function()
if _G.Buy == true then
repeat wait()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer","1")
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer","2")
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer","3")
until _G.Buy == false
end
end)
end)
Page:Button('Fire Punch',false,function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/PeomPokkao/FirePunch/main/README.md"))()
end)
Page:Button('Fake Kroblox',false,function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/PeomPokkao/FakeKroblox/main/README.md"))()
end)
Page:Button('Run Script Gui Noclip',false,function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/PeomPokkao/Noclip/main/README.md"))()
end)

Page:Button('Run Script Kaitun Switch Hub',false,function()
    https://raw.githubusercontent.com/PeomPokkao/Kaitun-SwitchHub-SeriesM/main/README.md
end)

-- ColorChanger
for k,v in pairs(game:GetService("CoreGui").Simlib:GetDescendants()) do
    if v:IsA"TextButton" then
        if v.BackgroundColor3 == Color3.fromRGB(68, 187, 165) then
            v.BackgroundColor3 = Color3.fromRGB(255,255,255)
        end
    end
end
for k,v in pairs(game:GetService("CoreGui").Simlib:GetDescendants()) do
    if v:IsA"TextLabel" then
        if v.TextColor3 == Color3.fromRGB(68, 187, 165) then
            v.TextColor3 = Color3.fromRGB(255,255,255)
        end
    end
end
for k,v in pairs(game:GetService("CoreGui").Simlib:GetDescendants()) do
    if v:IsA"TextLabel" then
        if v.TextColor3 == Color3.fromRGB(33, 133, 113) then
            v.TextColor3 = Color3.fromRGB(255,255,255)
        end
    end
end
