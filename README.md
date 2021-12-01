local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local colors = {
    SchemeColor = Color3.fromRGB(0,171,255),
    Background = Color3.fromRGB(35,35,35),
    Header = Color3.fromRGB(30,30,30),
    TextColor = Color3.fromRGB(255,255,255),
    ElementColor = Color3.fromRGB(20, 20, 20)
}
local Window = Library.CreateLib("KOKO HUB", colors)
--Tab Main
local Tab = Window:NewTab("Main")
local b = Tab:NewSection("Main")

b:NewToggle("AutoFarm","",function(a)
    autofarm = a
end)
spawn(function()
    while wait() do
        if autofarm then
 
local Event = game:GetService("Workspace")["Donut_Manx2"].Starter.RemoteClick
Event:FireServer()
 
local Event = game:GetService("ReplicatedStorage").Events.Clicked
Event:FireServer()
 
local Event = game:GetService("ReplicatedStorage").Events.UpdateData
Event:InvokeServer()

local Event = game:GetService("ReplicatedStorage").Events.Sell
Event:FireServer()

        end
    end
end)
