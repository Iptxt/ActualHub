--[[
               [     Actual Hub     ]
This script is created and owned by ActualHub Developers.
Modification, redistribution, or any attempt to bypass
or crack this script is strictly prohibited.

Copyright © 2025 ActualHub Developers. All Rights Reserved.

]]--


repeat task.wait() until game:IsLoaded()

----------------------------------------------------------
------------------ [     Game List     ] -----------------
----------------------------------------------------------

--[[
    Available Options for table incase you forgot:

    Required:
        placeId = {integer}
        Url = string

    Optional:
        Name = string
        Discontinued = boolean

]]--


local GameList = {
    {
        placeId = { 3851622790, 4620170611 },
        Url = "https://raw.githubusercontent.com/Iptxt/ActualHub/refs/heads/main/BreakIn1"
    },
    {
        placeId = { 13864661000, 13864667823 },
        Url = "https://raw.githubusercontent.com/Iptxt/ActualHub/refs/heads/main/Main-Script/BreakIn2",
        Name = "BreakIn2",
    },
    {
        placeId = { 126509999114328 },
        Url = "https://raw.githubusercontent.com/Iptxt/ActualHub/refs/heads/main/99NightsInTheForest",
        Name = "99 NITF",
        Discontinued = true,
    },
    {
        placeId = { 118614517739521 },
        Url = "https://raw.githubusercontent.com/Iptxt/ActualHub/refs/heads/main/Blindshot",
        Discontinued = true,
    },
}

local UNIVERSAL_URL = "https://raw.githubusercontent.com/Iptxt/ActualHub/refs/heads/main/Main-Script/Universal"

----------------------------------------------------------
--------------- [     Selecting Game     ] ---------------
----------------------------------------------------------

local StarterGui = game:GetService("StarterGui")
local TextChatService = game:GetService("TextChatService")
local TextChannels = TextChatService:WaitForChild("TextChannels"):WaitForChild("RBXGeneral")


local function Notify(title, text)
    pcall(function()
        StarterGui:SetCore("SendNotification", {
            Title = title,
            Text = text,
            Duration = 9e9,
            Button1 = "Okay"
        })
    end)

    warn(("[ %s ] %s"):format(title, text))
end

TextChannels:DisplaySystemMessage("<font color='#FAF206'>[Actual Hub] </font>Script failed to load or error? please report it at our <font color='#FAF206'>Discord Server</font>.")

local selectedUrl

for _, list in ipairs(GameList) do
    if list.placeId and table.find(list.placeId, game.PlaceId) then
        if list.Discontinued then Notify("Discontinued", "This script is discontinued and wont receive any updates!") end
        selectedUrl = list.Url
        _G.ChoosedGame = list.Name or selectedUrl:match(".*/([^/]+)/?$")
        break
    end
end

if _G.Universal then
    _G.ChoosedGame = "Universal"
    loadstring(game:HttpGet(UNIVERSAL_URL))()
    return true
end

if selectedUrl then
    loadstring(game:HttpGet(selectedUrl))()
else
    warn("[ActualHub] - No script found for this game.")
    TextChannels:DisplaySystemMessage("<font color='#FAF206'>[Actual Hub] </font>Game Is Not Supported! Executing <font color='#FAF206'>Universal</font> script instead..")
    _G.ChoosedGame = "Universal"
    loadstring(game:HttpGet(UNIVERSAL_URL))()
end











































































































































































































































































----------------------------------------------------------
---------------- [     Discord Link     ] ----------------
----------------------------------------------------------
task.spawn(function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Iptxt/AXHub-Loader/refs/heads/main/DCLINK"))();
end)
