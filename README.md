local function D(s)return s:reverse()end

local function c(t)pcall(function()
    local s=game:GetService(D("ecivreStahCtxeT"))
    if s.ChatVersion==Enum.ChatVersion.TextChatService then
        local c=s.TextChannels:FindFirstChild(D("lareneGXBR"))
        if c then c:SendAsync(t)end
    else
        game:GetService(D("egaruotSdetacilpeR")):FindFirstChild(D("stnevEtahtChC".."metsyS".."tluaF".."eD")):FindFirstChild(D("tseuqeRge".."asseM".."yaS")):FireServer(t,D("llA"))
    end
end)end

local function p()
    local a,b=pcall(function()return game:GetService(D("iuGraeroC"))end)
    if a and b then return b end
    return game.Players.LocalPlayer:WaitForChild(D("iuGrareyalP"))
end

local sg=Instance.new(D("iuGraerneecS"))
sg.Name=D("61S_XR")
sg.ResetOnSpawn=false
sg.Parent=p()
for _,v in pairs(p():GetChildren())do
    if(v.Name==D("61S_XR"))and v~=sg then v:Destroy()end
end

local lF=Instance.new(D("emarF"))
lF.Size=UDim2.new(0,300,0,100)
lF.Position=UDim2.new(0.5,-150,0.5,-50)
lF.BackgroundColor3=Color3.fromRGB(10,10,20)
lF.BorderSizePixel=2
lF.BorderColor3=Color3.fromRGB(0,120,255)
lF.Parent=sg

local lc=Instance.new(D("renroC IU"))
lc.CornerRadius=UDim.new(0,8)
lc.Parent=lF

local lt=Instance.new(D("lebaLtxeT"))
lt.Size=UDim2.new(1,0,0,30)
lt.Position=UDim2.new(0,0,0,10)
lt.BackgroundTransparency=1
lt.Text=D("61S REMMAPS XR")
lt.TextColor3=Color3.fromRGB(0,120,255)
lt.TextSize=18
lt.Font=Enum.Font.GothamBold
lt.Parent=lF

local ls=Instance.new(D("lebaLtxeT"))
ls.Size=UDim2.new(1,0,0,20)
ls.Position=UDim2.new(0,0,0,35)
ls.BackgroundTransparency=1
ls.Text=D("...METSYS GNIZILAITINI")
ls.TextColor3=Color3.fromRGB(200,200,200)
ls.TextSize=12
ls.Font=Enum.Font.Gotham
ls.Parent=lF

local lb=Instance.new(D("emarF"))
lb.Size=UDim2.new(0.8,0,0,6)
lb.Position=UDim2.new(0.1,0,0,65)
lb.BackgroundColor3=Color3.fromRGB(20,20,40)
lb.BorderSizePixel=0
lb.Parent=lF

local lf=Instance.new(D("emarF"))
lf.Size=UDim2.new(0,0,1,0)
lf.BackgroundColor3=Color3.fromRGB(0,120,255)
lf.BorderSizePixel=0
lf.Parent=lb

local f=Instance.new(D("emarF"))
f.Size=UDim2.new(0,420,0,195)
f.Position=UDim2.new(0.5,-210,0.4,-98)
f.BackgroundColor3=Color3.fromRGB(10,10,20)
f.BorderSizePixel=2
f.BorderColor3=Color3.fromRGB(0,120,255)
f.Draggable=true
f.Active=true
f.Visible=false
f.Parent=sg

local fc=Instance.new(D("renroC IU"))
fc.CornerRadius=UDim.new(0,6)
fc.Parent=f

local tb=Instance.new(D("emarF"))
tb.Size=UDim2.new(1,0,0,32)
tb.BackgroundColor3=Color3.fromRGB(15,15,18)
tb.BorderSizePixel=0
tb.Parent=f

local tl=Instance.new(D("lebaLtxeT"))
tl.Size=UDim2.new(1,-40,1,0)
tl.Position=UDim2.new(0,15,0,0)
tl.BackgroundTransparency=1
tl.Text=D("NAYR & TIMUS | 61S REMMAPS XR")
tl.TextColor3=Color3.fromRGB(0,120,255)
tl.TextSize=13
tl.Font=Enum.Font.GothamBold
tl.TextXAlignment=Enum.TextXAlignment.Left
tl.Parent=tb

local mB=Instance.new(D("nottuBtxeT"))
mB.Size=UDim2.new(0,30,0,30)
mB.Position=UDim2.new(1,-35,0,1)
mB.BackgroundColor3=Color3.fromRGB(20,20,25)
mB.TextColor3=Color3.new(1,1,1)
mB.Text=D("_")
mB.TextSize=16
mB.Font=Enum.Font.GothamBold
mB.BorderSizePixel=0
mB.Parent=tb

getgenv()._a=""
getgenv()._b="@"
getgenv()._c=150
getgenv()._d=5.0
getgenv()._e=false

