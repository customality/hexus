# Hexus API Functions

> Functions exclusive to Hexus. They cannot be accessed through Roblox LocalScripts.

## getrawmetatable
Gets an object's metatable. Equivalent to getmetatable, except it ignores the __metatable field.
```lua
local mt = getrawmetatable(game)
print(mt)
```

## setrawmetatable
Sets an object's metatable. Equivalent to setmetatable, except it ignores the __metatable field.
```lua
setrawmetatable(game, {})
```

## printconsole
Prints a message to Hexus' console tab.
```lua
printconsole("Hello, World!")
```

## getgenv
Gets Hexus' environment table.
```lua
local hexus_env = getgenv()
```

## getrenv
Gets Roblox' environment table.
```lua
local roblox_env = getrenv()
```

## getreg
Gets the registry table.
```lua
local reg = getreg()
```

## setreadonly
Sets the read-only property of a table to either true or false.
```lua
local t = {}
setreadonly(t, true) --lock table
```

## checkcaller
Checks if the caller function is a function made by Hexus.
```lua
local is_hexus = checkcaller()
```

## loadstring
Attempts to compile a string and returns the function or nil and the error.
```lua
local f, err = loadstring("print('Hello, World!')")
if err then
	print(err)
else
	f()
end
```

## setclipboard
Sets the clipboard content
```lua
setclipboard("Hello, Clipboard!")
```

## mouse1press
Presses the left mouse button.
```lua
mouse1press()
```

## mouse1release
Releases the left mouse button.
```lua
mouse1release()
```

## mouse2press
Presses the right mouse button.
```lua
mouse2press()
```

## mouse2release
Releases the right mouse button.
```lua
mouse2release()
```

## keypress
Presses a key.
```lua
keypress(65) --press 'a' key
```

## keyrelease
Releases a key.
```lua
keyrelease(65) --release 'a' key
```

## debug.getmetatable
Similar to getrawmetatable, but works on all value types.
```lua
local mt = debug.getmetatable(function() end)
local mt = debug.getmetatable("Hello, World!")
```

## debug.setmetatable
Similar to setrawmetatable, but works on all value types.
```lua
debug.setmetatable("", {__index = function() return "hi" end})
print(("").IndexingWithSomeRandomKey)
```
