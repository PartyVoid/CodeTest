
	local WeaponGui = Instance.new("ScreenGui", Plr.PlayerGui)
	WeaponGui.Name = "WeaponGui"
	WeaponGui.IgnoreGuiInset = true

	local MainFrame = Instance.new("Frame", WeaponGui)
	MainFrame.Draggable = true
	MainFrame.Active = true
	MainFrame.Selectable = true
	MainFrame.Size = UDim2.new(0.25,0,0.5,0)
	MainFrame.Position = UDim2.new(0.025,0,0.25,0)
	MainFrame.BorderSizePixel = 0
	MainFrame.BackgroundColor = BrickColor.new("White")
	MainFrame.Name = "MainFrame"

	local Grid = Instance.new("UIGridLayout", MainFrame)
	Grid.CellPadding = UDim2.new(0.025, 0, 0.05, 0)
	Grid.CellSize = UDim2.new(0.23,0,0.15,0)

	local knifeFrame = Instance.new("Frame", MainFrame)
	knifeFrame.Name = "KnifeFrame"
	knifeFrame.BackgroundColor = BrickColor.new("Grey")
	knifeFrame.BorderSizePixel = 0

	local knifeButton = Instance.new("TextButton", knifeFrame)
	knifeButton.Size = UDim2.new(1,0,1,0)
	knifeButton.Text = "Knife"
	knifeButton.BackgroundTransparency = 1
	knifeButton.TextColor = BrickColor.new("Black")
	knifeButton.Font = Enum.Font.FredokaOne
	knifeButton.TextScaled = true
	knifeButton.Name = "Button"

	knifeButton.MouseButton1Click:Connect(function()
		if not Plr.Backpack:FindFirstChild("Knife_Weapon") then
			local knifeTool = script.Knife_Weapon:Clone()
			knifeTool.Parent = Plr.Backpack
		end	
	end)
