# Noobs
:)
function getCurrentPlayerPOS()
    local plyr = game.Players.LocalPlayer;
    if plyr.Character then
        return plyr.Character.HumanoidRootPart.Position;
    end
    return false;
end

function teleportTO(placeCFrame)
    local plyr = game.Players.LocalPlayer;
    if plyr.Character then
        plyr.Character.HumanoidRootPart.CFrame = placeCFrame;
    end
end

function teleportVent(Spot)
    if game:GetService("Workspace").OhGod:FindFirstChild(Spot) then
        teleportTO(game:GetService("Workspace").OhGod[Spot].Abyss.CFrame)
    end
end

local library = loadstring(game:HttpGet(('https://raw.githubusercontent.com/AikaV3rm/UiLib/master/Lib.lua')))()

local w = library:CreateWindow("Cameo Game 2") -- Creates the window

local a = w:CreateFolder("Trinkets") -- Creates the folder(U will put here your buttons,etc)

local b = w:CreateFolder("Vent Spots") -- Creates the folder(U will put here your buttons,etc)

a:Button("Auto Pickup",function()
    loadstring(game:HttpGet("https://pastebin.com/raw/JarWyFnr", true))()
end)

b:Button("Inari",function()
    teleportVent('VentInari')
end)

b:Button("Desert",function()
    teleportVent('VentDesert')
end)

b:Button("Citadel",function()
    teleportVent('VentCitadel')
end)

b:Button("Forge 2",function()
    teleportVent('VentForge2')
end)

b:Button("Forge Throne",function()
    teleportVent('VentForgeThrone')
end)

b:Button("Pwns",function()
    teleportVent('VentPwns')
end)

b:Button("Chromaz",function()
    teleportVent('VentChromaz')
end)

b:Button("Plains 1",function()
    teleportVent('VentPlains1')
end)

b:Button("Plains 2",function()
    teleportVent('VentPlains2')
end)

b:Button("Deepforest",function()
    teleportVent('VentDeepforest')
end)

b:Button("Petal",function()
    teleportVent('VentPetal')
end)

b:Button("Water",function()
    teleportVent('VentWater')
end)

b:Button("Ruins",function()
    teleportVent('VentRuins')
end)

b:Button("Church",function()
    teleportVent('VentChurch')
end)

b:Button("Druid",function()
    teleportVent('VentDruid')
end)

b:Button("Hoss",function()
    teleportVent('VentHoss')
end)

b:Button("Sanctuary",function()
    teleportVent('VentSanc')
end)

b:Button("Sukari",function()
    teleportVent('VentSukari')
end)

b:Button("White Fang",function()
    teleportVent('VentWhitefang')
end)

b:Button("Labratory",function()
    teleportVent('VentLab')
end)

b:Button("Horiato Coner",function()
    teleportVent('VentCorner')
end)

b:Toggle("Toggle",function(bool)
    shared.toggle = bool
    print(shared.toggle)
end)

b:Slider("Slider",{
    min = 10; -- min value of the slider
    max = 50; -- max value of the slider
    precise = true; -- max 2 decimals
},function(value)
    print(value)
end)

b:Dropdown("Dropdown",{"A","B","C"},true,function(mob) --true/false, replaces the current title "Dropdown" with the option that t
    print(mob)
end)

b:Bind("Bind",Enum.KeyCode.C,function() --Default bind
    print("Yes")
end)

b:ColorPicker("ColorPicker",Color3.fromRGB(255,0,0),function(color) --Default color
    print(color)
end)

b:Box("Box","number",function(value) -- "number" or "string"
    print(value)
end)

b:DestroyGui()
