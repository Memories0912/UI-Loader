# HIRIMI LIBRARY
```lua
-- Loader
local Loader = loadstring(game:HttpGet("https://raw.githubusercontent.com/Memories0912/UI-Loader/refs/heads/main/Source.lua"))()
-- Make Gui
local HirimiLib = Loader:MakeGui({
	Name = "Hirimi Library",
	Description = "! DestroyerX",
	Size = UDim2.new(0, 500, 0, 400)
})
-- Gui Function
-- HirimiLib:DestroyGui()
-- Tab
local Tab1 = HirimiLib:CreateTab({Name = "Main", Icon = "rbxassetid://7733960981"})
local Tab2 = HirimiLib:CreateTab({Name = "Setting", Icon = "rbxassetid://7734053495"})
-- Section
local Section = Tab1:AddSection("Setting Farm")
local Section2 = Tab2:AddSection("Setting")
-- Paragraph
local Paragraph = Section:AddParagraph({
	Title = "Paragraph",
	Content = "This is a Paragraph"
})
-- Paragraph Function
Paragraph:Set({
	Title = "Paragraph",
	Content = "This is a Paragraph"
})
-- Toggle
local Toggle = Section:AddToggle({Title = "Toggle", Content = "This is a Toggle", Default = false,
	Callback = function(Value) 
		print(Value)
	end
})
-- Toggle Function
Toggle:Set(false)
-- Button
local Button = Section:AddButton({Title = "Button", Content = "This is a Button", Icon = "rbxassetid://16932740082",
	Callback = function()
		print("Button Clicked!")
	end
})
-- Slider
local Slider = Section:AddSlider({Title = "Slider", Content = "This is a Slider", Min = 0, Max = 100, Increment = 1, Default = 30,
	Callback = function(Value) 
		print(Value)
	end
})
-- Slider Function
Slider:Set(30)
-- TextInput
local Input = Section:AddInput({Title = "Input", Content = "This is a Input",
	Callback = function(Value) 
		print(Value)
	end
})
-- TextInput Function
Input:Set("Input TextBox")
-- Dropdown
local Dropdown = Section:AddDropdown({Title = "Dropdown", Content = "This is a Dropdown", Multi = false, Options = {"Option 1", "Option 2"}, Default = {"Option 1"},
	Callback = function(Value)
		print(Value)
	end
})
-- Dropdown Functions
Dropdown:Set({"Option 1"})
Dropdown:AddOption("Option 3")
Dropdown:Clear()
Dropdown:Refresh({"Option 1", "Option 2"}, {"Option 1"})
-- Notify
local Notify = Loader:MakeNotify({Title = "Hirimi Library", Content = "My UI better than Deep Voice", Time = 1, Delay = 5})
```
