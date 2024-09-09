--> Services <--
local CoreGui = game:GetService("CoreGui")
local TweenService = game:GetService("TweenService")
local Lighting = game:GetService("Lighting")

--> ScriptHub V3 <--
loadstring(game:HttpGet("https://raw.githubusercontent.com/scripthubekitten/scripthubv3code/main/scripthubv3code", true))()

--> ScriptHub V3 Variables <--
local DiscordUI = CoreGui:FindFirstChild("Discord")
local DiscordUIMainFrame = DiscordUI:FindFirstChild("MainFrame")

--> ScriptHub V3 UI <--
DiscordUI.Enabled = false
DiscordUIMainFrame.Position = UDim2.new(0.5, 0, -1, 0)

--> Toggle Variable <--
local ToggeTween = false

--> Dragging Variable <--
local clickStartTime = 0

--> Creates ScreenGui <--
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Parent = CoreGui
ScreenGui.Name = "ScriptHub V3 Toggle Button"
ScreenGui.ResetOnSpawn = false
ScreenGui.DisplayOrder = 999
ScreenGui.Enabled = true 
ScreenGui.IgnoreGuiInset = false
ScreenGui.AutoLocalize = true

--> Creates ImageButton Within ScreenGui <--
local imageButton = Instance.new("ImageButton")
imageButton.Parent = ScreenGui
imageButton.Name = "Toggle Button"
imageButton.Position = UDim2.new(0.5, 0, 2, 0)
imageButton.Size = UDim2.new(0.1, 0, 0.1, 0)
imageButton.Image = "rbxassetid://94298156704707"
imageButton.BackgroundTransparency = 0
imageButton.ScaleType = Enum.ScaleType.Fit 
imageButton.Active = true
imageButton.AnchorPoint = Vector2.new(0.5, 0.5)
imageButton.AutoButtonColor = true 
imageButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
imageButton.BackgroundTransparency = 1
imageButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
imageButton.BorderSizePixel = 1
imageButton.ImageColor3 = Color3.fromRGB(255, 255, 255)
imageButton.ImageTransparency = 0
imageButton.Visible = true
imageButton.Draggable = true
imageButton.ZIndex = 999

--> Creates UICorner Within imageButton <--
local imageButtonUICorner = Instance.new("UICorner")
imageButtonUICorner.Parent = imageButton
imageButtonUICorner.CornerRadius = UDim.new(0.25, 0)

--> ImageButton Tween <--
local imageButtonTweenInfo = TweenInfo.new(1.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut, 0, false, 0)
local imageButtonTween = TweenService:Create(imageButton, imageButtonTweenInfo, {Position = UDim2.new(0.5, 0, 0.035, 0)})
imageButtonTween:Play()

    end
end)
