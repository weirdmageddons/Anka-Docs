<details>
  <summary>getTiles()</summary>
   
  ```lua
  --  Returns the tiles in the world where the bot is located. [Table]

  for ,_ tile in pairs(getTiles()) do
    print(tile.fg) -- Foreground                              [int]
    print(tile.bg) -- Background                              [int]
    print(tile.isReady) -- Is ready to harvest                [bool]
    print(tile.x) -- Tile Position X                          [int]
    print(tile.y) -- Tile Position Y                          [int]
    print(tile.flags) -- Tile's flag                          [int]
    print(tile.hasExtra) -- Returns true if tile has extra    [bool]
  end
  ```
</details>

<details>
  <summary>getInventory()</summary>
     
  ```lua
  -- Returns the items in the bot's inventory. [Table]

  for ,_ item in pairs(getInventory()) do
    print(item.id) -- Item ID          [int]
    print(item.amount) -- Item amount  [int]
    print(item.name) -- Item name      [string]
  end
  ```
</details>

<details>
  <summary>getObjects()</summary>
   
  ```lua
  -- Returns the objects in the world where the bot is located. [Table]

  for ,_ object in pairs(getObjects()) do
    print(object.id) -- Object ID            [int]
    print(object.amount) -- Object amount    [int]
    print(object.x) -- Object Position X     [int]
    print(object.y) -- Object Position Y     [int]
    print(object.flags) -- Object Flags      [int]
    print(object.oid) -- Object OID          [int]
  end
  ```
</details>

<details>
  <summary>getPlayers()</summary>
   
  ```lua
  -- Returns the players in the world where the bot is located. [Table]

  for ,_ player in pairs(getPlayers()) do
    print(player.name) -- Player name        [string]
    print(player.country) -- Player Country  [string]
    print(player.netid) -- Player netID      [int]
    print(player.userid) -- Player userID    [int]
    print(player.x) -- Player Position X     [int]
    print(player.y) -- Player Position Y     [int]
  end
  ```
</details>

<details>
  <summary>getWorld()</summary>
   
  ```lua
  -- Returns information about the world where the bot is located

  print(getWorld().name) -- World name                    [string]
  print(getWorld().isJammed) -- World Public/Jammed       [bool]
  print(getWorld().width) -- World total width            [int]
  print(getWorld().height) -- World total height          [int]
  print(getWorld().tilecount) -- World total tile count   [int]
  print(getWorld().) -- []
  ```
</details>

<details>
  <summary>getLocal()</summary>
   
  ```lua
  -- Returns local information about the bot

  print(getLocal().name) -- Bot's name            [string]
  print(getLocal().status) -- Bot's game status   [string]
  print(getLocal().country) -- Bot's country      [string]
  print(getLocal().netid) -- Bot's netid          [int]
  print(getLocal().userid) -- Bot's userid        [int]
  print(getLocal().x) -- Bot's position x         [int]
  print(getLocal().y) -- Bot's position y         [int]
  print(getLocal().mac) -- Bot's mac              [string]
  print(getLocal().rid) -- Bot's rid              [string]
  print(getLocal().token) -- Bot's account token  [string]
  ```
</details>

<details>
  <summary>getTile(x, y)</summary>
   
  ```lua
  -- Returns information about a specific tile in the world where the bot is located

  print(tile.fg) -- Foreground                              [int]
  print(tile.bg) -- Background                              [int]
  print(tile.isReady) -- Is ready to harvest                [bool]
  print(tile.x) -- Tile Position X                          [int]
  print(tile.y) -- Tile Position Y                          [int]
  print(tile.flags) -- Tile's flag                          [int]
  print(tile.hasExtra) -- Returns true if tile has extra    [bool]
  ```
</details>

<details>
  <summary>getItemCount(itemID)</summary>
   
  ```lua
  -- Returns the count of a specific item in the bot's inventory

  print(getItemCount(242)) -- Item count in inventory   [int]
  ```
</details>

<details>
  <summary>connect()</summary>
   
  ```lua
  -- Connects the bot to the server.

  connect()
  ```
</details>

<details>
  <summary>disconnect()</summary>
   
  ```lua
  -- Disonnects the bot to the server.

  disconnect()
  ```
</details>

<details>
  <summary>sendPacket(packet_type, packet)</summary>
   
  ```lua
  -- Sends a text packet to the server.

  sendPacket(2, "action|respawn") -- [Param 1: int]  &  [Param 2: string]
  ```
</details>

<details>
  <summary>sendPacketRaw(packet)</summary>
   
  ```lua
  -- Sends a raw tank packet to the server

  local packet = {
    type = 1,        [int]
    objtype = 2,     [int]
    count1 = 3,      [int]
    count2 = 4,      [int]
    netid = 5,       [int]
    item = 6,        [int]
    flags = 7,       [int]
    float1 = 8,      [int]
    idata = 9,       [int]
    vecx = 10,       [int]
    vecy = 11,       [int]
    vec2x = 12,      [int]
    vec2y = 13,      [int]
    part = 14,       [int]
    int_x = 15,      [int]
    int_y = 16,      [int]
    data_size = 17   [int]
  }

  sendPacketRaw(packet)
  ```
