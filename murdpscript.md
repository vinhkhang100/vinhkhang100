local haha = game.Workspace.Gems:GetDescendants()
local safePlace 





local function kill(player)
	local args = {
		[1] = player.UserId
	}
	
	game:GetService("ReplicatedStorage").Events.Weapons.KnifeSwing:FireServer(unpack(args))
end
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("murder party hax(premium)", "DarkTheme")
local Game = Window:NewTab("Game")
local MurderP = Game:NewSection("Murder Party")
local AutoF = false
local AutoFTele = false
local ExpFarm = false
local Creditse = Window:NewTab("Credits")
local Credits = Creditse:NewSection("Haha yes")
Credits:NewLabel("bianhquan12345: Tester and helper")
Credits:NewLabel("vinhkhang100: Others")
Credits:NewButton("Copy discord link", "fuck (:", function ()
	setclipboard("https://discord.gg/4PmaapereF")
end)
local value = Instance.new("NumberValue",game.Workspace)
value.Name = "CheckT"
MurderP:NewButton("Reset","ssd", function()
game.Players.LocalPlayer.character.Humanoid.Health = 0
end)
local new = Instance.new("BoolValue", game.Workspace)
local CurrentBanged
local gsa = {}
for i,v in pairs(game.Players:GetChildren()) do

table.insert(gsa, i)
i = v
end

MurderP:NewTextBox("BangPlayer", "pk", function(txt)
	CurrentBanged = txt
end)

game.Players.PlayerAdded:Connect(function()
table.clear(gsa)
for i,v in pairs(game.Players:GetChildren()) do

table.insert(gsa, i)
i = v
end
choose:Refresh(gsa)
end)
game.Players.PlayerRemoving:Connect(function()
table.clear(gsa)
for i,v in pairs(game.Players:GetChildren()) do

table.insert(gsa, i)
i = v
end
choose:Refresh(gsa)
end)
local oksee = false
MurderP:NewToggle("Bang", "ok", function(state)
    if state then
        new.Value = true
    else
        new.Value = false
    end
end)

new.Changed:Connect(function()
if new.Value == true then
repeat
wait(0.1)
game.Players.LocalPlayer.character.HumanoidRootPart.CFrame = CFrame.new(game.Players[CurrentBanged].character.HumanoidRootPart.Position)
until new.Value == false
end
end)
MurderP:NewToggle("Auto collect coins", "sdadsa", function(state)
    if state then
       AutoF = true
    else
        AutoF = false
    end
end)
game.Workspace.Time.Changed:Connect(function()
	if game.Workspace.Time.Value == 119 then
		
safePlace = Instance.new("Part",game.Workspace)
safePlace.Anchored = true
safePlace.Size = Vector3.new(6,1,6)
safePlace.CFrame = CFrame.new(game.Players.LocalPlayer.character.HumanoidRootPart.Position) + Vector3.new(0,150,0)

if AutoF == true then
	game.Players.LocalPlayer.character.HumanoidRootPart.CFrame = CFrame.new(safePlace.Position)+Vector3.new(0,4,0)
repeat
			for i,v in ipairs(game.Workspace.Gems:GetDescendants()) do
				if v.Name == "TouchInterest" then
				firetouchinterest(game.Players.LocalPlayer.Character.Head, v.Parent,0)
				wait()
				end
				end
until game.Players.LocalPlayer.MatchCurrency.Value == 15



	end
end
if AutoF == true then

end

end)
local InfJUmp = false
MurderP:NewToggle("Inf jump", "haha yes?", function(state)
    if state then
        InfJUmp = true
    else
       InfJUmp = false
    end
end)
game:GetService("UserInputService").JumpRequest:connect(function()
	if InfJUmp == true then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
end)
MurderP:NewButton("Teleport to map", "you only need this if you want to go out the safe place", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(12, 1210, 43)
end)
MurderP:NewButton("Teleport to safe place", "haha yes", function ()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(safePlace.Position) + Vector3.new(0,3,0)
end)
MurderP:NewButton("Collect coins", "this will auto collect coins for u", function()
	for i,v in ipairs(game.Workspace.Gems:GetDescendants()) do
		if v.Name == "TouchInterest" then
		firetouchinterest(game.Players.LocalPlayer.Character.Head, v.Parent,0)
		wait(0.05)
		firetouchinterest(game.Players.LocalPlayer.Character.Head, v.Parent,1)
		end
		end

end)
local inf = false

