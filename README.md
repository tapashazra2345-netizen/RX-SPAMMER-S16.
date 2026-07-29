local function cN(t)
    pcall(function()
        local s = game:GetService("TextChatService")
        if s.ChatVersion == Enum.ChatVersion.TextChatService then
            local c = s.TextChannels:FindFirstChild("RBXGeneral")
            if c then c:SendAsync(t) end
        else
            game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(t, "All")
        end
    end)
end

local function gP()
    local s, t = pcall(function() return gethui() end)
    if s and t then return t end
    s, t = pcall(function() return game:GetService("CoreGui") end)
    if s and t then return t end
    return game.Players.LocalPlayer:WaitForChild("PlayerGui")
end

local sg = Instance.new("ScreenGui")
sg.Name = "RX_S16"
sg.ResetOnSpawn = false
sg.Parent = gP()
for _, v in pairs(gP():GetChildren()) do
    if (v.Name == "RX_S16") and v ~= sg then v:Destroy() end
end

-- ===== LOADING SCREEN (RX SPAMMER S16) =====
local lF = Instance.new("Frame")
lF.Size = UDim2.new(0, 300, 0, 100)
lF.Position = UDim2.new(0.5, -150, 0.5, -50)
lF.BackgroundColor3 = Color3.fromRGB(10, 10, 20)
lF.BorderSizePixel = 2
lF.BorderColor3 = Color3.fromRGB(0, 120, 255)
lF.Parent = sg

local lc = Instance.new("UICorner")
lc.CornerRadius = UDim.new(0, 8)
lc.Parent = lF

local lt = Instance.new("TextLabel")
lt.Size = UDim2.new(1, 0, 0, 30)
lt.Position = UDim2.new(0, 0, 0, 10)
lt.BackgroundTransparency = 1
lt.Text = "RX SPAMMER S16"          -- changed
lt.TextColor3 = Color3.fromRGB(0, 120, 255)
lt.TextSize = 18
lt.Font = Enum.Font.GothamBold
lt.Parent = lF

local ls = Instance.new("TextLabel")
ls.Size = UDim2.new(1, 0, 0, 20)
ls.Position = UDim2.new(0, 0, 0, 35)
ls.BackgroundTransparency = 1
ls.Text = "INITIALIZING SYSTEM..."   -- changed (matches S16 feel)
ls.TextColor3 = Color3.fromRGB(200, 200, 200)
ls.TextSize = 12
ls.Font = Enum.Font.Gotham
ls.Parent = lF

local lb = Instance.new("Frame")
lb.Size = UDim2.new(0.8, 0, 0, 6)
lb.Position = UDim2.new(0.1, 0, 0, 65)
lb.BackgroundColor3 = Color3.fromRGB(20, 20, 40)
lb.BorderSizePixel = 0
lb.Parent = lF

local lf = Instance.new("Frame")
lf.Size = UDim2.new(0, 0, 1, 0)
lf.BackgroundColor3 = Color3.fromRGB(0, 120, 255)
lf.BorderSizePixel = 0
lf.Parent = lb

-- ===== MAIN WINDOW =====
local f = Instance.new("Frame")
f.Size = UDim2.new(0, 420, 0, 195)
f.Position = UDim2.new(0.5, -210, 0.4, -98)
f.BackgroundColor3 = Color3.fromRGB(10, 10, 20)
f.BorderSizePixel = 2
f.BorderColor3 = Color3.fromRGB(0, 120, 255)
f.Draggable = true
f.Active = true
f.Visible = false
f.Parent = sg

local fc = Instance.new("UICorner")
fc.CornerRadius = UDim.new(0, 6)
fc.Parent = f

local tb = Instance.new("Frame")
tb.Size = UDim2.new(1, 0, 0, 32)
tb.BackgroundColor3 = Color3.fromRGB(15, 15, 18)
tb.BorderSizePixel = 0
tb.Parent = f

local tl = Instance.new("TextLabel")
tl.Size = UDim2.new(1, -40, 1, 0)
tl.Position = UDim2.new(0, 15, 0, 0)
tl.BackgroundTransparency = 1
tl.Text = "RX SPAMMER S16 | SUMIT & RYAN"   -- already S16
tl.TextColor3 = Color3.fromRGB(0, 120, 255)
tl.TextSize = 13
tl.Font = Enum.Font.GothamBold
tl.TextXAlignment = Enum.TextXAlignment.Left
tl.Parent = tb

local mB = Instance.new("TextButton")
mB.Size = UDim2.new(0, 30, 0, 30)
mB.Position = UDim2.new(1, -35, 0, 1)
mB.BackgroundColor3 = Color3.fromRGB(20, 20, 25)
mB.TextColor3 = Color3.new(1, 1, 1)
mB.Text = "_"
mB.TextSize = 16
mB.Font = Enum.Font.GothamBold
mB.BorderSizePixel = 0
mB.Parent = tb

getgenv().Target = ""
getgenv().Symbol = "@"
getgenv().Count = 160
getgenv().Delay = 3.0
getgenv().Enabled = false

local ms = {
    "TMX MARE RYXN AND SUMIT PAPA",
    "TMX MEH ROAD ROLLER",
    "TMX MARE VIYAY THALAPATHY",
    "TMX MARE WILD GORILA",
    "TMX MARE PHANTER",
    "TMX MEH OBSIDIAN"
}
local cM = 1
local y = 40

