if game.PlaceId == 85896571713843 then
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/jensonhirst/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "Sigma Bubble",IntroEnabled = false, HidePremium = true, SaveConfig = true, ConfigFolder = "OrionTest"})

-- Values
_G.autoGum = true
_G.autoSellGum = true
_G.autoHatch = true
_G.autoMultiHatch = true
_G.selectEgg = "Common Egg"
_G.autoEquipBest = true
_G.autoVoidChest = true
_G.autoGiantChest = true


-- Functions
function autoGum()
while _G.autoGum == true do
game:GetService("ReplicatedStorage").Shared.Framework.Network.Remote.Event:FireServer("BlowBubble")
wait(.1)
end
end

function autoSellGum()
while _G.autoSellGum == true do
game:GetService("ReplicatedStorage").Shared.Framework.Network.Remote.Event:FireServer("SellBubble")
wait(.1)
end
end

function autoHatch()
 while _G.autoHatch == true do
      game:GetService("ReplicatedStorage").Shared.Framework.Network.Remote.Event:FireServer("HatchEgg",_G.selectEgg,1)
      wait(1)
      end
end

function autoMultiHatch()
while _G.autoMultiHatch == true do
game:GetService("ReplicatedStorage").Shared.Framework.Network.Remote.Event:FireServer("HatchEgg",_G.selectEgg,99)
wait(1)
end
end

function autoEquipBest()
while _G.autoEquipBest == true do
game:GetService("ReplicatedStorage").Shared.Framework.Network.Remote.Event:FireServer("EquipBestPets")
wait(30)
end
end

function autoGiantChest()
while _G.autoGiantChest == true do
game:GetService("ReplicatedStorage").Shared.Framework.Network.Remote.Event:FireServer("ClaimChest","Giant Chest")
wait(900)
end
end

function autoVoidChest()
while _G.autoVoidChest == true do
game:GetService("ReplicatedStorage").Shared.Framework.Network.Remote.Event:FireServer("ClaimChest","Void Chest")
wait(2400)
end
end








-- Tabs

local FarmTab = Window:MakeTab({
	Name = "Auto Farm",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local EggTab = Window:MakeTab({
	Name = "Eggs",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local MiscTab = Window:MakeTab({
	Name = "Misc",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})


-- Toggles


local Section = FarmTab:AddSection({
	Name = "🍬 Auto Farm"
})

FarmTab:AddToggle({
	Name = "Auto Gum",
	Default = false,
	Callback = function(Value)
		_G.autoGum = Value
        autoGum()
	end    
})

FarmTab:AddToggle({
	Name = "Auto Sell",
	Default = false,
	Callback = function(Value)
		_G.autoSellGum = Value
        autoSellGum()
	end    
})

local Section = FarmTab:AddSection({
	Name = "📦 Auto Open Chests"
})

FarmTab:AddToggle({
	Name = "Auto Giant Chest",
	Default = false,
	Callback = function(Value)
		_G.autoGiantChest = Value
		autoGiantChest()
	end    
})

FarmTab:AddToggle({
	Name = "Auto Void Chest",
	Default = false,
	Callback = function(Value)
		_G.autoVoidChest = Value
		autoVoidChest()
	end    
})

local Section = EggTab:AddSection({
	Name = "🥚 Auto Hatch Eggs"
})

EggTab:AddToggle({
	Name = "Auto Hatch",
	Default = false,
	Callback = function(Value)
        _G.autoHatch = Value
        autoHatch()
	end    
})

EggTab:AddToggle({
	Name = "Auto Multi Hatch",
	Default = false,
	Callback = function(Value)
        _G.autoMultiHatch = Value
        autoMultiHatch()
	end    
})

MiscTab:AddToggle({
	Name = "Auto Equip Best Pets",
	Default = false,
	Callback = function(Value)
        _G.autoEquipBest = Value
        autoEquipBest()
	end    
})

-- Dropdown

EggTab:AddDropdown({
	Name = "Select egg",
	Default = "",
	Options = {"Common Egg", "Spotted Egg", "Iceshard Egg", "Spikey Egg", "Magma Egg", "Crystal Egg", "Lunar Egg", "Void Egg", "Hell Egg", "Nightmare Egg", "Rainbow Egg", "Infinity Egg"},
	Callback = function(Value)
		_G.selectEgg = Value
        print(_G.selectEgg)
	end    
})









end
OrionLib:Init()
