local DrRayLibrary = loadstring(game:HttpGet("https://raw.githubusercontent.com/AZYsGithub/DrRay-UI-Library/main/DrRay.lua"))()
local window = DrRayLibrary:Load("DrRay", "Default")



local tab = DrRayLibrary.newTab("Main", "ImageIdHere")



tab.newButton("Hide", "Prints Hello!", function()
   window:Hide()
end)

tab.newButton("color", "Prints Hello!", function()
    local mainColor = Color3.fromRGB(10, 30, 10) -- Customize as you wish; these are in RGB format. (mainColor applies to main colors like background, buttons, etc.)
local secondColor = Color3.fromRGB(50, 50, 10) -- Secondary Color; applies to Toggle when activated and slider background.
window:SetTheme(mainColor, secondColor)
end)

tab.newToggle("Toggle", "Toggle! (prints the state)", true, function(toggleState)
    if toggleState then
    local FOV = 500
game.Workspace.Camera.FieldOfView = FOV
        print("On")
    else
    local FOV = 70
game.Workspace.Camera.FieldOfView = FOV
        print("Off")
    end
end)

tab.newToggle("Toggle", "Toggle! (prints the state)", true, function(toggleState)
    if toggleState then
game.Lighting.FogEnd = 1000000
game.Lighting.FogStart = 0
game.Lighting.ClockTime = 14
game.Lighting.Brightness = 2
game.Lighting.GlobalShadows = true
        print("On")
    else
 game.Lighting.FogEnd = 1000
game.Lighting.FogStart = 0
game.Lighting.ClockTime = 14
game.Lighting.Brightness = 2
game.Lighting.GlobalShadows = true   
        print("Off")
    end
end)

tab.newButton("Button", "Prints Hello!", function()
    loadstring(game:HttpGet(('https://raw.githubusercontent.com/PrototypeRBLX/Speed-Script/main/README.md'),true))()
end)

tab.newToggle("Esp Player", "Toggle! (Function)", true, function(toggleState)
    if toggleState then
    
        print("On")
    else
    
        print("Off")
    end
end)



    window:Toggle()
    
