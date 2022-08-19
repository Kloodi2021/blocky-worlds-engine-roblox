# Blocky Worlds Engine
This Is An Open-Source Free Engine That Is For Roblox, Allowing You To Make Minecraft-Inspired Games Easily.
This Read-Me File Contains The Entire Documentation For This Engine, To Make Sure You Know How To Use Everything Correctly
And Make A Good Game.

You Can Use The Built-In Functions And Guis To Get The Hang Of It.
Then You Can Make Your Game Really Feel Better By Editing This Engine.

Documentation
---
## Functions
`SetBlockyCoreGuiEnabled(coreGui:string, enabled:boolean, target:Player)` Category: Misc

Allows You To Hide/Show Blocky Core Guis Such As The Hotbar Or The Leaderboard For A Specific Player (Use '*' Or "*" For The Target To Use All Players.).
* Core Guis (Will Update)
  * Hotbar
  * Leaderboard
 ___ 
 `SendTitle(title:string, subtitle:string?, lengthInSecs:number, target:Player)` Category: Communication
 
 Allows You To Send Messages In The Center Of The Screen To A Player (Use '*' Or "*" For The Target To Use All Players.).
 ___
 `SendSystemMessage(message:string)` Category: Communication
 
 Allows You To Send System Messages In The Chat.
 
 Tutorials
 ---
 ## The Basics
 Blocky Worlds Is An Open-Source Free Engine That Is For Roblox.
 This Tutorial Will Lead You Through The Basics Of Making A Game Using
 Blocky Worlds.
 
 ### Step 1: Setup Blocky Worlds
 The First Thing You Need Is The Engine Itself,
 And Setting It Up Is As Easy As Getting It.
 There Will Be A Script That Will Have Code.
 Make Sure You Have The Command Bar Visible.
 To Setup This Engine, Run The Code In The
 Command Bar. And You're Done!
 
 ### Step 2: Make Join Messages
 Making Join Messages Is Super Easy.
 Create A Script In `ServerScriptService`.
 Edit The Script Code To Look Like This:
 ```lua
 local blockyWorlds = require(game.ReplicatedStorage.BlockyWorldsEngine)

 game:GetService("Players").PlayerAdded:Connect(function(plr)
  blockyWorlds.SendSystemMessage(plr.Name .. " joined.")
 end)
 ```
 And There You Have It!
 
 ### Step 3: Sending Titles
 If You Want To Display Credits, Alerts, And Such, Then
 You Can Use `blockyWorlds.SendTitle()`.
 Pass In The Arguments, And Then You're Done!
 You Dont Need To Use A For Loop To Call A Function For
 All Players:
 
 DO NOT DO:
 ```lua
 for _, player in game:GetService("Players"):GetChildren() do
  blockyWorlds.SendTitle("Title", "Subtitle", 1, player)
 end
 ```
 
 INSTEAD, DO:
 ```lua
 blockyWorlds.SendTitle("Title", "Subtitle", 1, "*")
 ```
 
 Using "*" Instead Of A For Loop Will Save Time And Code, Make
 Sure To Do This. (Only If Its The Same Arguments For Each Player.)