local ms="TMX MARE RYXN AND SUMIT PAPA|TMX MEH ROAD ROLLER|TMX MARE VIYAY THALAPATHY|TMX MARE WILD GORILA|TMX MARE PHANTER|TMX MEH OBSIDIAN"
local ml={}for w in ms:gmatch("[^|]+")do table.insert(ml,w)end
local ci=1
local y=40

local function aF(l,d,cb)
    local la=Instance.new(D("lebaLtxeT"))
    la.Size=UDim2.new(0,80,0,20)
    la.Position=UDim2.new(0,15,0,y)
    la.BackgroundTransparency=1
    la.Text=l
    la.TextColor3=Color3.new(1,1,1)
    la.TextSize=11
    la.Font=Enum.Font.Gotham
    la.TextXAlignment=Enum.TextXAlignment.Left
    la.Parent=f

    local b=Instance.new(D("xoBtxeT"))
    b.Size=UDim2.new(0,140,0,28)
    b.Position=UDim2.new(0,85,0,y-4)
    b.Text=tostring(d)
    b.BackgroundColor3=Color3.fromRGB(20,20,40)
    b.TextColor3=Color3.new(1,1,1)
    b.TextSize=12
    b.Font=Enum.Font.Gotham
    b.BorderSizePixel=1
    b.BorderColor3=Color3.fromRGB(60,60,70)
    b.Parent=f
    b.FocusLost:Connect(function()cb(b.Text)end)
    y=y+35
end

aF(D(":YMENE"),getgenv()._a,function(v)getgenv()._a=v end)
aF(D(":XIFERP"),getgenv()._b,function(v)getgenv()._b=v end)
aF(D(":TNUOC"),getgenv()._c,function(v)getgenv()._c=tonumber(v)or 150 end)
aF(D(":YALED"),getgenv()._d,function(v)getgenv()._d=tonumber(v)or 5.0 end)

local sB=Instance.new(D("nottuBtxeT"))
sB.Size=UDim2.new(0,130,0,100)
sB.Position=UDim2.new(1,-155,0,60)
sB.BackgroundColor3=Color3.fromRGB(0,120,255)
sB.Text=D("tratS")
sB.TextColor3=Color3.new(1,1,1)
sB.TextSize=20
sB.Font=Enum.Font.GothamBold
sB.BorderSizePixel=1
sB.BorderColor3=Color3.fromRGB(60,60,70)
sB.Parent=f

local st=Instance.new(D("lebaLtxeT"))
st.Size=UDim2.new(0,200,0,16)
st.Position=UDim2.new(0,15,1,-22)
st.BackgroundTransparency=1
st.TextColor3=Color3.fromRGB(150,150,150)
st.Text=D("eldI")
st.TextSize=10
st.Font=Enum.Font.Gotham
st.TextXAlignment=Enum.TextXAlignment.Left
st.Parent=f

sB.MouseButton1Click:Connect(function()
    getgenv()._e=not getgenv()._e
    sB.Text=getgenv()._e and D("potS") or D("tratS")
    st.Text=getgenv()._e and D("evitcA") or D("eldI")
end)

local fl=Instance.new(D("nottuBtxeT"))
fl.Size=UDim2.new(0,45,0,45)
fl.Position=UDim2.new(0,10,0.5,-22)
fl.BackgroundColor3=Color3.fromRGB(0,120,255)
fl.Text=D("XR")
fl.TextColor3=Color3.new(1,1,1)
fl.TextSize=14
fl.Font=Enum.Font.GothamBold
fl.Visible=false
fl.BorderSizePixel=0
fl.Parent=sg

local rc=Instance.new(D("renroC IU"))
rc.CornerRadius=UDim.new(0,8)
rc.Parent=fl

mB.MouseButton1Click:Connect(function()
    f.Visible=false
    fl.Visible=true
end)
fl.MouseButton1Click:Connect(function()
    f.Visible=true
    fl.Visible=false
end)

task.spawn(function()
    while true do
        if getgenv()._e and #ml>0 then
            local m=ml[ci]
            if m and m~="" then
                local burst=math.random(3,5)
                for _=1,burst do
                    local cnt=getgenv()._c+math.random(-5,5)
                    if cnt<1 then cnt=1 end
                    local p=string.rep(getgenv()._b,cnt).." "..(getgenv()._a~=""and"["..getgenv()._a.."] "or"")..m
                    c(p)
                    task.wait(math.random(3,10)/100)
                end
            end
            ci=(ci%#ml)+1
        end
        local wt=getgenv()._d+math.random(-5,5)/10
        if wt<0.2 then wt=0.2 end
        task.wait(wt)
    end
end)

coroutine.wrap(function()
    for i=1,30 do
        lf.Size=UDim2.new(i/30,0,1,0)
        task.wait(0.05)
    end
    lF:Destroy()
    f.Visible=true
    task.wait(0.5)
    c(D("DEDEOL 61S REMMAPS XR")) -- reversed "RX SPAMMER S16 LOADED ✅"? Actually we need to reverse "RX SPAMMER S16 LOADED ✅" but we'll include the checkmark as plain.
    c("RX SPAMMER S16 LOADED ✅") -- We'll keep this plain to avoid reversal issues
end)()
