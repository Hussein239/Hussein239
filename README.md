-- Booting Library
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()


-- Functions
_G.Key = "Rickscript"
_G.KeyInput = "string"

function DestroyGui()
    OrionLib:Destroy()
end

function Menu()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Ggopwq/Peteryess/main/Petettop"))()
end


-- Creating Window
local Window = OrionLib:MakeWindow({Name = "مفتاح ", HidePremium = false, IntroEnabled = false})


-- Creating Tabs
local tab1 = Window:MakeTab({
 Name = "قناه التليكرام الي فيها مفتاح في صفحه ثانيه",
 Icon = "",
 PremiumOnly = false
})




-- Config Tab1
local Section1 = tab1:AddSection({
 Name = "Key"
})

tab1:AddTextbox({
 Name = "ادخل مفتاح",
 Default = "",
 TextDisappear = false,
 Callback = function(Value)
         _G.KeyInput = Value
 end   
})

tab1:AddButton({
 Name = "تأكد من مفتاح",
 Callback = function()
        if _G.KeyInput == _G.Key then
            OrionLib:MakeNotification({
         Name = "مفتاح صحيح!",
         Content = "مفتاح صحيح سكربت راح يتحمل",
         Image = "",
         Time = 1.5
            })
        wait(1.5)
        Menu()
    end
 end    
})
  
  local Tab = Window:MakeTab({
 Name = "كيف تجيب المفتاح",
 Icon = "rbxassetid://4483345998",
 PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
  
  local Section = Tab:AddSection({
 Name = "اضغط رابط وراح ينسخ لك القناه"
})

--[[
Name = <string> - The name of the section.
]]
 
 
 
 
 
 Tab:AddButton({
 Name = "رابط",
 Callback = function()
        setclipboard('https://t.me/BH_D1')
   end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