</details>

<details>
  <summary>findPath(x, y)</summary>
   
  ```lua
  -- Moves the bot to a specified position in the world

  findPath(12, 23)   [Param 1: int]  &  [Param 2: int]
  ```
</details>

<details>
  <summary>collect(distance)</summary>
   
  ```lua
  -- Makes the bot collect items within a specified distance

  collect(3)  [int]
  ```
</details>

<details>
  <summary>enter()</summary>
   
  ```lua
  -- Makes the bot enter the door at its current position

  enter()
  ```
</details>

<details>
  <summary>punch(x, y)</summary>
   
  ```lua
  -- Makes the bot punch at a specified position

  punch(12, 23)  [Param 1: int]  &  [Param 2: int]
  ```
</details>

<details>
  <summary>place(x, y, itemid)</summary>
   
  ```lua
  -- Places a specified item at a specified position

  place(12, 23, 242)  [Param 1: int]  &  [Param 2: int]  &  [Param 3: int]
  ```
</details>

<details>
  <summary>drop(itemid, count)</summary>
   
  ```lua
  -- Drops a specified amount of a specified item

  drop(242, 1)  [Param 1: int]  &  [Param 2: int]
  ```
</details>

<details>
  <summary>warp(world_name)</summary>
   
  ```lua
  -- Warps the bot to a specified world

  warp("BUYSURG")  [string]
  ```
</details>

<details>
  <summary>trash(itemid, count)</summary>
   
  ```lua
  -- Trashes a specified amount of a specified item

  trash(242, 1)  [Param 1: int]  &  [Param 2: int]
  ```
</details>

<details>
  <summary>leaveWorld()</summary>
   
  ```lua
  -- Makes the bot leave the current world

  leaveWorld()
  ```
</details>

<details>
  <summary>wrenchPlayer(netID)</summary>
   
  ```lua
  -- Uses a wrench on a specified player by netID

  wrenchPlayer(2)  [int]
  ```
</details>

<details>
  <summary>respawn()</summary>
   
  ```lua
  -- Makes the bot respawn

  respawn()
  ```
</details>

<details>
  <summary>isInTile(x, y)</summary>
   
  ```lua
  -- Returns true if the bot's position matches the specified parameters

  if (isInTile(x, y)) then  [Param 1: int]  &  [Param 2: int]
    print("Bot in " .. x .. "," .. y)
  end
  ```
</details>

<details>
  <summary>isWearing(itemid)</summary>
   
  ```lua
  -- Returns true if the bot is wearing a specified item

  if (isWearing(itemid) then  [bool]
    unwear(itemid)
  end
  ```
</details>

<details>
  <summary>getPing()</summary>
   
  ```lua
  -- Returns the bot's ping

  print(getPing())  [int]
  ```
</details>

<details>
  <summary>getInfo(item_id)</summary>
   
  ```lua
  -- Returns information about a specified item

  local info = getInfo(242)   [int]
  print(info.name)            [string]
  print(info.editable_type)   [int]
  print(info.item_category)   [int]
  print(info.action_type)     [int]
  print(info.collision_type)  [int]
  print(info.rarity)          [int]
  print(info.grow_time)       [int]
  print(info.clothing_type)   [int]
  ```
</details>

<details>
  <summary>wear(itemid)</summary>
   
  ```lua
  -- Makes the bot wear a specified item

  wear(itemid)  [int]
  ```
</details>

<details>
  <summary>unwear(itemid)</summary>
   
  ```lua
  -- Makes the bot unwear a specified item

  unmwear(itemid)  [int]
  ```
</details>

<details>
  <summary>hasAccess(x, y)</summary>
   
  ```lua
  -- Returns true if the bot has access to a specified tile

  if (hasAccess(12, 23)) then  [Param 1: int]  &  [Param 2: int]
    punch(12, 23)
  end
  ```
</details>

<details>
  <summary>isInWorld(world_name)</summary>
   
  ```lua
  -- Returns true if the bot is in a specified world

  if (isInWorld("BUYSURGS") then  [string]
    print("Bot in BUYSURGS")
  end
  ```
</details>

<details>
  <summary>sleep(millisecond)</summary>
   
  ```lua
  -- Pauses the script for a specified delay

  print("Test")
  sleep(2000)    [int]
  print("After 2 seconds")
  ```
</details>

<details>
  <summary>say(message)</summary>
   
  ```lua
  -- Makes the bot say a specified message in the world

  say("Sell Surg Item At `3ABLU")
  ```
</details>