local function aF(l, d, cb)
    local la = Instance.new("TextLabel")
    la.Size = UDim2.new(0, 80, 0, 20)
    la.Position = UDim2.new(0, 15, 0, y)
    la.BackgroundTransparency = 1
    la.Text = l
    la.TextColor3 = Color3.new(1, 1, 1)
    la.TextSize = 11
    la.Font = Enum.Font.Gotham
    la.TextXAlignment = Enum.TextXAlignment.Left
    la.Parent = f

    local b = Instance.new("TextBox")
    b.Size = UDim2.new(0, 140, 0, 28)
    b.Position = UDim2.new(0, 85, 0, y - 4)
    b.Text = tostring(d)
    b.BackgroundColor3 = Color3.fromRGB(20, 20, 40)
    b.TextColor3 = Color3.new(1, 1, 1)
    b.TextSize = 12
    b.Font = Enum.Font.Gotham
    b.BorderSizePixel = 1
    b.BorderColor3 = Color3.fromRGB(60, 60, 70)
    b.Parent = f
    b.FocusLost:Connect(function()
        cb(b.Text)
    end)
    y = y + 35
end

aF("ENEMY:", getgenv().Target, function(v) getgenv().Target = v end)
aF("PREFIX:", getgenv().Symbol, function(v) getgenv().Symbol = v end)
aF("COUNT:", getgenv().Count, function(v) getgenv().Count = tonumber(v) or 160 end)
aF("DELAY:", getgenv().Delay, function(v) getgenv().Delay = tonumber(v) or 3.0 end)

local sB = Instance.new("TextButton")
sB.Size = UDim2.new(0, 130, 0, 100)
sB.Position = UDim2.new(1, -155, 0, 60)
sB.BackgroundColor3 = Color3.fromRGB(0, 120, 255)
sB.Text = "OFF"
sB.TextColor3 = Color3.new(1, 1, 1)
sB.TextSize = 20
sB.Font = Enum.Font.GothamBold
sB.BorderSizePixel = 1
sB.BorderColor3 = Color3.fromRGB(60, 60, 70)
sB.Parent = f

local st = Instance.new("TextLabel")
st.Size = UDim2.new(0, 200, 0, 16)
st.Position = UDim2.new(0, 15, 1, -22)
st.BackgroundTransparency = 1
st.TextColor3 = Color3.fromRGB(150, 150, 150)
st.Text = "Ready | SUMIT & RYAN"
st.TextSize = 10
st.Font = Enum.Font.Gotham
st.TextXAlignment = Enum.TextXAlignment.Left
st.Parent = f

sB.MouseButton1Click:Connect(function()
    getgenv().Enabled = not getgenv().Enabled
    sB.Text = getgenv().Enabled and "ON" or "OFF"
    sB.BackgroundColor3 = getgenv().Enabled and Color3.fromRGB(0, 200, 100) or Color3.fromRGB(0, 120, 255)
    st.Text = getgenv().Enabled and "● SENDING..." or "● Stopped | SUMIT & RYAN"
    st.TextColor3 = getgenv().Enabled and Color3.fromRGB(0, 200, 100) or Color3.fromRGB(150, 150, 150)
end)

local fl = Instance.new("TextButton")
fl.Size = UDim2.new(0, 45, 0, 45)
fl.Position = UDim2.new(0, 10, 0.5, -22)
fl.BackgroundColor3 = Color3.fromRGB(0, 120, 255)
fl.Text = "S16"                    -- changed from "RX"
fl.TextColor3 = Color3.new(1, 1, 1)
fl.TextSize = 14
fl.Font = Enum.Font.GothamBold
fl.Visible = false
fl.BorderSizePixel = 0
fl.Parent = sg

local rc = Instance.new("UICorner")
rc.CornerRadius = UDim.new(0, 8)
rc.Parent = fl

mB.MouseButton1Click:Connect(function()
    f.Visible = false
    fl.Visible = true
end)

fl.MouseButton1Click:Connect(function()
    f.Visible = true
    fl.Visible = false
end)

task.spawn(function()
    while true do
        if getgenv().Enabled and #ms > 0 then
            local m = ms[cM]
            if m and m ~= "" then
                local p = string.rep(getgenv().Symbol, getgenv().Count) .. " " ..
                          (getgenv().Target ~= "" and "[" .. getgenv().Target .. "] " or "") .. m
                cN(p)
            end
            cM = (cM % #ms) + 1
        end
        task.wait(getgenv().Delay)
    end
end)

-- Loading animation
coroutine.wrap(function()
    for i = 1, 50 do
        lf.Size = UDim2.new(i / 50, 0, 1, 0)
        task.wait(0.04)
    end
    for i = 0, 1, 0.05 do
        lF.BackgroundTransparency = i
        lt.TextTransparency = i
        ls.TextTransparency = i
        lb.BackgroundTransparency = i
        lf.BackgroundTransparency = i
        task.wait(0.04)
    end
    lF:Destroy()
    f.Visible = true
    task.wait(0.5)
    cN("RX SPAMMER S16 LOADED ✅")
end)()
