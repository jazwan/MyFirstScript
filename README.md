![Screenshot_٢٠٢٥٠٧٢٥_٠٠١٧٠٦](https://github.com/user-attachments/assets/fcab6f97-79b1-4a14-981c-39ba8f64ae4c)
--// Notification Library
loadstring(game:HttpGet("https://pastefy.app/SsJzir8l/raw"))()
local NotificationLibrary = loadstring(game:HttpGet("https://raw.githubusercontent.com/IceMinisterq/Notification-Library/Main/Library.lua"))()
NotificationLibrary:SendNotification("Info", "واجهة إيم بوت باللون الأحمر والأسود - تصميم غزوان", 5)

local TweenService = game:GetService("TweenService")
local UserInputService = game:GetService("UserInputService")
local gui = Instance.new("ScreenGui", gethui())
gui.ResetOnSpawn = false

-- الإطار الأساسي
local frame = Instance.new("Frame", gui)
frame.Size = UDim2.new(0, 300, 0, 150)
frame.Position = UDim2.new(0.5, -150, 0.5, -75)
frame.BackgroundColor3 = Color3.fromRGB(30, 0, 0) -- أحمر غامق
frame.BorderColor3 = Color3.new(0,0,0)
frame.BorderSizePixel = 2
frame.AnchorPoint = Vector2.new(0.5, 0.5)
frame.Active = true
frame.Draggable = true

-- عنوان الواجهة
local title = Instance.new("TextLabel", frame)
title.Size = UDim2.new(1, 0, 0, 35)
title.Position = UDim2.new(0, 0, 0, 0)
title.BackgroundTransparency = 1
title.Text = "واجهة إيم بوت - تصميم غزوان"
title.TextColor3 = Color3.fromRGB(255, 0, 0)
title.Font = Enum.Font.GothamBold
title.TextSize = 20
title.TextStrokeTransparency = 0.7
title.TextStrokeColor3 = Color3.new(0,0,0)

-- زر إيم بوت
local button = Instance.new("TextButton", frame)
button.Size = UDim2.new(0.7, 0, 0, 50)
button.Position = UDim2.new(0.15, 0, 0.5, -25)
button.BackgroundColor3 = Color3.fromRGB(180, 0, 0)
button.BorderSizePixel = 0
button.Text = "إيم بوت"
button.TextColor3 = Color3.new(1,1,1)
button.Font = Enum.Font.GothamBold
button.TextSize = 24
button.AutoButtonColor = true
button.TextStrokeTransparency = 0.6
button.TextStrokeColor3 = Color3.new(0,0,0)
button.AnchorPoint = Vector2.new(0,0)

-- حقوق التصميم
local credit = Instance.new("TextLabel", frame)
credit.Size = UDim2.new(1, 0, 0, 20)
credit.Position = UDim2.new(0, 0, 1, -22)
credit.BackgroundTransparency = 1
credit.Text = "حقوق التصميم © غزوان"
credit.TextColor3 = Color3.fromRGB(255, 0, 0)
credit.Font = Enum.Font.GothamBold
credit.TextSize = 14
credit.TextStrokeTransparency = 0.8
credit.TextStrokeColor3 = Color3.new(0,0,0)
credit.TextXAlignment = Enum.TextXAlignment.Center

-- أصوات بسيطة للزر
local hoverSound = Instance.new("Sound", frame)
hoverSound.SoundId = "rbxassetid://4601634822"
hoverSound.Volume = 0.7

local clickSound = Instance.new("Sound", frame)
clickSound.SoundId = "rbxassetid://4601635211"
clickSound.Volume = 0.8

button.MouseEnter:Connect(function()
	hoverSound:Play()
end)
button.MouseButton1Click:Connect(function()
	clickSound:Play()
	-- تحميل وتشغيل سكربت الإيم بوت
	loadstring(game:HttpGet("https://pastefy.app/TXAILVzD/raw"))()
	NotificationLibrary:SendNotification("نجاح", "تم تفعيل الإيم بوت", 5)
end)