local mouse = game.Players.LocalPlayer:GetMouse()
mouse.Button1Down:Connect(function()
if inf == true then
-- R2Sv2 developed by Luckyxero

 for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
local A_1 = Vector3.new(v.Handle.Position)
local A_2 = Vector3.new(mouse.Hit.p)
local A_5 = false
local Event = game:GetService("ReplicatedStorage").Events.Weapons.GunAttack
Event:FireServer(A_1, A_2, A_5)
end
end
end)
MurderP:NewToggle("Xp Farm(team chaos only)","the exp farm is still beta", function (state)
	if state then
		ExpFarm = true
	else
		ExpFarm = false
	end
end)
game.Workspace.Time.Changed:Connect(function()
if game.Workspace.Time.Value == 119 then
		if ExpFarm == true then
		for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
			game.Players.LocalPlayer.character.Humanoid:EquipTool(v)

for i,v in pairs(game.Players:GetChildren()) do
if v.Name ~= game.Players.LocalPlayer.Name then
for is,ve in pairs(game.Players.LocalPlayer:GetChildren()) do
for dm,md in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
if ve.character["ClientKnife"] or md:FindFirstChild("ClientKnife") then


for ind,val in pairs(v:GetChildren()) do
for index,value in pairs(v.Backpack:GetChildren()) do
if #v.Backpack:GetChildren() == 0 then
repeat
game.Players.LocalPlayer.character.HumanoidRootPart.CFrame = CFrame.new(v.character.HumanoidRootPart.Position)
local vir = game:GetService("VirtualInputManager")
vir:SendMouseButtonEvent(0,0,0,true, game, 1)
wait(0.1)
until v.character.Humanoid.Health == 0
else
if value:FindFirstChild("ClientKnife") or value:FindFirstChild("ClientBow") or value:FindFirstChild("DummyBackpackItem") or val:FindFirstChild("ClientGun") or val:FindFirstChild("ClientBow") then

elseif value:FindFirstChild("ClientGun") or value:FindFirstChild("ClientLaptop") or value:FindFirstChild("ClientHat") or value:FindFirstChild("ClientMagnifyingGlass") or val:FindFirstChild("ClientGun") or val:FindFirstChild("ClientLaptop") or val:FindFirstChild("ClientHat") or val:FindFirstChild("ClientMagnifyingGlass") then
repeat
game.Players.LocalPlayer.character.HumanoidRootPart.CFrame = CFrame.new(v.character.HumanoidRootPart.Position) + Vector3.new(0,0,1)
local vir = game:GetService("VirtualInputManager")
vir:SendMouseButtonEvent(0,0,0,true,game,1)
wait(0.05)
until v.character.Humanoid.Health == 0
end
end
end
end
end
end
end
end

for i,v in pairs(game.Players:GetChildren()) do
if v.Name ~= game.Players.LocalPlayer.Name then
for is,ve in pairs(game.Players.LocalPlayer.character:GetChildren()) do
for dm,md in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
if ve["ClientKnife"] or md:FindFirstChild("ClientKnife") then


for ind,val in pairs(v:GetChildren()) do
for index,value in pairs(v.Backpack:GetChildren()) do
if #v.Backpack:GetChildren() == 0 then
repeat
game.Players.LocalPlayer.character.HumanoidRootPart.CFrame = CFrame.new(v.character.HumanoidRootPart.Position)
local vir = game:GetService("VirtualInputManager")
vir:SendMouseButtonEvent(0,0,0,true, game, 1)
wait(0.1)
until v.character.Humanoid.Health == 0
else
if value:FindFirstChild("ClientKnife") or value:FindFirstChild("ClientBow") or value:FindFirstChild("DummyBackpackItem") or val:FindFirstChild("ClientGun") or val:FindFirstChild("ClientBow") then


repeat
game.Players.LocalPlayer.character.HumanoidRootPart.CFrame = CFrame.new(v.character.HumanoidRootPart.Position) + Vector3.new(0,0,1)
local vir = game:GetService("VirtualInputManager")
vir:SendMouseButtonEvent(0,0,0,true,game,1)
wait(0.05)
until v.character.Humanoid.Health == 0
end
end
end
end
end
end
end
end
end


		end
end
end
end
	end)




local noclip = false
 game:GetService("RunService").Stepped:Connect(function()
if noclip then
    game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
end
    end)

MurderP:NewButton("Esp", "haha yes", function()

--- Tut

local esp_settings = { ---- table for esp settings 
    textsize = 8,
    colour = 255,255,255
}

local gui = Instance.new("BillboardGui")
local esp = Instance.new("TextLabel",gui) ---- new instances to make the billboard gui and the textlabel



gui.Name = "Cracked esp"; ---- properties of the esp
gui.ResetOnSpawn = false
gui.AlwaysOnTop = true;
gui.LightInfluence = 0;
gui.Size = UDim2.new(1.75, 0, 1.75, 0);
esp.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
esp.Text = ""
esp.Size = UDim2.new(0.0001, 0.00001, 0.0001, 0.00001);
esp.BorderSizePixel = 4;
esp.BorderColor3 = Color3.new(esp_settings.colour)
esp.BorderSizePixel = 0
esp.Font = "GothamSemibold"
esp.TextSize = esp_settings.textsize
esp.TextColor3 = Color3.fromRGB(esp_settings.colour)

game:GetService("RunService").RenderStepped:Connect(function() 
    for i,v in pairs (game:GetService("Players"):GetPlayers()) do
        if v ~= game:GetService("Players").LocalPlayer and v.Character.Head:FindFirstChild("Cracked esp")==nil  then
            esp.Text = "{"..v.Name.."}"
            gui:Clone().Parent = v.Character.Head
    end
end
end)

game.Players.PlayerAdded:Connect(function()

--- Tut

local esp_settings = { ---- table for esp settings 
    textsize = 8,
    colour = 255,255,255
}

local gui = Instance.new("BillboardGui")
local esp = Instance.new("TextLabel",gui) ---- new instances to make the billboard gui and the textlabel



gui.Name = "Cracked esp"; ---- properties of the esp
gui.ResetOnSpawn = false
gui.AlwaysOnTop = true;
gui.LightInfluence = 0;
gui.Size = UDim2.new(1.75, 0, 1.75, 0);
esp.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
esp.Text = ""
esp.Size = UDim2.new(0.0001, 0.00001, 0.0001, 0.00001);
esp.BorderSizePixel = 4;
esp.BorderColor3 = Color3.new(esp_settings.colour)
esp.BorderSizePixel = 0
esp.Font = "GothamSemibold"
esp.TextSize = esp_settings.textsize
esp.TextColor3 = Color3.fromRGB(esp_settings.colour)

game:GetService("RunService").RenderStepped:Connect(function() 
    for i,v in pairs (game:GetService("Players"):GetPlayers()) do
        if v ~= game:GetService("Players").LocalPlayer and v.Character.Head:FindFirstChild("Cracked esp")==nil  then
            esp.Text = "{"..v.Name.."}"
            gui:Clone().Parent = v.Character.Head
    end
end
end)
end)
end)
MurderP:NewKeybind("Toggle gui", ".", Enum.KeyCode.LeftControl, function()
	Library:ToggleUI()
end)



local SpamSwing = Instance.new("BoolValue", game.Workspace)
local SpamHat = Instance.new("BoolValue", game.Workspace)
MurderP:NewToggle("SpamSwing", ".", function(state)
    if state then
        SpamSwing.Value = true
    else
        SpamSwing.Value = false
    end
end)
MurderP:NewToggle("SpamHat", ".", function(state)
    if state then
        SpamHat.Value = true
    else
        SpamHat.Value = false
    end
end)
SpamSwing.Changed:Connect(function()
if SpamSwing.Value == true then
-- Script generated by SimpleSpy - credits to exx#9394
repeat
game:GetService("ReplicatedStorage").Events.Weapons.KnifeSwing:FireServer()
wait(0.05)
until SpamSwing.Value == false
end
end)
SpamHat.Changed:Connect(function()
if SpamHat.Value == true then
-- Script generated by SimpleSpy - credits to exx#9394
repeat

game:GetService("ReplicatedStorage").Events.Weapons.HatSwing:FireServer()
wait(0.05)
until SpamHat.Value == false
end
end)
local currentSpeed = game.Players.LocalPlayer.character.Humanoid.WalkSpeed
local currentJump = game.Players.LocalPlayer.character.Humanoid.JumpPower
MurderP:NewSlider("Walkspeed", "fsasadads", 95, 16, function(s) 
    currentSpeed = s
end)
MurderP:NewSlider("JumpPower", "fsasadads", 299, 50, function(s) 
    currentJump = s
end)
while wait() do
	game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = currentSpeed
	game.Players.LocalPlayer.Character.Humanoid.JumpPower = currentJump
end
